# Zernio.Api.CreatorPortalApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateCreatorPayoutLogin**](CreatorPortalApi.md#createcreatorpayoutlogin) | **POST** /public/creator-campaigns/{token}/payout-login | Open the creator&#39;s Stripe dashboard |
| [**GetCreatorPayoutStatement**](CreatorPortalApi.md#getcreatorpayoutstatement) | **GET** /public/creator-campaigns/{token}/payouts/{transferId}/statement | Download a payout statement |
| [**GetCreatorPayouts**](CreatorPortalApi.md#getcreatorpayouts) | **GET** /public/creator-campaigns/{token}/payouts | List a creator&#39;s earnings history |
| [**GetCreatorPortal**](CreatorPortalApi.md#getcreatorportal) | **GET** /public/creator-campaigns/{token} | Read a creator invite or participant page |
| [**JoinCreatorCampaign**](CreatorPortalApi.md#joincreatorcampaign) | **POST** /public/creator-campaigns/{token} | Join a campaign |
| [**PresignCreatorDraftUpload**](CreatorPortalApi.md#presigncreatordraftupload) | **POST** /public/creator-campaigns/{token}/drafts/upload | Get an upload URL for a draft |
| [**RecoverCreatorPortalLinks**](CreatorPortalApi.md#recovercreatorportallinks) | **POST** /public/creator-campaigns/recover-link | Email a creator their campaign links |
| [**RemoveCreatorAccount**](CreatorPortalApi.md#removecreatoraccount) | **DELETE** /public/creator-campaigns/{token}/accounts/{accountId} | Remove a connected account |
| [**RequestCreatorSample**](CreatorPortalApi.md#requestcreatorsample) | **POST** /public/creator-campaigns/{token}/samples | Request a product sample |
| [**SetCreatorSparkCode**](CreatorPortalApi.md#setcreatorsparkcode) | **PUT** /public/creator-campaigns/{token}/submissions/{submissionId}/spark-code | Set a post&#39;s Spark code |
| [**StartCreatorConnect**](CreatorPortalApi.md#startcreatorconnect) | **POST** /public/creator-campaigns/{token}/connect | Start connecting a creator account |
| [**StartCreatorPayouts**](CreatorPortalApi.md#startcreatorpayouts) | **POST** /public/creator-campaigns/{token}/payouts | Start payout onboarding |
| [**SubmitCreatorDraft**](CreatorPortalApi.md#submitcreatordraft) | **POST** /public/creator-campaigns/{token}/drafts | Submit a draft for review |
| [**SubmitCreatorPost**](CreatorPortalApi.md#submitcreatorpost) | **POST** /public/creator-campaigns/{token}/submissions | Submit a post |

<a id="createcreatorpayoutlogin"></a>
# **CreateCreatorPayoutLogin**
> StartCreatorPayouts200Response CreateCreatorPayoutLogin (string token)

Open the creator's Stripe dashboard

Returns a one-time link into the creator's Stripe Express dashboard, where they change bank details and see each payout. Only after the creator submitted their payout details. About 20 attempts per participant every 10 minutes. 

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
    public class CreateCreatorPayoutLoginExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | A participant token or an open invite token. A malformed token answers 404 like an unknown one.

            try
            {
                // Open the creator's Stripe dashboard
                StartCreatorPayouts200Response result = apiInstance.CreateCreatorPayoutLogin(token);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.CreateCreatorPayoutLogin: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCreatorPayoutLoginWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Open the creator's Stripe dashboard
    ApiResponse<StartCreatorPayouts200Response> response = apiInstance.CreateCreatorPayoutLoginWithHttpInfo(token);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.CreateCreatorPayoutLoginWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. |  |

### Return type

[**StartCreatorPayouts200Response**](StartCreatorPayouts200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Stripe login link. |  -  |
| **404** | The token is malformed, unknown or expired. Every case answers the same, so a link can never be probed. |  -  |
| **409** | The creator has not submitted payout details yet, or the campaign team pays them directly (\&quot;Finish payout setup first.\&quot;, &#x60;invalid_resource_state&#x60;). |  -  |
| **429** | Too many attempts from this link or IP address (&#x60;rate_limited&#x60;). Wait a few minutes and try again. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcreatorpayoutstatement"></a>
# **GetCreatorPayoutStatement**
> FileParameter GetCreatorPayoutStatement (string token, string transferId)

Download a payout statement

A PDF statement of one paid payout to this creator: who paid, the campaign, the date, the amount and the Stripe transfer id. It is a statement of a payment, not a tax invoice.  Only for a paid payout of this participant; anything else answers 404.  About 60 downloads per participant every 10 minutes. 

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
    public class GetCreatorPayoutStatementExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | A participant token or an open invite token. A malformed token answers 404 like an unknown one.
            var transferId = "transferId_example";  // string | 

            try
            {
                // Download a payout statement
                FileParameter result = apiInstance.GetCreatorPayoutStatement(token, transferId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.GetCreatorPayoutStatement: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCreatorPayoutStatementWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Download a payout statement
    ApiResponse<FileParameter> response = apiInstance.GetCreatorPayoutStatementWithHttpInfo(token, transferId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.GetCreatorPayoutStatementWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. |  |
| **transferId** | **string** |  |  |

### Return type

[**FileParameter**](FileParameter.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The statement, as an attachment. |  -  |
| **404** | The link is invalid, or no paid payout of this participant has this id (\&quot;Payout not found.\&quot;). |  -  |
| **429** | Too many attempts from this link or IP address (&#x60;rate_limited&#x60;). Wait a few minutes and try again. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcreatorpayouts"></a>
# **GetCreatorPayouts**
> GetCreatorPayouts200Response GetCreatorPayouts (string token, int? limit = null, int? skip = null)

List a creator's earnings history

The participant's ledger entries, newest first, with the bucket each one moved money from and to (`accruing`, `owed`, `payable`, `settling`, `settled`; null for the other side), plus the payout setup. Never cached. 

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
    public class GetCreatorPayoutsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | A participant token or an open invite token. A malformed token answers 404 like an unknown one.
            var limit = 50;  // int? |  (optional)  (default to 50)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List a creator's earnings history
                GetCreatorPayouts200Response result = apiInstance.GetCreatorPayouts(token, limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.GetCreatorPayouts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCreatorPayoutsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List a creator's earnings history
    ApiResponse<GetCreatorPayouts200Response> response = apiInstance.GetCreatorPayoutsWithHttpInfo(token, limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.GetCreatorPayoutsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. |  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**GetCreatorPayouts200Response**](GetCreatorPayouts200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Earnings history and payout setup. |  -  |
| **400** | Invalid request |  -  |
| **404** | The token is malformed, unknown or expired. Every case answers the same, so a link can never be probed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcreatorportal"></a>
# **GetCreatorPortal**
> GetCreatorPortal200Response GetCreatorPortal (string token)

Read a creator invite or participant page

What a creator sees behind a campaign link, with no API key. Never cached.  `token` is one of:  - An open invite token (from `POST /v1/creator-campaigns/{campaignId}/invite-link`): answers `kind: invite` with the campaign only. - A participant token (from an invite or a join): answers `kind: participant` with the creator's connected accounts, latest 100 submissions, draft versions, sample requests, earnings and payout setup. A creator held for approval reads it with `participant.status` `pending` (or `denied` once turned away).  Reading a participant page also re-checks the creator's connected accounts. 

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
    public class GetCreatorPortalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | A participant token or an open invite token. A malformed token answers 404 like an unknown one.

            try
            {
                // Read a creator invite or participant page
                GetCreatorPortal200Response result = apiInstance.GetCreatorPortal(token);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.GetCreatorPortal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCreatorPortalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read a creator invite or participant page
    ApiResponse<GetCreatorPortal200Response> response = apiInstance.GetCreatorPortalWithHttpInfo(token);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.GetCreatorPortalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. |  |

### Return type

[**GetCreatorPortal200Response**](GetCreatorPortal200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The invite or participant page. |  -  |
| **404** | The token is malformed, unknown or expired. Every case answers the same, so a link can never be probed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="joincreatorcampaign"></a>
# **JoinCreatorCampaign**
> JoinCreatorCampaign201Response JoinCreatorCampaign (string token, JoinCreatorCampaignRequest? joinCreatorCampaignRequest = null)

Join a campaign

Accepts a participant invite, or joins through an open invite link.  - Participant token: the body is ignored and the invite is accepted. - Open invite token: a new participant is created from `displayName` (required) and `email` (optional), and a fresh participant token comes back. Keep it: it is the creator's only key to their page. - On a campaign with `joinApproval: manual`, an open-link joiner lands `pending` and `campaign_participant.pending` fires instead of `campaign_participant.joined`. A pending creator holds no place under `caps.maxParticipants` (the limit is checked when the operator approves them) and cannot submit posts, drafts or sample requests until approved. Personal invites always get straight in.  Open-link joins are limited to about 20 per IP address and 60 per link every 10 minutes. 

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
    public class JoinCreatorCampaignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | A participant token or an open invite token. A malformed token answers 404 like an unknown one.
            var joinCreatorCampaignRequest = new JoinCreatorCampaignRequest?(); // JoinCreatorCampaignRequest? |  (optional) 

            try
            {
                // Join a campaign
                JoinCreatorCampaign201Response result = apiInstance.JoinCreatorCampaign(token, joinCreatorCampaignRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.JoinCreatorCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the JoinCreatorCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Join a campaign
    ApiResponse<JoinCreatorCampaign201Response> response = apiInstance.JoinCreatorCampaignWithHttpInfo(token, joinCreatorCampaignRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.JoinCreatorCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. |  |
| **joinCreatorCampaignRequest** | [**JoinCreatorCampaignRequest?**](JoinCreatorCampaignRequest?.md) |  | [optional]  |

### Return type

[**JoinCreatorCampaign201Response**](JoinCreatorCampaign201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Joined. Use &#x60;participantToken&#x60; for every later call. |  -  |
| **400** | Missing &#x60;displayName&#x60; on an open-link join (\&quot;Add your name to join.\&quot;, &#x60;missing_required_field&#x60;), an invalid field, or the campaign has ended (&#x60;invalid_resource_state&#x60;, \&quot;This campaign has ended.\&quot;). |  -  |
| **403** | The campaign is not taking new creators (&#x60;feature_not_available&#x60;, \&quot;This campaign is not taking new creators right now. Ask the campaign team.\&quot;), for example because it reached its participant cap. Not returned for the cap on a &#x60;joinApproval: manual&#x60; campaign, where the cap is checked on approval. |  -  |
| **404** | The token is malformed, unknown or expired. Every case answers the same, so a link can never be probed. |  -  |
| **429** | Too many attempts from this link or IP address (&#x60;rate_limited&#x60;). Wait a few minutes and try again. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="presigncreatordraftupload"></a>
# **PresignCreatorDraftUpload**
> PresignCreatorDraftUpload200Response PresignCreatorDraftUpload (string token, PresignCreatorDraftUploadRequest presignCreatorDraftUploadRequest)

Get an upload URL for a draft

Returns a presigned URL to upload one draft file to, on a campaign with `requireDraftApproval`. `PUT` the file to `uploadUrl` with the same `Content-Type`, then pass `publicUrl` as `mediaUrl` to `POST /public/creator-campaigns/{token}/drafts`. The URL expires after `expiresIn` seconds.  Accepted files: MP4, MOV or WebM video, JPG, PNG or WebP image, up to 500 MB. About 20 uploads per participant every 10 minutes. 

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
    public class PresignCreatorDraftUploadExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | A participant token or an open invite token. A malformed token answers 404 like an unknown one.
            var presignCreatorDraftUploadRequest = new PresignCreatorDraftUploadRequest(); // PresignCreatorDraftUploadRequest | 

            try
            {
                // Get an upload URL for a draft
                PresignCreatorDraftUpload200Response result = apiInstance.PresignCreatorDraftUpload(token, presignCreatorDraftUploadRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.PresignCreatorDraftUpload: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PresignCreatorDraftUploadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an upload URL for a draft
    ApiResponse<PresignCreatorDraftUpload200Response> response = apiInstance.PresignCreatorDraftUploadWithHttpInfo(token, presignCreatorDraftUploadRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.PresignCreatorDraftUploadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. |  |
| **presignCreatorDraftUploadRequest** | [**PresignCreatorDraftUploadRequest**](PresignCreatorDraftUploadRequest.md) |  |  |

### Return type

[**PresignCreatorDraftUpload200Response**](PresignCreatorDraftUpload200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Upload URL. |  -  |
| **400** | An invalid field: an unsupported &#x60;contentType&#x60; or a &#x60;size&#x60; over 500 MB. |  -  |
| **404** | The token is malformed, unknown or expired. Every case answers the same, so a link can never be probed. |  -  |
| **409** | The campaign does not review drafts, is not accepting posts (not started, paused or ended), the invite is not accepted yet, or the creator is pending, denied, suspended or removed (&#x60;invalid_resource_state&#x60;; the message says which). |  -  |
| **429** | Too many attempts from this link or IP address (&#x60;rate_limited&#x60;). Wait a few minutes and try again. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="recovercreatorportallinks"></a>
# **RecoverCreatorPortalLinks**
> RecoverCreatorPortalLinks202Response RecoverCreatorPortalLinks (RecoverCreatorPortalLinksRequest recoverCreatorPortalLinksRequest)

Email a creator their campaign links

For a creator who lost their link. Emails every personal participant link held by `email` in one message, optionally only the one for `campaignId`.  - Removed participants and draft campaigns are left out. - Always answers 202 with the same body, so the answer never tells whether the address has links. - Limited to 5 requests per hour per email address and 5 per hour per IP address. 

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
    public class RecoverCreatorPortalLinksExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var recoverCreatorPortalLinksRequest = new RecoverCreatorPortalLinksRequest(); // RecoverCreatorPortalLinksRequest | 

            try
            {
                // Email a creator their campaign links
                RecoverCreatorPortalLinks202Response result = apiInstance.RecoverCreatorPortalLinks(recoverCreatorPortalLinksRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.RecoverCreatorPortalLinks: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RecoverCreatorPortalLinksWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Email a creator their campaign links
    ApiResponse<RecoverCreatorPortalLinks202Response> response = apiInstance.RecoverCreatorPortalLinksWithHttpInfo(recoverCreatorPortalLinksRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.RecoverCreatorPortalLinksWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **recoverCreatorPortalLinksRequest** | [**RecoverCreatorPortalLinksRequest**](RecoverCreatorPortalLinksRequest.md) |  |  |

### Return type

[**RecoverCreatorPortalLinks202Response**](RecoverCreatorPortalLinks202Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Accepted. If the address has links, they are on their way. |  -  |
| **400** | The email is missing or not a valid address. |  -  |
| **429** | Too many attempts from this link or IP address (&#x60;rate_limited&#x60;). Wait a few minutes and try again. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removecreatoraccount"></a>
# **RemoveCreatorAccount**
> RemoveCreatorAccount200Response RemoveCreatorAccount (string token, string accountId)

Remove a connected account

Disconnects one of the creator's accounts. The account belongs to the creator, not to one campaign, so it stops counting in every campaign of this brand they joined.  What its posts already earned stays: accrued, approved and paid amounts are not touched.  Refused while a post from the account is still counting views, because those views are read through the account. It can be removed once their tracking ends. 

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
    public class RemoveCreatorAccountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | A participant token or an open invite token. A malformed token answers 404 like an unknown one.
            var accountId = "accountId_example";  // string | The `id` of one of the participant's `accounts`.

            try
            {
                // Remove a connected account
                RemoveCreatorAccount200Response result = apiInstance.RemoveCreatorAccount(token, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.RemoveCreatorAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveCreatorAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove a connected account
    ApiResponse<RemoveCreatorAccount200Response> response = apiInstance.RemoveCreatorAccountWithHttpInfo(token, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.RemoveCreatorAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. |  |
| **accountId** | **string** | The &#x60;id&#x60; of one of the participant&#39;s &#x60;accounts&#x60;. |  |

### Return type

[**RemoveCreatorAccount200Response**](RemoveCreatorAccount200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Removed. |  -  |
| **400** | Invalid request |  -  |
| **404** | The link is invalid or expired, or the account is not one of the participant&#39;s accounts on the campaign&#39;s platforms (&#x60;resource_not_found&#x60;). |  -  |
| **409** | A post from the account is still counting views (&#x60;invalid_resource_state&#x60;; the message says how many). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="requestcreatorsample"></a>
# **RequestCreatorSample**
> RequestCreatorSample201Response RequestCreatorSample (string token, RequestCreatorSampleRequest requestCreatorSampleRequest)

Request a product sample

Asks for a free sample of one of the campaign's `sampleProducts`, shipped to `shippingAddress`, and fires `campaign_sample.requested`. The request waits for the campaign team; on approval the creator gets a single-use discount code for the product.  - A product with `variants` needs `variantId`. - One open request per product: asking again while one is pending, approved or shipped answers 409. A declined product can be asked again.  About 10 requests per participant every 10 minutes. 

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
    public class RequestCreatorSampleExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | A participant token or an open invite token. A malformed token answers 404 like an unknown one.
            var requestCreatorSampleRequest = new RequestCreatorSampleRequest(); // RequestCreatorSampleRequest | 

            try
            {
                // Request a product sample
                RequestCreatorSample201Response result = apiInstance.RequestCreatorSample(token, requestCreatorSampleRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.RequestCreatorSample: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RequestCreatorSampleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Request a product sample
    ApiResponse<RequestCreatorSample201Response> response = apiInstance.RequestCreatorSampleWithHttpInfo(token, requestCreatorSampleRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.RequestCreatorSampleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. |  |
| **requestCreatorSampleRequest** | [**RequestCreatorSampleRequest**](RequestCreatorSampleRequest.md) |  |  |

### Return type

[**RequestCreatorSample201Response**](RequestCreatorSample201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Sample requested. |  -  |
| **400** | An invalid field, a product the campaign does not offer (&#x60;invalid_field_value&#x60;, &#x60;param: productId&#x60;), or a missing or unknown option (&#x60;param: variantId&#x60;, \&quot;Pick one of the options for this product\&quot;). |  -  |
| **404** | The token is malformed, unknown or expired. Every case answers the same, so a link can never be probed. |  -  |
| **409** | The campaign offers no samples or is not accepting posts, the creator is not active in it (invite not accepted, pending, denied, suspended or removed), or the creator already has an open request for this product (&#x60;invalid_resource_state&#x60;; the message says which). |  -  |
| **429** | Too many attempts from this link or IP address (&#x60;rate_limited&#x60;). Wait a few minutes and try again. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setcreatorsparkcode"></a>
# **SetCreatorSparkCode**
> SetCreatorSparkCode200Response SetCreatorSparkCode (string token, string submissionId, SetCreatorSparkCodeRequest setCreatorSparkCodeRequest)

Set a post's Spark code

The creator pastes the Spark code of one of their TikTok posts (generated in the TikTok app under the post's ad settings), so the brand can run the post as a Spark Ad under the creator's handle.  Send `null` to clear it. The code is never returned: submissions only expose `hasSparkCode`. 

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
    public class SetCreatorSparkCodeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | A participant token or an open invite token. A malformed token answers 404 like an unknown one.
            var submissionId = "submissionId_example";  // string | The `id` of one of the participant's `submissions`.
            var setCreatorSparkCodeRequest = new SetCreatorSparkCodeRequest(); // SetCreatorSparkCodeRequest | 

            try
            {
                // Set a post's Spark code
                SetCreatorSparkCode200Response result = apiInstance.SetCreatorSparkCode(token, submissionId, setCreatorSparkCodeRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.SetCreatorSparkCode: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetCreatorSparkCodeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set a post's Spark code
    ApiResponse<SetCreatorSparkCode200Response> response = apiInstance.SetCreatorSparkCodeWithHttpInfo(token, submissionId, setCreatorSparkCodeRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.SetCreatorSparkCodeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. |  |
| **submissionId** | **string** | The &#x60;id&#x60; of one of the participant&#39;s &#x60;submissions&#x60;. |  |
| **setCreatorSparkCodeRequest** | [**SetCreatorSparkCodeRequest**](SetCreatorSparkCodeRequest.md) |  |  |

### Return type

[**SetCreatorSparkCode200Response**](SetCreatorSparkCode200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Saved. |  -  |
| **400** | Invalid input, or the post is not a TikTok post (&#x60;invalid_field_value&#x60;). |  -  |
| **404** | The link is invalid or expired, or the post is not one of the participant&#39;s submissions (&#x60;resource_not_found&#x60;). |  -  |
| **409** | The post was rejected or withdrawn (&#x60;invalid_resource_state&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="startcreatorconnect"></a>
# **StartCreatorConnect**
> StartCreatorConnect200Response StartCreatorConnect (string token, StartCreatorConnectRequest startCreatorConnectRequest)

Start connecting a creator account

Returns the authorization URL that connects one of the creator's own social accounts, read-only, so their posts can be verified. Send the creator's browser to `authUrl`; they come back to their participant page. Only the campaign's platforms are accepted. 

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
    public class StartCreatorConnectExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | A participant token or an open invite token. A malformed token answers 404 like an unknown one.
            var startCreatorConnectRequest = new StartCreatorConnectRequest(); // StartCreatorConnectRequest | 

            try
            {
                // Start connecting a creator account
                StartCreatorConnect200Response result = apiInstance.StartCreatorConnect(token, startCreatorConnectRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.StartCreatorConnect: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the StartCreatorConnectWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Start connecting a creator account
    ApiResponse<StartCreatorConnect200Response> response = apiInstance.StartCreatorConnectWithHttpInfo(token, startCreatorConnectRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.StartCreatorConnectWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. |  |
| **startCreatorConnectRequest** | [**StartCreatorConnectRequest**](StartCreatorConnectRequest.md) |  |  |

### Return type

[**StartCreatorConnect200Response**](StartCreatorConnect200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Authorization URL. |  -  |
| **400** | The platform is not part of the campaign (&#x60;invalid_field_value&#x60;), the campaign allows no more connected accounts (\&quot;This campaign allows N connected accounts.\&quot;), or the campaign has ended (&#x60;invalid_resource_state&#x60;). |  -  |
| **404** | The token is malformed, unknown or expired. Every case answers the same, so a link can never be probed. |  -  |
| **409** | The creator&#39;s participation was suspended or removed (&#x60;invalid_resource_state&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="startcreatorpayouts"></a>
# **StartCreatorPayouts**
> StartCreatorPayouts200Response StartCreatorPayouts (string token, StartCreatorPayoutsRequest startCreatorPayoutsRequest)

Start payout onboarding

For a campaign that pays through the Zernio treasury: creates the creator's payee on first use and returns a Stripe-hosted onboarding link where they enter identity and bank details. `country` is required the first time and cannot change afterwards. About 20 attempts per participant every 10 minutes. 

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
    public class StartCreatorPayoutsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | A participant token or an open invite token. A malformed token answers 404 like an unknown one.
            var startCreatorPayoutsRequest = new StartCreatorPayoutsRequest(); // StartCreatorPayoutsRequest | 

            try
            {
                // Start payout onboarding
                StartCreatorPayouts200Response result = apiInstance.StartCreatorPayouts(token, startCreatorPayoutsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.StartCreatorPayouts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the StartCreatorPayoutsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Start payout onboarding
    ApiResponse<StartCreatorPayouts200Response> response = apiInstance.StartCreatorPayoutsWithHttpInfo(token, startCreatorPayoutsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.StartCreatorPayoutsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. |  |
| **startCreatorPayoutsRequest** | [**StartCreatorPayoutsRequest**](StartCreatorPayoutsRequest.md) |  |  |

### Return type

[**StartCreatorPayouts200Response**](StartCreatorPayouts200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Stripe onboarding link. |  -  |
| **400** | &#x60;country&#x60; is missing on the first call (\&quot;Choose the country you live in.\&quot;) or differs from the one already saved (\&quot;Payout country cannot be changed.\&quot;). |  -  |
| **404** | The token is malformed, unknown or expired. Every case answers the same, so a link can never be probed. |  -  |
| **409** | The campaign team pays the creator directly, so there is nothing to set up (&#x60;invalid_resource_state&#x60;). |  -  |
| **429** | Too many attempts from this link or IP address (&#x60;rate_limited&#x60;). Wait a few minutes and try again. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="submitcreatordraft"></a>
# **SubmitCreatorDraft**
> SubmitCreatorDraft201Response SubmitCreatorDraft (string token, SubmitCreatorDraftRequest submitCreatorDraftRequest)

Submit a draft for review

Sends a draft for the campaign team to review before the creator publishes, on a campaign with `requireDraftApproval`, and fires `campaign_draft.submitted`. `mediaUrl` must be a `publicUrl` from `POST /public/creator-campaigns/{token}/drafts/upload`.  ### Revisions  - Without `revisionOf` the draft starts a new chain at version 1. - With `revisionOf` it is the next version of that chain. Only one of the creator's own versions marked `revision_requested` takes a new version, and only once.  About 20 drafts per participant every 10 minutes. 

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
    public class SubmitCreatorDraftExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | A participant token or an open invite token. A malformed token answers 404 like an unknown one.
            var submitCreatorDraftRequest = new SubmitCreatorDraftRequest(); // SubmitCreatorDraftRequest | 

            try
            {
                // Submit a draft for review
                SubmitCreatorDraft201Response result = apiInstance.SubmitCreatorDraft(token, submitCreatorDraftRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.SubmitCreatorDraft: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubmitCreatorDraftWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Submit a draft for review
    ApiResponse<SubmitCreatorDraft201Response> response = apiInstance.SubmitCreatorDraftWithHttpInfo(token, submitCreatorDraftRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.SubmitCreatorDraftWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. |  |
| **submitCreatorDraftRequest** | [**SubmitCreatorDraftRequest**](SubmitCreatorDraftRequest.md) |  |  |

### Return type

[**SubmitCreatorDraft201Response**](SubmitCreatorDraft201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Draft submitted. |  -  |
| **400** | An invalid field, or &#x60;mediaUrl&#x60; is not a file uploaded for this campaign (&#x60;invalid_field_value&#x60;, &#x60;param: mediaUrl&#x60;, \&quot;Upload the file from your campaign page first\&quot;). |  -  |
| **404** | The token is malformed, unknown or expired. Every case answers the same, so a link can never be probed. |  -  |
| **409** | &#x60;invalid_resource_state&#x60;, and the message says which:  - The campaign does not review drafts or is not accepting posts. - The creator is not active in it (invite not accepted, pending, denied, suspended or removed). - &#x60;revisionOf&#x60; is not one of the creator&#39;s versions or is not &#x60;revision_requested&#x60;, or a newer version of it was already uploaded.  |  -  |
| **429** | Too many attempts from this link or IP address (&#x60;rate_limited&#x60;). Wait a few minutes and try again. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="submitcreatorpost"></a>
# **SubmitCreatorPost**
> SubmitCreatorPost201Response SubmitCreatorPost (string token, SubmitCreatorPostRequest submitCreatorPostRequest)

Submit a post

Submits the link to a post the creator published from a connected account. The post opens a tracking window and fires `campaign_submission.received` to the operator. About 30 attempts and 10 accepted posts per participant every 10 minutes. 

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
    public class SubmitCreatorPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CreatorPortalApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | A participant token or an open invite token. A malformed token answers 404 like an unknown one.
            var submitCreatorPostRequest = new SubmitCreatorPostRequest(); // SubmitCreatorPostRequest | 

            try
            {
                // Submit a post
                SubmitCreatorPost201Response result = apiInstance.SubmitCreatorPost(token, submitCreatorPostRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorPortalApi.SubmitCreatorPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubmitCreatorPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Submit a post
    ApiResponse<SubmitCreatorPost201Response> response = apiInstance.SubmitCreatorPostWithHttpInfo(token, submitCreatorPostRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorPortalApi.SubmitCreatorPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. |  |
| **submitCreatorPostRequest** | [**SubmitCreatorPostRequest**](SubmitCreatorPostRequest.md) |  |  |

### Return type

[**SubmitCreatorPost201Response**](SubmitCreatorPost201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Submitted. |  -  |
| **400** | The post cannot be submitted: 400 &#x60;invalid_field_value&#x60;.  - &#x60;param: url&#x60;: the link is not a post of an accepted platform, or the post was published before the campaign started or longer ago than the campaign accepts. - TikTok and X post ids carry their creation time, so a post from before the campaign is refused as such even when no connected account has it. - The post is from an account past the campaign&#39;s &#x60;caps.maxAccountsPerParticipant&#x60; (\&quot;This campaign allows 2 connected accounts.\&quot;). Only the first accounts the creator connected, up to that count, can submit. - &#x60;param: draftId&#x60; (&#x60;missing_required_field&#x60;): the campaign requires draft approval and no &#x60;draftId&#x60; was sent.  |  -  |
| **403** | The creator has not connected an account on that platform yet (&#x60;insufficient_permissions&#x60;, \&quot;Connect your TikTok account first, then submit the post again\&quot;). |  -  |
| **404** | The link is invalid or expired, or no connected account has the post (&#x60;resource_not_found&#x60;, &#x60;param: url&#x60;).  - When the link names its author (TikTok, Instagram, Threads, X) and that is not one of the creator&#39;s accounts, the message names both handles. - Otherwise it says the post was not found yet, for example because it was published moments ago.  |  -  |
| **409** | &#x60;invalid_resource_state&#x60;, and the message says which:  - The invite is not accepted yet, the creator is still pending approval or was denied, or the participation was suspended or removed. - The campaign is not accepting posts (not started, paused or ended). - The post was already submitted, or today&#39;s per-participant post limit is reached. - &#x60;draftId&#x60; is not one of the creator&#39;s approved drafts or already backs another post.  |  -  |
| **429** | Too many attempts from this link or IP address (&#x60;rate_limited&#x60;). Wait a few minutes and try again. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

