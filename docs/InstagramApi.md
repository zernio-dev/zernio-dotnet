# Zernio.Api.InstagramApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetInstagramStoryInsights**](InstagramApi.md#getinstagramstoryinsights) | **GET** /v1/accounts/{accountId}/instagram/stories/{storyId}/insights | Get Instagram story insights |
| [**ListInstagramStories**](InstagramApi.md#listinstagramstories) | **GET** /v1/accounts/{accountId}/instagram/stories | List active Instagram stories |

<a id="getinstagramstoryinsights"></a>
# **GetInstagramStoryInsights**
> GetInstagramStoryInsights200Response GetInstagramStoryInsights (string accountId, string storyId)

Get Instagram story insights

Returns metrics for a single story. The `source` field discriminates between three states:  - `live` — fetched from Meta in real time (story is still active) - `cached` — fetched from a persisted `story_insights` webhook payload   (story has expired but we received its final-state metrics from Meta) - `unavailable` — story has expired and we never received its webhook   payload (for example, the account connected after the story expired)  Field semantics follow Meta's API. Counts below 5 may be returned as 0 due to Meta's privacy floor on small audiences. The `navigation` field is the sum of `tapsForward + tapsBack + exits + swipesForward`. 

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
    public class GetInstagramStoryInsightsExample
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
            var apiInstance = new InstagramApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The Instagram account ID
            var storyId = "storyId_example";  // string | The Instagram media ID of the story.

            try
            {
                // Get Instagram story insights
                GetInstagramStoryInsights200Response result = apiInstance.GetInstagramStoryInsights(accountId, storyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstagramApi.GetInstagramStoryInsights: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInstagramStoryInsightsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Instagram story insights
    ApiResponse<GetInstagramStoryInsights200Response> response = apiInstance.GetInstagramStoryInsightsWithHttpInfo(accountId, storyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstagramApi.GetInstagramStoryInsightsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The Instagram account ID |  |
| **storyId** | **string** | The Instagram media ID of the story. |  |

### Return type

[**GetInstagramStoryInsights200Response**](GetInstagramStoryInsights200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Story insights |  -  |
| **400** | Invalid request. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Instagram account not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listinstagramstories"></a>
# **ListInstagramStories**
> ListInstagramStories200Response ListInstagramStories (string accountId)

List active Instagram stories

Returns the IG Business/Creator account's currently-active stories. Meta keeps stories live for 24h; expired stories are not returned.  Limitations propagated from Meta (these are NOT bugs): - 24h window only - Live videos excluded - Reshared stories not returned - `mediaUrl` may be null if Meta flagged the story for copyright - `caption`, `likeCount`, `commentsCount` do not apply to story media 

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
    public class ListInstagramStoriesExample
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
            var apiInstance = new InstagramApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The Instagram account ID

            try
            {
                // List active Instagram stories
                ListInstagramStories200Response result = apiInstance.ListInstagramStories(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstagramApi.ListInstagramStories: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListInstagramStoriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List active Instagram stories
    ApiResponse<ListInstagramStories200Response> response = apiInstance.ListInstagramStoriesWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstagramApi.ListInstagramStoriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The Instagram account ID |  |

### Return type

[**ListInstagramStories200Response**](ListInstagramStories200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Active stories |  -  |
| **400** | Invalid request. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Instagram account not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

