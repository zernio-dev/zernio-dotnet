# Zernio.Api.AdLibraryApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**SearchAdLibrary**](AdLibraryApi.md#searchadlibrary) | **GET** /v1/ads/library | Search the public Ad Library |

<a id="searchadlibrary"></a>
# **SearchAdLibrary**
> SearchAdLibrary200Response SearchAdLibrary (string? platform = null, string? accountId = null, string? q = null, string? pageIds = null, string? advertiser = null, string? countries = null, string? adType = null, string? status = null, string? platforms = null, string? mediaType = null, string? languages = null, DateOnly? since = null, DateOnly? until = null, string? searchType = null, string? fields = null, int? limit = null, string? after = null)

Search the public Ad Library

Competitor and market research over the public ad archives. Meta's Ad Library (`GET /ads_archive`) is searched with Zernio's own developer access, so `platform=meta` needs no connected account at all. LinkedIn's Ad Library (`GET /rest/adLibrary`) runs on a connected `linkedin` / `linkedinads` account, passed as `accountId`. Passing a Meta account as `accountId` also selects Meta. Rows are returned in the platform's raw shape under `data`; `paging.after` is an opaque cursor on both (`null` when exhausted).  **Meta coverage.** Political and social-issue ads are searchable worldwide. Every other ad is in the archive only if it was delivered to the EU or UK within the last year, so a US-only commercial advertiser is invisible. Spend, impressions and demographics are political-only fields and are left out of the default projection; request them via `fields`. All customers share Zernio's Meta quota, so a `429` means back off for a minute.  **LinkedIn coverage.** Ads served after June 1 2023, worldwide, kept for a year after their last impression. EU-delivered ads carry impression ranges and the disclosed targeting facets. Pages are capped at 25 ads (`limit` > 25 is a 400); `after` is the next offset.  Which params apply: `q`, `countries`, `since`, `until`, `limit`, `after` on both; `pageIds`, `adType`, `status`, `platforms`, `mediaType`, `languages`, `searchType`, `fields` are Meta-only; `advertiser` is LinkedIn-only. Passing a param the account's platform does not support is a 400 naming the param.

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
    public class SearchAdLibraryExample
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
            var apiInstance = new AdLibraryApi(httpClient, config, httpClientHandler);
            var platform = "meta";  // string? | Which archive to search. `meta` needs no accountId. Required unless accountId is given. (optional) 
            var accountId = "accountId_example";  // string? | Zernio SocialAccount id. Required for LinkedIn (linkedin / linkedinads: its token searches). Optional for Meta, where any facebook / instagram / metaads account only selects the platform. (optional) 
            var q = "q_example";  // string? | Keyword search. Meta does not translate it, so write it in the ads' language. Required unless pageIds (Meta) or advertiser (LinkedIn) is given. (optional) 
            var pageIds = "pageIds_example";  // string? | Meta only. Comma-separated Facebook Page ids (max 10) whose ads to list. (optional) 
            var advertiser = "advertiser_example";  // string? | LinkedIn only. Advertiser (Page) name to search. (optional) 
            var countries = "countries_example";  // string? | Comma-separated ISO 3166-1 alpha-2 codes the ads reached. Meta defaults to ALL (an explicit ALL is Meta-only); LinkedIn searches every market when omitted. (optional) 
            var adType = "ALL";  // string? | Meta only. (optional)  (default to ALL)
            var status = "ACTIVE";  // string? | Meta only. ACTIVE = eligible for delivery right now. (optional)  (default to ACTIVE)
            var platforms = "platforms_example";  // string? | Meta only. Comma-separated publisher platforms: FACEBOOK, INSTAGRAM, AUDIENCE_NETWORK, MESSENGER, WHATSAPP, OCULUS, THREADS, STREAMING_SERVICES. (optional) 
            var mediaType = "ALL";  // string? | Meta only. (optional) 
            var languages = "languages_example";  // string? | Meta only. Comma-separated ISO 639-1 codes of the ad text. (optional) 
            var since = DateOnly.Parse("2013-10-20");  // DateOnly? | Earliest delivery date (YYYY-MM-DD). (optional) 
            var until = DateOnly.Parse("2013-10-20");  // DateOnly? | Latest delivery date (YYYY-MM-DD). (optional) 
            var searchType = "KEYWORD_UNORDERED";  // string? | Meta only. Whether q matches words in any order or as an exact phrase (comma-separate phrases to match all of them). (optional)  (default to KEYWORD_UNORDERED)
            var fields = "fields_example";  // string? | Meta only. Raw Graph projection override, e.g. add spend,impressions,demographic_distribution for political ads. (optional) 
            var limit = 25;  // int? | Rows per page. LinkedIn accepts at most 25. (optional)  (default to 25)
            var after = "after_example";  // string? | paging.after of the previous page. (optional) 

            try
            {
                // Search the public Ad Library
                SearchAdLibrary200Response result = apiInstance.SearchAdLibrary(platform, accountId, q, pageIds, advertiser, countries, adType, status, platforms, mediaType, languages, since, until, searchType, fields, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdLibraryApi.SearchAdLibrary: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchAdLibraryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search the public Ad Library
    ApiResponse<SearchAdLibrary200Response> response = apiInstance.SearchAdLibraryWithHttpInfo(platform, accountId, q, pageIds, advertiser, countries, adType, status, platforms, mediaType, languages, since, until, searchType, fields, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdLibraryApi.SearchAdLibraryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **platform** | **string?** | Which archive to search. &#x60;meta&#x60; needs no accountId. Required unless accountId is given. | [optional]  |
| **accountId** | **string?** | Zernio SocialAccount id. Required for LinkedIn (linkedin / linkedinads: its token searches). Optional for Meta, where any facebook / instagram / metaads account only selects the platform. | [optional]  |
| **q** | **string?** | Keyword search. Meta does not translate it, so write it in the ads&#39; language. Required unless pageIds (Meta) or advertiser (LinkedIn) is given. | [optional]  |
| **pageIds** | **string?** | Meta only. Comma-separated Facebook Page ids (max 10) whose ads to list. | [optional]  |
| **advertiser** | **string?** | LinkedIn only. Advertiser (Page) name to search. | [optional]  |
| **countries** | **string?** | Comma-separated ISO 3166-1 alpha-2 codes the ads reached. Meta defaults to ALL (an explicit ALL is Meta-only); LinkedIn searches every market when omitted. | [optional]  |
| **adType** | **string?** | Meta only. | [optional] [default to ALL] |
| **status** | **string?** | Meta only. ACTIVE &#x3D; eligible for delivery right now. | [optional] [default to ACTIVE] |
| **platforms** | **string?** | Meta only. Comma-separated publisher platforms: FACEBOOK, INSTAGRAM, AUDIENCE_NETWORK, MESSENGER, WHATSAPP, OCULUS, THREADS, STREAMING_SERVICES. | [optional]  |
| **mediaType** | **string?** | Meta only. | [optional]  |
| **languages** | **string?** | Meta only. Comma-separated ISO 639-1 codes of the ad text. | [optional]  |
| **since** | **DateOnly?** | Earliest delivery date (YYYY-MM-DD). | [optional]  |
| **until** | **DateOnly?** | Latest delivery date (YYYY-MM-DD). | [optional]  |
| **searchType** | **string?** | Meta only. Whether q matches words in any order or as an exact phrase (comma-separate phrases to match all of them). | [optional] [default to KEYWORD_UNORDERED] |
| **fields** | **string?** | Meta only. Raw Graph projection override, e.g. add spend,impressions,demographic_distribution for political ads. | [optional]  |
| **limit** | **int?** | Rows per page. LinkedIn accepts at most 25. | [optional] [default to 25] |
| **after** | **string?** | paging.after of the previous page. | [optional]  |

### Return type

[**SearchAdLibrary200Response**](SearchAdLibrary200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **200** | Archived ads (raw platform shape) |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (legacy plans need the Ads add-on; included on usage-based plans), or &#x60;payment_required&#x60;: the billing owner has no payment method on file and no legacy paid plan. Searches are free; the card keeps the shared archive quota for real accounts. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **501** | Only supported on Meta and LinkedIn accounts |  -  |
| **503** | Meta&#39;s Ad Library is unavailable on Zernio&#39;s side (&#x60;PLATFORM_DISABLED&#x60;); LinkedIn searches are unaffected. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

