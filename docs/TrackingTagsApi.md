# Zernio.Api.TrackingTagsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddTrackingTagSharedAccount**](TrackingTagsApi.md#addtrackingtagsharedaccount) | **POST** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | Share with an ad account |
| [**AssignTrackingTagUser**](TrackingTagsApi.md#assigntrackingtaguser) | **POST** /v1/accounts/{accountId}/tracking-tags/{tagId}/users | Assign a user to a tag |
| [**CreateTrackingTag**](TrackingTagsApi.md#createtrackingtag) | **POST** /v1/accounts/{accountId}/tracking-tags | Create a tracking tag |
| [**CreateTrackingTagEvent**](TrackingTagsApi.md#createtrackingtagevent) | **POST** /v1/accounts/{accountId}/tracking-tags/{tagId}/events | Create a conversion event |
| [**DeleteTrackingTagEvent**](TrackingTagsApi.md#deletetrackingtagevent) | **DELETE** /v1/accounts/{accountId}/tracking-tags/{tagId}/events/{eventId} | Delete a conversion event |
| [**GetAdTrackingTags**](TrackingTagsApi.md#getadtrackingtags) | **GET** /v1/ads/{adId}/tracking-tags | Get ad tracking tags |
| [**GetTrackingTag**](TrackingTagsApi.md#gettrackingtag) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId} | Get a tracking tag |
| [**GetTrackingTagDiagnostics**](TrackingTagsApi.md#gettrackingtagdiagnostics) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/diagnostics | Get tag diagnostics |
| [**GetTrackingTagStats**](TrackingTagsApi.md#gettrackingtagstats) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/stats | Get aggregated event stats |
| [**GetTrackingTagStoreInstall**](TrackingTagsApi.md#gettrackingtagstoreinstall) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/install | Get store install status |
| [**InstallTrackingTagOnStore**](TrackingTagsApi.md#installtrackingtagonstore) | **POST** /v1/accounts/{accountId}/tracking-tags/{tagId}/install | Install on a Shopify store or WordPress site |
| [**ListTrackingTagEvents**](TrackingTagsApi.md#listtrackingtagevents) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/events | List conversion events |
| [**ListTrackingTagPartners**](TrackingTagsApi.md#listtrackingtagpartners) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/partners | List partner businesses of a tag |
| [**ListTrackingTagSharedAccounts**](TrackingTagsApi.md#listtrackingtagsharedaccounts) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | List accounts it is shared with |
| [**ListTrackingTagUsers**](TrackingTagsApi.md#listtrackingtagusers) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/users | List tag users |
| [**ListTrackingTags**](TrackingTagsApi.md#listtrackingtags) | **GET** /v1/accounts/{accountId}/tracking-tags | List tracking tags |
| [**RemoveTrackingTagFromStore**](TrackingTagsApi.md#removetrackingtagfromstore) | **DELETE** /v1/accounts/{accountId}/tracking-tags/{tagId}/install | Remove from a Shopify store or WordPress site |
| [**RemoveTrackingTagSharedAccount**](TrackingTagsApi.md#removetrackingtagsharedaccount) | **DELETE** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | Stop sharing with an account |
| [**RemoveTrackingTagUser**](TrackingTagsApi.md#removetrackingtaguser) | **DELETE** /v1/accounts/{accountId}/tracking-tags/{tagId}/users/{userId} | Remove a user from a tag |
| [**UpdateAdTrackingTags**](TrackingTagsApi.md#updateadtrackingtags) | **PATCH** /v1/ads/{adId}/tracking-tags | Set ad tracking tags |
| [**UpdateTrackingTag**](TrackingTagsApi.md#updatetrackingtag) | **PATCH** /v1/accounts/{accountId}/tracking-tags/{tagId} | Update a tracking tag |
| [**UpdateTrackingTagEvent**](TrackingTagsApi.md#updatetrackingtagevent) | **PATCH** /v1/accounts/{accountId}/tracking-tags/{tagId}/events/{eventId} | Update a conversion event |

<a id="addtrackingtagsharedaccount"></a>
# **AddTrackingTagSharedAccount**
> AddTrackingTagSharedAccount201Response AddTrackingTagSharedAccount (string accountId, string tagId, AddTrackingTagSharedAccountRequest addTrackingTagSharedAccountRequest)

Share with an ad account

Shares the pixel with another ad account so campaigns/audiences in that account can use it. Requires that you administer both the pixel's owning Business Manager and the target ad account; a pixel on a personal (non-BM) ad account can't be shared (Meta will reject the call). Meta and LinkedIn; other platforms return 501.  LinkedIn (`linkedinads`): grants `USE_ONLY` access from the ad account that created the tag, so the target can use the tag and its conversions but cannot edit or reshare it. `adAccountId` is the numeric LinkedIn ad account id. An ad account uses one Insight Tag at a time, so a target that already has one answers 400.  TikTok: links the pixel to an advertiser through Business Center (`/bc/pixel/link/update/`, `adAccountId` = numeric advertiser_id). Only a pixel that is an asset of a Business Center this connection manages can be shared; otherwise the answer is 400 asking to transfer it to Business Center first. 

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
    public class AddTrackingTagSharedAccountExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.
            var addTrackingTagSharedAccountRequest = new AddTrackingTagSharedAccountRequest(); // AddTrackingTagSharedAccountRequest | 

            try
            {
                // Share with an ad account
                AddTrackingTagSharedAccount201Response result = apiInstance.AddTrackingTagSharedAccount(accountId, tagId, addTrackingTagSharedAccountRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.AddTrackingTagSharedAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddTrackingTagSharedAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Share with an ad account
    ApiResponse<AddTrackingTagSharedAccount201Response> response = apiInstance.AddTrackingTagSharedAccountWithHttpInfo(accountId, tagId, addTrackingTagSharedAccountRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.AddTrackingTagSharedAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |
| **addTrackingTagSharedAccountRequest** | [**AddTrackingTagSharedAccountRequest**](AddTrackingTagSharedAccountRequest.md) |  |  |

### Return type

[**AddTrackingTagSharedAccount201Response**](AddTrackingTagSharedAccount201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Tracking tag shared with the ad account |  -  |
| **400** | Invalid body / &#x60;adAccountId&#x60;, or Meta rejected the share (e.g. personal ad account). |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="assigntrackingtaguser"></a>
# **AssignTrackingTagUser**
> AssignTrackingTagUser200Response AssignTrackingTagUser (string accountId, string tagId, AssignTrackingTagUserRequest assignTrackingTagUserRequest)

Assign a user to a tag

Gives a user of the owning business access to the tag. Assigning an already assigned user replaces their task set.  Meta: `tasks` are `AA_ANALYZE`, `ADVERTISE`, `ANALYZE`, `EDIT`, `UPLOAD`; `userId` is the business-scoped id from `GET /v1/ads/businesses/users`. A pixel on a personal ad account answers 400. Needs `business_management` like the list. 

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
    public class AssignTrackingTagUserExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var assignTrackingTagUserRequest = new AssignTrackingTagUserRequest(); // AssignTrackingTagUserRequest | 

            try
            {
                // Assign a user to a tag
                AssignTrackingTagUser200Response result = apiInstance.AssignTrackingTagUser(accountId, tagId, assignTrackingTagUserRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.AssignTrackingTagUser: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AssignTrackingTagUserWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Assign a user to a tag
    ApiResponse<AssignTrackingTagUser200Response> response = apiInstance.AssignTrackingTagUserWithHttpInfo(accountId, tagId, assignTrackingTagUserRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.AssignTrackingTagUserWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **assignTrackingTagUserRequest** | [**AssignTrackingTagUserRequest**](AssignTrackingTagUserRequest.md) |  |  |

### Return type

[**AssignTrackingTagUser200Response**](AssignTrackingTagUser200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User assigned |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the platform token lacks the permission (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform has no tag user assignment (code &#x60;platform_not_supported&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createtrackingtag"></a>
# **CreateTrackingTag**
> CreateTrackingTag201Response CreateTrackingTag (string accountId, CreateTrackingTagRequest createTrackingTagRequest)

Create a tracking tag

Meta: creates a Meta Pixel on the given ad account (`POST /act_{id}/adspixels`, where `name` is the only input). Returns the created tag including its install `code`. The pixel is owned by the Business Manager that owns the ad account; a pixel created on a personal (non-BM) ad account ends up with `ownerBusinessId: null` and can't be shared with other ad accounts.  Creating a Meta pixel does NOT install it. Install the returned `code` snippet on the site, or send events server-side via `POST /v1/ads/conversions`. The check `installed` is derived from `lastFiredTime`.  OpenAI Ads: creates an OpenAI pixel AND provisions a Conversions API key for it in the same call (`adAccountId` is required by this endpoint but ignored: one API key maps to exactly one ad account, so there's nothing to select). Returns 422 (`FEATURE_NOT_AVAILABLE`) if the ad account isn't enabled for pixel management; contact your OpenAI partner representative to enable it. There is no delete API for OpenAI pixels. If the pixel is created but the Conversions API key provisioning then fails, the pixel is left live on OpenAI (it cannot be cleaned up) and the error message names the surviving pixel id and warns against retrying, since a retry would create a second, orphaned pixel.  NOT idempotent on either platform: each call creates a new pixel (and, for OpenAI, a new Conversions API key plus, with `defaultEventType`, a new conversion event setting). Do not retry blindly on timeout. Meta (platform `metaads`) and OpenAI Ads (platform `openaiads`); other platforms return 501.  LinkedIn (`linkedinads`): creates the ad account's Insight Tag (`POST /rest/insightTags`). Idempotent: an ad account holds at most one Insight Tag, so when it already has one that tag is returned and nothing is created. `name` is ignored (LinkedIn tags have no name) and there is no API to delete an Insight Tag.  Pinterest (platform `pinterestads`): creates a Pinterest tag on the numeric ad account `adAccountId` (`POST /v5/ad_accounts/{id}/conversion_tags`). Returns the tag with Pinterest's `code` snippet. `automaticMatchingFields` switches on automatic enhanced match for those fields. NOT idempotent and Pinterest has no dry-run and no delete for tags (DELETE on `conversion_tags/{id}` answers 405), so never retry blindly: list first.  Google Ads (`googleads`): every Google Ads account has exactly one Google tag (`AW-...`), so this is idempotent. `adAccountId` is the 10-digit customer id. When the account already tracks conversions the existing tag is returned (201) and nothing is created. Otherwise a first WEBPAGE conversion action named `name` (category DEFAULT) is created, which is what switches Google's conversion tracking on, and the tag is returned with it as its first event.  TikTok: `POST /pixel/create/` on the advertiser in `adAccountId` (numeric). Names are at most 40 characters with no emoji and must be unique; TikTok refuses a duplicate name (400), which is its only retry guard. TikTok has no pixel delete API. 

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
    public class CreateTrackingTagExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Ads SocialAccount id (platform `metaads` or `openaiads`).
            var createTrackingTagRequest = new CreateTrackingTagRequest(); // CreateTrackingTagRequest | 

            try
            {
                // Create a tracking tag
                CreateTrackingTag201Response result = apiInstance.CreateTrackingTag(accountId, createTrackingTagRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.CreateTrackingTag: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTrackingTagWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a tracking tag
    ApiResponse<CreateTrackingTag201Response> response = apiInstance.CreateTrackingTagWithHttpInfo(accountId, createTrackingTagRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.CreateTrackingTagWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Ads SocialAccount id (platform &#x60;metaads&#x60; or &#x60;openaiads&#x60;). |  |
| **createTrackingTagRequest** | [**CreateTrackingTagRequest**](CreateTrackingTagRequest.md) |  |  |

### Return type

[**CreateTrackingTag201Response**](CreateTrackingTag201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Tracking tag created |  -  |
| **400** | Invalid body, invalid &#x60;adAccountId&#x60;, over the per-business pixel cap, or ad account not in a Business Manager. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | OpenAI Ads only: the ad account is not enabled for pixel management. Contact your OpenAI partner representative. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Creating a pixel is NOT idempotent, so before retrying confirm with GET /v1/accounts/{accountId}/tracking-tags that no pixel was created. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createtrackingtagevent"></a>
# **CreateTrackingTagEvent**
> CreateTrackingTagEvent201Response CreateTrackingTagEvent (string accountId, string tagId, CreateTrackingTagEventRequest createTrackingTagEventRequest)

Create a conversion event

Creates a conversion event tied to the tag. Pass the platform's own event type in `type` (e.g. Google `PURCHASE`, LinkedIn `ADD_TO_CART`, X `CHECKOUT_INITIATED`) or a neutral `siteEvent` the platform maps to its closest type. Each platform stores a subset of the optional fields; sending one it does not store answers 400 naming the supported fields. NOT idempotent unless noted per platform: do not retry blindly.  OpenAI Ads: creates a conversion event setting on the pixel (`POST /conversions/event_settings`, source = the pixel). Accepts `name`, `type` and `siteEvent` only. `type` is a standard event (`order_created`, `lead_created`, `items_added`, `contents_viewed`, `checkout_started`, `registration_completed`, `subscription_created`, `trial_started`, `appointment_scheduled`, `page_viewed`, `app_installed`, `app_opened`) or, for anything else, the custom event name itself (1 to 64 letters, digits, underscores or dashes; stored lowercase). `siteEvent` maps `search` and `add_payment_info` to the custom events `search` and `addpaymentinfo`, the names Zernio's Shopify pixel sends. The click attribution window is 30 days, the only value OpenAI documents. Only standard events can be a conversions campaign's optimization goal.  LinkedIn (`linkedinads`): creates an event-specific Insight Tag conversion rule (no URL match rules), the kind a page or the Shopify pixel fires by id. `type` is a LinkedIn conversion type (e.g. `PURCHASE`, `ADD_TO_CART`, `START_CHECKOUT`, `LEAD`); `siteEvent` maps to `KEY_PAGE_VIEW`, `VIEW_CONTENT`, `ADD_TO_CART`, `SEARCH`, `START_CHECKOUT`, `ADD_BILLING_INFO` or `PURCHASE`. `defaultValue` needs `currency` (the ad account currency) and is a fallback: a value sent with the event wins. Click and view windows are in days (LinkedIn validates them: the docs list 1, 7 and 30, and rules with 90 exist). Stores name, type, siteEvent, enabled, defaultValue, currency, clickWindowDays, viewWindowDays. Not idempotent.  Meta: creates a custom conversion on `adAccountId` (default: the pixel's owner ad account). Accepts `name`, `type` (Meta `custom_event_type`: `PURCHASE`, `LEAD`, `ADD_TO_CART`, `COMPLETE_REGISTRATION`, `OTHER`...), `siteEvent`, `urlContains` and `defaultValue` (in the ad account currency). The rule matches the standard event of `siteEvent` (or of `type`), plus `urlContains` when given; `urlContains` alone matches page views on that URL. `type: OTHER` needs `siteEvent` or `urlContains`. Idempotent by name: an active conversion with the same name on this pixel is returned instead of a duplicate. Meta caps custom conversions per ad account; the cap answers 400.  Google Ads (`googleads`): creates a WEBPAGE conversion action. `type` is a ConversionActionCategory (e.g. `PURCHASE`, `SIGNUP`, `DEFAULT`); `siteEvent` maps page_view, add_to_cart, initiate_checkout and purchase, while view_content, search and add_payment_info answer 400 (Google has no category for them). Stored fields: name, type, defaultValue, currency, alwaysUseDefaultValue, clickWindowDays (1 to 90), viewWindowDays (1 to 30), primary, countingType, enabled. Actions are created enabled (`enabled: false` answers 400); Google blocks the HIDDEN status on WEBPAGE actions. Names are unique per account, so a replay answers 400 (DUPLICATE_NAME) instead of creating a second one.  Pinterest (platform `pinterestads`): creates an advertiser defined event on the tag's ad account. Fields: `name` (1-100 letters, digits, `_` or `-`, case-insensitive, max 15 per ad account) and `type` (one of Pinterest's optimizable types: SIGNUP, ADD_TO_CART, LEAD, CHECKOUT, SUBSCRIBE, ADD_TO_WISHLIST, ADD_PAYMENT_INFO, INITIATE_CHECKOUT, CONTACT, CUSTOMIZE_PRODUCT, FIND_LOCATION, SCHEDULE, SUBMIT_APPLICATION, START_TRIAL, PAGE_VISIT, VIEW_CATEGORY, VIEW_CONTENT, SEARCH, WATCH_VIDEO) or `siteEvent`. A duplicate name answers 400.  TikTok: `POST /pixel/event/create/`. `type` is a TikTok pixel event type (SHOPPING, ON_WEB_CART, ON_WEB_DETAIL, INITIATE_ORDER, ADD_BILLING, ON_WEB_SEARCH, PAGE_VIEW, ON_WEB_REGISTER, FORM, ...), or pass `siteEvent`. Stores `name` (at most 40 characters), `defaultValue` and `currency` (USD, JPY or INR only). TikTok returns no id: the new event is read back from the pixel, and while TikTok's listing has not refreshed the response carries an empty `id` and `status: pending`. 

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
    public class CreateTrackingTagEventExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var createTrackingTagEventRequest = new CreateTrackingTagEventRequest(); // CreateTrackingTagEventRequest | 

            try
            {
                // Create a conversion event
                CreateTrackingTagEvent201Response result = apiInstance.CreateTrackingTagEvent(accountId, tagId, createTrackingTagEventRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.CreateTrackingTagEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTrackingTagEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a conversion event
    ApiResponse<CreateTrackingTagEvent201Response> response = apiInstance.CreateTrackingTagEventWithHttpInfo(accountId, tagId, createTrackingTagEventRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.CreateTrackingTagEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **createTrackingTagEventRequest** | [**CreateTrackingTagEventRequest**](CreateTrackingTagEventRequest.md) |  |  |

### Return type

[**CreateTrackingTagEvent201Response**](CreateTrackingTagEvent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Conversion event created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the platform token lacks the permission (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform cannot create conversion events through its API (code &#x60;platform_not_supported&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletetrackingtagevent"></a>
# **DeleteTrackingTagEvent**
> DeleteTrackingTagEvent200Response DeleteTrackingTagEvent (string accountId, string tagId, string eventId, string? adAccountId = null)

Delete a conversion event

Removes the conversion event. Platforms without a hard delete archive or disable it instead; `state` in the response says which (`deleted`, `archived`, `disabled`).  OpenAI Ads answers 501: there is no delete or archive route for event settings (`DELETE /v1/conversions/event_settings/{id}` and `POST .../{id}/archive` answer 404 \"Invalid URL\"). Archive the event in OpenAI Ads Manager.  LinkedIn (`linkedinads`): LinkedIn has no delete for conversion rules (not in the conversion-tracking API, and `DELETE /rest/conversions/{id}` has no route), so the rule is disabled (`enabled: false`) and `state` is `disabled`. Re-enable it with `enabled: true`.  Meta: `archived`. Meta's delete archives the custom conversion (it stays readable with `status: archived`) and there is no hard delete; deleting an archived one is a no-op.  Google Ads (`googleads`): removes the conversion action (state `archived`). Google keeps it with status REMOVED and its history; PATCH with `enabled: true` restores it. Deleting an already archived action succeeds without a call to Google.  Pinterest (platform `pinterestads`): stops Pinterest tracking the event name (`state: disabled`); Pinterest keeps the event's history.  TikTok: hard delete (`/pixel/event/delete/`); TikTok refuses events bound to an ad group (400). 

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
    public class DeleteTrackingTagEventExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | 
            var eventId = "eventId_example";  // string | Event id (`TrackingTagEvent.id`).
            var adAccountId = "adAccountId_example";  // string? | Scopes the lookup on platforms whose tag ids live inside an ad account. (optional) 

            try
            {
                // Delete a conversion event
                DeleteTrackingTagEvent200Response result = apiInstance.DeleteTrackingTagEvent(accountId, tagId, eventId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.DeleteTrackingTagEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTrackingTagEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a conversion event
    ApiResponse<DeleteTrackingTagEvent200Response> response = apiInstance.DeleteTrackingTagEventWithHttpInfo(accountId, tagId, eventId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.DeleteTrackingTagEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** |  |  |
| **eventId** | **string** | Event id (&#x60;TrackingTagEvent.id&#x60;). |  |
| **adAccountId** | **string?** | Scopes the lookup on platforms whose tag ids live inside an ad account. | [optional]  |

### Return type

[**DeleteTrackingTagEvent200Response**](DeleteTrackingTagEvent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Conversion event removed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the platform token lacks the permission (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform cannot remove conversion events through its API (code &#x60;platform_not_supported&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadtrackingtags"></a>
# **GetAdTrackingTags**
> GetAdTrackingTags200Response GetAdTrackingTags (string adId)

Get ad tracking tags

Unified read of the platform's native click-URL tracking params. - Meta (facebook/instagram): the creative's `url_tags` (and template_url_spec). - Google (googleads): the campaign's `trackingUrlTemplate` + `finalUrlSuffix`. - LinkedIn (linkedinads): the campaign's Dynamic UTM `dynamicValueParameters` + `customValueParameters`. Returns 405 for platforms without a click-URL tracking surface (TikTok, X, Pinterest).  **Not pixels.** Despite the shared path segment, this endpoint has nothing to do with measurement tags. For an ad account's pixels use `GET /v1/accounts/{accountId}/tracking-tags?adAccountId=act_...` (Meta Pixels, with `kind` and `ownerAdAccountId`) or `GET /v1/accounts/{accountId}/conversion-destinations`. 

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
    public class GetAdTrackingTagsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Ad id (hex _id, platformAdId, or effective story/media id).

            try
            {
                // Get ad tracking tags
                GetAdTrackingTags200Response result = apiInstance.GetAdTrackingTags(adId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.GetAdTrackingTags: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdTrackingTagsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get ad tracking tags
    ApiResponse<GetAdTrackingTags200Response> response = apiInstance.GetAdTrackingTagsWithHttpInfo(adId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.GetAdTrackingTagsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Ad id (hex _id, platformAdId, or effective story/media id). |  |

### Return type

[**GetAdTrackingTags200Response**](GetAdTrackingTags200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tracking tags for the ad&#39;s platform (shape varies by platform). |  -  |
| **401** | Unauthorized |  -  |
| **404** | Ad not found |  -  |
| **405** | Platform has no click-URL tracking surface |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettrackingtag"></a>
# **GetTrackingTag**
> GetTrackingTag200Response GetTrackingTag (string accountId, string tagId, string? adAccountId = null)

Get a tracking tag

Returns the full tag record including the base-code `code` snippet, `lastFiredTime`, `ownerBusinessId`, `isUnavailable`, etc. Meta only (platform `metaads`); other platforms return 501.  OpenAI Ads (`openaiads`): `tagId` is the pixel's API id (`cds_...`) or its `pixel_id`. OpenAI documents no single-pixel read, so the tag is resolved from the pixel list; the response adds `code` (the official `oaiq` base code plus `page_viewed`) and `events` (the conversion event settings whose source is this pixel). `siteTagId` is the `pixel_id` the site and the Conversions API send; `id` is what event settings reference.  LinkedIn (`linkedinads`): `code` is LinkedIn's base code, `lastFiredTime` is the most recent callback across the tag's domains (unix seconds, null when it never fired) and `events` lists the ad account's conversion rules. `siteEvent` and `siteEventId` are set only on rules a page can fire (event-specific Insight Tag rules: not Conversions API rules, no URL match rules). `adAccountId` picks which ad account's rules to read; it defaults to the account that created the tag.  Pinterest (platform `pinterestads`): returns the tag with Pinterest's own `code` snippet and `lastFiredTime`. Without `adAccountId` Zernio finds the ad account that owns the tag (404 when no readable ad account holds it).  TikTok: read from `/pixel/list/?pixel_id=`; `code` is TikTok's `pixel_script`, `events` the pixel events. `lastFiredTime` is not available on TikTok. Without `adAccountId` the connection's advertisers are searched. 

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
    public class GetTrackingTagExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var adAccountId = "adAccountId_example";  // string? | Scopes the lookup on platforms whose tag ids live inside an ad account. Ignored elsewhere. (optional) 

            try
            {
                // Get a tracking tag
                GetTrackingTag200Response result = apiInstance.GetTrackingTag(accountId, tagId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTag: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTrackingTagWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a tracking tag
    ApiResponse<GetTrackingTag200Response> response = apiInstance.GetTrackingTagWithHttpInfo(accountId, tagId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **adAccountId** | **string?** | Scopes the lookup on platforms whose tag ids live inside an ad account. Ignored elsewhere. | [optional]  |

### Return type

[**GetTrackingTag200Response**](GetTrackingTag200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tracking tag fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettrackingtagdiagnostics"></a>
# **GetTrackingTagDiagnostics**
> GetTrackingTagDiagnostics200Response GetTrackingTagDiagnostics (string accountId, string tagId)

Get tag diagnostics

The platform's health checks for the tag. Platforms without tag diagnostics answer 501.  Meta: the pixel's checks from Events Manager (`da_checks`), e.g. whether events miss parameters or their content ids do not match the pixel's catalogs. 

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
    public class GetTrackingTagDiagnosticsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).

            try
            {
                // Get tag diagnostics
                GetTrackingTagDiagnostics200Response result = apiInstance.GetTrackingTagDiagnostics(accountId, tagId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagDiagnostics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTrackingTagDiagnosticsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get tag diagnostics
    ApiResponse<GetTrackingTagDiagnostics200Response> response = apiInstance.GetTrackingTagDiagnosticsWithHttpInfo(accountId, tagId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagDiagnosticsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |

### Return type

[**GetTrackingTagDiagnostics200Response**](GetTrackingTagDiagnostics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Diagnostics fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the platform token lacks the permission (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform has no tag diagnostics (code &#x60;platform_not_supported&#x60;). |  -  |
| **502** | The platform was unreachable or returned an unclassified error (type: platform_error). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettrackingtagstats"></a>
# **GetTrackingTagStats**
> GetTrackingTagStats200Response GetTrackingTagStats (string accountId, string tagId, string? adAccountId = null, string? aggregation = null, int? startTime = null, int? endTime = null)

Get aggregated event stats

Returns event counts / health for the tag, where the platform exposes them. Meta: aggregated counts (`GET /{pixel_id}/stats`), rows passed through as-is; their shape depends on the `aggregation` requested. Platforms without a stats API answer 501.  OpenAI Ads: the recent-events stream (`GET /conversions/events`), the latest (at most 50) Pixel SDK events received in the last 15 minutes, one row per event (`event_type`, `api_channel`, `event_timestamp_ms`, `received_at_ms`, ...). Conversions API events are not included. It is a fixed window: `startTime`/`endTime` answer 400. Use it to confirm an install fires; attributed totals come from ads analytics. Accounts not enabled for the stream answer 422 `feature_not_available`.  LinkedIn (`linkedinads`): health rows rather than counts, since LinkedIn exposes no per- event fire counts: one row per site domain the tag has seen (`kind: domain`, `domainName`, `lastFiredTime`, `creationTime`, `blocked`) and one per conversion rule (`kind: conversion_rule`, `id`, `name`, `type`, `conversionMethod`, `status`, `lastFiredTime`). Times are unix seconds; `startTime`/`endTime` are ignored.  Pinterest (platform `pinterestads`): rows typed by `type`: one `tag` row (`lastFiredTime`, `status`, `enhancedMatchStatus`), `event` rows for the conversion events Pinterest has seen on the tag (`source` is `page_visit` or `ocpm_eligible`, the latter meaning the event can be optimized for, with the neutral `siteEvent` where one maps), and `event_quality` rows with the ad account's Event Quality Score for tag events over the last `1d` and `14d` (ad-account level, not per tag; an account Pinterest cannot score yet carries `error` instead). Pinterest has no time-bounded counts, so `startTime`/`endTime` answer 400.  TikTok: per-event counts from `/pixel/event/stats/` (`total_count`, `browser_event_total_count`, `server_event_total_count`, `attributed_count`, `preview_count`), bucketed by UTC day. Defaults to the last 7 days; at most 30 days per request. `aggregation` is not accepted. 

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
    public class GetTrackingTagStatsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var adAccountId = "adAccountId_example";  // string? | Scopes the lookup on platforms whose tag ids live inside an ad account. Ignored elsewhere. (optional) 
            var aggregation = "event";  // string? | Meta only (400 on other platforms): aggregation dimension. Defaults to `event`. (optional)  (default to event)
            var startTime = 56;  // int? | Unix seconds lower bound. (optional) 
            var endTime = 56;  // int? | Unix seconds upper bound. (optional) 

            try
            {
                // Get aggregated event stats
                GetTrackingTagStats200Response result = apiInstance.GetTrackingTagStats(accountId, tagId, adAccountId, aggregation, startTime, endTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagStats: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTrackingTagStatsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get aggregated event stats
    ApiResponse<GetTrackingTagStats200Response> response = apiInstance.GetTrackingTagStatsWithHttpInfo(accountId, tagId, adAccountId, aggregation, startTime, endTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagStatsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **adAccountId** | **string?** | Scopes the lookup on platforms whose tag ids live inside an ad account. Ignored elsewhere. | [optional]  |
| **aggregation** | **string?** | Meta only (400 on other platforms): aggregation dimension. Defaults to &#x60;event&#x60;. | [optional] [default to event] |
| **startTime** | **int?** | Unix seconds lower bound. | [optional]  |
| **endTime** | **int?** | Unix seconds upper bound. | [optional]  |

### Return type

[**GetTrackingTagStats200Response**](GetTrackingTagStats200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Stats fetched |  -  |
| **400** | Invalid query parameter. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettrackingtagstoreinstall"></a>
# **GetTrackingTagStoreInstall**
> GetTrackingTagStoreInstall200Response GetTrackingTagStoreInstall (string accountId, string tagId, string storeAccountId, string? adAccountId = null)

Get store install status

Whether this tag is the one the Shopify store fires for its platform. `installedTagId` names the tag of that platform the store currently fires, which can be a different tag, and `tags` lists every Zernio tag on the store (all platforms).  WordPress: whether the Zernio widget for this pixel is live (in an active widget area, script intact), plus a read-only `preflight` with the theme's widget areas and, when an install would be blocked, the `reason` POST would return. The preflight reads capabilities only, so `ready: true` is not a guarantee: `DISALLOW_UNFILTERED_HTML` or a multisite admin who is not a Super Admin still strips the script, which POST detects. `tags` lists every Zernio widget on the site (all platforms, with `active`). 

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
    public class GetTrackingTagStoreInstallExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var storeAccountId = "storeAccountId_example";  // string | The connected Shopify or WordPress account id.
            var adAccountId = "adAccountId_example";  // string? | Scopes the tag lookup on platforms whose tag ids live inside an ad account. (optional) 

            try
            {
                // Get store install status
                GetTrackingTagStoreInstall200Response result = apiInstance.GetTrackingTagStoreInstall(accountId, tagId, storeAccountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagStoreInstall: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTrackingTagStoreInstallWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get store install status
    ApiResponse<GetTrackingTagStoreInstall200Response> response = apiInstance.GetTrackingTagStoreInstallWithHttpInfo(accountId, tagId, storeAccountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagStoreInstallWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **storeAccountId** | **string** | The connected Shopify or WordPress account id. |  |
| **adAccountId** | **string?** | Scopes the tag lookup on platforms whose tag ids live inside an ad account. | [optional]  |

### Return type

[**GetTrackingTagStoreInstall200Response**](GetTrackingTagStoreInstall200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Install status |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The store must re-approve the Zernio Shopify app to grant pixel access (code &#x60;reconnect_required&#x60;). Send the merchant to &#x60;details.authUrl&#x60;; the Shopify account id stays the same. Also returned while the store account itself needs reconnection (code &#x60;ads_connection_required&#x60;). |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="installtrackingtagonstore"></a>
# **InstallTrackingTagOnStore**
> InstallTrackingTagOnStore200Response InstallTrackingTagOnStore (string accountId, string tagId, InstallTrackingTagOnStoreRequest installTrackingTagOnStoreRequest)

Install on a Shopify store or WordPress site

Puts the Meta pixel on a connected Shopify store's storefront and checkout through Zernio's Shopify web pixel (a Shopify app pixel, no theme edits). The store then sends PageView, ViewContent, AddToCart, Search, InitiateCheckout, AddPaymentInfo and Purchase (with value, currency, content_ids and contents) to the pixel, each with an event id. Purchase uses `shopify_order_{orderId}` as its event id, so a Conversions API Purchase you send for the same order with that `eventId` is deduplicated by Meta.  Idempotent: a store runs one Zernio web pixel holding one tag per platform, so calling it again updates the install, installing a different tag of the same platform replaces the previous one (reported in `replacedTagId`), and other platforms' tags are kept. Events respect the store's customer privacy settings (marketing consent).  `accountId` is the Meta ads account that owns the pixel (`tagId`); `storeAccountId` is the Shopify account.  OpenAI Ads on Shopify: each event is sent through OpenAI's documented image tag (`GET https://bzr.openai.com/v1/sdk/events`) as `page_viewed`, `contents_viewed`, `items_added`, `checkout_started`, `order_created`, and custom events `search` and `addpaymentinfo` (lowercase, so a Conversions API Search/AddPaymentInfo with the same event id deduplicates). Amounts are sent in the currency's minor unit. The landing page's `oppref` click id is kept in the `__oppref` cookie for 30 days and sent with every event. The image tag cannot carry the `__obref` browser id (OpenAI rejects the parameter), and the search text is never sent. On WordPress the widget holds the official `oaiq` base code and a `page_viewed` call.  Stores connected before pixel support must re-approve the Zernio app: the call then answers 409 `reconnect_required` with `details.authUrl` to send the merchant to (the Shopify account id stays the same). Platforms without an install path return 501.  **WordPress** (`storeAccountId` is a connected WordPress.com or self-hosted site): Zernio adds a Custom HTML widget with the Meta pixel base code (fbevents.js, `init`, `PageView`) to a widget area of the active theme (a footer area when there is one, else the first active area; pass `sidebarId` to choose), then reads the widget back to confirm WordPress kept the `<script>` tag. The widget carries a Zernio marker, so the call is idempotent per pixel: repeating it updates or moves the same widget, and pixel code the site owner pasted by hand is never touched. Several pixels can run side by side (one widget each). When the site cannot run the pixel, nothing is left behind and the call answers 422 `tracking_tag_install_blocked` with `details.reason`: - `insufficient_permissions`: the connected user lacks `edit_theme_options` (needs Administrator). - `scripts_stripped`: WordPress removed the script (the user lacks `unfiltered_html`, e.g. a multisite admin who is not a Super Admin, or `DISALLOW_UNFILTERED_HTML` is set). - `wordpress_com_plan`: a WordPress.com plan that strips scripts (plans without plugins). - `no_widget_areas`: the theme has no widget areas (block themes such as Twenty Twenty-Five). - `widgets_api_unavailable`: no widgets REST API (WordPress older than 5.8, or disabled). The `error` message names the manual alternative (Meta's official WordPress plugin). With `verifyHomepage` (default true) the homepage is fetched afterwards and `homepageCheck` says whether the pixel is visible; `not_found` can be a stale page cache, the widget read-back is authoritative.  **LinkedIn** (`linkedinads`): Shopify sends every page view to the Insight Tag, plus each store event that has an enabled event-specific Insight Tag conversion rule of the matching type (view_content = VIEW_CONTENT, add_to_cart = ADD_TO_CART, search = SEARCH, initiate_checkout = START_CHECKOUT, add_payment_info = ADD_BILLING_INFO, purchase = PURCHASE). Each conversion carries the event id; Purchase uses `shopify_order_{orderId}`, so a Conversions API event sent to a separate CONVERSIONS_API rule with that `eventId` is deduplicated by LinkedIn. Conversions API rules cannot be fired from a page, and no rule is created for you. The `li_fat_id` click id is read from the landing URL and kept in a first-party cookie for 30 days. WordPress gets LinkedIn's base code, which records page views.  **Pinterest (platform `pinterestads`)**: Shopify sends `pagevisit`, `viewcontent`, `addtocart`, `search`, `initiatecheckout`, `addpaymentinfo` and `checkout` to the tag, each with `event_id` (Purchase: `shopify_order_{orderId}`, for dedup with the Pinterest Conversions API), value, currency, order quantity and line items, plus the `epik` click id kept in the `_epik` cookie. WordPress gets Pinterest's base code (core.js, `load`, `page`) with a `pagevisit` event; the manual fallback is the official Pinterest for WooCommerce plugin (WooCommerce stores). 

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
    public class InstallTrackingTagOnStoreExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var installTrackingTagOnStoreRequest = new InstallTrackingTagOnStoreRequest(); // InstallTrackingTagOnStoreRequest | 

            try
            {
                // Install on a Shopify store or WordPress site
                InstallTrackingTagOnStore200Response result = apiInstance.InstallTrackingTagOnStore(accountId, tagId, installTrackingTagOnStoreRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.InstallTrackingTagOnStore: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the InstallTrackingTagOnStoreWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Install on a Shopify store or WordPress site
    ApiResponse<InstallTrackingTagOnStore200Response> response = apiInstance.InstallTrackingTagOnStoreWithHttpInfo(accountId, tagId, installTrackingTagOnStoreRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.InstallTrackingTagOnStoreWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **installTrackingTagOnStoreRequest** | [**InstallTrackingTagOnStoreRequest**](InstallTrackingTagOnStoreRequest.md) |  |  |

### Return type

[**InstallTrackingTagOnStore200Response**](InstallTrackingTagOnStore200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pixel installed on the store |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The store must re-approve the Zernio Shopify app to grant pixel access (code &#x60;reconnect_required&#x60;). Send the merchant to &#x60;details.authUrl&#x60;; the Shopify account id stays the same. Also returned while the store account itself needs reconnection (code &#x60;ads_connection_required&#x60;). |  -  |
| **422** | WordPress only: the site cannot run the pixel and nothing was left on it. Code &#x60;tracking_tag_install_blocked&#x60;; the reason is in &#x60;details.reason&#x60;. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta, Shopify or the WordPress site was unreachable or returned an unclassified error. On WordPress a write may have completed; call GET before retrying. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtrackingtagevents"></a>
# **ListTrackingTagEvents**
> ListTrackingTagEvents200Response ListTrackingTagEvents (string accountId, string tagId, string? adAccountId = null)

List conversion events

The tag's conversion events, on platforms where each conversion is its own object: Google conversion actions, LinkedIn conversion rules, X web event tags, OpenAI event settings, TikTok pixel events, Meta custom conversions, Pinterest advertiser defined events.  OpenAI Ads: the account's conversion event settings whose source is this pixel. `siteEventId` is the event name the site sends (a standard event such as `order_created`, or the lowercase custom event name); `clickWindowDays` is the attribution window.  LinkedIn (`linkedinads`): the conversion rules of the ad account (`adAccountId`, default the account that created the tag), including Conversions API and URL-match rules. `siteEventId` (the rule id a page fires) is set only on event-specific Insight Tag rules; `defaultValue`/`currency` come from the rule value, `clickWindowDays`/`viewWindowDays` from its post-click and view-through windows.  Meta: the pixel's custom conversions. Meta keeps them per AD ACCOUNT (a pixel has no custom conversions edge), so the list reads `adAccountId` (default: the pixel's owner ad account) and keeps the conversions whose pixel is this one. Archived conversions are included with `status: archived`. `urlContains` and `siteEvent` are parsed from Meta's rule.  Google Ads (`googleads`): the enabled WEBPAGE conversion actions of the account; `siteEventId` is the conversion label (the part after `AW-.../` in `send_to`), and value settings, lookback windows, `primary` and `countingType` are returned. Archived (removed) actions are listed with status `REMOVED`; imported (GA4, upload, app) actions are not events of the tag.  Pinterest (platform `pinterestads`): the ad account's advertiser defined events, custom event names mapped to a standard type (`type`, e.g. `SIGNUP`). They belong to the ad account, so every tag on it shares them. `id`, `name` and `siteEventId` are all the event name, which the site sends as `pintrk('track', '<name>')` or the Conversions API sends as `event_name`. Standard events (`pagevisit`, `checkout`...) need no object and are not listed.  TikTok: the pixel's events from `/pixel/list/`. TikTok refreshes this list every 2 to 4 hours, so a just-created event can be missing. `siteEventId` is the `ttq.track()` name the site fires. 

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
    public class ListTrackingTagEventsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var adAccountId = "adAccountId_example";  // string? | Scopes the lookup on platforms whose tag ids live inside an ad account. (optional) 

            try
            {
                // List conversion events
                ListTrackingTagEvents200Response result = apiInstance.ListTrackingTagEvents(accountId, tagId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagEvents: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTrackingTagEventsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List conversion events
    ApiResponse<ListTrackingTagEvents200Response> response = apiInstance.ListTrackingTagEventsWithHttpInfo(accountId, tagId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagEventsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **adAccountId** | **string?** | Scopes the lookup on platforms whose tag ids live inside an ad account. | [optional]  |

### Return type

[**ListTrackingTagEvents200Response**](ListTrackingTagEvents200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Conversion events listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the platform token lacks the permission (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform has no conversion-event objects (code &#x60;platform_not_supported&#x60;); the message names the alternative. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtrackingtagpartners"></a>
# **ListTrackingTagPartners**
> ListTrackingTagPartners200Response ListTrackingTagPartners (string accountId, string tagId)

List partner businesses of a tag

Other businesses the tag is shared with. Read-only. Platforms without partner sharing answer 501.  Meta: the pixel's shared agencies. Sharing a pixel with a new partner is not available: `/{pixel}/agencies` answers \"(#3) Application does not have the capability to make this API call\" for our app. 

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
    public class ListTrackingTagPartnersExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).

            try
            {
                // List partner businesses of a tag
                ListTrackingTagPartners200Response result = apiInstance.ListTrackingTagPartners(accountId, tagId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagPartners: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTrackingTagPartnersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List partner businesses of a tag
    ApiResponse<ListTrackingTagPartners200Response> response = apiInstance.ListTrackingTagPartnersWithHttpInfo(accountId, tagId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagPartnersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |

### Return type

[**ListTrackingTagPartners200Response**](ListTrackingTagPartners200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Partners listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the platform token lacks the permission (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform has no partner sharing (code &#x60;platform_not_supported&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtrackingtagsharedaccounts"></a>
# **ListTrackingTagSharedAccounts**
> ListTrackingTagSharedAccounts200Response ListTrackingTagSharedAccounts (string accountId, string tagId)

List accounts it is shared with

Meta (`metaads`) and LinkedIn (`linkedinads`); other platforms return 501.  LinkedIn (`linkedinads`): the ad accounts this connection can see that hold access to the Insight Tag; the role (`FULL` or `USE_ONLY`) is appended to `name`. LinkedIn exposes permissions per ad account only, so accounts the connection cannot see are not listed.  TikTok (`tiktokads`): the advertisers linked to the pixel in its Business Center (`/bc/pixel/link/get/`); a pixel outside Business Center answers 400. 

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
    public class ListTrackingTagSharedAccountsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.

            try
            {
                // List accounts it is shared with
                ListTrackingTagSharedAccounts200Response result = apiInstance.ListTrackingTagSharedAccounts(accountId, tagId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagSharedAccounts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTrackingTagSharedAccountsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List accounts it is shared with
    ApiResponse<ListTrackingTagSharedAccounts200Response> response = apiInstance.ListTrackingTagSharedAccountsWithHttpInfo(accountId, tagId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagSharedAccountsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |

### Return type

[**ListTrackingTagSharedAccounts200Response**](ListTrackingTagSharedAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Shared ad accounts listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtrackingtagusers"></a>
# **ListTrackingTagUsers**
> ListTrackingTagUsers200Response ListTrackingTagUsers (string accountId, string tagId)

List tag users

People and system users of the owning business with access to the tag. Platforms without tag user assignment answer 501.  Meta: the pixel's assigned users in its owning Business Manager. A pixel on a personal ad account has no business and returns an empty list. Needs the `business_management` permission on the connecting Meta user (an admin of the owning business); without it the call answers 403 asking to reconnect. 

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
    public class ListTrackingTagUsersExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).

            try
            {
                // List tag users
                ListTrackingTagUsers200Response result = apiInstance.ListTrackingTagUsers(accountId, tagId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagUsers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTrackingTagUsersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List tag users
    ApiResponse<ListTrackingTagUsers200Response> response = apiInstance.ListTrackingTagUsersWithHttpInfo(accountId, tagId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagUsersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |

### Return type

[**ListTrackingTagUsers200Response**](ListTrackingTagUsers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tag users listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the platform token lacks the permission (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform has no tag user assignment (code &#x60;platform_not_supported&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtrackingtags"></a>
# **ListTrackingTags**
> ListTrackingTags200Response ListTrackingTags (string accountId, string? adAccountId = null)

List tracking tags

Returns the tracking tags (Meta Pixels, or OpenAI Ads pixels) the connected ads account can see. Pass `?adAccountId=act_...` (Meta only) to scope the list to a single ad account; omit it to list every pixel reachable by the token (the name is then suffixed with the ad account it was discovered on, for disambiguation). The list view omits `code`. Call `getTrackingTag` for the install snippet and full detail.  Meta (platform `metaads`) and OpenAI Ads (platform `openaiads`); other platforms return 501. The `accountId` must be the ads SocialAccount created by the Ads add-on connect flow (Meta) or the OpenAI Ads connect flow, not a Facebook/Instagram posting account. Get your Meta `act_...` ids from `GET /v1/ads/accounts`; `adAccountId` is ignored for OpenAI Ads (one API key maps to exactly one ad account).  LinkedIn (`linkedinads`): lists the Insight Tag of each ad account (LinkedIn allows one per ad account; a tag shared with several accounts appears once). `adAccountId` is the numeric ad account id or `urn:li:sponsoredAccount:{id}`; omit it to scan every active ad account the connection can see. The tag `id` IS the partner id the site embeds, so `siteTagId` equals `id`. LinkedIn tags have no name; it is shown as `Insight Tag {id}`.  Pinterest (platform `pinterestads`): lists Pinterest tags (conversion tags). `adAccountId` is the numeric Pinterest ad account id (no prefix); omit it to walk every ad account the connection can read (an ad account the user has no Business Access role on is skipped). `id` equals `siteTagId`, the id the site loads with `pintrk('load', id)`.  TikTok (platform `tiktokads`): TikTok Pixels across the connection's advertisers, or one advertiser with `?adAccountId=<numeric advertiser_id>`. `id` is the numeric `pixel_id`, `siteTagId` the alphanumeric `pixel_code` from Events Manager. Connections authorized before the Pixel Management permission (about 2026-05-28) answer 403 until reconnected. 

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
    public class ListTrackingTagsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Ads SocialAccount id (platform `metaads` or `openaiads`).
            var adAccountId = "adAccountId_example";  // string? | Optional, Meta only. Scope to one ad account, e.g. `act_123456789`. Ignored for OpenAI Ads. (optional) 

            try
            {
                // List tracking tags
                ListTrackingTags200Response result = apiInstance.ListTrackingTags(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTags: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTrackingTagsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List tracking tags
    ApiResponse<ListTrackingTags200Response> response = apiInstance.ListTrackingTagsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Ads SocialAccount id (platform &#x60;metaads&#x60; or &#x60;openaiads&#x60;). |  |
| **adAccountId** | **string?** | Optional, Meta only. Scope to one ad account, e.g. &#x60;act_123456789&#x60;. Ignored for OpenAI Ads. | [optional]  |

### Return type

[**ListTrackingTags200Response**](ListTrackingTags200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tracking tags listed |  -  |
| **400** | Account platform not supported, or invalid &#x60;adAccountId&#x60;. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removetrackingtagfromstore"></a>
# **RemoveTrackingTagFromStore**
> RemoveTrackingTagFromStore200Response RemoveTrackingTagFromStore (string accountId, string tagId, string storeAccountId, string? adAccountId = null)

Remove from a Shopify store or WordPress site

Removes the tag from the store. Idempotent: nothing installed returns 200 with `installed: false`. If the store fires a different tag of the same platform, nothing is removed and the call answers 409 `invalid_resource_state`. Shopify: other platforms' tags stay; the web pixel itself is deleted once no tag remains.  WordPress: deletes every widget Zernio created for this pixel and reports how many in `removed` (0 when nothing was installed). Pixel code added by hand is left alone. 

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
    public class RemoveTrackingTagFromStoreExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var storeAccountId = "storeAccountId_example";  // string | The connected Shopify or WordPress account id.
            var adAccountId = "adAccountId_example";  // string? | Scopes the tag lookup on platforms whose tag ids live inside an ad account. (optional) 

            try
            {
                // Remove from a Shopify store or WordPress site
                RemoveTrackingTagFromStore200Response result = apiInstance.RemoveTrackingTagFromStore(accountId, tagId, storeAccountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.RemoveTrackingTagFromStore: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveTrackingTagFromStoreWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove from a Shopify store or WordPress site
    ApiResponse<RemoveTrackingTagFromStore200Response> response = apiInstance.RemoveTrackingTagFromStoreWithHttpInfo(accountId, tagId, storeAccountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.RemoveTrackingTagFromStoreWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **storeAccountId** | **string** | The connected Shopify or WordPress account id. |  |
| **adAccountId** | **string?** | Scopes the tag lookup on platforms whose tag ids live inside an ad account. | [optional]  |

### Return type

[**RemoveTrackingTagFromStore200Response**](RemoveTrackingTagFromStore200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pixel removed (or was not installed) |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The store fires a different pixel (code &#x60;invalid_resource_state&#x60;), or the store must re-approve the Zernio app (code &#x60;reconnect_required&#x60;, see &#x60;details.authUrl&#x60;). |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removetrackingtagsharedaccount"></a>
# **RemoveTrackingTagSharedAccount**
> void RemoveTrackingTagSharedAccount (string accountId, string tagId, string? adAccountId = null)

Stop sharing with an account

`adAccountId` may be passed as a query parameter (recommended) or as a JSON body field for clients that can send DELETE bodies. Meta and LinkedIn; other platforms return 501.  LinkedIn (`linkedinads`): revokes the ad account's access. Zernio answers 400 instead of revoking the last ad account that holds the tag: LinkedIn accepts that call and the tag is orphaned (verified live).  TikTok: unlinks through Business Center (`/bc/pixel/link/update/` with `UNLINK`). 

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
    public class RemoveTrackingTagSharedAccountExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.
            var adAccountId = "adAccountId_example";  // string? | Ad account to unshare, e.g. `act_123456789`. May also be sent in the JSON body. (optional) 

            try
            {
                // Stop sharing with an account
                apiInstance.RemoveTrackingTagSharedAccount(accountId, tagId, adAccountId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.RemoveTrackingTagSharedAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveTrackingTagSharedAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Stop sharing with an account
    apiInstance.RemoveTrackingTagSharedAccountWithHttpInfo(accountId, tagId, adAccountId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.RemoveTrackingTagSharedAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |
| **adAccountId** | **string?** | Ad account to unshare, e.g. &#x60;act_123456789&#x60;. May also be sent in the JSON body. | [optional]  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Ad account unshared (no content). |  -  |
| **400** | &#x60;adAccountId&#x60; missing (neither query nor body), or Meta rejected the unshare. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removetrackingtaguser"></a>
# **RemoveTrackingTagUser**
> RemoveTrackingTagUser200Response RemoveTrackingTagUser (string accountId, string tagId, string userId)

Remove a user from a tag

Removes a user's access to the tag, on platforms whose API allows it.  Meta answers 501: the Business SDK has no delete on the pixel's assigned users, `DELETE /{pixel}/assigned_users` answers \"Unsupported delete request\" (code 100, subcode 33) and re-assigning with no tasks is refused. Remove the user in Business Settings. 

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
    public class RemoveTrackingTagUserExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | 
            var userId = "userId_example";  // string | User id (`TrackingTagUser.id`).

            try
            {
                // Remove a user from a tag
                RemoveTrackingTagUser200Response result = apiInstance.RemoveTrackingTagUser(accountId, tagId, userId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.RemoveTrackingTagUser: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveTrackingTagUserWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove a user from a tag
    ApiResponse<RemoveTrackingTagUser200Response> response = apiInstance.RemoveTrackingTagUserWithHttpInfo(accountId, tagId, userId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.RemoveTrackingTagUserWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** |  |  |
| **userId** | **string** | User id (&#x60;TrackingTagUser.id&#x60;). |  |

### Return type

[**RemoveTrackingTagUser200Response**](RemoveTrackingTagUser200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User removed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the platform token lacks the permission (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform cannot remove tag users through its API (code &#x60;platform_not_supported&#x60;); the message says where to do it. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadtrackingtags"></a>
# **UpdateAdTrackingTags**
> UpdateAdTrackingTags200Response UpdateAdTrackingTags (string adId, UpdateAdTrackingTagsRequest updateAdTrackingTagsRequest)

Set ad tracking tags

Unified update. Send only the fields for the ad's platform: - Meta: `urlTags` (array of {key,value}). Meta creatives are immutable, so this rebuilds the   creative and repoints the ad. By DEFAULT we PRESERVE the existing creative verbatim   (re-post its object_story_spec + the new url_tags, reusing the image), so you send `urlTags`   ALONE, with no need to read back headline/body/CTA. `creative` (headline, body, callToAction,   linkUrl, imageUrl) is OPTIONAL and only needed to rebuild explicitly, or for SHARE / page-post   / dark / asset_feed creatives whose object_story_spec Meta strips (those return 422 asking for   `creative`). - Google: `trackingUrlTemplate` and/or `finalUrlSuffix` (full template strings; account quota applies). - LinkedIn: `dynamicValueParameters` and/or `customValueParameters` (campaign-level Dynamic UTM). 

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
    public class UpdateAdTrackingTagsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | 
            var updateAdTrackingTagsRequest = new UpdateAdTrackingTagsRequest(); // UpdateAdTrackingTagsRequest | 

            try
            {
                // Set ad tracking tags
                UpdateAdTrackingTags200Response result = apiInstance.UpdateAdTrackingTags(adId, updateAdTrackingTagsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.UpdateAdTrackingTags: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdTrackingTagsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set ad tracking tags
    ApiResponse<UpdateAdTrackingTags200Response> response = apiInstance.UpdateAdTrackingTagsWithHttpInfo(adId, updateAdTrackingTagsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.UpdateAdTrackingTagsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** |  |  |
| **updateAdTrackingTagsRequest** | [**UpdateAdTrackingTagsRequest**](UpdateAdTrackingTagsRequest.md) |  |  |

### Return type

[**UpdateAdTrackingTags200Response**](UpdateAdTrackingTags200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tags as they now stand, in the same shape the GET on this path returns: &#x60;platform&#x60; plus the fields that platform supports. Meta returns &#x60;level&#x60;, &#x60;urlTags&#x60; and &#x60;templateUrlSpec&#x60;; Google returns &#x60;trackingUrlTemplate&#x60; and &#x60;finalUrlSuffix&#x60;. A field the platform does not support is absent.  |  -  |
| **401** | Unauthorized |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | Ad not found |  -  |
| **405** | Platform has no click-URL tracking surface |  -  |
| **422** | Meta creative cannot be rebuilt (e.g. placement-customized/asset-feed/dark creative) |  -  |
| **502** | Meta accepted the request then failed to produce the media (upload session, chunk transfer, processing timeout, or a response with no image hash). Inspect &#x60;platformError.reason&#x60;. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatetrackingtag"></a>
# **UpdateTrackingTag**
> GetTrackingTag200Response UpdateTrackingTag (string accountId, string tagId, UpdateTrackingTagRequest updateTrackingTagRequest)

Update a tracking tag

Partial-update a pixel. Whitelisted fields: `name` (rename), `enableAutomaticMatching`, `automaticMatchingFields`, `firstPartyCookieStatus`, `dataUseSetting`. At least one is required. Returns the re-fetched canonical tag. Meta only (platform `metaads`); other platforms return 501.  OpenAI Ads answers 501: its API has no pixel update or delete route (`POST`/`PATCH`/`PUT`/`DELETE /v1/conversions/pixels/{id}` answer 405 \"Invalid method\"); rename a pixel in OpenAI Ads Manager.  Google Ads (`googleads`): the only writable tag setting is `autoTagging` (the account's gclid auto-tagging, without which the tag cannot attribute conversions to ad clicks). Google rejects every write to `conversion_tracking_setting` for our developer token (`SERVICE_ACCESS_DENIED`), so the tag id and cross-account ownership stay managed in the Google Ads UI.  There is no DELETE: Meta has no API to delete a pixel. To stop using one, unshare it from your ad accounts (`DELETE .../tracking-tags/{tagId}/shared-accounts`) or disable it in Events Manager.  LinkedIn (`linkedinads`): only `firstPartyCookieStatus` (`first_party_cookie_enabled` or `first_party_cookie_disabled`), which sets the tag's first-party tracking. It applies to every ad account using the tag. `empty` answers 400: LinkedIn has no unset state.  Pinterest (platform `pinterestads`): 501. Pinterest API v5 has no endpoint to edit a tag: its spec lists only POST/GET on `conversion_tags` and GET on `conversion_tags/{id}`, and PATCH or PUT on `conversion_tags/{id}` answer 405 \"Method not allowed\". Set enhanced match at creation (`automaticMatchingFields`) or change it and the name in Pinterest Ads Manager.  TikTok: `name`, `enableAutomaticMatching` + `automaticMatchingFields` (folded onto TikTok's five switches: em, ph, fn/ln, ct/st/zp/country, external_id; ge and db answer 400), and first-party cookies via `enableFirstPartyCookies` or `firstPartyCookieStatus` (enabled or disabled). TikTok has no pixel delete: the endpoint is absent from its API and `POST /pixel/delete/` answers 404. 

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
    public class UpdateTrackingTagExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.
            var updateTrackingTagRequest = new UpdateTrackingTagRequest(); // UpdateTrackingTagRequest | 

            try
            {
                // Update a tracking tag
                GetTrackingTag200Response result = apiInstance.UpdateTrackingTag(accountId, tagId, updateTrackingTagRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.UpdateTrackingTag: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTrackingTagWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a tracking tag
    ApiResponse<GetTrackingTag200Response> response = apiInstance.UpdateTrackingTagWithHttpInfo(accountId, tagId, updateTrackingTagRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.UpdateTrackingTagWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |
| **updateTrackingTagRequest** | [**UpdateTrackingTagRequest**](UpdateTrackingTagRequest.md) |  |  |

### Return type

[**GetTrackingTag200Response**](GetTrackingTag200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tracking tag updated (re-fetched canonical state) |  -  |
| **400** | Invalid body (e.g. no fields supplied) or Meta validation failure. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatetrackingtagevent"></a>
# **UpdateTrackingTagEvent**
> CreateTrackingTagEvent201Response UpdateTrackingTagEvent (string accountId, string tagId, string eventId, TrackingTagEventInput trackingTagEventInput)

Update a conversion event

Partial update; at least one field. A field the platform does not store answers 400.  OpenAI Ads answers 501: OpenAI documents only list and create for event settings, and `POST`/`PATCH`/`PUT /v1/conversions/event_settings/{id}` answer 404 \"Invalid URL\". Create a new event instead.  LinkedIn (`linkedinads`): partial update of the conversion rule; same fields as create. Pass `adAccountId` when the rule lives in another ad account than the one that created the tag.  Meta: only `name` and `defaultValue` can change (Meta's custom conversion update takes nothing else); `type`, `siteEvent` and `urlContains` answer 400, create a new event instead.  Google Ads (`googleads`): same fields as create, on the account's WEBPAGE actions (others answer 404). `enabled: false` archives the action (same as DELETE) and `enabled: true` restores an archived one.  Pinterest (platform `pinterestads`): remaps the event to another `type` or `siteEvent`. Pinterest identifies the event by its name, so `name` cannot change (400): create the new name and delete the old one.  TikTok: `name`, `defaultValue` and `currency` (USD, JPY or INR); the type cannot change (delete and recreate). 

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
    public class UpdateTrackingTagEventExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | 
            var eventId = "eventId_example";  // string | Event id (`TrackingTagEvent.id`).
            var trackingTagEventInput = new TrackingTagEventInput(); // TrackingTagEventInput | 

            try
            {
                // Update a conversion event
                CreateTrackingTagEvent201Response result = apiInstance.UpdateTrackingTagEvent(accountId, tagId, eventId, trackingTagEventInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.UpdateTrackingTagEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTrackingTagEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a conversion event
    ApiResponse<CreateTrackingTagEvent201Response> response = apiInstance.UpdateTrackingTagEventWithHttpInfo(accountId, tagId, eventId, trackingTagEventInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.UpdateTrackingTagEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** |  |  |
| **eventId** | **string** | Event id (&#x60;TrackingTagEvent.id&#x60;). |  |
| **trackingTagEventInput** | [**TrackingTagEventInput**](TrackingTagEventInput.md) |  |  |

### Return type

[**CreateTrackingTagEvent201Response**](CreateTrackingTagEvent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Conversion event updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the platform token lacks the permission (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform cannot update conversion events through its API (code &#x60;platform_not_supported&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

