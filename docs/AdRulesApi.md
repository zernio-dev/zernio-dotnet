# Zernio.Api.AdRulesApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateAdRule**](AdRulesApi.md#createadrule) | **POST** /v1/ads/rules | Create an ad rule |
| [**DeleteAdRule**](AdRulesApi.md#deleteadrule) | **DELETE** /v1/ads/rules/{ruleId} | Delete an ad rule |
| [**GetAdRule**](AdRulesApi.md#getadrule) | **GET** /v1/ads/rules/{ruleId} | Get an ad rule |
| [**ListAdRuleActivity**](AdRulesApi.md#listadruleactivity) | **GET** /v1/ads/rules/activity | List every change ad rules made |
| [**ListAdRuleRuns**](AdRulesApi.md#listadruleruns) | **GET** /v1/ads/rules/{ruleId}/runs | List an ad rule&#39;s runs |
| [**ListAdRules**](AdRulesApi.md#listadrules) | **GET** /v1/ads/rules | List ad rules |
| [**PreviewAdRule**](AdRulesApi.md#previewadrule) | **POST** /v1/ads/rules/{ruleId}/preview | Preview an ad rule |
| [**UpdateAdRule**](AdRulesApi.md#updateadrule) | **PATCH** /v1/ads/rules/{ruleId} | Update an ad rule |

<a id="createadrule"></a>
# **CreateAdRule**
> CreateAdRule201Response CreateAdRule (CreateAdRuleRequest createAdRuleRequest)

Create an ad rule

Creates a rule that checks the campaigns or ad sets of one ad account on a schedule and acts on each one that meets every condition.  Rules support Meta, Google, TikTok, LinkedIn, Pinterest, X and Reddit ads connections. Each campaign or ad set is evaluated on its own, over the ad account's calendar days, from the metrics Zernio syncs. A rule can notify (the `ad_rule.triggered` webhook), and take at most one of `pause`, `activate` and `adjust_budget`. After acting on an object, the rule leaves that object alone for `cooldownMinutes`; a rule that pauses, activates or adjusts budgets needs a cooldown at least as long as its schedule.  `activate` only reactivates objects a rule paused, never ones you paused yourself, and only once the cooldown has passed since that pause. If you reactivate and pause such an object yourself between two runs of a rule, Zernio cannot tell your pause from the rule's, and an `activate` rule may reactivate it.  Use `POST /v1/ads/rules/{ruleId}/preview` to see what a rule would match before enabling it. 

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
    public class CreateAdRuleExample
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
            var apiInstance = new AdRulesApi(httpClient, config, httpClientHandler);
            var createAdRuleRequest = new CreateAdRuleRequest(); // CreateAdRuleRequest | 

            try
            {
                // Create an ad rule
                CreateAdRule201Response result = apiInstance.CreateAdRule(createAdRuleRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdRulesApi.CreateAdRule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdRuleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create an ad rule
    ApiResponse<CreateAdRule201Response> response = apiInstance.CreateAdRuleWithHttpInfo(createAdRuleRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdRulesApi.CreateAdRuleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createAdRuleRequest** | [**CreateAdRuleRequest**](CreateAdRuleRequest.md) |  |  |

### Return type

[**CreateAdRule201Response**](CreateAdRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Rule created |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;ads_addon_required&#x60; when the team has no ads access (legacy plans need the Ads add-on), &#x60;ad_account_not_selected&#x60; when &#x60;adAccountId&#x60; is not in the connection&#39;s selected ad accounts, or &#x60;ads_allowance_exceeded&#x60; when a rule that reactivates or raises budgets is created for a team past its free live-ads allowance with no payment method. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteadrule"></a>
# **DeleteAdRule**
> UpdateYoutubeDefaultPlaylist200Response DeleteAdRule (string ruleId)

Delete an ad rule

Deletes a rule and its run history. Changes the rule already made on the platform stay. 

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
    public class DeleteAdRuleExample
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
            var apiInstance = new AdRulesApi(httpClient, config, httpClientHandler);
            var ruleId = "ruleId_example";  // string | 

            try
            {
                // Delete an ad rule
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.DeleteAdRule(ruleId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdRulesApi.DeleteAdRule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAdRuleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete an ad rule
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.DeleteAdRuleWithHttpInfo(ruleId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdRulesApi.DeleteAdRuleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ruleId** | **string** |  |  |

### Return type

[**UpdateYoutubeDefaultPlaylist200Response**](UpdateYoutubeDefaultPlaylist200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rule deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (code &#x60;ads_addon_required&#x60;). Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadrule"></a>
# **GetAdRule**
> CreateAdRule201Response GetAdRule (string ruleId)

Get an ad rule

Returns one ad rule. 

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
    public class GetAdRuleExample
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
            var apiInstance = new AdRulesApi(httpClient, config, httpClientHandler);
            var ruleId = "ruleId_example";  // string | 

            try
            {
                // Get an ad rule
                CreateAdRule201Response result = apiInstance.GetAdRule(ruleId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdRulesApi.GetAdRule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdRuleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an ad rule
    ApiResponse<CreateAdRule201Response> response = apiInstance.GetAdRuleWithHttpInfo(ruleId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdRulesApi.GetAdRuleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ruleId** | **string** |  |  |

### Return type

[**CreateAdRule201Response**](CreateAdRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rule |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (code &#x60;ads_addon_required&#x60;). Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadruleactivity"></a>
# **ListAdRuleActivity**
> ListAdRuleActivity200Response ListAdRuleActivity (string? ruleId = null, string? accountId = null, string? type = null, DateTime? from = null, DateTime? to = null, int? limit = null, string? cursor = null)

List every change ad rules made

The permanent record of what your rules did: one entry per pause, reactivation or budget change (including skipped and failed attempts), newest first, across all rules of the profiles the key can reach. Entries stay after a rule is renamed or deleted; `ruleName` is the rule's name when it acted. 

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
    public class ListAdRuleActivityExample
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
            var apiInstance = new AdRulesApi(httpClient, config, httpClientHandler);
            var ruleId = "ruleId_example";  // string? |  (optional) 
            var accountId = "accountId_example";  // string? | Only changes of rules on this ads connection. (optional) 
            var type = "pause";  // string? |  (optional) 
            var from = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | ISO 8601 date-time, inclusive. (optional) 
            var to = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | ISO 8601 date-time, inclusive. (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? | `nextCursor` from the previous page. (optional) 

            try
            {
                // List every change ad rules made
                ListAdRuleActivity200Response result = apiInstance.ListAdRuleActivity(ruleId, accountId, type, from, to, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdRulesApi.ListAdRuleActivity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdRuleActivityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List every change ad rules made
    ApiResponse<ListAdRuleActivity200Response> response = apiInstance.ListAdRuleActivityWithHttpInfo(ruleId, accountId, type, from, to, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdRulesApi.ListAdRuleActivityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ruleId** | **string?** |  | [optional]  |
| **accountId** | **string?** | Only changes of rules on this ads connection. | [optional]  |
| **type** | **string?** |  | [optional]  |
| **from** | **DateTime?** | ISO 8601 date-time, inclusive. | [optional]  |
| **to** | **DateTime?** | ISO 8601 date-time, inclusive. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** | &#x60;nextCursor&#x60; from the previous page. | [optional]  |

### Return type

[**ListAdRuleActivity200Response**](ListAdRuleActivity200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Changes, newest first |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (code &#x60;ads_addon_required&#x60;). Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadruleruns"></a>
# **ListAdRuleRuns**
> ListAdRuleRuns200Response ListAdRuleRuns (string ruleId, int? limit = null, int? skip = null)

List an ad rule's runs

Lists a rule's scheduled runs, newest first: what each run evaluated, matched and did. Runs that changed something (or tried to) are kept permanently, also after the rule is deleted; runs that changed nothing are dropped after about 31 days. For every change across all rules, use `GET /v1/ads/rules/activity`. 

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
    public class ListAdRuleRunsExample
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
            var apiInstance = new AdRulesApi(httpClient, config, httpClientHandler);
            var ruleId = "ruleId_example";  // string | 
            var limit = 20;  // int? |  (optional)  (default to 20)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List an ad rule's runs
                ListAdRuleRuns200Response result = apiInstance.ListAdRuleRuns(ruleId, limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdRulesApi.ListAdRuleRuns: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdRuleRunsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List an ad rule's runs
    ApiResponse<ListAdRuleRuns200Response> response = apiInstance.ListAdRuleRunsWithHttpInfo(ruleId, limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdRulesApi.ListAdRuleRunsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ruleId** | **string** |  |  |
| **limit** | **int?** |  | [optional] [default to 20] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**ListAdRuleRuns200Response**](ListAdRuleRuns200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Runs |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (code &#x60;ads_addon_required&#x60;). Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadrules"></a>
# **ListAdRules**
> ListAdRules200Response ListAdRules (string? accountId = null, string? adAccountId = null, int? limit = null, int? skip = null)

List ad rules

Lists the ad rules on the profiles your key can reach, newest first. 

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
    public class ListAdRulesExample
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
            var apiInstance = new AdRulesApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string? | Only rules on this ads connection. (optional) 
            var adAccountId = "adAccountId_example";  // string? | Only rules watching this platform ad account. (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List ad rules
                ListAdRules200Response result = apiInstance.ListAdRules(accountId, adAccountId, limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdRulesApi.ListAdRules: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdRulesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List ad rules
    ApiResponse<ListAdRules200Response> response = apiInstance.ListAdRulesWithHttpInfo(accountId, adAccountId, limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdRulesApi.ListAdRulesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string?** | Only rules on this ads connection. | [optional]  |
| **adAccountId** | **string?** | Only rules watching this platform ad account. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**ListAdRules200Response**](ListAdRules200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rules |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (code &#x60;ads_addon_required&#x60;). Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="previewadrule"></a>
# **PreviewAdRule**
> AdRuleEvaluation PreviewAdRule (string ruleId)

Preview an ad rule

Evaluates a rule against current metrics and returns what it would match right now, without acting on anything, sending a webhook or starting a cooldown. Works on disabled rules. 

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
    public class PreviewAdRuleExample
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
            var apiInstance = new AdRulesApi(httpClient, config, httpClientHandler);
            var ruleId = "ruleId_example";  // string | 

            try
            {
                // Preview an ad rule
                AdRuleEvaluation result = apiInstance.PreviewAdRule(ruleId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdRulesApi.PreviewAdRule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PreviewAdRuleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Preview an ad rule
    ApiResponse<AdRuleEvaluation> response = apiInstance.PreviewAdRuleWithHttpInfo(ruleId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdRulesApi.PreviewAdRuleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ruleId** | **string** |  |  |

### Return type

[**AdRuleEvaluation**](AdRuleEvaluation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Evaluation |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (code &#x60;ads_addon_required&#x60;). Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadrule"></a>
# **UpdateAdRule**
> CreateAdRule201Response UpdateAdRule (string ruleId, UpdateAdRuleRequest updateAdRuleRequest)

Update an ad rule

Changes any field of a rule except its connection and ad account. Send `campaignIds: null` to check the whole ad account again. Changing the schedule, or enabling a disabled rule, moves the next run; re-sending `enabled: true` on an enabled rule does not. 

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
    public class UpdateAdRuleExample
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
            var apiInstance = new AdRulesApi(httpClient, config, httpClientHandler);
            var ruleId = "ruleId_example";  // string | 
            var updateAdRuleRequest = new UpdateAdRuleRequest(); // UpdateAdRuleRequest | 

            try
            {
                // Update an ad rule
                CreateAdRule201Response result = apiInstance.UpdateAdRule(ruleId, updateAdRuleRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdRulesApi.UpdateAdRule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdRuleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update an ad rule
    ApiResponse<CreateAdRule201Response> response = apiInstance.UpdateAdRuleWithHttpInfo(ruleId, updateAdRuleRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdRulesApi.UpdateAdRuleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ruleId** | **string** |  |  |
| **updateAdRuleRequest** | [**UpdateAdRuleRequest**](UpdateAdRuleRequest.md) |  |  |

### Return type

[**CreateAdRule201Response**](CreateAdRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rule updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;ads_addon_required&#x60; when the team has no ads access, or &#x60;ads_allowance_exceeded&#x60; when the change enables a rule that reactivates or raises budgets for a team past its free live-ads allowance with no payment method. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

