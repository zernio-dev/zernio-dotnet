# Zernio.Api.ReachAndFrequencyApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CancelRfReservation**](ReachAndFrequencyApi.md#cancelrfreservation) | **DELETE** /v1/ads/rf-predictions/{predictionId} | Cancel a Reach &amp; Frequency reservation |
| [**CreateRfPrediction**](ReachAndFrequencyApi.md#createrfprediction) | **POST** /v1/ads/rf-predictions | Create a Reach &amp; Frequency prediction |
| [**GetRfPrediction**](ReachAndFrequencyApi.md#getrfprediction) | **GET** /v1/ads/rf-predictions/{predictionId} | Read a Reach &amp; Frequency prediction |
| [**ReserveRfPrediction**](ReachAndFrequencyApi.md#reserverfprediction) | **POST** /v1/ads/rf-predictions/{predictionId}/reserve | Reserve a Reach &amp; Frequency prediction |

<a id="cancelrfreservation"></a>
# **CancelRfReservation**
> void CancelRfReservation (string predictionId, string accountId, string adAccountId)

Cancel a Reach & Frequency reservation

Releases a RESERVATION's locked price and inventory. Unreserved predictions expire on their own.

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
    public class CancelRfReservationExample
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
            var apiInstance = new ReachAndFrequencyApi(httpClient, config, httpClientHandler);
            var predictionId = "predictionId_example";  // string | 
            var accountId = "accountId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | 

            try
            {
                // Cancel a Reach & Frequency reservation
                apiInstance.CancelRfReservation(predictionId, accountId, adAccountId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReachAndFrequencyApi.CancelRfReservation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CancelRfReservationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cancel a Reach & Frequency reservation
    apiInstance.CancelRfReservationWithHttpInfo(predictionId, accountId, adAccountId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReachAndFrequencyApi.CancelRfReservationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **predictionId** | **string** |  |  |
| **accountId** | **string** |  |  |
| **adAccountId** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reservation cancelled |  -  |
| **400** | Invalid input, or Meta rejected the cancel |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createrfprediction"></a>
# **CreateRfPrediction**
> CreateRfPrediction201Response CreateRfPrediction (CreateRfPredictionRequest createRfPredictionRequest)

Create a Reach & Frequency prediction

Creates an R&F prediction — a QUOTE, nothing is bought and no ad entities are created. Provide a date range plus exactly one of `budgetAmount` (Meta predicts reach) or `reach` (Meta predicts the budget). The response carries the estimate and its allowed bounds (min/max budget and reach). Predictions expire on their own; to buy, reserve one via POST /v1/ads/rf-predictions/{predictionId}/reserve and pass the RESERVED id to POST /v1/ads/create with `buyingType: \"RESERVED\"`.  Reservation campaigns reject automatic placements, so omitted `placements` default to Facebook feed (+ Instagram stream when a linked IG professional account resolves); Instagram placements require that IG account.

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
    public class CreateRfPredictionExample
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
            var apiInstance = new ReachAndFrequencyApi(httpClient, config, httpClientHandler);
            var createRfPredictionRequest = new CreateRfPredictionRequest(); // CreateRfPredictionRequest | 

            try
            {
                // Create a Reach & Frequency prediction
                CreateRfPrediction201Response result = apiInstance.CreateRfPrediction(createRfPredictionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReachAndFrequencyApi.CreateRfPrediction: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateRfPredictionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a Reach & Frequency prediction
    ApiResponse<CreateRfPrediction201Response> response = apiInstance.CreateRfPredictionWithHttpInfo(createRfPredictionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReachAndFrequencyApi.CreateRfPredictionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createRfPredictionRequest** | [**CreateRfPredictionRequest**](CreateRfPredictionRequest.md) |  |  |

### Return type

[**CreateRfPrediction201Response**](CreateRfPrediction201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Prediction created (usually ready within seconds) |  -  |
| **400** | Invalid input, or Meta rejected the prediction — message carries Meta&#39;s error |  -  |
| **401** | Unauthorized |  -  |
| **422** | No Facebook Page resolved for the account |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getrfprediction"></a>
# **GetRfPrediction**
> CreateRfPrediction201Response GetRfPrediction (string predictionId, string accountId, string adAccountId)

Read a Reach & Frequency prediction

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
    public class GetRfPredictionExample
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
            var apiInstance = new ReachAndFrequencyApi(httpClient, config, httpClientHandler);
            var predictionId = "predictionId_example";  // string | 
            var accountId = "accountId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | 

            try
            {
                // Read a Reach & Frequency prediction
                CreateRfPrediction201Response result = apiInstance.GetRfPrediction(predictionId, accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReachAndFrequencyApi.GetRfPrediction: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetRfPredictionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read a Reach & Frequency prediction
    ApiResponse<CreateRfPrediction201Response> response = apiInstance.GetRfPredictionWithHttpInfo(predictionId, accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReachAndFrequencyApi.GetRfPredictionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **predictionId** | **string** |  |  |
| **accountId** | **string** |  |  |
| **adAccountId** | **string** |  |  |

### Return type

[**CreateRfPrediction201Response**](CreateRfPrediction201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Prediction status and estimates |  -  |
| **400** | Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="reserverfprediction"></a>
# **ReserveRfPrediction**
> ReserveRfPrediction201Response ReserveRfPrediction (string predictionId, ReserveRfPredictionRequest reserveRfPredictionRequest)

Reserve a Reach & Frequency prediction

Locks the quoted price + inventory until the returned `expiresAt` and mints a NEW prediction id — pass that RESERVED id (not the original) as `rfPredictionId` on POST /v1/ads/create. Release an unused reservation via DELETE.

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
    public class ReserveRfPredictionExample
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
            var apiInstance = new ReachAndFrequencyApi(httpClient, config, httpClientHandler);
            var predictionId = "predictionId_example";  // string | 
            var reserveRfPredictionRequest = new ReserveRfPredictionRequest(); // ReserveRfPredictionRequest | 

            try
            {
                // Reserve a Reach & Frequency prediction
                ReserveRfPrediction201Response result = apiInstance.ReserveRfPrediction(predictionId, reserveRfPredictionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReachAndFrequencyApi.ReserveRfPrediction: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReserveRfPredictionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reserve a Reach & Frequency prediction
    ApiResponse<ReserveRfPrediction201Response> response = apiInstance.ReserveRfPredictionWithHttpInfo(predictionId, reserveRfPredictionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReachAndFrequencyApi.ReserveRfPredictionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **predictionId** | **string** |  |  |
| **reserveRfPredictionRequest** | [**ReserveRfPredictionRequest**](ReserveRfPredictionRequest.md) |  |  |

### Return type

[**ReserveRfPrediction201Response**](ReserveRfPrediction201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Reserved; &#x60;prediction.predictionId&#x60; is the new RESERVED id |  -  |
| **400** | Invalid input, or Meta rejected the reserve |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

