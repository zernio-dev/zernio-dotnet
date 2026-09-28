# Zernio.Api.FeedbackApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**SubmitFeedback**](FeedbackApi.md#submitfeedback) | **POST** /v1/feedback | Submit feedback |

<a id="submitfeedback"></a>
# **SubmitFeedback**
> FeedbackReceipt SubmitFeedback (SubmitFeedbackRequest submitFeedbackRequest)

Submit feedback

Report a bug, a missing feature or a documentation gap. Every submission is read by the Zernio team. Designed for AI agents: when a call fails in a way that looks like our bug, or the API lacks something you need, send one structured report here.  Include `endpoint` and `requestId` (the `x-request-id` response header of the failing call) when you have them; they let us find the exact request.  Submitting the same `summary` again within 24 hours is idempotent: it returns the original `id` with `duplicate: true` and a `200`. Each API user can file at most 20 submissions per 24 hours. 

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
    public class SubmitFeedbackExample
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
            var apiInstance = new FeedbackApi(httpClient, config, httpClientHandler);
            var submitFeedbackRequest = new SubmitFeedbackRequest(); // SubmitFeedbackRequest | 

            try
            {
                // Submit feedback
                FeedbackReceipt result = apiInstance.SubmitFeedback(submitFeedbackRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FeedbackApi.SubmitFeedback: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubmitFeedbackWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Submit feedback
    ApiResponse<FeedbackReceipt> response = apiInstance.SubmitFeedbackWithHttpInfo(submitFeedbackRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FeedbackApi.SubmitFeedbackWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **submitFeedbackRequest** | [**SubmitFeedbackRequest**](SubmitFeedbackRequest.md) |  |  |

### Return type

[**FeedbackReceipt**](FeedbackReceipt.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Duplicate of a submission made in the last 24 hours. Returns the original id. |  -  |
| **201** | Feedback received |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **429** | More than 20 submissions in the last 24 hours. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

