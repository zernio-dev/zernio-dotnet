# Zernio.Api.SMSApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**SendSms**](SMSApi.md#sendsms) | **POST** /v1/sms/messages | Send an SMS or MMS |

<a id="sendsms"></a>
# **SendSms**
> SendSms200Response SendSms (SendSmsRequest sendSmsRequest)

Send an SMS or MMS

Send a text (SMS) or media (MMS) message from one of your SMS-enabled numbers.  Provide `text`, `mediaUrls`, or both. Supply an `Idempotency-Key` header to make retries safe (a repeated key replays the original result instead of sending again). US numbers must have an approved carrier registration before they can deliver. 

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
    public class SendSmsExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var sendSmsRequest = new SendSmsRequest(); // SendSmsRequest | 

            try
            {
                // Send an SMS or MMS
                SendSms200Response result = apiInstance.SendSms(sendSmsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.SendSms: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendSmsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send an SMS or MMS
    ApiResponse<SendSms200Response> response = apiInstance.SendSmsWithHttpInfo(sendSmsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.SendSmsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sendSmsRequest** | [**SendSmsRequest**](SendSmsRequest.md) |  |  |

### Return type

[**SendSms200Response**](SendSms200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Message accepted for delivery. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

