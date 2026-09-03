# Zernio.Api.AccountsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteAccount**](AccountsApi.md#deleteaccount) | **DELETE** /v1/accounts/{accountId} | Disconnect account |
| [**GetAccountHealth**](AccountsApi.md#getaccounthealth) | **GET** /v1/accounts/{accountId}/health | Check account health |
| [**GetAccountPosts**](AccountsApi.md#getaccountposts) | **GET** /v1/accounts/{accountId}/posts | List posts published on the platform |
| [**GetAllAccountsHealth**](AccountsApi.md#getallaccountshealth) | **GET** /v1/accounts/health | Check accounts health |
| [**GetBlueskySettings**](AccountsApi.md#getblueskysettings) | **GET** /v1/accounts/{accountId}/bluesky-settings | Get Bluesky account settings |
| [**GetFollowerStats**](AccountsApi.md#getfollowerstats) | **GET** /v1/accounts/follower-stats | Get follower stats |
| [**GetInstagramFollowStatus**](AccountsApi.md#getinstagramfollowstatus) | **GET** /v1/accounts/{accountId}/follow-status/{userId} | Check whether an Instagram user follows the account |
| [**GetSlackSettings**](AccountsApi.md#getslacksettings) | **GET** /v1/accounts/{accountId}/slack-settings | Get Slack account settings |
| [**GetTikTokCreatorInfo**](AccountsApi.md#gettiktokcreatorinfo) | **GET** /v1/accounts/{accountId}/tiktok/creator-info | Get TikTok creator info |
| [**ListAccounts**](AccountsApi.md#listaccounts) | **GET** /v1/accounts | List accounts |
| [**MoveAccountToProfile**](AccountsApi.md#moveaccounttoprofile) | **PATCH** /v1/accounts/{accountId} | Move account to another profile |
| [**UpdateAccount**](AccountsApi.md#updateaccount) | **PUT** /v1/accounts/{accountId} | Update account |
| [**UpdateBlueskySettings**](AccountsApi.md#updateblueskysettings) | **PATCH** /v1/accounts/{accountId}/bluesky-settings | Update Bluesky account settings |
| [**UpdateSlackSettings**](AccountsApi.md#updateslacksettings) | **PATCH** /v1/accounts/{accountId}/slack-settings | Update Slack account settings |

<a id="deleteaccount"></a>
# **DeleteAccount**
> DeleteAccountGroup200Response DeleteAccount (string accountId)

Disconnect account

Disconnects and removes a connected social account. Repeating the call for an account already disconnected returns 404, the account stays in its 1h grace window and the disconnect is not re-run.

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
    public class DeleteAccountExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Disconnect account
                DeleteAccountGroup200Response result = apiInstance.DeleteAccount(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.DeleteAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Disconnect account
    ApiResponse<DeleteAccountGroup200Response> response = apiInstance.DeleteAccountWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.DeleteAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**DeleteAccountGroup200Response**](DeleteAccountGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Disconnected |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getaccounthealth"></a>
# **GetAccountHealth**
> GetAccountHealth200Response GetAccountHealth (string accountId)

Check account health

Returns detailed health info for a specific account including token status, permissions, and recommendations.  For WhatsApp accounts the response also includes `platformConnection`, a live probe of the Meta link behind the channel (the same read as `GET /v1/whatsapp/number-info`). The OAuth token can be perfectly valid while Meta refuses to serve the phone-number object (for example after a phone-side coexistence disconnect), so `tokenStatus` alone is not a liveness signal for WhatsApp. When the Meta link is dead, `platformConnection.status` is `disconnected` and the overall `status` is `error`. 

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
    public class GetAccountHealthExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The account ID to check

            try
            {
                // Check account health
                GetAccountHealth200Response result = apiInstance.GetAccountHealth(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.GetAccountHealth: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAccountHealthWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check account health
    ApiResponse<GetAccountHealth200Response> response = apiInstance.GetAccountHealthWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.GetAccountHealthWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The account ID to check |  |

### Return type

[**GetAccountHealth200Response**](GetAccountHealth200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account health details |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getaccountposts"></a>
# **GetAccountPosts**
> GetAccountPosts200Response GetAccountPosts (string accountId)

List posts published on the platform

Returns the 25 most recent posts that exist on the platform for a connected account, read live from the platform API. This covers everything on the account, including posts that were never created through Zernio.  Use it to obtain the platform's own post id, which the analytics endpoints take as input. On YouTube the returned `id` is the video ID that `GET /v1/analytics/youtube/daily-views`, `/video-retention` and `/demographics` expect as `videoId`, so this endpoint is what backs a video picker in your own UI.  Not every field applies to every platform: `reactionCount` is Facebook and LinkedIn, `shareCount` is platform dependent, `cid` is the Bluesky content id needed to reply, and `subreddit` is Reddit only. Absent fields are omitted from the response.  The account's token is refreshed before the call when it has expired. When the refresh cannot recover it, the response is a 401 with code `TOKEN_EXPIRED` and the account has to be reconnected. 

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
    public class GetAccountPostsExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // List posts published on the platform
                GetAccountPosts200Response result = apiInstance.GetAccountPosts(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.GetAccountPosts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAccountPostsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List posts published on the platform
    ApiResponse<GetAccountPosts200Response> response = apiInstance.GetAccountPostsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.GetAccountPostsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetAccountPosts200Response**](GetAccountPosts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Posts list |  -  |
| **400** | Invalid accountId, platform does not support posts listing, or the account has no access token |  -  |
| **401** | Unauthorized |  -  |
| **403** | X analytics capability not enabled for this account (code X_ANALYTICS_NOT_ENABLED) |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getallaccountshealth"></a>
# **GetAllAccountsHealth**
> GetAllAccountsHealth200Response GetAllAccountsHealth (string? profileId = null, string? platform = null, string? status = null)

Check accounts health

Returns health status of all connected accounts including token validity, permissions, and issues needing attention.

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
    public class GetAllAccountsHealthExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? | Filter by profile ID (optional) 
            var platform = "facebook";  // string? | Filter by platform (optional) 
            var status = "healthy";  // string? | Filter by health status (optional) 

            try
            {
                // Check accounts health
                GetAllAccountsHealth200Response result = apiInstance.GetAllAccountsHealth(profileId, platform, status);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.GetAllAccountsHealth: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllAccountsHealthWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check accounts health
    ApiResponse<GetAllAccountsHealth200Response> response = apiInstance.GetAllAccountsHealthWithHttpInfo(profileId, platform, status);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.GetAllAccountsHealthWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** | Filter by profile ID | [optional]  |
| **platform** | **string?** | Filter by platform | [optional]  |
| **status** | **string?** | Filter by health status | [optional]  |

### Return type

[**GetAllAccountsHealth200Response**](GetAllAccountsHealth200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account health summary |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getblueskysettings"></a>
# **GetBlueskySettings**
> GetBlueskySettings200Response GetBlueskySettings (string accountId)

Get Bluesky account settings

Returns the account's default post languages (defaultLangs), applied at publish time whenever a post's platformSpecificData.langs is absent. Null when no default is set.

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
    public class GetBlueskySettingsExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get Bluesky account settings
                GetBlueskySettings200Response result = apiInstance.GetBlueskySettings(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.GetBlueskySettings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBlueskySettingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Bluesky account settings
    ApiResponse<GetBlueskySettings200Response> response = apiInstance.GetBlueskySettingsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.GetBlueskySettingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetBlueskySettings200Response**](GetBlueskySettings200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Bluesky account settings |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getfollowerstats"></a>
# **GetFollowerStats**
> FollowerStatsResponse GetFollowerStats (string? accountIds = null, string? profileId = null, DateOnly? fromDate = null, DateOnly? toDate = null, string? granularity = null)

Get follower stats

Returns follower count history and growth metrics for connected social accounts. Requires analytics add-on subscription. Follower counts are refreshed once per day. 

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
    public class GetFollowerStatsExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var accountIds = "accountIds_example";  // string? | Comma-separated list of account IDs (optional, defaults to all user's accounts) (optional) 
            var profileId = "profileId_example";  // string? | Filter by profile ID (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Start date in YYYY-MM-DD format (defaults to 30 days ago) (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | End date in YYYY-MM-DD format (defaults to today) (optional) 
            var granularity = "daily";  // string? | Data aggregation level (optional)  (default to daily)

            try
            {
                // Get follower stats
                FollowerStatsResponse result = apiInstance.GetFollowerStats(accountIds, profileId, fromDate, toDate, granularity);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.GetFollowerStats: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFollowerStatsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get follower stats
    ApiResponse<FollowerStatsResponse> response = apiInstance.GetFollowerStatsWithHttpInfo(accountIds, profileId, fromDate, toDate, granularity);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.GetFollowerStatsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountIds** | **string?** | Comma-separated list of account IDs (optional, defaults to all user&#39;s accounts) | [optional]  |
| **profileId** | **string?** | Filter by profile ID | [optional]  |
| **fromDate** | **DateOnly?** | Start date in YYYY-MM-DD format (defaults to 30 days ago) | [optional]  |
| **toDate** | **DateOnly?** | End date in YYYY-MM-DD format (defaults to today) | [optional]  |
| **granularity** | **string?** | Data aggregation level | [optional] [default to daily] |

### Return type

[**FollowerStatsResponse**](FollowerStatsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Follower stats |  -  |
| **401** | Unauthorized |  -  |
| **403** | Analytics access required. Legacy plans need the Analytics add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getinstagramfollowstatus"></a>
# **GetInstagramFollowStatus**
> GetInstagramFollowStatus200Response GetInstagramFollowStatus (string accountId, string userId, bool? refresh = null)

Check whether an Instagram user follows the account

Resolves the follow relationship between an Instagram user and the connected account, plus their public profile counters.  `userId` is the Instagram-scoped id (IGSID) Meta gives you on a webhook: `sender.id` on `message.received`, `comment.author.id` on `comment.received`.  **Meta only answers for people who have MESSAGED the account.** Commenting grants no consent, so a commenter who has never DMed you is unresolvable - that is a platform rule, not a limitation of this endpoint. When it cannot be resolved the response is still `200` with `isFollower: null` and an `unavailableReason`, because \"unknown\" is a normal state to branch on:    * `consent_required` - the user has never messaged this account.   * `dm_access_disabled` - the account owner turned off Instagram Direct API access.   * `not_messageable` - the id is not a messaging-scoped id.   * `error` - a transient Graph API failure.  To gate a comment automation on this, use the automation's `audience` rules instead of calling this per comment - they run the same lookup only on comments that actually match a keyword, and can ask the commenter to confirm with one tap.  Answers are cached briefly per (account, user). Pass `refresh=true` right after asking someone to follow, so a follow from a moment ago is visible. 

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
    public class GetInstagramFollowStatusExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Instagram account ID
            var userId = "userId_example";  // string | Instagram-scoped user id (IGSID) from a webhook payload
            var refresh = true;  // bool? | Bypass the cache and re-query Meta (optional) 

            try
            {
                // Check whether an Instagram user follows the account
                GetInstagramFollowStatus200Response result = apiInstance.GetInstagramFollowStatus(accountId, userId, refresh);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.GetInstagramFollowStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInstagramFollowStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check whether an Instagram user follows the account
    ApiResponse<GetInstagramFollowStatus200Response> response = apiInstance.GetInstagramFollowStatusWithHttpInfo(accountId, userId, refresh);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.GetInstagramFollowStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Instagram account ID |  |
| **userId** | **string** | Instagram-scoped user id (IGSID) from a webhook payload |  |
| **refresh** | **bool?** | Bypass the cache and re-query Meta | [optional]  |

### Return type

[**GetInstagramFollowStatus200Response**](GetInstagramFollowStatus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Follow status (fields are null when Meta would not resolve it) |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getslacksettings"></a>
# **GetSlackSettings**
> GetSlackSettings200Response GetSlackSettings (string accountId)

Get Slack account settings

Returns the connected Slack channel details and the default message identity (name and avatar shown as the author on every post, with Slack's APP badge). The identity applies to messages only; the app's own Slack profile is global and cannot be changed per workspace.

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
    public class GetSlackSettingsExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get Slack account settings
                GetSlackSettings200Response result = apiInstance.GetSlackSettings(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.GetSlackSettings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSlackSettingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Slack account settings
    ApiResponse<GetSlackSettings200Response> response = apiInstance.GetSlackSettingsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.GetSlackSettingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetSlackSettings200Response**](GetSlackSettings200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Slack account settings |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettiktokcreatorinfo"></a>
# **GetTikTokCreatorInfo**
> GetTikTokCreatorInfo200Response GetTikTokCreatorInfo (string accountId, string? mediaType = null)

Get TikTok creator info

Returns TikTok creator details, available privacy levels, posting limits, and commercial content options for a specific TikTok account. Only works with TikTok accounts.

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
    public class GetTikTokCreatorInfoExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The TikTok account ID
            var mediaType = "video";  // string? | The media type to get creator info for (affects available interaction settings) (optional)  (default to video)

            try
            {
                // Get TikTok creator info
                GetTikTokCreatorInfo200Response result = apiInstance.GetTikTokCreatorInfo(accountId, mediaType);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.GetTikTokCreatorInfo: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTikTokCreatorInfoWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get TikTok creator info
    ApiResponse<GetTikTokCreatorInfo200Response> response = apiInstance.GetTikTokCreatorInfoWithHttpInfo(accountId, mediaType);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.GetTikTokCreatorInfoWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The TikTok account ID |  |
| **mediaType** | **string?** | The media type to get creator info for (affects available interaction settings) | [optional] [default to video] |

### Return type

[**GetTikTokCreatorInfo200Response**](GetTikTokCreatorInfo200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | TikTok creator info and posting options |  -  |
| **400** | Account is not a TikTok account |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **429** | Creator has reached TikTok daily posting limit |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listaccounts"></a>
# **ListAccounts**
> AccountsListResponse ListAccounts (string? profileId = null, string? platform = null, string? status = null, bool? includeOverLimit = null, int? page = null, int? limit = null)

List accounts

Returns connected social accounts. Only includes accounts within the plan limit by default. Follower data requires analytics add-on. Supports optional server-side pagination via page/limit params. When omitted, returns all accounts (backward-compatible). page and limit must be supplied together; out-of-range page/limit values are rejected with 400 rather than silently clamped. 

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
    public class ListAccountsExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? | Filter accounts by profile ID. Must be a valid ObjectId. (optional) 
            var platform = "platform_example";  // string? | Filter accounts by platform (e.g. \"instagram\", \"twitter\"). (optional) 
            var status = "connected";  // string? | Filter accounts by connection status. `connected` returns healthy accounts; `disconnected` returns accounts that need reconnection (per the same reconnection check surfaced in the dashboard). Omit to return accounts in any status. When combined with page/limit, pagination totals reflect the filtered result set.  (optional) 
            var includeOverLimit = false;  // bool? | When true, includes accounts from over-limit profiles. (optional)  (default to false)
            var page = 56;  // int? | Page number (1-based). Must be provided together with limit to enable server-side pagination; sending only one of the two returns 400. Omit both for all accounts.  (optional) 
            var limit = 56;  // int? | Page size. Must be provided together with page; sending only one of the two returns 400.  (optional) 

            try
            {
                // List accounts
                AccountsListResponse result = apiInstance.ListAccounts(profileId, platform, status, includeOverLimit, page, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.ListAccounts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAccountsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List accounts
    ApiResponse<AccountsListResponse> response = apiInstance.ListAccountsWithHttpInfo(profileId, platform, status, includeOverLimit, page, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.ListAccountsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** | Filter accounts by profile ID. Must be a valid ObjectId. | [optional]  |
| **platform** | **string?** | Filter accounts by platform (e.g. \&quot;instagram\&quot;, \&quot;twitter\&quot;). | [optional]  |
| **status** | **string?** | Filter accounts by connection status. &#x60;connected&#x60; returns healthy accounts; &#x60;disconnected&#x60; returns accounts that need reconnection (per the same reconnection check surfaced in the dashboard). Omit to return accounts in any status. When combined with page/limit, pagination totals reflect the filtered result set.  | [optional]  |
| **includeOverLimit** | **bool?** | When true, includes accounts from over-limit profiles. | [optional] [default to false] |
| **page** | **int?** | Page number (1-based). Must be provided together with limit to enable server-side pagination; sending only one of the two returns 400. Omit both for all accounts.  | [optional]  |
| **limit** | **int?** | Page size. Must be provided together with page; sending only one of the two returns 400.  | [optional]  |

### Return type

[**AccountsListResponse**](AccountsListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Accounts (with optional pagination) |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="moveaccounttoprofile"></a>
# **MoveAccountToProfile**
> MoveAccountToProfile200Response MoveAccountToProfile (string accountId, MoveAccountToProfileRequest moveAccountToProfileRequest)

Move account to another profile

Moves a connected social account to a different profile owned by the same user. The target profile must belong to the same user as the account.  For API keys restricted to specific profiles, BOTH the source account's current profile AND the target profile must be in the key's allowed set. Calls with a target profile outside the key's scope return 403. 

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
    public class MoveAccountToProfileExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var moveAccountToProfileRequest = new MoveAccountToProfileRequest(); // MoveAccountToProfileRequest | 

            try
            {
                // Move account to another profile
                MoveAccountToProfile200Response result = apiInstance.MoveAccountToProfile(accountId, moveAccountToProfileRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.MoveAccountToProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MoveAccountToProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Move account to another profile
    ApiResponse<MoveAccountToProfile200Response> response = apiInstance.MoveAccountToProfileWithHttpInfo(accountId, moveAccountToProfileRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.MoveAccountToProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **moveAccountToProfileRequest** | [**MoveAccountToProfileRequest**](MoveAccountToProfileRequest.md) |  |  |

### Return type

[**MoveAccountToProfile200Response**](MoveAccountToProfile200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account moved |  -  |
| **400** | Missing or invalid profileId |  -  |
| **401** | Unauthorized |  -  |
| **403** | API key does not have access to the source account or target profile |  -  |
| **404** | Account or target profile not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateaccount"></a>
# **UpdateAccount**
> UpdateAccount200Response UpdateAccount (string accountId, UpdateAccountRequest updateAccountRequest)

Update account

Updates a connected social account's display name or username override.  For X/Twitter accounts on usage-based billing, also accepts an `xCapabilities` object to toggle background API operations that incur X API pass-through costs. Both fields are opt-in (default `false`) — when off, no analytics syncs or DM polling are performed for that account, and no API call is metered for those operations. Publishing and deleting posts are always available regardless of these toggles. Setting `xCapabilities` on a non-X account returns 400. 

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
    public class UpdateAccountExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var updateAccountRequest = new UpdateAccountRequest(); // UpdateAccountRequest | 

            try
            {
                // Update account
                UpdateAccount200Response result = apiInstance.UpdateAccount(accountId, updateAccountRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.UpdateAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update account
    ApiResponse<UpdateAccount200Response> response = apiInstance.UpdateAccountWithHttpInfo(accountId, updateAccountRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.UpdateAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **updateAccountRequest** | [**UpdateAccountRequest**](UpdateAccountRequest.md) |  |  |

### Return type

[**UpdateAccount200Response**](UpdateAccount200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated |  -  |
| **400** | Invalid request (e.g. xCapabilities on a non-X account) |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateblueskysettings"></a>
# **UpdateBlueskySettings**
> void UpdateBlueskySettings (string accountId, UpdateBlueskySettingsRequest updateBlueskySettingsRequest)

Update Bluesky account settings

Set or clear the account's default post languages. 1-3 BCP-47 codes (e.g. \"pt\", \"en-US\"), the same validation as per-post langs; explicit null clears the default. Per-post platformSpecificData.langs always overrides this default. Applies to posts published after the change; already-published posts cannot be retagged (Bluesky has no post edit).

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
    public class UpdateBlueskySettingsExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var updateBlueskySettingsRequest = new UpdateBlueskySettingsRequest(); // UpdateBlueskySettingsRequest | 

            try
            {
                // Update Bluesky account settings
                apiInstance.UpdateBlueskySettings(accountId, updateBlueskySettingsRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.UpdateBlueskySettings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBlueskySettingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Bluesky account settings
    apiInstance.UpdateBlueskySettingsWithHttpInfo(accountId, updateBlueskySettingsRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.UpdateBlueskySettingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **updateBlueskySettingsRequest** | [**UpdateBlueskySettingsRequest**](UpdateBlueskySettingsRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated settings |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateslacksettings"></a>
# **UpdateSlackSettings**
> void UpdateSlackSettings (string accountId, UpdateSlackSettingsRequest updateSlackSettingsRequest)

Update Slack account settings

Set or clear the default message identity for this channel. Empty string clears a field; per-post platformSpecificData.username/iconUrl still override these defaults.

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
    public class UpdateSlackSettingsExample
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
            var apiInstance = new AccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var updateSlackSettingsRequest = new UpdateSlackSettingsRequest(); // UpdateSlackSettingsRequest | 

            try
            {
                // Update Slack account settings
                apiInstance.UpdateSlackSettings(accountId, updateSlackSettingsRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountsApi.UpdateSlackSettings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateSlackSettingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Slack account settings
    apiInstance.UpdateSlackSettingsWithHttpInfo(accountId, updateSlackSettingsRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountsApi.UpdateSlackSettingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **updateSlackSettingsRequest** | [**UpdateSlackSettingsRequest**](UpdateSlackSettingsRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated settings |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

