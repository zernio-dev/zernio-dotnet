# Zernio.Api.InboxApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetWhatsAppMedia**](InboxApi.md#getwhatsappmedia) | **GET** /v1/whatsapp/media/{mediaId} | Download WhatsApp media |

<a id="getwhatsappmedia"></a>
# **GetWhatsAppMedia**
> FileParameter GetWhatsAppMedia (string mediaId, string accountId)

Download WhatsApp media

Streams the binary for a WhatsApp attachment. This is the endpoint the `url` on a WhatsApp `attachments[]` entry points at, in both the `message.received` webhook and the List messages response.  **This is an authenticated endpoint, not a public link.** Send `Authorization: Bearer <your API key>` exactly as you would for any other call. Passing the URL straight to a browser, an LLM vision API, or a no-code \"download file\" step without the header returns `401`. This is the most common integration mistake on this endpoint, and it differs from Instagram, Facebook and Telegram, whose `attachments[].url` is a direct CDN link that needs no header.  **Fetch on receipt, not lazily.** WhatsApp media lives in Meta's media store, not ours, and it is removed after a limited retention window (currently 7 days, and Meta has been dropping some inbound media sooner). Once Meta drops it the media is unrecoverable and this endpoint answers `400` permanently, so retrying will never succeed. Download and store the bytes when the webhook arrives. 

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
    public class GetWhatsAppMediaExample
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
            var apiInstance = new InboxApi(httpClient, config, httpClientHandler);
            var mediaId = "mediaId_example";  // string | The media id from `attachments[].payload.id`.
            var accountId = "accountId_example";  // string | The WhatsApp account that received the media.

            try
            {
                // Download WhatsApp media
                FileParameter result = apiInstance.GetWhatsAppMedia(mediaId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InboxApi.GetWhatsAppMedia: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWhatsAppMediaWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Download WhatsApp media
    ApiResponse<FileParameter> response = apiInstance.GetWhatsAppMediaWithHttpInfo(mediaId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InboxApi.GetWhatsAppMediaWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **mediaId** | **string** | The media id from &#x60;attachments[].payload.id&#x60;. |  |
| **accountId** | **string** | The WhatsApp account that received the media. |  |

### Return type

[**FileParameter**](FileParameter.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The media binary, streamed with its original content type. |  -  |
| **400** | Media is no longer available on WhatsApp servers (expired or deleted by Meta). Permanent, do not retry. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account not found, not accessible to the caller, or the media does not belong to it. |  -  |
| **502** | Meta could not be reached or returned an unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

