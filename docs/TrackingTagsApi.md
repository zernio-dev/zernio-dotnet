# Zernio.Api.TrackingTagsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddTrackingTagSharedAccount**](TrackingTagsApi.md#addtrackingtagsharedaccount) | **POST** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | Share a tracking tag with an ad account |
| [**CreateTrackingTag**](TrackingTagsApi.md#createtrackingtag) | **POST** /v1/accounts/{accountId}/tracking-tags | Create a tracking tag (Meta Pixel) |
| [**GetTrackingTag**](TrackingTagsApi.md#gettrackingtag) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId} | Fetch a single tracking tag (Meta Pixel) |
| [**GetTrackingTagStats**](TrackingTagsApi.md#gettrackingtagstats) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/stats | Aggregated event stats for a tracking tag (Meta Pixel) |
| [**ListTrackingTagSharedAccounts**](TrackingTagsApi.md#listtrackingtagsharedaccounts) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | List ad accounts a tracking tag is shared with |
| [**ListTrackingTags**](TrackingTagsApi.md#listtrackingtags) | **GET** /v1/accounts/{accountId}/tracking-tags | List tracking tags (Meta Pixels) |
| [**RemoveTrackingTagSharedAccount**](TrackingTagsApi.md#removetrackingtagsharedaccount) | **DELETE** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | Stop sharing a tracking tag with an ad account |
| [**UpdateTrackingTag**](TrackingTagsApi.md#updatetrackingtag) | **PATCH** /v1/accounts/{accountId}/tracking-tags/{tagId} | Update a tracking tag (Meta Pixel) |

<a id="addtrackingtagsharedaccount"></a>
# **AddTrackingTagSharedAccount**
> AddTrackingTagSharedAccount201Response AddTrackingTagSharedAccount (string accountId, string tagId, AddTrackingTagSharedAccountRequest addTrackingTagSharedAccountRequest)

Share a tracking tag with an ad account

Shares the pixel with another ad account so campaigns/audiences in that account can use it. Requires that you administer both the pixel's owning Business Manager and the target ad account; a pixel on a personal (non-BM) ad account can't be shared (Meta will reject the call). Meta only (platform `metaads`); other platforms return 405. 

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
    public class AddTrackingTagSharedAccountExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.
            var addTrackingTagSharedAccountRequest = new AddTrackingTagSharedAccountRequest(); // AddTrackingTagSharedAccountRequest | 

            try
            {
                // Share a tracking tag with an ad account
                AddTrackingTagSharedAccount201Response result = apiInstance.AddTrackingTagSharedAccount(accountId, tagId, addTrackingTagSharedAccountRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.AddTrackingTagSharedAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddTrackingTagSharedAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Share a tracking tag with an ad account
    ApiResponse<AddTrackingTagSharedAccount201Response> response = apiInstance.AddTrackingTagSharedAccountWithHttpInfo(accountId, tagId, addTrackingTagSharedAccountRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.AddTrackingTagSharedAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |
| **addTrackingTagSharedAccountRequest** | [**AddTrackingTagSharedAccountRequest**](AddTrackingTagSharedAccountRequest.md) |  |  |

### Return type

[**AddTrackingTagSharedAccount201Response**](AddTrackingTagSharedAccount201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Tracking tag shared with the ad account |  -  |
| **400** | Invalid body / &#x60;adAccountId&#x60;, or Meta rejected the share (e.g. personal ad account). |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | Account or tracking tag not found. |  -  |
| **405** | Platform does not support shared accounts. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createtrackingtag"></a>
# **CreateTrackingTag**
> CreateTrackingTag201Response CreateTrackingTag (string accountId, CreateTrackingTagRequest createTrackingTagRequest)

Create a tracking tag (Meta Pixel)

Creates a Meta Pixel on the given ad account (`POST /act_{id}/adspixels` — `name` is the only input). Returns the created tag including its install `code`. The pixel is owned by the Business Manager that owns the ad account; a pixel created on a personal (non-BM) ad account ends up with `ownerBusinessId: null` and can't be shared with other ad accounts.  Creating a pixel does NOT install it — install the returned `code` snippet on the site, or send events server-side via `POST /v1/ads/conversions`. The check `installed` is derived from `lastFiredTime`.  NOT idempotent: each call creates a new pixel. Do not retry blindly on timeout. Meta only (platform `metaads`); other platforms return 405. 

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
    public class CreateTrackingTagExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Meta ads SocialAccount id (platform `metaads`).
            var createTrackingTagRequest = new CreateTrackingTagRequest(); // CreateTrackingTagRequest | 

            try
            {
                // Create a tracking tag (Meta Pixel)
                CreateTrackingTag201Response result = apiInstance.CreateTrackingTag(accountId, createTrackingTagRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.CreateTrackingTag: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTrackingTagWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a tracking tag (Meta Pixel)
    ApiResponse<CreateTrackingTag201Response> response = apiInstance.CreateTrackingTagWithHttpInfo(accountId, createTrackingTagRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.CreateTrackingTagWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Meta ads SocialAccount id (platform &#x60;metaads&#x60;). |  |
| **createTrackingTagRequest** | [**CreateTrackingTagRequest**](CreateTrackingTagRequest.md) |  |  |

### Return type

[**CreateTrackingTag201Response**](CreateTrackingTag201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Tracking tag created |  -  |
| **400** | Invalid body, invalid &#x60;adAccountId&#x60;, over the per-business pixel cap, or ad account not in a Business Manager. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | Account not found or not accessible. |  -  |
| **405** | Platform does not support creating tracking tags. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettrackingtag"></a>
# **GetTrackingTag**
> CreateTrackingTag201Response GetTrackingTag (string accountId, string tagId)

Fetch a single tracking tag (Meta Pixel)

Returns the full tag record including the base-code `code` snippet, `lastFiredTime`, `ownerBusinessId`, `isUnavailable`, etc. Meta only (platform `metaads`); other platforms return 405. 

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
    public class GetTrackingTagExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.

            try
            {
                // Fetch a single tracking tag (Meta Pixel)
                CreateTrackingTag201Response result = apiInstance.GetTrackingTag(accountId, tagId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTag: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTrackingTagWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Fetch a single tracking tag (Meta Pixel)
    ApiResponse<CreateTrackingTag201Response> response = apiInstance.GetTrackingTagWithHttpInfo(accountId, tagId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |

### Return type

[**CreateTrackingTag201Response**](CreateTrackingTag201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tracking tag fetched |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | Account or tracking tag not found. |  -  |
| **405** | Platform does not support fetching a tracking tag. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettrackingtagstats"></a>
# **GetTrackingTagStats**
> GetTrackingTagStats200Response GetTrackingTagStats (string accountId, string tagId, string? aggregation = null, int? startTime = null, int? endTime = null)

Aggregated event stats for a tracking tag (Meta Pixel)

Returns aggregated event counts for the pixel (`GET /{pixel_id}/stats`). Rows are passed through from Meta as-is — their shape depends on the `aggregation` requested. Meta only (platform `metaads`); other platforms return 405. 

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
    public class GetTrackingTagStatsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.
            var aggregation = "event";  // string? | Aggregation dimension. Defaults to `event`. (optional)  (default to event)
            var startTime = 56;  // int? | Unix seconds lower bound. (optional) 
            var endTime = 56;  // int? | Unix seconds upper bound. (optional) 

            try
            {
                // Aggregated event stats for a tracking tag (Meta Pixel)
                GetTrackingTagStats200Response result = apiInstance.GetTrackingTagStats(accountId, tagId, aggregation, startTime, endTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagStats: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTrackingTagStatsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Aggregated event stats for a tracking tag (Meta Pixel)
    ApiResponse<GetTrackingTagStats200Response> response = apiInstance.GetTrackingTagStatsWithHttpInfo(accountId, tagId, aggregation, startTime, endTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagStatsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |
| **aggregation** | **string?** | Aggregation dimension. Defaults to &#x60;event&#x60;. | [optional] [default to event] |
| **startTime** | **int?** | Unix seconds lower bound. | [optional]  |
| **endTime** | **int?** | Unix seconds upper bound. | [optional]  |

### Return type

[**GetTrackingTagStats200Response**](GetTrackingTagStats200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Stats fetched |  -  |
| **400** | Invalid query parameter. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | Account or tracking tag not found. |  -  |
| **405** | Platform does not support tracking-tag stats. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtrackingtagsharedaccounts"></a>
# **ListTrackingTagSharedAccounts**
> ListTrackingTagSharedAccounts200Response ListTrackingTagSharedAccounts (string accountId, string tagId)

List ad accounts a tracking tag is shared with

Meta only (platform `metaads`); other platforms return 405.

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
    public class ListTrackingTagSharedAccountsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.

            try
            {
                // List ad accounts a tracking tag is shared with
                ListTrackingTagSharedAccounts200Response result = apiInstance.ListTrackingTagSharedAccounts(accountId, tagId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagSharedAccounts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTrackingTagSharedAccountsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List ad accounts a tracking tag is shared with
    ApiResponse<ListTrackingTagSharedAccounts200Response> response = apiInstance.ListTrackingTagSharedAccountsWithHttpInfo(accountId, tagId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagSharedAccountsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |

### Return type

[**ListTrackingTagSharedAccounts200Response**](ListTrackingTagSharedAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Shared ad accounts listed |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | Account or tracking tag not found. |  -  |
| **405** | Platform does not support shared accounts. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtrackingtags"></a>
# **ListTrackingTags**
> ListTrackingTags200Response ListTrackingTags (string accountId, string? adAccountId = null)

List tracking tags (Meta Pixels)

Returns the tracking tags (Meta Pixels) the connected ads account can see. Pass `?adAccountId=act_...` to scope the list to a single ad account; omit it to list every pixel reachable by the token (the name is then suffixed with the ad account it was discovered on, for disambiguation). The list view omits `code` — call `getTrackingTag` for the install snippet and full detail.  Meta only today (platform `metaads`); other platforms return 405. The `accountId` must be the Meta *ads* SocialAccount created by the Ads add-on connect flow, not a Facebook/Instagram posting account. Get your `act_...` ids from `GET /v1/ads/accounts`. 

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
    public class ListTrackingTagsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Meta ads SocialAccount id (platform `metaads`).
            var adAccountId = "adAccountId_example";  // string? | Optional. Scope to one ad account, e.g. `act_123456789`. (optional) 

            try
            {
                // List tracking tags (Meta Pixels)
                ListTrackingTags200Response result = apiInstance.ListTrackingTags(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTags: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTrackingTagsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List tracking tags (Meta Pixels)
    ApiResponse<ListTrackingTags200Response> response = apiInstance.ListTrackingTagsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Meta ads SocialAccount id (platform &#x60;metaads&#x60;). |  |
| **adAccountId** | **string?** | Optional. Scope to one ad account, e.g. &#x60;act_123456789&#x60;. | [optional]  |

### Return type

[**ListTrackingTags200Response**](ListTrackingTags200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tracking tags listed |  -  |
| **400** | Account platform not supported, or invalid &#x60;adAccountId&#x60;. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | Account not found or not accessible. |  -  |
| **405** | Platform does not support listing tracking tags. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removetrackingtagsharedaccount"></a>
# **RemoveTrackingTagSharedAccount**
> void RemoveTrackingTagSharedAccount (string accountId, string tagId, string? adAccountId = null)

Stop sharing a tracking tag with an ad account

`adAccountId` may be passed as a query parameter (recommended) or as a JSON body field for clients that can send DELETE bodies. Meta only (platform `metaads`); other platforms return 405. 

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
    public class RemoveTrackingTagSharedAccountExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.
            var adAccountId = "adAccountId_example";  // string? | Ad account to unshare, e.g. `act_123456789`. May also be sent in the JSON body. (optional) 

            try
            {
                // Stop sharing a tracking tag with an ad account
                apiInstance.RemoveTrackingTagSharedAccount(accountId, tagId, adAccountId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.RemoveTrackingTagSharedAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveTrackingTagSharedAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Stop sharing a tracking tag with an ad account
    apiInstance.RemoveTrackingTagSharedAccountWithHttpInfo(accountId, tagId, adAccountId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.RemoveTrackingTagSharedAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |
| **adAccountId** | **string?** | Ad account to unshare, e.g. &#x60;act_123456789&#x60;. May also be sent in the JSON body. | [optional]  |

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
| **204** | Ad account unshared (no content). |  -  |
| **400** | &#x60;adAccountId&#x60; missing (neither query nor body), or Meta rejected the unshare. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | Account or tracking tag not found. |  -  |
| **405** | Platform does not support shared accounts. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatetrackingtag"></a>
# **UpdateTrackingTag**
> CreateTrackingTag201Response UpdateTrackingTag (string accountId, string tagId, UpdateTrackingTagRequest updateTrackingTagRequest)

Update a tracking tag (Meta Pixel)

Partial-update a pixel. Whitelisted fields: `name` (rename), `enableAutomaticMatching`, `automaticMatchingFields`, `firstPartyCookieStatus`, `dataUseSetting`. At least one is required. Returns the re-fetched canonical tag. Meta only (platform `metaads`); other platforms return 405.  There is no DELETE — Meta has no API to delete a pixel. To stop using one, unshare it from your ad accounts (`DELETE .../tracking-tags/{tagId}/shared-accounts`) or disable it in Events Manager. 

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
    public class UpdateTrackingTagExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.
            var updateTrackingTagRequest = new UpdateTrackingTagRequest(); // UpdateTrackingTagRequest | 

            try
            {
                // Update a tracking tag (Meta Pixel)
                CreateTrackingTag201Response result = apiInstance.UpdateTrackingTag(accountId, tagId, updateTrackingTagRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.UpdateTrackingTag: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTrackingTagWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a tracking tag (Meta Pixel)
    ApiResponse<CreateTrackingTag201Response> response = apiInstance.UpdateTrackingTagWithHttpInfo(accountId, tagId, updateTrackingTagRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.UpdateTrackingTagWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |
| **updateTrackingTagRequest** | [**UpdateTrackingTagRequest**](UpdateTrackingTagRequest.md) |  |  |

### Return type

[**CreateTrackingTag201Response**](CreateTrackingTag201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tracking tag updated (re-fetched canonical state) |  -  |
| **400** | Invalid body (e.g. no fields supplied) or Meta validation failure. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | Account or tracking tag not found. |  -  |
| **405** | Platform does not support updating tracking tags. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

