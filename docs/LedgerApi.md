# Zernio.Api.LedgerApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetLedgerBalances**](LedgerApi.md#getledgerbalances) | **GET** /v1/ledger/balances | Get ledger balances |
| [**ListLedgerEntries**](LedgerApi.md#listledgerentries) | **GET** /v1/ledger/entries | List ledger entries |

<a id="getledgerbalances"></a>
# **GetLedgerBalances**
> GetLedgerBalances200Response GetLedgerBalances (string scopeType, string scopeId, string? currency = null)

Get ledger balances

Returns the balance of each bucket (for example accruing, owed, payable) for one ledger scope. A scope owned by another team returns an empty balances object. A profile-scoped key (or a member limited to some profiles) only reads `campaign` and `participant` scopes of campaigns under its profiles; any other scope returns an empty balances object. 

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
    public class GetLedgerBalancesExample
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
            var apiInstance = new LedgerApi(httpClient, config, httpClientHandler);
            var scopeType = "scopeType_example";  // string | Scope type, for example participant or campaign.
            var scopeId = "scopeId_example";  // string | Scope identifier.
            var currency = "\"usd\"";  // string? | Lowercase ISO 4217 currency code. (optional)  (default to "usd")

            try
            {
                // Get ledger balances
                GetLedgerBalances200Response result = apiInstance.GetLedgerBalances(scopeType, scopeId, currency);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LedgerApi.GetLedgerBalances: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetLedgerBalancesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get ledger balances
    ApiResponse<GetLedgerBalances200Response> response = apiInstance.GetLedgerBalancesWithHttpInfo(scopeType, scopeId, currency);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LedgerApi.GetLedgerBalancesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **scopeType** | **string** | Scope type, for example participant or campaign. |  |
| **scopeId** | **string** | Scope identifier. |  |
| **currency** | **string?** | Lowercase ISO 4217 currency code. | [optional] [default to &quot;usd&quot;] |

### Return type

[**GetLedgerBalances200Response**](GetLedgerBalances200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Balances per bucket in cents |  -  |
| **400** | Invalid request |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases. (1) The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key: fix it by creating a key with the group enabled in the dashboard API keys tab and revoking the old one. (2) The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), which is never grantable to restricted keys; the error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; and the fix is a full-access key or the dashboard, never a new restricted key. (3) On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold, so a restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listledgerentries"></a>
# **ListLedgerEntries**
> ListLedgerEntries200Response ListLedgerEntries (string? scopeType = null, string? scopeId = null, string? kind = null, string? referenceType = null, string? referenceId = null, int? limit = null, int? skip = null)

List ledger entries

Lists ledger entries for your team, newest first. Filter by scope (matches either side of the entry), kind, or the reference that caused the entry. A profile-scoped key (or a member limited to some profiles) only sees entries of campaigns under its profiles and of their participants; operator and platform scopes stay hidden from it. 

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
    public class ListLedgerEntriesExample
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
            var apiInstance = new LedgerApi(httpClient, config, httpClientHandler);
            var scopeType = "scopeType_example";  // string? |  (optional) 
            var scopeId = "scopeId_example";  // string? |  (optional) 
            var kind = "accrual";  // string? |  (optional) 
            var referenceType = "referenceType_example";  // string? |  (optional) 
            var referenceId = "referenceId_example";  // string? |  (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List ledger entries
                ListLedgerEntries200Response result = apiInstance.ListLedgerEntries(scopeType, scopeId, kind, referenceType, referenceId, limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LedgerApi.ListLedgerEntries: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListLedgerEntriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List ledger entries
    ApiResponse<ListLedgerEntries200Response> response = apiInstance.ListLedgerEntriesWithHttpInfo(scopeType, scopeId, kind, referenceType, referenceId, limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LedgerApi.ListLedgerEntriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **scopeType** | **string?** |  | [optional]  |
| **scopeId** | **string?** |  | [optional]  |
| **kind** | **string?** |  | [optional]  |
| **referenceType** | **string?** |  | [optional]  |
| **referenceId** | **string?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**ListLedgerEntries200Response**](ListLedgerEntries200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ledger entries |  -  |
| **400** | Invalid request |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases. (1) The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key: fix it by creating a key with the group enabled in the dashboard API keys tab and revoking the old one. (2) The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), which is never grantable to restricted keys; the error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; and the fix is a full-access key or the dashboard, never a new restricted key. (3) On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold, so a restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

