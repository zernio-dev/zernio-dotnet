# Zernio.Api.ToolsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DownloadTikTokVideo**](ToolsApi.md#downloadtiktokvideo) | **GET** /v1/tools/tiktok/download | Download a TikTok video |

<a id="downloadtiktokvideo"></a>
# **DownloadTikTokVideo**
> DownloadTikTokVideo200Response DownloadTikTokVideo (string url, string? action = null, string? formatId = null)

Download a TikTok video

Get a download URL or list available formats for a TikTok video. Requires Tools API access and uses the Tools API rate limit. Provider gateway failures and provider-side access blocks return 503; an unavailable video returns 404.

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
    public class DownloadTikTokVideoExample
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
            var apiInstance = new ToolsApi(httpClient, config, httpClientHandler);
            var url = https://www.tiktok.com/@example/video/7412345678901234567;  // string | TikTok video URL or numeric video ID.
            var action = "download";  // string? | Return a download URL or the available formats. (optional)  (default to download)
            var formatId = "formatId_example";  // string? | Format ID from the formats response. Omit to select the first available format. (optional) 

            try
            {
                // Download a TikTok video
                DownloadTikTokVideo200Response result = apiInstance.DownloadTikTokVideo(url, action, formatId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ToolsApi.DownloadTikTokVideo: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DownloadTikTokVideoWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Download a TikTok video
    ApiResponse<DownloadTikTokVideo200Response> response = apiInstance.DownloadTikTokVideoWithHttpInfo(url, action, formatId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ToolsApi.DownloadTikTokVideoWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **url** | **string** | TikTok video URL or numeric video ID. |  |
| **action** | **string?** | Return a download URL or the available formats. | [optional] [default to download] |
| **formatId** | **string?** | Format ID from the formats response. Omit to select the first available format. | [optional]  |

### Return type

[**DownloadTikTokVideo200Response**](DownloadTikTokVideo200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Download URL or available formats. |  -  |
| **400** | Missing or invalid url, action, or formatId. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Tools API access is required. |  -  |
| **404** | The video or a downloadable format was not found. |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted.  Reddit rate-limits per connected Reddit user (1000 requests per 10-minute window), and that budget is shared by every operation using that account. Retry after the window resets rather than retrying immediately; repeated calls while exhausted do not succeed and keep the budget spent.  |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |
| **502** | The platform returned a server error. |  -  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

