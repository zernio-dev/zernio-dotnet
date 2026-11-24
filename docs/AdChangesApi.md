# Zernio.Api.AdChangesApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ConfirmAdChange**](AdChangesApi.md#confirmadchange) | **POST** /v1/ads/changes/{changeId}/confirm | Confirm a staged ad change |
| [**DiscardAdChange**](AdChangesApi.md#discardadchange) | **DELETE** /v1/ads/changes/{changeId} | Discard a staged ad change |
| [**GetAdChange**](AdChangesApi.md#getadchange) | **GET** /v1/ads/changes/{changeId} | Get a staged ad change |

<a id="confirmadchange"></a>
# **ConfirmAdChange**
> Dictionary&lt;string, Object&gt; ConfirmAdChange (string changeId)

Confirm a staged ad change

Applies a staged change and returns what the direct write returns: the response body of the route the change was staged on.  The caller needs the same access to the object as for the direct write, and the checks of that write run here, including the live ads allowance.  ### Changed since staging  Before writing, the object is read from the ad network again and compared with what it held when the change was staged.  If it changed in between, nothing is written, the change ends as `failed` and the answer is `409` `change_target_changed` with the current values in `details.current`. Stage the change again from those values.  ### Retrying  A change is applied at most once. Confirming a change that is already `confirmed` returns its stored result again. A change that failed answers `409` `change_not_staged`: stage a new one.  A refusal before anything is written leaves the change `staged`, so the confirm can be sent again: `403` `ads_allowance_exceeded`, or on a one-field change a `429` from Zernio's own limits. Any other failed write ends the change as `failed`.  ### Creates  A staged create is sent once. The ad network checks at confirm whatever it did not check at staging, and media is fetched here. A create that fails ends as `failed` and is not retried: `error.details` keeps what the create reported about objects it had already made. 

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
    public class ConfirmAdChangeExample
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
            var apiInstance = new AdChangesApi(httpClient, config, httpClientHandler);
            var changeId = "changeId_example";  // string | The id of the staged change.

            try
            {
                // Confirm a staged ad change
                Dictionary<string, Object> result = apiInstance.ConfirmAdChange(changeId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdChangesApi.ConfirmAdChange: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConfirmAdChangeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Confirm a staged ad change
    ApiResponse<Dictionary<string, Object>> response = apiInstance.ConfirmAdChangeWithHttpInfo(changeId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdChangesApi.ConfirmAdChangeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **changeId** | **string** | The id of the staged change. |  |

### Return type

**Dictionary<string, Object>**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The change was applied. The body is the response of the staged write, for example the body of PUT /v1/ads/campaigns/{campaignId}/status. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The refusals of the staged write: &#x60;ads_addon_required&#x60;, &#x60;ads_allowance_exceeded&#x60; or &#x60;ad_account_not_selected&#x60;. None of them writes anything, and the change stays &#x60;staged&#x60;. |  -  |
| **404** | Resource not found |  -  |
| **409** | The change was not applied. The code says why:  - &#x60;change_target_changed&#x60;: the object changed on the ad network after the change was staged. &#x60;details.current&#x60; carries its current values. - &#x60;change_not_staged&#x60;: the change has already failed. - &#x60;change_outcome_unknown&#x60;: another confirm of this change is running, or one started and never recorded how it ended. Read the change, and check the object on the ad network before staging a new one.  |  -  |
| **429** | Code &#x60;rate_limited&#x60;. A refusal by Zernio&#39;s own limit (&#x60;details.reason&#x60; on Meta, &#x60;details.budgetScope&#x60; on Google) on a change of one field wrote nothing and leaves the change &#x60;staged&#x60;. Any other &#x60;429&#x60;, including one from the ad network, ends the change as &#x60;failed&#x60;. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="discardadchange"></a>
# **DiscardAdChange**
> void DiscardAdChange (string changeId)

Discard a staged ad change

Deletes a change that is still staged. Nothing was written to the ad network, so there is nothing to undo.  A change that was already confirmed or has failed cannot be discarded. 

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
    public class DiscardAdChangeExample
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
            var apiInstance = new AdChangesApi(httpClient, config, httpClientHandler);
            var changeId = "changeId_example";  // string | The id of the staged change.

            try
            {
                // Discard a staged ad change
                apiInstance.DiscardAdChange(changeId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdChangesApi.DiscardAdChange: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DiscardAdChangeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Discard a staged ad change
    apiInstance.DiscardAdChangeWithHttpInfo(changeId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdChangesApi.DiscardAdChangeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **changeId** | **string** | The id of the staged change. |  |

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
| **204** | Change discarded |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (code &#x60;ads_addon_required&#x60;). Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | Resource not found |  -  |
| **409** | The change is no longer staged: &#x60;change_not_staged&#x60; when it was confirmed or has failed, &#x60;change_outcome_unknown&#x60; while a confirm is running. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadchange"></a>
# **GetAdChange**
> GetAdChange200Response GetAdChange (string changeId)

Get a staged ad change

Returns one ad change with its before/after diff. A change is created by sending a supported ad write with `stage: true`.  A staged change does not expire. A confirmed or failed change stays readable for 7 days. 

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
    public class GetAdChangeExample
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
            var apiInstance = new AdChangesApi(httpClient, config, httpClientHandler);
            var changeId = "changeId_example";  // string | The id of the staged change.

            try
            {
                // Get a staged ad change
                GetAdChange200Response result = apiInstance.GetAdChange(changeId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdChangesApi.GetAdChange: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdChangeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a staged ad change
    ApiResponse<GetAdChange200Response> response = apiInstance.GetAdChangeWithHttpInfo(changeId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdChangesApi.GetAdChangeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **changeId** | **string** | The id of the staged change. |  |

### Return type

[**GetAdChange200Response**](GetAdChange200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The change |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (code &#x60;ads_addon_required&#x60;). Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

