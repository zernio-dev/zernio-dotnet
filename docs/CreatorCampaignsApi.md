# Zernio.Api.CreatorCampaignsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ActivateCreatorCampaign**](CreatorCampaignsApi.md#activatecreatorcampaign) | **POST** /v1/creator-campaigns/{campaignId}/activate | Activate creator campaign |
| [**ApproveCampaignSubmission**](CreatorCampaignsApi.md#approvecampaignsubmission) | **POST** /v1/creator-campaigns/{campaignId}/submissions/{submissionId}/approve | Approve campaign submission |
| [**CloseCreatorCampaign**](CreatorCampaignsApi.md#closecreatorcampaign) | **POST** /v1/creator-campaigns/{campaignId}/close | Close creator campaign |
| [**CreateCampaignAdjustment**](CreatorCampaignsApi.md#createcampaignadjustment) | **POST** /v1/creator-campaigns/{campaignId}/adjustments | Create campaign adjustment |
| [**CreateCampaignInviteLink**](CreatorCampaignsApi.md#createcampaigninvitelink) | **POST** /v1/creator-campaigns/{campaignId}/invite-link | Create campaign invite link |
| [**CreateCampaignParticipant**](CreatorCampaignsApi.md#createcampaignparticipant) | **POST** /v1/creator-campaigns/{campaignId}/participants | Invite campaign participant |
| [**CreateCampaignPayoutBatch**](CreatorCampaignsApi.md#createcampaignpayoutbatch) | **POST** /v1/creator-campaigns/{campaignId}/payout-batches | Pay creators with one card payment |
| [**CreateCreatorCampaign**](CreatorCampaignsApi.md#createcreatorcampaign) | **POST** /v1/creator-campaigns | Create creator campaign |
| [**GetCampaignParticipant**](CreatorCampaignsApi.md#getcampaignparticipant) | **GET** /v1/creator-campaigns/{campaignId}/participants/{participantId} | Get campaign participant |
| [**GetCampaignReport**](CreatorCampaignsApi.md#getcampaignreport) | **GET** /v1/creator-campaigns/{campaignId}/report | Get campaign report |
| [**GetCampaignSubmission**](CreatorCampaignsApi.md#getcampaignsubmission) | **GET** /v1/creator-campaigns/{campaignId}/submissions/{submissionId} | Get campaign submission |
| [**GetCreatorCampaign**](CreatorCampaignsApi.md#getcreatorcampaign) | **GET** /v1/creator-campaigns/{campaignId} | Get creator campaign |
| [**ListCampaignLedger**](CreatorCampaignsApi.md#listcampaignledger) | **GET** /v1/creator-campaigns/{campaignId}/ledger | List campaign ledger |
| [**ListCampaignParticipants**](CreatorCampaignsApi.md#listcampaignparticipants) | **GET** /v1/creator-campaigns/{campaignId}/participants | List campaign participants |
| [**ListCampaignPayables**](CreatorCampaignsApi.md#listcampaignpayables) | **GET** /v1/creator-campaigns/{campaignId}/payables | List campaign payables |
| [**ListCampaignPayoutBatches**](CreatorCampaignsApi.md#listcampaignpayoutbatches) | **GET** /v1/creator-campaigns/{campaignId}/payout-batches | List payout batches |
| [**ListCampaignSubmissions**](CreatorCampaignsApi.md#listcampaignsubmissions) | **GET** /v1/creator-campaigns/{campaignId}/submissions | List campaign submissions |
| [**ListCreatorCampaigns**](CreatorCampaignsApi.md#listcreatorcampaigns) | **GET** /v1/creator-campaigns | List creator campaigns |
| [**PauseCreatorCampaign**](CreatorCampaignsApi.md#pausecreatorcampaign) | **POST** /v1/creator-campaigns/{campaignId}/pause | Pause creator campaign |
| [**RaiseCreatorCampaignBudget**](CreatorCampaignsApi.md#raisecreatorcampaignbudget) | **POST** /v1/creator-campaigns/{campaignId}/budget | Raise creator campaign budget |
| [**ReinstateCampaignParticipant**](CreatorCampaignsApi.md#reinstatecampaignparticipant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/reinstate | Reinstate campaign participant |
| [**RejectCampaignSubmission**](CreatorCampaignsApi.md#rejectcampaignsubmission) | **POST** /v1/creator-campaigns/{campaignId}/submissions/{submissionId}/reject | Reject campaign submission |
| [**RemoveCampaignParticipant**](CreatorCampaignsApi.md#removecampaignparticipant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/remove | Remove campaign participant |
| [**ReopenCampaignSubmission**](CreatorCampaignsApi.md#reopencampaignsubmission) | **POST** /v1/creator-campaigns/{campaignId}/submissions/{submissionId}/reopen | Reopen campaign submission |
| [**SettleCampaignParticipant**](CreatorCampaignsApi.md#settlecampaignparticipant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/settle | Settle campaign participant |
| [**SuspendCampaignParticipant**](CreatorCampaignsApi.md#suspendcampaignparticipant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/suspend | Suspend campaign participant |
| [**UpdateCreatorCampaign**](CreatorCampaignsApi.md#updatecreatorcampaign) | **PATCH** /v1/creator-campaigns/{campaignId} | Update creator campaign |

<a id="activatecreatorcampaign"></a>
# **ActivateCreatorCampaign**
> CreateCreatorCampaign201Response ActivateCreatorCampaign (string campaignId)

Activate creator campaign

Moves a `draft` or `paused` campaign to `active`, where creators can join and submit posts and tracked views accrue earnings. Needs at least one platform and a budget above zero; any other starting state answers 409. 

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
    public class ActivateCreatorCampaignExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.

            try
            {
                // Activate creator campaign
                CreateCreatorCampaign201Response result = apiInstance.ActivateCreatorCampaign(campaignId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.ActivateCreatorCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ActivateCreatorCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Activate creator campaign
    ApiResponse<CreateCreatorCampaign201Response> response = apiInstance.ActivateCreatorCampaignWithHttpInfo(campaignId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.ActivateCreatorCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |

### Return type

[**CreateCreatorCampaign201Response**](CreateCreatorCampaign201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="approvecampaignsubmission"></a>
# **ApproveCampaignSubmission**
> ApproveCampaignSubmission200Response ApproveCampaignSubmission (string campaignId, string submissionId, string? idempotencyKey = null)

Approve campaign submission

Approves a `tracking` or `pending_review` submission of an active campaign and fires `campaign_submission.approved`. The Zernio dashboard offers Approve only on `pending_review` (a post that needs a decision) and waits for `tracking` posts to get there; the API accepts `tracking` so an integration can approve early. What the post earned so far moves to owed and is held for the campaign's `holdDays`; later earnings post straight to owed. A per-post campaign pays `perApprovedPostCents` here. Any other state answers 409. The same post approved in another of your campaigns also answers 409 (`invalid_resource_state`, \"This post is already approved in another campaign of yours.\"), so one post never earns twice. 

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
    public class ApproveCampaignSubmissionExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var submissionId = "submissionId_example";  // string | Submission ID.
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. (optional) 

            try
            {
                // Approve campaign submission
                ApproveCampaignSubmission200Response result = apiInstance.ApproveCampaignSubmission(campaignId, submissionId, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.ApproveCampaignSubmission: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ApproveCampaignSubmissionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Approve campaign submission
    ApiResponse<ApproveCampaignSubmission200Response> response = apiInstance.ApproveCampaignSubmissionWithHttpInfo(campaignId, submissionId, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.ApproveCampaignSubmissionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **submissionId** | **string** | Submission ID. |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. | [optional]  |

### Return type

[**ApproveCampaignSubmission200Response**](ApproveCampaignSubmission200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Submission approved |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign or submission is not in a state that allows approval, or the same post is already approved in another of your campaigns (&#x60;invalid_resource_state&#x60;, \&quot;This post is already approved in another campaign of yours.\&quot;). Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="closecreatorcampaign"></a>
# **CloseCreatorCampaign**
> CreateCreatorCampaign201Response CloseCreatorCampaign (string campaignId)

Close creator campaign

Closes an `active` or `paused` campaign for good and fires `creator_campaign.closed`. Open tracking windows are cancelled. A pool campaign is split among participants at this moment by their approved eligible views, so closing a pool campaign answers 409 while any post still awaits review. A campaign also closes by itself once `endsAt` passed and every tracking window had its final read. 

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
    public class CloseCreatorCampaignExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.

            try
            {
                // Close creator campaign
                CreateCreatorCampaign201Response result = apiInstance.CloseCreatorCampaign(campaignId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.CloseCreatorCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CloseCreatorCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Close creator campaign
    ApiResponse<CreateCreatorCampaign201Response> response = apiInstance.CloseCreatorCampaignWithHttpInfo(campaignId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.CloseCreatorCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |

### Return type

[**CreateCreatorCampaign201Response**](CreateCreatorCampaign201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcampaignadjustment"></a>
# **CreateCampaignAdjustment**
> CreateCampaignAdjustment201Response CreateCampaignAdjustment (string campaignId, CreateCampaignAdjustmentRequest createCampaignAdjustmentRequest, string? idempotencyKey = null)

Create campaign adjustment

Posts a manual adjustment to a participant's payable balance against the campaign budget: a positive amount credits the participant (a bonus), a negative one claws back. `cause` is kept on the ledger entry. A claw-back larger than the payable balance answers 409. 

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
    public class CreateCampaignAdjustmentExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var createCampaignAdjustmentRequest = new CreateCampaignAdjustmentRequest(); // CreateCampaignAdjustmentRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. (optional) 

            try
            {
                // Create campaign adjustment
                CreateCampaignAdjustment201Response result = apiInstance.CreateCampaignAdjustment(campaignId, createCampaignAdjustmentRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.CreateCampaignAdjustment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCampaignAdjustmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create campaign adjustment
    ApiResponse<CreateCampaignAdjustment201Response> response = apiInstance.CreateCampaignAdjustmentWithHttpInfo(campaignId, createCampaignAdjustmentRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.CreateCampaignAdjustmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **createCampaignAdjustmentRequest** | [**CreateCampaignAdjustmentRequest**](CreateCampaignAdjustmentRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. | [optional]  |

### Return type

[**CreateCampaignAdjustment201Response**](CreateCampaignAdjustment201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Adjustment posted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcampaigninvitelink"></a>
# **CreateCampaignInviteLink**
> CreateCampaignInviteLink201Response CreateCampaignInviteLink (string campaignId)

Create campaign invite link

Creates the campaign's open invite link: anyone with it can join as a participant (up to `caps.maxParticipants`). Creating a new link revokes the previous one. The URL is returned only here. Answers 409 on a closed campaign. 

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
    public class CreateCampaignInviteLinkExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.

            try
            {
                // Create campaign invite link
                CreateCampaignInviteLink201Response result = apiInstance.CreateCampaignInviteLink(campaignId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.CreateCampaignInviteLink: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCampaignInviteLinkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create campaign invite link
    ApiResponse<CreateCampaignInviteLink201Response> response = apiInstance.CreateCampaignInviteLinkWithHttpInfo(campaignId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.CreateCampaignInviteLinkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |

### Return type

[**CreateCampaignInviteLink201Response**](CreateCampaignInviteLink201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Invite link created |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcampaignparticipant"></a>
# **CreateCampaignParticipant**
> CreateCampaignParticipant201Response CreateCampaignParticipant (string campaignId, CreateCampaignParticipantRequest createCampaignParticipantRequest, string? idempotencyKey = null)

Invite campaign participant

Invites one creator and returns their personal invite URL. Send it to the creator: on that page they connect their accounts (read-only), submit posts and see their earnings. The URL is returned only here; inviting again creates no second link (409 for a creator already in the campaign). A creator is matched by email within your workspace, so the same person keeps one identity across your campaigns.  Answers 409 on a closed campaign and 403 `feature_not_available` once `caps.maxParticipants` is reached. 

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
    public class CreateCampaignParticipantExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var createCampaignParticipantRequest = new CreateCampaignParticipantRequest(); // CreateCampaignParticipantRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. (optional) 

            try
            {
                // Invite campaign participant
                CreateCampaignParticipant201Response result = apiInstance.CreateCampaignParticipant(campaignId, createCampaignParticipantRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.CreateCampaignParticipant: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCampaignParticipantWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Invite campaign participant
    ApiResponse<CreateCampaignParticipant201Response> response = apiInstance.CreateCampaignParticipantWithHttpInfo(campaignId, createCampaignParticipantRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.CreateCampaignParticipantWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **createCampaignParticipantRequest** | [**CreateCampaignParticipantRequest**](CreateCampaignParticipantRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. | [optional]  |

### Return type

[**CreateCampaignParticipant201Response**](CreateCampaignParticipant201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Participant invited |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcampaignpayoutbatch"></a>
# **CreateCampaignPayoutBatch**
> CreateCampaignPayoutBatch201Response CreateCampaignPayoutBatch (string campaignId, string? idempotencyKey = null, CreateCampaignPayoutBatchRequest? createCampaignPayoutBatchRequest = null)

Pay creators with one card payment

Pays exactly what is owed: every payable creator of a `treasury` campaign who finished payout setup (or only `participantIds`, minus `excludeParticipantIds`) is held in `settling`, and the response carries a Stripe Checkout `url` for the total plus the fee (4% per creator, 50 cent minimum). Once the card payment completes, each creator gets a transfer funded by that charge and the batch ends `paid` or `partially_failed`. A creator whose payouts were disabled before the payment landed is skipped and stays payable. If the Checkout expires unpaid (24 hours), every amount is payable again.  Card payouts are limited to $2,000.00 gross per rolling 30 days by default; over it the call answers 402 (\"Over your instant payout limit. Top up your balance to pay more this month, or contact support to raise the limit.\"). Nothing payable answers 400 (\"Nothing is payable.\"). Needs an owner, admin or billing admin, signed in or through a full-access key they created. Send an `Idempotency-Key` so a retry never opens a second batch. 

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
    public class CreateCampaignPayoutBatchExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. (optional) 
            var createCampaignPayoutBatchRequest = new CreateCampaignPayoutBatchRequest?(); // CreateCampaignPayoutBatchRequest? |  (optional) 

            try
            {
                // Pay creators with one card payment
                CreateCampaignPayoutBatch201Response result = apiInstance.CreateCampaignPayoutBatch(campaignId, idempotencyKey, createCampaignPayoutBatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.CreateCampaignPayoutBatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCampaignPayoutBatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pay creators with one card payment
    ApiResponse<CreateCampaignPayoutBatch201Response> response = apiInstance.CreateCampaignPayoutBatchWithHttpInfo(campaignId, idempotencyKey, createCampaignPayoutBatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.CreateCampaignPayoutBatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. | [optional]  |
| **createCampaignPayoutBatchRequest** | [**CreateCampaignPayoutBatchRequest?**](CreateCampaignPayoutBatchRequest?.md) |  | [optional]  |

### Return type

[**CreateCampaignPayoutBatch201Response**](CreateCampaignPayoutBatch201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Batch created; send the operator to &#x60;url&#x60; to pay. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Over the instant payout limit (code &#x60;payment_required&#x60;). |  -  |
| **403** | Refused (&#x60;insufficient_permissions&#x60;). Either a restricted API key without the &#x60;money&#x60; resource group, or a profile-scoped API key: money leaves the whole team&#39;s balance, so moving it needs a full-access key or a signed-in session (\&quot;Moving money needs a full-access key or a signed-in session.\&quot;). A member or viewer is refused too, signed in or through a key they created: only an owner, admin or billing admin moves money.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcreatorcampaign"></a>
# **CreateCreatorCampaign**
> CreateCreatorCampaign201Response CreateCreatorCampaign (CreateCreatorCampaignRequest createCreatorCampaignRequest, string? idempotencyKey = null)

Create creator campaign

Creates a campaign in `draft`. Creators are paid for verified performance of the posts they submit: Zernio tracks each post through a tracking window, scores its authenticity and records every earning in a ledger. Activate the campaign to start accepting submissions.  Creator campaigns run on usage-based billing; a workspace not on it gets 403 `feature_not_available`. `profileId` must be a profile this key can reach, otherwise 404. 

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
    public class CreateCreatorCampaignExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var createCreatorCampaignRequest = new CreateCreatorCampaignRequest(); // CreateCreatorCampaignRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. (optional) 

            try
            {
                // Create creator campaign
                CreateCreatorCampaign201Response result = apiInstance.CreateCreatorCampaign(createCreatorCampaignRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.CreateCreatorCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCreatorCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create creator campaign
    ApiResponse<CreateCreatorCampaign201Response> response = apiInstance.CreateCreatorCampaignWithHttpInfo(createCreatorCampaignRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.CreateCreatorCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCreatorCampaignRequest** | [**CreateCreatorCampaignRequest**](CreateCreatorCampaignRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. | [optional]  |

### Return type

[**CreateCreatorCampaign201Response**](CreateCreatorCampaign201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Campaign created |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | Same Idempotency-Key still processing; retry after a short backoff |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcampaignparticipant"></a>
# **GetCampaignParticipant**
> GetCampaignParticipant200Response GetCampaignParticipant (string campaignId, string participantId)

Get campaign participant

Returns one participant with connected accounts, balances by state, flags and submission counts. 

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
    public class GetCampaignParticipantExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var participantId = "participantId_example";  // string | Participant ID.

            try
            {
                // Get campaign participant
                GetCampaignParticipant200Response result = apiInstance.GetCampaignParticipant(campaignId, participantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.GetCampaignParticipant: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCampaignParticipantWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get campaign participant
    ApiResponse<GetCampaignParticipant200Response> response = apiInstance.GetCampaignParticipantWithHttpInfo(campaignId, participantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.GetCampaignParticipantWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **participantId** | **string** | Participant ID. |  |

### Return type

[**GetCampaignParticipant200Response**](GetCampaignParticipant200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Participant |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcampaignreport"></a>
# **GetCampaignReport**
> GetCampaignReport200Response GetCampaignReport (string campaignId)

Get campaign report

Returns spend against budget, views, submission counts, the top ten participants by earnings and the authenticity score distribution. 

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
    public class GetCampaignReportExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.

            try
            {
                // Get campaign report
                GetCampaignReport200Response result = apiInstance.GetCampaignReport(campaignId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.GetCampaignReport: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCampaignReportWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get campaign report
    ApiResponse<GetCampaignReport200Response> response = apiInstance.GetCampaignReportWithHttpInfo(campaignId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.GetCampaignReportWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |

### Return type

[**GetCampaignReport200Response**](GetCampaignReport200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign report |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcampaignsubmission"></a>
# **GetCampaignSubmission**
> GetCampaignSubmission200Response GetCampaignSubmission (string campaignId, string submissionId)

Get campaign submission

Returns one submission with its per-sync samples (views, likes, comments, shares, saves). 

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
    public class GetCampaignSubmissionExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var submissionId = "submissionId_example";  // string | Submission ID.

            try
            {
                // Get campaign submission
                GetCampaignSubmission200Response result = apiInstance.GetCampaignSubmission(campaignId, submissionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.GetCampaignSubmission: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCampaignSubmissionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get campaign submission
    ApiResponse<GetCampaignSubmission200Response> response = apiInstance.GetCampaignSubmissionWithHttpInfo(campaignId, submissionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.GetCampaignSubmissionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **submissionId** | **string** | Submission ID. |  |

### Return type

[**GetCampaignSubmission200Response**](GetCampaignSubmission200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Submission |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcreatorcampaign"></a>
# **GetCreatorCampaign**
> CreateCreatorCampaign201Response GetCreatorCampaign (string campaignId)

Get creator campaign

Returns the campaign with its budget consumption, participant count and submission counts. 

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
    public class GetCreatorCampaignExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.

            try
            {
                // Get creator campaign
                CreateCreatorCampaign201Response result = apiInstance.GetCreatorCampaign(campaignId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.GetCreatorCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCreatorCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get creator campaign
    ApiResponse<CreateCreatorCampaign201Response> response = apiInstance.GetCreatorCampaignWithHttpInfo(campaignId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.GetCreatorCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |

### Return type

[**CreateCreatorCampaign201Response**](CreateCreatorCampaign201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcampaignledger"></a>
# **ListCampaignLedger**
> ListCampaignLedger200Response ListCampaignLedger (string campaignId, string? participantId = null, string? kind = null, int? limit = null, int? skip = null)

List campaign ledger

Lists ledger entries, newest first. Without `participantId` it lists every entry of the campaign: earnings drawn from the budget (accruals, per-post payments, pool shares, adjustments), the approvals, hold releases and settlements that move money between its participants' buckets, and their reversals. Pass `participantId` to narrow the list to one participant's entries. 

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
    public class ListCampaignLedgerExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var participantId = "participantId_example";  // string? | List only this participant's entries. (optional) 
            var kind = "accrual";  // string? |  (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List campaign ledger
                ListCampaignLedger200Response result = apiInstance.ListCampaignLedger(campaignId, participantId, kind, limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.ListCampaignLedger: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCampaignLedgerWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List campaign ledger
    ApiResponse<ListCampaignLedger200Response> response = apiInstance.ListCampaignLedgerWithHttpInfo(campaignId, participantId, kind, limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.ListCampaignLedgerWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **participantId** | **string?** | List only this participant&#39;s entries. | [optional]  |
| **kind** | **string?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**ListCampaignLedger200Response**](ListCampaignLedger200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ledger entries |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcampaignparticipants"></a>
# **ListCampaignParticipants**
> ListCampaignParticipants200Response ListCampaignParticipants (string campaignId, string? status = null, int? limit = null, int? skip = null)

List campaign participants

Lists the campaign's participants with their balances, flags and submission counts. 

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
    public class ListCampaignParticipantsExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var status = "invited";  // string? |  (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List campaign participants
                ListCampaignParticipants200Response result = apiInstance.ListCampaignParticipants(campaignId, status, limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.ListCampaignParticipants: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCampaignParticipantsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List campaign participants
    ApiResponse<ListCampaignParticipants200Response> response = apiInstance.ListCampaignParticipantsWithHttpInfo(campaignId, status, limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.ListCampaignParticipantsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **status** | **string?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**ListCampaignParticipants200Response**](ListCampaignParticipants200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Participants |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcampaignpayables"></a>
# **ListCampaignPayables**
> ListCampaignPayables200Response ListCampaignPayables (string campaignId)

List campaign payables

Lists every participant with a payable balance (earnings past their hold), with the ledger entries behind it. Pay these, then record each payout with the settle endpoint. 

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
    public class ListCampaignPayablesExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.

            try
            {
                // List campaign payables
                ListCampaignPayables200Response result = apiInstance.ListCampaignPayables(campaignId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.ListCampaignPayables: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCampaignPayablesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List campaign payables
    ApiResponse<ListCampaignPayables200Response> response = apiInstance.ListCampaignPayablesWithHttpInfo(campaignId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.ListCampaignPayablesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |

### Return type

[**ListCampaignPayables200Response**](ListCampaignPayables200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payables |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcampaignpayoutbatches"></a>
# **ListCampaignPayoutBatches**
> ListCampaignPayoutBatches200Response ListCampaignPayoutBatches (string campaignId, int? limit = null, int? skip = null)

List payout batches

The campaign's payout batches, newest first, with each creator's item.

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
    public class ListCampaignPayoutBatchesExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var limit = 20;  // int? |  (optional)  (default to 20)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List payout batches
                ListCampaignPayoutBatches200Response result = apiInstance.ListCampaignPayoutBatches(campaignId, limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.ListCampaignPayoutBatches: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCampaignPayoutBatchesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List payout batches
    ApiResponse<ListCampaignPayoutBatches200Response> response = apiInstance.ListCampaignPayoutBatchesWithHttpInfo(campaignId, limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.ListCampaignPayoutBatchesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **limit** | **int?** |  | [optional] [default to 20] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**ListCampaignPayoutBatches200Response**](ListCampaignPayoutBatches200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payout batches. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcampaignsubmissions"></a>
# **ListCampaignSubmissions**
> ListCampaignSubmissions200Response ListCampaignSubmissions (string campaignId, string? status = null, string? participantId = null, string? flag = null, string? platform = null, int? minScore = null, int? maxScore = null, string? q = null, string? sort = null, string? order = null, int? limit = null, int? skip = null)

List campaign submissions

Lists submitted posts with views, earnings, authenticity score and flags. Filter by status, participant, flag, platform or score range to build a review queue, for example `status=pending_review`. 

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
    public class ListCampaignSubmissionsExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var status = "received";  // string? |  (optional) 
            var participantId = "participantId_example";  // string? |  (optional) 
            var flag = "duplicate_media";  // string? |  (optional) 
            var platform = "tiktok";  // string? |  (optional) 
            var minScore = 56;  // int? |  (optional) 
            var maxScore = 56;  // int? |  (optional) 
            var q = "q_example";  // string? | Only submissions whose creator name or post link contains this text, ignoring case. (optional) 
            var sort = "submittedAt";  // string? | What to sort by. Posts with no value to sort by (not read yet, not scored) come last in either direction. (optional)  (default to submittedAt)
            var order = "asc";  // string? |  (optional)  (default to desc)
            var limit = 50;  // int? |  (optional)  (default to 50)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List campaign submissions
                ListCampaignSubmissions200Response result = apiInstance.ListCampaignSubmissions(campaignId, status, participantId, flag, platform, minScore, maxScore, q, sort, order, limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.ListCampaignSubmissions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCampaignSubmissionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List campaign submissions
    ApiResponse<ListCampaignSubmissions200Response> response = apiInstance.ListCampaignSubmissionsWithHttpInfo(campaignId, status, participantId, flag, platform, minScore, maxScore, q, sort, order, limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.ListCampaignSubmissionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **status** | **string?** |  | [optional]  |
| **participantId** | **string?** |  | [optional]  |
| **flag** | **string?** |  | [optional]  |
| **platform** | **string?** |  | [optional]  |
| **minScore** | **int?** |  | [optional]  |
| **maxScore** | **int?** |  | [optional]  |
| **q** | **string?** | Only submissions whose creator name or post link contains this text, ignoring case. | [optional]  |
| **sort** | **string?** | What to sort by. Posts with no value to sort by (not read yet, not scored) come last in either direction. | [optional] [default to submittedAt] |
| **order** | **string?** |  | [optional] [default to desc] |
| **limit** | **int?** |  | [optional] [default to 50] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**ListCampaignSubmissions200Response**](ListCampaignSubmissions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Submissions |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcreatorcampaigns"></a>
# **ListCreatorCampaigns**
> ListCreatorCampaigns200Response ListCreatorCampaigns (string? status = null, string? profileId = null, string? q = null, int? limit = null, int? skip = null)

List creator campaigns

Lists the team's campaigns in the profiles this key can reach, newest first. 

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
    public class ListCreatorCampaignsExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var status = "draft";  // string? |  (optional) 
            var profileId = "profileId_example";  // string? | Only campaigns in this profile. (optional) 
            var q = "q_example";  // string? | Only campaigns whose name or brand name contains this text, ignoring case. (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List creator campaigns
                ListCreatorCampaigns200Response result = apiInstance.ListCreatorCampaigns(status, profileId, q, limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.ListCreatorCampaigns: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCreatorCampaignsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List creator campaigns
    ApiResponse<ListCreatorCampaigns200Response> response = apiInstance.ListCreatorCampaignsWithHttpInfo(status, profileId, q, limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.ListCreatorCampaignsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **status** | **string?** |  | [optional]  |
| **profileId** | **string?** | Only campaigns in this profile. | [optional]  |
| **q** | **string?** | Only campaigns whose name or brand name contains this text, ignoring case. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**ListCreatorCampaigns200Response**](ListCreatorCampaigns200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaigns |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="pausecreatorcampaign"></a>
# **PauseCreatorCampaign**
> CreateCreatorCampaign201Response PauseCreatorCampaign (string campaignId)

Pause creator campaign

Moves an `active` campaign to `paused`: no new submissions, and approvals answer 409 until the campaign is activated again. 

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
    public class PauseCreatorCampaignExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.

            try
            {
                // Pause creator campaign
                CreateCreatorCampaign201Response result = apiInstance.PauseCreatorCampaign(campaignId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.PauseCreatorCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PauseCreatorCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pause creator campaign
    ApiResponse<CreateCreatorCampaign201Response> response = apiInstance.PauseCreatorCampaignWithHttpInfo(campaignId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.PauseCreatorCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |

### Return type

[**CreateCreatorCampaign201Response**](CreateCreatorCampaign201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="raisecreatorcampaignbudget"></a>
# **RaiseCreatorCampaignBudget**
> CreateCreatorCampaign201Response RaiseCreatorCampaignBudget (string campaignId, RaiseCreatorCampaignBudgetRequest raiseCreatorCampaignBudgetRequest, string? idempotencyKey = null)

Raise creator campaign budget

Raises the budget of a campaign that is `draft`, `active` or `paused`. Only the budget changes; the pay terms stay as creators joined them, which `PATCH` refuses to change once the campaign is live. The new `budgetCents` must be above the current budget, otherwise 400 `invalid_field_value`. When it is also above what the campaign has spent, `budgetExhaustedAt` is cleared and earnings that stopped at the old budget resume. A closed campaign answers 409 `invalid_resource_state`. 

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
    public class RaiseCreatorCampaignBudgetExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var raiseCreatorCampaignBudgetRequest = new RaiseCreatorCampaignBudgetRequest(); // RaiseCreatorCampaignBudgetRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. (optional) 

            try
            {
                // Raise creator campaign budget
                CreateCreatorCampaign201Response result = apiInstance.RaiseCreatorCampaignBudget(campaignId, raiseCreatorCampaignBudgetRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.RaiseCreatorCampaignBudget: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RaiseCreatorCampaignBudgetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Raise creator campaign budget
    ApiResponse<CreateCreatorCampaign201Response> response = apiInstance.RaiseCreatorCampaignBudgetWithHttpInfo(campaignId, raiseCreatorCampaignBudgetRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.RaiseCreatorCampaignBudgetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **raiseCreatorCampaignBudgetRequest** | [**RaiseCreatorCampaignBudgetRequest**](RaiseCreatorCampaignBudgetRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. | [optional]  |

### Return type

[**CreateCreatorCampaign201Response**](CreateCreatorCampaign201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Budget raised |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="reinstatecampaignparticipant"></a>
# **ReinstateCampaignParticipant**
> GetCampaignParticipant200Response ReinstateCampaignParticipant (string campaignId, string participantId)

Reinstate campaign participant

Reinstates a `suspended` participant: they can submit posts again. Any other status answers 409; a removed participant stays removed. 

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
    public class ReinstateCampaignParticipantExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var participantId = "participantId_example";  // string | Participant ID.

            try
            {
                // Reinstate campaign participant
                GetCampaignParticipant200Response result = apiInstance.ReinstateCampaignParticipant(campaignId, participantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.ReinstateCampaignParticipant: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReinstateCampaignParticipantWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reinstate campaign participant
    ApiResponse<GetCampaignParticipant200Response> response = apiInstance.ReinstateCampaignParticipantWithHttpInfo(campaignId, participantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.ReinstateCampaignParticipantWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **participantId** | **string** | Participant ID. |  |

### Return type

[**GetCampaignParticipant200Response**](GetCampaignParticipant200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Participant reinstated |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="rejectcampaignsubmission"></a>
# **RejectCampaignSubmission**
> ApproveCampaignSubmission200Response RejectCampaignSubmission (string campaignId, string submissionId, RejectCampaignSubmissionRequest rejectCampaignSubmissionRequest, string? idempotencyKey = null)

Reject campaign submission

Rejects a submission (also one already approved) and fires `campaign_submission.rejected`. Its tracking window is cancelled and its unsettled earnings return to the campaign budget. Rejecting a rejected submission returns it unchanged; an expired or withdrawn one answers 409. 

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
    public class RejectCampaignSubmissionExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var submissionId = "submissionId_example";  // string | Submission ID.
            var rejectCampaignSubmissionRequest = new RejectCampaignSubmissionRequest(); // RejectCampaignSubmissionRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. (optional) 

            try
            {
                // Reject campaign submission
                ApproveCampaignSubmission200Response result = apiInstance.RejectCampaignSubmission(campaignId, submissionId, rejectCampaignSubmissionRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.RejectCampaignSubmission: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RejectCampaignSubmissionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reject campaign submission
    ApiResponse<ApproveCampaignSubmission200Response> response = apiInstance.RejectCampaignSubmissionWithHttpInfo(campaignId, submissionId, rejectCampaignSubmissionRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.RejectCampaignSubmissionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **submissionId** | **string** | Submission ID. |  |
| **rejectCampaignSubmissionRequest** | [**RejectCampaignSubmissionRequest**](RejectCampaignSubmissionRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. | [optional]  |

### Return type

[**ApproveCampaignSubmission200Response**](ApproveCampaignSubmission200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Submission rejected |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removecampaignparticipant"></a>
# **RemoveCampaignParticipant**
> GetCampaignParticipant200Response RemoveCampaignParticipant (string campaignId, string participantId)

Remove campaign participant

Removes the participant from the campaign. Their earnings stay in the ledger. Removing an already removed participant returns it unchanged. 

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
    public class RemoveCampaignParticipantExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var participantId = "participantId_example";  // string | Participant ID.

            try
            {
                // Remove campaign participant
                GetCampaignParticipant200Response result = apiInstance.RemoveCampaignParticipant(campaignId, participantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.RemoveCampaignParticipant: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveCampaignParticipantWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove campaign participant
    ApiResponse<GetCampaignParticipant200Response> response = apiInstance.RemoveCampaignParticipantWithHttpInfo(campaignId, participantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.RemoveCampaignParticipantWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **participantId** | **string** | Participant ID. |  |

### Return type

[**GetCampaignParticipant200Response**](GetCampaignParticipant200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Participant removed |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="reopencampaignsubmission"></a>
# **ReopenCampaignSubmission**
> ApproveCampaignSubmission200Response ReopenCampaignSubmission (string campaignId, string submissionId, string? idempotencyKey = null)

Reopen campaign submission

Puts a rejected submission back to `pending_review` so it can be decided again. Its tracking window resumes, so it works only while that window has not ended; otherwise 409 `invalid_resource_state` (\"This post's tracking window has ended.\"). A post that earned money which was already paid out cannot be reopened, and neither can a post of a closed campaign. Reopening a submission that is already `pending_review` returns it unchanged; any other status answers 409. No webhook fires. 

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
    public class ReopenCampaignSubmissionExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var submissionId = "submissionId_example";  // string | Submission ID.
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. (optional) 

            try
            {
                // Reopen campaign submission
                ApproveCampaignSubmission200Response result = apiInstance.ReopenCampaignSubmission(campaignId, submissionId, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.ReopenCampaignSubmission: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReopenCampaignSubmissionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reopen campaign submission
    ApiResponse<ApproveCampaignSubmission200Response> response = apiInstance.ReopenCampaignSubmissionWithHttpInfo(campaignId, submissionId, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.ReopenCampaignSubmissionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **submissionId** | **string** | Submission ID. |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. | [optional]  |

### Return type

[**ApproveCampaignSubmission200Response**](ApproveCampaignSubmission200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Submission reopened |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="settlecampaignparticipant"></a>
# **SettleCampaignParticipant**
> SettleCampaignParticipant201Response SettleCampaignParticipant (string campaignId, string participantId, SettleCampaignParticipantRequest settleCampaignParticipantRequest, string? idempotencyKey = null)

Settle campaign participant

Records a payout of the participant's payable balance and fires `campaign_payout.settled`. Omit `amountCents` to settle the whole payable balance; an amount above it answers 400, and nothing payable answers 409.  - `none` settlement: records a payout you made elsewhere. - `external` settlement: pay from your own rails when `campaign_payout.payable` fires, then   call this with your payout id in `externalReference` (required in this mode). - `treasury` settlement: transfers the amount from your Zernio balance to the creator's   connected Stripe account, then records it with the Stripe transfer id as `externalReference`.   The transfer fee (4%, $0.50 minimum) is added on top: the creator receives the full amount   and your balance is debited `totalCents`. The creator must have finished payout setup from   their campaign page (409 otherwise), and a balance that does not cover the amount plus the   fee answers 402. While Stripe confirms the transfer the amount sits in the participant's   `settling` balance: a reject in that window cannot reverse it. If Stripe refuses the transfer   the amount returns to payable; if Stripe does not answer, the amount stays in `settling` and   the next settle call for this participant finishes that payout first (even with nothing   payable left). A retry asking for a different `amountCents` than the payout in progress   answers 409 with the amount in progress, and a settle while another request is still   waiting on Stripe for the same payout answers 409 (\"This payout is being sent to Stripe   right now. Try again in a minute.\"). A payout Stripe has not confirmed after 24 hours answers   409 (\"This payout is being confirmed with Stripe. Try again after the next reconciliation   (within 24 hours).\") until the daily reconciliation finishes it: settled if Stripe made the   transfer, returned to payable if it did not.   Set `recordOnly: true` to record a payout you made yourself instead of moving money through   the treasury (the webhook then carries `recorded: true`).   A treasury payout needs an owner, admin or billing admin, signed in or through a full-access   key they created (403 otherwise); recording with `recordOnly` does not. A creator held by an unfinished   payout batch answers 409 (\"This creator is in a card payout that is not finished yet.\").  Send an `Idempotency-Key` so a retry never records the payout twice. 

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
    public class SettleCampaignParticipantExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var participantId = "participantId_example";  // string | Participant ID.
            var settleCampaignParticipantRequest = new SettleCampaignParticipantRequest(); // SettleCampaignParticipantRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. (optional) 

            try
            {
                // Settle campaign participant
                SettleCampaignParticipant201Response result = apiInstance.SettleCampaignParticipant(campaignId, participantId, settleCampaignParticipantRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.SettleCampaignParticipant: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SettleCampaignParticipantWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Settle campaign participant
    ApiResponse<SettleCampaignParticipant201Response> response = apiInstance.SettleCampaignParticipantWithHttpInfo(campaignId, participantId, settleCampaignParticipantRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.SettleCampaignParticipantWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **participantId** | **string** | Participant ID. |  |
| **settleCampaignParticipantRequest** | [**SettleCampaignParticipantRequest**](SettleCampaignParticipantRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. | [optional]  |

### Return type

[**SettleCampaignParticipant201Response**](SettleCampaignParticipant201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Settlement recorded |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Your Zernio balance does not cover the amount plus the fee on top (code &#x60;payment_required&#x60;). Top up and retry. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |
| **502** | Stripe did not confirm the transfer (code &#x60;temporarily_unavailable&#x60;). Retry the settle call: the transfer is not made twice within Stripe&#39;s 24-hour idempotency window; after that, retries answer 409 until the daily reconciliation settles the payout or returns it to payable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="suspendcampaignparticipant"></a>
# **SuspendCampaignParticipant**
> GetCampaignParticipant200Response SuspendCampaignParticipant (string campaignId, string participantId)

Suspend campaign participant

Suspends an `active` participant: they can no longer submit posts. Any other status answers 409. 

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
    public class SuspendCampaignParticipantExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var participantId = "participantId_example";  // string | Participant ID.

            try
            {
                // Suspend campaign participant
                GetCampaignParticipant200Response result = apiInstance.SuspendCampaignParticipant(campaignId, participantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.SuspendCampaignParticipant: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SuspendCampaignParticipantWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Suspend campaign participant
    ApiResponse<GetCampaignParticipant200Response> response = apiInstance.SuspendCampaignParticipantWithHttpInfo(campaignId, participantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.SuspendCampaignParticipantWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **participantId** | **string** | Participant ID. |  |

### Return type

[**GetCampaignParticipant200Response**](GetCampaignParticipant200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Participant suspended |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecreatorcampaign"></a>
# **UpdateCreatorCampaign**
> CreateCreatorCampaign201Response UpdateCreatorCampaign (string campaignId, UpdateCreatorCampaignRequest updateCreatorCampaignRequest)

Update creator campaign

Updates any subset of the campaign's settings. `economics` (and with it the campaign type) can only change while the campaign is a draft; afterwards that answers 409, and a live campaign's budget is raised with `POST /v1/creator-campaigns/{campaignId}/budget`. An empty body answers 400. 

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
    public class UpdateCreatorCampaignExample
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
            var apiInstance = new CreatorCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Campaign ID.
            var updateCreatorCampaignRequest = new UpdateCreatorCampaignRequest(); // UpdateCreatorCampaignRequest | 

            try
            {
                // Update creator campaign
                CreateCreatorCampaign201Response result = apiInstance.UpdateCreatorCampaign(campaignId, updateCreatorCampaignRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreatorCampaignsApi.UpdateCreatorCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCreatorCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update creator campaign
    ApiResponse<CreateCreatorCampaign201Response> response = apiInstance.UpdateCreatorCampaignWithHttpInfo(campaignId, updateCreatorCampaignRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreatorCampaignsApi.UpdateCreatorCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Campaign ID. |  |
| **updateCreatorCampaignRequest** | [**UpdateCreatorCampaignRequest**](UpdateCreatorCampaignRequest.md) |  |  |

### Return type

[**CreateCreatorCampaign201Response**](CreateCreatorCampaign201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused. Code &#x60;feature_not_available&#x60;: creator campaigns run on usage-based billing and the workspace that owns the campaign is not on it yet (\&quot;Creator campaigns require usage-based billing...\&quot;; contact support to switch), or the campaign reached &#x60;caps.maxParticipants&#x60; (invites and joins only). Code &#x60;insufficient_permissions&#x60;: a restricted API key without the &#x60;creator_campaigns&#x60; resource group.  |  -  |
| **404** | The campaign, participant or submission does not exist, belongs to another team, or sits in a profile this key cannot reach (code &#x60;resource_not_found&#x60;). |  -  |
| **409** | The campaign, participant or submission is not in a state that allows this action (code &#x60;invalid_resource_state&#x60;); the message names the current state. Also returned while the same &#x60;Idempotency-Key&#x60; is still processing. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

