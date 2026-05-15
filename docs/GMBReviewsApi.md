# Zernio.Api.GMBReviewsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BatchGetGoogleBusinessReviews**](GMBReviewsApi.md#batchgetgooglebusinessreviews) | **POST** /v1/accounts/{accountId}/gmb-reviews/batch | Batch get reviews |
| [**DeleteGoogleBusinessReviewReply**](GMBReviewsApi.md#deletegooglebusinessreviewreply) | **DELETE** /v1/accounts/{accountId}/gmb-reviews/{reviewId}/reply | Delete a review reply |
| [**GetGoogleBusinessReviews**](GMBReviewsApi.md#getgooglebusinessreviews) | **GET** /v1/accounts/{accountId}/gmb-reviews | Get reviews |
| [**ReplyToGoogleBusinessReview**](GMBReviewsApi.md#replytogooglebusinessreview) | **POST** /v1/accounts/{accountId}/gmb-reviews/{reviewId}/reply | Reply to a review |

<a id="batchgetgooglebusinessreviews"></a>
# **BatchGetGoogleBusinessReviews**
> BatchGetGoogleBusinessReviews200Response BatchGetGoogleBusinessReviews (string accountId, BatchGetGoogleBusinessReviewsRequest batchGetGoogleBusinessReviewsRequest)

Batch get reviews

Fetches reviews across multiple locations in a single request. More efficient than calling GET /gmb-reviews per location for multi-location businesses. Reviews are grouped by location in the response. 

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
    public class BatchGetGoogleBusinessReviewsExample
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
            var apiInstance = new GMBReviewsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var batchGetGoogleBusinessReviewsRequest = new BatchGetGoogleBusinessReviewsRequest(); // BatchGetGoogleBusinessReviewsRequest | 

            try
            {
                // Batch get reviews
                BatchGetGoogleBusinessReviews200Response result = apiInstance.BatchGetGoogleBusinessReviews(accountId, batchGetGoogleBusinessReviewsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GMBReviewsApi.BatchGetGoogleBusinessReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BatchGetGoogleBusinessReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Batch get reviews
    ApiResponse<BatchGetGoogleBusinessReviews200Response> response = apiInstance.BatchGetGoogleBusinessReviewsWithHttpInfo(accountId, batchGetGoogleBusinessReviewsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GMBReviewsApi.BatchGetGoogleBusinessReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **batchGetGoogleBusinessReviewsRequest** | [**BatchGetGoogleBusinessReviewsRequest**](BatchGetGoogleBusinessReviewsRequest.md) |  |  |

### Return type

[**BatchGetGoogleBusinessReviews200Response**](BatchGetGoogleBusinessReviews200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Batch reviews fetched successfully |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletegooglebusinessreviewreply"></a>
# **DeleteGoogleBusinessReviewReply**
> DeleteGoogleBusinessReviewReply200Response DeleteGoogleBusinessReviewReply (string accountId, string reviewId)

Delete a review reply

Removes the business owner reply from a Google Business review. The review itself remains.

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
    public class DeleteGoogleBusinessReviewReplyExample
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
            var apiInstance = new GMBReviewsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The Zernio account ID (from /v1/accounts)
            var reviewId = "reviewId_example";  // string | The review ID portion (e.g. \"AIe9_BGx1234567890\"), not the full resource name

            try
            {
                // Delete a review reply
                DeleteGoogleBusinessReviewReply200Response result = apiInstance.DeleteGoogleBusinessReviewReply(accountId, reviewId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GMBReviewsApi.DeleteGoogleBusinessReviewReply: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteGoogleBusinessReviewReplyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a review reply
    ApiResponse<DeleteGoogleBusinessReviewReply200Response> response = apiInstance.DeleteGoogleBusinessReviewReplyWithHttpInfo(accountId, reviewId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GMBReviewsApi.DeleteGoogleBusinessReviewReplyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The Zernio account ID (from /v1/accounts) |  |
| **reviewId** | **string** | The review ID portion (e.g. \&quot;AIe9_BGx1234567890\&quot;), not the full resource name |  |

### Return type

[**DeleteGoogleBusinessReviewReply200Response**](DeleteGoogleBusinessReviewReply200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reply deleted successfully |  -  |
| **400** | Invalid request, non-GBP account, or account missing location metadata |  -  |
| **401** | Unauthorized or token invalid (account must be reconnected) |  -  |
| **404** | Resource not found |  -  |
| **500** | Failed to delete reply |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getgooglebusinessreviews"></a>
# **GetGoogleBusinessReviews**
> GetGoogleBusinessReviews200Response GetGoogleBusinessReviews (string accountId, string? locationId = null, int? pageSize = null, string? pageToken = null)

Get reviews

Returns reviews for a GBP account including ratings, comments, and owner replies. Use nextPageToken for pagination.

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
    public class GetGoogleBusinessReviewsExample
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
            var apiInstance = new GMBReviewsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The Zernio account ID (from /v1/accounts)
            var locationId = "locationId_example";  // string? | Override which location to query. If omitted, uses the account's selected location. Use GET /gmb-locations to list valid IDs. (optional) 
            var pageSize = 50;  // int? | Number of reviews to fetch per page (max 50) (optional)  (default to 50)
            var pageToken = "pageToken_example";  // string? | Pagination token from previous response (optional) 

            try
            {
                // Get reviews
                GetGoogleBusinessReviews200Response result = apiInstance.GetGoogleBusinessReviews(accountId, locationId, pageSize, pageToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GMBReviewsApi.GetGoogleBusinessReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetGoogleBusinessReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get reviews
    ApiResponse<GetGoogleBusinessReviews200Response> response = apiInstance.GetGoogleBusinessReviewsWithHttpInfo(accountId, locationId, pageSize, pageToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GMBReviewsApi.GetGoogleBusinessReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The Zernio account ID (from /v1/accounts) |  |
| **locationId** | **string?** | Override which location to query. If omitted, uses the account&#39;s selected location. Use GET /gmb-locations to list valid IDs. | [optional]  |
| **pageSize** | **int?** | Number of reviews to fetch per page (max 50) | [optional] [default to 50] |
| **pageToken** | **string?** | Pagination token from previous response | [optional]  |

### Return type

[**GetGoogleBusinessReviews200Response**](GetGoogleBusinessReviews200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reviews fetched successfully |  -  |
| **400** | Invalid request - not a Google Business account or missing location |  -  |
| **401** | Unauthorized or token invalid |  -  |
| **403** | Permission denied for this location |  -  |
| **404** | Resource not found |  -  |
| **500** | Failed to fetch reviews |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="replytogooglebusinessreview"></a>
# **ReplyToGoogleBusinessReview**
> ReplyToGoogleBusinessReview200Response ReplyToGoogleBusinessReview (string accountId, string reviewId, ReplyToGoogleBusinessReviewRequest replyToGoogleBusinessReviewRequest)

Reply to a review

Posts (or updates) the business owner reply to a Google Business review. The reply is associated with the account's currently selected location (set via /v1/accounts/{accountId}/gmb-locations). Calling this endpoint a second time on the same review overwrites the previous reply (PUT semantics on Google's side). 

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
    public class ReplyToGoogleBusinessReviewExample
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
            var apiInstance = new GMBReviewsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The Zernio account ID (from /v1/accounts)
            var reviewId = "reviewId_example";  // string | The review ID portion (e.g. \"AIe9_BGx1234567890\"), not the full resource name
            var replyToGoogleBusinessReviewRequest = new ReplyToGoogleBusinessReviewRequest(); // ReplyToGoogleBusinessReviewRequest | 

            try
            {
                // Reply to a review
                ReplyToGoogleBusinessReview200Response result = apiInstance.ReplyToGoogleBusinessReview(accountId, reviewId, replyToGoogleBusinessReviewRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GMBReviewsApi.ReplyToGoogleBusinessReview: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReplyToGoogleBusinessReviewWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reply to a review
    ApiResponse<ReplyToGoogleBusinessReview200Response> response = apiInstance.ReplyToGoogleBusinessReviewWithHttpInfo(accountId, reviewId, replyToGoogleBusinessReviewRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GMBReviewsApi.ReplyToGoogleBusinessReviewWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The Zernio account ID (from /v1/accounts) |  |
| **reviewId** | **string** | The review ID portion (e.g. \&quot;AIe9_BGx1234567890\&quot;), not the full resource name |  |
| **replyToGoogleBusinessReviewRequest** | [**ReplyToGoogleBusinessReviewRequest**](ReplyToGoogleBusinessReviewRequest.md) |  |  |

### Return type

[**ReplyToGoogleBusinessReview200Response**](ReplyToGoogleBusinessReview200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reply posted successfully |  -  |
| **400** | Invalid request, missing comment, non-GBP account, or account missing location metadata |  -  |
| **401** | Unauthorized or token invalid (account must be reconnected) |  -  |
| **404** | Resource not found |  -  |
| **500** | Failed to post reply |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

