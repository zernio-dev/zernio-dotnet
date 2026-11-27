# Zernio.Api.ConversionsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddAdConversionAssociations**](ConversionsApi.md#addadconversionassociations) | **POST** /v1/ads/conversions/destinations/{destinationId}/associations | Associate campaigns |
| [**AddConversionAssociations**](ConversionsApi.md#addconversionassociations) | **POST** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | Associate campaigns |
| [**AdjustConversions**](ConversionsApi.md#adjustconversions) | **POST** /v1/ads/conversions/adjustments | Adjust uploaded conversions |
| [**CheckTrackingSiteProxy**](ConversionsApi.md#checktrackingsiteproxy) | **POST** /v1/tracking-sites/{siteId}/proxy-check | Check a tracking site&#39;s own-domain path |
| [**CreateAdConversionDestination**](ConversionsApi.md#createadconversiondestination) | **POST** /v1/ads/conversions/destinations | Create a conversion destination |
| [**CreateAdCustomConversion**](ConversionsApi.md#createadcustomconversion) | **POST** /v1/ads/conversions/custom-conversions | Create custom conversion |
| [**CreateConversionAction**](ConversionsApi.md#createconversionaction) | **POST** /v1/ads/conversions/actions | Create conversion action |
| [**CreateConversionDestination**](ConversionsApi.md#createconversiondestination) | **POST** /v1/accounts/{accountId}/conversion-destinations | Create a conversion destination |
| [**CreateCustomConversionGoal**](ConversionsApi.md#createcustomconversiongoal) | **POST** /v1/ads/conversions/custom-goals | Create a custom conversion goal |
| [**CreateEventDestination**](ConversionsApi.md#createeventdestination) | **POST** /v1/events/destinations | Add an event destination |
| [**CreateForwardingRule**](ConversionsApi.md#createforwardingrule) | **POST** /v1/events/forwarding-rules | Add a forwarding rule |
| [**CreateTrackingSite**](ConversionsApi.md#createtrackingsite) | **POST** /v1/tracking-sites | Turn on server-side tracking for a website |
| [**DeleteAdConversionDestination**](ConversionsApi.md#deleteadconversiondestination) | **DELETE** /v1/ads/conversions/destinations/{destinationId} | Delete a conversion destination |
| [**DeleteConversionDestination**](ConversionsApi.md#deleteconversiondestination) | **DELETE** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Delete a conversion destination |
| [**DeleteEventDestination**](ConversionsApi.md#deleteeventdestination) | **DELETE** /v1/events/destinations/{destinationId} | Remove an event destination |
| [**DeleteForwardingRule**](ConversionsApi.md#deleteforwardingrule) | **DELETE** /v1/events/forwarding-rules/{ruleId} | Remove a forwarding rule |
| [**DeleteTrackingSite**](ConversionsApi.md#deletetrackingsite) | **DELETE** /v1/tracking-sites/{siteId} | Delete a tracking site |
| [**GetAdConversionDestination**](ConversionsApi.md#getadconversiondestination) | **GET** /v1/ads/conversions/destinations/{destinationId} | Get a conversion destination |
| [**GetAdConversionMetrics**](ConversionsApi.md#getadconversionmetrics) | **GET** /v1/ads/conversions/destinations/{destinationId}/metrics | Get attribution metrics |
| [**GetConversionDestination**](ConversionsApi.md#getconversiondestination) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Get a conversion destination |
| [**GetConversionMetrics**](ConversionsApi.md#getconversionmetrics) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/metrics | Get attribution metrics |
| [**GetConversionPaths**](ConversionsApi.md#getconversionpaths) | **GET** /v1/events/paths | List the touch paths that lead to conversions |
| [**GetConversionsQuality**](ConversionsApi.md#getconversionsquality) | **GET** /v1/ads/conversions/quality | Get Event Match Quality |
| [**GetEvent**](ConversionsApi.md#getevent) | **GET** /v1/events/{eventId} | Get one stored event and its deliveries |
| [**GetEventsAccuracy**](ConversionsApi.md#geteventsaccuracy) | **GET** /v1/events/accuracy | Get delivery accuracy per destination |
| [**GetEventsOverview**](ConversionsApi.md#geteventsoverview) | **GET** /v1/events/overview | Get today&#39;s tracking overview |
| [**GetEventsOverviewDaily**](ConversionsApi.md#geteventsoverviewdaily) | **GET** /v1/events/overview/daily | Get daily tracking figures |
| [**GetLtvCohorts**](ConversionsApi.md#getltvcohorts) | **GET** /v1/events/ltv | Get buyer cohorts by first purchase month and first channel |
| [**GetSurveyAnswers**](ConversionsApi.md#getsurveyanswers) | **GET** /v1/events/survey | Get post-purchase survey answers |
| [**GetTrackingSite**](ConversionsApi.md#gettrackingsite) | **GET** /v1/tracking-sites/{siteId} | Get a tracking site |
| [**ListAdConversionAssociations**](ConversionsApi.md#listadconversionassociations) | **GET** /v1/ads/conversions/destinations/{destinationId}/associations | List associated campaigns |
| [**ListAdConversionDestinations**](ConversionsApi.md#listadconversiondestinations) | **GET** /v1/ads/conversions/destinations | List conversion destinations |
| [**ListAdConversionGoals**](ConversionsApi.md#listadconversiongoals) | **GET** /v1/ads/conversions/goals | List account conversion goals |
| [**ListAdCustomConversions**](ConversionsApi.md#listadcustomconversions) | **GET** /v1/ads/conversions/custom-conversions | List custom conversions |
| [**ListConversionActions**](ConversionsApi.md#listconversionactions) | **GET** /v1/ads/conversions/actions | List conversion actions |
| [**ListConversionAssociations**](ConversionsApi.md#listconversionassociations) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | List associated campaigns |
| [**ListConversionDestinations**](ConversionsApi.md#listconversiondestinations) | **GET** /v1/accounts/{accountId}/conversion-destinations | List conversion destinations |
| [**ListCustomConversionGoals**](ConversionsApi.md#listcustomconversiongoals) | **GET** /v1/ads/conversions/custom-goals | List custom conversion goals |
| [**ListEventDestinations**](ConversionsApi.md#listeventdestinations) | **GET** /v1/events/destinations | List event destinations |
| [**ListEventNames**](ConversionsApi.md#listeventnames) | **GET** /v1/events/names | List stored event names |
| [**ListEvents**](ConversionsApi.md#listevents) | **GET** /v1/events | List stored events |
| [**ListForwardingRules**](ConversionsApi.md#listforwardingrules) | **GET** /v1/events/forwarding-rules | List forwarding rules |
| [**ListTrackingSites**](ConversionsApi.md#listtrackingsites) | **GET** /v1/tracking-sites | List tracking sites |
| [**RemoveAdConversionAssociations**](ConversionsApi.md#removeadconversionassociations) | **DELETE** /v1/ads/conversions/destinations/{destinationId}/associations | Remove associated campaigns |
| [**RemoveConversionAssociations**](ConversionsApi.md#removeconversionassociations) | **DELETE** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | Remove associated campaigns |
| [**RemoveCustomConversionGoal**](ConversionsApi.md#removecustomconversiongoal) | **DELETE** /v1/ads/conversions/custom-goals/{goalId} | Remove a custom conversion goal |
| [**RestateEvent**](ConversionsApi.md#restateevent) | **PATCH** /v1/events/{eventId} | Change a stored event&#39;s value |
| [**RetractEvent**](ConversionsApi.md#retractevent) | **DELETE** /v1/events/{eventId} | Retract a stored event |
| [**RotateTrackingSiteKey**](ConversionsApi.md#rotatetrackingsitekey) | **POST** /v1/tracking-sites/{siteId}/rotate-key | Rotate a tracking site&#39;s key |
| [**SendConversions**](ConversionsApi.md#sendconversions) | **POST** /v1/ads/conversions | Send conversion events to one destination (legacy) |
| [**SendEvents**](ConversionsApi.md#sendevents) | **POST** /v1/events | Send events to every destination |
| [**UpdateAdConversionDestination**](ConversionsApi.md#updateadconversiondestination) | **PATCH** /v1/ads/conversions/destinations/{destinationId} | Update a conversion destination |
| [**UpdateAdConversionGoals**](ConversionsApi.md#updateadconversiongoals) | **PATCH** /v1/ads/conversions/goals | Update account conversion goals |
| [**UpdateConversionAction**](ConversionsApi.md#updateconversionaction) | **PATCH** /v1/ads/conversions/actions/{actionId} | Update a conversion action&#39;s settings |
| [**UpdateConversionDestination**](ConversionsApi.md#updateconversiondestination) | **PATCH** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Update a conversion destination |
| [**UpdateCustomConversionGoal**](ConversionsApi.md#updatecustomconversiongoal) | **PATCH** /v1/ads/conversions/custom-goals/{goalId} | Update a custom conversion goal |
| [**UpdateForwardingRule**](ConversionsApi.md#updateforwardingrule) | **PATCH** /v1/events/forwarding-rules/{ruleId} | Update a forwarding rule |
| [**UpdateTrackingSite**](ConversionsApi.md#updatetrackingsite) | **PATCH** /v1/tracking-sites/{siteId} | Update a tracking site |

<a id="addadconversionassociations"></a>
# **AddAdConversionAssociations**
> AddAdConversionAssociations200Response AddAdConversionAssociations (string destinationId, AddAdConversionAssociationsRequest addAdConversionAssociationsRequest)

Associate campaigns

Links campaigns to a LinkedIn conversion rule so they track it, reporting which links succeeded or failed.  Returns a per-campaign success/failure result so callers can retry only the rows that failed (e.g. wrong campaign type for the rule's objective). 

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
    public class AddAdConversionAssociationsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var destinationId = "destinationId_example";  // string | 
            var addAdConversionAssociationsRequest = new AddAdConversionAssociationsRequest(); // AddAdConversionAssociationsRequest | 

            try
            {
                // Associate campaigns
                AddAdConversionAssociations200Response result = apiInstance.AddAdConversionAssociations(destinationId, addAdConversionAssociationsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.AddAdConversionAssociations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddAdConversionAssociationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Associate campaigns
    ApiResponse<AddAdConversionAssociations200Response> response = apiInstance.AddAdConversionAssociationsWithHttpInfo(destinationId, addAdConversionAssociationsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.AddAdConversionAssociationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **destinationId** | **string** |  |  |
| **addAdConversionAssociationsRequest** | [**AddAdConversionAssociationsRequest**](AddAdConversionAssociationsRequest.md) |  |  |

### Return type

[**AddAdConversionAssociations200Response**](AddAdConversionAssociations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Per-campaign batch result. Status is 200 even when some rows failed. Inspect &#x60;failed[]&#x60; for details. Inputs that fail local URN validation are bucketed into &#x60;failed&#x60; without ever hitting LinkedIn.  |  -  |
| **400** | Invalid body. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads add-on or LinkedIn reconnect required.  Also returned with code &#x60;ad_account_not_selected&#x60; when the connection has selected ad accounts and the targeted ad account is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection) or use a connection that has it selected. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support associations. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="addconversionassociations"></a>
# **AddConversionAssociations**
> AddAdConversionAssociations200Response AddConversionAssociations (string accountId, string destinationId, AddConversionAssociationsRequest addConversionAssociationsRequest)

Associate campaigns

The first path of `POST /v1/ads/conversions/destinations/{destinationId}/associations` (`addAdConversionAssociations`), which does the same with `accountId` as a parameter. It keeps working. 

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
    public class AddConversionAssociationsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var addConversionAssociationsRequest = new AddConversionAssociationsRequest(); // AddConversionAssociationsRequest | 

            try
            {
                // Associate campaigns
                AddAdConversionAssociations200Response result = apiInstance.AddConversionAssociations(accountId, destinationId, addConversionAssociationsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.AddConversionAssociations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddConversionAssociationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Associate campaigns
    ApiResponse<AddAdConversionAssociations200Response> response = apiInstance.AddConversionAssociationsWithHttpInfo(accountId, destinationId, addConversionAssociationsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.AddConversionAssociationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **addConversionAssociationsRequest** | [**AddConversionAssociationsRequest**](AddConversionAssociationsRequest.md) |  |  |

### Return type

[**AddAdConversionAssociations200Response**](AddAdConversionAssociations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Per-campaign batch result. Status is 200 even when some rows failed. Inspect &#x60;failed[]&#x60; for details. Inputs that fail local URN validation are bucketed into &#x60;failed&#x60; without ever hitting LinkedIn.  |  -  |
| **400** | Invalid body. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads add-on or LinkedIn reconnect required.  Also returned with code &#x60;ad_account_not_selected&#x60; when the connection has selected ad accounts and the targeted ad account is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection) or use a connection that has it selected. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support associations. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="adjustconversions"></a>
# **AdjustConversions**
> AdjustConversions200Response AdjustConversions (AdjustConversionsRequest adjustConversionsRequest)

Adjust uploaded conversions

Retracts, restates the value of, or enhances conversions you already sent to Google Ads, Impact or a Microsoft Ads offline conversion goal, for refunds or late customer data. To change Zernio's stored event too, and every platform at once, use `PATCH` or `DELETE /v1/events/{eventId}`.  It adjusts conversions previously uploaded via `POST /v1/ads/conversions`: retract them, restate their value, or enhance them with first-party data. Requires the Ads add-on.  ### Google Ads, Impact and Microsoft Ads only  Google handles adjustments through the classic Google Ads API (`ConversionAdjustmentUploadService`). The Data Manager `ingestEvents` path used for sending conversions is ingest-only.  On Impact, the partner's commission follows the refund:  - `RETRACTION` reverses the action and `RESTATEMENT` sets its sale amount. Impact has no `ENHANCEMENT`. - The action is found by the `destinationId` event type and `orderId`: the `platformData.order_id` the conversion was sent with, or its `eventId` when it had none. - Impact applies changes asynchronously and refuses them on its side past the action's locking date.  On Microsoft Ads (`ApplyOfflineConversionAdjustments`), only offline conversion goals take changes; a UET tag refuses them:  - `RETRACTION` retracts the conversion and `RESTATEMENT` sets its new value. Microsoft has no `ENHANCEMENT`. - Microsoft has no order id: send `msclkid` and `conversionTime`, the click id and time the conversion was sent with.  Other platforms have no equivalent, so this endpoint returns `405` for them.  ### Adjustment types  - `RETRACTION`: remove the conversion entirely (refund, chargeback, cancelled order, churn). - `RESTATEMENT`: change the conversion's value (upgrade / downgrade / partial refund). Send the corrected **total** value in `restatementValue` (not a delta). - `ENHANCEMENT`: attach first-party identifiers (hashed email / phone) to an existing conversion (enhanced conversions applied after the fact).  ### Identifying the original conversion  Per adjustment, send one of:  - `orderId`: the transaction ID you sent as `eventId` on the original conversion. Recommended, and **required** for `ENHANCEMENT`. - `gclid` + `conversionTime`: the click ID and the original conversion's time (unix seconds). Not available for `ENHANCEMENT`. - `msclkid` + `conversionTime`: the only key on Microsoft Ads.  ### Other fields  - `destinationId` is the same value you send to `POST /v1/ads/conversions`: the conversion action resource name on Google, e.g. `customers/1234567890/conversionActions/987654321`, `<program id>:<event type id>` on Impact, and `accounts/{adAccountId}/conversionGoals/{goalId}` on Microsoft Ads. - PII in `user` is hashed with SHA-256 server-side (Gmail-specific normalization included). Send plaintext. - Times are unix seconds; we convert to Google's required `yyyy-MM-dd HH:mm:ss+00:00` format.  ### Limits  Up to 2000 adjustments per request. Partial failure is supported (inspect `adjustmentsFailed` / `failures[]`). 

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
    public class AdjustConversionsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var adjustConversionsRequest = new AdjustConversionsRequest(); // AdjustConversionsRequest | 

            try
            {
                // Adjust uploaded conversions
                AdjustConversions200Response result = apiInstance.AdjustConversions(adjustConversionsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.AdjustConversions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AdjustConversionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Adjust uploaded conversions
    ApiResponse<AdjustConversions200Response> response = apiInstance.AdjustConversionsWithHttpInfo(adjustConversionsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.AdjustConversionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adjustConversionsRequest** | [**AdjustConversionsRequest**](AdjustConversionsRequest.md) |  |  |

### Return type

[**AdjustConversions200Response**](AdjustConversions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Adjustments processed. Inspect &#x60;adjustmentsFailed&#x60; and &#x60;failures[]&#x60; for partial failure (Google reports per-row errors via partial failure).  |  -  |
| **400** | Invalid body, or a malformed adjustment (missing key, missing restatementValue for RESTATEMENT, missing identifiers for ENHANCEMENT), or (param &#x60;destinationId&#x60;) the customer named in &#x60;destinationId&#x60; is not one of this connection&#39;s Google Ads accounts. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans).  Or, for Google Ads, code &#x60;ad_account_not_selected&#x60;: the connection has selected ad accounts and the Google Ads customer named in &#x60;destinationId&#x60; is not among them (param &#x60;destinationId&#x60;; &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;).  Fix: add the customer to the selection (GET /v1/connect/googleads/ads with adAccountIds, which replaces the selection), or use a connection that has it selected.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Conversion adjustments are only available for Google Ads (the account&#39;s platform is not &#x60;googleads&#x60;). |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | Google Ads errors:  - &#x60;ads_connection_required&#x60;: no Google Ads customer account is left on this connection after its ad-account selection. Reconnect via GET /v1/connect/googleads/ads with a Google user that can reach the ad account, or select one of its ad accounts. - &#x60;invalid_resource_state&#x60;: the connection reaches only a Google Ads manager account with no client accounts yet. Create one with POST /v1/ads/accounts or under the manager in Google Ads, then retry.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="checktrackingsiteproxy"></a>
# **CheckTrackingSiteProxy**
> CreateTrackingSite201Response CheckTrackingSiteProxy (string siteId)

Check a tracking site's own-domain path

Loads `https://<first domain><proxyPath>/z.js` from Zernio's servers and records whether your proxy serves the tag, signed, in `proxy.status`. Once `verified`, cookies come from your own domain and Safari keeps them; a connected Tag Manager container moves to the path. Also runs after `proxyPath` changes.

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
    public class CheckTrackingSiteProxyExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var siteId = "siteId_example";  // string | 

            try
            {
                // Check a tracking site's own-domain path
                CreateTrackingSite201Response result = apiInstance.CheckTrackingSiteProxy(siteId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.CheckTrackingSiteProxy: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckTrackingSiteProxyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check a tracking site's own-domain path
    ApiResponse<CreateTrackingSite201Response> response = apiInstance.CheckTrackingSiteProxyWithHttpInfo(siteId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.CheckTrackingSiteProxyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **siteId** | **string** |  |  |

### Return type

[**CreateTrackingSite201Response**](CreateTrackingSite201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The site with &#x60;proxy.status&#x60; updated. &#x60;proxy&#x60; is null when the site has no &#x60;proxyPath&#x60;. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createadconversiondestination"></a>
# **CreateAdConversionDestination**
> CreateAdConversionDestination201Response CreateAdConversionDestination (CreateAdConversionDestinationRequest createAdConversionDestinationRequest)

Create a conversion destination

Creates a new place to send conversion events: a Google Ads conversion action or a LinkedIn conversion rule.  Supported for LinkedIn (conversion rule) and Google Ads (conversion action). It returns 405 for:  - Meta and OpenAI Ads: their pixels are created via their own tracking-tags flow instead (`POST /v1/accounts/{accountId}/tracking-tags`) - Reddit: create Reddit pixels in Reddit Ads Manager  ### LinkedIn  Creation is NOT idempotent. A retry creates a second destination. Deduplicate before retrying.  The rule is created with `conversionMethod=CONVERSIONS_API` and (by default) auto-associated with all of the ad account's campaigns via `autoAssociationType=ALL_CAMPAIGNS`. Pass `autoAssociationType: NONE` to opt out and manage associations explicitly via the associations endpoints below.  365-day attribution windows are only valid for these rule types; the API rejects other combinations locally:  - `SUBMIT_APPLICATION` - `PURCHASE` - `ADD_TO_CART` - `QUALIFIED_LEAD` - `LEAD`  ### Google Ads  Calling with a name that already exists reuses the existing conversion action transparently (the response is identical to a fresh create).  Calling with the same name but a different category, or a name already used by a website (`WEBPAGE`) action, returns a typed `IDEMPOTENCY_CONFLICT` (409) rather than silently returning the mismatched action.  The conversion action is created with `type=UPLOAD_CLICKS` (required for API-uploaded offline conversions, immutable after creation).  The `type` field carries the Google `ConversionActionCategory` enum value, e.g. `PURCHASE`, `SUBSCRIBE_PAID`, `SIGNUP`, `IMPORTED_LEAD`, `BOOK_APPOINTMENT`. Unified standard event names (e.g. `Purchase`, `Subscribe`, `CompleteRegistration`, `Lead`, `Schedule`) are resolved to their Google category equivalents automatically.  The action defaults to secondary (non-primary) to avoid immediately steering Smart Bidding; pass `primaryForGoal: true` to opt in. 

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
    public class CreateAdConversionDestinationExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var createAdConversionDestinationRequest = new CreateAdConversionDestinationRequest(); // CreateAdConversionDestinationRequest | 

            try
            {
                // Create a conversion destination
                CreateAdConversionDestination201Response result = apiInstance.CreateAdConversionDestination(createAdConversionDestinationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.CreateAdConversionDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdConversionDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a conversion destination
    ApiResponse<CreateAdConversionDestination201Response> response = apiInstance.CreateAdConversionDestinationWithHttpInfo(createAdConversionDestinationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.CreateAdConversionDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createAdConversionDestinationRequest** | [**CreateAdConversionDestinationRequest**](CreateAdConversionDestinationRequest.md) |  |  |

### Return type

[**CreateAdConversionDestination201Response**](CreateAdConversionDestination201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Destination created |  -  |
| **400** | Invalid body or platform validation failure. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the connected LinkedIn account lacks the &#x60;rw_conversions&#x60; scope (reconnect required).  Also returned with code &#x60;ad_account_not_selected&#x60; when the connection has selected ad accounts and the targeted ad account is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection) or use a connection that has it selected.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support destination creation. |  -  |
| **409** | Conflict. One of:  - &#x60;IDEMPOTENCY_CONFLICT&#x60; (Google Ads only): a conversion action with the given name already exists but has a different category. Use a different name or the existing destination. - ads_connection_required: the account is inactive or needs reconnection. Reconnect it and read GET /v1/accounts for its current ID before retrying.  |  -  |
| **422** | Google Ads connection not usable.  - Code &#x60;ads_connection_required&#x60;: no Google Ads customer account is left on this connection after its ad-account selection. Reconnect via GET /v1/connect/googleads/ads with a Google user that can reach the ad account, or select one of its ad accounts. - Code &#x60;invalid_resource_state&#x60;: the connection reaches only a Google Ads manager account with no client accounts yet. Create one with POST /v1/ads/accounts or under the manager in Google Ads, then retry.  |  -  |
| **429** | Rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createadcustomconversion"></a>
# **CreateAdCustomConversion**
> CustomConversionResult CreateAdCustomConversion (CreateAdCustomConversionRequest createAdCustomConversionRequest)

Create custom conversion

Creates a Meta custom conversion for ads to optimise toward, reusing an existing one with the same name and pixel.  It provisions the Meta custom conversion an ads flow optimises toward, and hands back the `customConversionId` for `promotedObject.customConversionId` on POST /v1/ads/create. This removes the manual \"create it in Ads Manager first\" step.  ### Reuse is ours, not Meta's  Meta's create is not idempotent, so a retried request would otherwise mint a duplicate carrying none of the original's optimisation history.  A non-archived conversion with the same `name` on the same `pixelId` is returned instead of created, with `reused: true` and a 200 rather than a 201.  ### Rule  `rule` is forwarded verbatim in Meta's own grammar (e.g. `{\"url\": {\"i_contains\": \"thank-you\"}}`). Meta validates it and rejects a malformed one with \"A conversion rule is required at creation time\". 

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
    public class CreateAdCustomConversionExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var createAdCustomConversionRequest = new CreateAdCustomConversionRequest(); // CreateAdCustomConversionRequest | 

            try
            {
                // Create custom conversion
                CustomConversionResult result = apiInstance.CreateAdCustomConversion(createAdCustomConversionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.CreateAdCustomConversion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdCustomConversionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create custom conversion
    ApiResponse<CustomConversionResult> response = apiInstance.CreateAdCustomConversionWithHttpInfo(createAdCustomConversionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.CreateAdCustomConversionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createAdCustomConversionRequest** | [**CreateAdCustomConversionRequest**](CreateAdCustomConversionRequest.md) |  |  |

### Return type

[**CustomConversionResult**](CustomConversionResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | An existing custom conversion was reused |  -  |
| **201** | Custom conversion created |  -  |
| **400** | Invalid input, or Meta rejected the conversion (bad rule, per-account cap reached) |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required, or the token lacks the ads permissions.  Also returned with code &#x60;ad_account_not_selected&#x60; when the connection has selected ad accounts and the ad account this request targets is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  To fix it, add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection) or use a connection that has it selected. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createconversionaction"></a>
# **CreateConversionAction**
> CreateConversionAction201Response CreateConversionAction (CreateConversionActionRequest createConversionActionRequest)

Create conversion action

Creates a Google Ads conversion action: a website one counted by a tag on your site, or one counted from the conversions you send to Zernio.  - `type: WEBPAGE` creates a website action and returns it with the tag snippets to install, read back after creation since Google never returns them on the create response itself. - `type: UPLOAD_CLICKS` creates an action for the conversions sent with `POST /v1/events`, the same action `POST /v1/ads/conversions/destinations` creates. It is secondary unless `primaryForGoal: true`.  The category defaults to `DEFAULT`. A name already used by another action returns Google's error.  Clears the cached list that `GET` on this resource would otherwise keep serving. Google-only; other platforms return `501`. Requires the Ads add-on. 

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
    public class CreateConversionActionExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var createConversionActionRequest = new CreateConversionActionRequest(); // CreateConversionActionRequest | 

            try
            {
                // Create conversion action
                CreateConversionAction201Response result = apiInstance.CreateConversionAction(createConversionActionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.CreateConversionAction: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateConversionActionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create conversion action
    ApiResponse<CreateConversionAction201Response> response = apiInstance.CreateConversionActionWithHttpInfo(createConversionActionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.CreateConversionActionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createConversionActionRequest** | [**CreateConversionActionRequest**](CreateConversionActionRequest.md) |  |  |

### Return type

[**CreateConversionAction201Response**](CreateConversionAction201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The created conversion action, with its tag snippets. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans).  Also returned with code &#x60;ad_account_not_selected&#x60; when the connection has selected ad accounts and the targeted ad account is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection) or use a connection that has it selected.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | Google Ads.  - &#x60;ads_connection_required&#x60;: no Google Ads customer account is left on this connection after its ad-account selection. Reconnect via GET /v1/connect/googleads/ads with a Google user that can reach the ad account, or select one of its ad accounts. - &#x60;invalid_resource_state&#x60;: the connection reaches only a Google Ads manager account with no client accounts yet. Create one with POST /v1/ads/accounts or under the manager in Google Ads, then retry.  |  -  |
| **501** | Conversion actions are only available for Google Ads (the account&#39;s platform is not &#x60;googleads&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createconversiondestination"></a>
# **CreateConversionDestination**
> CreateAdConversionDestination201Response CreateConversionDestination (string accountId, CreateConversionDestinationRequest createConversionDestinationRequest)

Create a conversion destination

The first path of `POST /v1/ads/conversions/destinations` (`createAdConversionDestination`), which does the same with `accountId` as a parameter. It keeps working. 

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
    public class CreateConversionDestinationExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | SocialAccount ID (linkedinads or googleads).
            var createConversionDestinationRequest = new CreateConversionDestinationRequest(); // CreateConversionDestinationRequest | 

            try
            {
                // Create a conversion destination
                CreateAdConversionDestination201Response result = apiInstance.CreateConversionDestination(accountId, createConversionDestinationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.CreateConversionDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateConversionDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a conversion destination
    ApiResponse<CreateAdConversionDestination201Response> response = apiInstance.CreateConversionDestinationWithHttpInfo(accountId, createConversionDestinationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.CreateConversionDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | SocialAccount ID (linkedinads or googleads). |  |
| **createConversionDestinationRequest** | [**CreateConversionDestinationRequest**](CreateConversionDestinationRequest.md) |  |  |

### Return type

[**CreateAdConversionDestination201Response**](CreateAdConversionDestination201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Destination created |  -  |
| **400** | Invalid body or platform validation failure. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the connected LinkedIn account lacks the &#x60;rw_conversions&#x60; scope (reconnect required).  Also returned with code &#x60;ad_account_not_selected&#x60; when the connection has selected ad accounts and the targeted ad account is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection) or use a connection that has it selected.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support destination creation. |  -  |
| **409** | Conflict. One of:  - &#x60;IDEMPOTENCY_CONFLICT&#x60; (Google Ads only): a conversion action with the given name already exists but has a different category. Use a different name or the existing destination. - ads_connection_required: the account is inactive or needs reconnection. Reconnect it and read GET /v1/accounts for its current ID before retrying.  |  -  |
| **422** | Google Ads connection not usable.  - Code &#x60;ads_connection_required&#x60;: no Google Ads customer account is left on this connection after its ad-account selection. Reconnect via GET /v1/connect/googleads/ads with a Google user that can reach the ad account, or select one of its ad accounts. - Code &#x60;invalid_resource_state&#x60;: the connection reaches only a Google Ads manager account with no client accounts yet. Create one with POST /v1/ads/accounts or under the manager in Google Ads, then retry.  |  -  |
| **429** | Rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcustomconversiongoal"></a>
# **CreateCustomConversionGoal**
> CreateSharedBudget201ResponseBudget CreateCustomConversionGoal (CreateCustomConversionGoalRequest createCustomConversionGoalRequest)

Create a custom conversion goal

Creates a Google Ads custom conversion goal from a set of conversion actions, so a campaign can bid on just those.  Creates a custom conversion goal from conversion action ids. Point a campaign at it with `PATCH /v1/ads/campaigns/{campaignId}/conversion-goals`. 

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
    public class CreateCustomConversionGoalExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var createCustomConversionGoalRequest = new CreateCustomConversionGoalRequest(); // CreateCustomConversionGoalRequest | 

            try
            {
                // Create a custom conversion goal
                CreateSharedBudget201ResponseBudget result = apiInstance.CreateCustomConversionGoal(createCustomConversionGoalRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.CreateCustomConversionGoal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCustomConversionGoalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a custom conversion goal
    ApiResponse<CreateSharedBudget201ResponseBudget> response = apiInstance.CreateCustomConversionGoalWithHttpInfo(createCustomConversionGoalRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.CreateCustomConversionGoalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCustomConversionGoalRequest** | [**CreateCustomConversionGoalRequest**](CreateCustomConversionGoalRequest.md) |  |  |

### Return type

[**CreateSharedBudget201ResponseBudget**](CreateSharedBudget201ResponseBudget.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Custom goal created |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;ad_account_not_selected&#x60;. The connection has selected ad accounts (its ad-account scope, set with the dashboard picker or GET /v1/connect/{platform}/ads with adAccountIds) and the targeted ad account is not among them. The connection may not act on it, even though its token can reach it.  &#x60;details&#x60; carries &#x60;accountId&#x60; (the connection), &#x60;adAccountId&#x60; (the refused ad account) and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (adAccountIds replaces the whole selection, so pass the ids already selected plus this one) or use a connection that has it selected. Connections without a selection keep reaching every ad account their token can manage.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | Only available on Google Ads accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createeventdestination"></a>
# **CreateEventDestination**
> CreateEventDestination201Response CreateEventDestination (CreateEventDestinationRequest createEventDestinationRequest)

Add an event destination

The first name of `POST /v1/events/forwarding-rules`, which saves the same rule. It keeps working and answers under `destination`.

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
    public class CreateEventDestinationExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var createEventDestinationRequest = new CreateEventDestinationRequest(); // CreateEventDestinationRequest | 

            try
            {
                // Add an event destination
                CreateEventDestination201Response result = apiInstance.CreateEventDestination(createEventDestinationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.CreateEventDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateEventDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add an event destination
    ApiResponse<CreateEventDestination201Response> response = apiInstance.CreateEventDestinationWithHttpInfo(createEventDestinationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.CreateEventDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createEventDestinationRequest** | [**CreateEventDestinationRequest**](CreateEventDestinationRequest.md) |  |  |

### Return type

[**CreateEventDestination201Response**](CreateEventDestination201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Destination saved. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **409** | The profile already sends events to this destination (code &#x60;invalid_resource_state&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createforwardingrule"></a>
# **CreateForwardingRule**
> CreateForwardingRule201Response CreateForwardingRule (CreateForwardingRuleRequest createForwardingRuleRequest)

Add a forwarding rule

Saves where a profile's events go: every event sent to `POST /v1/events` for that profile is then forwarded to this destination.  Pick `destinationId` from `GET /v1/ads/conversions/destinations`. Set `eventNames` to forward only those events, such as only `Purchase`; leave it out to forward every event.  - `eventNameMap` renames events for this destination (send your `Lead` as its `Purchase`). - `valueOverride` changes the value it gets (a fixed amount or a percent of the event's value). - `valueCondition` forwards only events above, below or equal to a value. - `eventValues` sets the value of each event name (a `Lead` worth 20 EUR, a `QualifiedLead` worth 150 EUR) and wins over `valueOverride` for the names it lists.  Each applies to this rule only: the event is stored, and sent to other rules, as received. 

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
    public class CreateForwardingRuleExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var createForwardingRuleRequest = new CreateForwardingRuleRequest(); // CreateForwardingRuleRequest | 

            try
            {
                // Add a forwarding rule
                CreateForwardingRule201Response result = apiInstance.CreateForwardingRule(createForwardingRuleRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.CreateForwardingRule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateForwardingRuleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add a forwarding rule
    ApiResponse<CreateForwardingRule201Response> response = apiInstance.CreateForwardingRuleWithHttpInfo(createForwardingRuleRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.CreateForwardingRuleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createForwardingRuleRequest** | [**CreateForwardingRuleRequest**](CreateForwardingRuleRequest.md) |  |  |

### Return type

[**CreateForwardingRule201Response**](CreateForwardingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Rule saved. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **409** | The profile already forwards events to this destination (code &#x60;invalid_resource_state&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createtrackingsite"></a>
# **CreateTrackingSite**
> CreateTrackingSite201Response CreateTrackingSite (string idempotencyKey, CreateTrackingSiteRequest createTrackingSiteRequest)

Turn on server-side tracking for a website

Creates a tracking site. With `storeAccountId`, Zernio installs its tag on the connected Shopify, WordPress (WooCommerce), Wix or Webflow store. With only `url`, paste the returned `install.snippet` into the site. Adding a `url` the profile already tracks returns that site and its snippet instead of creating a second one.  The ad accounts you picked for each connection get a forwarding rule, so website conversions reach them at once. `checks` shows each step; `setup.status` turns `ready` when all have passed. 

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
    public class CreateTrackingSiteExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var idempotencyKey = "idempotencyKey_example";  // string | A unique key per site you create, such as a UUID. A retry with the same key and body returns the same site.
            var createTrackingSiteRequest = new CreateTrackingSiteRequest(); // CreateTrackingSiteRequest | 

            try
            {
                // Turn on server-side tracking for a website
                CreateTrackingSite201Response result = apiInstance.CreateTrackingSite(idempotencyKey, createTrackingSiteRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.CreateTrackingSite: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTrackingSiteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Turn on server-side tracking for a website
    ApiResponse<CreateTrackingSite201Response> response = apiInstance.CreateTrackingSiteWithHttpInfo(idempotencyKey, createTrackingSiteRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.CreateTrackingSiteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **idempotencyKey** | **string** | A unique key per site you create, such as a UUID. A retry with the same key and body returns the same site. |  |
| **createTrackingSiteRequest** | [**CreateTrackingSiteRequest**](CreateTrackingSiteRequest.md) |  |  |

### Return type

[**CreateTrackingSite201Response**](CreateTrackingSite201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Site created. |  -  |
| **400** | Invalid body, an unsupported store (code &#x60;store_not_supported&#x60;) or a store with no known address (code &#x60;store_url_unknown&#x60;). |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **409** | The store already has a site (code &#x60;store_already_tracked&#x60;, with &#x60;details.siteId&#x60;) or is disconnected (code &#x60;reconnect_required&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteadconversiondestination"></a>
# **DeleteAdConversionDestination**
> void DeleteAdConversionDestination (string accountId, string destinationId, string? adAccountId = null)

Delete a conversion destination

Disables a LinkedIn conversion rule, which is how LinkedIn deletes it; the rule can still be read afterwards.  LinkedIn-only today. LinkedIn does not expose hard-delete on conversion rules; what their UI calls \"delete\" is the same `enabled: false` flip we apply here. The rule remains fetchable via GET with `status: 'inactive'`; the unified discovery endpoint hides it by default.  `adAccountId` may be passed as a query parameter (recommended) or as a JSON body field for clients that can send DELETE bodies. 

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
    public class DeleteAdConversionDestinationExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected ads account (SocialAccount ID).
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string? | Required as query OR in JSON body. (optional) 

            try
            {
                // Delete a conversion destination
                apiInstance.DeleteAdConversionDestination(accountId, destinationId, adAccountId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.DeleteAdConversionDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAdConversionDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a conversion destination
    apiInstance.DeleteAdConversionDestinationWithHttpInfo(accountId, destinationId, adAccountId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.DeleteAdConversionDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected ads account (SocialAccount ID). |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string?** | Required as query OR in JSON body. | [optional]  |

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
| **204** | Soft-deleted. |  -  |
| **400** | adAccountId missing, or accountId is not a valid id. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads add-on or LinkedIn reconnect required.  Also returned with code &#x60;ad_account_not_selected&#x60; when the connection has selected ad accounts and the ad account this request targets is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  To fix it, add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection) or use a connection that has it selected. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support deleting destinations. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteconversiondestination"></a>
# **DeleteConversionDestination**
> void DeleteConversionDestination (string accountId, string destinationId, string? adAccountId = null)

Delete a conversion destination

The first path of `DELETE /v1/ads/conversions/destinations/{destinationId}` (`deleteAdConversionDestination`), which does the same with `accountId` as a parameter. It keeps working. 

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
    public class DeleteConversionDestinationExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string? | Required as query OR in JSON body. (optional) 

            try
            {
                // Delete a conversion destination
                apiInstance.DeleteConversionDestination(accountId, destinationId, adAccountId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.DeleteConversionDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteConversionDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a conversion destination
    apiInstance.DeleteConversionDestinationWithHttpInfo(accountId, destinationId, adAccountId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.DeleteConversionDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string?** | Required as query OR in JSON body. | [optional]  |

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
| **204** | Soft-deleted. |  -  |
| **400** | adAccountId missing, or accountId is not a valid id. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads add-on or LinkedIn reconnect required.  Also returned with code &#x60;ad_account_not_selected&#x60; when the connection has selected ad accounts and the ad account this request targets is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  To fix it, add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection) or use a connection that has it selected. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support deleting destinations. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteeventdestination"></a>
# **DeleteEventDestination**
> DeleteSmsSenderId200Response DeleteEventDestination (string destinationId)

Remove an event destination

The first name of `DELETE /v1/events/forwarding-rules/{ruleId}`. `destinationId` here is the rule `id`, not the platform destination.

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
    public class DeleteEventDestinationExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var destinationId = "destinationId_example";  // string | 

            try
            {
                // Remove an event destination
                DeleteSmsSenderId200Response result = apiInstance.DeleteEventDestination(destinationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.DeleteEventDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteEventDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove an event destination
    ApiResponse<DeleteSmsSenderId200Response> response = apiInstance.DeleteEventDestinationWithHttpInfo(destinationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.DeleteEventDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **destinationId** | **string** |  |  |

### Return type

[**DeleteSmsSenderId200Response**](DeleteSmsSenderId200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Destination removed. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteforwardingrule"></a>
# **DeleteForwardingRule**
> DeleteSmsSenderId200Response DeleteForwardingRule (string ruleId)

Remove a forwarding rule

Stops forwarding events to this rule's destination. Events already sent are not affected.

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
    public class DeleteForwardingRuleExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var ruleId = "ruleId_example";  // string | The rule `id`.

            try
            {
                // Remove a forwarding rule
                DeleteSmsSenderId200Response result = apiInstance.DeleteForwardingRule(ruleId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.DeleteForwardingRule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteForwardingRuleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove a forwarding rule
    ApiResponse<DeleteSmsSenderId200Response> response = apiInstance.DeleteForwardingRuleWithHttpInfo(ruleId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.DeleteForwardingRuleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ruleId** | **string** | The rule &#x60;id&#x60;. |  |

### Return type

[**DeleteSmsSenderId200Response**](DeleteSmsSenderId200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rule removed. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletetrackingsite"></a>
# **DeleteTrackingSite**
> void DeleteTrackingSite (string siteId)

Delete a tracking site

Stops collecting at once, removes the tag from the connected store and releases the custom subdomain. Events already stored are kept.

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
    public class DeleteTrackingSiteExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var siteId = "siteId_example";  // string | 

            try
            {
                // Delete a tracking site
                apiInstance.DeleteTrackingSite(siteId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.DeleteTrackingSite: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTrackingSiteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a tracking site
    apiInstance.DeleteTrackingSiteWithHttpInfo(siteId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.DeleteTrackingSiteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **siteId** | **string** |  |  |

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
| **204** | Site deleted. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadconversiondestination"></a>
# **GetAdConversionDestination**
> GetAdConversionDestination200Response GetAdConversionDestination (string accountId, string destinationId, string adAccountId)

Get a conversion destination

Shows one LinkedIn conversion rule with its full settings.  LinkedIn-only today. Returns the full destination record for one conversion rule. The `adAccountId` query parameter is required because LinkedIn rules are scoped to a sponsored ad account. 

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
    public class GetAdConversionDestinationExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected ads account (SocialAccount ID).
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | Numeric ID or full `urn:li:sponsoredAccount:{id}` URN.

            try
            {
                // Get a conversion destination
                GetAdConversionDestination200Response result = apiInstance.GetAdConversionDestination(accountId, destinationId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.GetAdConversionDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdConversionDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a conversion destination
    ApiResponse<GetAdConversionDestination200Response> response = apiInstance.GetAdConversionDestinationWithHttpInfo(accountId, destinationId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.GetAdConversionDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected ads account (SocialAccount ID). |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string** | Numeric ID or full &#x60;urn:li:sponsoredAccount:{id}&#x60; URN. |  |

### Return type

[**GetAdConversionDestination200Response**](GetAdConversionDestination200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Destination fetched |  -  |
| **400** | Validation error. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads add-on or LinkedIn reconnect required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support fetching a single destination. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadconversionmetrics"></a>
# **GetAdConversionMetrics**
> GetAdConversionMetrics200Response GetAdConversionMetrics (string accountId, string destinationId, string adAccountId, string startDate, string? endDate = null, string? granularity = null)

Get attribution metrics

Shows the conversions an ad network credited to a destination over time, bucketed by date.  **LinkedIn** (a conversion rule): `externalWebsiteConversions`, `externalWebsitePostClickConversions`, `externalWebsitePostViewConversions`, `conversionValueInLocalCurrency`, `qualifiedLeads`, `costInLocalCurrency`.  **Google Ads** (a conversion action, `destinationId` as `customers/{customerId}/conversionActions/{id}` or the bare id; `adAccountId` is the customer id): `conversions`, `conversionsValue`, `allConversions`, `allConversionsValue`. Dates are in the Google Ads account's time zone, days with no conversions have no row, and month and year buckets are cut to the asked range.  Other platforms answer 405.  Date-range constraints on LinkedIn: - `granularity=DAILY` is retained for ~6 months only - `granularity=ALL` with a range > 6 months auto-rounds to month boundaries - `granularity=MONTHLY`/`YEARLY` retains 24 months  Throttle: LinkedIn caps adAnalytics at 45M metric values per 5-minute window across the calling token. Single-rule queries are well within that limit; surfaces as 429 if hit. 

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
    public class GetAdConversionMetricsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected ads account (SocialAccount ID).
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | 
            var startDate = "startDate_example";  // string | 
            var endDate = "endDate_example";  // string? |  (optional) 
            var granularity = "ALL";  // string? |  (optional)  (default to DAILY)

            try
            {
                // Get attribution metrics
                GetAdConversionMetrics200Response result = apiInstance.GetAdConversionMetrics(accountId, destinationId, adAccountId, startDate, endDate, granularity);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.GetAdConversionMetrics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdConversionMetricsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get attribution metrics
    ApiResponse<GetAdConversionMetrics200Response> response = apiInstance.GetAdConversionMetricsWithHttpInfo(accountId, destinationId, adAccountId, startDate, endDate, granularity);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.GetAdConversionMetricsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected ads account (SocialAccount ID). |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string** |  |  |
| **startDate** | **string** |  |  |
| **endDate** | **string?** |  | [optional]  |
| **granularity** | **string?** |  | [optional] [default to DAILY] |

### Return type

[**GetAdConversionMetrics200Response**](GetAdConversionMetrics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Metrics rows |  -  |
| **400** | Validation error or invalid date range. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads add-on or reconnect required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support metrics readback. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | Platform analytics rate limit hit. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getconversiondestination"></a>
# **GetConversionDestination**
> GetAdConversionDestination200Response GetConversionDestination (string accountId, string destinationId, string adAccountId)

Get a conversion destination

The first path of `GET /v1/ads/conversions/destinations/{destinationId}` (`getAdConversionDestination`), which does the same with `accountId` as a parameter. It keeps working. 

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
    public class GetConversionDestinationExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | Numeric ID or full `urn:li:sponsoredAccount:{id}` URN.

            try
            {
                // Get a conversion destination
                GetAdConversionDestination200Response result = apiInstance.GetConversionDestination(accountId, destinationId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.GetConversionDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetConversionDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a conversion destination
    ApiResponse<GetAdConversionDestination200Response> response = apiInstance.GetConversionDestinationWithHttpInfo(accountId, destinationId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.GetConversionDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string** | Numeric ID or full &#x60;urn:li:sponsoredAccount:{id}&#x60; URN. |  |

### Return type

[**GetAdConversionDestination200Response**](GetAdConversionDestination200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Destination fetched |  -  |
| **400** | Validation error. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads add-on or LinkedIn reconnect required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support fetching a single destination. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getconversionmetrics"></a>
# **GetConversionMetrics**
> GetAdConversionMetrics200Response GetConversionMetrics (string accountId, string destinationId, string adAccountId, string startDate, string? endDate = null, string? granularity = null)

Get attribution metrics

The first path of `GET /v1/ads/conversions/destinations/{destinationId}/metrics` (`getAdConversionMetrics`), which does the same with `accountId` as a parameter. It keeps working. 

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
    public class GetConversionMetricsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | 
            var startDate = "startDate_example";  // string | 
            var endDate = "endDate_example";  // string? |  (optional) 
            var granularity = "ALL";  // string? |  (optional)  (default to DAILY)

            try
            {
                // Get attribution metrics
                GetAdConversionMetrics200Response result = apiInstance.GetConversionMetrics(accountId, destinationId, adAccountId, startDate, endDate, granularity);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.GetConversionMetrics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetConversionMetricsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get attribution metrics
    ApiResponse<GetAdConversionMetrics200Response> response = apiInstance.GetConversionMetricsWithHttpInfo(accountId, destinationId, adAccountId, startDate, endDate, granularity);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.GetConversionMetricsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string** |  |  |
| **startDate** | **string** |  |  |
| **endDate** | **string?** |  | [optional]  |
| **granularity** | **string?** |  | [optional] [default to DAILY] |

### Return type

[**GetAdConversionMetrics200Response**](GetAdConversionMetrics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Metrics rows |  -  |
| **400** | Validation error or invalid date range. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads add-on or reconnect required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support metrics readback. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | Platform analytics rate limit hit. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getconversionpaths"></a>
# **GetConversionPaths**
> GetConversionPaths200Response GetConversionPaths (DateOnly fromDate, DateOnly toDate, string? profileId = null, int? limit = null)

List the touch paths that lead to conversions

The most frequent sequences of touches people made before a conversion (sale, lead or another counted event) whose time falls in the range: ad clicks, tagged visits, search, referrals and earlier lead forms, oldest first.  Only conversions with more than one touch have a path. Without `profileId` it covers every profile you can access. Requires the Ads add-on. 

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
    public class GetConversionPathsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly | 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly | Inclusive. At most 400 days after `fromDate`.
            var profileId = "profileId_example";  // string? | The profile to read. Omit for every profile you can access. (optional) 
            var limit = 10;  // int? |  (optional)  (default to 10)

            try
            {
                // List the touch paths that lead to conversions
                GetConversionPaths200Response result = apiInstance.GetConversionPaths(fromDate, toDate, profileId, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.GetConversionPaths: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetConversionPathsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List the touch paths that lead to conversions
    ApiResponse<GetConversionPaths200Response> response = apiInstance.GetConversionPathsWithHttpInfo(fromDate, toDate, profileId, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.GetConversionPathsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fromDate** | **DateOnly** |  |  |
| **toDate** | **DateOnly** | Inclusive. At most 400 days after &#x60;fromDate&#x60;. |  |
| **profileId** | **string?** | The profile to read. Omit for every profile you can access. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 10] |

### Return type

[**GetConversionPaths200Response**](GetConversionPaths200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The paths, most frequent first. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getconversionsquality"></a>
# **GetConversionsQuality**
> GetConversionsQuality200Response GetConversionsQuality (string accountId, string destinationId)

Get Event Match Quality

Shows how well your server-side conversion events match users, with event match quality and coverage for Meta or Pinterest.  Reads Meta Event Match Quality (EMQ) and pixel↔CAPI event coverage for a pixel/dataset, live from Meta's Dataset Quality API. Web events only (a Meta limitation). Other platforms return 405, except Pinterest. Requires the Ads add-on.  Pinterest (`pinterestads`): `destinationId` is the numeric ad account id. Rows come from Pinterest's Event Quality Score for Conversions API web events over the last 14 days, one per event name, with each identifier's coverage in `matchKeys` and `eventCoveragePercentage` set to the tag/API `event_id` overlap. No `compositeScore`. 

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
    public class GetConversionsQualityExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | SocialAccount _id (a metaads or pinterestads account).
            var destinationId = "destinationId_example";  // string | Meta pixel/dataset ID, or the numeric Pinterest ad account id.

            try
            {
                // Get Event Match Quality
                GetConversionsQuality200Response result = apiInstance.GetConversionsQuality(accountId, destinationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.GetConversionsQuality: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetConversionsQualityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Event Match Quality
    ApiResponse<GetConversionsQuality200Response> response = apiInstance.GetConversionsQualityWithHttpInfo(accountId, destinationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.GetConversionsQualityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | SocialAccount _id (a metaads or pinterestads account). |  |
| **destinationId** | **string** | Meta pixel/dataset ID, or the numeric Pinterest ad account id. |  |

### Return type

[**GetConversionsQuality200Response**](GetConversionsQuality200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Match-quality rows, one per event name. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not expose Event Match Quality (neither Meta nor Pinterest). |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getevent"></a>
# **GetEvent**
> GetEvent200Response GetEvent (string eventId, string profileId)

Get one stored event and its deliveries

Returns one stored event of a profile (the latest copy of it) and, for each destination it was forwarded to, the newest send: `sent`, `retrying` (failed for now and queued again) or `failed` (final). Requires the Ads add-on. 

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
    public class GetEventExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var eventId = "eventId_example";  // string | The `eventId` the event was sent with.
            var profileId = "profileId_example";  // string | Profile the event belongs to.

            try
            {
                // Get one stored event and its deliveries
                GetEvent200Response result = apiInstance.GetEvent(eventId, profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.GetEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get one stored event and its deliveries
    ApiResponse<GetEvent200Response> response = apiInstance.GetEventWithHttpInfo(eventId, profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.GetEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **eventId** | **string** | The &#x60;eventId&#x60; the event was sent with. |  |
| **profileId** | **string** | Profile the event belongs to. |  |

### Return type

[**GetEvent200Response**](GetEvent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The event and its deliveries. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="geteventsaccuracy"></a>
# **GetEventsAccuracy**
> GetEventsAccuracy200Response GetEventsAccuracy (string? profileId = null, string? period = null)

Get delivery accuracy per destination

For each forwarding rule of a profile: what its destination received over a period, and how many of the profile's real sales reached it.  `deliveries` counts every event sent to the destination in the period, whatever its source, by the latest outcome of each. `accuracy` compares only sales: Shopify and WooCommerce orders and Stripe payments, as Elevar's Channel Accuracy does. Sales a rule leaves out by choice do not count against it.  Without `profileId` it covers every profile you can access. Requires the Ads add-on. 

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
    public class GetEventsAccuracyExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? | The profile to read. Omit to cover every profile you can access. (optional) 
            var period = "today";  // string? | The window, ending now: `today` (since 00:00 UTC), or the last 7, 30 or 90 days. (optional)  (default to 7d)

            try
            {
                // Get delivery accuracy per destination
                GetEventsAccuracy200Response result = apiInstance.GetEventsAccuracy(profileId, period);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.GetEventsAccuracy: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEventsAccuracyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get delivery accuracy per destination
    ApiResponse<GetEventsAccuracy200Response> response = apiInstance.GetEventsAccuracyWithHttpInfo(profileId, period);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.GetEventsAccuracyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** | The profile to read. Omit to cover every profile you can access. | [optional]  |
| **period** | **string?** | The window, ending now: &#x60;today&#x60; (since 00:00 UTC), or the last 7, 30 or 90 days. | [optional] [default to 7d] |

### Return type

[**GetEventsAccuracy200Response**](GetEventsAccuracy200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One entry per forwarding rule. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | No ads access on the account (&#x60;ads_addon_required&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="geteventsoverview"></a>
# **GetEventsOverview**
> GetEventsOverview200Response GetEventsOverview (string? profileId = null)

Get today's tracking overview

How a profile's conversion tracking is doing today (UTC day): events stored, how many reached the ad platforms, each forwarding rule's destination, each event source and, when the profile has a tracking site, the site's funnel.  Without `profileId` it covers every profile you can access, summed across them. Requires the Ads add-on. 

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
    public class GetEventsOverviewExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? | The profile to read. Omit to cover every profile you can access, summed across them. (optional) 

            try
            {
                // Get today's tracking overview
                GetEventsOverview200Response result = apiInstance.GetEventsOverview(profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.GetEventsOverview: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEventsOverviewWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get today's tracking overview
    ApiResponse<GetEventsOverview200Response> response = apiInstance.GetEventsOverviewWithHttpInfo(profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.GetEventsOverviewWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** | The profile to read. Omit to cover every profile you can access, summed across them. | [optional]  |

### Return type

[**GetEventsOverview200Response**](GetEventsOverview200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The profile&#39;s tracking overview. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="geteventsoverviewdaily"></a>
# **GetEventsOverviewDaily**
> GetEventsOverviewDaily200Response GetEventsOverviewDaily (string? profileId = null, string? period = null, string? eventName = null, string? sources = null, string? platform = null)

Get daily tracking figures

The tracking figures of a period, day by day (UTC): events stored per event name, events sent to each ad platform and how many it accepted, the period's totals in the same shape as the overview's `today`, and how many website conversions each platform's browser pixel missed.  An event sent to a destination counts once, on the day of its first send, by its latest outcome. Without `profileId` it covers every profile you can access. `eventName`, `sources` and `platform` narrow every figure. Requires the Ads add-on. 

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
    public class GetEventsOverviewDailyExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? | The profile to read. Omit to cover every profile you can access, summed across them. (optional) 
            var period = "today";  // string? | The days to cover, each ending today (UTC): `today`, the last 7, 30 or 90 days. (optional)  (default to 7d)
            var eventName = "eventName_example";  // string? | Only events of this name, such as `Purchase`. (optional) 
            var sources = "sources_example";  // string? | Comma-separated sources (`web`, `shopify`, `stripe`, `api`...). Only events from them. (optional) 
            var platform = "platform_example";  // string? | Only sends to this platform (`metaads`, `googleads`...), and only the events sent to it. (optional) 

            try
            {
                // Get daily tracking figures
                GetEventsOverviewDaily200Response result = apiInstance.GetEventsOverviewDaily(profileId, period, eventName, sources, platform);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.GetEventsOverviewDaily: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEventsOverviewDailyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get daily tracking figures
    ApiResponse<GetEventsOverviewDaily200Response> response = apiInstance.GetEventsOverviewDailyWithHttpInfo(profileId, period, eventName, sources, platform);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.GetEventsOverviewDailyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** | The profile to read. Omit to cover every profile you can access, summed across them. | [optional]  |
| **period** | **string?** | The days to cover, each ending today (UTC): &#x60;today&#x60;, the last 7, 30 or 90 days. | [optional] [default to 7d] |
| **eventName** | **string?** | Only events of this name, such as &#x60;Purchase&#x60;. | [optional]  |
| **sources** | **string?** | Comma-separated sources (&#x60;web&#x60;, &#x60;shopify&#x60;, &#x60;stripe&#x60;, &#x60;api&#x60;...). Only events from them. | [optional]  |
| **platform** | **string?** | Only sends to this platform (&#x60;metaads&#x60;, &#x60;googleads&#x60;...), and only the events sent to it. | [optional]  |

### Return type

[**GetEventsOverviewDaily200Response**](GetEventsOverviewDaily200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The period&#39;s daily figures. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getltvcohorts"></a>
# **GetLtvCohorts**
> GetLtvCohorts200Response GetLtvCohorts (string fromMonth, string toMonth, string? profileId = null)

Get buyer cohorts by first purchase month and first channel

Buyers grouped by the month of their first purchase and the platform that first brought them, with their purchases added up over the year after (months 0, 1, 3, 6 and 12).  A buyer is a hashed email, else external id, else phone. The first channel is the first touch's platform, else the first purchase's own campaign, else `none`. Values stay in each purchase's currency, one row per currency. Requires the Ads add-on. 

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
    public class GetLtvCohortsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var fromMonth = 2026-01;  // string | 
            var toMonth = 2026-11;  // string | 
            var profileId = "profileId_example";  // string? | The profile to read. Omit for every profile you can access. (optional) 

            try
            {
                // Get buyer cohorts by first purchase month and first channel
                GetLtvCohorts200Response result = apiInstance.GetLtvCohorts(fromMonth, toMonth, profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.GetLtvCohorts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetLtvCohortsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get buyer cohorts by first purchase month and first channel
    ApiResponse<GetLtvCohorts200Response> response = apiInstance.GetLtvCohortsWithHttpInfo(fromMonth, toMonth, profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.GetLtvCohortsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fromMonth** | **string** |  |  |
| **toMonth** | **string** |  |  |
| **profileId** | **string?** | The profile to read. Omit for every profile you can access. | [optional]  |

### Return type

[**GetLtvCohorts200Response**](GetLtvCohorts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The cohorts, newest first. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getsurveyanswers"></a>
# **GetSurveyAnswers**
> GetSurveyAnswers200Response GetSurveyAnswers (DateOnly fromDate, DateOnly toDate, string? profileId = null)

Get post-purchase survey answers

How buyers said they heard about the store, from the \"How did you hear about us?\" block on the Shopify thank-you page. Each answer comes with its orders and their revenue.  Revenue is what the orders are worth now (refunds taken off), summed across currencies as sent. Without `profileId` it covers every profile you can access. Requires the Ads add-on. 

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
    public class GetSurveyAnswersExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly | First day an answer was given.
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly | Inclusive. At most 400 days after `fromDate`.
            var profileId = "profileId_example";  // string? | The profile to read. Omit for every profile you can access. (optional) 

            try
            {
                // Get post-purchase survey answers
                GetSurveyAnswers200Response result = apiInstance.GetSurveyAnswers(fromDate, toDate, profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.GetSurveyAnswers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSurveyAnswersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get post-purchase survey answers
    ApiResponse<GetSurveyAnswers200Response> response = apiInstance.GetSurveyAnswersWithHttpInfo(fromDate, toDate, profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.GetSurveyAnswersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fromDate** | **DateOnly** | First day an answer was given. |  |
| **toDate** | **DateOnly** | Inclusive. At most 400 days after &#x60;fromDate&#x60;. |  |
| **profileId** | **string?** | The profile to read. Omit for every profile you can access. | [optional]  |

### Return type

[**GetSurveyAnswers200Response**](GetSurveyAnswers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The answers, most given first. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettrackingsite"></a>
# **GetTrackingSite**
> CreateTrackingSite201Response GetTrackingSite (string siteId)

Get a tracking site

One site, with its snippet, its custom subdomain and the latest result of each setup check.

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
    public class GetTrackingSiteExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var siteId = "siteId_example";  // string | 

            try
            {
                // Get a tracking site
                CreateTrackingSite201Response result = apiInstance.GetTrackingSite(siteId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.GetTrackingSite: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTrackingSiteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a tracking site
    ApiResponse<CreateTrackingSite201Response> response = apiInstance.GetTrackingSiteWithHttpInfo(siteId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.GetTrackingSiteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **siteId** | **string** |  |  |

### Return type

[**CreateTrackingSite201Response**](CreateTrackingSite201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The site. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | No site with this id in your workspace (code &#x60;tracking_site_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadconversionassociations"></a>
# **ListAdConversionAssociations**
> ListAdConversionAssociations200Response ListAdConversionAssociations (string accountId, string destinationId, string adAccountId)

List associated campaigns

Lists the LinkedIn campaigns that track a conversion rule, so you can spot newer campaigns that still need linking.  LinkedIn-only today. Returns the campaigns currently associated with this conversion rule. Auto-association on rule creation runs once at create time; campaigns created after the rule still need explicit association. 

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
    public class ListAdConversionAssociationsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected ads account (SocialAccount ID).
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | 

            try
            {
                // List associated campaigns
                ListAdConversionAssociations200Response result = apiInstance.ListAdConversionAssociations(accountId, destinationId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.ListAdConversionAssociations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdConversionAssociationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List associated campaigns
    ApiResponse<ListAdConversionAssociations200Response> response = apiInstance.ListAdConversionAssociationsWithHttpInfo(accountId, destinationId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.ListAdConversionAssociationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected ads account (SocialAccount ID). |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string** |  |  |

### Return type

[**ListAdConversionAssociations200Response**](ListAdConversionAssociations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Associations listed |  -  |
| **400** | Validation error. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads add-on or LinkedIn reconnect required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support associations. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadconversiondestinations"></a>
# **ListAdConversionDestinations**
> ListAdConversionDestinations200Response ListAdConversionDestinations (string accountId)

List conversion destinations

Lists where an ad account can receive conversion events (pixels, conversion actions or rules), so you know where to send them.  Returns the list of pixels (Meta), conversion actions (Google), conversion rules (LinkedIn), pixels (OpenAI Ads, Reddit) or ad accounts (Pinterest) accessible to the connected ads account. Save the returned `id` as a destination with `POST /v1/events/destinations` (or pass it in `destinations` on `POST /v1/events`).  For Google and LinkedIn, each destination's `type` reflects the conversion type (PURCHASE, LEAD, SIGN_UP, etc.), and the event type is locked to the destination. For Meta, OpenAI Ads and Reddit, `type` is absent: pixels accept any event name per request.  For Reddit, the pixels of every ad account the connection reaches (only the scoped ones when the connection has an ad-account scope), each with the `adAccountId` that owns it. Reddit pixels are created in Reddit Ads Manager, not through Zernio.  For LinkedIn, destinations are returned across every sponsored ad account the connected token can access; the `adAccountId` field on each destination identifies the parent ad account and is required for subsequent CRUD calls (update, delete, associations, metrics). 

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
    public class ListAdConversionDestinationsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | SocialAccount ID (metaads, googleads, linkedinads, tiktokads, openaiads, pinterestads, or redditads).

            try
            {
                // List conversion destinations
                ListAdConversionDestinations200Response result = apiInstance.ListAdConversionDestinations(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.ListAdConversionDestinations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdConversionDestinationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List conversion destinations
    ApiResponse<ListAdConversionDestinations200Response> response = apiInstance.ListAdConversionDestinationsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.ListAdConversionDestinationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | SocialAccount ID (metaads, googleads, linkedinads, tiktokads, openaiads, pinterestads, or redditads). |  |

### Return type

[**ListAdConversionDestinations200Response**](ListAdConversionDestinations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Destinations listed |  -  |
| **400** | Account&#39;s platform is not supported by the Conversions API. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), OR (for LinkedIn) the connected account lacks the &#x60;rw_conversions&#x60; scope and must be reconnected.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadconversiongoals"></a>
# **ListAdConversionGoals**
> ListAdConversionGoals200Response ListAdConversionGoals (string accountId, string? adAccountId = null, string? customerId = null)

List account conversion goals

Lists a Google Ads account's default conversion goals, which ones are used for bidding, and the conversion actions in each.  These are Google Ads account-default conversion goals (CustomerConversionGoal), one per category and origin. Each goal carries:  - `biddable`: whether the goal is used for bidding and reported in the Conversions column. - The conversion actions that belong to it, each flagged `primaryForGoal` (primary) or not (secondary).  ### Caching  Reads are cached for 10 minutes. When the shared Google quota is exhausted, the last successful result is served with `stale: true`. 

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
    public class ListAdConversionGoalsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (Google Ads)
            var adAccountId = "adAccountId_example";  // string? | Google customer id. Required when the connection has multiple customers. (optional) 
            var customerId = "customerId_example";  // string? | Alias of adAccountId (optional) 

            try
            {
                // List account conversion goals
                ListAdConversionGoals200Response result = apiInstance.ListAdConversionGoals(accountId, adAccountId, customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.ListAdConversionGoals: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdConversionGoalsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List account conversion goals
    ApiResponse<ListAdConversionGoals200Response> response = apiInstance.ListAdConversionGoalsWithHttpInfo(accountId, adAccountId, customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.ListAdConversionGoalsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (Google Ads) |  |
| **adAccountId** | **string?** | Google customer id. Required when the connection has multiple customers. | [optional]  |
| **customerId** | **string?** | Alias of adAccountId | [optional]  |

### Return type

[**ListAdConversionGoals200Response**](ListAdConversionGoals200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account conversion goals |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;ad_account_not_selected&#x60;. The connection has selected ad accounts (its ad-account scope, set with the dashboard picker or GET /v1/connect/{platform}/ads with adAccountIds) and the targeted ad account is not among them. The connection may not act on it, even though its token can reach it.  &#x60;details&#x60; carries &#x60;accountId&#x60; (the connection), &#x60;adAccountId&#x60; (the refused ad account) and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (adAccountIds replaces the whole selection, so pass the ids already selected plus this one) or use a connection that has it selected. Connections without a selection keep reaching every ad account their token can manage.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | Only available on Google Ads accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadcustomconversions"></a>
# **ListAdCustomConversions**
> ListAdCustomConversions200Response ListAdCustomConversions (string accountId, string adAccountId)

List custom conversions

Lists a Meta ad account's custom conversions, including archived ones.  The ad account's Meta custom conversions, including archived ones (`isArchived`). 

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
    public class ListAdCustomConversionsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Meta ads SocialAccount id.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).

            try
            {
                // List custom conversions
                ListAdCustomConversions200Response result = apiInstance.ListAdCustomConversions(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.ListAdCustomConversions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdCustomConversionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List custom conversions
    ApiResponse<ListAdCustomConversions200Response> response = apiInstance.ListAdCustomConversionsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.ListAdCustomConversionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Meta ads SocialAccount id. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |

### Return type

[**ListAdCustomConversions200Response**](ListAdCustomConversions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Custom conversions |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required, or the token lacks the ads permissions.  Also returned with code &#x60;ad_account_not_selected&#x60; when the connection has selected ad accounts and the targeted ad account is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection), or use a connection that has it selected. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listconversionactions"></a>
# **ListConversionActions**
> ListConversionActions200Response ListConversionActions (string accountId, string? adAccountId = null, string? customerId = null, string? type = null)

List conversion actions

Lists the conversion actions in a Google Ads account, with the website tag snippets to install where available.  Lists Google Ads conversion actions on the resolved customer, all types by default. Each action's `tagSnippets` (global site tag + event snippet) is included when Google has them for that action's type, e.g. `WEBPAGE`. Google-only; other platforms return `501`. Requires the Ads add-on.  `adAccountId` (alias `customerId`) is optional: when omitted, it is resolved from the connection's accessible Google Ads customers, and the call fails with `400` when more than one is accessible (pass `adAccountId` to disambiguate).  The list itself is cached for the quota window (1 hour fresh, up to 7 days last-good; the cache key does not vary on `type`). The response carries `cachedAt` and `stale`, set when a quota-exhausted call falls back to the last-good copy instead of a live read. 

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
    public class ListConversionActionsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | SocialAccount _id (must be a googleads account).
            var adAccountId = "adAccountId_example";  // string? | Platform ad account ID (Google customer ID, digits only). Resolved automatically when the connection has exactly one accessible customer. (optional) 
            var customerId = "customerId_example";  // string? | Alias of adAccountId, kept for existing callers (optional) 
            var type = "type_example";  // string? | Filter by Google's ConversionActionType enum (e.g. WEBPAGE, UPLOAD_CLICKS). (optional) 

            try
            {
                // List conversion actions
                ListConversionActions200Response result = apiInstance.ListConversionActions(accountId, adAccountId, customerId, type);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.ListConversionActions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListConversionActionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List conversion actions
    ApiResponse<ListConversionActions200Response> response = apiInstance.ListConversionActionsWithHttpInfo(accountId, adAccountId, customerId, type);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.ListConversionActionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | SocialAccount _id (must be a googleads account). |  |
| **adAccountId** | **string?** | Platform ad account ID (Google customer ID, digits only). Resolved automatically when the connection has exactly one accessible customer. | [optional]  |
| **customerId** | **string?** | Alias of adAccountId, kept for existing callers | [optional]  |
| **type** | **string?** | Filter by Google&#39;s ConversionActionType enum (e.g. WEBPAGE, UPLOAD_CLICKS). | [optional]  |

### Return type

[**ListConversionActions200Response**](ListConversionActions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The resolved customer and its conversion actions. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans).  Also returned with code &#x60;ad_account_not_selected&#x60; when the connection has selected ad accounts and the targeted Google Ads customer is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  Fix: add it to the selection (GET /v1/connect/googleads/ads with adAccountIds, which replaces the selection) or use a connection that has it selected.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | Google Ads only. Two cases:  - &#x60;ads_connection_required&#x60;: no Google Ads customer account is left on this connection after its ad-account selection. Reconnect via GET /v1/connect/googleads/ads with a Google user that can reach the ad account, or select one of its ad accounts. - &#x60;invalid_resource_state&#x60;: the connection reaches only a Google Ads manager account with no client accounts yet. Create one with POST /v1/ads/accounts or under the manager in Google Ads, then retry.  |  -  |
| **501** | Conversion actions are only available for Google Ads (the account&#39;s platform is not &#x60;googleads&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listconversionassociations"></a>
# **ListConversionAssociations**
> ListAdConversionAssociations200Response ListConversionAssociations (string accountId, string destinationId, string adAccountId)

List associated campaigns

The first path of `GET /v1/ads/conversions/destinations/{destinationId}/associations` (`listAdConversionAssociations`), which does the same with `accountId` as a parameter. It keeps working. 

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
    public class ListConversionAssociationsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | 

            try
            {
                // List associated campaigns
                ListAdConversionAssociations200Response result = apiInstance.ListConversionAssociations(accountId, destinationId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.ListConversionAssociations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListConversionAssociationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List associated campaigns
    ApiResponse<ListAdConversionAssociations200Response> response = apiInstance.ListConversionAssociationsWithHttpInfo(accountId, destinationId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.ListConversionAssociationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string** |  |  |

### Return type

[**ListAdConversionAssociations200Response**](ListAdConversionAssociations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Associations listed |  -  |
| **400** | Validation error. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads add-on or LinkedIn reconnect required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support associations. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listconversiondestinations"></a>
# **ListConversionDestinations**
> ListAdConversionDestinations200Response ListConversionDestinations (string accountId)

List conversion destinations

The first path of `GET /v1/ads/conversions/destinations` (`listAdConversionDestinations`), which does the same with `accountId` as a parameter. It keeps working. 

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
    public class ListConversionDestinationsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | SocialAccount ID (metaads, googleads, linkedinads, tiktokads, openaiads, pinterestads, or redditads).

            try
            {
                // List conversion destinations
                ListAdConversionDestinations200Response result = apiInstance.ListConversionDestinations(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.ListConversionDestinations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListConversionDestinationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List conversion destinations
    ApiResponse<ListAdConversionDestinations200Response> response = apiInstance.ListConversionDestinationsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.ListConversionDestinationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | SocialAccount ID (metaads, googleads, linkedinads, tiktokads, openaiads, pinterestads, or redditads). |  |

### Return type

[**ListAdConversionDestinations200Response**](ListAdConversionDestinations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Destinations listed |  -  |
| **400** | Account&#39;s platform is not supported by the Conversions API. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), OR (for LinkedIn) the connected account lacks the &#x60;rw_conversions&#x60; scope and must be reconnected.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcustomconversiongoals"></a>
# **ListCustomConversionGoals**
> ListCustomConversionGoals200Response ListCustomConversionGoals (string accountId, string? adAccountId = null, string? customerId = null)

List custom conversion goals

Lists the custom conversion goals in a Google Ads account, each a named set of conversion actions a campaign can bid on.  Google Ads custom conversion goals (a named set of conversion actions a campaign can bid on). Removed goals are excluded. Cached like the other Google reads. 

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
    public class ListCustomConversionGoalsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (Google Ads)
            var adAccountId = "adAccountId_example";  // string? | Google customer id. Required when the connection has multiple customers. (optional) 
            var customerId = "customerId_example";  // string? | Alias of adAccountId (optional) 

            try
            {
                // List custom conversion goals
                ListCustomConversionGoals200Response result = apiInstance.ListCustomConversionGoals(accountId, adAccountId, customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.ListCustomConversionGoals: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCustomConversionGoalsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List custom conversion goals
    ApiResponse<ListCustomConversionGoals200Response> response = apiInstance.ListCustomConversionGoalsWithHttpInfo(accountId, adAccountId, customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.ListCustomConversionGoalsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (Google Ads) |  |
| **adAccountId** | **string?** | Google customer id. Required when the connection has multiple customers. | [optional]  |
| **customerId** | **string?** | Alias of adAccountId | [optional]  |

### Return type

[**ListCustomConversionGoals200Response**](ListCustomConversionGoals200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Custom conversion goals |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;ad_account_not_selected&#x60;. The connection has selected ad accounts (its ad-account scope, set with the dashboard picker or GET /v1/connect/{platform}/ads with adAccountIds) and the targeted ad account is not among them. The connection may not act on it, even though its token can reach it.  &#x60;details&#x60; carries &#x60;accountId&#x60; (the connection), &#x60;adAccountId&#x60; (the refused ad account) and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (adAccountIds replaces the whole selection, so pass the ids already selected plus this one) or use a connection that has it selected. Connections without a selection keep reaching every ad account their token can manage.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | Only available on Google Ads accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listeventdestinations"></a>
# **ListEventDestinations**
> ListEventDestinations200Response ListEventDestinations (string? profileId = null)

List event destinations

The first name of `GET /v1/events/forwarding-rules`, which lists the same rules. It keeps working and answers under `destinations`.

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
    public class ListEventDestinationsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? |  (optional) 

            try
            {
                // List event destinations
                ListEventDestinations200Response result = apiInstance.ListEventDestinations(profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.ListEventDestinations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListEventDestinationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List event destinations
    ApiResponse<ListEventDestinations200Response> response = apiInstance.ListEventDestinationsWithHttpInfo(profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.ListEventDestinationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** |  | [optional]  |

### Return type

[**ListEventDestinations200Response**](ListEventDestinations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Event destinations. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listeventnames"></a>
# **ListEventNames**
> ListEventNames200Response ListEventNames (string? profileId = null)

List stored event names

The event names stored for a profile in the last 30 days, with how many events carry each, most used first. It includes custom names, such as a site's own events, so you can filter `GET /v1/events` by `eventName`.  Without `profileId` it covers every profile you can access. Retracted events are left out. Requires the Ads add-on. 

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
    public class ListEventNamesExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? | The profile to read. Omit to cover every profile you can access. (optional) 

            try
            {
                // List stored event names
                ListEventNames200Response result = apiInstance.ListEventNames(profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.ListEventNames: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListEventNamesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List stored event names
    ApiResponse<ListEventNames200Response> response = apiInstance.ListEventNamesWithHttpInfo(profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.ListEventNamesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** | The profile to read. Omit to cover every profile you can access. | [optional]  |

### Return type

[**ListEventNames200Response**](ListEventNames200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The event names, up to 200. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listevents"></a>
# **ListEvents**
> ListEvents200Response ListEvents (string? profileId = null, int? limit = null, DateTime? from = null, DateTime? to = null, string? eventName = null, string? source = null, string? platform = null, string? deliveryStatus = null, bool? fromAd = null, string? campaignId = null, string? cursor = null)

List stored events

Lists the conversion events stored by `POST /v1/events`, newest first: for one profile, or for every profile you can access when `profileId` is omitted.  Personal data is never returned: `hasEmail`, `hasPhone` and `hasExternalId` only say whether the event carried that identifier. Events sent with `testCode` are not stored, so they never appear here.  Paginate with `cursor`: pass the `nextCursor` of the previous page until it comes back `null`. 

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
    public class ListEventsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? | The profile to list. Omit to cover every profile you can access. (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var from = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | Only events at or after this time (ISO 8601, on the event time). (optional) 
            var to = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | Only events before this time (ISO 8601, on the event time). (optional) 
            var eventName = "eventName_example";  // string? | Only events with this name, such as `Purchase`. (optional) 
            var source = "api";  // string? | Only events from this source, such as `stripe` for the payments of a connected Stripe account. (optional) 
            var platform = "platform_example";  // string? | Only events sent to this ad platform, such as `metaads` or `googleads`. (optional) 
            var deliveryStatus = "sent";  // string? | Only events whose latest send to a destination (of `platform`, when given) was accepted (`sent`) or was not (`failed`: failed or still retrying). (optional) 
            var fromAd = true;  // bool? | `true`: only events carrying an ad click or a campaign (a gclid, gbraid or wbraid, a `zrn`, or a matched campaign). `false`: only the others. (optional) 
            var campaignId = "campaignId_example";  // string? | Only events of this ad platform campaign id: matched to it, or behind a Google click of it. (optional) 
            var cursor = "cursor_example";  // string? | `nextCursor` from the previous page. (optional) 

            try
            {
                // List stored events
                ListEvents200Response result = apiInstance.ListEvents(profileId, limit, from, to, eventName, source, platform, deliveryStatus, fromAd, campaignId, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.ListEvents: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListEventsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List stored events
    ApiResponse<ListEvents200Response> response = apiInstance.ListEventsWithHttpInfo(profileId, limit, from, to, eventName, source, platform, deliveryStatus, fromAd, campaignId, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.ListEventsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** | The profile to list. Omit to cover every profile you can access. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **from** | **DateTime?** | Only events at or after this time (ISO 8601, on the event time). | [optional]  |
| **to** | **DateTime?** | Only events before this time (ISO 8601, on the event time). | [optional]  |
| **eventName** | **string?** | Only events with this name, such as &#x60;Purchase&#x60;. | [optional]  |
| **source** | **string?** | Only events from this source, such as &#x60;stripe&#x60; for the payments of a connected Stripe account. | [optional]  |
| **platform** | **string?** | Only events sent to this ad platform, such as &#x60;metaads&#x60; or &#x60;googleads&#x60;. | [optional]  |
| **deliveryStatus** | **string?** | Only events whose latest send to a destination (of &#x60;platform&#x60;, when given) was accepted (&#x60;sent&#x60;) or was not (&#x60;failed&#x60;: failed or still retrying). | [optional]  |
| **fromAd** | **bool?** | &#x60;true&#x60;: only events carrying an ad click or a campaign (a gclid, gbraid or wbraid, a &#x60;zrn&#x60;, or a matched campaign). &#x60;false&#x60;: only the others. | [optional]  |
| **campaignId** | **string?** | Only events of this ad platform campaign id: matched to it, or behind a Google click of it. | [optional]  |
| **cursor** | **string?** | &#x60;nextCursor&#x60; from the previous page. | [optional]  |

### Return type

[**ListEvents200Response**](ListEvents200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A page of stored events. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listforwardingrules"></a>
# **ListForwardingRules**
> ListForwardingRules200Response ListForwardingRules (string? profileId = null)

List forwarding rules

Lists the forwarding rules of one profile, or of every profile you can access. A rule sends a profile's events to one ad platform destination.

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
    public class ListForwardingRulesExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? |  (optional) 

            try
            {
                // List forwarding rules
                ListForwardingRules200Response result = apiInstance.ListForwardingRules(profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.ListForwardingRules: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListForwardingRulesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List forwarding rules
    ApiResponse<ListForwardingRules200Response> response = apiInstance.ListForwardingRulesWithHttpInfo(profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.ListForwardingRulesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** |  | [optional]  |

### Return type

[**ListForwardingRules200Response**](ListForwardingRules200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Forwarding rules. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtrackingsites"></a>
# **ListTrackingSites**
> ListTrackingSites200Response ListTrackingSites (string? profileId = null, int? limit = null, string? cursor = null)

List tracking sites

The websites whose visits and conversions Zernio collects, newest first. Pass `profileId` to list one profile's sites.

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
    public class ListTrackingSitesExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? |  (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? | `pagination.nextCursor` from the previous page. (optional) 

            try
            {
                // List tracking sites
                ListTrackingSites200Response result = apiInstance.ListTrackingSites(profileId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.ListTrackingSites: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTrackingSitesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List tracking sites
    ApiResponse<ListTrackingSites200Response> response = apiInstance.ListTrackingSitesWithHttpInfo(profileId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.ListTrackingSitesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** | &#x60;pagination.nextCursor&#x60; from the previous page. | [optional]  |

### Return type

[**ListTrackingSites200Response**](ListTrackingSites200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One page of sites. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removeadconversionassociations"></a>
# **RemoveAdConversionAssociations**
> RemoveAdConversionAssociations200Response RemoveAdConversionAssociations (string accountId, string destinationId, string adAccountId, string campaignIds)

Remove associated campaigns

Unlinks campaigns from a LinkedIn conversion rule so they stop tracking it.  Pass `adAccountId` and `campaignIds` as query parameters (`campaignIds` is comma-separated).  The route also accepts a JSON body with the same fields, for clients that prefer DELETE-with-body. The documented surface is query-only because some SDK code generators (e.g. Python) collapse query + body parameters with the same name into a single kwarg. 

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
    public class RemoveAdConversionAssociationsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected ads account (SocialAccount ID).
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | 
            var campaignIds = "campaignIds_example";  // string | Comma-separated list of campaign IDs.

            try
            {
                // Remove associated campaigns
                RemoveAdConversionAssociations200Response result = apiInstance.RemoveAdConversionAssociations(accountId, destinationId, adAccountId, campaignIds);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.RemoveAdConversionAssociations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveAdConversionAssociationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove associated campaigns
    ApiResponse<RemoveAdConversionAssociations200Response> response = apiInstance.RemoveAdConversionAssociationsWithHttpInfo(accountId, destinationId, adAccountId, campaignIds);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.RemoveAdConversionAssociationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected ads account (SocialAccount ID). |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string** |  |  |
| **campaignIds** | **string** | Comma-separated list of campaign IDs. |  |

### Return type

[**RemoveAdConversionAssociations200Response**](RemoveAdConversionAssociations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Per-campaign batch result. Status is 200 even when some rows failed. Inspect &#x60;failed[]&#x60; for details.  |  -  |
| **400** | Validation error: missing &#x60;adAccountId&#x60; or &#x60;campaignIds&#x60;, campaignIds exceeds 100 entries per request, or &#x60;accountId&#x60; is not a valid id.  |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Forbidden. One of:  - Ads add-on or LinkedIn reconnect required. - Code &#x60;ad_account_not_selected&#x60;: the connection has selected ad accounts and the ad account this request targets is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  To fix &#x60;ad_account_not_selected&#x60;, add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection) or use a connection that has it selected. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support associations. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removeconversionassociations"></a>
# **RemoveConversionAssociations**
> RemoveAdConversionAssociations200Response RemoveConversionAssociations (string accountId, string destinationId, string adAccountId, string campaignIds)

Remove associated campaigns

The first path of `DELETE /v1/ads/conversions/destinations/{destinationId}/associations` (`removeAdConversionAssociations`), which does the same with `accountId` as a parameter. It keeps working. 

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
    public class RemoveConversionAssociationsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | 
            var campaignIds = "campaignIds_example";  // string | Comma-separated list of campaign IDs.

            try
            {
                // Remove associated campaigns
                RemoveAdConversionAssociations200Response result = apiInstance.RemoveConversionAssociations(accountId, destinationId, adAccountId, campaignIds);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.RemoveConversionAssociations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveConversionAssociationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove associated campaigns
    ApiResponse<RemoveAdConversionAssociations200Response> response = apiInstance.RemoveConversionAssociationsWithHttpInfo(accountId, destinationId, adAccountId, campaignIds);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.RemoveConversionAssociationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string** |  |  |
| **campaignIds** | **string** | Comma-separated list of campaign IDs. |  |

### Return type

[**RemoveAdConversionAssociations200Response**](RemoveAdConversionAssociations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Per-campaign batch result. Status is 200 even when some rows failed. Inspect &#x60;failed[]&#x60; for details.  |  -  |
| **400** | Validation error: missing &#x60;adAccountId&#x60; or &#x60;campaignIds&#x60;, campaignIds exceeds 100 entries per request, or &#x60;accountId&#x60; is not a valid id.  |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Forbidden. One of:  - Ads add-on or LinkedIn reconnect required. - Code &#x60;ad_account_not_selected&#x60;: the connection has selected ad accounts and the ad account this request targets is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  To fix &#x60;ad_account_not_selected&#x60;, add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection) or use a connection that has it selected. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support associations. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removecustomconversiongoal"></a>
# **RemoveCustomConversionGoal**
> RemoveCustomConversionGoal200Response RemoveCustomConversionGoal (string goalId, string accountId, string? adAccountId = null, string? customerId = null)

Remove a custom conversion goal

Deletes a Google Ads custom conversion goal; switch any campaigns using it to another goal first.  Google refuses (400) while any campaign still uses it: switch those campaigns to another goal first. 

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
    public class RemoveCustomConversionGoalExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var goalId = "goalId_example";  // string | Google custom conversion goal id
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (Google Ads)
            var adAccountId = "adAccountId_example";  // string? | Google customer id. Required when the connection has multiple customers. (optional) 
            var customerId = "customerId_example";  // string? | Alias of adAccountId (optional) 

            try
            {
                // Remove a custom conversion goal
                RemoveCustomConversionGoal200Response result = apiInstance.RemoveCustomConversionGoal(goalId, accountId, adAccountId, customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.RemoveCustomConversionGoal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveCustomConversionGoalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove a custom conversion goal
    ApiResponse<RemoveCustomConversionGoal200Response> response = apiInstance.RemoveCustomConversionGoalWithHttpInfo(goalId, accountId, adAccountId, customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.RemoveCustomConversionGoalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goalId** | **string** | Google custom conversion goal id |  |
| **accountId** | **string** | Zernio SocialAccount id (Google Ads) |  |
| **adAccountId** | **string?** | Google customer id. Required when the connection has multiple customers. | [optional]  |
| **customerId** | **string?** | Alias of adAccountId | [optional]  |

### Return type

[**RemoveCustomConversionGoal200Response**](RemoveCustomConversionGoal200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Custom goal removed |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;ad_account_not_selected&#x60;. The connection has selected ad accounts (its ad-account scope, set with the dashboard picker or GET /v1/connect/{platform}/ads with adAccountIds) and the targeted ad account is not among them. The connection may not act on it, even though its token can reach it.  &#x60;details&#x60; carries &#x60;accountId&#x60; (the connection), &#x60;adAccountId&#x60; (the refused ad account) and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (adAccountIds replaces the whole selection, so pass the ids already selected plus this one) or use a connection that has it selected. Connections without a selection keep reaching every ad account their token can manage.  |  -  |
| **404** | Goal not found on this customer, or account unavailable |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | Only available on Google Ads accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="restateevent"></a>
# **RestateEvent**
> RestateEvent200Response RestateEvent (string eventId, RestateEventRequest restateEventRequest)

Change a stored event's value

Changes the value of an event you already sent, for a partial refund or an upgrade. Send the corrected total, not a difference.  Zernio stores a new version of the event, so campaign results count the new value at once. It then passes the change to each destination the event reached: Google Ads restates the conversion, and platforms without a correction API report `not_supported` and keep their count. 

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
    public class RestateEventExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var eventId = "eventId_example";  // string | The `eventId` the event was sent with.
            var restateEventRequest = new RestateEventRequest(); // RestateEventRequest | 

            try
            {
                // Change a stored event's value
                RestateEvent200Response result = apiInstance.RestateEvent(eventId, restateEventRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.RestateEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestateEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Change a stored event's value
    ApiResponse<RestateEvent200Response> response = apiInstance.RestateEventWithHttpInfo(eventId, restateEventRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.RestateEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **eventId** | **string** | The &#x60;eventId&#x60; the event was sent with. |  |
| **restateEventRequest** | [**RestateEventRequest**](RestateEventRequest.md) |  |  |

### Return type

[**RestateEvent200Response**](RestateEvent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The event was restated. Check each destination. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="retractevent"></a>
# **RetractEvent**
> RetractEvent200Response RetractEvent (string eventId, string profileId)

Retract a stored event

Retracts an event you already sent, for a refund, a cancelled order or a lost deal. It stops counting in campaign results and ad rules.  Each destination the event reached is told where the platform allows it: Google Ads retracts the conversion, and the other platforms report `not_supported` and keep their count. Sending the same `eventId` again stores it anew. 

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
    public class RetractEventExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var eventId = "eventId_example";  // string | The `eventId` the event was sent with.
            var profileId = "profileId_example";  // string | Profile the event belongs to.

            try
            {
                // Retract a stored event
                RetractEvent200Response result = apiInstance.RetractEvent(eventId, profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.RetractEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RetractEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retract a stored event
    ApiResponse<RetractEvent200Response> response = apiInstance.RetractEventWithHttpInfo(eventId, profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.RetractEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **eventId** | **string** | The &#x60;eventId&#x60; the event was sent with. |  |
| **profileId** | **string** | Profile the event belongs to. |  |

### Return type

[**RetractEvent200Response**](RetractEvent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The event was retracted. Check each destination. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="rotatetrackingsitekey"></a>
# **RotateTrackingSiteKey**
> CreateTrackingSite201Response RotateTrackingSiteKey (string siteId, string idempotencyKey)

Rotate a tracking site's key

Issues a new `siteKey`. The old key keeps working for 7 days, so update the snippet on your site within that time.

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
    public class RotateTrackingSiteKeyExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var siteId = "siteId_example";  // string | 
            var idempotencyKey = "idempotencyKey_example";  // string | A unique key per rotation, such as a UUID.

            try
            {
                // Rotate a tracking site's key
                CreateTrackingSite201Response result = apiInstance.RotateTrackingSiteKey(siteId, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.RotateTrackingSiteKey: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RotateTrackingSiteKeyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Rotate a tracking site's key
    ApiResponse<CreateTrackingSite201Response> response = apiInstance.RotateTrackingSiteKeyWithHttpInfo(siteId, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.RotateTrackingSiteKeyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **siteId** | **string** |  |  |
| **idempotencyKey** | **string** | A unique key per rotation, such as a UUID. |  |

### Return type

[**CreateTrackingSite201Response**](CreateTrackingSite201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The site with its new key and snippet. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sendconversions"></a>
# **SendConversions**
> SendConversions200Response SendConversions (SendConversionsRequest sendConversionsRequest)

Send conversion events to one destination (legacy)

Legacy: use [`POST /v1/events`](/conversions/send-events) instead. It sends each event once to every saved destination, retries failures, stores the event and reports what each platform answered. This endpoint keeps working and is not being removed.  Sends conversion events, such as purchases or leads, from your server to one ad platform destination so it can attribute and optimize ads.  Relays one or more events to the target ad platform's native Conversions API. The platform is inferred from the provided `accountId`. Requires the Ads add-on.  ### Supported platforms  - Meta (`metaads`) via Graph API - Google Ads (`googleads`) via Data Manager API `ingestEvents` - LinkedIn (`linkedinads`) via `/rest/conversionEvents` - TikTok (`tiktokads`) via the Offline Events API `/offline/batch/` (OFFLINE conversions only) - OpenAI Ads (`openaiads`) via its Conversions API (a separate host, `bzr.openai.com`) - Pinterest (`pinterestads`) via `POST /v5/ad_accounts/{id}/events` - Reddit (`redditads`) via the Reddit Conversions API (`POST /api/v3/pixels/{pixelId}/conversion_events`) - Microsoft Advertising (`microsoftads`) via offline conversion uploads (`ApplyOfflineConversions`) or the UET Conversions API (`POST https://capi.uet.microsoft.com/v1/{tagId}/events`) - X Ads (`xads`) via the X Conversion API (`POST /12/measurement/conversions/{pixelId}`) - Snapchat (`snapchatads`) via the Snapchat Conversions API (`POST https://tr.snapchat.com/v3/{pixelId}/events`) - Taboola (`taboolaads`) via its S2S postback (`GET https://trc.taboola.com/actions-handler/log/3/s2s-action`), one request per event - Outbrain (`outbrainads`) via its S2S pixel (`GET https://tr.outbrain.com/unifiedPixel`), one request per event - Klaviyo (`klaviyo`) via the Events API (`POST https://a.klaviyo.com/api/events`) - Attentive (`attentive`) via the eCommerce and Custom Events APIs - Impact (`impact`) via the Conversions API (`POST /Advertisers/{AccountSID}/Conversions`) - Awin (`awin`) via the Conversion API (`POST /s2s/advertiser/{advertiserId}/orders`) - Campaign Manager 360 (`campaignmanager360`, coming soon: pending Google's verification of the `dfatrafficking` permission) via the Data Manager API `ingestEvents`, to a Floodlight activity - The Trade Desk (`tradedeskads`) via the Real-Time Conversions API (`POST https://insight.adsrvr.org/track/realtimeconversion`) - Amazon Ads (`amazonads`) via the Amazon Ads Conversions API (`POST /adsApi/v1/create/events`)  ### `destinationId` per platform  - Meta: pixel (dataset) ID, e.g. `123456789012345` - Google: conversion action resource name, e.g. `customers/1234567890/conversionActions/987654321` - LinkedIn: conversion rule ID or URN, e.g. `104012` or `urn:lla:llaPartnerConversion:104012` - TikTok: Offline Event Set ID, e.g. `7057103914977558530`. An Offline Event Set has no test mode, so an event with `testCode` is not sent (code `TEST_MODE_UNSUPPORTED`). - OpenAI Ads: pixel wire id (numeric `pixel_id`, distinct from the internal pixel id), as returned by `GET /v1/ads/conversions/destinations` - Pinterest: numeric ad account id, e.g. `549755885175` (Pinterest attributes to the ad account, not to a tag) - Reddit: pixel id, e.g. `a2_abc123`, as returned by `GET /v1/ads/conversions/destinations` (any other shape returns 400) - Microsoft Advertising offline conversion goal, e.g. `accounts/123456789/conversionGoals/987654`. Each event needs `clickIds.msclkid`, an `email` or a `phone`; the goal decides the event type. - Microsoft Advertising UET tag, e.g. `accounts/123456789/uetTags/26012345`. Each event needs `clickIds.msclkid`, an `email` or a `phone`. `eventName` is the event action its goals match (a `PageView` with `sourceUrl` is a page load) and `eventId` dedups with the browser tag. - Microsoft has no test mode: with `testCode`, UET events are sent with ad storage denied, which Microsoft excludes from conversion attribution and retargeting. - X Ads: X Pixel event id, e.g. `tw-rbhhj-rcfms`. Each event needs `clickIds.twclid`, an `email`, a `phone`, or `ipAddress` plus `userAgent`; the event decides the type and `eventId` is sent as `conversion_id`. - Snapchat: the connection's Snap Pixel ID, e.g. `1a2b3c4d-5e6f-4a8b-9c0d-1e2f3a4b5c6d`. Each event needs an `email`, a `phone`, or `ipAddress` plus `userAgent`; website events also need `sourceUrl`. With `testCode`, events go to Snap's validate endpoint and are not recorded. - Taboola: the connection's numeric Taboola Account ID, e.g. `1234567`. Each event needs `clickIds.tblci`. `eventName` is sent as is and must equal the Event Name of a conversion rule in Realize (case-sensitive). Taboola has no test mode, so an event with `testCode` is not sent (code `TEST_MODE_UNSUPPORTED`). - Outbrain: the connection's Outbrain marketer id, e.g. `00f4b02153ee75f3c9dc4fc128ab0419ab`. Each event needs `clickIds.ob_click_id`. `eventName` is sent as is and must equal the name of an Event-Based Conversion in Amplify (case-sensitive). Outbrain has no test mode, so an event with `testCode` is not sent (code `TEST_MODE_UNSUPPORTED`). - Klaviyo: the connection's Klaviyo account id. Each event needs an unhashed `email`, a `phone` with its country code, or an `externalId`; `eventId` is the `unique_id`. Klaviyo has no test mode, so an event with `testCode` is not sent (code `TEST_MODE_UNSUPPORTED`). - Klaviyo metrics: `Purchase` is `Placed Order`, `InitiateCheckout` `Started Checkout`, `ViewContent` `Viewed Product`, `AddToCart` `Added to Cart`; any other name is a metric of that name. - Attentive: the connection's Attentive company id. `Purchase`, `AddToCart` and `ViewContent` with priced `items` go to the eCommerce endpoints; every other event goes out as a custom event named `eventName`. Each event needs an unhashed `email`, a `phone` with its country code, or an `externalId`. A `testCode` is refused. - Impact: `<program id>:<event type id>`, e.g. `12345:67890`. Each event needs `clickIds.irclickid`, an `externalId` (sent as `CustomerId`) or `platformData.promo_code`; the email is sent SHA-256 hashed. Priced `items` are sent as item lines, otherwise `value` as the order subtotal. A `testCode` is refused: credit a test partner instead. - Awin: the connection's advertiser id. Each event needs `clickIds.awc` (or `platformData.voucher`), `value` and `currency`; `value` is the order amount on the `DEFAULT` commission group (`platformData.commission_group` overrides it). With `testCode`, orders are sent with `isTest` and not tracked. - Attentive and Impact have no test mode, so an event with `testCode` is not sent (code `TEST_MODE_UNSUPPORTED`). - Impact and Awin refuse browsing and funnel steps (`ViewContent`, `AddToCart`, `InitiateCheckout` and the like): they pay a partner for every conversion they get. - Campaign Manager 360: `<floodlightConfigurationId>:<floodlightActivityId>`, e.g. `1234567:7654321`. Each event needs `clickIds.gclid` or `clickIds.dclid` (a hashed email or phone only enhances it); `eventId` is the transaction id Google dedups on. With `testCode`, events are only validated (`validateOnly`) and not recorded. - The Trade Desk: the connection's tracking tag id, e.g. `abc1234`. Each event needs `clickIds.tdid`, `clickIds.uid2` or `clickIds.uid2Token`; `eventId` is sent as `order_id`. TTD has no test mode, so an event with `testCode` is not sent (code `TEST_MODE_UNSUPPORTED`). - Amazon Ads: `<region>:<profileId>:<accountId>:<country>`, e.g. `EU:42:ENTITY1ABC:DE`. Each event needs an `email` or a `phone` (sent hashed); `eventId` is Amazon's dedup key; standard event names keep their name and custom ones are sent as `Custom` (Amazon caps conversion definitions at 100). No test mode: an event with `testCode` is not sent.  Callers can list valid destinations via `GET /v1/ads/conversions/destinations`.  ### Pinterest notes  - Each event needs an `email`, or `ipAddress` plus `userAgent`. Others are listed in `failures` with code `INVALID_EVENT` and the rest are still sent. - `clickIds.epik` (the `_epik` cookie) is sent as `click_id`. - `actionSource` `web` stays `web`, offline sources become `offline`, and app events need `platformData.action_source` `app_android` or `app_ios`. - Pinterest answers per event, so one bad event does not fail its chunk (failures carry code `PINTEREST_EVENT_FAILED`). - `consent.adUserData: DENIED` sets `opt_out`. - The connected user needs a Business Access role on the ad account (403 otherwise).  ### Reddit notes  - Each event needs a match key: `clickIds.rdt_cid`, `clickIds.rdt_uuid`, `email`, `phone`, `externalId`, or `ipAddress` plus `userAgent`. - Reddit accepts events up to 7 days old. `eventTime` is unix SECONDS (a value more than an hour in the future is refused as milliseconds). - Events failing these checks are listed in `failures` with code `INVALID_EVENT` and the rest are still sent. - Email (lowercased, dots and `+tags` stripped from the local part), phone (E.164 with the leading `+`) and `externalId` are SHA-256 hashed. IP and user agent go plaintext. - `consent.adUserData: DENIED` sends no user fields. - `actionSource` maps to WEBSITE (`web`), APP (`app`) or OTHER, overridable with `platformData.action_source`. `platformData.order_id` is forwarded. - `testCode` is sent as Reddit's `test_id`.  Reddit errors:  - 403 `reconnect_required`: the connection was authorized without the `adsconversions` permission (reconnect via GET /v1/connect/redditads/ads). - 403 `insufficient_permissions`: the Reddit user has no role on the ad account that owns the pixel. - `REDDIT_REJECTED`: Reddit throttling and other rejections, reported per chunk in `failures`.  ### TikTok notes  Two kinds of destination. A TikTok pixel (`destinationId` `pixel:<pixelCode>`, as listed by the destinations endpoint) takes website events through the Events API and honours `testCode`. An offline event set (its numeric id) takes in-store, CRM and call-center conversions; each of those events must carry an email or phone.  The connected TikTok ads account must have granted the Offline Events permission; older grants must reconnect.  ### OpenAI Ads notes  Requires a tracking tag (pixel) to already exist on the account. Returns 422 with code `TRACKING_TAG_REQUIRED` if `POST /v1/accounts/{accountId}/tracking-tags` hasn't been called yet.  ### Hashing  All PII (email, phone, names, external IDs) is hashed with SHA-256 server-side per each platform's normalization spec, including Google's Gmail-specific dot/plus-suffix stripping. Send plaintext.  LinkedIn `externalIds` are passed through as plaintext per LinkedIn's spec; only emails and phones are hashed.  For LinkedIn, the connected account must have been authorized after the Conversions API rollout (the OAuth grant must include `rw_conversions`). Older accounts must reconnect.  ### Batching  Batching is handled automatically. Per-platform caps:  - Meta: 1000 events per request; rejects the entire batch if any event is malformed. - Google: 2000. - LinkedIn: 5000, all-or-nothing per chunk. - OpenAI Ads: 1000 per request. Larger submissions are split into 1000-event chunks, each all-or-nothing (a malformed event fails every event in that chunk, not the whole request). - Reddit: works the same way as OpenAI Ads, in chunks of 1000. - TikTok: 1000. Microsoft: its offline conversion cap per request. X: 500. Other destinations are sent in their platform's own batch size or one event at a time. - An event a platform would refuse (too old, no usable identifier) is listed in `failures` and the rest of its chunk is still sent, except on Google Ads and OpenAI Ads.  ### Dedup  Pass a stable `eventId` on every event:  - Meta and LinkedIn use it to dedupe against browser-side pixel/Insight Tag events. - Google maps it to `transactionId`. - Reddit receives it as `conversion_id`, its dedup key against Reddit Pixel events.  ### `eventName` per platform  - Meta: free-form. Standard names (Purchase, Lead, ...) match Meta's built-in events; custom strings are accepted. - Google: ignored. The conversion action's category determines the event type. Send the standard name closest to your action for documentation, but the platform will not branch on it. - LinkedIn: ignored. The conversion rule's `type` (LEAD, PURCHASE, etc.) is locked to the destination at rule-creation time. Send the standard name for documentation; LinkedIn does not branch on it. - OpenAI Ads: a fixed subset of standard names maps 1:1 onto OpenAI's own event-type enum: Purchase, Lead, AddToCart, ViewContent, InitiateCheckout, CompleteRegistration, Subscribe, StartTrial, Schedule. Any other standard name or custom string is sent as `type: custom` with the name preserved. - Pinterest: standard names map onto Pinterest's (see below). Any other string is sent as is, so it matches an advertiser defined event of that name.  Pinterest name mapping:  - Purchase = `checkout` - AddToCart = `add_to_cart` - InitiateCheckout = `initiate_checkout` - AddPaymentInfo = `add_payment_info` - Lead = `lead` - CompleteRegistration = `signup` - Subscribe = `subscribe` - ViewContent = `view_content` - Search = `search` - PageView = `page_visit` 

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
    public class SendConversionsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var sendConversionsRequest = new SendConversionsRequest(); // SendConversionsRequest | 

            try
            {
                // Send conversion events to one destination (legacy)
                SendConversions200Response result = apiInstance.SendConversions(sendConversionsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.SendConversions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendConversionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send conversion events to one destination (legacy)
    ApiResponse<SendConversions200Response> response = apiInstance.SendConversionsWithHttpInfo(sendConversionsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.SendConversionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sendConversionsRequest** | [**SendConversionsRequest**](SendConversionsRequest.md) |  |  |

### Return type

[**SendConversions200Response**](SendConversions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Events processed. Inspect &#x60;eventsFailed&#x60; and &#x60;failures[]&#x60; to detect partial failure.  - Meta: a batch is all-or-nothing (either every event in a chunk succeeds, or every event in the chunk is listed in failures). - Google: success/failure is reported at the request level only. - OpenAI Ads and Reddit: each 1000-event chunk is all-or-nothing, same as Meta.  |  -  |
| **400** | Invalid body (missing accountId/destinationId/events, malformed event shape, a &#x60;test_event_code&#x60; that is not a non-empty string, &#x60;testCode&#x60; and &#x60;test_event_code&#x60; with different values), or (Google Ads, param &#x60;destinationId&#x60;) the customer named in &#x60;destinationId&#x60; is not one of this connection&#39;s Google Ads accounts. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Forbidden. One of:  - Ads access required (Ads add-on on legacy plans, included on usage-based plans). - LinkedIn: the connected account lacks the &#x60;rw_conversions&#x60; scope and must be reconnected. - Reddit: the connection lacks the &#x60;adsconversions&#x60; permission (code &#x60;reconnect_required&#x60;, reconnect Reddit Ads), or the Reddit user has no role on the ad account that owns the pixel (code &#x60;insufficient_permissions&#x60;). - Google Ads: code &#x60;ad_account_not_selected&#x60;. The connection has selected ad accounts and the Google Ads customer named in &#x60;destinationId&#x60; is not among them (param &#x60;destinationId&#x60;; &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;).  For &#x60;ad_account_not_selected&#x60;, add the customer to the selection (GET /v1/connect/googleads/ads with adAccountIds, which replaces the selection) or use a connection that has it selected.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | The account is not ready to receive conversions.  - OpenAI Ads, code &#x60;TRACKING_TAG_REQUIRED&#x60;: no tracking tag (pixel) exists yet for this account. Create one via &#x60;POST /v1/accounts/{accountId}/tracking-tags&#x60; first. - Google Ads, code &#x60;ads_connection_required&#x60;: no Google Ads customer account is left on this connection after its ad-account selection. Reconnect via GET /v1/connect/googleads/ads with a Google user that can reach the ad account, or select one of its ad accounts. - Google Ads, code &#x60;invalid_resource_state&#x60;: the connection reaches only a Google Ads manager account with no client accounts yet. Create one with POST /v1/ads/accounts or under the manager in Google Ads, then retry.  |  -  |
| **429** | LinkedIn token-level rate limit hit (600 requests/min, 300k/day per token). Retry with backoff. Meta and Google have their own rate-limit semantics surfaced via platform-specific 4xx responses.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sendevents"></a>
# **SendEvents**
> SendEvents200Response SendEvents (SendEventsRequest sendEventsRequest, string? idempotencyKey = null)

Send events to every destination

The recommended way to send conversions. Sends conversion events once and forwards them to every ad platform destination saved for the profile (see `POST /v1/events/destinations`), or to the `destinations` given in the request. Requires the Ads add-on.  ### Forwarding  - Each destination receives the events exactly as `POST /v1/ads/conversions` would send them, so the per-platform notes there (hashing, batching, `eventName` semantics, dedup on `eventId`) apply here too. - A destination saved with `eventNames` only receives events with those names. - One destination failing never blocks the others: each one reports its own result.  ### Consent  Send each visitor's consent on the event (`events[].consent`) or for the whole request (`consent`), as Google Consent Mode's four signals. Zernio applies it per destination for visitors in the EEA, the UK and Switzerland, read from `user.country` (website events use the visitor's country):  - A signal left out counts as `DENIED`. Zernio has no setting to change this. - Meta, LinkedIn, TikTok, Pinterest, Reddit, X, Snapchat, Microsoft, OpenAI and AppLovin get the event only with `adUserData: GRANTED` and neither `adStorage` nor `adPersonalization` `DENIED`. - Google Ads gets every event with `adUserData` and `adPersonalization` set, a missing one as `DENIED`. Google decides what it can use. - Google Analytics gets the event only with `analyticsStorage: GRANTED`, with the same ad signals. - An event left out is reported on its destination as `drops` (with `consent_denied` or `consent_missing`), as `dropped` on `GET /v1/events/{eventId}`, and counted in `GET /v1/events/overview`. It is still stored and counted in your results. - Visitors elsewhere, or with no `user.country`, are sent as before with the consent they carry.  Zernio applies the consent you send; it does not collect it or give legal advice. Profiles created before this rule started (Nov 2026) keep sending as before until they are switched over.  ### Storage  Zernio also stores each event for the profile's reporting.  - Email, phone and `externalId` are stored only as SHA-256 hashes. - `sourceUrl` keeps only its origin, path and attribution parameters (`utm_*`, `zrn`, `zcid`, `gclid`, `gbraid`, `wbraid`, `fbclid`, `ttclid`, `twclid`, `msclkid`, `li_fat_id`, `epik`, `rdt_cid`, `oppref`, `aleid`, `alart`), each also under a `z`-prefixed copy such as `zgclid`. - Events sent with `testCode` are forwarded but not stored. - Sending an event again with the same `eventId` replaces the stored one. - A stored `Purchase`, `Lead` or `QualifiedLead` tied to one of your campaigns (see `campaign` on each event) counts in `GET /v1/ads/campaign-results` and in ad rules as `sales` and `revenue`, `leads` or `qualified_leads`. 

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
    public class SendEventsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var sendEventsRequest = new SendEventsRequest(); // SendEventsRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  (optional) 

            try
            {
                // Send events to every destination
                SendEvents200Response result = apiInstance.SendEvents(sendEventsRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.SendEvents: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendEventsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send events to every destination
    ApiResponse<SendEvents200Response> response = apiInstance.SendEventsWithHttpInfo(sendEventsRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.SendEventsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sendEventsRequest** | [**SendEventsRequest**](SendEventsRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  | [optional]  |

### Return type

[**SendEvents200Response**](SendEvents200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Events processed. Check each destination for partial failure. |  -  |
| **202** | Stored and queued (&#x60;mode: async&#x60;). &#x60;destinations&#x60; is empty; follow each event on GET /v1/events/{eventId}. |  -  |
| **400** | Invalid body, including a &#x60;test_event_code&#x60; that is not a non-empty string, or &#x60;testCode&#x60; and &#x60;test_event_code&#x60; with different values (&#x60;param: test_event_code&#x60;). |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **409** | Same Idempotency-Key still processing; retry after a short backoff |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadconversiondestination"></a>
# **UpdateAdConversionDestination**
> GetAdConversionDestination200Response UpdateAdConversionDestination (string destinationId, UpdateAdConversionDestinationRequest updateAdConversionDestinationRequest)

Update a conversion destination

Changes a LinkedIn conversion rule's name, value, attribution windows, or turns it on or off.  Partial-update a conversion rule. LinkedIn-only today. Whitelisted fields: `name`, `enabled`, attribution windows, `valueType`, `value`, `attributionType`. The rule's `type` and parent ad account are intentionally not exposed for update. Recreate the rule if those need to change. 

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
    public class UpdateAdConversionDestinationExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var destinationId = "destinationId_example";  // string | 
            var updateAdConversionDestinationRequest = new UpdateAdConversionDestinationRequest(); // UpdateAdConversionDestinationRequest | 

            try
            {
                // Update a conversion destination
                GetAdConversionDestination200Response result = apiInstance.UpdateAdConversionDestination(destinationId, updateAdConversionDestinationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.UpdateAdConversionDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdConversionDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a conversion destination
    ApiResponse<GetAdConversionDestination200Response> response = apiInstance.UpdateAdConversionDestinationWithHttpInfo(destinationId, updateAdConversionDestinationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.UpdateAdConversionDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **destinationId** | **string** |  |  |
| **updateAdConversionDestinationRequest** | [**UpdateAdConversionDestinationRequest**](UpdateAdConversionDestinationRequest.md) |  |  |

### Return type

[**GetAdConversionDestination200Response**](GetAdConversionDestination200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Destination updated (re-fetched canonical state) |  -  |
| **400** | Invalid body or LinkedIn validation failure. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads add-on or LinkedIn reconnect required.  Also returned with code &#x60;ad_account_not_selected&#x60; when the connection has selected ad accounts and the targeted ad account is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection), or use a connection that has it selected. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support updating destinations. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadconversiongoals"></a>
# **UpdateAdConversionGoals**
> UpdateAdConversionGoals200Response UpdateAdConversionGoals (UpdateAdConversionGoalsRequest updateAdConversionGoalsRequest)

Update account conversion goals

Turns bidding on or off for a Google Ads account's default conversion goals, which campaigns using account goals follow.  Sets `biddable` on one or more account-default goals, addressed by category and origin, in one mutate. Campaigns that use account-level goals (`goalConfigLevel: CUSTOMER`) follow the change. Returns the re-read goal list.

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
    public class UpdateAdConversionGoalsExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var updateAdConversionGoalsRequest = new UpdateAdConversionGoalsRequest(); // UpdateAdConversionGoalsRequest | 

            try
            {
                // Update account conversion goals
                UpdateAdConversionGoals200Response result = apiInstance.UpdateAdConversionGoals(updateAdConversionGoalsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.UpdateAdConversionGoals: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdConversionGoalsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update account conversion goals
    ApiResponse<UpdateAdConversionGoals200Response> response = apiInstance.UpdateAdConversionGoalsWithHttpInfo(updateAdConversionGoalsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.UpdateAdConversionGoalsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateAdConversionGoalsRequest** | [**UpdateAdConversionGoalsRequest**](UpdateAdConversionGoalsRequest.md) |  |  |

### Return type

[**UpdateAdConversionGoals200Response**](UpdateAdConversionGoals200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Goals updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;ad_account_not_selected&#x60;. The connection has selected ad accounts (its ad-account scope, set with the dashboard picker or GET /v1/connect/{platform}/ads with adAccountIds) and the targeted ad account is not among them. The connection may not act on it, even though its token can reach it.  &#x60;details&#x60; carries &#x60;accountId&#x60; (the connection), &#x60;adAccountId&#x60; (the refused ad account) and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (adAccountIds replaces the whole selection, so pass the ids already selected plus this one) or use a connection that has it selected. Connections without a selection keep reaching every ad account their token can manage.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | Only available on Google Ads accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateconversionaction"></a>
# **UpdateConversionAction**
> UpdateConversionAction200Response UpdateConversionAction (string actionId, UpdateConversionActionRequest updateConversionActionRequest)

Update a conversion action's settings

Changes a Google Ads conversion action's settings, such as primary or secondary, counting, value and lookback windows, or removes or restores it.  Updates a Google Ads conversion action in one mutate, each field sent written on its own update mask leaf so omitted fields keep their value. Send at least one field.  `primaryForGoal` sets `primary_for_goal`: a primary action counts toward its goal's bidding and the Conversions column; a secondary one is observation-only (All conversions). `countingType`, `category`, the value settings (`defaultValue`, `defaultCurrency`, `alwaysUseDefaultValue`) and the click-through / view-through lookback windows map to the same-named conversion_action fields.  `status: REMOVED` removes the action (Google keeps it, with its history, as REMOVED) and must be sent alone; `status: ENABLED` restores a removed action. Google refuses HIDDEN on website actions, so it is not offered.

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
    public class UpdateConversionActionExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var actionId = "actionId_example";  // string | Google conversion action id
            var updateConversionActionRequest = new UpdateConversionActionRequest(); // UpdateConversionActionRequest | 

            try
            {
                // Update a conversion action's settings
                UpdateConversionAction200Response result = apiInstance.UpdateConversionAction(actionId, updateConversionActionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.UpdateConversionAction: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateConversionActionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a conversion action's settings
    ApiResponse<UpdateConversionAction200Response> response = apiInstance.UpdateConversionActionWithHttpInfo(actionId, updateConversionActionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.UpdateConversionActionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **actionId** | **string** | Google conversion action id |  |
| **updateConversionActionRequest** | [**UpdateConversionActionRequest**](UpdateConversionActionRequest.md) |  |  |

### Return type

[**UpdateConversionAction200Response**](UpdateConversionAction200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Action updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;ad_account_not_selected&#x60;. The connection has selected ad accounts (its ad-account scope, set with the dashboard picker or GET /v1/connect/{platform}/ads with adAccountIds) and the targeted ad account is not among them. The connection may not act on it, even though its token can reach it.  &#x60;details&#x60; carries &#x60;accountId&#x60; (the connection), &#x60;adAccountId&#x60; (the refused ad account) and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (adAccountIds replaces the whole selection, so pass the ids already selected plus this one) or use a connection that has it selected. Connections without a selection keep reaching every ad account their token can manage.  |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | Only available on Google Ads accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateconversiondestination"></a>
# **UpdateConversionDestination**
> GetAdConversionDestination200Response UpdateConversionDestination (string accountId, string destinationId, UpdateConversionDestinationRequest updateConversionDestinationRequest)

Update a conversion destination

The first path of `PATCH /v1/ads/conversions/destinations/{destinationId}` (`updateAdConversionDestination`), which does the same with `accountId` as a parameter. It keeps working. 

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
    public class UpdateConversionDestinationExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var updateConversionDestinationRequest = new UpdateConversionDestinationRequest(); // UpdateConversionDestinationRequest | 

            try
            {
                // Update a conversion destination
                GetAdConversionDestination200Response result = apiInstance.UpdateConversionDestination(accountId, destinationId, updateConversionDestinationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.UpdateConversionDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateConversionDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a conversion destination
    ApiResponse<GetAdConversionDestination200Response> response = apiInstance.UpdateConversionDestinationWithHttpInfo(accountId, destinationId, updateConversionDestinationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.UpdateConversionDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **updateConversionDestinationRequest** | [**UpdateConversionDestinationRequest**](UpdateConversionDestinationRequest.md) |  |  |

### Return type

[**GetAdConversionDestination200Response**](GetAdConversionDestination200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Destination updated (re-fetched canonical state) |  -  |
| **400** | Invalid body or LinkedIn validation failure. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads add-on or LinkedIn reconnect required.  Also returned with code &#x60;ad_account_not_selected&#x60; when the connection has selected ad accounts and the targeted ad account is not among them. &#x60;details&#x60; carries &#x60;accountId&#x60;, &#x60;adAccountId&#x60; and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (GET /v1/connect/{platform}/ads with adAccountIds, which replaces the selection), or use a connection that has it selected. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **405** | Platform does not support updating destinations. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecustomconversiongoal"></a>
# **UpdateCustomConversionGoal**
> UpdateCustomConversionGoal200Response UpdateCustomConversionGoal (string goalId, UpdateCustomConversionGoalRequest updateCustomConversionGoalRequest)

Update a custom conversion goal

Renames a Google Ads custom conversion goal or replaces the conversion actions in it.  Returns the re-read goal. 

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
    public class UpdateCustomConversionGoalExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var goalId = "goalId_example";  // string | Google custom conversion goal id
            var updateCustomConversionGoalRequest = new UpdateCustomConversionGoalRequest(); // UpdateCustomConversionGoalRequest | 

            try
            {
                // Update a custom conversion goal
                UpdateCustomConversionGoal200Response result = apiInstance.UpdateCustomConversionGoal(goalId, updateCustomConversionGoalRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.UpdateCustomConversionGoal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCustomConversionGoalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a custom conversion goal
    ApiResponse<UpdateCustomConversionGoal200Response> response = apiInstance.UpdateCustomConversionGoalWithHttpInfo(goalId, updateCustomConversionGoalRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.UpdateCustomConversionGoalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goalId** | **string** | Google custom conversion goal id |  |
| **updateCustomConversionGoalRequest** | [**UpdateCustomConversionGoalRequest**](UpdateCustomConversionGoalRequest.md) |  |  |

### Return type

[**UpdateCustomConversionGoal200Response**](UpdateCustomConversionGoal200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Custom goal updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;ad_account_not_selected&#x60;. The connection has selected ad accounts (its ad-account scope, set with the dashboard picker or GET /v1/connect/{platform}/ads with adAccountIds) and the targeted ad account is not among them. The connection may not act on it, even though its token can reach it.  &#x60;details&#x60; carries &#x60;accountId&#x60; (the connection), &#x60;adAccountId&#x60; (the refused ad account) and &#x60;selectedAdAccountIds&#x60;.  Fix: add the ad account to the selection (adAccountIds replaces the whole selection, so pass the ids already selected plus this one) or use a connection that has it selected. Connections without a selection keep reaching every ad account their token can manage.  |  -  |
| **404** | Goal not found on this customer, or account unavailable |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | Only available on Google Ads accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateforwardingrule"></a>
# **UpdateForwardingRule**
> CreateForwardingRule201Response UpdateForwardingRule (string ruleId, UpdateForwardingRuleRequest updateForwardingRuleRequest)

Update a forwarding rule

Changes the fields you send and keeps the others. Send `eventNameMap: null` to stop renaming, `valueOverride: { \"mode\": \"original\" }` to send the event's own value again, and `valueCondition: null` to forward whatever the value. `eventValues` replaces the whole map; `null` or `{}` clears it.  `apiSecret` replaces the secret of a rule whose destination needs one, such as a Google Analytics data stream's Measurement Protocol API secret. Events that name the stream in `destinations` on `POST /v1/events` use it too.  Before saving, Zernio sends one hit to Google's validation server; Google does not confirm the secret itself, so check GA4 Realtime after the next events. 

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
    public class UpdateForwardingRuleExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var ruleId = "ruleId_example";  // string | The rule `id`.
            var updateForwardingRuleRequest = new UpdateForwardingRuleRequest(); // UpdateForwardingRuleRequest | 

            try
            {
                // Update a forwarding rule
                CreateForwardingRule201Response result = apiInstance.UpdateForwardingRule(ruleId, updateForwardingRuleRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.UpdateForwardingRule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateForwardingRuleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a forwarding rule
    ApiResponse<CreateForwardingRule201Response> response = apiInstance.UpdateForwardingRuleWithHttpInfo(ruleId, updateForwardingRuleRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.UpdateForwardingRuleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ruleId** | **string** | The rule &#x60;id&#x60;. |  |
| **updateForwardingRuleRequest** | [**UpdateForwardingRuleRequest**](UpdateForwardingRuleRequest.md) |  |  |

### Return type

[**CreateForwardingRule201Response**](CreateForwardingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rule saved. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatetrackingsite"></a>
# **UpdateTrackingSite**
> CreateTrackingSite201Response UpdateTrackingSite (string siteId, UpdateTrackingSiteRequest updateTrackingSiteRequest)

Update a tracking site

Changes the site's name, domains, consent mode, custom subdomain or own-domain path. Send at least one field.  `customHostname` sets a subdomain of the site, such as `t.brand.com`; create the CNAME in `customHostname.dnsRecord`. The snippet switches to it once its status is `active`. `null` removes it.  `proxyPath` serves the tag from a path of the site itself, such as `brand.com/zt`, through a proxy on your server. The response's `proxy.secret` signs what the proxy forwards. `null` removes it.  `googleTagIds` lists the site's own Google tags that the same proxy relays to Google's tag gateway. Load each from its `proxy.googleTags[].src` instead of googletagmanager.com. `null` or an empty list removes them.  `pixels` lists the ad pixels the tag loads for you. In the EEA, UK and Switzerland none loads until the visitor accepts on the site's consent banner. Elsewhere `consentMode` decides. Remove your own copy of each pixel, or it fires twice. `null` or an empty list removes them.  `consentModeBridge` writes the banner's answer into Google Consent Mode v2. The tag reads OneTrust, Cookiebot, Usercentrics, Didomi, Shopify's privacy banner and any IAB TCF v2 banner. 

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
    public class UpdateTrackingSiteExample
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
            var apiInstance = new ConversionsApi(httpClient, config, httpClientHandler);
            var siteId = "siteId_example";  // string | 
            var updateTrackingSiteRequest = new UpdateTrackingSiteRequest(); // UpdateTrackingSiteRequest | 

            try
            {
                // Update a tracking site
                CreateTrackingSite201Response result = apiInstance.UpdateTrackingSite(siteId, updateTrackingSiteRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConversionsApi.UpdateTrackingSite: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTrackingSiteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a tracking site
    ApiResponse<CreateTrackingSite201Response> response = apiInstance.UpdateTrackingSiteWithHttpInfo(siteId, updateTrackingSiteRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConversionsApi.UpdateTrackingSiteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **siteId** | **string** |  |  |
| **updateTrackingSiteRequest** | [**UpdateTrackingSiteRequest**](UpdateTrackingSiteRequest.md) |  |  |

### Return type

[**CreateTrackingSite201Response**](CreateTrackingSite201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated site. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **409** | Another site already uses this subdomain (code &#x60;custom_hostname_taken&#x60;). |  -  |
| **502** | The subdomain could not be registered for now (code &#x60;provider_unavailable&#x60;). Try again. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

