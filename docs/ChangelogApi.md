# Zernio.Api.ChangelogApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ListChangelog**](ChangelogApi.md#listchangelog) | **GET** /v1/changelog | List API changelog entries |

<a id="listchangelog"></a>
# **ListChangelog**
> ListChangelog200Response ListChangelog (string? type = null, string? platform = null, DateTime? before = null, int? limit = null)

List API changelog entries

The API changelog, newest first. Each entry is what the `api.changelog.published` webhook delivered: the announcement in `message`, and in `changes` the deterministic diff of the OpenAPI spec (operations and schemas added, removed and modified) for automation to act on. Page with `before` set to the previous page's `nextCursor`. 

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
    public class ListChangelogExample
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
            var apiInstance = new ChangelogApi(httpClient, config, httpClientHandler);
            var type = "new_feature";  // string? | Only entries of this type. (optional) 
            var platform = whatsapp;  // string? | Only entries tagged with this platform or area slug (see `platforms` on the entry). One slug per request. (optional) 
            var before = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | Only entries published strictly before this instant. Pass the previous page's `nextCursor`. (optional) 
            var limit = 20;  // int? |  (optional)  (default to 20)

            try
            {
                // List API changelog entries
                ListChangelog200Response result = apiInstance.ListChangelog(type, platform, before, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ChangelogApi.ListChangelog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListChangelogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List API changelog entries
    ApiResponse<ListChangelog200Response> response = apiInstance.ListChangelogWithHttpInfo(type, platform, before, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ChangelogApi.ListChangelogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **type** | **string?** | Only entries of this type. | [optional]  |
| **platform** | **string?** | Only entries tagged with this platform or area slug (see &#x60;platforms&#x60; on the entry). One slug per request. | [optional]  |
| **before** | **DateTime?** | Only entries published strictly before this instant. Pass the previous page&#39;s &#x60;nextCursor&#x60;. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 20] |

### Return type

[**ListChangelog200Response**](ListChangelog200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Changelog entries |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

