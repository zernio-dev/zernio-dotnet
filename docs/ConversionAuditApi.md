# Zernio.Api.ConversionAuditApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AuditConversionTracking**](ConversionAuditApi.md#auditconversiontracking) | **GET** /v1/conversion-audit | Audit a site&#39;s ad conversion tracking |
| [**CreateConversionAuditMonitor**](ConversionAuditApi.md#createconversionauditmonitor) | **POST** /v1/conversion-audit/monitors | Watch a domain |
| [**DeleteConversionAuditMonitor**](ConversionAuditApi.md#deleteconversionauditmonitor) | **DELETE** /v1/conversion-audit/monitors/{monitorId} | Stop watching a domain |
| [**GetLatestConversionAudit**](ConversionAuditApi.md#getlatestconversionaudit) | **GET** /v1/conversion-audit/latest | Get a host&#39;s latest stored conversion audit |
| [**GetMetaConversionAudit**](ConversionAuditApi.md#getmetaconversionaudit) | **GET** /v1/conversion-audit/meta-audit | Audit a connected Meta pixel from inside Events Manager |
| [**ListConversionAuditMonitors**](ConversionAuditApi.md#listconversionauditmonitors) | **GET** /v1/conversion-audit/monitors | List watched domains |

<a id="auditconversiontracking"></a>
# **AuditConversionTracking**
> ConversionAuditAnswer AuditConversionTracking (string url)

Audit a site's ad conversion tracking

Scan any public URL for ad-platform conversion tracking, score how much conversion signal it leaks before the ad platforms see it, and get a fix prompt to hand to a coding agent.  The API key is optional. Without one, a caller's IP address gets 20 scans a minute. The Zernio MCP server always needs a key, because its sign-in covers the whole connection.  The scan fetches the page (SSRF-guarded) and its Google Tag Manager containers, and can render it in a headless browser. It finds every ad platform's browser pixel, checks for visible server-side (Conversions API) tracking, and estimates the signal lost to ad blockers, browser limits and short cookie windows.  Visitors who decline consent are never counted as lost.  The scan reads the page only and changes nothing on the site. Like the free page, it publishes the result as the host's public report.  Reading the result:  - `report.visibility: \"limited\"` means some pixels load through a tag manager or a store platform, so only part of the setup is visible from outside. It does not mean the tracking failed or is missing. - `status: \"warn\"` (browser-only) is the leak: the platform is tracked in the browser but not server-side. - `status: \"good\"` (server-side) means conversions reach the platform server-side, which recovers most of that signal. - `fixPrompt` is the same fix prompt the Conversion Leak Report page shows: this scan's findings, then the steps to send conversions server-side with `POST /v1/events` and to verify them. - To fix the leak with Zernio, follow https://docs.zernio.com/products/server-side-tracking/fix-with-agent: a tracking site, its tag, a forwarding rule per network to the pixel the page runs, then a rescan. A network turns `good` once the site's events reached that pixel in the last 7 days. - `publicReport` links the host's public page on is-bleeding.com. A homepage scan that could read the site's pixels becomes that page's snapshot, the same as a scan on is-bleeding.com. Any other scan links the stored snapshot, taken at `scannedAt`, or returns null when the host has none.  Without a key, each IP address also shares one hourly ceiling with every other keyless caller. With a key, a user gets 60 scans a minute. 

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
    public class AuditConversionTrackingExample
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
            var apiInstance = new ConversionAuditApi(httpClient, config, httpClientHandler);
            var url = example.com;  // string | The website address to audit. A bare domain is accepted and normalized to https.

            try
            {
                // Audit a site's ad conversion tracking
                ConversionAuditAnswer result = apiInstance.AuditConversionTracking(url);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionAuditApi.AuditConversionTracking: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AuditConversionTrackingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Audit a site's ad conversion tracking
    ApiResponse<ConversionAuditAnswer> response = apiInstance.AuditConversionTrackingWithHttpInfo(url);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionAuditApi.AuditConversionTrackingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **url** | **string** | The website address to audit. A bare domain is accepted and normalized to https. |  |

### Return type

[**ConversionAuditAnswer**](ConversionAuditAnswer.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The scored audit and its fix prompt |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted. Behavior per platform:  - **Reddit:** rate-limits per connected Reddit user (1000 requests per 10-minute window), shared by every operation on that account. Retry after the window resets; repeated calls while exhausted do not succeed and keep the budget spent. - **Google Ads:** writes and reports run on one developer token shared by every Google Ads account on Zernio. It holds Standard access (no daily operations cap), so this only happens when Google throttles the token or your ad account. - **Google Ads envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60; (&#x60;ACCOUNT&#x60; when it is your own ad account&#39;s quota), &#x60;details.resetsAt&#x60; (ISO instant when Google accepts requests again) and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **YouTube Analytics:** reads (channel-insights, demographics, daily-views, video-retention) use the \&quot;Queries per day\&quot; quota of the Google Cloud project the account is connected through, shared with other Zernio customers, so a 429 is not your own volume. Resets at midnight Pacific Time. - **YouTube Analytics envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaExhausted: true&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60;, &#x60;details.resetsAt&#x60; and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **Meta ads:** every Meta throttle (codes 4, 17, 32, 613 and business-use-case codes 80000-80014) returns 429 &#x60;rate_limited&#x60;, even when Meta answers HTTP 400. &#x60;Retry-After&#x60; comes from Meta&#39;s &#x60;x-business-use-case-usage&#x60; estimate when sent, else Meta&#39;s 60-second minimum (30 seconds for the one-write-per-30-seconds limit on one object). - **Pinterest ads:** limits per user and app, per category (ads_read, ads_write, ads_analytics). &#x60;Retry-After&#x60; comes from Pinterest&#39;s &#x60;x-ratelimit-reset&#x60; when sent, otherwise 60 seconds. - **TikTok ads:** limits per app and per endpoint (per second, minute and day), answering overage with code 40100 or code 40002 &#x60;OVER_QPS_LIMIT&#x60;. Both return 429 &#x60;rate_limited&#x60; with &#x60;platform: tiktok&#x60; and &#x60;Retry-After: 10&#x60;. Space out bulk reads (e.g. one ad at a time per advertiser) instead of retrying at once.  **TikTok Smart+ review read** (&#x60;GET /v1/ads/{adId}/tiktok-smart-plus-review&#x60;) has its own stricter TikTok quota. After an overage, Zernio answers 429 for that advertiser and connection without calling TikTok for about 60 seconds, then 120, up to 240 while TikTok keeps refusing, each with up to 10% random jitter.  A successful call holds nothing back; the next overage pauses about 60 seconds again. &#x60;Retry-After&#x60; is the time left. The advertiser-wide read (&#x60;GET /v1/ads/tiktok-smart-plus-reviews&#x60;) answers 200 with &#x60;retryAfterSeconds&#x60; and &#x60;refreshState&#x60; instead. Keep one request in flight per advertiser there.  |  * Retry-After - Seconds until card payments are tried again. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createconversionauditmonitor"></a>
# **CreateConversionAuditMonitor**
> ConversionAuditMonitorAnswer CreateConversionAuditMonitor (CreateConversionAuditMonitorRequest createConversionAuditMonitorRequest)

Watch a domain

Watch a domain's conversion tracking. Zernio rescans its homepage once a day and emails the account's address when tracking breaks, with what changed and the fix prompt for a coding agent. A break is:  - a score drop of 5 points or more - an ad network that stops tracking or stops firing - a pixel that starts firing before the cookie banner is answered - a server-side path that disappears  A break is confirmed by a second scan before any email goes out. The first check compares against the host's stored report when it has one, so run `auditConversionTracking` first to start from today's state.  Watching a domain you already watch returns it with `created: false` and status `200`. An account can watch up to 25 domains. 

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
    public class CreateConversionAuditMonitorExample
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
            var apiInstance = new ConversionAuditApi(httpClient, config, httpClientHandler);
            var createConversionAuditMonitorRequest = new CreateConversionAuditMonitorRequest(); // CreateConversionAuditMonitorRequest | 

            try
            {
                // Watch a domain
                ConversionAuditMonitorAnswer result = apiInstance.CreateConversionAuditMonitor(createConversionAuditMonitorRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionAuditApi.CreateConversionAuditMonitor: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateConversionAuditMonitorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Watch a domain
    ApiResponse<ConversionAuditMonitorAnswer> response = apiInstance.CreateConversionAuditMonitorWithHttpInfo(createConversionAuditMonitorRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionAuditApi.CreateConversionAuditMonitorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createConversionAuditMonitorRequest** | [**CreateConversionAuditMonitorRequest**](CreateConversionAuditMonitorRequest.md) |  |  |

### Return type

[**ConversionAuditMonitorAnswer**](ConversionAuditMonitorAnswer.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | You already watch this domain |  -  |
| **201** | The domain is now watched |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The account already watches 25 domains, or the key&#39;s resource group is disabled |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteconversionauditmonitor"></a>
# **DeleteConversionAuditMonitor**
> DeleteAutomationTemplate200Response DeleteConversionAuditMonitor (string monitorId)

Stop watching a domain

Stops the daily checks and alert emails for this domain. The host's public report stays.

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
    public class DeleteConversionAuditMonitorExample
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
            var apiInstance = new ConversionAuditApi(httpClient, config, httpClientHandler);
            var monitorId = "monitorId_example";  // string | The monitor's `id`, from `listConversionAuditMonitors` or `createConversionAuditMonitor`.

            try
            {
                // Stop watching a domain
                DeleteAutomationTemplate200Response result = apiInstance.DeleteConversionAuditMonitor(monitorId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionAuditApi.DeleteConversionAuditMonitor: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteConversionAuditMonitorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Stop watching a domain
    ApiResponse<DeleteAutomationTemplate200Response> response = apiInstance.DeleteConversionAuditMonitorWithHttpInfo(monitorId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionAuditApi.DeleteConversionAuditMonitorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **monitorId** | **string** | The monitor&#39;s &#x60;id&#x60;, from &#x60;listConversionAuditMonitors&#x60; or &#x60;createConversionAuditMonitor&#x60;. |  |

### Return type

[**DeleteAutomationTemplate200Response**](DeleteAutomationTemplate200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The domain is no longer watched |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getlatestconversionaudit"></a>
# **GetLatestConversionAudit**
> GetLatestConversionAudit200Response GetLatestConversionAudit (string host)

Get a host's latest stored conversion audit

Read the latest stored Conversion Leak Report for a host without running a new scan. Each homepage scan on is-bleeding.com that could read the site's pixels replaces that host's stored report. Scans made with `auditConversionTracking` are stored the same way.  The API key is optional. Without one, a caller's IP address gets 60 requests a minute. The Zernio MCP server always needs a key.  Returns `404` when the host has no stored report. Run `auditConversionTracking` to scan it now. 

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
    public class GetLatestConversionAuditExample
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
            var apiInstance = new ConversionAuditApi(httpClient, config, httpClientHandler);
            var host = example.com;  // string | The host to look up. A full URL is reduced to its host; `www.` and letter case are ignored.

            try
            {
                // Get a host's latest stored conversion audit
                GetLatestConversionAudit200Response result = apiInstance.GetLatestConversionAudit(host);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionAuditApi.GetLatestConversionAudit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetLatestConversionAuditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a host's latest stored conversion audit
    ApiResponse<GetLatestConversionAudit200Response> response = apiInstance.GetLatestConversionAuditWithHttpInfo(host);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionAuditApi.GetLatestConversionAuditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **host** | **string** | The host to look up. A full URL is reduced to its host; &#x60;www.&#x60; and letter case are ignored. |  |

### Return type

[**GetLatestConversionAudit200Response**](GetLatestConversionAudit200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The stored report, its fix prompt and its public page |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted. Behavior per platform:  - **Reddit:** rate-limits per connected Reddit user (1000 requests per 10-minute window), shared by every operation on that account. Retry after the window resets; repeated calls while exhausted do not succeed and keep the budget spent. - **Google Ads:** writes and reports run on one developer token shared by every Google Ads account on Zernio. It holds Standard access (no daily operations cap), so this only happens when Google throttles the token or your ad account. - **Google Ads envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60; (&#x60;ACCOUNT&#x60; when it is your own ad account&#39;s quota), &#x60;details.resetsAt&#x60; (ISO instant when Google accepts requests again) and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **YouTube Analytics:** reads (channel-insights, demographics, daily-views, video-retention) use the \&quot;Queries per day\&quot; quota of the Google Cloud project the account is connected through, shared with other Zernio customers, so a 429 is not your own volume. Resets at midnight Pacific Time. - **YouTube Analytics envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaExhausted: true&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60;, &#x60;details.resetsAt&#x60; and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **Meta ads:** every Meta throttle (codes 4, 17, 32, 613 and business-use-case codes 80000-80014) returns 429 &#x60;rate_limited&#x60;, even when Meta answers HTTP 400. &#x60;Retry-After&#x60; comes from Meta&#39;s &#x60;x-business-use-case-usage&#x60; estimate when sent, else Meta&#39;s 60-second minimum (30 seconds for the one-write-per-30-seconds limit on one object). - **Pinterest ads:** limits per user and app, per category (ads_read, ads_write, ads_analytics). &#x60;Retry-After&#x60; comes from Pinterest&#39;s &#x60;x-ratelimit-reset&#x60; when sent, otherwise 60 seconds. - **TikTok ads:** limits per app and per endpoint (per second, minute and day), answering overage with code 40100 or code 40002 &#x60;OVER_QPS_LIMIT&#x60;. Both return 429 &#x60;rate_limited&#x60; with &#x60;platform: tiktok&#x60; and &#x60;Retry-After: 10&#x60;. Space out bulk reads (e.g. one ad at a time per advertiser) instead of retrying at once.  **TikTok Smart+ review read** (&#x60;GET /v1/ads/{adId}/tiktok-smart-plus-review&#x60;) has its own stricter TikTok quota. After an overage, Zernio answers 429 for that advertiser and connection without calling TikTok for about 60 seconds, then 120, up to 240 while TikTok keeps refusing, each with up to 10% random jitter.  A successful call holds nothing back; the next overage pauses about 60 seconds again. &#x60;Retry-After&#x60; is the time left. The advertiser-wide read (&#x60;GET /v1/ads/tiktok-smart-plus-reviews&#x60;) answers 200 with &#x60;retryAfterSeconds&#x60; and &#x60;refreshState&#x60; instead. Keep one request in flight per advertiser there.  |  * Retry-After - Seconds until card payments are tried again. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getmetaconversionaudit"></a>
# **GetMetaConversionAudit**
> MetaDatasetAudit GetMetaConversionAudit (string accountId, string? adAccountId = null, string? pixelId = null)

Audit a connected Meta pixel from inside Events Manager

The connected follow-up to the Conversion Leak Report. A page scan only sees the browser; this reads what Meta itself recorded for the ad account's pixel (dataset) with the connection's own token, over the last 7 days.  ### What it reads  - each event's volume per day, its last 24 hours and the last hour Meta counted it in - the share of each event that arrived through the Conversions API (server) rather than the browser pixel - Event Match Quality per event, with the coverage of every customer-information key Meta matched on (email, phone, external id, IP address, user agent, `fbp`, `fbc`, name and address fields) - the event_id, external_id and fbp deduplication coverage of browser and server copies, where an event has both - Meta's diagnostics for the dataset and its failed dataset checks - whether automatic advanced matching and first-party cookies are on  Each `findings` entry is a problem one of those numbers shows, with its fix and who makes it (`fix.by`):  - `zernio`: turning on Zernio server-side events or the Zernio site tag fixes it - `you`: a change in your site or API call - `meta`: a setting only Events Manager has  Meta does not return a business's verified domains or an Aggregated Event Measurement setup to this API, so both are listed under `unavailable`, with any read Meta refused.  `accountId` is a Meta ads connection (or the Facebook account it belongs to). Without `adAccountId`, the first selected ad account that has a pixel is audited; without `pixelId`, its most recently active pixel. The result is cached for 10 minutes per pixel. 

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
    public class GetMetaConversionAuditExample
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
            var apiInstance = new ConversionAuditApi(httpClient, config, httpClientHandler);
            var accountId = 6a10b66d520992756da032cb;  // string | The Meta ads connection to read with.
            var adAccountId = act_757082720485182;  // string? | The ad account whose pixel is audited. Must be selected on the connection. (optional) 
            var pixelId = 1729525464415281;  // string? | One of the ad account's pixels (`datasets[].id`). (optional) 

            try
            {
                // Audit a connected Meta pixel from inside Events Manager
                MetaDatasetAudit result = apiInstance.GetMetaConversionAudit(accountId, adAccountId, pixelId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionAuditApi.GetMetaConversionAudit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetMetaConversionAuditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Audit a connected Meta pixel from inside Events Manager
    ApiResponse<MetaDatasetAudit> response = apiInstance.GetMetaConversionAuditWithHttpInfo(accountId, adAccountId, pixelId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionAuditApi.GetMetaConversionAuditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The Meta ads connection to read with. |  |
| **adAccountId** | **string?** | The ad account whose pixel is audited. Must be selected on the connection. | [optional]  |
| **pixelId** | **string?** | One of the ad account&#39;s pixels (&#x60;datasets[].id&#x60;). | [optional]  |

### Return type

[**MetaDatasetAudit**](MetaDatasetAudit.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The pixel&#39;s events, findings and what Meta did not expose |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The ad account is not selected on the connection, or the key cannot use ads |  -  |
| **404** | Resource not found |  -  |
| **501** | The connection is not a Meta connection |  -  |
| **502** | Meta refused to list the ad account&#39;s pixels |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listconversionauditmonitors"></a>
# **ListConversionAuditMonitors**
> ListConversionAuditMonitors200Response ListConversionAuditMonitors ()

List watched domains

The domains you watch with the Conversion Leak Report, each with its last score and the score of each daily check.  Zernio rescans every watched domain once a day. When tracking breaks, it emails you what changed and the fix prompt. `createConversionAuditMonitor` lists what counts as a break. 

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
    public class ListConversionAuditMonitorsExample
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
            var apiInstance = new ConversionAuditApi(httpClient, config, httpClientHandler);

            try
            {
                // List watched domains
                ListConversionAuditMonitors200Response result = apiInstance.ListConversionAuditMonitors();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionAuditApi.ListConversionAuditMonitors: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListConversionAuditMonitorsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List watched domains
    ApiResponse<ListConversionAuditMonitors200Response> response = apiInstance.ListConversionAuditMonitorsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionAuditApi.ListConversionAuditMonitorsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListConversionAuditMonitors200Response**](ListConversionAuditMonitors200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Your watched domains, sorted by host |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

