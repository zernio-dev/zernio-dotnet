# Zernio.Api.ContentRetentionApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetContentRetention**](ContentRetentionApi.md#getcontentretention) | **GET** /v1/content-retention | Get content retention mode |
| [**UpdateContentRetention**](ContentRetentionApi.md#updatecontentretention) | **PUT** /v1/content-retention | Turn zero content retention on or off |

<a id="getcontentretention"></a>
# **GetContentRetention**
> ContentRetentionResponse GetContentRetention ()

Get content retention mode

Returns whether your team stores content. `none` is zero content retention: Zernio keeps identifiers and metadata only, and content fields come back as `null` with `contentNotRetained: true`. See the zero content retention guide for what changes. 

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
    public class GetContentRetentionExample
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
            var apiInstance = new ContentRetentionApi(httpClient, config, httpClientHandler);

            try
            {
                // Get content retention mode
                ContentRetentionResponse result = apiInstance.GetContentRetention();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContentRetentionApi.GetContentRetention: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetContentRetentionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get content retention mode
    ApiResponse<ContentRetentionResponse> response = apiInstance.GetContentRetentionWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContentRetentionApi.GetContentRetentionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ContentRetentionResponse**](ContentRetentionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The team&#39;s content retention mode |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecontentretention"></a>
# **UpdateContentRetention**
> ContentRetentionResponse UpdateContentRetention (UpdateContentRetentionRequest updateContentRetentionRequest)

Turn zero content retention on or off

Sets your team's content retention mode for every member. Only the team owner can change it, with a signed-in session or a full-access API key.  - `none` turns on zero content retention: from then on Zernio stores no message text, comments, lead answers, mentions, post text after publishing, call transcripts or recordings. Webhooks become the only copy, so store each event when it arrives. - `standard` stores content again for new data. Content that was not stored cannot come back. - The change applies to new data within about 5 minutes. Content stored before it stays until it is deleted. 

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
    public class UpdateContentRetentionExample
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
            var apiInstance = new ContentRetentionApi(httpClient, config, httpClientHandler);
            var updateContentRetentionRequest = new UpdateContentRetentionRequest(); // UpdateContentRetentionRequest | 

            try
            {
                // Turn zero content retention on or off
                ContentRetentionResponse result = apiInstance.UpdateContentRetention(updateContentRetentionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContentRetentionApi.UpdateContentRetention: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateContentRetentionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Turn zero content retention on or off
    ApiResponse<ContentRetentionResponse> response = apiInstance.UpdateContentRetentionWithHttpInfo(updateContentRetentionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContentRetentionApi.UpdateContentRetentionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateContentRetentionRequest** | [**UpdateContentRetentionRequest**](UpdateContentRetentionRequest.md) |  |  |

### Return type

[**ContentRetentionResponse**](ContentRetentionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The mode now set |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Only the team owner can change the mode, on a signed-in session or a full-access API key (&#x60;insufficient_permissions&#x60;). Read-only, profile-scoped and restricted API keys and third-party OAuth tokens get 403 too. |  -  |
| **409** | Invalid resource state (&#x60;invalid_resource_state&#x60;): a Zernio phone number of the team has a WhatsApp verification in progress. Teams with zero content retention cannot receive the verification code, so finish or cancel it first. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

