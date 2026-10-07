# Zernio.Api.RedditSearchApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetRedditFeed**](RedditSearchApi.md#getredditfeed) | **GET** /v1/reddit/feed | Get subreddit feed |
| [**GetRedditPostComments**](RedditSearchApi.md#getredditpostcomments) | **GET** /v1/reddit/comments/{postId} | Get the comments of a Reddit post |
| [**SearchReddit**](RedditSearchApi.md#searchreddit) | **GET** /v1/reddit/search | Search posts |

<a id="getredditfeed"></a>
# **GetRedditFeed**
> SearchReddit200Response GetRedditFeed (string accountId, string? subreddit = null, string? sort = null, int? limit = null, string? after = null, string? t = null)

Get subreddit feed

Fetch posts from a subreddit feed. Supports sorting, time filtering, and cursor-based pagination.

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
    public class GetRedditFeedExample
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
            var apiInstance = new RedditSearchApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var subreddit = "subreddit_example";  // string? |  (optional) 
            var sort = "hot";  // string? |  (optional)  (default to hot)
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string? |  (optional) 
            var t = "hour";  // string? |  (optional) 

            try
            {
                // Get subreddit feed
                SearchReddit200Response result = apiInstance.GetRedditFeed(accountId, subreddit, sort, limit, after, t);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditSearchApi.GetRedditFeed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetRedditFeedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get subreddit feed
    ApiResponse<SearchReddit200Response> response = apiInstance.GetRedditFeedWithHttpInfo(accountId, subreddit, sort, limit, after, t);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditSearchApi.GetRedditFeedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **subreddit** | **string?** |  | [optional]  |
| **sort** | **string?** |  | [optional] [default to hot] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string?** |  | [optional]  |
| **t** | **string?** |  | [optional]  |

### Return type

[**SearchReddit200Response**](SearchReddit200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Feed items |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | No active Reddit account with this ID is available to the API key. It may have been disconnected or deleted, or it belongs to a profile the key cannot access. Re-connecting an account issues a NEW account ID, so an ID stored from before a reconnect will not resolve.  |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted.  Reddit rate-limits per connected Reddit user (1000 requests per 10-minute window), and that budget is shared by every operation using that account. Retry after the window resets rather than retrying immediately; repeated calls while exhausted do not succeed and keep the budget spent.  Google Ads: writes and reports run on one developer token shared by every Google Ads account on Zernio. The token holds Standard access (no daily operations cap), so this only happens when Google throttles the token or your ad account. The envelope has &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60; (&#x60;ACCOUNT&#x60; when it is your own ad account&#39;s quota), &#x60;details.resetsAt&#x60; (ISO instant when Google accepts requests again) and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed.  Meta ads: every Meta throttle (codes 4, 17, 32, 613 and the business-use-case codes 80000-80014) returns 429 &#x60;rate_limited&#x60;, even when Meta itself answers HTTP 400. &#x60;Retry-After&#x60; comes from Meta&#39;s &#x60;x-business-use-case-usage&#x60; estimate when Meta sends one, otherwise it is Meta&#39;s documented 60-second minimum (30 seconds for the one-write-per-30-seconds limit on a single object).  |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getredditpostcomments"></a>
# **GetRedditPostComments**
> GetRedditPostComments200Response GetRedditPostComments (string postId, string accountId, string? sort = null, int? limit = null, string? commentId = null)

Get the comments of a Reddit post

Reads the comments of any Reddit post the connected account can see, for example one found through `/v1/reddit/feed` or `/v1/reddit/search`, straight from Reddit on every call. The tree comes flattened in thread order (a reply follows its parent); rebuild it from `parentId`, which is `t3_…` for a reply to the post and `t1_…` for a reply to a comment. Deleted and removed comments are passed through as Reddit sends them (`[deleted]` / `[removed]`). Where Reddit truncates a thread, the ids it left out are listed in `more`; `commentId` fetches one such comment with its replies. A post Reddit no longer serves answers 404 and a private subreddit 403, both with `platform_api_error`. For comments on posts published through Zernio, `/v1/inbox/comments/{postId}` adds caching, moderation and replies. 

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
    public class GetRedditPostCommentsExample
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
            var apiInstance = new RedditSearchApi(httpClient, config, httpClientHandler);
            var postId = "postId_example";  // string | Reddit post id, with or without the `t3_` prefix (as `id` or `fullname` on RedditPost).
            var accountId = "accountId_example";  // string | An active Reddit account the request is made as.
            var sort = "new";  // string? |  (optional)  (default to new)
            var limit = 25;  // int? | Maximum number of top-level comments. (optional)  (default to 25)
            var commentId = "commentId_example";  // string? | Return only this comment and its replies, with or without the `t1_` prefix; pass an id from `more` to expand it. (optional) 

            try
            {
                // Get the comments of a Reddit post
                GetRedditPostComments200Response result = apiInstance.GetRedditPostComments(postId, accountId, sort, limit, commentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditSearchApi.GetRedditPostComments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetRedditPostCommentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get the comments of a Reddit post
    ApiResponse<GetRedditPostComments200Response> response = apiInstance.GetRedditPostCommentsWithHttpInfo(postId, accountId, sort, limit, commentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditSearchApi.GetRedditPostCommentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **postId** | **string** | Reddit post id, with or without the &#x60;t3_&#x60; prefix (as &#x60;id&#x60; or &#x60;fullname&#x60; on RedditPost). |  |
| **accountId** | **string** | An active Reddit account the request is made as. |  |
| **sort** | **string?** |  | [optional] [default to new] |
| **limit** | **int?** | Maximum number of top-level comments. | [optional] [default to 25] |
| **commentId** | **string?** | Return only this comment and its replies, with or without the &#x60;t1_&#x60; prefix; pass an id from &#x60;more&#x60; to expand it. | [optional]  |

### Return type

[**GetRedditPostComments200Response**](GetRedditPostComments200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The post and its comments |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Reddit refused the thread, typically a private or quarantined subreddit (&#x60;platform_api_error&#x60;). |  -  |
| **404** | Either no active Reddit account with this ID is available to the API key (&#x60;account_not_found&#x60;), or Reddit no longer serves the post, for example because it was deleted (&#x60;platform_api_error&#x60;).  |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted.  Reddit rate-limits per connected Reddit user (1000 requests per 10-minute window), and that budget is shared by every operation using that account. Retry after the window resets rather than retrying immediately; repeated calls while exhausted do not succeed and keep the budget spent.  Google Ads: writes and reports run on one developer token shared by every Google Ads account on Zernio. The token holds Standard access (no daily operations cap), so this only happens when Google throttles the token or your ad account. The envelope has &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60; (&#x60;ACCOUNT&#x60; when it is your own ad account&#39;s quota), &#x60;details.resetsAt&#x60; (ISO instant when Google accepts requests again) and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed.  Meta ads: every Meta throttle (codes 4, 17, 32, 613 and the business-use-case codes 80000-80014) returns 429 &#x60;rate_limited&#x60;, even when Meta itself answers HTTP 400. &#x60;Retry-After&#x60; comes from Meta&#39;s &#x60;x-business-use-case-usage&#x60; estimate when Meta sends one, otherwise it is Meta&#39;s documented 60-second minimum (30 seconds for the one-write-per-30-seconds limit on a single object).  |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="searchreddit"></a>
# **SearchReddit**
> SearchReddit200Response SearchReddit (string accountId, string q, string? subreddit = null, string? restrictSr = null, string? sort = null, int? limit = null, string? after = null)

Search posts

Search Reddit posts using a connected account. Optionally scope to a specific subreddit.

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
    public class SearchRedditExample
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
            var apiInstance = new RedditSearchApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var q = "q_example";  // string | 
            var subreddit = "subreddit_example";  // string? |  (optional) 
            var restrictSr = "0";  // string? |  (optional) 
            var sort = "relevance";  // string? |  (optional)  (default to new)
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string? |  (optional) 

            try
            {
                // Search posts
                SearchReddit200Response result = apiInstance.SearchReddit(accountId, q, subreddit, restrictSr, sort, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditSearchApi.SearchReddit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchRedditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search posts
    ApiResponse<SearchReddit200Response> response = apiInstance.SearchRedditWithHttpInfo(accountId, q, subreddit, restrictSr, sort, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditSearchApi.SearchRedditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **q** | **string** |  |  |
| **subreddit** | **string?** |  | [optional]  |
| **restrictSr** | **string?** |  | [optional]  |
| **sort** | **string?** |  | [optional] [default to new] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string?** |  | [optional]  |

### Return type

[**SearchReddit200Response**](SearchReddit200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Search results |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | No active Reddit account with this ID is available to the API key. It may have been disconnected or deleted, or it belongs to a profile the key cannot access. Re-connecting an account issues a NEW account ID, so an ID stored from before a reconnect will not resolve.  |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted.  Reddit rate-limits per connected Reddit user (1000 requests per 10-minute window), and that budget is shared by every operation using that account. Retry after the window resets rather than retrying immediately; repeated calls while exhausted do not succeed and keep the budget spent.  Google Ads: writes and reports run on one developer token shared by every Google Ads account on Zernio. The token holds Standard access (no daily operations cap), so this only happens when Google throttles the token or your ad account. The envelope has &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60; (&#x60;ACCOUNT&#x60; when it is your own ad account&#39;s quota), &#x60;details.resetsAt&#x60; (ISO instant when Google accepts requests again) and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed.  Meta ads: every Meta throttle (codes 4, 17, 32, 613 and the business-use-case codes 80000-80014) returns 429 &#x60;rate_limited&#x60;, even when Meta itself answers HTTP 400. &#x60;Retry-After&#x60; comes from Meta&#39;s &#x60;x-business-use-case-usage&#x60; estimate when Meta sends one, otherwise it is Meta&#39;s documented 60-second minimum (30 seconds for the one-write-per-30-seconds limit on a single object).  |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

