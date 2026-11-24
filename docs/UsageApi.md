# Zernio.Api.UsageApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetBilling**](UsageApi.md#getbilling) | **GET** /v1/billing | Account billing snapshot (plan, cycle, balance, caps, status) |
| [**GetCallsUsage**](UsageApi.md#getcallsusage) | **GET** /v1/usage/calls | Calling usage and cost |
| [**GetSmsUsage**](UsageApi.md#getsmsusage) | **GET** /v1/usage/sms | SMS usage (volumes) |
| [**GetUsage**](UsageApi.md#getusage) | **GET** /v1/usage | Usage snapshot (default) or billed-spend metering (with params) |
| [**GetUsageStats**](UsageApi.md#getusagestats) | **GET** /v1/usage-stats | Get plan and usage snapshot (plan, limits, payment status) |
| [**GetXApiPricing**](UsageApi.md#getxapipricing) | **GET** /v1/billing/x-pricing | Get X API pricing table |

<a id="getbilling"></a>
# **GetBilling**
> BillingSnapshot GetBilling ()

Account billing snapshot (plan, cycle, balance, caps, status)

The billing \"wallet/statement\" view: current plan, billing cycle, accrued balance + remaining credits this period, spend caps, and payment / access status. This is the billing half of the legacy `/v1/usage-stats` snapshot. The per-product consumption half is metering and lives on `GET /v1/usage`.  Accounts on usage-based billing get a populated `balance`; legacy Stripe accounts get `balance: null` plus a deprecated `legacy.limits` block and, when payment-blocked, `status.openInvoiceUrl` / `status.declineReason`. 

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
    public class GetBillingExample
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
                // Account billing snapshot (plan, cycle, balance, caps, status)
                BillingSnapshot result = apiInstance.GetBilling();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsageApi.GetBilling: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBillingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Account billing snapshot (plan, cycle, balance, caps, status)
    ApiResponse<BillingSnapshot> response = apiInstance.GetBillingWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsageApi.GetBillingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**BillingSnapshot**](BillingSnapshot.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Billing snapshot |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcallsusage"></a>
# **GetCallsUsage**
> GetCallsUsage200Response GetCallsUsage (DateTime? since = null, DateTime? until = null, string? channel = null, string? number = null, string? groupBy = null, string? profileId = null, string? externalId = null)

Calling usage and cost

Aggregated calling usage across your numbers, both channels (WhatsApp Business Calling + regular phone/PSTN): call counts, answered counts, minutes, and cost. Use it for cost visibility or to rebill your own customers per number.  Costs come from each call's billing snapshot, so this endpoint always agrees with the invoice: `billableUSD` is what Zernio bills; `metaUSD` is the WhatsApp per-minute charge Meta bills directly to your WABA (display only, never billed by Zernio).  Optional `groupBy` returns a breakdown by UTC day, by your number, by channel, or by profile. Defaults to the last 30 days.  ### Per profile  A call belongs to the profile of the account (number) it was placed on.  - `profileId` or `externalId` scopes every figure to one profile. - `groupBy=profile` returns one group per profile carrying its `profileId` and `externalId`. - Calls on numbers outside any of your profiles count in `totals` but in no group. - A profile-scoped API key or member only ever sees its own profiles' calls, with or without a filter (since 1.630.0), so `totals` and every group cover those profiles only. Full-access keys and sessions see the whole team. 

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
            var profileId = "profileId_example";  // string? | Scope to the calls of this profile. Mutually exclusive with `externalId`. 404 when the profile is not in your team or outside a scoped key's profiles. (optional) 
            var externalId = "externalId_example";  // string? | Same as `profileId`, naming the profile by the `externalId` you set on it. 404 when none of your visible profiles carries it; 400 when two of them do. (optional) 

            try
            {
                // Calling usage and cost
                GetCallsUsage200Response result = apiInstance.GetCallsUsage(since, until, channel, number, groupBy, profileId, externalId);
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
    // Calling usage and cost
    ApiResponse<GetCallsUsage200Response> response = apiInstance.GetCallsUsageWithHttpInfo(since, until, channel, number, groupBy, profileId, externalId);
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
| **profileId** | **string?** | Scope to the calls of this profile. Mutually exclusive with &#x60;externalId&#x60;. 404 when the profile is not in your team or outside a scoped key&#39;s profiles. | [optional]  |
| **externalId** | **string?** | Same as &#x60;profileId&#x60;, naming the profile by the &#x60;externalId&#x60; you set on it. 404 when none of your visible profiles carries it; 400 when two of them do. | [optional]  |

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
| **400** | since must be before until, &#x60;profileId&#x60; together with &#x60;externalId&#x60;, or an &#x60;externalId&#x60; shared by two of your profiles. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The profile named by &#x60;profileId&#x60; / &#x60;externalId&#x60; is not visible to the caller. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getsmsusage"></a>
# **GetSmsUsage**
> GetSmsUsage200Response GetSmsUsage (DateTime? since = null, DateTime? until = null, string? number = null, string? groupBy = null, string? profileId = null, string? externalId = null)

SMS usage (volumes)

Aggregated SMS/MMS volumes across your numbers: sent, received, and total message counts, with an optional breakdown by UTC day or by number. Defaults to the last 30 days.  Volumes only, deliberately: SMS cost is carrier-rated asynchronously and billed to your invoice, so per-message cost is not available here. Calling usage (GET /v1/usage/calls) does include billable cost.  ### Per profile  A message belongs to the profile of the SMS number it went through.  - `profileId` or `externalId` scopes the counts to one profile. Combined with `number`, only that number's messages on that profile count. - `groupBy=profile` returns one group per profile carrying its `profileId` and `externalId`. - Alphanumeric sender IDs sit on no profile, so their messages count in `totals` but in no group. - A profile-scoped API key or member only ever sees its own profiles' messages, with or without a filter (since 1.630.0). Full-access keys and sessions see every number. 

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
            var profileId = "profileId_example";  // string? | Scope to the messages of this profile. Mutually exclusive with `externalId`. 404 when the profile is not in your team or outside a scoped key's profiles. (optional) 
            var externalId = "externalId_example";  // string? | Same as `profileId`, naming the profile by the `externalId` you set on it. 404 when none of your visible profiles carries it; 400 when two of them do. (optional) 

            try
            {
                // SMS usage (volumes)
                GetSmsUsage200Response result = apiInstance.GetSmsUsage(since, until, number, groupBy, profileId, externalId);
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
    ApiResponse<GetSmsUsage200Response> response = apiInstance.GetSmsUsageWithHttpInfo(since, until, number, groupBy, profileId, externalId);
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
| **profileId** | **string?** | Scope to the messages of this profile. Mutually exclusive with &#x60;externalId&#x60;. 404 when the profile is not in your team or outside a scoped key&#39;s profiles. | [optional]  |
| **externalId** | **string?** | Same as &#x60;profileId&#x60;, naming the profile by the &#x60;externalId&#x60; you set on it. 404 when none of your visible profiles carries it; 400 when two of them do. | [optional]  |

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
| **400** | since must be before until, &#x60;profileId&#x60; together with &#x60;externalId&#x60;, or an &#x60;externalId&#x60; shared by two of your profiles. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | &#x60;number&#x60; doesn&#39;t match any of your SMS-enabled numbers, or the profile named by &#x60;profileId&#x60; / &#x60;externalId&#x60; is not visible to the caller. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getusage"></a>
# **GetUsage**
> GetUsage200Response GetUsage (bool? reconcile = null, string? range = null, DateOnly? from = null, DateOnly? to = null, string? granularity = null, string? groupBy = null, string? profileId = null, string? externalId = null, string? accountId = null)

Usage snapshot (default) or billed-spend metering (with params)

Dual-mode endpoint, selected by query params, and fully backward compatible.  ### Without metering params (the default)  Returns the plan / quota / usage snapshot: plan name, billing period, limits, usage counts, access state. Identical to `GET /v1/usage-stats`. Existing integrations keep working unchanged.  ### With `range`, `granularity`, `from`, or `to`  Returns usage METERING: billed spend (USD) by product family over the window, at `day` / `month` / `total` granularity. Product families: `accounts`, `numbers`, `imessage`, `rcs`, `calls`, `sms`, `messages`, `verify`, `dlc`, `xApi`, `ads`, `automations`, `websiteEvents`, `credits`, `other`.  Data comes from the usage-based invoice breakdown (the CHARGE view, which always reconciles with what gets billed). Also served at `GET /v1/usage/daily`.  Usage-based accounts only: legacy Stripe accounts get `{ \"supported\": false, \"days\": [] }`.  ### Attribution (metering mode)  `groupBy=profile|account` adds an `attribution` breakdown of the window's spend per profile or account. It is assembled from your own records and pro-rated against the invoice so `sum(groups) + unattributed` equals `totals` exactly.  `profileId` / `accountId` instead project the whole payload (`days`, `totals`, `lineItems`) onto that one group:  - `peaks`, `callUsage` and `tax` are then `null` (team-level facts). - Projected `days` spread the group's period share over each day (usage is attributed per period, not per day). - `profileId` / `accountId` on their own do not select metering mode: pair them with `range`. - `externalId` names the profile by the id you set on it (`POST /v1/profiles`), so you can bill a tenant without storing our profile id.  With `groupBy=profile`, each group also carries `profileId` and `externalId`.  Profile-scoped API keys and members only see their profiles' groups (`attribution.restricted: true`, with `totals` summing the visible groups).  Credits, managed messages, RCS messages, ad automations, Verify and website events are always unattributed.  iMessage sender and RCS agent fees go to the profile of the sender or agent. Automation runs split each day's fee by that day's runs.  A 10DLC fee goes to a profile only when its registration names one. Registrations filed by API or dashboard belong to the owner and stay unattributed.  A caller that sees the whole workspace gets `restricted: false` and the same `totals` as without `groupBy`. Shares are measured over everything the bill and its members carry, so `unattributed` can include spend outside the workspace, never named.  Since 1.817.0 every billed account has one even price: the window's `accounts` total, after tiers and the monthly credit, divided by the billed accounts your members have connected now. Before, the oldest accounts took the credit and could show $0. Your invoice did not change.  Example: 5 accounts cost $30 minus the $12 credit, $18, so $3.60 each. A profile with 2 of them shows $7.20. In a contract's first month, a credit carried over is unattributed instead, so they show $6.00 each.  Since 1.630.0 a profile-scoped key or member never gets the team payload in metering mode: without `groupBy` or a filter, `days`, `totals` and `lineItems` are projected onto its visible profiles, `peaks`, `callUsage` and `tax` are `null`, and no `attribution` is returned. Full-access keys and sessions keep the team payload.  ### Related endpoints  - Per-domain consumption *volumes*: `GET /v1/usage/calls` and `GET /v1/usage/sms`. - The billing statement (balance, credits, caps, payment status): `GET /v1/billing`. 

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
            var reconcile = true;  // bool? | Snapshot mode only. For Stripe subscription users, `true` forces a subscription reconciliation pass even when cached plan data looks complete.  (optional) 
            var range = "cycle";  // string? | Window to report. `cycle` / `prev-cycle` resolve to the customer's real billing-period bounds (falling back to a trailing 30 days when no invoice exists yet); `7d`…`12mo` are trailing windows; `custom` uses `from` / `to`.  (optional)  (default to cycle)
            var from = DateOnly.Parse("2013-10-20");  // DateOnly? | Inclusive start (UTC date). Required when `range=custom`. (optional) 
            var to = DateOnly.Parse("2013-10-20");  // DateOnly? | Inclusive end (UTC date). Required when `range=custom`. Max span 366 days. (optional) 
            var granularity = "day";  // string? | Bucketing of the `days` series: `day` (one row per UTC day), `month` (one row per calendar month, dated to the 1st), or `total` (no series, read `totals`). Does not affect `totals`.  (optional)  (default to day)
            var groupBy = "profile";  // string? | Metering mode. Adds `attribution`: the window's spend split per profile or per account (keys are ids; resolve names via `GET /v1/profiles` / `GET /v1/accounts`). (optional) 
            var profileId = "profileId_example";  // string? | Metering mode (pair with `range`). Project the payload onto this profile's attributed share. Mutually exclusive with `externalId` and `accountId`, and `groupBy` (if given) must be `profile`; 404 when the profile is not in your team (or outside a scoped key's profiles). (optional) 
            var externalId = "externalId_example";  // string? | Metering mode (pair with `range`). Same as `profileId`, naming the profile by the `externalId` you set on it. Ignored without metering params. 404 when none of your visible profiles carries it; 400 when two of them do (externalId is unique per user, not per team), then filter by `profileId`. (optional) 
            var accountId = "accountId_example";  // string? | Metering mode (pair with `range`). Project the payload onto this account's attributed share. Mutually exclusive with `profileId` and `externalId`, and `groupBy` (if given) must be `account`; 404 when the account is not visible to the caller. (optional) 

            try
            {
                // Usage snapshot (default) or billed-spend metering (with params)
                GetUsage200Response result = apiInstance.GetUsage(reconcile, range, from, to, granularity, groupBy, profileId, externalId, accountId);
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
    // Usage snapshot (default) or billed-spend metering (with params)
    ApiResponse<GetUsage200Response> response = apiInstance.GetUsageWithHttpInfo(reconcile, range, from, to, granularity, groupBy, profileId, externalId, accountId);
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
| **reconcile** | **bool?** | Snapshot mode only. For Stripe subscription users, &#x60;true&#x60; forces a subscription reconciliation pass even when cached plan data looks complete.  | [optional]  |
| **range** | **string?** | Window to report. &#x60;cycle&#x60; / &#x60;prev-cycle&#x60; resolve to the customer&#39;s real billing-period bounds (falling back to a trailing 30 days when no invoice exists yet); &#x60;7d&#x60;…&#x60;12mo&#x60; are trailing windows; &#x60;custom&#x60; uses &#x60;from&#x60; / &#x60;to&#x60;.  | [optional] [default to cycle] |
| **from** | **DateOnly?** | Inclusive start (UTC date). Required when &#x60;range&#x3D;custom&#x60;. | [optional]  |
| **to** | **DateOnly?** | Inclusive end (UTC date). Required when &#x60;range&#x3D;custom&#x60;. Max span 366 days. | [optional]  |
| **granularity** | **string?** | Bucketing of the &#x60;days&#x60; series: &#x60;day&#x60; (one row per UTC day), &#x60;month&#x60; (one row per calendar month, dated to the 1st), or &#x60;total&#x60; (no series, read &#x60;totals&#x60;). Does not affect &#x60;totals&#x60;.  | [optional] [default to day] |
| **groupBy** | **string?** | Metering mode. Adds &#x60;attribution&#x60;: the window&#39;s spend split per profile or per account (keys are ids; resolve names via &#x60;GET /v1/profiles&#x60; / &#x60;GET /v1/accounts&#x60;). | [optional]  |
| **profileId** | **string?** | Metering mode (pair with &#x60;range&#x60;). Project the payload onto this profile&#39;s attributed share. Mutually exclusive with &#x60;externalId&#x60; and &#x60;accountId&#x60;, and &#x60;groupBy&#x60; (if given) must be &#x60;profile&#x60;; 404 when the profile is not in your team (or outside a scoped key&#39;s profiles). | [optional]  |
| **externalId** | **string?** | Metering mode (pair with &#x60;range&#x60;). Same as &#x60;profileId&#x60;, naming the profile by the &#x60;externalId&#x60; you set on it. Ignored without metering params. 404 when none of your visible profiles carries it; 400 when two of them do (externalId is unique per user, not per team), then filter by &#x60;profileId&#x60;. | [optional]  |
| **accountId** | **string?** | Metering mode (pair with &#x60;range&#x60;). Project the payload onto this account&#39;s attributed share. Mutually exclusive with &#x60;profileId&#x60; and &#x60;externalId&#x60;, and &#x60;groupBy&#x60; (if given) must be &#x60;account&#x60;; 404 when the account is not visible to the caller. | [optional]  |

### Return type

[**GetUsage200Response**](GetUsage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Snapshot (no metering params) or billed spend by product over the window (with metering params).  |  -  |
| **400** | Invalid query parameter, conflicting filters (&#x60;profileId&#x60; / &#x60;externalId&#x60; / &#x60;accountId&#x60;), or an &#x60;externalId&#x60; shared by two of your profiles. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The profile (&#x60;profileId&#x60; / &#x60;externalId&#x60;) or account is not visible to the caller. |  -  |
| **429** | The billing backend is rate limiting reads (code &#x60;rate_limited&#x60;). Wait &#x60;Retry-After&#x60; seconds and retry. Before 1.81.0 this surfaced as a 500. |  * Retry-After - Seconds until card payments are tried again. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getusagestats"></a>
# **GetUsageStats**
> UsageStats GetUsageStats (bool? reconcile = null, string? profileId = null, string? externalId = null)

Get plan and usage snapshot (plan, limits, payment status)

The plan / quota / payment-status snapshot: current plan name, billing period, plan limits, usage counts, and access state.  Identical to a bare `GET /v1/usage` call (this path is its deprecated alias).  ### Related endpoints  - Billed spend by product: call `GET /v1/usage` with `range` / `granularity` params. - Billed spend per profile, by your own `externalId`: `GET /v1/usage?range=cycle&groupBy=profile` ([what each customer costs you](/multi-tenant)). - The statement view (balance, credits, caps, payment status) lives at `GET /v1/billing`.  ### Response shape  The response shape depends on the account's `billingSystem`:  - Stripe users: per-period `usage.uploads` / `usage.profiles` counters. - Usage-based billing users: `usage.connectedAccounts`, `usage.xApiCallsByOperation` (per-operation X API call counts; resolve keys via `GET /v1/billing/x-pricing`), plus a `spend` block with `currentPeriodCents`, `xSpendCents`, and `xSpendLimitCents`.  The legacy `usage.xApiCalls` 3-tier aggregate is still emitted for back-compat. It excludes the $0.200 URL tier and any future tiers, so new clients should consume `xApiCallsByOperation` only.  ### Per profile  `profileId` or `externalId` adds a `profile` block with the counters that are meaningful per profile (`usage.connectedAccounts`). Everything else (plan, limits, uploads, X usage, spend, payment state) stays team-level. These filters work on this path only: a bare `GET /v1/usage` ignores them.  Since 1.630.0 a profile-scoped API key or member gets a `profiles` array with one block per profile it can see (or the single `profile` block when it filters), and `usage.connectedAccounts` / `usage.profiles` count only those profiles.  Plan, billing and payment fields are unchanged. Full-access keys and sessions keep the team counts and get no `profiles` array. 

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
            var profileId = "profileId_example";  // string? | Add the `profile` block for this profile. Mutually exclusive with `externalId`. 404 when the profile is not in your team or outside a scoped key's profiles. (optional) 
            var externalId = "externalId_example";  // string? | Same as `profileId`, naming the profile by the `externalId` you set on it. 404 when none of your visible profiles carries it; 400 when two of them do. (optional) 

            try
            {
                // Get plan and usage snapshot (plan, limits, payment status)
                UsageStats result = apiInstance.GetUsageStats(reconcile, profileId, externalId);
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
    // Get plan and usage snapshot (plan, limits, payment status)
    ApiResponse<UsageStats> response = apiInstance.GetUsageStatsWithHttpInfo(reconcile, profileId, externalId);
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
| **profileId** | **string?** | Add the &#x60;profile&#x60; block for this profile. Mutually exclusive with &#x60;externalId&#x60;. 404 when the profile is not in your team or outside a scoped key&#39;s profiles. | [optional]  |
| **externalId** | **string?** | Same as &#x60;profileId&#x60;, naming the profile by the &#x60;externalId&#x60; you set on it. 404 when none of your visible profiles carries it; 400 when two of them do. | [optional]  |

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
| **400** | Invalid query parameter, &#x60;profileId&#x60; together with &#x60;externalId&#x60;, or an &#x60;externalId&#x60; shared by two of your profiles. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The user, or the profile named by &#x60;profileId&#x60; / &#x60;externalId&#x60;, was not found. |  -  |
| **429** | The billing backend is rate limiting reads (code &#x60;rate_limited&#x60;). Wait &#x60;Retry-After&#x60; seconds and retry. Before 1.81.0 this surfaced as a 500. |  * Retry-After - Seconds until card payments are tried again. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getxapipricing"></a>
# **GetXApiPricing**
> XApiPricing GetXApiPricing ()

Get X API pricing table

Returns Zernio's canonical X API pricing table. Each X action has its own billing product and its own rate, and Zernio passes X API costs through at exact rates with zero markup.  The response is identical for every authenticated user (pricing is universal), so it is safe to cache on the client for the duration of a billing period.  To compute your own per-operation spend, pair this endpoint with `GET /v1/usage-stats`, which returns `usage.xApiCallsByOperation` keyed by the same `operation` field you get here. 

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
                // Get X API pricing table
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
    // Get X API pricing table
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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

