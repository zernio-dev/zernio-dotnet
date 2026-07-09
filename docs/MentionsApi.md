# Zernio.Api.MentionsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ListInboxMentions**](MentionsApi.md#listinboxmentions) | **GET** /v1/inbox/mentions | List mentions |
| [**ReplyToMention**](MentionsApi.md#replytomention) | **POST** /v1/inbox/mentions/reply | Reply to a mention |

<a id="listinboxmentions"></a>
# **ListInboxMentions**
> ListInboxMentions200Response ListInboxMentions (string? accountId = null, string? profileId = null, string? sortOrder = null, int? limit = null, string? cursor = null)

List mentions

Returns mentions of your connected organization accounts, delivered via platform webhooks. Currently supports LinkedIn organization mentions.  Requires Inbox addon. 

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
    public class ListInboxMentionsExample
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
            var apiInstance = new MentionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string? | Filter by social account ID (optional) 
            var profileId = "profileId_example";  // string? | Filter by profile ID (optional) 
            var sortOrder = "asc";  // string? | Sort order by publishedAt (optional)  (default to desc)
            var limit = 25;  // int? |  (optional)  (default to 25)
            var cursor = "cursor_example";  // string? | Cursor for pagination (ID of the last item from the previous page) (optional) 

            try
            {
                // List mentions
                ListInboxMentions200Response result = apiInstance.ListInboxMentions(accountId, profileId, sortOrder, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MentionsApi.ListInboxMentions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListInboxMentionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List mentions
    ApiResponse<ListInboxMentions200Response> response = apiInstance.ListInboxMentionsWithHttpInfo(accountId, profileId, sortOrder, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MentionsApi.ListInboxMentionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string?** | Filter by social account ID | [optional]  |
| **profileId** | **string?** | Filter by profile ID | [optional]  |
| **sortOrder** | **string?** | Sort order by publishedAt | [optional] [default to desc] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **cursor** | **string?** | Cursor for pagination (ID of the last item from the previous page) | [optional]  |

### Return type

[**ListInboxMentions200Response**](ListInboxMentions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated list of mentions |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox addon required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="replytomention"></a>
# **ReplyToMention**
> ReplyToMention200Response ReplyToMention (ReplyToMentionRequest replyToMentionRequest)

Reply to a mention

Reply to a mention of the connected account. Supported on Instagram only.  Two shapes, selected by whether `commentId` is present:  - **Comment mention** (someone @mentioned the account inside a comment): pass both   `mediaId` and `commentId`. Instagram posts a reply under that comment. - **Caption mention** (someone @mentioned the account in their media caption, so no   comment exists): pass `mediaId` only. Instagram posts a comment on their media.  Story mentions are not supported by Instagram's API.  Note that `GET /v1/inbox/mentions` currently returns LinkedIn mentions only and does not surface Instagram mentions. Source `mediaId` and `commentId` from Instagram's `comments` webhook, which is where mention notifications are delivered for accounts connected through Instagram Login. 

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
    public class ReplyToMentionExample
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
            var apiInstance = new MentionsApi(httpClient, config, httpClientHandler);
            var replyToMentionRequest = new ReplyToMentionRequest(); // ReplyToMentionRequest | 

            try
            {
                // Reply to a mention
                ReplyToMention200Response result = apiInstance.ReplyToMention(replyToMentionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MentionsApi.ReplyToMention: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReplyToMentionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reply to a mention
    ApiResponse<ReplyToMention200Response> response = apiInstance.ReplyToMentionWithHttpInfo(replyToMentionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MentionsApi.ReplyToMentionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **replyToMentionRequest** | [**ReplyToMentionRequest**](ReplyToMentionRequest.md) |  |  |

### Return type

[**ReplyToMention200Response**](ReplyToMention200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reply posted |  -  |
| **400** | Platform does not support replying to mentions (code: platform_not_supported), or missing mediaId/message. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account not found |  -  |
| **502** | Instagram was unreachable or returned an unclassified error. Instagram 4xx statuses are forwarded as-is. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

