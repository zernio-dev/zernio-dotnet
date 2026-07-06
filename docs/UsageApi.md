# Zernio.Api.UsageApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetCallsUsage**](UsageApi.md#getcallsusage) | **GET** /v1/usage/calls | Calling usage (volumes + billable cost) |
| [**GetSmsUsage**](UsageApi.md#getsmsusage) | **GET** /v1/usage/sms | SMS usage (volumes) |
| [**GetUsage**](UsageApi.md#getusage) | **GET** /v1/usage | Get plan and usage snapshot |
| [**GetUsageStats**](UsageApi.md#getusagestats) | **GET** /v1/usage-stats | Get plan and usage stats |
| [**GetXApiPricing**](UsageApi.md#getxapipricing) | **GET** /v1/billing/x-pricing | Get X/Twitter API pricing table |

<a id="getcallsusage"></a>
# **GetCallsUsage**
> GetCallsUsage200Response GetCallsUsage (DateTime? since = null, DateTime? until = null, string? channel = null, string? number = null, string? groupBy = null)

Calling usage (volumes + billable cost)

Aggregated calling usage across your numbers, both channels (WhatsApp Business Calling + regular phone/PSTN): call counts, answered counts, minutes, and cost. Use it for cost visibility or to rebill your own customers per number.  Costs come from each call's billing snapshot, so this endpoint always agrees with the invoice: `billableUSD` is what Zernio bills; `metaUSD` is the WhatsApp per-minute charge Meta bills directly to your WABA (display only, never billed by Zernio).  Optional `groupBy` returns a breakdown by UTC day, by your number, or by channel. Defaults to the last 30 days. 

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
    public class GetCallsUsageExample
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
            var apiInstance = new UsageApi(httpClient, config, httpClientHandler);
            var since = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | Start of the window (inclusive). Default 30 days before `until`. (optional) 
            var until = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | End of the window (exclusive). Default now. (optional) 
            var channel = "whatsapp";  // string? |  (optional) 
            var number = "number_example";  // string? | Scope to calls involving this number (typically one of YOUR numbers). E.164, leading + optional. (optional) 
            var groupBy = "day";  // string? |  (optional) 

            try
            {
                // Calling usage (volumes + billable cost)
                GetCallsUsage200Response result = apiInstance.GetCallsUsage(since, until, channel, number, groupBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsageApi.GetCallsUsage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCallsUsageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Calling usage (volumes + billable cost)
    ApiResponse<GetCallsUsage200Response> response = apiInstance.GetCallsUsageWithHttpInfo(since, until, channel, number, groupBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsageApi.GetCallsUsageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **since** | **DateTime?** | Start of the window (inclusive). Default 30 days before &#x60;until&#x60;. | [optional]  |
| **until** | **DateTime?** | End of the window (exclusive). Default now. | [optional]  |
| **channel** | **string?** |  | [optional]  |
| **number** | **string?** | Scope to calls involving this number (typically one of YOUR numbers). E.164, leading + optional. | [optional]  |
| **groupBy** | **string?** |  | [optional]  |

### Return type

[**GetCallsUsage200Response**](GetCallsUsage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Usage totals (+ breakdown when groupBy is set). |  -  |
| **400** | since must be before until |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getsmsusage"></a>
# **GetSmsUsage**
> GetSmsUsage200Response GetSmsUsage (DateTime? since = null, DateTime? until = null, string? number = null, string? groupBy = null)

SMS usage (volumes)

Aggregated SMS/MMS volumes across your numbers: sent, received, and total message counts, with an optional breakdown by UTC day or by number. Defaults to the last 30 days.  Volumes only, deliberately: SMS cost is carrier-rated asynchronously and billed to your invoice, so per-message cost is not available here. Calling usage (GET /v1/usage/calls) does include billable cost. 

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
    public class GetSmsUsageExample
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
            var apiInstance = new UsageApi(httpClient, config, httpClientHandler);
            var since = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | Start of the window (inclusive). Default 30 days before `until`. (optional) 
            var until = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | End of the window (exclusive). Default now. (optional) 
            var number = "number_example";  // string? | Scope to one of YOUR SMS-enabled numbers (E.164, leading + optional). (optional) 
            var groupBy = "day";  // string? |  (optional) 

            try
            {
                // SMS usage (volumes)
                GetSmsUsage200Response result = apiInstance.GetSmsUsage(since, until, number, groupBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsageApi.GetSmsUsage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSmsUsageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // SMS usage (volumes)
    ApiResponse<GetSmsUsage200Response> response = apiInstance.GetSmsUsageWithHttpInfo(since, until, number, groupBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsageApi.GetSmsUsageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **since** | **DateTime?** | Start of the window (inclusive). Default 30 days before &#x60;until&#x60;. | [optional]  |
| **until** | **DateTime?** | End of the window (exclusive). Default now. | [optional]  |
| **number** | **string?** | Scope to one of YOUR SMS-enabled numbers (E.164, leading + optional). | [optional]  |
| **groupBy** | **string?** |  | [optional]  |

### Return type

[**GetSmsUsage200Response**](GetSmsUsage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Volume totals (+ breakdown when groupBy is set). |  -  |
| **400** | since must be before until |  -  |
| **401** | Unauthorized |  -  |
| **404** | &#x60;number&#x60; doesn&#39;t match any of your SMS-enabled numbers |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getusage"></a>
# **GetUsage**
> UsageStats GetUsage (bool? reconcile = null)

Get plan and usage snapshot

The usage hub: current plan name, billing period, plan limits, and usage counts, in one snapshot. For metered consumption over an arbitrary window with breakdowns (by day, by number), use the domain spokes: `GET /v1/usage/calls` and `GET /v1/usage/sms`.  The response shape depends on the account's `billingSystem`:   * Stripe users: per-period `usage.uploads` / `usage.profiles` counters.   * Metronome (usage-based) users: `usage.connectedAccounts`,     `usage.xApiCallsByOperation` (per-operation X API call counts —     resolve keys via `GET /v1/billing/x-pricing`), plus a `spend`     block with `currentPeriodCents`, `xSpendCents`, and     `xSpendLimitCents`. The legacy `usage.xApiCalls` 3-tier     aggregate is still emitted for back-compat but excludes the     $0.200 URL tier and any future tiers — new clients should     consume `xApiCallsByOperation` only. 

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
    public class GetUsageExample
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
            var apiInstance = new UsageApi(httpClient, config, httpClientHandler);
            var reconcile = true;  // bool? | For Stripe subscription users, `true` forces a subscription reconciliation pass even when cached plan data looks complete. Omit the parameter, or pass `false`, to use the default first-time-only reconciliation behavior. Invalid boolean values are rejected.  (optional) 

            try
            {
                // Get plan and usage snapshot
                UsageStats result = apiInstance.GetUsage(reconcile);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsageApi.GetUsage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetUsageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get plan and usage snapshot
    ApiResponse<UsageStats> response = apiInstance.GetUsageWithHttpInfo(reconcile);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsageApi.GetUsageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **reconcile** | **bool?** | For Stripe subscription users, &#x60;true&#x60; forces a subscription reconciliation pass even when cached plan data looks complete. Omit the parameter, or pass &#x60;false&#x60;, to use the default first-time-only reconciliation behavior. Invalid boolean values are rejected.  | [optional]  |

### Return type

[**UsageStats**](UsageStats.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Usage snapshot |  -  |
| **400** | Invalid query parameter |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getusagestats"></a>
# **GetUsageStats**
> UsageStats GetUsageStats (bool? reconcile = null)

Get plan and usage stats

Deprecated alias of `GET /v1/usage`; same contract. New integrations should use that path (the usage hub), with `GET /v1/usage/calls` and `GET /v1/usage/sms` for metered breakdowns.  Returns the current plan name, billing period, plan limits, and usage counts.  The response shape depends on the account's `billingSystem`:   * Stripe users: per-period `usage.uploads` / `usage.profiles` counters.   * Metronome (usage-based) users: `usage.connectedAccounts`,     `usage.xApiCallsByOperation` (per-operation X API call counts —     resolve keys via `GET /v1/billing/x-pricing`), plus a `spend`     block with `currentPeriodCents`, `xSpendCents`, and     `xSpendLimitCents`. The legacy `usage.xApiCalls` 3-tier     aggregate is still emitted for back-compat but excludes the     $0.200 URL tier and any future tiers — new clients should     consume `xApiCallsByOperation` only. 

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
    public class GetUsageStatsExample
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
            var apiInstance = new UsageApi(httpClient, config, httpClientHandler);
            var reconcile = true;  // bool? | For Stripe subscription users, `true` forces a subscription reconciliation pass even when cached plan data looks complete. Omit the parameter, or pass `false`, to use the default first-time-only reconciliation behavior. Invalid boolean values are rejected.  (optional) 

            try
            {
                // Get plan and usage stats
                UsageStats result = apiInstance.GetUsageStats(reconcile);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsageApi.GetUsageStats: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetUsageStatsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get plan and usage stats
    ApiResponse<UsageStats> response = apiInstance.GetUsageStatsWithHttpInfo(reconcile);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsageApi.GetUsageStatsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **reconcile** | **bool?** | For Stripe subscription users, &#x60;true&#x60; forces a subscription reconciliation pass even when cached plan data looks complete. Omit the parameter, or pass &#x60;false&#x60;, to use the default first-time-only reconciliation behavior. Invalid boolean values are rejected.  | [optional]  |

### Return type

[**UsageStats**](UsageStats.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Usage stats |  -  |
| **400** | Invalid query parameter |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getxapipricing"></a>
# **GetXApiPricing**
> XApiPricing GetXApiPricing ()

Get X/Twitter API pricing table

Returns Zernio's canonical X/Twitter API pricing table. Each X action has its own Metronome product and its own rate, and Zernio passes X API costs through at exact rates with zero markup.  The response is identical for every authenticated user (pricing is universal), so it is safe to cache on the client for the duration of a billing period.  To compute your own per-operation spend, pair this endpoint with `GET /v1/usage-stats` — that endpoint returns `usage.xApiCallsByOperation` keyed by the same `operation` field you get here. 

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
    public class GetXApiPricingExample
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
            var apiInstance = new UsageApi(httpClient, config, httpClientHandler);

            try
            {
                // Get X/Twitter API pricing table
                XApiPricing result = apiInstance.GetXApiPricing();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsageApi.GetXApiPricing: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetXApiPricingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get X/Twitter API pricing table
    ApiResponse<XApiPricing> response = apiInstance.GetXApiPricingWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsageApi.GetXApiPricingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**XApiPricing**](XApiPricing.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | X pricing table |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

