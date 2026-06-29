# Zernio.Api.WorkflowsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ActivateWorkflow**](WorkflowsApi.md#activateworkflow) | **POST** /v1/workflows/{workflowId}/activate | Activate workflow |
| [**CreateWorkflow**](WorkflowsApi.md#createworkflow) | **POST** /v1/workflows | Create workflow |
| [**DeleteWorkflow**](WorkflowsApi.md#deleteworkflow) | **DELETE** /v1/workflows/{workflowId} | Delete workflow |
| [**DuplicateWorkflow**](WorkflowsApi.md#duplicateworkflow) | **POST** /v1/workflows/{workflowId}/duplicate | Duplicate a workflow |
| [**GetWorkflow**](WorkflowsApi.md#getworkflow) | **GET** /v1/workflows/{workflowId} | Get workflow with graph |
| [**GetWorkflowVersion**](WorkflowsApi.md#getworkflowversion) | **GET** /v1/workflows/{workflowId}/versions/{version} | Get a specific workflow version |
| [**ListWorkflowExecutionEvents**](WorkflowsApi.md#listworkflowexecutionevents) | **GET** /v1/workflows/{workflowId}/executions/{executionId}/events | Get an execution&#39;s timeline |
| [**ListWorkflowExecutions**](WorkflowsApi.md#listworkflowexecutions) | **GET** /v1/workflows/{workflowId}/executions | List workflow runs |
| [**ListWorkflowVersions**](WorkflowsApi.md#listworkflowversions) | **GET** /v1/workflows/{workflowId}/versions | List a workflow&#39;s version history |
| [**ListWorkflows**](WorkflowsApi.md#listworkflows) | **GET** /v1/workflows | List workflows |
| [**PauseWorkflow**](WorkflowsApi.md#pauseworkflow) | **POST** /v1/workflows/{workflowId}/pause | Pause workflow |
| [**RestoreWorkflowVersion**](WorkflowsApi.md#restoreworkflowversion) | **POST** /v1/workflows/{workflowId}/versions/{version}/restore | Restore a workflow version |
| [**TriggerWorkflow**](WorkflowsApi.md#triggerworkflow) | **POST** /v1/workflows/{workflowId}/executions | Manually start a workflow run |
| [**UpdateWorkflow**](WorkflowsApi.md#updateworkflow) | **PATCH** /v1/workflows/{workflowId} | Update workflow |

<a id="activateworkflow"></a>
# **ActivateWorkflow**
> ActivateWorkflow200Response ActivateWorkflow (string workflowId)

Activate workflow

Validate the graph is runnable and set the workflow live. Once active, matching inbound messages start executions. Idempotent.

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
    public class ActivateWorkflowExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var workflowId = "workflowId_example";  // string | 

            try
            {
                // Activate workflow
                ActivateWorkflow200Response result = apiInstance.ActivateWorkflow(workflowId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.ActivateWorkflow: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ActivateWorkflowWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Activate workflow
    ApiResponse<ActivateWorkflow200Response> response = apiInstance.ActivateWorkflowWithHttpInfo(workflowId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.ActivateWorkflowWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workflowId** | **string** |  |  |

### Return type

[**ActivateWorkflow200Response**](ActivateWorkflow200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Workflow activated |  -  |
| **400** | Incomplete or invalid graph |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createworkflow"></a>
# **CreateWorkflow**
> CreateWorkflow200Response CreateWorkflow (CreateWorkflowRequest createWorkflowRequest)

Create workflow

Create a branching conversation workflow (draft) from a node/edge graph. Created in `draft` status; activate it to start matching inbound messages. The graph is validated structurally; completeness (a trigger node + reachable entry) is required at activation. 

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
    public class CreateWorkflowExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var createWorkflowRequest = new CreateWorkflowRequest(); // CreateWorkflowRequest | 

            try
            {
                // Create workflow
                CreateWorkflow200Response result = apiInstance.CreateWorkflow(createWorkflowRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.CreateWorkflow: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateWorkflowWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create workflow
    ApiResponse<CreateWorkflow200Response> response = apiInstance.CreateWorkflowWithHttpInfo(createWorkflowRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.CreateWorkflowWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createWorkflowRequest** | [**CreateWorkflowRequest**](CreateWorkflowRequest.md) |  |  |

### Return type

[**CreateWorkflow200Response**](CreateWorkflow200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Workflow created |  -  |
| **400** | Invalid graph (duplicate node ids, edges referencing missing nodes, or a WhatsApp-only node on another platform) |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteworkflow"></a>
# **DeleteWorkflow**
> void DeleteWorkflow (string workflowId)

Delete workflow

Permanently delete a workflow and all of its executions.

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
    public class DeleteWorkflowExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var workflowId = "workflowId_example";  // string | 

            try
            {
                // Delete workflow
                apiInstance.DeleteWorkflow(workflowId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.DeleteWorkflow: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteWorkflowWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete workflow
    apiInstance.DeleteWorkflowWithHttpInfo(workflowId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.DeleteWorkflowWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workflowId** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Workflow deleted |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="duplicateworkflow"></a>
# **DuplicateWorkflow**
> DuplicateWorkflow201Response DuplicateWorkflow (string workflowId)

Duplicate a workflow

Create an independent copy of a workflow's graph, name, description, and account binding. The copy is created in `draft` status with fresh execution counters and a new id — execution history is NOT copied. Useful for branching off a known-good workflow before making experimental edits. 

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
    public class DuplicateWorkflowExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var workflowId = "workflowId_example";  // string | 

            try
            {
                // Duplicate a workflow
                DuplicateWorkflow201Response result = apiInstance.DuplicateWorkflow(workflowId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.DuplicateWorkflow: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuplicateWorkflowWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Duplicate a workflow
    ApiResponse<DuplicateWorkflow201Response> response = apiInstance.DuplicateWorkflowWithHttpInfo(workflowId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.DuplicateWorkflowWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workflowId** | **string** |  |  |

### Return type

[**DuplicateWorkflow201Response**](DuplicateWorkflow201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Workflow duplicated |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getworkflow"></a>
# **GetWorkflow**
> GetWorkflow200Response GetWorkflow (string workflowId)

Get workflow with graph

Returns a workflow including its full node/edge graph and run stats.

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
    public class GetWorkflowExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var workflowId = "workflowId_example";  // string | 

            try
            {
                // Get workflow with graph
                GetWorkflow200Response result = apiInstance.GetWorkflow(workflowId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.GetWorkflow: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWorkflowWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get workflow with graph
    ApiResponse<GetWorkflow200Response> response = apiInstance.GetWorkflowWithHttpInfo(workflowId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.GetWorkflowWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workflowId** | **string** |  |  |

### Return type

[**GetWorkflow200Response**](GetWorkflow200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Workflow details |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getworkflowversion"></a>
# **GetWorkflowVersion**
> GetWorkflowVersion200Response GetWorkflowVersion (string workflowId, int version)

Get a specific workflow version

Returns the full snapshot for a single historical version, including the graph.

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
    public class GetWorkflowVersionExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var workflowId = "workflowId_example";  // string | 
            var version = 56;  // int | 

            try
            {
                // Get a specific workflow version
                GetWorkflowVersion200Response result = apiInstance.GetWorkflowVersion(workflowId, version);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.GetWorkflowVersion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWorkflowVersionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a specific workflow version
    ApiResponse<GetWorkflowVersion200Response> response = apiInstance.GetWorkflowVersionWithHttpInfo(workflowId, version);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.GetWorkflowVersionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workflowId** | **string** |  |  |
| **version** | **int** |  |  |

### Return type

[**GetWorkflowVersion200Response**](GetWorkflowVersion200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Version snapshot |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listworkflowexecutionevents"></a>
# **ListWorkflowExecutionEvents**
> ListWorkflowExecutionEvents200Response ListWorkflowExecutionEvents (string workflowId, string executionId)

Get an execution's timeline

Returns the per-step run-log for a single workflow execution: trigger fired, each node visited, edge handles taken, errors, and durations. Backed by Tinybird (90-day retention). Used by the Runs UI drawer to render the timeline. 

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
    public class ListWorkflowExecutionEventsExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var workflowId = "workflowId_example";  // string | 
            var executionId = "executionId_example";  // string | 

            try
            {
                // Get an execution's timeline
                ListWorkflowExecutionEvents200Response result = apiInstance.ListWorkflowExecutionEvents(workflowId, executionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.ListWorkflowExecutionEvents: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWorkflowExecutionEventsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an execution's timeline
    ApiResponse<ListWorkflowExecutionEvents200Response> response = apiInstance.ListWorkflowExecutionEventsWithHttpInfo(workflowId, executionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.ListWorkflowExecutionEventsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workflowId** | **string** |  |  |
| **executionId** | **string** |  |  |

### Return type

[**ListWorkflowExecutionEvents200Response**](ListWorkflowExecutionEvents200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Timeline events for the execution |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listworkflowexecutions"></a>
# **ListWorkflowExecutions**
> ListWorkflowExecutions200Response ListWorkflowExecutions (string workflowId, string? status = null, int? limit = null, int? skip = null)

List workflow runs

Returns recent executions (runs) with their status, current node, and accumulated variables.

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
    public class ListWorkflowExecutionsExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var workflowId = "workflowId_example";  // string | 
            var status = "running";  // string? |  (optional) 
            var limit = 25;  // int? |  (optional)  (default to 25)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List workflow runs
                ListWorkflowExecutions200Response result = apiInstance.ListWorkflowExecutions(workflowId, status, limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.ListWorkflowExecutions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWorkflowExecutionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List workflow runs
    ApiResponse<ListWorkflowExecutions200Response> response = apiInstance.ListWorkflowExecutionsWithHttpInfo(workflowId, status, limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.ListWorkflowExecutionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workflowId** | **string** |  |  |
| **status** | **string?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**ListWorkflowExecutions200Response**](ListWorkflowExecutions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Executions list |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listworkflowversions"></a>
# **ListWorkflowVersions**
> ListWorkflowVersions200Response ListWorkflowVersions (string workflowId)

List a workflow's version history

Returns the snapshot history. A new version is recorded automatically before every PATCH to `nodes` / `edges` / `entryNodeId`, and explicitly when a previous version is restored. Lightweight list — call `getWorkflowVersion` for the full snapshot graph. 

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
    public class ListWorkflowVersionsExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var workflowId = "workflowId_example";  // string | 

            try
            {
                // List a workflow's version history
                ListWorkflowVersions200Response result = apiInstance.ListWorkflowVersions(workflowId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.ListWorkflowVersions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWorkflowVersionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List a workflow's version history
    ApiResponse<ListWorkflowVersions200Response> response = apiInstance.ListWorkflowVersionsWithHttpInfo(workflowId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.ListWorkflowVersionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workflowId** | **string** |  |  |

### Return type

[**ListWorkflowVersions200Response**](ListWorkflowVersions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Versions list |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listworkflows"></a>
# **ListWorkflows**
> ListWorkflows200Response ListWorkflows (string? profileId = null, string? status = null, int? limit = null, int? skip = null)

List workflows

Returns workflows with run stats. Filter by status or profile.

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
    public class ListWorkflowsExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? | Filter by profile. Omit to list across all profiles (optional) 
            var status = "draft";  // string? |  (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List workflows
                ListWorkflows200Response result = apiInstance.ListWorkflows(profileId, status, limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.ListWorkflows: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWorkflowsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List workflows
    ApiResponse<ListWorkflows200Response> response = apiInstance.ListWorkflowsWithHttpInfo(profileId, status, limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.ListWorkflowsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** | Filter by profile. Omit to list across all profiles | [optional]  |
| **status** | **string?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**ListWorkflows200Response**](ListWorkflows200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Workflows list |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="pauseworkflow"></a>
# **PauseWorkflow**
> PauseWorkflow200Response PauseWorkflow (string workflowId)

Pause workflow

Stop matching new inbound messages. In-flight executions continue to completion. Idempotent.

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
    public class PauseWorkflowExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var workflowId = "workflowId_example";  // string | 

            try
            {
                // Pause workflow
                PauseWorkflow200Response result = apiInstance.PauseWorkflow(workflowId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.PauseWorkflow: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PauseWorkflowWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pause workflow
    ApiResponse<PauseWorkflow200Response> response = apiInstance.PauseWorkflowWithHttpInfo(workflowId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.PauseWorkflowWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workflowId** | **string** |  |  |

### Return type

[**PauseWorkflow200Response**](PauseWorkflow200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Workflow paused |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="restoreworkflowversion"></a>
# **RestoreWorkflowVersion**
> RestoreWorkflowVersion200Response RestoreWorkflowVersion (string workflowId, int version)

Restore a workflow version

Replace the current graph with the named version's snapshot. Before the swap, the current graph is itself snapshotted as a new version, so a restore is reversible. The workflow must be in `draft` or `paused` status (same gate as a normal graph edit). The returned workflow carries `restoredFromVersion` so the UI can surface which version was rolled back to. 

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
    public class RestoreWorkflowVersionExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var workflowId = "workflowId_example";  // string | 
            var version = 56;  // int | 

            try
            {
                // Restore a workflow version
                RestoreWorkflowVersion200Response result = apiInstance.RestoreWorkflowVersion(workflowId, version);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.RestoreWorkflowVersion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreWorkflowVersionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore a workflow version
    ApiResponse<RestoreWorkflowVersion200Response> response = apiInstance.RestoreWorkflowVersionWithHttpInfo(workflowId, version);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.RestoreWorkflowVersionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workflowId** | **string** |  |  |
| **version** | **int** |  |  |

### Return type

[**RestoreWorkflowVersion200Response**](RestoreWorkflowVersion200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Workflow restored to the named version |  -  |
| **400** | Workflow is not draft/paused, or the named version&#39;s graph is invalid for the current platform |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="triggerworkflow"></a>
# **TriggerWorkflow**
> TriggerWorkflow200Response TriggerWorkflow (string workflowId, TriggerWorkflowRequest triggerWorkflowRequest)

Manually start a workflow run

Kick off a run without waiting for an inbound message (useful for testing). Target an existing conversation by `conversationId`, or — WhatsApp only — a phone number via `to` (a conversation is found or created). `text` seeds the run's `lastMessage` variable. The graph must be runnable. 

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
    public class TriggerWorkflowExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var workflowId = "workflowId_example";  // string | 
            var triggerWorkflowRequest = new TriggerWorkflowRequest(); // TriggerWorkflowRequest | 

            try
            {
                // Manually start a workflow run
                TriggerWorkflow200Response result = apiInstance.TriggerWorkflow(workflowId, triggerWorkflowRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.TriggerWorkflow: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TriggerWorkflowWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Manually start a workflow run
    ApiResponse<TriggerWorkflow200Response> response = apiInstance.TriggerWorkflowWithHttpInfo(workflowId, triggerWorkflowRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.TriggerWorkflowWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workflowId** | **string** |  |  |
| **triggerWorkflowRequest** | [**TriggerWorkflowRequest**](TriggerWorkflowRequest.md) |  |  |

### Return type

[**TriggerWorkflow200Response**](TriggerWorkflow200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Run started |  -  |
| **400** | Missing target, invalid graph, or &#x60;to&#x60; used on a non-WhatsApp workflow |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateworkflow"></a>
# **UpdateWorkflow**
> UpdateWorkflow200Response UpdateWorkflow (string workflowId, UpdateWorkflowRequest? updateWorkflowRequest = null)

Update workflow

Update name, description, the graph, or reassign to a different account. The graph can only be modified while the workflow is draft or paused. Account swaps re-validate the graph against the new platform (so e.g. moving from WhatsApp to Facebook surfaces a `start_call` node as an error instead of silently saving an unrunnable graph). 

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
    public class UpdateWorkflowExample
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
            var apiInstance = new WorkflowsApi(httpClient, config, httpClientHandler);
            var workflowId = "workflowId_example";  // string | 
            var updateWorkflowRequest = new UpdateWorkflowRequest?(); // UpdateWorkflowRequest? |  (optional) 

            try
            {
                // Update workflow
                UpdateWorkflow200Response result = apiInstance.UpdateWorkflow(workflowId, updateWorkflowRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkflowsApi.UpdateWorkflow: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateWorkflowWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update workflow
    ApiResponse<UpdateWorkflow200Response> response = apiInstance.UpdateWorkflowWithHttpInfo(workflowId, updateWorkflowRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkflowsApi.UpdateWorkflowWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workflowId** | **string** |  |  |
| **updateWorkflowRequest** | [**UpdateWorkflowRequest?**](UpdateWorkflowRequest?.md) |  | [optional]  |

### Return type

[**UpdateWorkflow200Response**](UpdateWorkflow200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Workflow updated |  -  |
| **400** | Invalid graph, or a graph edit attempted while the workflow is active |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

