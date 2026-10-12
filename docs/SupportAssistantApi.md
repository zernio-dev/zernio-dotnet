# Zernio.Api.SupportAssistantApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AskSupportQuestion**](SupportAssistantApi.md#asksupportquestion) | **POST** /v1/support/runs | Ask a support question |
| [**GetSupportAnswer**](SupportAssistantApi.md#getsupportanswer) | **GET** /v1/support/runs/{runId} | Get a support answer |
| [**ListSupportAnswers**](SupportAssistantApi.md#listsupportanswers) | **GET** /v1/support/runs | List a thread&#39;s support answers |

<a id="asksupportquestion"></a>
# **AskSupportQuestion**
> AskSupportQuestion202Response AskSupportQuestion (AskSupportQuestionRequest askSupportQuestionRequest, string? idempotencyKey = null)

Ask a support question

Asks Ana, the Zernio support agent, a question about your workspace. Each question starts a run that answers asynchronously: this returns 202 with a `runId`, and the answer arrives through the `support.run.completed` and `support.run.failed` webhooks. `GET /v1/support/runs/{runId}` is the fallback. Pass `threadId` to continue an earlier conversation, and `context` to point Ana at a post, account or profile. When Ana finds a problem on Zernio's side she opens a support ticket with the team (see `supportTicket` on the run) and the run ends as `needs_human`.  **Pricing.** Each question is billed once, when its run finishes, for the tokens Ana used:  - Input: $6 per million tokens - Output: $30 per million tokens - Cache reads: $0.60 per million tokens - Cache writes: $7.50 per million tokens  Most questions cost between $0.10 and $0.50. A run never bills more than its `maxCostUsd` ($0.50 to $3, $3 by default): near the cap Ana stops investigating and answers with what she found. Runs that end as `needs_human` are billed like any other; failed runs are free. The run's `usage` holds the token counts and `costUsd` the amount billed. Charges appear as \"Support API\" on your invoice.  Requires an unrestricted API key, usage-based billing and a card on file. Limits per account: 3 active runs and $100 of runs per UTC month. Send an Idempotency-Key header to make retries safe. 

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
    public class AskSupportQuestionExample
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
            var apiInstance = new SupportAssistantApi(httpClient, config, httpClientHandler);
            var askSupportQuestionRequest = new AskSupportQuestionRequest(); // AskSupportQuestionRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. (optional) 

            try
            {
                // Ask a support question
                AskSupportQuestion202Response result = apiInstance.AskSupportQuestion(askSupportQuestionRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupportAssistantApi.AskSupportQuestion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AskSupportQuestionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ask a support question
    ApiResponse<AskSupportQuestion202Response> response = apiInstance.AskSupportQuestionWithHttpInfo(askSupportQuestionRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupportAssistantApi.AskSupportQuestionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **askSupportQuestionRequest** | [**AskSupportQuestionRequest**](AskSupportQuestionRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. | [optional]  |

### Return type

[**AskSupportQuestion202Response**](AskSupportQuestion202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Run accepted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | A card is required (code &#x60;payment_method_required&#x60;) or the last payment failed (code &#x60;payment_required&#x60;). Add or update the card in Billing. |  -  |
| **403** | Code &#x60;insufficient_permissions&#x60;: the credential is not an unrestricted API key, or the user is read-only, restricted or profile-scoped. |  -  |
| **404** | Code &#x60;support_thread_not_found&#x60; (&#x60;threadId&#x60;), &#x60;post_not_found&#x60;, &#x60;account_not_found&#x60; or &#x60;profile_not_found&#x60; (&#x60;context.*&#x60;). |  -  |
| **409** | Code &#x60;support_run_in_progress&#x60;: the thread already has a run queued or running, so poll it first. Code &#x60;billing_setup_incomplete&#x60;: no billing customer to attach a card to, contact support. Also returned while a request with the same Idempotency-Key is still processing. |  -  |
| **422** | Code &#x60;usage_billing_required&#x60;: the Support Assistant needs a usage-based plan. Also returned when an Idempotency-Key is reused with a different request. |  -  |
| **429** | Code &#x60;support_active_runs_limit&#x60;: 3 runs are already active, retry when one finishes. Code &#x60;support_monthly_cap_exceeded&#x60;: this run could take the account past $100 for the UTC month; &#x60;Retry-After&#x60; runs until the next month starts, which can be weeks. |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getsupportanswer"></a>
# **GetSupportAnswer**
> SupportRun GetSupportAnswer (string runId)

Get a support answer

Returns a run started by your team, with Ana's answer once it is ready. Prefer the `support.run.completed` and `support.run.failed` webhooks; use this as the fallback, waiting `pollAfterSeconds` between polls. `costUsd` is the amount billed for the question, never above `maxCostUsd`, and 0 for a failed run (rates on Ask a support question).

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
    public class GetSupportAnswerExample
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
            var apiInstance = new SupportAssistantApi(httpClient, config, httpClientHandler);
            var runId = "runId_example";  // string | 

            try
            {
                // Get a support answer
                SupportRun result = apiInstance.GetSupportAnswer(runId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupportAssistantApi.GetSupportAnswer: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSupportAnswerWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a support answer
    ApiResponse<SupportRun> response = apiInstance.GetSupportAnswerWithHttpInfo(runId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupportAssistantApi.GetSupportAnswerWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **runId** | **string** |  |  |

### Return type

[**SupportRun**](SupportRun.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The run |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | A card is required (code &#x60;payment_method_required&#x60;) or the last payment failed (code &#x60;payment_required&#x60;). |  -  |
| **403** | Code &#x60;insufficient_permissions&#x60;: not an unrestricted API key, or a read-only, restricted or profile-scoped user. |  -  |
| **404** | Code &#x60;support_run_not_found&#x60;: no such run, or it was not started by your team. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listsupportanswers"></a>
# **ListSupportAnswers**
> ListSupportAnswers200Response ListSupportAnswers (string threadId, int? limit = null, string? cursor = null)

List a thread's support answers

Lists the runs of one thread that your team started, with Ana's answers, oldest first. Replies from the Zernio team after a support ticket arrive by email and are not included. Runs are kept for 90 days. Page through a long thread with `limit` and `cursor`: pass `nextCursor` as `cursor` until it is null.

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
    public class ListSupportAnswersExample
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
            var apiInstance = new SupportAssistantApi(httpClient, config, httpClientHandler);
            var threadId = "threadId_example";  // string | The thread to list, as returned by `POST /v1/support/runs`.
            var limit = 20;  // int? | Runs per page. (optional)  (default to 20)
            var cursor = "cursor_example";  // string? | Pass `nextCursor` from the previous page. (optional) 

            try
            {
                // List a thread's support answers
                ListSupportAnswers200Response result = apiInstance.ListSupportAnswers(threadId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupportAssistantApi.ListSupportAnswers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListSupportAnswersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List a thread's support answers
    ApiResponse<ListSupportAnswers200Response> response = apiInstance.ListSupportAnswersWithHttpInfo(threadId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupportAssistantApi.ListSupportAnswersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **threadId** | **string** | The thread to list, as returned by &#x60;POST /v1/support/runs&#x60;. |  |
| **limit** | **int?** | Runs per page. | [optional] [default to 20] |
| **cursor** | **string?** | Pass &#x60;nextCursor&#x60; from the previous page. | [optional]  |

### Return type

[**ListSupportAnswers200Response**](ListSupportAnswers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The thread&#39;s runs, oldest first |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | A card is required (code &#x60;payment_method_required&#x60;) or the last payment failed (code &#x60;payment_required&#x60;). |  -  |
| **403** | Code &#x60;insufficient_permissions&#x60;: not an unrestricted API key, or a read-only, restricted or profile-scoped user. |  -  |
| **404** | Code &#x60;support_thread_not_found&#x60;: no run in this thread was started by your team, or its runs are older than 90 days. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

