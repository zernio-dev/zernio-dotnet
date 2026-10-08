# Zernio.Api.SupportRunsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateSupportRun**](SupportRunsApi.md#createsupportrun) | **POST** /v1/support/runs | Start a support run (private beta) |
| [**GetSupportRun**](SupportRunsApi.md#getsupportrun) | **GET** /v1/support/runs/{runId} | Get a support run (private beta) |

<a id="createsupportrun"></a>
# **CreateSupportRun**
> CreateSupportRun202Response CreateSupportRun (CreateSupportRunRequest createSupportRunRequest, string? idempotencyKey = null)

Start a support run (private beta)

Private beta: returns 403 `feature_not_available` unless enabled for your account. Asks Ana, the Zernio support agent, a question about your workspace. The run is asynchronous: this returns 202 with a `runId`, and the answer arrives through the `support.run.completed` and `support.run.failed` webhooks. `GET /v1/support/runs/{runId}` is the fallback. Pass `threadId` to continue an earlier conversation, and `context` to point Ana at a post, account or profile. Billed when the run finishes at the model cost plus 20%, never above `maxCostUsd`; failed runs are free. Requires an unrestricted API key, usage-based billing and a card on file. Limits per account: 3 active runs and $100 of runs per UTC month. Send an Idempotency-Key header to make retries safe.

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
    public class CreateSupportRunExample
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
            var apiInstance = new SupportRunsApi(httpClient, config, httpClientHandler);
            var createSupportRunRequest = new CreateSupportRunRequest(); // CreateSupportRunRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. (optional) 

            try
            {
                // Start a support run (private beta)
                CreateSupportRun202Response result = apiInstance.CreateSupportRun(createSupportRunRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupportRunsApi.CreateSupportRun: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateSupportRunWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Start a support run (private beta)
    ApiResponse<CreateSupportRun202Response> response = apiInstance.CreateSupportRunWithHttpInfo(createSupportRunRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupportRunsApi.CreateSupportRunWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createSupportRunRequest** | [**CreateSupportRunRequest**](CreateSupportRunRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. | [optional]  |

### Return type

[**CreateSupportRun202Response**](CreateSupportRun202Response.md)

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
| **403** | Code &#x60;insufficient_permissions&#x60;: the credential is not an unrestricted API key, or the user is read-only, restricted or profile-scoped. Code &#x60;feature_not_available&#x60;: the private beta is not enabled for your account. |  -  |
| **404** | Code &#x60;support_thread_not_found&#x60; (&#x60;threadId&#x60;), &#x60;post_not_found&#x60;, &#x60;account_not_found&#x60; or &#x60;profile_not_found&#x60; (&#x60;context.*&#x60;). |  -  |
| **409** | Code &#x60;support_run_in_progress&#x60;: the thread already has a run queued or running, so poll it first. Code &#x60;billing_setup_incomplete&#x60;: no billing customer to attach a card to, contact support. Also returned while a request with the same Idempotency-Key is still processing. |  -  |
| **422** | Code &#x60;usage_billing_required&#x60;: support runs need a usage-based plan. Also returned when an Idempotency-Key is reused with a different request. |  -  |
| **429** | Code &#x60;support_active_runs_limit&#x60;: 3 runs are already active, retry when one finishes. Code &#x60;support_monthly_cap_exceeded&#x60;: this run could take the account past $100 for the UTC month; &#x60;Retry-After&#x60; runs until the next month starts, which can be weeks. |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getsupportrun"></a>
# **GetSupportRun**
> SupportRun GetSupportRun (string runId)

Get a support run (private beta)

Private beta: returns 403 `feature_not_available` unless enabled for your account. Returns a run started by your team. Prefer the `support.run.completed` and `support.run.failed` webhooks; use this as the fallback, waiting `pollAfterSeconds` between polls. `costUsd` is the amount billed: the model cost plus 20%, never above `maxCostUsd`, and 0 for a failed run.

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
    public class GetSupportRunExample
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
            var apiInstance = new SupportRunsApi(httpClient, config, httpClientHandler);
            var runId = "runId_example";  // string | 

            try
            {
                // Get a support run (private beta)
                SupportRun result = apiInstance.GetSupportRun(runId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupportRunsApi.GetSupportRun: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSupportRunWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a support run (private beta)
    ApiResponse<SupportRun> response = apiInstance.GetSupportRunWithHttpInfo(runId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupportRunsApi.GetSupportRunWithHttpInfo: " + e.Message);
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
| **403** | Code &#x60;insufficient_permissions&#x60; (not an unrestricted API key, or a read-only, restricted or profile-scoped user) or &#x60;feature_not_available&#x60; (private beta not enabled). |  -  |
| **404** | Code &#x60;support_run_not_found&#x60;: no such run, or it was not started by your team. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

