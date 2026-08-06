# Zernio.Api.TwitterEngagementApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BookmarkPost**](TwitterEngagementApi.md#bookmarkpost) | **POST** /v1/twitter/bookmark | Bookmark a tweet |
| [**FollowUser**](TwitterEngagementApi.md#followuser) | **POST** /v1/twitter/follow | Follow a user |
| [**GetTweet**](TwitterEngagementApi.md#gettweet) | **GET** /v1/twitter/tweet | Look up a tweet |
| [**RemoveBookmark**](TwitterEngagementApi.md#removebookmark) | **DELETE** /v1/twitter/bookmark | Remove bookmark |
| [**RetweetPost**](TwitterEngagementApi.md#retweetpost) | **POST** /v1/twitter/retweet | Retweet a post |
| [**SearchTweets**](TwitterEngagementApi.md#searchtweets) | **GET** /v1/twitter/search | Search recent tweets |
| [**UndoRetweet**](TwitterEngagementApi.md#undoretweet) | **DELETE** /v1/twitter/retweet | Undo retweet |
| [**UnfollowUser**](TwitterEngagementApi.md#unfollowuser) | **DELETE** /v1/twitter/follow | Unfollow a user |

<a id="bookmarkpost"></a>
# **BookmarkPost**
> BookmarkPost200Response BookmarkPost (BookmarkPostRequest bookmarkPostRequest)

Bookmark a tweet

Bookmark a tweet by ID. Requires the bookmark.write OAuth scope. Rate limit: 50 requests per 15-min window. 

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
    public class BookmarkPostExample
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
            var apiInstance = new TwitterEngagementApi(httpClient, config, httpClientHandler);
            var bookmarkPostRequest = new BookmarkPostRequest(); // BookmarkPostRequest | 

            try
            {
                // Bookmark a tweet
                BookmarkPost200Response result = apiInstance.BookmarkPost(bookmarkPostRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterEngagementApi.BookmarkPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BookmarkPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Bookmark a tweet
    ApiResponse<BookmarkPost200Response> response = apiInstance.BookmarkPostWithHttpInfo(bookmarkPostRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterEngagementApi.BookmarkPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **bookmarkPostRequest** | [**BookmarkPostRequest**](BookmarkPostRequest.md) |  |  |

### Return type

[**BookmarkPost200Response**](BookmarkPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tweet bookmarked |  -  |
| **400** | Bad request or platform limitation |  -  |
| **401** | Unauthorized |  -  |
| **403** | X rejected the request (e.g. suspended account, missing OAuth scope) |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="followuser"></a>
# **FollowUser**
> FollowUser200Response FollowUser (FollowUserRequest followUserRequest)

Follow a user

Follow a user on X/Twitter. Requires the follows.write OAuth scope. For protected accounts, a follow request is sent instead (pending_follow will be true). 

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
    public class FollowUserExample
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
            var apiInstance = new TwitterEngagementApi(httpClient, config, httpClientHandler);
            var followUserRequest = new FollowUserRequest(); // FollowUserRequest | 

            try
            {
                // Follow a user
                FollowUser200Response result = apiInstance.FollowUser(followUserRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterEngagementApi.FollowUser: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FollowUserWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Follow a user
    ApiResponse<FollowUser200Response> response = apiInstance.FollowUserWithHttpInfo(followUserRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterEngagementApi.FollowUserWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **followUserRequest** | [**FollowUserRequest**](FollowUserRequest.md) |  |  |

### Return type

[**FollowUser200Response**](FollowUser200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User followed or follow request sent |  -  |
| **400** | Bad request or platform limitation |  -  |
| **401** | Unauthorized |  -  |
| **403** | X rejected the request (e.g. suspended account, missing OAuth scope) |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettweet"></a>
# **GetTweet**
> GetTweet200Response GetTweet (string accountId, string id)

Look up a tweet

Resolve a single tweet by ID or URL into its text, author and public metrics.  Use this to render a post you are referencing, e.g. the tweet quoted by a quote-style post. Unlike `/v1/twitter/search` this is not limited to the last 7 days and works for any tweet visible to the connected account.  Billed as an X posts read ($0.005). Repeat lookups of the same tweet within the same UTC day are charged once. 

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
    public class GetTweetExample
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
            var apiInstance = new TwitterEngagementApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The social account ID whose X token is used for the lookup
            var id = "id_example";  // string | Numeric tweet ID or a tweet URL (e.g. https://x.com/user/status/123...)

            try
            {
                // Look up a tweet
                GetTweet200Response result = apiInstance.GetTweet(accountId, id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterEngagementApi.GetTweet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTweetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Look up a tweet
    ApiResponse<GetTweet200Response> response = apiInstance.GetTweetWithHttpInfo(accountId, id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterEngagementApi.GetTweetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The social account ID whose X token is used for the lookup |  |
| **id** | **string** | Numeric tweet ID or a tweet URL (e.g. https://x.com/user/status/123...) |  |

### Return type

[**GetTweet200Response**](GetTweet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The resolved tweet |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **402** | X API spend cap reached for this billing period |  -  |
| **403** | X analytics capability not enabled for this account (code X_ANALYTICS_NOT_ENABLED), or the tweet author is protected or suspended |  -  |
| **404** | Account not found, or the tweet was deleted or never existed |  -  |
| **429** | X rate limit exceeded |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removebookmark"></a>
# **RemoveBookmark**
> RemoveBookmark200Response RemoveBookmark (string accountId, string tweetId)

Remove bookmark

Remove a bookmark from a tweet. 

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
    public class RemoveBookmarkExample
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
            var apiInstance = new TwitterEngagementApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tweetId = "tweetId_example";  // string | The ID of the tweet to unbookmark

            try
            {
                // Remove bookmark
                RemoveBookmark200Response result = apiInstance.RemoveBookmark(accountId, tweetId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterEngagementApi.RemoveBookmark: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveBookmarkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove bookmark
    ApiResponse<RemoveBookmark200Response> response = apiInstance.RemoveBookmarkWithHttpInfo(accountId, tweetId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterEngagementApi.RemoveBookmarkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tweetId** | **string** | The ID of the tweet to unbookmark |  |

### Return type

[**RemoveBookmark200Response**](RemoveBookmark200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Bookmark removed |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | X rejected the request (e.g. suspended account, missing OAuth scope) |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="retweetpost"></a>
# **RetweetPost**
> RetweetPost200Response RetweetPost (RetweetPostRequest retweetPostRequest)

Retweet a post

Retweet (repost) a tweet by ID. Rate limit: 50 requests per 15-min window. Shares the 300/3hr creation limit with tweet creation. 

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
    public class RetweetPostExample
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
            var apiInstance = new TwitterEngagementApi(httpClient, config, httpClientHandler);
            var retweetPostRequest = new RetweetPostRequest(); // RetweetPostRequest | 

            try
            {
                // Retweet a post
                RetweetPost200Response result = apiInstance.RetweetPost(retweetPostRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterEngagementApi.RetweetPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RetweetPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retweet a post
    ApiResponse<RetweetPost200Response> response = apiInstance.RetweetPostWithHttpInfo(retweetPostRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterEngagementApi.RetweetPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **retweetPostRequest** | [**RetweetPostRequest**](RetweetPostRequest.md) |  |  |

### Return type

[**RetweetPost200Response**](RetweetPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tweet retweeted |  -  |
| **400** | Bad request or platform limitation |  -  |
| **401** | Unauthorized |  -  |
| **403** | X rejected the request (e.g. suspended account, missing OAuth scope) |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="searchtweets"></a>
# **SearchTweets**
> SearchTweets200Response SearchTweets (string accountId, string query, int? limit = null, string? sinceId = null, string? untilId = null, DateTime? startTime = null, DateTime? endTime = null, string? cursor = null, string? sortOrder = null)

Search recent tweets

Search public tweets from the last 7 days matching an X search query, e.g. to discover tweets to reply to. The query string is passed through to X unchanged and supports X's search operators (`from:user`, `-is:retweet`, `is:reply`, `lang:en`, `\"exact phrase\"`, `conversation_id:123`, boolean `OR`, ...). Note that standalone operators like `is:` / `has:` / `lang:` must be combined with a keyword or `from:` clause.  To reply to a found tweet, pass its `id` as the twitter platform entry's `platformSpecificData.replyToTweetId` when creating a post.  Rate limit: 300 requests per 15-min window per connected account. 

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
    public class SearchTweetsExample
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
            var apiInstance = new TwitterEngagementApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The social account ID
            var query = "query_example";  // string | X search query, max 512 characters. Operators are passed through unchanged; X rejects malformed queries with a 400.
            var limit = 10;  // int? | Results per page. X requires a minimum of 10; values below 10 are rejected. (optional)  (default to 10)
            var sinceId = "sinceId_example";  // string? | Only return tweets with an ID greater than (more recent than) this numeric tweet ID. Non-numeric values are rejected with 400. (optional) 
            var untilId = "untilId_example";  // string? | Only return tweets with an ID less than (older than) this numeric tweet ID. Non-numeric values are rejected with 400. (optional) 
            var startTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | Oldest UTC timestamp (ISO 8601, inclusive), within the last 7 days (optional) 
            var endTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | Newest UTC timestamp (ISO 8601, exclusive), within the last 7 days (optional) 
            var cursor = "cursor_example";  // string? | Pagination cursor from a previous response (optional) 
            var sortOrder = "recency";  // string? |  (optional)  (default to recency)

            try
            {
                // Search recent tweets
                SearchTweets200Response result = apiInstance.SearchTweets(accountId, query, limit, sinceId, untilId, startTime, endTime, cursor, sortOrder);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterEngagementApi.SearchTweets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchTweetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search recent tweets
    ApiResponse<SearchTweets200Response> response = apiInstance.SearchTweetsWithHttpInfo(accountId, query, limit, sinceId, untilId, startTime, endTime, cursor, sortOrder);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterEngagementApi.SearchTweetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The social account ID |  |
| **query** | **string** | X search query, max 512 characters. Operators are passed through unchanged; X rejects malformed queries with a 400. |  |
| **limit** | **int?** | Results per page. X requires a minimum of 10; values below 10 are rejected. | [optional] [default to 10] |
| **sinceId** | **string?** | Only return tweets with an ID greater than (more recent than) this numeric tweet ID. Non-numeric values are rejected with 400. | [optional]  |
| **untilId** | **string?** | Only return tweets with an ID less than (older than) this numeric tweet ID. Non-numeric values are rejected with 400. | [optional]  |
| **startTime** | **DateTime?** | Oldest UTC timestamp (ISO 8601, inclusive), within the last 7 days | [optional]  |
| **endTime** | **DateTime?** | Newest UTC timestamp (ISO 8601, exclusive), within the last 7 days | [optional]  |
| **cursor** | **string?** | Pagination cursor from a previous response | [optional]  |
| **sortOrder** | **string?** |  | [optional] [default to recency] |

### Return type

[**SearchTweets200Response**](SearchTweets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Matching tweets |  -  |
| **400** | Bad request (invalid params, or X rejected the query as malformed) |  -  |
| **401** | Unauthorized |  -  |
| **402** | X API spend cap reached for this billing period |  -  |
| **403** | X analytics capability not enabled for this account (code X_ANALYTICS_NOT_ENABLED) |  -  |
| **404** | Account not found |  -  |
| **429** | X search rate limit exceeded (300 requests per 15 minutes) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="undoretweet"></a>
# **UndoRetweet**
> UndoRetweet200Response UndoRetweet (string accountId, string tweetId)

Undo retweet

Undo a retweet (un-repost a tweet). 

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
    public class UndoRetweetExample
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
            var apiInstance = new TwitterEngagementApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tweetId = "tweetId_example";  // string | The ID of the original tweet to un-retweet

            try
            {
                // Undo retweet
                UndoRetweet200Response result = apiInstance.UndoRetweet(accountId, tweetId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterEngagementApi.UndoRetweet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UndoRetweetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Undo retweet
    ApiResponse<UndoRetweet200Response> response = apiInstance.UndoRetweetWithHttpInfo(accountId, tweetId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterEngagementApi.UndoRetweetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tweetId** | **string** | The ID of the original tweet to un-retweet |  |

### Return type

[**UndoRetweet200Response**](UndoRetweet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Retweet undone |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | X rejected the request (e.g. suspended account, missing OAuth scope) |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="unfollowuser"></a>
# **UnfollowUser**
> UnfollowUser200Response UnfollowUser (string accountId, string targetUserId)

Unfollow a user

Unfollow a user on X/Twitter. 

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
    public class UnfollowUserExample
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
            var apiInstance = new TwitterEngagementApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var targetUserId = "targetUserId_example";  // string | The Twitter ID of the user to unfollow

            try
            {
                // Unfollow a user
                UnfollowUser200Response result = apiInstance.UnfollowUser(accountId, targetUserId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterEngagementApi.UnfollowUser: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UnfollowUserWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Unfollow a user
    ApiResponse<UnfollowUser200Response> response = apiInstance.UnfollowUserWithHttpInfo(accountId, targetUserId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterEngagementApi.UnfollowUserWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **targetUserId** | **string** | The Twitter ID of the user to unfollow |  |

### Return type

[**UnfollowUser200Response**](UnfollowUser200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User unfollowed |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | X rejected the request (e.g. suspended account, missing OAuth scope) |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

