# Zernio.Api.SlackApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ListSlackMembers**](SlackApi.md#listslackmembers) | **GET** /v1/accounts/{accountId}/slack-members | List Slack workspace members |

<a id="listslackmembers"></a>
# **ListSlackMembers**
> ListSlackMembers200Response ListSlackMembers (string accountId, string? query = null, int? limit = null)

List Slack workspace members

Members of the connected Slack workspace that can receive a direct message, for populating a recipient picker. Bots, deactivated members and Slackbot are excluded. Start a DM by passing a member id as `participantId` to POST /v1/inbox/conversations.

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
    public class ListSlackMembersExample
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
            var apiInstance = new SlackApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var query = "query_example";  // string? | Case-insensitive filter over display name and handle. (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)

            try
            {
                // List Slack workspace members
                ListSlackMembers200Response result = apiInstance.ListSlackMembers(accountId, query, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SlackApi.ListSlackMembers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListSlackMembersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Slack workspace members
    ApiResponse<ListSlackMembers200Response> response = apiInstance.ListSlackMembersWithHttpInfo(accountId, query, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SlackApi.ListSlackMembersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **query** | **string?** | Case-insensitive filter over display name and handle. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |

### Return type

[**ListSlackMembers200Response**](ListSlackMembers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Workspace members |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Slack account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

