# Zernio.Api.AutomationsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ActivateAutomation**](AutomationsApi.md#activateautomation) | **POST** /v1/automations/{automationId}/activate | Turn an automation on |
| [**ApproveAutomationApproval**](AutomationsApi.md#approveautomationapproval) | **POST** /v1/automations/{automationId}/approvals/{approvalId}/approve | Approve an approval request |
| [**BacktestAutomation**](AutomationsApi.md#backtestautomation) | **POST** /v1/automations/{automationId}/backtest | Backtest a saved automation |
| [**BacktestAutomationDraft**](AutomationsApi.md#backtestautomationdraft) | **POST** /v1/automations/backtest | Backtest an unsaved automation |
| [**CreateAutomation**](AutomationsApi.md#createautomation) | **POST** /v1/automations | Create an automation |
| [**CreateAutomationTemplate**](AutomationsApi.md#createautomationtemplate) | **POST** /v1/automations/templates | Create an automation template |
| [**DeleteAutomation**](AutomationsApi.md#deleteautomation) | **DELETE** /v1/automations/{automationId} | Delete an automation |
| [**DeleteAutomationTemplate**](AutomationsApi.md#deleteautomationtemplate) | **DELETE** /v1/automations/templates/{templateId} | Delete an automation template |
| [**GetAutomation**](AutomationsApi.md#getautomation) | **GET** /v1/automations/{automationId} | Get an automation |
| [**GetAutomationApproval**](AutomationsApi.md#getautomationapproval) | **GET** /v1/automations/{automationId}/approvals/{approvalId} | Get an approval request |
| [**GetAutomationCatalog**](AutomationsApi.md#getautomationcatalog) | **GET** /v1/automations/catalog | Get the automations catalog |
| [**GetAutomationControls**](AutomationsApi.md#getautomationcontrols) | **GET** /v1/automations/controls | Get automation controls |
| [**GetAutomationRun**](AutomationsApi.md#getautomationrun) | **GET** /v1/automations/{automationId}/runs/{runId} | Get one run of an automation |
| [**GetAutomationTemplate**](AutomationsApi.md#getautomationtemplate) | **GET** /v1/automations/templates/{templateId} | Get an automation template |
| [**GetAutomationTestSample**](AutomationsApi.md#getautomationtestsample) | **GET** /v1/automations/{automationId}/test/sample | Get a sample test body for an automation |
| [**GetSharedAutomationTemplate**](AutomationsApi.md#getsharedautomationtemplate) | **GET** /v1/automations/templates/shared/{shareToken} | Get a shared automation template |
| [**GetZernioAutomationTemplate**](AutomationsApi.md#getzernioautomationtemplate) | **GET** /v1/automations/templates/zernio/{templateId} | Get a Zernio automation template |
| [**InstallAutomationTemplate**](AutomationsApi.md#installautomationtemplate) | **POST** /v1/automations/templates/{templateId}/install | Install an automation template |
| [**InstallSharedAutomationTemplate**](AutomationsApi.md#installsharedautomationtemplate) | **POST** /v1/automations/templates/shared/{shareToken}/install | Install a shared automation template |
| [**InstallZernioAutomationTemplate**](AutomationsApi.md#installzernioautomationtemplate) | **POST** /v1/automations/templates/zernio/{templateId}/install | Install a Zernio automation template |
| [**ListAutomationActions**](AutomationsApi.md#listautomationactions) | **GET** /v1/automations/actions | List automation actions |
| [**ListAutomationApprovals**](AutomationsApi.md#listautomationapprovals) | **GET** /v1/automations/{automationId}/approvals | List an automation&#39;s approval requests |
| [**ListAutomationChecks**](AutomationsApi.md#listautomationchecks) | **GET** /v1/automations/{automationId}/checks | List an automation&#39;s checks |
| [**ListAutomationRuns**](AutomationsApi.md#listautomationruns) | **GET** /v1/automations/{automationId}/runs | List an automation&#39;s runs |
| [**ListAutomationTemplates**](AutomationsApi.md#listautomationtemplates) | **GET** /v1/automations/templates | List automation templates |
| [**ListAutomations**](AutomationsApi.md#listautomations) | **GET** /v1/automations | List automations |
| [**PauseAutomation**](AutomationsApi.md#pauseautomation) | **POST** /v1/automations/{automationId}/pause | Turn an automation off |
| [**PreviewAutomation**](AutomationsApi.md#previewautomation) | **POST** /v1/automations/{automationId}/preview | Preview a saved automation |
| [**PreviewAutomationDraft**](AutomationsApi.md#previewautomationdraft) | **POST** /v1/automations/preview | Preview an unsaved automation |
| [**RejectAutomationApproval**](AutomationsApi.md#rejectautomationapproval) | **POST** /v1/automations/{automationId}/approvals/{approvalId}/reject | Reject an approval request |
| [**TakeOverAutomation**](AutomationsApi.md#takeoverautomation) | **POST** /v1/automations/{automationId}/take-over | Take over an automation |
| [**TestAutomation**](AutomationsApi.md#testautomation) | **POST** /v1/automations/{automationId}/test | Test an automation on a sample event |
| [**UpdateAutomation**](AutomationsApi.md#updateautomation) | **PATCH** /v1/automations/{automationId} | Edit an automation |
| [**UpdateAutomationAdAccountControls**](AutomationsApi.md#updateautomationadaccountcontrols) | **PATCH** /v1/automations/controls/ad-accounts | Update one ad account&#39;s controls |
| [**UpdateAutomationControls**](AutomationsApi.md#updateautomationcontrols) | **PATCH** /v1/automations/controls | Turn every ad automation off or on |
| [**UpdateAutomationTemplate**](AutomationsApi.md#updateautomationtemplate) | **PATCH** /v1/automations/templates/{templateId} | Update an automation template |

<a id="activateautomation"></a>
# **ActivateAutomation**
> CreateAutomation201Response ActivateAutomation (string automationId)

Turn an automation on

An ad rule's first check runs right away.

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
    public class ActivateAutomationExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 

            try
            {
                // Turn an automation on
                CreateAutomation201Response result = apiInstance.ActivateAutomation(automationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.ActivateAutomation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ActivateAutomationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Turn an automation on
    ApiResponse<CreateAutomation201Response> response = apiInstance.ActivateAutomationWithHttpInfo(automationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.ActivateAutomationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |

### Return type

[**CreateAutomation201Response**](CreateAutomation201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Automation on |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ad rules only: your account has no ads access (code &#x60;ads_addon_required&#x60;). Ads are included on usage-based plans. Event and scheduled automations never get this 403: a boost step without ads access is refused with a 400 at its path. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="approveautomationapproval"></a>
# **ApproveAutomationApproval**
> GetAutomationApproval200Response ApproveAutomationApproval (string automationId, string approvalId, AutomationApprovalDecision? automationApprovalDecision = null)

Approve an approval request

Approves a pending request, so the automation acts on each change it holds. Each change is checked again first, and one that no longer applies is skipped.  Only the approvers the automation names now can decide, matched by the email of the user behind the API key. A request already decided, expired or cancelled is refused with nothing changed.  Each applied or failed change fires `automation.action.applied` or `automation.action.failed`. 

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
    public class ApproveAutomationApprovalExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 
            var approvalId = "approvalId_example";  // string | 
            var automationApprovalDecision = new AutomationApprovalDecision?(); // AutomationApprovalDecision? |  (optional) 

            try
            {
                // Approve an approval request
                GetAutomationApproval200Response result = apiInstance.ApproveAutomationApproval(automationId, approvalId, automationApprovalDecision);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.ApproveAutomationApproval: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ApproveAutomationApprovalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Approve an approval request
    ApiResponse<GetAutomationApproval200Response> response = apiInstance.ApproveAutomationApprovalWithHttpInfo(automationId, approvalId, automationApprovalDecision);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.ApproveAutomationApprovalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |
| **approvalId** | **string** |  |  |
| **automationApprovalDecision** | [**AutomationApprovalDecision?**](AutomationApprovalDecision?.md) |  | [optional]  |

### Return type

[**GetAutomationApproval200Response**](GetAutomationApproval200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The request after the decision |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;insufficient_permissions&#x60; when you are not one of the approvers or &#x60;token&#x60; was sent to someone else, or &#x60;ads_addon_required&#x60; when the account has no ads access. |  -  |
| **404** | Resource not found |  -  |
| **409** | Code &#x60;invalid_resource_state&#x60;. Nothing was changed. The request was already approved or rejected, it expired, or it was cancelled when the automation stopped asking for approval.  Also returned when the automation no longer asks for approval or never does, and when it is acting on the ad account right now (try again in a minute).  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="backtestautomation"></a>
# **BacktestAutomation**
> AutomationBacktest BacktestAutomation (string automationId, int? days = null)

Backtest a saved automation

What a saved automation would have done over the last `days` days, replayed on stored daily metrics. Nothing is changed.  Each day lists what it would have done. Its own changes carry into later days, but the metrics stay what really happened. `notes` says what the replay could not know.  Only ad automations can be backtested, on at most 5,000 ads. 

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
    public class BacktestAutomationExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 
            var days = 30;  // int? | How many whole days before today to replay. Today is not replayed. (optional)  (default to 30)

            try
            {
                // Backtest a saved automation
                AutomationBacktest result = apiInstance.BacktestAutomation(automationId, days);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.BacktestAutomation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BacktestAutomationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Backtest a saved automation
    ApiResponse<AutomationBacktest> response = apiInstance.BacktestAutomationWithHttpInfo(automationId, days);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.BacktestAutomationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |
| **days** | **int?** | How many whole days before today to replay. Today is not replayed. | [optional] [default to 30] |

### Return type

[**AutomationBacktest**](AutomationBacktest.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Backtest |  -  |
| **400** | The automation is invalid, or holds something its kind cannot: &#x60;details.problems&#x60; lists each problem with its JSON path. A few ad rule checks (an unsupported platform, step or metric, a cooldown shorter than the schedule, approvers not on the team) answer with &#x60;param&#x60; instead. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ad rules only: your account has no ads access (code &#x60;ads_addon_required&#x60;). Ads are included on usage-based plans. Event and scheduled automations never get this 403: a boost step without ads access is refused with a 400 at its path. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="backtestautomationdraft"></a>
# **BacktestAutomationDraft**
> AutomationBacktest BacktestAutomationDraft (AutomationDefinition automationDefinition, int? days = null)

Backtest an unsaved automation

Replays an automation over past days on stored daily metrics, without saving it or changing anything. It refuses what saving would refuse.  Each day lists what it would have done. Its own changes carry into later days, but the metrics stay what really happened. `notes` says what the replay could not know.  Only ad automations can be backtested, on at most 5,000 ads. 

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
    public class BacktestAutomationDraftExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationDefinition = new AutomationDefinition(); // AutomationDefinition | 
            var days = 30;  // int? | How many whole days before today to replay. Today is not replayed. (optional)  (default to 30)

            try
            {
                // Backtest an unsaved automation
                AutomationBacktest result = apiInstance.BacktestAutomationDraft(automationDefinition, days);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.BacktestAutomationDraft: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BacktestAutomationDraftWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Backtest an unsaved automation
    ApiResponse<AutomationBacktest> response = apiInstance.BacktestAutomationDraftWithHttpInfo(automationDefinition, days);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.BacktestAutomationDraftWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationDefinition** | [**AutomationDefinition**](AutomationDefinition.md) |  |  |
| **days** | **int?** | How many whole days before today to replay. Today is not replayed. | [optional] [default to 30] |

### Return type

[**AutomationBacktest**](AutomationBacktest.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Backtest |  -  |
| **400** | The automation is invalid, or holds something its kind cannot: &#x60;details.problems&#x60; lists each problem with its JSON path. A few ad rule checks (an unsupported platform, step or metric, a cooldown shorter than the schedule, approvers not on the team) answer with &#x60;param&#x60; instead. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ad rules only: your account has no ads access (code &#x60;ads_addon_required&#x60;). Ads are included on usage-based plans. Event and scheduled automations never get this 403: a boost step without ads access is refused with a 400 at its path. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createautomation"></a>
# **CreateAutomation**
> CreateAutomation201Response CreateAutomation (CreateAutomationRequest createAutomationRequest, string? idempotencyKey = null)

Create an automation

Creates an automation. Its trigger picks the kind:  - **Ad rule**: a `schedule` over campaigns, ad sets, ads, Google keywords or Google search terms, with metric `conditions` and ad `steps`. It stays paused unless `status` is `active`; preview it first with `POST /v1/automations/preview`. - **Event**: a Zernio event in `trigger.type`, such as `post.failed`, with notify steps. It is on unless `status` is `paused`. - **Scheduled**: a `schedule` over a profile's posts, with notify steps and an optional boost. It is on unless `status` is `paused`. - **Sequence**: an `enrollment` trigger on one messaging account, with message steps sent over time. It is on unless `status` is `draft`. It needs what `/v1/sequences` needs: the inbox add-on and a key with the `messages` group. - **Comment to DM**: a comment door in `trigger.type`, such as `comment.keyword`, with a `graph` of the shapes `/v1/comment-automations` holds. It is on unless `status` is `paused`, and needs what `/v1/comment-automations` needs. A post that already has an active automation is a 409. - **Flow** (`kind` is `workflow`): a flow trigger such as `inbound_message` (or a `graph` whose trigger node names it) on one account, with the builder's `graph`. It is a draft unless `status` is `active`, which needs a complete graph; `paused` is refused. It needs the inbox add-on and a full-access key.  An ad rule, event, scheduled automation or sequence can instead be sent as `name`, `status` and an automation `graph` (`AutomationGraph`, the one its response carries). The graph's trigger picks the kind, and it is saved exactly as its own shape would be.  A comment to DM or flow sent as an automation graph is refused (`not_supported`).  Everything an automation cannot hold is refused at once: the 400 lists every problem with its JSON path in `details.problems`. 

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
    public class CreateAutomationExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var createAutomationRequest = new CreateAutomationRequest(); // CreateAutomationRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  (optional) 

            try
            {
                // Create an automation
                CreateAutomation201Response result = apiInstance.CreateAutomation(createAutomationRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.CreateAutomation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAutomationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create an automation
    ApiResponse<CreateAutomation201Response> response = apiInstance.CreateAutomationWithHttpInfo(createAutomationRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.CreateAutomationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createAutomationRequest** | [**CreateAutomationRequest**](CreateAutomationRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  | [optional]  |

### Return type

[**CreateAutomation201Response**](CreateAutomation201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Automation created |  -  |
| **400** | The automation is invalid, or holds something its kind cannot: &#x60;details.problems&#x60; lists each problem with its JSON path. A few ad rule checks (an unsupported platform, step or metric, a cooldown shorter than the schedule, approvers not on the team) answer with &#x60;param&#x60; instead. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ad rules only: no ads access (&#x60;ads_addon_required&#x60;), the ad account is not one the connection selected (&#x60;ad_account_not_selected&#x60;), or turning it on would raise live spend past the free ads allowance (&#x60;ads_allowance_exceeded&#x60;). |  -  |
| **409** | Same Idempotency-Key still processing; retry after a short backoff |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createautomationtemplate"></a>
# **CreateAutomationTemplate**
> CreateAutomationTemplate201Response CreateAutomationTemplate (CreateAutomationTemplateRequest createAutomationTemplateRequest, string? idempotencyKey = null)

Create an automation template

Saves a reusable setup of one or more automations (up to 20) that your team, or anyone you share it with, can install. Start from your own automations, one of Zernio's templates, a shared template, or definitions sent as they are.  Nothing tied to one account is kept. Ad accounts, a trigger's profile and accounts, and alert destinations become `inputs` that each install fills. Campaign ids, id filters, dates and approval steps are dropped.  From one of Zernio's templates, each threshold and budget or bid amount also becomes an input, with the template's own value as its default.  A template that would not install is refused: the 400 lists every problem in `details.problems`. 

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
    public class CreateAutomationTemplateExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var createAutomationTemplateRequest = new CreateAutomationTemplateRequest(); // CreateAutomationTemplateRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  (optional) 

            try
            {
                // Create an automation template
                CreateAutomationTemplate201Response result = apiInstance.CreateAutomationTemplate(createAutomationTemplateRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.CreateAutomationTemplate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAutomationTemplateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create an automation template
    ApiResponse<CreateAutomationTemplate201Response> response = apiInstance.CreateAutomationTemplateWithHttpInfo(createAutomationTemplateRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.CreateAutomationTemplateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createAutomationTemplateRequest** | [**CreateAutomationTemplateRequest**](CreateAutomationTemplateRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  | [optional]  |

### Return type

[**CreateAutomationTemplate201Response**](CreateAutomationTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Template created |  -  |
| **400** | The automation is invalid, or holds something its kind cannot: &#x60;details.problems&#x60; lists each problem with its JSON path. A few ad rule checks (an unsupported platform, step or metric, a cooldown shorter than the schedule, approvers not on the team) answer with &#x60;param&#x60; instead. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | An automation in &#x60;from.automationIds&#x60;, the Zernio template or the shared template was not found. |  -  |
| **409** | Your team already keeps 200 templates (code &#x60;automation_template_limit&#x60;); delete one to save another. Also returned when the same Idempotency-Key is still processing. |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteautomation"></a>
# **DeleteAutomation**
> UpdateYoutubeDefaultPlaylist200Response DeleteAutomation (string automationId)

Delete an automation

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
    public class DeleteAutomationExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 

            try
            {
                // Delete an automation
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.DeleteAutomation(automationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.DeleteAutomation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAutomationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete an automation
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.DeleteAutomationWithHttpInfo(automationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.DeleteAutomationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |

### Return type

[**UpdateYoutubeDefaultPlaylist200Response**](UpdateYoutubeDefaultPlaylist200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Automation deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteautomationtemplate"></a>
# **DeleteAutomationTemplate**
> DeleteAutomationTemplate200Response DeleteAutomationTemplate (string templateId)

Delete an automation template

Deletes one of your team's templates and its share link. Automations already installed from it stay. 

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
    public class DeleteAutomationTemplateExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var templateId = "templateId_example";  // string | The template's id.

            try
            {
                // Delete an automation template
                DeleteAutomationTemplate200Response result = apiInstance.DeleteAutomationTemplate(templateId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.DeleteAutomationTemplate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAutomationTemplateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete an automation template
    ApiResponse<DeleteAutomationTemplate200Response> response = apiInstance.DeleteAutomationTemplateWithHttpInfo(templateId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.DeleteAutomationTemplateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** | The template&#39;s id. |  |

### Return type

[**DeleteAutomationTemplate200Response**](DeleteAutomationTemplate200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Template deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | No template with this id in your team. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getautomation"></a>
# **GetAutomation**
> CreateAutomation201Response GetAutomation (string automationId)

Get an automation

An automation installed from a template also carries `template`.

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
    public class GetAutomationExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 

            try
            {
                // Get an automation
                CreateAutomation201Response result = apiInstance.GetAutomation(automationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.GetAutomation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAutomationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an automation
    ApiResponse<CreateAutomation201Response> response = apiInstance.GetAutomationWithHttpInfo(automationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.GetAutomationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |

### Return type

[**CreateAutomation201Response**](CreateAutomation201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Automation |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getautomationapproval"></a>
# **GetAutomationApproval**
> GetAutomationApproval200Response GetAutomationApproval (string automationId, string approvalId)

Get an approval request

One approval request with the changes it holds, who may decide it and whether you can.

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
    public class GetAutomationApprovalExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 
            var approvalId = "approvalId_example";  // string | 

            try
            {
                // Get an approval request
                GetAutomationApproval200Response result = apiInstance.GetAutomationApproval(automationId, approvalId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.GetAutomationApproval: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAutomationApprovalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an approval request
    ApiResponse<GetAutomationApproval200Response> response = apiInstance.GetAutomationApprovalWithHttpInfo(automationId, approvalId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.GetAutomationApprovalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |
| **approvalId** | **string** |  |  |

### Return type

[**GetAutomationApproval200Response**](GetAutomationApproval200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Approval request |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **409** | Code &#x60;invalid_resource_state&#x60;: this automation never waits for approval. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getautomationcatalog"></a>
# **GetAutomationCatalog**
> GetAutomationCatalog200Response GetAutomationCatalog ()

Get the automations catalog

What an automation can contain and where each part works, built from the same checks that validate a save, so it never offers what saving refuses.  - `schema`: the JSON Schema of the body of `POST /v1/automations`. - `triggers`: every trigger, tagged with its `kind`. Ad rule and scheduled triggers list their intervals; event triggers list each event with its facts. - The other sections describe ad rules: per subject (campaign, ad set, ad) its metrics and steps with the platforms that accept them, plus filters, groups, alerts, conditions, limits and approval. 

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
    public class GetAutomationCatalogExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);

            try
            {
                // Get the automations catalog
                GetAutomationCatalog200Response result = apiInstance.GetAutomationCatalog();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.GetAutomationCatalog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAutomationCatalogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get the automations catalog
    ApiResponse<GetAutomationCatalog200Response> response = apiInstance.GetAutomationCatalogWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.GetAutomationCatalogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**GetAutomationCatalog200Response**](GetAutomationCatalog200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Catalog |  * Cache-Control -  <br>  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getautomationcontrols"></a>
# **GetAutomationControls**
> GetAutomationControls200Response GetAutomationControls ()

Get automation controls

The team's switch for every ad rule, and each ad account's own switch and daily raise limit. Boosting automations do not read them.  Every team member sees the same controls. `adAccounts` lists each ad account your automations use, plus any ad account that has controls set. 

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
    public class GetAutomationControlsExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);

            try
            {
                // Get automation controls
                GetAutomationControls200Response result = apiInstance.GetAutomationControls();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.GetAutomationControls: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAutomationControlsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get automation controls
    ApiResponse<GetAutomationControls200Response> response = apiInstance.GetAutomationControlsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.GetAutomationControlsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**GetAutomationControls200Response**](GetAutomationControls200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Controls |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ad rules only: your account has no ads access (code &#x60;ads_addon_required&#x60;). Ads are included on usage-based plans. Event and scheduled automations never get this 403: a boost step without ads access is refused with a 400 at its path. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getautomationrun"></a>
# **GetAutomationRun**
> GetAutomationRun200Response GetAutomationRun (string automationId, string runId)

Get one run of an automation

The run with each step it took, where its store keeps them: a flow run's nodes, a comment to DM log's DM and public reply, an ad rule, event or scheduled check's actions. 

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
    public class GetAutomationRunExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 
            var runId = "runId_example";  // string | 

            try
            {
                // Get one run of an automation
                GetAutomationRun200Response result = apiInstance.GetAutomationRun(automationId, runId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.GetAutomationRun: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAutomationRunWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get one run of an automation
    ApiResponse<GetAutomationRun200Response> response = apiInstance.GetAutomationRunWithHttpInfo(automationId, runId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.GetAutomationRunWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |
| **runId** | **string** |  |  |

### Return type

[**GetAutomationRun200Response**](GetAutomationRun200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Run |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getautomationtemplate"></a>
# **GetAutomationTemplate**
> CreateAutomationTemplate201Response GetAutomationTemplate (string templateId)

Get an automation template

Returns one of your team's templates, with its inputs and automations. 

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
    public class GetAutomationTemplateExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var templateId = "templateId_example";  // string | The template's id.

            try
            {
                // Get an automation template
                CreateAutomationTemplate201Response result = apiInstance.GetAutomationTemplate(templateId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.GetAutomationTemplate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAutomationTemplateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an automation template
    ApiResponse<CreateAutomationTemplate201Response> response = apiInstance.GetAutomationTemplateWithHttpInfo(templateId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.GetAutomationTemplateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** | The template&#39;s id. |  |

### Return type

[**CreateAutomationTemplate201Response**](CreateAutomationTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Template |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | No template with this id in your team. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getautomationtestsample"></a>
# **GetAutomationTestSample**
> GetAutomationTestSample200Response GetAutomationTestSample (string automationId)

Get a sample test body for an automation

A body `POST /v1/automations/{automationId}/test` accepts for this automation: a comment with its first keyword, an inbound event its flow's trigger takes, its event's webhook payload with sample values, or the contact a sequence enrolled last. Kinds that read live data instead take no event. 

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
    public class GetAutomationTestSampleExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 

            try
            {
                // Get a sample test body for an automation
                GetAutomationTestSample200Response result = apiInstance.GetAutomationTestSample(automationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.GetAutomationTestSample: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAutomationTestSampleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a sample test body for an automation
    ApiResponse<GetAutomationTestSample200Response> response = apiInstance.GetAutomationTestSampleWithHttpInfo(automationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.GetAutomationTestSampleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |

### Return type

[**GetAutomationTestSample200Response**](GetAutomationTestSample200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sample |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getsharedautomationtemplate"></a>
# **GetSharedAutomationTemplate**
> CreateAutomationTemplate201Response GetSharedAutomationTemplate (string shareToken)

Get a shared automation template

Returns a template shared by link, from any team. Who made it and its install counts in that team are left out, and `share` is null. 

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
    public class GetSharedAutomationTemplateExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var shareToken = "shareToken_example";  // string | The token from the template's `share.token`.

            try
            {
                // Get a shared automation template
                CreateAutomationTemplate201Response result = apiInstance.GetSharedAutomationTemplate(shareToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.GetSharedAutomationTemplate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSharedAutomationTemplateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a shared automation template
    ApiResponse<CreateAutomationTemplate201Response> response = apiInstance.GetSharedAutomationTemplateWithHttpInfo(shareToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.GetSharedAutomationTemplateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **shareToken** | **string** | The token from the template&#39;s &#x60;share.token&#x60;. |  |

### Return type

[**CreateAutomationTemplate201Response**](CreateAutomationTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Template |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | No template is shared with this token, or its link was turned off. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getzernioautomationtemplate"></a>
# **GetZernioAutomationTemplate**
> CreateAutomationTemplate201Response GetZernioAutomationTemplate (string templateId)

Get a Zernio automation template

Returns one of Zernio's ready-made templates in the same shape as your own: an ad rule (like `stop_losers`), a comment to DM (`comment-keyword-dm`, `comment-keyword-dm-follow-gate`) or a sequence (`sequence-welcome-series`, `sequence-nurture`).  In an ad rule, each threshold and budget or bid amount is an input with the template's own value as its default, so an install can change it or leave it. A comment to DM or a sequence asks for a profile and one account of it. 

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
    public class GetZernioAutomationTemplateExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var templateId = stop_losers;  // string | The id of one of Zernio's templates, for example `stop_losers`.

            try
            {
                // Get a Zernio automation template
                CreateAutomationTemplate201Response result = apiInstance.GetZernioAutomationTemplate(templateId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.GetZernioAutomationTemplate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetZernioAutomationTemplateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a Zernio automation template
    ApiResponse<CreateAutomationTemplate201Response> response = apiInstance.GetZernioAutomationTemplateWithHttpInfo(templateId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.GetZernioAutomationTemplateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** | The id of one of Zernio&#39;s templates, for example &#x60;stop_losers&#x60;. |  |

### Return type

[**CreateAutomationTemplate201Response**](CreateAutomationTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Template |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | No Zernio template with this id. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="installautomationtemplate"></a>
# **InstallAutomationTemplate**
> AutomationTemplateInstallResponse InstallAutomationTemplate (string templateId, AutomationTemplateInstallRequest automationTemplateInstallRequest, string? idempotencyKey = null)

Install an automation template

Creates every automation in the template, with your values in place of its inputs. All or nothing: if one automation fails, the ones already created are removed. New automations stay paused unless `status` is `active`.  To install on many ad accounts at once, send `targets` (up to 50). Each target is its own install with its own `inputs`, which win over the shared `inputs`. A failed target leaves the others in place, and the response is 207. 

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
    public class InstallAutomationTemplateExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var templateId = "templateId_example";  // string | The template's id.
            var automationTemplateInstallRequest = new AutomationTemplateInstallRequest(); // AutomationTemplateInstallRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  (optional) 

            try
            {
                // Install an automation template
                AutomationTemplateInstallResponse result = apiInstance.InstallAutomationTemplate(templateId, automationTemplateInstallRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.InstallAutomationTemplate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the InstallAutomationTemplateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Install an automation template
    ApiResponse<AutomationTemplateInstallResponse> response = apiInstance.InstallAutomationTemplateWithHttpInfo(templateId, automationTemplateInstallRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.InstallAutomationTemplateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** | The template&#39;s id. |  |
| **automationTemplateInstallRequest** | [**AutomationTemplateInstallRequest**](AutomationTemplateInstallRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  | [optional]  |

### Return type

[**AutomationTemplateInstallResponse**](AutomationTemplateInstallResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Installed. &#x60;installation&#x60; for one install, &#x60;installations&#x60; when &#x60;targets&#x60; was sent and every target installed. |  -  |
| **207** | Some targets installed and some failed: check each &#x60;installations[].status&#x60;. |  -  |
| **400** | The request is invalid, or an input is missing, unknown or of the wrong type: &#x60;details.problems&#x60; lists each one at its path, such as &#x60;inputs.adAccount&#x60;.  When no target installed, the first target&#39;s error is returned with every target&#39;s result in &#x60;details.installations&#x60;. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ad rules only: your account has no ads access (code &#x60;ads_addon_required&#x60;). Ads are included on usage-based plans. Event and scheduled automations never get this 403: a boost step without ads access is refused with a 400 at its path. |  -  |
| **404** | No template with this id in your team. |  -  |
| **409** | Same Idempotency-Key still processing; retry after a short backoff |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="installsharedautomationtemplate"></a>
# **InstallSharedAutomationTemplate**
> AutomationTemplateInstallResponse InstallSharedAutomationTemplate (string shareToken, AutomationTemplateInstallRequest automationTemplateInstallRequest, string? idempotencyKey = null)

Install a shared automation template

Installs a template shared by link into your account, the same way as your own templates.  To install on many ad accounts at once, send `targets` (up to 50). Each target is its own install with its own `inputs`, which win over the shared `inputs`. A failed target leaves the others in place, and the response is 207. 

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
    public class InstallSharedAutomationTemplateExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var shareToken = "shareToken_example";  // string | The token from the template's `share.token`.
            var automationTemplateInstallRequest = new AutomationTemplateInstallRequest(); // AutomationTemplateInstallRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  (optional) 

            try
            {
                // Install a shared automation template
                AutomationTemplateInstallResponse result = apiInstance.InstallSharedAutomationTemplate(shareToken, automationTemplateInstallRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.InstallSharedAutomationTemplate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the InstallSharedAutomationTemplateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Install a shared automation template
    ApiResponse<AutomationTemplateInstallResponse> response = apiInstance.InstallSharedAutomationTemplateWithHttpInfo(shareToken, automationTemplateInstallRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.InstallSharedAutomationTemplateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **shareToken** | **string** | The token from the template&#39;s &#x60;share.token&#x60;. |  |
| **automationTemplateInstallRequest** | [**AutomationTemplateInstallRequest**](AutomationTemplateInstallRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  | [optional]  |

### Return type

[**AutomationTemplateInstallResponse**](AutomationTemplateInstallResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Installed. &#x60;installation&#x60; for one install, &#x60;installations&#x60; when &#x60;targets&#x60; was sent and every target installed. |  -  |
| **207** | Some targets installed and some failed: check each &#x60;installations[].status&#x60;. |  -  |
| **400** | The request is invalid, or an input is missing, unknown or of the wrong type: &#x60;details.problems&#x60; lists each one at its path, such as &#x60;inputs.adAccount&#x60;.  When no target installed, the first target&#39;s error is returned with every target&#39;s result in &#x60;details.installations&#x60;. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ad rules only: your account has no ads access (code &#x60;ads_addon_required&#x60;). Ads are included on usage-based plans. Event and scheduled automations never get this 403: a boost step without ads access is refused with a 400 at its path. |  -  |
| **404** | No template is shared with this token, or its link was turned off. |  -  |
| **409** | Same Idempotency-Key still processing; retry after a short backoff |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="installzernioautomationtemplate"></a>
# **InstallZernioAutomationTemplate**
> AutomationTemplateInstallResponse InstallZernioAutomationTemplate (string templateId, AutomationTemplateInstallRequest automationTemplateInstallRequest, string? idempotencyKey = null)

Install a Zernio automation template

Installs one of Zernio's ready-made templates. Leave a value input out to keep the template's default.  To install on many ad accounts at once, send `targets` (up to 50). Each target is its own install with its own `inputs`, which win over the shared `inputs`. A failed target leaves the others in place, and the response is 207. 

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
    public class InstallZernioAutomationTemplateExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var templateId = stop_losers;  // string | The id of one of Zernio's templates, for example `stop_losers`.
            var automationTemplateInstallRequest = new AutomationTemplateInstallRequest(); // AutomationTemplateInstallRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  (optional) 

            try
            {
                // Install a Zernio automation template
                AutomationTemplateInstallResponse result = apiInstance.InstallZernioAutomationTemplate(templateId, automationTemplateInstallRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.InstallZernioAutomationTemplate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the InstallZernioAutomationTemplateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Install a Zernio automation template
    ApiResponse<AutomationTemplateInstallResponse> response = apiInstance.InstallZernioAutomationTemplateWithHttpInfo(templateId, automationTemplateInstallRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.InstallZernioAutomationTemplateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** | The id of one of Zernio&#39;s templates, for example &#x60;stop_losers&#x60;. |  |
| **automationTemplateInstallRequest** | [**AutomationTemplateInstallRequest**](AutomationTemplateInstallRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  | [optional]  |

### Return type

[**AutomationTemplateInstallResponse**](AutomationTemplateInstallResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Installed. &#x60;installation&#x60; for one install, &#x60;installations&#x60; when &#x60;targets&#x60; was sent and every target installed. |  -  |
| **207** | Some targets installed and some failed: check each &#x60;installations[].status&#x60;. |  -  |
| **400** | The request is invalid, or an input is missing, unknown or of the wrong type: &#x60;details.problems&#x60; lists each one at its path, such as &#x60;inputs.adAccount&#x60;.  When no target installed, the first target&#39;s error is returned with every target&#39;s result in &#x60;details.installations&#x60;. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ad rules only: your account has no ads access (code &#x60;ads_addon_required&#x60;). Ads are included on usage-based plans. Event and scheduled automations never get this 403: a boost step without ads access is refused with a 400 at its path. |  -  |
| **404** | No Zernio template with this id. |  -  |
| **409** | Same Idempotency-Key still processing; retry after a short backoff |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listautomationactions"></a>
# **ListAutomationActions**
> ListAutomationActions200Response ListAutomationActions (string? automationId = null, string? accountId = null, string? type = null, DateTime? from = null, DateTime? to = null, int? limit = null, string? cursor = null)

List automation actions

Every change your ad rules made, newest first: what changed, the value before and after, and whether it was applied, skipped or failed. What event and scheduled automations did is in each one's checks. 

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
    public class ListAutomationActionsExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string? |  (optional) 
            var accountId = "accountId_example";  // string? | Only actions on this ads connection. (optional) 
            var type = "ads.pause";  // string? | A change reads as the value it set, so budget changes filter as `ads.set_budget`. (optional) 
            var from = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var to = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? | `nextCursor` from the previous page. (optional) 

            try
            {
                // List automation actions
                ListAutomationActions200Response result = apiInstance.ListAutomationActions(automationId, accountId, type, from, to, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.ListAutomationActions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAutomationActionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List automation actions
    ApiResponse<ListAutomationActions200Response> response = apiInstance.ListAutomationActionsWithHttpInfo(automationId, accountId, type, from, to, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.ListAutomationActionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string?** |  | [optional]  |
| **accountId** | **string?** | Only actions on this ads connection. | [optional]  |
| **type** | **string?** | A change reads as the value it set, so budget changes filter as &#x60;ads.set_budget&#x60;. | [optional]  |
| **from** | **DateTime?** |  | [optional]  |
| **to** | **DateTime?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** | &#x60;nextCursor&#x60; from the previous page. | [optional]  |

### Return type

[**ListAutomationActions200Response**](ListAutomationActions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Actions |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listautomationapprovals"></a>
# **ListAutomationApprovals**
> ListAutomationApprovals200Response ListAutomationApprovals (string automationId, string? status = null, int? limit = null)

List an automation's approval requests

The requests an automation sent for a person's approval before acting, newest first. Each lists the changes it holds, who may decide it and until when.  Only automations that ask for approval have requests. Others return 409. 

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
    public class ListAutomationApprovalsExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 
            var status = "pending";  // string? | Only requests in this status. (optional) 
            var limit = 20;  // int? | How many requests to return. There is no cursor; the newest come first. (optional)  (default to 20)

            try
            {
                // List an automation's approval requests
                ListAutomationApprovals200Response result = apiInstance.ListAutomationApprovals(automationId, status, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.ListAutomationApprovals: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAutomationApprovalsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List an automation's approval requests
    ApiResponse<ListAutomationApprovals200Response> response = apiInstance.ListAutomationApprovalsWithHttpInfo(automationId, status, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.ListAutomationApprovalsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |
| **status** | **string?** | Only requests in this status. | [optional]  |
| **limit** | **int?** | How many requests to return. There is no cursor; the newest come first. | [optional] [default to 20] |

### Return type

[**ListAutomationApprovals200Response**](ListAutomationApprovals200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Approval requests |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **409** | Code &#x60;invalid_resource_state&#x60;: this automation never waits for approval. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listautomationchecks"></a>
# **ListAutomationChecks**
> ListAutomationChecks200Response ListAutomationChecks (string automationId, int? limit = null, string? cursor = null)

List an automation's checks

Each time the automation ran, newest first, with what matched and what it did. For an event automation, each check is one event that reached it. 

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
    public class ListAutomationChecksExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 
            var limit = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string? | `nextCursor` from the previous page. (optional) 

            try
            {
                // List an automation's checks
                ListAutomationChecks200Response result = apiInstance.ListAutomationChecks(automationId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.ListAutomationChecks: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAutomationChecksWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List an automation's checks
    ApiResponse<ListAutomationChecks200Response> response = apiInstance.ListAutomationChecksWithHttpInfo(automationId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.ListAutomationChecksWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |
| **limit** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string?** | &#x60;nextCursor&#x60; from the previous page. | [optional]  |

### Return type

[**ListAutomationChecks200Response**](ListAutomationChecks200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Checks |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listautomationruns"></a>
# **ListAutomationRuns**
> ListAutomationRuns200Response ListAutomationRuns (string automationId, string? status = null, DateTime? since = null, int? limit = null, string? cursor = null)

List an automation's runs

Every run of any kind of automation, newest first, in one shape. Flows read both their run stores, comment to DM reads its engine runs and its older trigger logs, and ad rules, event and scheduled automations list their checks that acted or tried to (`/checks` lists every check). 

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
    public class ListAutomationRunsExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 
            var status = "live";  // string? |  (optional) 
            var since = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | Only runs started at or after this time. (optional) 
            var limit = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string? | `nextCursor` from the previous page. (optional) 

            try
            {
                // List an automation's runs
                ListAutomationRuns200Response result = apiInstance.ListAutomationRuns(automationId, status, since, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.ListAutomationRuns: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAutomationRunsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List an automation's runs
    ApiResponse<ListAutomationRuns200Response> response = apiInstance.ListAutomationRunsWithHttpInfo(automationId, status, since, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.ListAutomationRunsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |
| **status** | **string?** |  | [optional]  |
| **since** | **DateTime?** | Only runs started at or after this time. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string?** | &#x60;nextCursor&#x60; from the previous page. | [optional]  |

### Return type

[**ListAutomationRuns200Response**](ListAutomationRuns200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Runs |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listautomationtemplates"></a>
# **ListAutomationTemplates**
> ListAutomationTemplates200Response ListAutomationTemplates (string? scope = null)

List automation templates

Lists your team's templates, newest first. Every team member sees the templates any member saved. A team keeps up to 200. 

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
    public class ListAutomationTemplatesExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var scope = "team";  // string? | Which templates to list. Only `team` today. (optional)  (default to team)

            try
            {
                // List automation templates
                ListAutomationTemplates200Response result = apiInstance.ListAutomationTemplates(scope);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.ListAutomationTemplates: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAutomationTemplatesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List automation templates
    ApiResponse<ListAutomationTemplates200Response> response = apiInstance.ListAutomationTemplatesWithHttpInfo(scope);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.ListAutomationTemplatesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **scope** | **string?** | Which templates to list. Only &#x60;team&#x60; today. | [optional] [default to team] |

### Return type

[**ListAutomationTemplates200Response**](ListAutomationTemplates200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Templates |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listautomations"></a>
# **ListAutomations**
> ListAutomations200Response ListAutomations (string? accountId = null, string? adAccountId = null, string? q = null, string? kind = null, int? limit = null, string? cursor = null)

List automations

Lists the automations on the profiles your key can reach, newest first, across every kind: ad rules, event automations, scheduled automations, sequences, comment to DM and flows. One `cursor` pages them all.  Each kind is listed only for callers its own route lets read it; the others are left out, never an error:  - **Sequences and comment to DM** need the inbox add-on and a key with the `messages` group, as `/v1/sequences` and `/v1/comment-automations` do. - **Flows** need the inbox add-on and a full-access key, as `/v1/workflows` does. - **Ad rules, event and scheduled automations** need only access to their profile, as reading, pausing and deleting them does. Creating, editing, activating or previewing an ad rule needs the ads add-on. 

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
    public class ListAutomationsExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string? | Only automations on this account: the ads connection of an ad rule, one of the `accountIds` of an event or scheduled automation, or the account a sequence, comment to DM or flow runs on. (optional) 
            var adAccountId = "adAccountId_example";  // string? | Only ad rules checking this platform ad account. (optional) 
            var q = welcome;  // string? | Only automations whose name contains this text, ignoring case. `%` and `_` match themselves. (optional) 
            var kind = ad_rule,event;  // string? | Only these kinds, comma separated: `ad_rule`, `event`, `scheduled`, `sequence`, `comment`, `workflow`. (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? | `nextCursor` from the previous page, sent back unchanged with the same `q`, `kind`, `accountId` and `adAccountId`.  Opaque: it holds the creation time and id of the page's last automation, and the next page is every kind's automations strictly older than it, so an automation created meanwhile never shifts or repeats a page.  (optional) 

            try
            {
                // List automations
                ListAutomations200Response result = apiInstance.ListAutomations(accountId, adAccountId, q, kind, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.ListAutomations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAutomationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List automations
    ApiResponse<ListAutomations200Response> response = apiInstance.ListAutomationsWithHttpInfo(accountId, adAccountId, q, kind, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.ListAutomationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string?** | Only automations on this account: the ads connection of an ad rule, one of the &#x60;accountIds&#x60; of an event or scheduled automation, or the account a sequence, comment to DM or flow runs on. | [optional]  |
| **adAccountId** | **string?** | Only ad rules checking this platform ad account. | [optional]  |
| **q** | **string?** | Only automations whose name contains this text, ignoring case. &#x60;%&#x60; and &#x60;_&#x60; match themselves. | [optional]  |
| **kind** | **string?** | Only these kinds, comma separated: &#x60;ad_rule&#x60;, &#x60;event&#x60;, &#x60;scheduled&#x60;, &#x60;sequence&#x60;, &#x60;comment&#x60;, &#x60;workflow&#x60;. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** | &#x60;nextCursor&#x60; from the previous page, sent back unchanged with the same &#x60;q&#x60;, &#x60;kind&#x60;, &#x60;accountId&#x60; and &#x60;adAccountId&#x60;.  Opaque: it holds the creation time and id of the page&#39;s last automation, and the next page is every kind&#39;s automations strictly older than it, so an automation created meanwhile never shifts or repeats a page.  | [optional]  |

### Return type

[**ListAutomations200Response**](ListAutomations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Automations |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="pauseautomation"></a>
# **PauseAutomation**
> CreateAutomation201Response PauseAutomation (string automationId)

Turn an automation off

Pausing never needs ads access.

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
    public class PauseAutomationExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 

            try
            {
                // Turn an automation off
                CreateAutomation201Response result = apiInstance.PauseAutomation(automationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.PauseAutomation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PauseAutomationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Turn an automation off
    ApiResponse<CreateAutomation201Response> response = apiInstance.PauseAutomationWithHttpInfo(automationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.PauseAutomationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |

### Return type

[**CreateAutomation201Response**](CreateAutomation201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Automation off |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="previewautomation"></a>
# **PreviewAutomation**
> AutomationPreview PreviewAutomation (string automationId, int? limit = null)

Preview a saved automation

Shows what an ad rule would do if it ran now. Nothing is changed. Event and scheduled automations cannot be previewed yet (400, `not_supported`). 

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
    public class PreviewAutomationExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 
            var limit = 100;  // int? | How many subjects to list, matches first. `evaluated` and `matched` always count them all. (optional)  (default to 100)

            try
            {
                // Preview a saved automation
                AutomationPreview result = apiInstance.PreviewAutomation(automationId, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.PreviewAutomation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PreviewAutomationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Preview a saved automation
    ApiResponse<AutomationPreview> response = apiInstance.PreviewAutomationWithHttpInfo(automationId, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.PreviewAutomationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |
| **limit** | **int?** | How many subjects to list, matches first. &#x60;evaluated&#x60; and &#x60;matched&#x60; always count them all. | [optional] [default to 100] |

### Return type

[**AutomationPreview**](AutomationPreview.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Preview |  -  |
| **400** | The automation is invalid, or holds something its kind cannot: &#x60;details.problems&#x60; lists each problem with its JSON path. A few ad rule checks (an unsupported platform, step or metric, a cooldown shorter than the schedule, approvers not on the team) answer with &#x60;param&#x60; instead. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ad rules only: your account has no ads access (code &#x60;ads_addon_required&#x60;). Ads are included on usage-based plans. Event and scheduled automations never get this 403: a boost step without ads access is refused with a 400 at its path. |  -  |
| **404** | Resource not found |  -  |
| **409** | A keyword or search term rule is still loading its daily history from Google (&#x60;history_loading&#x60;). Loading starts when the rule is saved and a 30-day window takes about two minutes. The message says how many days are loaded. Try again shortly. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="previewautomationdraft"></a>
# **PreviewAutomationDraft**
> AutomationPreview PreviewAutomationDraft (AutomationDefinition automationDefinition, int? limit = null)

Preview an unsaved automation

Shows what an ad rule would do if it ran now, without saving it or changing anything: every object it checks, each condition with its actual value, and the steps a match would run. It refuses what saving would refuse.  Event and scheduled automations cannot be previewed yet (400, `not_supported`). 

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
    public class PreviewAutomationDraftExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationDefinition = new AutomationDefinition(); // AutomationDefinition | 
            var limit = 100;  // int? | How many subjects to list, matches first. `evaluated` and `matched` always count them all. (optional)  (default to 100)

            try
            {
                // Preview an unsaved automation
                AutomationPreview result = apiInstance.PreviewAutomationDraft(automationDefinition, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.PreviewAutomationDraft: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PreviewAutomationDraftWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Preview an unsaved automation
    ApiResponse<AutomationPreview> response = apiInstance.PreviewAutomationDraftWithHttpInfo(automationDefinition, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.PreviewAutomationDraftWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationDefinition** | [**AutomationDefinition**](AutomationDefinition.md) |  |  |
| **limit** | **int?** | How many subjects to list, matches first. &#x60;evaluated&#x60; and &#x60;matched&#x60; always count them all. | [optional] [default to 100] |

### Return type

[**AutomationPreview**](AutomationPreview.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Preview |  -  |
| **400** | The automation is invalid, or holds something its kind cannot: &#x60;details.problems&#x60; lists each problem with its JSON path. A few ad rule checks (an unsupported platform, step or metric, a cooldown shorter than the schedule, approvers not on the team) answer with &#x60;param&#x60; instead. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ad rules only: your account has no ads access (code &#x60;ads_addon_required&#x60;). Ads are included on usage-based plans. Event and scheduled automations never get this 403: a boost step without ads access is refused with a 400 at its path. |  -  |
| **409** | A keyword or search term rule is still loading its daily history from Google (&#x60;history_loading&#x60;). Loading starts when the rule is saved and a 30-day window takes about two minutes. The message says how many days are loaded. Try again shortly. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="rejectautomationapproval"></a>
# **RejectAutomationApproval**
> GetAutomationApproval200Response RejectAutomationApproval (string automationId, string approvalId, AutomationApprovalDecision? automationApprovalDecision = null)

Reject an approval request

Rejects a pending request: every change it holds is skipped and nothing is changed on the ad account.  Only the approvers the automation names now can decide, matched by the email of the user behind the API key. Rejecting needs no ads access, like pausing. 

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
    public class RejectAutomationApprovalExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 
            var approvalId = "approvalId_example";  // string | 
            var automationApprovalDecision = new AutomationApprovalDecision?(); // AutomationApprovalDecision? |  (optional) 

            try
            {
                // Reject an approval request
                GetAutomationApproval200Response result = apiInstance.RejectAutomationApproval(automationId, approvalId, automationApprovalDecision);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.RejectAutomationApproval: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RejectAutomationApprovalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reject an approval request
    ApiResponse<GetAutomationApproval200Response> response = apiInstance.RejectAutomationApprovalWithHttpInfo(automationId, approvalId, automationApprovalDecision);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.RejectAutomationApprovalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |
| **approvalId** | **string** |  |  |
| **automationApprovalDecision** | [**AutomationApprovalDecision?**](AutomationApprovalDecision?.md) |  | [optional]  |

### Return type

[**GetAutomationApproval200Response**](GetAutomationApproval200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The request after the decision |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;insufficient_permissions&#x60;: you are not one of the approvers, or &#x60;token&#x60; was sent to someone else. |  -  |
| **404** | Resource not found |  -  |
| **409** | Code &#x60;invalid_resource_state&#x60;. Nothing was changed. The request was already approved or rejected, it expired, or it was cancelled when the automation stopped asking for approval.  Also returned when the automation no longer asks for approval or never does, and when it is acting on the ad account right now (try again in a minute).  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="takeoverautomation"></a>
# **TakeOverAutomation**
> TakeOverAutomation200Response TakeOverAutomation (string automationId)

Take over an automation

Makes the caller the automation's owner, so its AI steps use the caller's own AI key. Only the owner or an admin of the active workspace can take over, from the dashboard.  When the member who made an automation leaves the workspace, its AI steps pause until it is taken over; every other step keeps running. 

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
    public class TakeOverAutomationExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 

            try
            {
                // Take over an automation
                TakeOverAutomation200Response result = apiInstance.TakeOverAutomation(automationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.TakeOverAutomation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TakeOverAutomationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Take over an automation
    ApiResponse<TakeOverAutomation200Response> response = apiInstance.TakeOverAutomationWithHttpInfo(automationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.TakeOverAutomationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |

### Return type

[**TakeOverAutomation200Response**](TakeOverAutomation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Automation taken over |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Not the owner or an admin of the active workspace (insufficient_permissions). |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="testautomation"></a>
# **TestAutomation**
> TestAutomation200Response TestAutomation (string automationId, TestAutomationRequest? testAutomationRequest = null)

Test an automation on a sample event

Runs one sample through the automation's own decision code and says whether it would run, what it matched and the steps it would take. Nothing is claimed, sent or written, whatever the automation does.  What each kind reads:  - Comment to DM: a comment (`event.text`, `event.platformPostId`). - Flow: an inbound event (`event.trigger`, `event.text`, `event.firstMessage`). - Event automation: the event's webhook payload, or the sample payload when `event` is left out. - Ad rule: the ad account as it is now, like a preview. `subjectId` narrows to one object. - Scheduled automation: the posts it would check now, and its next check. `subjectId` narrows to one post. - Sequence: the contact in `subjectId`.  A paused or draft automation is tested as if it were live, and answers `wouldRun: false` with its status as `reason`. Cooldowns, daily caps and a conversation's live run read history and are left out. `GET /v1/automations/{automationId}/test/sample` returns a body to start from. 

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
    public class TestAutomationExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 
            var testAutomationRequest = new TestAutomationRequest?(); // TestAutomationRequest? |  (optional) 

            try
            {
                // Test an automation on a sample event
                TestAutomation200Response result = apiInstance.TestAutomation(automationId, testAutomationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.TestAutomation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TestAutomationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Test an automation on a sample event
    ApiResponse<TestAutomation200Response> response = apiInstance.TestAutomationWithHttpInfo(automationId, testAutomationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.TestAutomationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |
| **testAutomationRequest** | [**TestAutomationRequest?**](TestAutomationRequest?.md) |  | [optional]  |

### Return type

[**TestAutomation200Response**](TestAutomation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Decision |  -  |
| **400** | The automation is invalid, or holds something its kind cannot: &#x60;details.problems&#x60; lists each problem with its JSON path. A few ad rule checks (an unsupported platform, step or metric, a cooldown shorter than the schedule, approvers not on the team) answer with &#x60;param&#x60; instead. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ad rules only: your account has no ads access (code &#x60;ads_addon_required&#x60;). Ads are included on usage-based plans. Event and scheduled automations never get this 403: a boost step without ads access is refused with a 400 at its path. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateautomation"></a>
# **UpdateAutomation**
> CreateAutomation201Response UpdateAutomation (string automationId, UpdateAutomationRequest updateAutomationRequest, string? ifMatch = null)

Edit an automation

Replaces the top-level fields you send and keeps the rest: to change one step, send all of `steps`. The result is checked as a whole automation, so problems carry the same paths as on create.  An automation keeps its kind, and an ad rule stays on its ad account. Send `alert: null` to remove an ad rule's alert.  Send the `version` you read as `If-Match`: if the automation was saved since, the edit is refused with a 409 (`automation_stale`). An edit is also refused with a 409 when another save lands while it is being applied. 

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
    public class UpdateAutomationExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var automationId = "automationId_example";  // string | 
            var updateAutomationRequest = new UpdateAutomationRequest(); // UpdateAutomationRequest | 
            var ifMatch = "ifMatch_example";  // string? | The automation's `version` when you read it. (optional) 

            try
            {
                // Edit an automation
                CreateAutomation201Response result = apiInstance.UpdateAutomation(automationId, updateAutomationRequest, ifMatch);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.UpdateAutomation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAutomationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Edit an automation
    ApiResponse<CreateAutomation201Response> response = apiInstance.UpdateAutomationWithHttpInfo(automationId, updateAutomationRequest, ifMatch);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.UpdateAutomationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **automationId** | **string** |  |  |
| **updateAutomationRequest** | [**UpdateAutomationRequest**](UpdateAutomationRequest.md) |  |  |
| **ifMatch** | **string?** | The automation&#39;s &#x60;version&#x60; when you read it. | [optional]  |

### Return type

[**CreateAutomation201Response**](CreateAutomation201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Automation updated |  -  |
| **400** | The automation is invalid, or holds something its kind cannot: &#x60;details.problems&#x60; lists each problem with its JSON path. A few ad rule checks (an unsupported platform, step or metric, a cooldown shorter than the schedule, approvers not on the team) answer with &#x60;param&#x60; instead. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ad rules only: your account has no ads access (code &#x60;ads_addon_required&#x60;). Ads are included on usage-based plans. Event and scheduled automations never get this 403: a boost step without ads access is refused with a 400 at its path. |  -  |
| **404** | Resource not found |  -  |
| **409** | The automation was saved after the &#x60;version&#x60; in &#x60;If-Match&#x60; (code &#x60;automation_stale&#x60;). &#x60;details.version&#x60; is the current one: read it again and resend your edit. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateautomationadaccountcontrols"></a>
# **UpdateAutomationAdAccountControls**
> GetAutomationControls200Response UpdateAutomationAdAccountControls (UpdateAutomationAdAccountControlsRequest updateAutomationAdAccountControlsRequest)

Update one ad account's controls

Turns ad rules off or on for one ad account, sets its daily raise limit, or both. Send at least one of `paused` and `dailyRaiseLimit`; fields you leave out keep their value.  The ad account must be one the connection in `accountId` reaches, as for an automation on it. Controls apply to every ad rule of the team on that ad account. 

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
    public class UpdateAutomationAdAccountControlsExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var updateAutomationAdAccountControlsRequest = new UpdateAutomationAdAccountControlsRequest(); // UpdateAutomationAdAccountControlsRequest | 

            try
            {
                // Update one ad account's controls
                GetAutomationControls200Response result = apiInstance.UpdateAutomationAdAccountControls(updateAutomationAdAccountControlsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.UpdateAutomationAdAccountControls: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAutomationAdAccountControlsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update one ad account's controls
    ApiResponse<GetAutomationControls200Response> response = apiInstance.UpdateAutomationAdAccountControlsWithHttpInfo(updateAutomationAdAccountControlsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.UpdateAutomationAdAccountControlsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateAutomationAdAccountControlsRequest** | [**UpdateAutomationAdAccountControlsRequest**](UpdateAutomationAdAccountControlsRequest.md) |  |  |

### Return type

[**GetAutomationControls200Response**](GetAutomationControls200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The controls after the change |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;ads_addon_required&#x60; when the account has no ads access, or &#x60;ad_account_not_selected&#x60; when the ad account is not among the connection&#39;s selected ad accounts. |  -  |
| **404** | Resource not found |  -  |
| **409** | Code &#x60;ads_connection_required&#x60;: the connection needs reconnecting. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateautomationcontrols"></a>
# **UpdateAutomationControls**
> GetAutomationControls200Response UpdateAutomationControls (UpdateAutomationControlsRequest updateAutomationControlsRequest)

Turn every ad automation off or on

Turns every ad rule of the team off (`paused: true`) or back on. Each rule keeps its own status, so turning the switch back on resumes exactly the rules that were active.  Scheduled automations that boost posts are not stopped by it: pause them one by one.  It reaches every profile, so only the account owner or a full-access team member can use it. A key limited to some profiles gets 403.  Turning off a switch that is already off keeps its original `pausedAt`. 

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
    public class UpdateAutomationControlsExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var updateAutomationControlsRequest = new UpdateAutomationControlsRequest(); // UpdateAutomationControlsRequest | 

            try
            {
                // Turn every ad automation off or on
                GetAutomationControls200Response result = apiInstance.UpdateAutomationControls(updateAutomationControlsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.UpdateAutomationControls: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAutomationControlsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Turn every ad automation off or on
    ApiResponse<GetAutomationControls200Response> response = apiInstance.UpdateAutomationControlsWithHttpInfo(updateAutomationControlsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.UpdateAutomationControlsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateAutomationControlsRequest** | [**UpdateAutomationControlsRequest**](UpdateAutomationControlsRequest.md) |  |  |

### Return type

[**GetAutomationControls200Response**](GetAutomationControls200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The controls after the change |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;insufficient_permissions&#x60; when the caller is not the account owner or a full-access team member, or &#x60;ads_addon_required&#x60; when the account has no ads access. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateautomationtemplate"></a>
# **UpdateAutomationTemplate**
> CreateAutomationTemplate201Response UpdateAutomationTemplate (string templateId, UpdateAutomationTemplateRequest updateAutomationTemplateRequest)

Update an automation template

Renames a template, turns its share link on or off, or replaces its automations. Send at least one field.  Renaming or sharing keeps the `version`. New content (`from` or `automations`) is a new version; automations already installed keep the version they came from.  `visibility: link` turns the share link on (the same link while it stays on) and `visibility: team` revokes it. To copy a shared template, use `POST /v1/automations/templates` instead. 

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
    public class UpdateAutomationTemplateExample
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
            var apiInstance = new AutomationsApi(httpClient, config, httpClientHandler);
            var templateId = "templateId_example";  // string | The template's id.
            var updateAutomationTemplateRequest = new UpdateAutomationTemplateRequest(); // UpdateAutomationTemplateRequest | 

            try
            {
                // Update an automation template
                CreateAutomationTemplate201Response result = apiInstance.UpdateAutomationTemplate(templateId, updateAutomationTemplateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutomationsApi.UpdateAutomationTemplate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAutomationTemplateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update an automation template
    ApiResponse<CreateAutomationTemplate201Response> response = apiInstance.UpdateAutomationTemplateWithHttpInfo(templateId, updateAutomationTemplateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutomationsApi.UpdateAutomationTemplateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** | The template&#39;s id. |  |
| **updateAutomationTemplateRequest** | [**UpdateAutomationTemplateRequest**](UpdateAutomationTemplateRequest.md) |  |  |

### Return type

[**CreateAutomationTemplate201Response**](CreateAutomationTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Template updated |  -  |
| **400** | The automation is invalid, or holds something its kind cannot: &#x60;details.problems&#x60; lists each problem with its JSON path. A few ad rule checks (an unsupported platform, step or metric, a cooldown shorter than the schedule, approvers not on the team) answer with &#x60;param&#x60; instead. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | No template with this id in your team, or a source in &#x60;from&#x60; was not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

