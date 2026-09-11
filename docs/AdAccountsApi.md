# Zernio.Api.AdAccountsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddAccountCallouts**](AdAccountsApi.md#addaccountcallouts) | **POST** /v1/ads/accounts/callouts | Add account callouts |
| [**AddAccountSitelinks**](AdAccountsApi.md#addaccountsitelinks) | **POST** /v1/ads/accounts/sitelinks | Add account sitelinks |
| [**AddAccountStructuredSnippets**](AdAccountsApi.md#addaccountstructuredsnippets) | **POST** /v1/ads/accounts/structured-snippets | Add account snippets |
| [**CreateAdAccount**](AdAccountsApi.md#createadaccount) | **POST** /v1/ads/accounts | Create Meta ad account |
| [**CreateAdNegativeKeywordList**](AdAccountsApi.md#createadnegativekeywordlist) | **POST** /v1/ads/accounts/negative-keyword-lists | Create a negative keyword list |
| [**CreateCustomConversion**](AdAccountsApi.md#createcustomconversion) | **POST** /v1/accounts/{accountId}/custom-conversions | Create custom conversion |
| [**CreateHighDemandPeriod**](AdAccountsApi.md#createhighdemandperiod) | **POST** /v1/ads/high-demand-periods | Schedule a budget increase |
| [**CreateValueRuleSet**](AdAccountsApi.md#createvalueruleset) | **POST** /v1/ads/value-rule-sets | Create a value rule set |
| [**DeleteAdComment**](AdAccountsApi.md#deleteadcomment) | **DELETE** /v1/ads/{adId}/comments/{commentId} | Delete an ad comment |
| [**DeleteAdNegativeKeywordList**](AdAccountsApi.md#deleteadnegativekeywordlist) | **DELETE** /v1/ads/accounts/negative-keyword-lists/{listId} | Delete a negative keyword list |
| [**DeleteValueRuleSet**](AdAccountsApi.md#deletevalueruleset) | **DELETE** /v1/ads/value-rule-sets/{valueRuleSetId} | Delete a value rule set |
| [**GetAdAccountFinance**](AdAccountsApi.md#getadaccountfinance) | **GET** /v1/ads/accounts/finance | Ad account finances |
| [**GetAdComments**](AdAccountsApi.md#getadcomments) | **GET** /v1/ads/{adId}/comments | List comments on an ad |
| [**GetAdNegativeKeywordList**](AdAccountsApi.md#getadnegativekeywordlist) | **GET** /v1/ads/accounts/negative-keyword-lists/{listId} | Get a negative keyword list |
| [**GetAdsActivityLog**](AdAccountsApi.md#getadsactivitylog) | **GET** /v1/ads/activity | Ad account change / audit log |
| [**GetDsaDefaults**](AdAccountsApi.md#getdsadefaults) | **GET** /v1/ads/dsa-defaults | Get ad account DSA defaults |
| [**GetDsaRecommendations**](AdAccountsApi.md#getdsarecommendations) | **GET** /v1/ads/dsa-recommendations | Get DSA recommendations |
| [**GetIosFourteenCampaignLimits**](AdAccountsApi.md#getiosfourteencampaignlimits) | **GET** /v1/ads/ios-fourteen-campaign-limits | Get iOS 14 campaign limits |
| [**GetValueRuleSet**](AdAccountsApi.md#getvalueruleset) | **GET** /v1/ads/value-rule-sets/{valueRuleSetId} | Read a value rule set |
| [**HideAdComment**](AdAccountsApi.md#hideadcomment) | **POST** /v1/ads/{adId}/comments/{commentId}/hide | Hide or unhide an ad comment |
| [**ListAccountCallouts**](AdAccountsApi.md#listaccountcallouts) | **GET** /v1/ads/accounts/callouts | List account callouts |
| [**ListAccountSitelinks**](AdAccountsApi.md#listaccountsitelinks) | **GET** /v1/ads/accounts/sitelinks | List account sitelinks |
| [**ListAccountStructuredSnippets**](AdAccountsApi.md#listaccountstructuredsnippets) | **GET** /v1/ads/accounts/structured-snippets | List account snippets |
| [**ListAdAccounts**](AdAccountsApi.md#listadaccounts) | **GET** /v1/ads/accounts | List ad accounts |
| [**ListAdLabels**](AdAccountsApi.md#listadlabels) | **GET** /v1/ads/labels | Ad labels |
| [**ListAdNegativeKeywordLists**](AdAccountsApi.md#listadnegativekeywordlists) | **GET** /v1/ads/accounts/negative-keyword-lists | List negative keyword lists |
| [**ListAdStudies**](AdAccountsApi.md#listadstudies) | **GET** /v1/ads/studies | A/B tests and lift studies |
| [**ListAdsBusinessCenters**](AdAccountsApi.md#listadsbusinesscenters) | **GET** /v1/ads/business-centers | List TikTok Business Centers |
| [**ListAdsInstagramAccounts**](AdAccountsApi.md#listadsinstagramaccounts) | **GET** /v1/ads/instagram-accounts | List Instagram ad identities |
| [**ListAdvertisableApplications**](AdAccountsApi.md#listadvertisableapplications) | **GET** /v1/ads/advertisable-applications | List advertisable apps |
| [**ListCustomConversions**](AdAccountsApi.md#listcustomconversions) | **GET** /v1/accounts/{accountId}/custom-conversions | List custom conversions |
| [**ListHighDemandPeriods**](AdAccountsApi.md#listhighdemandperiods) | **GET** /v1/ads/high-demand-periods | List high-demand periods |
| [**ListMetaBusinesses**](AdAccountsApi.md#listmetabusinesses) | **GET** /v1/ads/businesses | Businesses list |
| [**ListTikTokAdPixels**](AdAccountsApi.md#listtiktokadpixels) | **GET** /v1/ads/pixels | List TikTok ad pixels |
| [**ListValueRuleSets**](AdAccountsApi.md#listvaluerulesets) | **GET** /v1/ads/value-rule-sets | List value rule sets |
| [**RemoveAccountCallout**](AdAccountsApi.md#removeaccountcallout) | **DELETE** /v1/ads/accounts/callouts | Remove account callout |
| [**RemoveAccountSitelink**](AdAccountsApi.md#removeaccountsitelink) | **DELETE** /v1/ads/accounts/sitelinks | Remove account sitelink |
| [**RemoveAccountStructuredSnippet**](AdAccountsApi.md#removeaccountstructuredsnippet) | **DELETE** /v1/ads/accounts/structured-snippets | Remove account snippet |
| [**ReplaceAdNegativeKeywordListKeywords**](AdAccountsApi.md#replaceadnegativekeywordlistkeywords) | **PUT** /v1/ads/accounts/negative-keyword-lists/{listId}/keywords | Replace negative list keywords |
| [**ReplyToAdComment**](AdAccountsApi.md#replytoadcomment) | **POST** /v1/ads/{adId}/comments/{commentId}/reply | Reply to an ad comment |
| [**UpdateAccountCallouts**](AdAccountsApi.md#updateaccountcallouts) | **PUT** /v1/ads/accounts/callouts | Update account callouts |
| [**UpdateAccountSitelinks**](AdAccountsApi.md#updateaccountsitelinks) | **PUT** /v1/ads/accounts/sitelinks | Update account sitelinks |
| [**UpdateAccountStructuredSnippets**](AdAccountsApi.md#updateaccountstructuredsnippets) | **PUT** /v1/ads/accounts/structured-snippets | Update account snippets |
| [**UpdateAdAccount**](AdAccountsApi.md#updateadaccount) | **PATCH** /v1/ads/accounts | Update ad account settings |
| [**UpdateAdNegativeKeywordList**](AdAccountsApi.md#updateadnegativekeywordlist) | **PUT** /v1/ads/accounts/negative-keyword-lists/{listId} | Rename a negative keyword list |
| [**UpdateValueRuleSet**](AdAccountsApi.md#updatevalueruleset) | **PUT** /v1/ads/value-rule-sets/{valueRuleSetId} | Replace a value rule set |

<a id="addaccountcallouts"></a>
# **AddAccountCallouts**
> AddAccountCallouts201Response AddAccountCallouts (AddAccountCalloutsRequest addAccountCalloutsRequest)

Add account callouts

Creates assets and customer_asset links for this Google customer. Links apply at account level.

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
    public class AddAccountCalloutsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var addAccountCalloutsRequest = new AddAccountCalloutsRequest(); // AddAccountCalloutsRequest | 

            try
            {
                // Add account callouts
                AddAccountCallouts201Response result = apiInstance.AddAccountCallouts(addAccountCalloutsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.AddAccountCallouts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddAccountCalloutsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add account callouts
    ApiResponse<AddAccountCallouts201Response> response = apiInstance.AddAccountCalloutsWithHttpInfo(addAccountCalloutsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.AddAccountCalloutsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **addAccountCalloutsRequest** | [**AddAccountCalloutsRequest**](AddAccountCalloutsRequest.md) |  |  |

### Return type

[**AddAccountCallouts201Response**](AddAccountCallouts201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **201** | Assets created and attached. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="addaccountsitelinks"></a>
# **AddAccountSitelinks**
> AddAccountSitelinks201Response AddAccountSitelinks (AddAccountSitelinksRequest addAccountSitelinksRequest)

Add account sitelinks

Creates assets and customer_asset links for this Google customer. Links apply at account level.

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
    public class AddAccountSitelinksExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var addAccountSitelinksRequest = new AddAccountSitelinksRequest(); // AddAccountSitelinksRequest | 

            try
            {
                // Add account sitelinks
                AddAccountSitelinks201Response result = apiInstance.AddAccountSitelinks(addAccountSitelinksRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.AddAccountSitelinks: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddAccountSitelinksWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add account sitelinks
    ApiResponse<AddAccountSitelinks201Response> response = apiInstance.AddAccountSitelinksWithHttpInfo(addAccountSitelinksRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.AddAccountSitelinksWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **addAccountSitelinksRequest** | [**AddAccountSitelinksRequest**](AddAccountSitelinksRequest.md) |  |  |

### Return type

[**AddAccountSitelinks201Response**](AddAccountSitelinks201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **201** | Assets created and attached. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="addaccountstructuredsnippets"></a>
# **AddAccountStructuredSnippets**
> AddAccountStructuredSnippets201Response AddAccountStructuredSnippets (AddAccountStructuredSnippetsRequest addAccountStructuredSnippetsRequest)

Add account snippets

Creates assets and customer_asset links for this Google customer. Links apply at account level.

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
    public class AddAccountStructuredSnippetsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var addAccountStructuredSnippetsRequest = new AddAccountStructuredSnippetsRequest(); // AddAccountStructuredSnippetsRequest | 

            try
            {
                // Add account snippets
                AddAccountStructuredSnippets201Response result = apiInstance.AddAccountStructuredSnippets(addAccountStructuredSnippetsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.AddAccountStructuredSnippets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddAccountStructuredSnippetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add account snippets
    ApiResponse<AddAccountStructuredSnippets201Response> response = apiInstance.AddAccountStructuredSnippetsWithHttpInfo(addAccountStructuredSnippetsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.AddAccountStructuredSnippetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **addAccountStructuredSnippetsRequest** | [**AddAccountStructuredSnippetsRequest**](AddAccountStructuredSnippetsRequest.md) |  |  |

### Return type

[**AddAccountStructuredSnippets201Response**](AddAccountStructuredSnippets201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **201** | Assets created and attached. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createadaccount"></a>
# **CreateAdAccount**
> CreateAdAccount201Response CreateAdAccount (CreateAdAccountRequest createAdAccountRequest)

Create Meta ad account

Creates a durable Meta ad account in the end user's own business portfolio using their connected Meta Ads token. Requires an active metaads accountId, Ads access, business_management permission and business admin access. Discover portfolios with GET /v1/ads/businesses. System-user tokens may return an empty businesses list; supply the known business ID in that case.  The self-serve account starts without a payment method. The user must add a payment method in Ads Manager before ads can deliver. Zernio cannot add payment methods. Meta may require business verification and limits how many accounts a business can create. Closing an account does not guarantee more capacity. An ad account cannot truly be deleted, even after closing it and removing it from a business.  timezoneId is Meta's numeric ID, not an IANA timezone name. Select it from https://developers.facebook.com/docs/marketing-api/reference/ad-account/timezone-ids/. For example, 1 is America/Los_Angeles. Meta validates supported currencies and IDs. endAdvertiser, mediaAgency and partner default to NONE for the self-serve flow.  The new account is added atomically to an existing scoped ad-account allowlist. Unrestricted connections stay unrestricted. Reconnecting the same Meta identity preserves this scope unless a caller explicitly replaces it. Discovery is nudged immediately. Use the returned adAccountId with the existing ads endpoints.  This operation is not idempotent and Zernio never automatically retries it. Unknown body fields are rejected. No validateOnly or dry-run option is supported. After a timeout or a 502 with details.creationStatus=unknown, check the business in Ads Manager before attempting another creation. A 201 with connectionUpdated=false means the account exists but needs reconnecting with adAccountIds containing the returned ID and the previous scoped IDs via GET /v1/connect/facebook/ads. Do not repeat the create call. 

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
    public class CreateAdAccountExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var createAdAccountRequest = new CreateAdAccountRequest(); // CreateAdAccountRequest | 

            try
            {
                // Create Meta ad account
                CreateAdAccount201Response result = apiInstance.CreateAdAccount(createAdAccountRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.CreateAdAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Meta ad account
    ApiResponse<CreateAdAccount201Response> response = apiInstance.CreateAdAccountWithHttpInfo(createAdAccountRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.CreateAdAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createAdAccountRequest** | [**CreateAdAccountRequest**](CreateAdAccountRequest.md) |  |  |

### Return type

[**CreateAdAccount201Response**](CreateAdAccount201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **201** | Ad account created. Check connectionUpdated and payment instructions. |  -  |
| **400** | Invalid input or Meta rejection. details.reason identifies creation_limit, business_verification_required, unsupported_currency, unsupported_timezone or business_unavailable when recognized. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access denied or Meta permission missing. details.reason may be business_management_required, business_admin_required or business_access_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **502** | Creation outcome unknown. Check Ads Manager before repeating this non-idempotent request. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createadnegativekeywordlist"></a>
# **CreateAdNegativeKeywordList**
> CreateAdNegativeKeywordList201Response CreateAdNegativeKeywordList (CreateAdNegativeKeywordListRequest createAdNegativeKeywordListRequest)

Create a negative keyword list

Creates one Google Ads shared negative keyword list with optional initial keywords in a single atomic mutation. Daily quota is reserved for every mutate item, so large batches may return 429 before any change. This operation is not idempotent. The list is not attached to any campaign.

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
    public class CreateAdNegativeKeywordListExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var createAdNegativeKeywordListRequest = new CreateAdNegativeKeywordListRequest(); // CreateAdNegativeKeywordListRequest | 

            try
            {
                // Create a negative keyword list
                CreateAdNegativeKeywordList201Response result = apiInstance.CreateAdNegativeKeywordList(createAdNegativeKeywordListRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.CreateAdNegativeKeywordList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdNegativeKeywordListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a negative keyword list
    ApiResponse<CreateAdNegativeKeywordList201Response> response = apiInstance.CreateAdNegativeKeywordListWithHttpInfo(createAdNegativeKeywordListRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.CreateAdNegativeKeywordListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createAdNegativeKeywordListRequest** | [**CreateAdNegativeKeywordListRequest**](CreateAdNegativeKeywordListRequest.md) |  |  |

### Return type

[**CreateAdNegativeKeywordList201Response**](CreateAdNegativeKeywordList201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successful response. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access and permission to the selected account are required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | Ambiguous campaign or account selection. Use a profile-scoped key. A list still attached to a campaign may also be rejected by Google. The account may also be inactive or need reconnection (code ads_connection_required). Reconnect it and read GET /v1/accounts for its current ID before retrying. |  -  |
| **422** | Google Ads connection is missing or unavailable. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Available only on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcustomconversion"></a>
# **CreateCustomConversion**
> CustomConversionResult CreateCustomConversion (string accountId, CreateCustomConversionRequest createCustomConversionRequest)

Create custom conversion

Provision the Meta custom conversion an ads flow optimises toward, and hand back the `customConversionId` for `promotedObject.customConversionId` on POST /v1/ads/create. Removes the manual \"create it in Ads Manager first\" step.  **Reuse is ours, not Meta's.** Meta's create is not idempotent, so a retried request would otherwise mint a duplicate carrying none of the original's optimisation history. A non-archived conversion with the same `name` on the same `pixelId` is returned instead of created, with `reused: true` and a 200 rather than a 201.  `rule` is forwarded verbatim in Meta's own grammar (e.g. `{\"url\": {\"i_contains\": \"thank-you\"}}`); Meta validates it and rejects a malformed one with \"A conversion rule is required at creation time\".

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
    public class CreateCustomConversionExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Meta ads SocialAccount id.
            var createCustomConversionRequest = new CreateCustomConversionRequest(); // CreateCustomConversionRequest | 

            try
            {
                // Create custom conversion
                CustomConversionResult result = apiInstance.CreateCustomConversion(accountId, createCustomConversionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.CreateCustomConversion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCustomConversionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create custom conversion
    ApiResponse<CustomConversionResult> response = apiInstance.CreateCustomConversionWithHttpInfo(accountId, createCustomConversionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.CreateCustomConversionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Meta ads SocialAccount id. |  |
| **createCustomConversionRequest** | [**CreateCustomConversionRequest**](CreateCustomConversionRequest.md) |  |  |

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
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **200** | An existing custom conversion was reused |  -  |
| **201** | Custom conversion created |  -  |
| **400** | Invalid input, or Meta rejected the conversion (bad rule, per-account cap reached) |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the token lacks the ads permissions. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createhighdemandperiod"></a>
# **CreateHighDemandPeriod**
> CreateHighDemandPeriod201Response CreateHighDemandPeriod (CreateHighDemandPeriodRequest createHighDemandPeriodRequest)

Schedule a budget increase

Pre-schedule a temporary budget increase (Black Friday, a launch, a sale) instead of editing the budget by hand on the day. Same target rule as the GET: exactly one of `campaignId` / `adSetId`.  Two Meta constraints worth knowing before you call it. `timeStart` / `timeEnd` must fall on a 15-minute boundary, and a campaign cannot mix `ABSOLUTE` and `MULTIPLIER` across its schedules; the second type is rejected with \"Can't mix your budget scaling selection\". Window rules (must sit inside the campaign's run dates, minimum lead time, no overlap) are Meta's and its message is forwarded verbatim.

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
    public class CreateHighDemandPeriodExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var createHighDemandPeriodRequest = new CreateHighDemandPeriodRequest(); // CreateHighDemandPeriodRequest | 

            try
            {
                // Schedule a budget increase
                CreateHighDemandPeriod201Response result = apiInstance.CreateHighDemandPeriod(createHighDemandPeriodRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.CreateHighDemandPeriod: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateHighDemandPeriodWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule a budget increase
    ApiResponse<CreateHighDemandPeriod201Response> response = apiInstance.CreateHighDemandPeriodWithHttpInfo(createHighDemandPeriodRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.CreateHighDemandPeriodWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createHighDemandPeriodRequest** | [**CreateHighDemandPeriodRequest**](CreateHighDemandPeriodRequest.md) |  |  |

### Return type

[**CreateHighDemandPeriod201Response**](CreateHighDemandPeriod201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **201** | Budget schedule created |  -  |
| **400** | Invalid input, or Meta rejected the schedule |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createvalueruleset"></a>
# **CreateValueRuleSet**
> CreateValueRuleSet201Response CreateValueRuleSet (CreateValueRuleSetRequest createValueRuleSetRequest)

Create a value rule set

Creates a value rule set on the ad account (Meta's `POST /act_X/value_rule_set`). Attach the returned id to an ad set with `valueRuleSetId` on `POST /v1/ads/create` or `PUT /v1/ads/ad-sets/{adSetId}`.  **Rule order is semantic**: rules are evaluated in array order and only the first matching rule adjusts the bid for an overlapping audience.  `adjustValue` is an unsigned magnitude in percent; the direction lives in `adjustSign`. `INCREASE` accepts 1-1000, `DECREASE` accepts 1-90. There is no signed field and 0 is out of range.  `criteriaValueTypes` is positionally paired with `criteriaValues` (same length, same order). Every type is the literal `\"NONE\"` except on `LOCATION`, which uses `LOCATION_COUNTRY` / `LOCATION_REGION` / `LOCATION_CITY` / `LOCATION_COMSCORE_MARKET` and may mix them within one criterion. Location values are Targeting-Search keys: a two-letter country code for `LOCATION_COUNTRY`, a numeric key for the rest.  `LOCATION_DMA` was replaced by `LOCATION_COMSCORE_MARKET` on 2026-06-22 and rules using DMAs are no longer active, so this API rejects it.  `AUDIENCE_LABEL` values (e.g. `HIGH_VALUE`) are applied to a Custom Audience in Ads Manager. There is no API to provision them, so label strings are passed through unvalidated and a typo produces a rule that never fires.  Ads Manager turns a rule set read-only (this API stays editable) when a rule uses more than 2 criteria, a custom age range, or the placements `FB_MARKETPLACE`, `FB_SEARCH`, `FB_VIDEO` or `IG_EXPLORE`.  Limits: 6 rule sets per ad account, 10 rules per set, 4 criteria per rule. The per-account cap is enforced by Meta, not here.

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
    public class CreateValueRuleSetExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var createValueRuleSetRequest = new CreateValueRuleSetRequest(); // CreateValueRuleSetRequest | 

            try
            {
                // Create a value rule set
                CreateValueRuleSet201Response result = apiInstance.CreateValueRuleSet(createValueRuleSetRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.CreateValueRuleSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateValueRuleSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a value rule set
    ApiResponse<CreateValueRuleSet201Response> response = apiInstance.CreateValueRuleSetWithHttpInfo(createValueRuleSetRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.CreateValueRuleSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createValueRuleSetRequest** | [**CreateValueRuleSetRequest**](CreateValueRuleSetRequest.md) |  |  |

### Return type

[**CreateValueRuleSet201Response**](CreateValueRuleSet201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **201** | Value rule set created |  -  |
| **400** | Invalid input, or Meta rejected the create (per-account rule-set cap, ineligible criteria, or an account that is not enabled for value rules) |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteadcomment"></a>
# **DeleteAdComment**
> ReplyToAdComment200Response DeleteAdComment (string adId, string commentId, DateOnly? since = null, DateOnly? until = null)

Delete an ad comment

Delete your own TikTok ad comment or reply. TikTok must return can_delete=true for the comment. Other users' comments can be hidden instead.  Unknown identity and video item fields are resolved only when needed for this action, then persisted for reuse. Comment-specific fields take precedence. If TikTok no longer returns the ad needed to resolve identity, 404 ad_not_found directs you to check deletion or archival in TikTok Ads Manager. Listing can still succeed. Unsupported or unavailable identity returns 403 feature_not_available. Denied access to ad details returns 403 insufficient_permissions with reconnect guidance and the upstream platformError.  Requires Ads access. The ad is resolved within the caller's accessible profiles. Before moderation, Zernio verifies that the comment belongs to this ad using TikTok's ad-group comment listing. The default search window is the last 30 days. Use since/until for older comments, with at most 30 days between the dates. Lookups scan at most 2,000 ad-group comments; narrow the date window if exceeded. Meta returns 501 feature_not_available with guidance to use the existing inbox comment endpoints and the account/post IDs from GET /v1/ads/{adId}/comments. 

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
    public class DeleteAdCommentExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Internal Zernio ad ID or indexed platform ad ID.
            var commentId = "commentId_example";  // string | TikTok comment ID from the ad comment listing.
            var since = DateOnly.Parse("2013-10-20");  // DateOnly? | Start date of the comment lookup window. Defaults to 30 days before until. (optional) 
            var until = DateOnly.Parse("2013-10-20");  // DateOnly? | End date of the comment lookup window. Defaults to today in UTC. (optional) 

            try
            {
                // Delete an ad comment
                ReplyToAdComment200Response result = apiInstance.DeleteAdComment(adId, commentId, since, until);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.DeleteAdComment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAdCommentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete an ad comment
    ApiResponse<ReplyToAdComment200Response> response = apiInstance.DeleteAdCommentWithHttpInfo(adId, commentId, since, until);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.DeleteAdCommentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Internal Zernio ad ID or indexed platform ad ID. |  |
| **commentId** | **string** | TikTok comment ID from the ad comment listing. |  |
| **since** | **DateOnly?** | Start date of the comment lookup window. Defaults to 30 days before until. | [optional]  |
| **until** | **DateOnly?** | End date of the comment lookup window. Defaults to today in UTC. | [optional]  |

### Return type

[**ReplyToAdComment200Response**](ReplyToAdComment200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comment action completed. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access, own-comment deletion or supported identity is unavailable (feature_not_available), or TikTok denies ad-detail access (insufficient_permissions). |  -  |
| **404** | Ad is inaccessible or unavailable on TikTok for identity resolution (ad_not_found), or the comment was not found on this ad in the selected date window (resource_not_found). |  -  |
| **422** | TikTok Ads connection is unavailable. |  -  |
| **501** | Moderation on this route supports TikTok. Use the inbox comment routes for Meta. |  -  |
| **502** | TikTok rejected the request or was unavailable. Inspect platformError for its code and message. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteadnegativekeywordlist"></a>
# **DeleteAdNegativeKeywordList**
> DeleteAdNegativeKeywordList200Response DeleteAdNegativeKeywordList (string listId, string accountId, string? customerId = null, string? platform = null)

Delete a negative keyword list

Removes the Google shared negative keyword list. Detach it from all campaigns first; an in-use list is rejected. Only NEGATIVE_KEYWORDS shared sets are supported.

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
    public class DeleteAdNegativeKeywordListExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var listId = "listId_example";  // string | 
            var accountId = "accountId_example";  // string | 
            var customerId = "customerId_example";  // string? |  (optional) 
            var platform = "facebook";  // string? |  (optional) 

            try
            {
                // Delete a negative keyword list
                DeleteAdNegativeKeywordList200Response result = apiInstance.DeleteAdNegativeKeywordList(listId, accountId, customerId, platform);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.DeleteAdNegativeKeywordList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAdNegativeKeywordListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a negative keyword list
    ApiResponse<DeleteAdNegativeKeywordList200Response> response = apiInstance.DeleteAdNegativeKeywordListWithHttpInfo(listId, accountId, customerId, platform);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.DeleteAdNegativeKeywordListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listId** | **string** |  |  |
| **accountId** | **string** |  |  |
| **customerId** | **string?** |  | [optional]  |
| **platform** | **string?** |  | [optional]  |

### Return type

[**DeleteAdNegativeKeywordList200Response**](DeleteAdNegativeKeywordList200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access and permission to the selected account are required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | Ambiguous campaign or account selection. Use a profile-scoped key. A list still attached to a campaign may also be rejected by Google. The account may also be inactive or need reconnection (code ads_connection_required). Reconnect it and read GET /v1/accounts for its current ID before retrying. |  -  |
| **422** | Google Ads connection is missing or unavailable. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Available only on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletevalueruleset"></a>
# **DeleteValueRuleSet**
> DeleteValueRuleSet200Response DeleteValueRuleSet (string valueRuleSetId, string accountId)

Delete a value rule set

Deletes the rule set (Meta's `POST /{value-rule-set-id}/delete_rule_set`, a custom action edge rather than an HTTP DELETE on its side). Ad sets pointing at it are not modified here; detach them first with `valueRulesApplied: false` on `PUT /v1/ads/ad-sets/{adSetId}`.

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
    public class DeleteValueRuleSetExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var valueRuleSetId = "valueRuleSetId_example";  // string | Platform value rule set id.
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.

            try
            {
                // Delete a value rule set
                DeleteValueRuleSet200Response result = apiInstance.DeleteValueRuleSet(valueRuleSetId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.DeleteValueRuleSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteValueRuleSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a value rule set
    ApiResponse<DeleteValueRuleSet200Response> response = apiInstance.DeleteValueRuleSetWithHttpInfo(valueRuleSetId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.DeleteValueRuleSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **valueRuleSetId** | **string** | Platform value rule set id. |  |
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |

### Return type

[**DeleteValueRuleSet200Response**](DeleteValueRuleSet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **200** | Value rule set deleted |  -  |
| **400** | Invalid input, or Meta rejected the delete. A bad id comes back as GraphMethodException code 100 / subcode 33, which reads like a permission error rather than a 404. |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadaccountfinance"></a>
# **GetAdAccountFinance**
> GetAdAccountFinance200Response GetAdAccountFinance (string accountId, string adAccountId)

Ad account finances

Finances of one Meta ad account: prepaid `balance`, lifetime `amountSpent`, account `spendCap` (null = no cap) and the `fundingSource`. Money values are converted from Meta's minor units to whole units of `currency`.

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
    public class GetAdAccountFinanceExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).

            try
            {
                // Ad account finances
                GetAdAccountFinance200Response result = apiInstance.GetAdAccountFinance(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetAdAccountFinance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdAccountFinanceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad account finances
    ApiResponse<GetAdAccountFinance200Response> response = apiInstance.GetAdAccountFinanceWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetAdAccountFinanceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |

### Return type

[**GetAdAccountFinance200Response**](GetAdAccountFinance200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **200** | Account finances |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadcomments"></a>
# **GetAdComments**
> GetAdComments200Response GetAdComments (string adId, string? placement = null, int? limit = null, DateOnly? since = null, DateOnly? until = null, string? cursor = null)

List comments on an ad

Returns comments on an ad's underlying creative post. Useful for moderating or analyzing engagement on dark posts (ad creatives that never went live organically), which the regular GET /v1/inbox/comments/{postId} endpoint cannot serve because dark posts are not in Zernio's post database.  An ad that runs on both Facebook feed and Instagram feed has two separate underlying posts with separate comment threads (the creative's effective_object_story_id and effective_instagram_media_id). Use the `placement` query param to pick one; with no param the Instagram side is returned when it exists, otherwise Facebook. The identifiers are read from the ad record (persisted during sync) with a Marketing-API fallback for ads that predate the field.  For Instagram-placed comments, the Instagram account that runs the ad must be connected to Zernio, because those comments are read through that account's token. If no connected Instagram account on the profile can read the ad's media, the call returns ads_connection_required (the Facebook side, if any, is still readable via ?placement=facebook).  TikTok uses the connected TikTok Ads advertiser token and supports both paid video ads and Spark Ads. `since` and `until` select a date window of at most 30 days; the default is the last 30 days. TikTok searches by ad group, so Zernio filters each page to this ad. A page can be empty while `pagination.hasMore` is true. Reuse `pagination.cursor` with the same `limit`; the cursor retains the date window. `placement` is Meta-only and returns a 400 for TikTok. Listing needs no identity or video item ID. When the ad group is stored, each page makes one comment-list call and no ad-detail lookup, including for external ads that TikTok no longer returns from ad details. `meta.tiktokItemId: null` does not prevent listing. If the ad group is missing, Zernio fetches ad details; unavailable details return 404 ad_not_found, and no ad group returns 400 ad_not_commentable.  TikTok returns replies as separate comments with `parentId`; nested reply fetching is not supported. `canReply` requires a first-level comment, comment-management permission, a video item ID and a supported TT_USER or CUSTOMIZED_USER identity. `canDelete` requires TikTok's own-comment deletion capability, a video item ID and a supported identity. Both flags are false when identity or item is unknown. Listing uses stored and comment-specific fields without fetching identity. A direct reply or delete request can lazily resolve missing fields and succeed even after a false flag. `canHide` is true because visibility changes need only advertiser and comment IDs. `canLike` is false. Use the ad comment reply, hide and delete operations below to moderate TikTok comments. Other platforms return feature_not_available.  Requires the Ads add-on. Response shape matches GET /v1/inbox/comments/{postId}.  The `{adId}` path segment accepts any identifier dialect Zernio indexes for the ad: Zernio internal `_id` (24-char hex), the numeric `platformAdId` (the value shipped in `comment.received` webhooks as `comment.ad.id`), or the creative's `effective_object_story_id` / `effective_instagram_media_id`. Caller doesn't need a translation step. 

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
    public class GetAdCommentsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Internal Zernio ad ID or indexed platform ad/post ID.
            var placement = "facebook";  // string? | Which side of the ad to return comments for. Omit to default to the Instagram side when present, else Facebook. Returns ad_not_commentable if the ad has no such placement. (optional) 
            var limit = 25;  // int? |  (optional)  (default to 25)
            var since = DateOnly.Parse("2013-10-20");  // DateOnly? | TikTok-only start date. Defaults to 30 days before until. Maximum window is 30 days. (optional) 
            var until = DateOnly.Parse("2013-10-20");  // DateOnly? | TikTok-only end date. Defaults to today in UTC. (optional) 
            var cursor = "cursor_example";  // string? | Pagination cursor from a previous response. (optional) 

            try
            {
                // List comments on an ad
                GetAdComments200Response result = apiInstance.GetAdComments(adId, placement, limit, since, until, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetAdComments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdCommentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List comments on an ad
    ApiResponse<GetAdComments200Response> response = apiInstance.GetAdCommentsWithHttpInfo(adId, placement, limit, since, until, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetAdCommentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Internal Zernio ad ID or indexed platform ad/post ID. |  |
| **placement** | **string?** | Which side of the ad to return comments for. Omit to default to the Instagram side when present, else Facebook. Returns ad_not_commentable if the ad has no such placement. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **since** | **DateOnly?** | TikTok-only start date. Defaults to 30 days before until. Maximum window is 30 days. | [optional]  |
| **until** | **DateOnly?** | TikTok-only end date. Defaults to today in UTC. | [optional]  |
| **cursor** | **string?** | Pagination cursor from a previous response. | [optional]  |

### Return type

[**GetAdComments200Response**](GetAdComments200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comments on the ad. |  -  |
| **400** | Invalid ad ID format, or the ad&#39;s creative format does not expose a commentable underlying post (code ad_not_commentable).  |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (legacy plans need the Ads add-on; included by default on usage-based plans), or ad platform is not Meta or TikTok (code feature_not_available). |  -  |
| **404** | Resource not found |  -  |
| **422** | Ads account token unavailable, or (for Instagram-placed ads) no connected Instagram account on the profile can read the ad&#39;s media (code ads_connection_required).  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadnegativekeywordlist"></a>
# **GetAdNegativeKeywordList**
> GetAdNegativeKeywordList200Response GetAdNegativeKeywordList (string listId, string accountId, string? customerId = null, string? platform = null)

Get a negative keyword list

Google Ads shared negative keyword lists (shared_set type NEGATIVE_KEYWORDS). Reads are cached for 10 minutes; quota exhaustion may return the last successful result for up to 7 days with stale=true. Customer selection is limited to this connection and its account scope. Includes the keywords and their criterion ids.

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
    public class GetAdNegativeKeywordListExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var listId = "listId_example";  // string | 
            var accountId = "accountId_example";  // string | 
            var customerId = "customerId_example";  // string? |  (optional) 
            var platform = "facebook";  // string? |  (optional) 

            try
            {
                // Get a negative keyword list
                GetAdNegativeKeywordList200Response result = apiInstance.GetAdNegativeKeywordList(listId, accountId, customerId, platform);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetAdNegativeKeywordList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdNegativeKeywordListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a negative keyword list
    ApiResponse<GetAdNegativeKeywordList200Response> response = apiInstance.GetAdNegativeKeywordListWithHttpInfo(listId, accountId, customerId, platform);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetAdNegativeKeywordListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listId** | **string** |  |  |
| **accountId** | **string** |  |  |
| **customerId** | **string?** |  | [optional]  |
| **platform** | **string?** |  | [optional]  |

### Return type

[**GetAdNegativeKeywordList200Response**](GetAdNegativeKeywordList200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access and permission to the selected account are required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | Ambiguous campaign or account selection. Use a profile-scoped key. A list still attached to a campaign may also be rejected by Google. The account may also be inactive or need reconnection (code ads_connection_required). Reconnect it and read GET /v1/accounts for its current ID before retrying. |  -  |
| **422** | Google Ads connection is missing or unavailable. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Available only on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadsactivitylog"></a>
# **GetAdsActivityLog**
> GetAdsActivityLog200Response GetAdsActivityLog (string accountId, string adAccountId, DateOnly? since = null, DateOnly? until = null, string? objectId = null, int? limit = null, string? after = null)

Ad account change / audit log

Account-level audit log from Meta's `/act_X/activities`: who changed what and when (creates, edits, status flips, budget changes...) with Meta's translated event names and the structured before/after in `extra_data`. Rows are returned verbatim. Meta has no server-side per-object filter on this edge, so `objectId` filters the returned page client-side (combine with paging to walk history for one campaign/ad set/ad).

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
    public class GetAdsActivityLogExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).
            var since = DateOnly.Parse("2013-10-20");  // DateOnly? | Start of range (YYYY-MM-DD). (optional) 
            var until = DateOnly.Parse("2013-10-20");  // DateOnly? | End of range (YYYY-MM-DD). (optional) 
            var objectId = "objectId_example";  // string? | Client-side filter to one Meta object id (campaign, ad set or ad). (optional) 
            var limit = 50;  // int? | Rows per page (optional)  (default to 50)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // Ad account change / audit log
                GetAdsActivityLog200Response result = apiInstance.GetAdsActivityLog(accountId, adAccountId, since, until, objectId, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetAdsActivityLog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdsActivityLogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad account change / audit log
    ApiResponse<GetAdsActivityLog200Response> response = apiInstance.GetAdsActivityLogWithHttpInfo(accountId, adAccountId, since, until, objectId, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetAdsActivityLogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |
| **since** | **DateOnly?** | Start of range (YYYY-MM-DD). | [optional]  |
| **until** | **DateOnly?** | End of range (YYYY-MM-DD). | [optional]  |
| **objectId** | **string?** | Client-side filter to one Meta object id (campaign, ad set or ad). | [optional]  |
| **limit** | **int?** | Rows per page | [optional] [default to 50] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**GetAdsActivityLog200Response**](GetAdsActivityLog200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **200** | Activity rows (raw Meta shape) |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getdsadefaults"></a>
# **GetDsaDefaults**
> UpdateAdAccount200Response GetDsaDefaults (string accountId, string adAccountId)

Get ad account DSA defaults

Returns the default DSA beneficiary and payor currently set on a Meta ad account, whether they were set via `PATCH /v1/ads/accounts` or in Meta Ads Manager. Fields are omitted when no default is configured. Meta accounts only. 

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
    public class GetDsaDefaultsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Account ID (metaads, or a facebook/instagram posting account)
            var adAccountId = "adAccountId_example";  // string | Meta ad account ID (act_...)

            try
            {
                // Get ad account DSA defaults
                UpdateAdAccount200Response result = apiInstance.GetDsaDefaults(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetDsaDefaults: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDsaDefaultsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get ad account DSA defaults
    ApiResponse<UpdateAdAccount200Response> response = apiInstance.GetDsaDefaultsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetDsaDefaultsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Account ID (metaads, or a facebook/instagram posting account) |  |
| **adAccountId** | **string** | Meta ad account ID (act_...) |  |

### Return type

[**UpdateAdAccount200Response**](UpdateAdAccount200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Current DSA defaults (empty object when none are set) |  -  |
| **400** | Non-Meta adAccountId |  -  |
| **401** | Unauthorized |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getdsarecommendations"></a>
# **GetDsaRecommendations**
> GetDsaRecommendations200Response GetDsaRecommendations (string accountId, string adAccountId)

Get DSA recommendations

Returns Meta's suggested beneficiary/payor names for an ad account, derived by Meta from the account's recent activity. Useful for prefilling `dsaBeneficiary`/`dsaPayor` inputs, or the defaults sent to `PATCH /v1/ads/accounts`, in your own UI.  Meta returns a single flat list. Entries are not labeled as beneficiary or payor, and since these are legal disclosures Zernio never applies them automatically: let your user pick the right entity. The list may be empty for accounts with little activity. Meta accounts only. 

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
    public class GetDsaRecommendationsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Account ID (metaads, or a facebook/instagram posting account)
            var adAccountId = "adAccountId_example";  // string | Meta ad account ID (act_...)

            try
            {
                // Get DSA recommendations
                GetDsaRecommendations200Response result = apiInstance.GetDsaRecommendations(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetDsaRecommendations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDsaRecommendationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get DSA recommendations
    ApiResponse<GetDsaRecommendations200Response> response = apiInstance.GetDsaRecommendationsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetDsaRecommendationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Account ID (metaads, or a facebook/instagram posting account) |  |
| **adAccountId** | **string** | Meta ad account ID (act_...) |  |

### Return type

[**GetDsaRecommendations200Response**](GetDsaRecommendations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Suggested DSA strings (may be empty when Meta has no recommendations) |  -  |
| **400** | Non-Meta adAccountId |  -  |
| **401** | Unauthorized |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getiosfourteencampaignlimits"></a>
# **GetIosFourteenCampaignLimits**
> GetIosFourteenCampaignLimits200Response GetIosFourteenCampaignLimits (string accountId, string adAccountId, string applicationId)

Get iOS 14 campaign limits

Reads Meta iOS 14 campaign limits for an application on an ad account. applicationId is sent as Meta app_id. This read does not establish that the application is configured for iOS promotion.

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
    public class GetIosFourteenCampaignLimitsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio Meta Ads or Facebook SocialAccount ID.
            var adAccountId = "adAccountId_example";  // string | Meta ad account ID including the act_ prefix.
            var applicationId = "applicationId_example";  // string | Meta application ID from advertisable-applications.

            try
            {
                // Get iOS 14 campaign limits
                GetIosFourteenCampaignLimits200Response result = apiInstance.GetIosFourteenCampaignLimits(accountId, adAccountId, applicationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetIosFourteenCampaignLimits: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetIosFourteenCampaignLimitsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get iOS 14 campaign limits
    ApiResponse<GetIosFourteenCampaignLimits200Response> response = apiInstance.GetIosFourteenCampaignLimitsWithHttpInfo(accountId, adAccountId, applicationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetIosFourteenCampaignLimitsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio Meta Ads or Facebook SocialAccount ID. |  |
| **adAccountId** | **string** | Meta ad account ID including the act_ prefix. |  |
| **applicationId** | **string** | Meta application ID from advertisable-applications. |  |

### Return type

[**GetIosFourteenCampaignLimits200Response**](GetIosFourteenCampaignLimits200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Application campaign limits. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The account or Meta asset is not accessible. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **501** | Only supported on Meta Ads and Facebook accounts. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getvalueruleset"></a>
# **GetValueRuleSet**
> GetValueRuleSet200Response GetValueRuleSet (string valueRuleSetId, string accountId)

Read a value rule set

Reads one value rule set including every nested rule id and criterion id. This is step one of any edit: `PUT` is a full replace, so you need the ids before you can keep the objects you are not changing.  Meta's own read returns `GENDER` values lowercase (`\"male\"`) while writes require `\"MALE\"`. Values are passed through untouched, so never case-compare a stored rule against a fetched one.

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
    public class GetValueRuleSetExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var valueRuleSetId = "valueRuleSetId_example";  // string | Platform value rule set id.
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.

            try
            {
                // Read a value rule set
                GetValueRuleSet200Response result = apiInstance.GetValueRuleSet(valueRuleSetId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetValueRuleSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetValueRuleSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read a value rule set
    ApiResponse<GetValueRuleSet200Response> response = apiInstance.GetValueRuleSetWithHttpInfo(valueRuleSetId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetValueRuleSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **valueRuleSetId** | **string** | Platform value rule set id. |  |
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |

### Return type

[**GetValueRuleSet200Response**](GetValueRuleSet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **200** | Value rule set |  -  |
| **400** | Invalid input, or Meta rejected the read. A bad id comes back as GraphMethodException code 100 / subcode 33, which cannot be told apart from a permission problem. |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="hideadcomment"></a>
# **HideAdComment**
> HideAdComment200Response HideAdComment (string adId, string commentId, HideAdCommentRequest hideAdCommentRequest, DateOnly? since = null, DateOnly? until = null)

Hide or unhide an ad comment

Hide or restore a TikTok ad comment. Send hidden=true to hide it or hidden=false to make it public again. Identity and video item ID are not required; no identity lookup is performed.  Requires Ads access. The ad is resolved within the caller's accessible profiles. Before moderation, Zernio verifies that the comment belongs to this ad using TikTok's ad-group comment listing. The default search window is the last 30 days. Use since/until for older comments, with at most 30 days between the dates. Lookups scan at most 2,000 ad-group comments; narrow the date window if exceeded. Meta returns 501 feature_not_available with guidance to use the existing inbox comment endpoints and the account/post IDs from GET /v1/ads/{adId}/comments. 

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
    public class HideAdCommentExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Internal Zernio ad ID or indexed platform ad ID.
            var commentId = "commentId_example";  // string | TikTok comment ID from the ad comment listing.
            var hideAdCommentRequest = new HideAdCommentRequest(); // HideAdCommentRequest | 
            var since = DateOnly.Parse("2013-10-20");  // DateOnly? | Start date of the comment lookup window. Defaults to 30 days before until. (optional) 
            var until = DateOnly.Parse("2013-10-20");  // DateOnly? | End date of the comment lookup window. Defaults to today in UTC. (optional) 

            try
            {
                // Hide or unhide an ad comment
                HideAdComment200Response result = apiInstance.HideAdComment(adId, commentId, hideAdCommentRequest, since, until);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.HideAdComment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the HideAdCommentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Hide or unhide an ad comment
    ApiResponse<HideAdComment200Response> response = apiInstance.HideAdCommentWithHttpInfo(adId, commentId, hideAdCommentRequest, since, until);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.HideAdCommentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Internal Zernio ad ID or indexed platform ad ID. |  |
| **commentId** | **string** | TikTok comment ID from the ad comment listing. |  |
| **hideAdCommentRequest** | [**HideAdCommentRequest**](HideAdCommentRequest.md) |  |  |
| **since** | **DateOnly?** | Start date of the comment lookup window. Defaults to 30 days before until. | [optional]  |
| **until** | **DateOnly?** | End date of the comment lookup window. Defaults to today in UTC. | [optional]  |

### Return type

[**HideAdComment200Response**](HideAdComment200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comment action completed. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access or the required TikTok comment capability is unavailable. |  -  |
| **404** | Ad is inaccessible or the comment was not found on this ad in the selected date window. |  -  |
| **422** | TikTok Ads connection is unavailable. |  -  |
| **501** | Moderation on this route supports TikTok. Use the inbox comment routes for Meta. |  -  |
| **502** | TikTok rejected the request or was unavailable. Inspect platformError for its code and message. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listaccountcallouts"></a>
# **ListAccountCallouts**
> ListAccountCallouts200Response ListAccountCallouts (string accountId, string? customerId = null)

List account callouts

Lists directly attached Google assets. Fresh reads are cached for 10 minutes; exhausted quota may return the last successful read with stale=true. Inherited assets are not included. Preserves Google RMF C.75 account-level callouts.

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
    public class ListAccountCalloutsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var customerId = "customerId_example";  // string? |  (optional) 

            try
            {
                // List account callouts
                ListAccountCallouts200Response result = apiInstance.ListAccountCallouts(accountId, customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAccountCallouts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAccountCalloutsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List account callouts
    ApiResponse<ListAccountCallouts200Response> response = apiInstance.ListAccountCalloutsWithHttpInfo(accountId, customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAccountCalloutsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **customerId** | **string?** |  | [optional]  |

### Return type

[**ListAccountCallouts200Response**](ListAccountCallouts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listaccountsitelinks"></a>
# **ListAccountSitelinks**
> ListAccountSitelinks200Response ListAccountSitelinks (string accountId, string? customerId = null)

List account sitelinks

Lists directly attached Google assets. Fresh reads are cached for 10 minutes; exhausted quota may return the last successful read with stale=true. Inherited assets are not included.

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
    public class ListAccountSitelinksExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var customerId = "customerId_example";  // string? |  (optional) 

            try
            {
                // List account sitelinks
                ListAccountSitelinks200Response result = apiInstance.ListAccountSitelinks(accountId, customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAccountSitelinks: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAccountSitelinksWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List account sitelinks
    ApiResponse<ListAccountSitelinks200Response> response = apiInstance.ListAccountSitelinksWithHttpInfo(accountId, customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAccountSitelinksWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **customerId** | **string?** |  | [optional]  |

### Return type

[**ListAccountSitelinks200Response**](ListAccountSitelinks200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listaccountstructuredsnippets"></a>
# **ListAccountStructuredSnippets**
> ListAccountStructuredSnippets200Response ListAccountStructuredSnippets (string accountId, string? customerId = null)

List account snippets

Lists directly attached Google assets. Fresh reads are cached for 10 minutes; exhausted quota may return the last successful read with stale=true. Inherited assets are not included.

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
    public class ListAccountStructuredSnippetsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var customerId = "customerId_example";  // string? |  (optional) 

            try
            {
                // List account snippets
                ListAccountStructuredSnippets200Response result = apiInstance.ListAccountStructuredSnippets(accountId, customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAccountStructuredSnippets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAccountStructuredSnippetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List account snippets
    ApiResponse<ListAccountStructuredSnippets200Response> response = apiInstance.ListAccountStructuredSnippetsWithHttpInfo(accountId, customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAccountStructuredSnippetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **customerId** | **string?** |  | [optional]  |

### Return type

[**ListAccountStructuredSnippets200Response**](ListAccountStructuredSnippets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadaccounts"></a>
# **ListAdAccounts**
> ListAdAccounts200Response ListAdAccounts (string accountId, string? adAccountId = null, int? limit = null)

List ad accounts

Returns the platform ad accounts available for the given account (e.g. Meta ad accounts, TikTok advertiser IDs, Google Ads customer IDs). Meta business-login accounts use their own system-user token. Fresh Meta discovery includes businessId and businessName from the owning Business Manager when available; cached entries gain these fields after the next discovery refresh.  For TikTok agencies: enumerates every advertiser under every Business Center the token can read (paginated server-side), then chunks the lookup against TikTok's `/advertiser/info/` endpoint (which has a per-call cap of ≤100 IDs). Solo advertisers without a BC fall back to the OAuth-time `advertiser_ids` list. Cached for 1h on the SocialAccount; lazy-refreshed on first call after expiry.  For Google Ads: responds `429` when Google's API quota is temporarily exhausted (instead of an empty list). Retry after a delay. 

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
    public class ListAdAccountsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Account ID
            var adAccountId = "adAccountId_example";  // string? | Filter response to a single platform ad account ID (e.g. `act_123` for Meta, advertiser_id for TikTok). Returns at most one item. (optional) 
            var limit = 56;  // int? | Clamp the returned `accounts[]` length. Useful for typeahead pickers on agency tokens with hundreds of advertisers. (optional) 

            try
            {
                // List ad accounts
                ListAdAccounts200Response result = apiInstance.ListAdAccounts(accountId, adAccountId, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAdAccounts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdAccountsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List ad accounts
    ApiResponse<ListAdAccounts200Response> response = apiInstance.ListAdAccountsWithHttpInfo(accountId, adAccountId, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAdAccountsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Account ID |  |
| **adAccountId** | **string?** | Filter response to a single platform ad account ID (e.g. &#x60;act_123&#x60; for Meta, advertiser_id for TikTok). Returns at most one item. | [optional]  |
| **limit** | **int?** | Clamp the returned &#x60;accounts[]&#x60; length. Useful for typeahead pickers on agency tokens with hundreds of advertisers. | [optional]  |

### Return type

[**ListAdAccounts200Response**](ListAdAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **400** | Invalid request |  -  |
| **200** | Ad accounts |  -  |
| **401** | Unauthorized |  -  |
| **422** | Platform ads connection required (TikTok Ads, X Ads) or Instagram missing linked Facebook account |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted.  Reddit rate-limits per connected Reddit user (1000 requests per 10-minute window), and that budget is shared by every operation using that account. Retry after the window resets rather than retrying immediately; repeated calls while exhausted do not succeed and keep the budget spent.  |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadlabels"></a>
# **ListAdLabels**
> ListAdLabels200Response ListAdLabels (string accountId, string adAccountId, int? limit = null, string? after = null)

Ad labels

Lists the ad account's organizational labels (Meta's `/act_X/adlabels`), rows returned verbatim (id, name, created/updated time).

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
    public class ListAdLabelsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // Ad labels
                ListAdLabels200Response result = apiInstance.ListAdLabels(accountId, adAccountId, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAdLabels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdLabelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad labels
    ApiResponse<ListAdLabels200Response> response = apiInstance.ListAdLabelsWithHttpInfo(accountId, adAccountId, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAdLabelsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**ListAdLabels200Response**](ListAdLabels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **200** | Ad labels (raw Meta shape) |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadnegativekeywordlists"></a>
# **ListAdNegativeKeywordLists**
> ListAdNegativeKeywordLists200Response ListAdNegativeKeywordLists (string accountId, string? customerId = null, string? platform = null)

List negative keyword lists

Google Ads shared negative keyword lists (shared_set type NEGATIVE_KEYWORDS). Reads are cached for 10 minutes; quota exhaustion may return the last successful result for up to 7 days with stale=true. Customer selection is limited to this connection and its account scope.

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
    public class ListAdNegativeKeywordListsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var customerId = "customerId_example";  // string? |  (optional) 
            var platform = "facebook";  // string? |  (optional) 

            try
            {
                // List negative keyword lists
                ListAdNegativeKeywordLists200Response result = apiInstance.ListAdNegativeKeywordLists(accountId, customerId, platform);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAdNegativeKeywordLists: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdNegativeKeywordListsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List negative keyword lists
    ApiResponse<ListAdNegativeKeywordLists200Response> response = apiInstance.ListAdNegativeKeywordListsWithHttpInfo(accountId, customerId, platform);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAdNegativeKeywordListsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **customerId** | **string?** |  | [optional]  |
| **platform** | **string?** |  | [optional]  |

### Return type

[**ListAdNegativeKeywordLists200Response**](ListAdNegativeKeywordLists200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access and permission to the selected account are required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | Ambiguous campaign or account selection. Use a profile-scoped key. A list still attached to a campaign may also be rejected by Google. The account may also be inactive or need reconnection (code ads_connection_required). Reconnect it and read GET /v1/accounts for its current ID before retrying. |  -  |
| **422** | Google Ads connection is missing or unavailable. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Available only on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadstudies"></a>
# **ListAdStudies**
> ListAdStudies200Response ListAdStudies (string accountId, string adAccountId, string? fields = null, int? limit = null, string? after = null)

A/B tests and lift studies

Lists the ad account's A/B tests and lift studies (Meta's `/act_X/ad_studies`), rows returned verbatim. The default projection covers id, name, type, timing and cells with split percentages; `fields` is a raw-passthrough override.

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
    public class ListAdStudiesExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).
            var fields = id,name,type,cells{id,name,treatment_percentage};  // string? | Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers, so a nested edge can be paged explicitly: without a .limit() modifier the expansion runs at the Meta default page size and the tail is dropped silently. (optional) 
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // A/B tests and lift studies
                ListAdStudies200Response result = apiInstance.ListAdStudies(accountId, adAccountId, fields, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAdStudies: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdStudiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // A/B tests and lift studies
    ApiResponse<ListAdStudies200Response> response = apiInstance.ListAdStudiesWithHttpInfo(accountId, adAccountId, fields, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAdStudiesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |
| **fields** | **string?** | Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers, so a nested edge can be paged explicitly: without a .limit() modifier the expansion runs at the Meta default page size and the tail is dropped silently. | [optional]  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**ListAdStudies200Response**](ListAdStudies200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **200** | Ad studies (raw Meta shape) |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadsbusinesscenters"></a>
# **ListAdsBusinessCenters**
> ListAdsBusinessCenters200Response ListAdsBusinessCenters (string accountId)

List TikTok Business Centers

Returns the TikTok Business Centers (BCs) the connected `tiktokads` account can read. Each BC reports its advertiser count so callers can build agency-style pickers without re-walking `/v1/ads/accounts` per BC.  TikTok-only. Solo advertisers (non-agency tokens) return an empty array. 

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
    public class ListAdsBusinessCentersExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | ID of the `tiktokads` (or parent `tiktok` posting) SocialAccount

            try
            {
                // List TikTok Business Centers
                ListAdsBusinessCenters200Response result = apiInstance.ListAdsBusinessCenters(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAdsBusinessCenters: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdsBusinessCentersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List TikTok Business Centers
    ApiResponse<ListAdsBusinessCenters200Response> response = apiInstance.ListAdsBusinessCentersWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAdsBusinessCentersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | ID of the &#x60;tiktokads&#x60; (or parent &#x60;tiktok&#x60; posting) SocialAccount |  |

### Return type

[**ListAdsBusinessCenters200Response**](ListAdsBusinessCenters200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Business centers |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **422** | TikTok Ads not connected |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadsinstagramaccounts"></a>
# **ListAdsInstagramAccounts**
> ListAdsInstagramAccounts200Response ListAdsInstagramAccounts (string accountId, string adAccountId)

List Instagram ad identities

Discovers identities through connected_instagram_accounts, Page linkage and Page-backed identities, with a best-effort business fallback. Business permission errors do not fail discovery. The resolved object uses the same profile-scoped resolver as ad creation; null means no identity was resolved. Format-specific observed-actor fallbacks at creative creation are not predicted.

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
    public class ListAdsInstagramAccountsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio Meta Ads or Facebook SocialAccount ID.
            var adAccountId = "adAccountId_example";  // string | Meta ad account ID including the act_ prefix.

            try
            {
                // List Instagram ad identities
                ListAdsInstagramAccounts200Response result = apiInstance.ListAdsInstagramAccounts(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAdsInstagramAccounts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdsInstagramAccountsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Instagram ad identities
    ApiResponse<ListAdsInstagramAccounts200Response> response = apiInstance.ListAdsInstagramAccountsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAdsInstagramAccountsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio Meta Ads or Facebook SocialAccount ID. |  |
| **adAccountId** | **string** | Meta ad account ID including the act_ prefix. |  |

### Return type

[**ListAdsInstagramAccounts200Response**](ListAdsInstagramAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Instagram identities and Page linkage. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The account or Meta asset is not accessible. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **501** | Only supported on Meta Ads and Facebook accounts. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadvertisableapplications"></a>
# **ListAdvertisableApplications**
> ListAdvertisableApplications200Response ListAdvertisableApplications (string accountId, string adAccountId)

List advertisable apps

Lists applications available to a Meta ad account, their supported platforms and unmodified object store URLs. A listed app still needs a configured mobile platform and store URL to run install promotion.

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
    public class ListAdvertisableApplicationsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio Meta Ads or Facebook SocialAccount ID.
            var adAccountId = "adAccountId_example";  // string | Meta ad account ID including the act_ prefix.

            try
            {
                // List advertisable apps
                ListAdvertisableApplications200Response result = apiInstance.ListAdvertisableApplications(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAdvertisableApplications: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdvertisableApplicationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List advertisable apps
    ApiResponse<ListAdvertisableApplications200Response> response = apiInstance.ListAdvertisableApplicationsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAdvertisableApplicationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio Meta Ads or Facebook SocialAccount ID. |  |
| **adAccountId** | **string** | Meta ad account ID including the act_ prefix. |  |

### Return type

[**ListAdvertisableApplications200Response**](ListAdvertisableApplications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Applications available for promotion. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The account or Meta asset is not accessible. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **501** | Only supported on Meta Ads and Facebook accounts. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcustomconversions"></a>
# **ListCustomConversions**
> ListCustomConversions200Response ListCustomConversions (string accountId, string adAccountId)

List custom conversions

The ad account's Meta custom conversions, including archived ones (`isArchived`).

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
    public class ListCustomConversionsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Meta ads SocialAccount id.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).

            try
            {
                // List custom conversions
                ListCustomConversions200Response result = apiInstance.ListCustomConversions(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListCustomConversions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCustomConversionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List custom conversions
    ApiResponse<ListCustomConversions200Response> response = apiInstance.ListCustomConversionsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListCustomConversionsWithHttpInfo: " + e.Message);
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

[**ListCustomConversions200Response**](ListCustomConversions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **200** | Custom conversions |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the token lacks the ads permissions. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listhighdemandperiods"></a>
# **ListHighDemandPeriods**
> ListHighDemandPeriods200Response ListHighDemandPeriods (string accountId, string? campaignId = null, string? adSetId = null, int? limit = null, string? after = null)

List high-demand periods

Scheduled budget increases (Meta's budget-scheduling API). The Graph edge lives on the campaign and ad-set nodes only, so exactly one of `campaignId` / `adSetId` (platform ids) is required. Rows returned verbatim (budget_value, budget_value_type, time window, recurrence).

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
    public class ListHighDemandPeriodsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var campaignId = "campaignId_example";  // string? | Platform campaign id. Exactly one of campaignId / adSetId. (optional) 
            var adSetId = "adSetId_example";  // string? | Platform ad set id. Exactly one of campaignId / adSetId. (optional) 
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // List high-demand periods
                ListHighDemandPeriods200Response result = apiInstance.ListHighDemandPeriods(accountId, campaignId, adSetId, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListHighDemandPeriods: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListHighDemandPeriodsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List high-demand periods
    ApiResponse<ListHighDemandPeriods200Response> response = apiInstance.ListHighDemandPeriodsWithHttpInfo(accountId, campaignId, adSetId, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListHighDemandPeriodsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **campaignId** | **string?** | Platform campaign id. Exactly one of campaignId / adSetId. | [optional]  |
| **adSetId** | **string?** | Platform ad set id. Exactly one of campaignId / adSetId. | [optional]  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**ListHighDemandPeriods200Response**](ListHighDemandPeriods200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **200** | Budget schedules (raw Meta shape) |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listmetabusinesses"></a>
# **ListMetaBusinesses**
> ListMetaBusinesses200Response ListMetaBusinesses (string accountId, int? limit = null, string? after = null)

Businesses list

Business Manager portfolios the connected Meta user belongs to (Meta's `/me/businesses`), rows returned verbatim (id, name, verification_status, created_time). Token-scoped, so no `adAccountId` is needed. For TikTok Business Centers use `GET /v1/ads/business-centers`.

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
    public class ListMetaBusinessesExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // Businesses list
                ListMetaBusinesses200Response result = apiInstance.ListMetaBusinesses(accountId, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListMetaBusinesses: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListMetaBusinessesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Businesses list
    ApiResponse<ListMetaBusinesses200Response> response = apiInstance.ListMetaBusinessesWithHttpInfo(accountId, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListMetaBusinessesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**ListMetaBusinesses200Response**](ListMetaBusinesses200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **200** | Businesses (raw Meta shape) |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtiktokadpixels"></a>
# **ListTikTokAdPixels**
> ListTikTokAdPixels200Response ListTikTokAdPixels (string accountId, string? advertiserId = null, string? code = null)

List TikTok ad pixels

Lists pixels and their supported optimization events for a connected TikTok Ads account. The advertiser defaults to the first advertiser on the connection. Reconnect if Pixel Management permission has not been granted.

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
    public class ListTikTokAdPixelsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount ID.
            var advertiserId = "advertiserId_example";  // string? | Advertiser belonging to this connection. (optional) 
            var code = "code_example";  // string? | Filter by a Pixel Code. (optional) 

            try
            {
                // List TikTok ad pixels
                ListTikTokAdPixels200Response result = apiInstance.ListTikTokAdPixels(accountId, advertiserId, code);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListTikTokAdPixels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTikTokAdPixelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List TikTok ad pixels
    ApiResponse<ListTikTokAdPixels200Response> response = apiInstance.ListTikTokAdPixelsWithHttpInfo(accountId, advertiserId, code);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListTikTokAdPixelsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount ID. |  |
| **advertiserId** | **string?** | Advertiser belonging to this connection. | [optional]  |
| **code** | **string?** | Filter by a Pixel Code. | [optional]  |

### Return type

[**ListTikTokAdPixels200Response**](ListTikTokAdPixels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | TikTok pixels. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | Pixel Management permission is missing (code reconnect_required). Reconnect TikTok Ads to grant it. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listvaluerulesets"></a>
# **ListValueRuleSets**
> ListValueRuleSets200Response ListValueRuleSets (string accountId, string adAccountId, int? limit = null, string? after = null)

List value rule sets

Lists the ad account's value rule sets (Meta's `/act_X/value_rule_set`). A value rule set adjusts the auction bid up or down for audience segments you value differently; attach one to an ad set with `valueRuleSetId` on `POST /v1/ads/create` or `PUT /v1/ads/ad-sets/{adSetId}`.  Rows are returned in the same camelCase shape the `PUT` body takes, ids included, so a set round-trips 1:1: **the update is a full replace, not a patch**, so you GET, mutate and send the whole thing back.  Limits: 6 rule sets per ad account, 10 rules per set, 4 criteria per rule.  **Rule order is semantic.** Rules are evaluated in array order and only the FIRST matching rule adjusts the bid for an overlapping audience. The order you send is the order that is stored and returned.  Eligibility: value rule sets apply only to ad sets on the `LOWEST_COST_WITHOUT_CAP` (auto-bid) or `COST_CAP` bid strategies. Meta rejects the rest server-side.

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
    public class ListValueRuleSetsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. Meta does not document paging on this edge; `after` comes back null when it omits cursors. (optional) 

            try
            {
                // List value rule sets
                ListValueRuleSets200Response result = apiInstance.ListValueRuleSets(accountId, adAccountId, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListValueRuleSets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListValueRuleSetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List value rule sets
    ApiResponse<ListValueRuleSets200Response> response = apiInstance.ListValueRuleSetsWithHttpInfo(accountId, adAccountId, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListValueRuleSetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. Meta does not document paging on this edge; &#x60;after&#x60; comes back null when it omits cursors. | [optional]  |

### Return type

[**ListValueRuleSets200Response**](ListValueRuleSets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **200** | Value rule sets |  -  |
| **400** | Invalid input, or Meta rejected the query. Meta answers a bad rule-set id with GraphMethodException code 100 / subcode 33, which is indistinguishable between not-found, no-permission, and account-not-enabled. |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removeaccountcallout"></a>
# **RemoveAccountCallout**
> RemoveAccountCallout200Response RemoveAccountCallout (RemoveAccountCalloutRequest removeAccountCalloutRequest)

Remove account callout

Removes the customer_asset attachment only. The underlying shared asset and its campaign or ad-group attachments remain.

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
    public class RemoveAccountCalloutExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var removeAccountCalloutRequest = new RemoveAccountCalloutRequest(); // RemoveAccountCalloutRequest | 

            try
            {
                // Remove account callout
                RemoveAccountCallout200Response result = apiInstance.RemoveAccountCallout(removeAccountCalloutRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.RemoveAccountCallout: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveAccountCalloutWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove account callout
    ApiResponse<RemoveAccountCallout200Response> response = apiInstance.RemoveAccountCalloutWithHttpInfo(removeAccountCalloutRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.RemoveAccountCalloutWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **removeAccountCalloutRequest** | [**RemoveAccountCalloutRequest**](RemoveAccountCalloutRequest.md) |  |  |

### Return type

[**RemoveAccountCallout200Response**](RemoveAccountCallout200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removeaccountsitelink"></a>
# **RemoveAccountSitelink**
> RemoveAccountCallout200Response RemoveAccountSitelink (RemoveAccountCalloutRequest removeAccountCalloutRequest)

Remove account sitelink

Removes the customer_asset attachment only. The underlying shared asset and its campaign or ad-group attachments remain.

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
    public class RemoveAccountSitelinkExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var removeAccountCalloutRequest = new RemoveAccountCalloutRequest(); // RemoveAccountCalloutRequest | 

            try
            {
                // Remove account sitelink
                RemoveAccountCallout200Response result = apiInstance.RemoveAccountSitelink(removeAccountCalloutRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.RemoveAccountSitelink: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveAccountSitelinkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove account sitelink
    ApiResponse<RemoveAccountCallout200Response> response = apiInstance.RemoveAccountSitelinkWithHttpInfo(removeAccountCalloutRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.RemoveAccountSitelinkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **removeAccountCalloutRequest** | [**RemoveAccountCalloutRequest**](RemoveAccountCalloutRequest.md) |  |  |

### Return type

[**RemoveAccountCallout200Response**](RemoveAccountCallout200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removeaccountstructuredsnippet"></a>
# **RemoveAccountStructuredSnippet**
> RemoveAccountCallout200Response RemoveAccountStructuredSnippet (RemoveAccountCalloutRequest removeAccountCalloutRequest)

Remove account snippet

Removes the customer_asset attachment only. The underlying shared asset and its campaign or ad-group attachments remain.

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
    public class RemoveAccountStructuredSnippetExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var removeAccountCalloutRequest = new RemoveAccountCalloutRequest(); // RemoveAccountCalloutRequest | 

            try
            {
                // Remove account snippet
                RemoveAccountCallout200Response result = apiInstance.RemoveAccountStructuredSnippet(removeAccountCalloutRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.RemoveAccountStructuredSnippet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveAccountStructuredSnippetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove account snippet
    ApiResponse<RemoveAccountCallout200Response> response = apiInstance.RemoveAccountStructuredSnippetWithHttpInfo(removeAccountCalloutRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.RemoveAccountStructuredSnippetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **removeAccountCalloutRequest** | [**RemoveAccountCalloutRequest**](RemoveAccountCalloutRequest.md) |  |  |

### Return type

[**RemoveAccountCallout200Response**](RemoveAccountCallout200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="replaceadnegativekeywordlistkeywords"></a>
# **ReplaceAdNegativeKeywordListKeywords**
> ReplaceAdNegativeKeywordListKeywords200Response ReplaceAdNegativeKeywordListKeywords (string listId, ReplaceAdNegativeKeywordListKeywordsRequest replaceAdNegativeKeywordListKeywordsRequest)

Replace negative list keywords

Replaces the full desired keyword set. Existing keywords are diffed by normalized text and match type; creates and removals are applied atomically in one mutation. Unchanged criteria retain their ids. Send an empty keywords array to clear the list. Changes affect every campaign using this list. Each create or removal consumes one daily operation; the entire batch must fit the remaining quota.

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
    public class ReplaceAdNegativeKeywordListKeywordsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var listId = "listId_example";  // string | 
            var replaceAdNegativeKeywordListKeywordsRequest = new ReplaceAdNegativeKeywordListKeywordsRequest(); // ReplaceAdNegativeKeywordListKeywordsRequest | 

            try
            {
                // Replace negative list keywords
                ReplaceAdNegativeKeywordListKeywords200Response result = apiInstance.ReplaceAdNegativeKeywordListKeywords(listId, replaceAdNegativeKeywordListKeywordsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ReplaceAdNegativeKeywordListKeywords: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReplaceAdNegativeKeywordListKeywordsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Replace negative list keywords
    ApiResponse<ReplaceAdNegativeKeywordListKeywords200Response> response = apiInstance.ReplaceAdNegativeKeywordListKeywordsWithHttpInfo(listId, replaceAdNegativeKeywordListKeywordsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ReplaceAdNegativeKeywordListKeywordsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listId** | **string** |  |  |
| **replaceAdNegativeKeywordListKeywordsRequest** | [**ReplaceAdNegativeKeywordListKeywordsRequest**](ReplaceAdNegativeKeywordListKeywordsRequest.md) |  |  |

### Return type

[**ReplaceAdNegativeKeywordListKeywords200Response**](ReplaceAdNegativeKeywordListKeywords200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access and permission to the selected account are required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | Ambiguous campaign or account selection. Use a profile-scoped key. A list still attached to a campaign may also be rejected by Google. The account may also be inactive or need reconnection (code ads_connection_required). Reconnect it and read GET /v1/accounts for its current ID before retrying. |  -  |
| **422** | Google Ads connection is missing or unavailable. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Available only on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="replytoadcomment"></a>
# **ReplyToAdComment**
> ReplyToAdComment200Response ReplyToAdComment (string adId, string commentId, ReplyToAdCommentRequest replyToAdCommentRequest, DateOnly? since = null, DateOnly? until = null)

Reply to an ad comment

Reply to a first-level TikTok ad comment. Requires a TT_USER or CUSTOMIZED_USER identity with comment-management permission. Replies to replies are rejected. The response commentId identifies the new reply. This operation is not idempotent; do not blindly retry an uncertain response.  Unknown identity and video item fields are resolved only when needed for this action, then persisted for reuse. Comment-specific fields take precedence. If TikTok no longer returns the ad needed to resolve identity, 404 ad_not_found directs you to check deletion or archival in TikTok Ads Manager. Listing can still succeed. Unsupported or unavailable identity returns 403 feature_not_available. Denied access to ad details returns 403 insufficient_permissions with reconnect guidance and the upstream platformError.  Requires Ads access. The ad is resolved within the caller's accessible profiles. Before moderation, Zernio verifies that the comment belongs to this ad using TikTok's ad-group comment listing. The default search window is the last 30 days. Use since/until for older comments, with at most 30 days between the dates. Lookups scan at most 2,000 ad-group comments; narrow the date window if exceeded. Meta returns 501 feature_not_available with guidance to use the existing inbox comment endpoints and the account/post IDs from GET /v1/ads/{adId}/comments. 

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
    public class ReplyToAdCommentExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Internal Zernio ad ID or indexed platform ad ID.
            var commentId = "commentId_example";  // string | TikTok comment ID from the ad comment listing.
            var replyToAdCommentRequest = new ReplyToAdCommentRequest(); // ReplyToAdCommentRequest | 
            var since = DateOnly.Parse("2013-10-20");  // DateOnly? | Start date of the comment lookup window. Defaults to 30 days before until. (optional) 
            var until = DateOnly.Parse("2013-10-20");  // DateOnly? | End date of the comment lookup window. Defaults to today in UTC. (optional) 

            try
            {
                // Reply to an ad comment
                ReplyToAdComment200Response result = apiInstance.ReplyToAdComment(adId, commentId, replyToAdCommentRequest, since, until);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ReplyToAdComment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReplyToAdCommentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reply to an ad comment
    ApiResponse<ReplyToAdComment200Response> response = apiInstance.ReplyToAdCommentWithHttpInfo(adId, commentId, replyToAdCommentRequest, since, until);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ReplyToAdCommentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Internal Zernio ad ID or indexed platform ad ID. |  |
| **commentId** | **string** | TikTok comment ID from the ad comment listing. |  |
| **replyToAdCommentRequest** | [**ReplyToAdCommentRequest**](ReplyToAdCommentRequest.md) |  |  |
| **since** | **DateOnly?** | Start date of the comment lookup window. Defaults to 30 days before until. | [optional]  |
| **until** | **DateOnly?** | End date of the comment lookup window. Defaults to today in UTC. | [optional]  |

### Return type

[**ReplyToAdComment200Response**](ReplyToAdComment200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comment action completed. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access or supported identity is unavailable (feature_not_available), or TikTok denies ad-detail access or comment-management permission (insufficient_permissions). Grant permission and reconnect the TikTok Ads account before retrying. |  -  |
| **404** | Ad is inaccessible or unavailable on TikTok for identity resolution (ad_not_found), or the comment was not found on this ad in the selected date window (resource_not_found). |  -  |
| **422** | TikTok Ads connection is unavailable. |  -  |
| **501** | Moderation on this route supports TikTok. Use the inbox comment routes for Meta. |  -  |
| **502** | TikTok rejected the request or was unavailable. Inspect platformError for its code and message. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateaccountcallouts"></a>
# **UpdateAccountCallouts**
> UpdateAccountCallouts200Response UpdateAccountCallouts (UpdateAccountCalloutsRequest updateAccountCalloutsRequest)

Update account callouts

Edits existing Google assets in place. Send updates with assetResourceName and the fields to change. An asset is shared: changes affect every attachment using it. Omitted fields stay unchanged. The operation consumes the Google operations budget and invalidates affected cached lists.

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
    public class UpdateAccountCalloutsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var updateAccountCalloutsRequest = new UpdateAccountCalloutsRequest(); // UpdateAccountCalloutsRequest | 

            try
            {
                // Update account callouts
                UpdateAccountCallouts200Response result = apiInstance.UpdateAccountCallouts(updateAccountCalloutsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.UpdateAccountCallouts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAccountCalloutsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update account callouts
    ApiResponse<UpdateAccountCallouts200Response> response = apiInstance.UpdateAccountCalloutsWithHttpInfo(updateAccountCalloutsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.UpdateAccountCalloutsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateAccountCalloutsRequest** | [**UpdateAccountCalloutsRequest**](UpdateAccountCalloutsRequest.md) |  |  |

### Return type

[**UpdateAccountCallouts200Response**](UpdateAccountCallouts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateaccountsitelinks"></a>
# **UpdateAccountSitelinks**
> UpdateAccountCallouts200Response UpdateAccountSitelinks (UpdateAccountSitelinksRequest updateAccountSitelinksRequest)

Update account sitelinks

Edits existing Google assets in place. Send updates with assetResourceName and the fields to change. An asset is shared: changes affect every attachment using it. Omitted fields stay unchanged. The operation consumes the Google operations budget and invalidates affected cached lists.

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
    public class UpdateAccountSitelinksExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var updateAccountSitelinksRequest = new UpdateAccountSitelinksRequest(); // UpdateAccountSitelinksRequest | 

            try
            {
                // Update account sitelinks
                UpdateAccountCallouts200Response result = apiInstance.UpdateAccountSitelinks(updateAccountSitelinksRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.UpdateAccountSitelinks: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAccountSitelinksWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update account sitelinks
    ApiResponse<UpdateAccountCallouts200Response> response = apiInstance.UpdateAccountSitelinksWithHttpInfo(updateAccountSitelinksRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.UpdateAccountSitelinksWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateAccountSitelinksRequest** | [**UpdateAccountSitelinksRequest**](UpdateAccountSitelinksRequest.md) |  |  |

### Return type

[**UpdateAccountCallouts200Response**](UpdateAccountCallouts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateaccountstructuredsnippets"></a>
# **UpdateAccountStructuredSnippets**
> UpdateAccountCallouts200Response UpdateAccountStructuredSnippets (UpdateAccountStructuredSnippetsRequest updateAccountStructuredSnippetsRequest)

Update account snippets

Edits existing Google assets in place. Send updates with assetResourceName and the fields to change. An asset is shared: changes affect every attachment using it. Omitted fields stay unchanged. The operation consumes the Google operations budget and invalidates affected cached lists.

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
    public class UpdateAccountStructuredSnippetsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var updateAccountStructuredSnippetsRequest = new UpdateAccountStructuredSnippetsRequest(); // UpdateAccountStructuredSnippetsRequest | 

            try
            {
                // Update account snippets
                UpdateAccountCallouts200Response result = apiInstance.UpdateAccountStructuredSnippets(updateAccountStructuredSnippetsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.UpdateAccountStructuredSnippets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAccountStructuredSnippetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update account snippets
    ApiResponse<UpdateAccountCallouts200Response> response = apiInstance.UpdateAccountStructuredSnippetsWithHttpInfo(updateAccountStructuredSnippetsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.UpdateAccountStructuredSnippetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateAccountStructuredSnippetsRequest** | [**UpdateAccountStructuredSnippetsRequest**](UpdateAccountStructuredSnippetsRequest.md) |  |  |

### Return type

[**UpdateAccountCallouts200Response**](UpdateAccountCallouts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadaccount"></a>
# **UpdateAdAccount**
> UpdateAdAccount200Response UpdateAdAccount (UpdateAdAccountRequest updateAdAccountRequest)

Update ad account settings

Sets the default DSA beneficiary and payor on a Meta ad account (EU DSA, Article 26). Set them once and every EU-targeted call to `/v1/ads/create`, `/v1/ads/boost` and `/v1/ads/ctwa` on that ad account can omit `dsaBeneficiary`/`dsaPayor`: Meta applies the defaults automatically.  The values are written to the ad account on Meta, the same setting Ads Manager edits. Nothing is stored in Zernio, and defaults already set in Ads Manager work identically. Zernio never guesses these values for you. Beneficiary and payor are legal disclosures shown to EU users, so you must provide the entity names explicitly. Use `GET /v1/ads/dsa-recommendations` to offer suggestions in your UI.  If `defaultDsaPayor` is omitted, the beneficiary is also set as the payor, which covers the common case where the same entity benefits from and pays for the ads. Read the current values back with `GET /v1/ads/dsa-defaults`.  Currently supported for Meta accounts only; other platforms return 400. 

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
    public class UpdateAdAccountExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var updateAdAccountRequest = new UpdateAdAccountRequest(); // UpdateAdAccountRequest | 

            try
            {
                // Update ad account settings
                UpdateAdAccount200Response result = apiInstance.UpdateAdAccount(updateAdAccountRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.UpdateAdAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update ad account settings
    ApiResponse<UpdateAdAccount200Response> response = apiInstance.UpdateAdAccountWithHttpInfo(updateAdAccountRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.UpdateAdAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateAdAccountRequest** | [**UpdateAdAccountRequest**](UpdateAdAccountRequest.md) |  |  |

### Return type

[**UpdateAdAccount200Response**](UpdateAdAccount200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | DSA defaults updated (re-read from Meta after the write) |  -  |
| **400** | Unsupported platform (non-Meta account) or invalid adAccountId |  -  |
| **401** | Unauthorized |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadnegativekeywordlist"></a>
# **UpdateAdNegativeKeywordList**
> UpdateAdNegativeKeywordList200Response UpdateAdNegativeKeywordList (string listId, UpdateAdNegativeKeywordListRequest updateAdNegativeKeywordListRequest)

Rename a negative keyword list

Renames a shared negative keyword list. Keywords and campaign associations are unchanged. Use the keywords endpoint to edit the desired keyword set.

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
    public class UpdateAdNegativeKeywordListExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var listId = "listId_example";  // string | 
            var updateAdNegativeKeywordListRequest = new UpdateAdNegativeKeywordListRequest(); // UpdateAdNegativeKeywordListRequest | 

            try
            {
                // Rename a negative keyword list
                UpdateAdNegativeKeywordList200Response result = apiInstance.UpdateAdNegativeKeywordList(listId, updateAdNegativeKeywordListRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.UpdateAdNegativeKeywordList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdNegativeKeywordListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Rename a negative keyword list
    ApiResponse<UpdateAdNegativeKeywordList200Response> response = apiInstance.UpdateAdNegativeKeywordListWithHttpInfo(listId, updateAdNegativeKeywordListRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.UpdateAdNegativeKeywordListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listId** | **string** |  |  |
| **updateAdNegativeKeywordListRequest** | [**UpdateAdNegativeKeywordListRequest**](UpdateAdNegativeKeywordListRequest.md) |  |  |

### Return type

[**UpdateAdNegativeKeywordList200Response**](UpdateAdNegativeKeywordList200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access and permission to the selected account are required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | Ambiguous campaign or account selection. Use a profile-scoped key. A list still attached to a campaign may also be rejected by Google. The account may also be inactive or need reconnection (code ads_connection_required). Reconnect it and read GET /v1/accounts for its current ID before retrying. |  -  |
| **422** | Google Ads connection is missing or unavailable. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Available only on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatevalueruleset"></a>
# **UpdateValueRuleSet**
> UpdateValueRuleSet200Response UpdateValueRuleSet (string valueRuleSetId, UpdateValueRuleSetRequest updateValueRuleSetRequest)

Replace a value rule set

**THIS IS A FULL REPLACE, NOT A PATCH.** Meta's update is declarative: the body you send becomes the rule set.  - `GET /v1/ads/value-rule-sets/{valueRuleSetId}` FIRST. - Keep a rule or criterion by echoing its `id`. - Create one by including the object WITHOUT an `id`. - Delete one by OMITTING it from the array. There is no warning and no undo.  `name` and `rules` are both required for exactly this reason: a partial body would silently destroy every rule left out.  **Rule order is semantic**: the array order you send is the evaluation order, and only the first matching rule adjusts the bid for an overlapping audience.  Existing rule sets created elsewhere may contain `LOCATION_DMA` criteria. Those went inert on 2026-06-22 and are rejected here; migrate them to `LOCATION_COMSCORE_MARKET`.

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
    public class UpdateValueRuleSetExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var valueRuleSetId = "valueRuleSetId_example";  // string | Platform value rule set id.
            var updateValueRuleSetRequest = new UpdateValueRuleSetRequest(); // UpdateValueRuleSetRequest | 

            try
            {
                // Replace a value rule set
                UpdateValueRuleSet200Response result = apiInstance.UpdateValueRuleSet(valueRuleSetId, updateValueRuleSetRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.UpdateValueRuleSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateValueRuleSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Replace a value rule set
    ApiResponse<UpdateValueRuleSet200Response> response = apiInstance.UpdateValueRuleSetWithHttpInfo(valueRuleSetId, updateValueRuleSetRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.UpdateValueRuleSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **valueRuleSetId** | **string** | Platform value rule set id. |  |
| **updateValueRuleSetRequest** | [**UpdateValueRuleSetRequest**](UpdateValueRuleSetRequest.md) |  |  |

### Return type

[**UpdateValueRuleSet200Response**](UpdateValueRuleSet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **200** | Value rule set replaced |  -  |
| **400** | Invalid input, or Meta rejected the update |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

