# Zernio.Api.MessagingAdsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateCallAd**](MessagingAdsApi.md#createcallad) | **POST** /v1/ads/call | Create Click-to-Call ad |
| [**CreateCtwaAd**](MessagingAdsApi.md#createctwaad) | **POST** /v1/ads/ctwa | Create CTWA ad (deprecated) |
| [**CreateMessagingAd**](MessagingAdsApi.md#createmessagingad) | **POST** /v1/ads/messaging | Create messaging ad |

<a id="createcallad"></a>
# **CreateCallAd**
> CreateMessagingAd201Response CreateCallAd (CreateCallAdRequest createCallAdRequest, string? idempotencyKey = null)

Create Click-to-Call ad

Creates a Meta ad with a Call Now button that dials your phone number, optimized for quality calls.  Same shape and flow as POST /v1/ads/ctwa, but the CTA is CALL_NOW dialing `phoneNumber` via a tel: link. Supports the same single-creative and multi-creative shapes as CTWA.  - The ad set is destination_type PHONE_CALL optimizing QUALITY_CALL. - The campaign objective defaults to OUTCOME_LEADS.  ### Idempotency  This endpoint is not idempotent at the platform level: a blind retry creates a second campaign/ad set/ad. Send an `Idempotency-Key` header to make retries safe.  The first request with a given key creates the ad and we store the response. A retry with the same key replays that exact response (with `Idempotent-Replayed: true`) instead of creating duplicates.  - Reusing a key with a different body returns 422. - A key whose first request is still in flight returns 409 (retry after a short backoff). - If the first request is cut off mid-create (for example by a function timeout), its key can stay in progress and keep returning 409 until it expires. Use a new key to retry sooner, after checking whether the ad was created.  Keys are scoped to your credential and expire after 24h. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class CreateCallAdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MessagingAdsApi(httpClient, config, httpClientHandler);
            var createCallAdRequest = new CreateCallAdRequest(); // CreateCallAdRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  (optional) 

            try
            {
                // Create Click-to-Call ad
                CreateMessagingAd201Response result = apiInstance.CreateCallAd(createCallAdRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagingAdsApi.CreateCallAd: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCallAdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Click-to-Call ad
    ApiResponse<CreateMessagingAd201Response> response = apiInstance.CreateCallAdWithHttpInfo(createCallAdRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagingAdsApi.CreateCallAdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCallAdRequest** | [**CreateCallAdRequest**](CreateCallAdRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  | [optional]  |

### Return type

[**CreateMessagingAd201Response**](CreateMessagingAd201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Ad(s) created and submitted for review. The route shares its handler with &#x60;POST /v1/ads/ctwa&#x60;, so the body is the same tagged union discriminated by &#x60;adType&#x60;: &#x60;single&#x60; carries &#x60;{ adType, ad, message }&#x60;, and &#x60;multi&#x60; carries &#x60;{ adType, ads, platformCampaignId, platformAdSetId, message }&#x60;.  |  -  |
| **400** | Invalid input |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with one of these codes:  - &#x60;ads_allowance_exceeded&#x60;: the team has no payment method on file and has reached the 500 free live ads. Add a card to resume. - &#x60;ad_account_not_selected&#x60;: the connection has selected ad accounts and the targeted ad account is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;. - &#x60;ad_account_not_selected&#x60;, fix: add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection) or use a connection that has it selected. - &#x60;insufficient_permissions&#x60;: the Facebook user behind the connection&#39;s token lacks the Advertise permission on the Meta ad account, or the token lacks &#x60;ads_management&#x60; (Meta subcode 2490585, 2490591 or 4841020; see &#x60;ErrorResponse.details&#x60;).  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | No Facebook Page resolved for the account |  -  |
| **502** | Meta accepted the request then failed to produce the media (upload session, chunk transfer, processing timeout, or a response with no image hash). Inspect &#x60;platformError.reason&#x60;. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createctwaad"></a>
# **CreateCtwaAd**
> CreateMessagingAd201Response CreateCtwaAd (CtwaAdRequestBody ctwaAdRequestBody, string? idempotencyKey = null)

Create CTWA ad (deprecated)

Deprecated: use POST /v1/ads/messaging with `destination: whatsapp`. This endpoint stays available for back-compat; no removal planned.  Creates one or more Click-to-WhatsApp (CTWA) ads on Meta under a single campaign and ad set. When tapped, each ad opens a WhatsApp conversation with the business attached to the supplied Facebook Page.  The full hierarchy (campaign, ad set, creative(s), ad(s)) is created and activated in one call. The CTA is locked to WHATSAPP_MESSAGE and the destination is hard-coded to api.whatsapp.com/send. Meta resolves the actual WhatsApp number from the Page-to-WA pairing configured in Page settings or Business Manager.  ### Request shapes  Two mutually exclusive shapes:  - **Single-creative**: supply top-level `headline`, `body`, and one of `imageUrl` / `video`, or a `platformPostId` / `objectStoryId` reference. Creates 1 campaign + 1 ad set + 1 ad. - **Multi-creative**: supply a `creatives[]` array with N entries (each carrying fresh media and copy or an existing post reference). Creates 1 campaign + 1 ad set + N ads sharing budget and targeting.  Multi-creative lets Meta A/B the creatives inside a single auction instead of fragmenting budget across N parallel campaigns. It is recommended when launching multiple creative variants for the same campaign.  Existing posts and reels are supported through `platformPostId` (alias `existingPostId`) or `objectStoryId`, either per creative or at the top level. Omit fresh media and copy for that creative.  Optional `whatsappPhoneNumber` selects a number already paired with the Page (WhatsApp destination only).  ### Attach shape  Send `adSetId` (with either creative shape) to add the ads to an EXISTING messaging ad set instead of building a campaign. The ad set keeps its learning phase, which makes this the way to refresh a CTWA creative without resetting delivery.  The ad set then owns budget, targeting and schedule. So `budgetAmount`, `budgetType`, `endDate`, `objective`, `countries`, `interests` and `audienceId` are rejected with a 400 alongside it rather than silently dropped.  The target ad set's `destination_type` must match the ad's destination (a WhatsApp ad needs a `WHATSAPP` ad set). Otherwise Meta would accept an ad that never delivers.  ### Prerequisites  Enforced by Meta and surfaced as platform_error on failure:  - The Facebook Page must be paired with a verified WhatsApp Business number. - The WhatsApp Business Account must be business-verified. - The Meta access token must carry ads_management.  ### WhatsApp number prerequisite  Link the WhatsApp number to the Facebook Page used for the ad before creating it: Meta checks the pairing at creation. Link it from either:  - the WhatsApp Business app (Settings > Business tools > Facebook & Instagram); - the Page settings (Linked accounts > WhatsApp).  Linking does not affect the number's WhatsApp connection in Zernio (Cloud API or coexistence), so no reconnect or re-sync is needed.  If Meta creates a new ad set without the requested `whatsappPhoneNumber`, the 201 response carries a `warnings` entry. This can happen even when the number is linked (Meta can drop a Page's second linked number).  ### Idempotency  This endpoint is not idempotent at the platform level: a blind retry creates a second campaign/ad set/ad. Send an `Idempotency-Key` header to make retries safe.  - The first request with a given key creates the ad and we store the response. - A retry with the same key replays that exact response (with `Idempotent-Replayed: true`) instead of creating duplicates. - Reusing a key with a different body returns 422. - A key whose first request is still in flight returns 409 (retry after a short backoff). - If the first request is cut off mid-create (for example by a function timeout), its key can stay in progress and keep returning 409 until it expires. Use a new key to retry sooner, after checking whether the ad was created. - Keys are scoped to your credential and expire after 24h. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class CreateCtwaAdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MessagingAdsApi(httpClient, config, httpClientHandler);
            var ctwaAdRequestBody = new CtwaAdRequestBody(); // CtwaAdRequestBody | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  (optional) 

            try
            {
                // Create CTWA ad (deprecated)
                CreateMessagingAd201Response result = apiInstance.CreateCtwaAd(ctwaAdRequestBody, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagingAdsApi.CreateCtwaAd: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCtwaAdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create CTWA ad (deprecated)
    ApiResponse<CreateMessagingAd201Response> response = apiInstance.CreateCtwaAdWithHttpInfo(ctwaAdRequestBody, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagingAdsApi.CreateCtwaAdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ctwaAdRequestBody** | [**CtwaAdRequestBody**](CtwaAdRequestBody.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  | [optional]  |

### Return type

[**CreateMessagingAd201Response**](CreateMessagingAd201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | CTWA ad(s) created and submitted to Meta for review. Response is a tagged union discriminated by &#x60;adType&#x60;:  - &#x60;adType: \&quot;single\&quot;&#x60; → single-creative request: &#x60;{ adType, ad,   message }&#x60; where &#x60;ad&#x60; is the persisted Ad document. - &#x60;adType: \&quot;multi\&quot;&#x60; → multi-creative request: &#x60;{ adType, ads,   platformCampaignId, platformAdSetId, message }&#x60; where &#x60;ads&#x60; is   the array of N persisted Ad documents all sharing the returned   campaign and ad set IDs.  Generated SDK clients can narrow on &#x60;adType&#x60; instead of sniffing for field presence.  |  -  |
| **400** | Invalid body. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Forbidden. Also returned with these codes:  - &#x60;ads_allowance_exceeded&#x60;: the team has no payment method on file and has reached the 500 free live ads. Add a card to resume. - &#x60;ad_account_not_selected&#x60;: the connection has selected ad accounts and the targeted ad account is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;. - &#x60;ad_account_not_selected&#x60; fix: add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection), or use a connection that has it selected. - &#x60;insufficient_permissions&#x60;: the Facebook user behind the token lacks the Advertise permission on the Meta ad account, or the token lacks &#x60;ads_management&#x60; (Meta subcode 2490585, 2490591 or 4841020; see &#x60;ErrorResponse.details&#x60;).  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | Page is not connected to a verified WhatsApp number, or code &#x60;ad_account_unusable&#x60; when Meta refuses writes on the ad account (see &#x60;ErrorResponse.details&#x60;). |  -  |
| **502** | Meta rejected the request (e.g. WABA business verification missing). Inspect &#x60;platformError&#x60; for the upstream Meta payload.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createmessagingad"></a>
# **CreateMessagingAd**
> CreateMessagingAd200Response CreateMessagingAd (CreateMessagingAdRequest createMessagingAdRequest, string? idempotencyKey = null)

Create messaging ad

Creates a Meta ad that opens a chat with you on WhatsApp, Messenger or Instagram Direct when someone taps it.  ### Destinations  `destination` selects where the tapped ad opens a conversation:  - WhatsApp - the Page's Messenger inbox - the linked Instagram account's Direct inbox  `destinations` puts two or three of them on one ad set and lets Meta pick the app per viewer.  The ad set is created with the matching destination_type and CONVERSATIONS optimization. The campaign objective defaults to OUTCOME_ENGAGEMENT.  This endpoint supersedes POST /v1/ads/ctwa (deprecated, equivalent to `destination: whatsapp`).  ### Creatives and connections  Supports single-creative and multi-creative shapes.  - Existing posts and reels are supported through `platformPostId` (alias `existingPostId`) or `objectStoryId`, either per creative or at the top level. Omit fresh media and copy for that creative. - Optional `whatsappPhoneNumber` selects a number already paired with the Page (WhatsApp destination only). - `accountId` is a Facebook, Instagram or Meta ads (business login) connection. - `pageId` picks the Page when that connection was granted several.  ### Required fields per shape  A missing one is a 400 naming it in `param`.  - Always `accountId`, `adAccountId`, `name`, and exactly one of `destination` / `destinations`. - `budgetAmount` and `budgetType` unless `adSetId` or `existingCampaignId` is set, plus `endDate` for a lifetime budget. - Single image or video: `headline`, `body`, and exactly one of `imageUrl` / `video`. With `placementAssets`, `headline` and `body` only (the media comes from `placementAssets`). - `carouselCards`: `body` and the 2-10 cards; `headline` is optional, `imageUrl` / `video` / top-level `description` are a 400. - Existing post (`platformPostId` or `objectStoryId`): no copy or media fields. - `creatives[]`: the same rules per entry, with no top-level creative fields. - `welcomeMessage`, when sent: `text` plus exactly one of `prefillText` / `quickReplies`.  ### WhatsApp number prerequisite  For the WhatsApp destination, link the WhatsApp number to the Facebook Page used for the ad before creating it: Meta checks the pairing at creation. Link it from either:  - the WhatsApp Business app (Settings > Business tools > Facebook & Instagram) - the Page settings (Linked accounts > WhatsApp)  Linking does not affect the number's WhatsApp connection in Zernio (Cloud API or coexistence), so no reconnect or re-sync is needed.  If Meta creates a new ad set without the requested `whatsappPhoneNumber`, the 201 response carries a `warnings` entry. This can happen even when the number is linked (Meta can drop a Page's second linked number).  ### Idempotency  This endpoint is not idempotent at the platform level: a blind retry creates a second campaign/ad set/ad. Send an `Idempotency-Key` header to make retries safe.  The first request with a given key creates the ad and we store the response. A retry with the same key replays that exact response (with `Idempotent-Replayed: true`) instead of creating duplicates.  - Reusing a key with a different body returns 422. - A key whose first request is still in flight returns 409 (retry after a short backoff). - If the first request is cut off mid-create (for example by a function timeout), its key can stay in progress and keep returning 409 until it expires. Use a new key to retry sooner, after checking whether the ad was created.  Keys are scoped to your credential and expire after 24h. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class CreateMessagingAdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MessagingAdsApi(httpClient, config, httpClientHandler);
            var createMessagingAdRequest = new CreateMessagingAdRequest(); // CreateMessagingAdRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  (optional) 

            try
            {
                // Create messaging ad
                CreateMessagingAd200Response result = apiInstance.CreateMessagingAd(createMessagingAdRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagingAdsApi.CreateMessagingAd: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateMessagingAdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create messaging ad
    ApiResponse<CreateMessagingAd200Response> response = apiInstance.CreateMessagingAdWithHttpInfo(createMessagingAdRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagingAdsApi.CreateMessagingAdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createMessagingAdRequest** | [**CreateMessagingAdRequest**](CreateMessagingAdRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  | [optional]  |

### Return type

[**CreateMessagingAd200Response**](CreateMessagingAd200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | &#x60;validateOnly: true&#x60; only. Meta accepted every node; nothing was created. |  -  |
| **201** | Ad(s) created and submitted for review. The route shares its handler with &#x60;POST /v1/ads/ctwa&#x60;, so the body is the same tagged union discriminated by &#x60;adType&#x60;: &#x60;single&#x60; carries &#x60;{ adType, ad, message }&#x60;, and &#x60;multi&#x60; carries &#x60;{ adType, ads, platformCampaignId, platformAdSetId, message }&#x60;.  |  -  |
| **400** | Invalid input |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with these codes:  - &#x60;ads_allowance_exceeded&#x60;: the team has no payment method on file and has reached the 500 free live ads. Add a card to resume. - &#x60;ad_account_not_selected&#x60;: the connection has selected ad accounts and the targeted ad account is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;. - &#x60;ad_account_not_selected&#x60; fix: add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection), or use a connection that has it selected.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | No Facebook Page resolved for the account |  -  |
| **502** | Meta accepted the request then failed to produce the media (upload session, chunk transfer, processing timeout, or a response with no image hash). Inspect &#x60;platformError.reason&#x60;. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

