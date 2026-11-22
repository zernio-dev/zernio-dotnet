# Zernio.Api.WorkspacesApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateWorkspace**](WorkspacesApi.md#createworkspace) | **POST** /v1/workspaces | Create workspace |
| [**CreateWorkspaceApiKey**](WorkspacesApi.md#createworkspaceapikey) | **POST** /v1/workspaces/{workspaceId}/api-keys | Create workspace key |
| [**DeleteWorkspace**](WorkspacesApi.md#deleteworkspace) | **DELETE** /v1/workspaces/{workspaceId} | Delete workspace |
| [**GetWorkspace**](WorkspacesApi.md#getworkspace) | **GET** /v1/workspaces/{workspaceId} | Get workspace |
| [**ListWorkspaces**](WorkspacesApi.md#listworkspaces) | **GET** /v1/workspaces | List workspaces |
| [**UpdateWorkspace**](WorkspacesApi.md#updateworkspace) | **PATCH** /v1/workspaces/{workspaceId} | Rename workspace |

<a id="createworkspace"></a>
# **CreateWorkspace**
> CreateWorkspace201Response CreateWorkspace (CreateWorkspaceRequest createWorkspaceRequest)

Create workspace

Creates a new, empty workspace owned by the key's owner, for example one per client of your product.  - Send `apiKey` to get the new workspace's first key in the same call. A key only manages its own workspace, so no other key can mint one there later. - The workspace has no billing. Its keys can read, but writes return 402 `workspace_billing_required` until billing is set up at `billing.setupUrl`. - Needs a full-access key. Creation is capped at 5 a day and 20 owned workspaces without billing (429). 

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
    public class CreateWorkspaceExample
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
            var apiInstance = new WorkspacesApi(httpClient, config, httpClientHandler);
            var createWorkspaceRequest = new CreateWorkspaceRequest(); // CreateWorkspaceRequest | 

            try
            {
                // Create workspace
                CreateWorkspace201Response result = apiInstance.CreateWorkspace(createWorkspaceRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.CreateWorkspace: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateWorkspaceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create workspace
    ApiResponse<CreateWorkspace201Response> response = apiInstance.CreateWorkspaceWithHttpInfo(createWorkspaceRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.CreateWorkspaceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createWorkspaceRequest** | [**CreateWorkspaceRequest**](CreateWorkspaceRequest.md) |  |  |

### Return type

[**CreateWorkspace201Response**](CreateWorkspace201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | The calling key acts in a workspace without billing, which cannot make changes through the API. Error code: workspace_billing_required. Set billing up for that workspace in the dashboard. |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |
| **429** | Creation cap reached. Error code: workspace_daily_limit_reached (5 a day) or workspace_limit_reached (20 owned without billing). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createworkspaceapikey"></a>
# **CreateWorkspaceApiKey**
> CreateWorkspaceApiKey201Response CreateWorkspaceApiKey (string workspaceId, CreateWorkspaceApiKeyRequest createWorkspaceApiKeyRequest)

Create workspace key

Creates another API key that acts in this workspace as its creator. It covers every profile, and its full value is returned only once.  - The caller must be owner or admin there. - The calling credential must be a full-access key of this same workspace. Profile-scoped, restricted and handed-over keys, OAuth tokens and keys of other workspaces get 403. - For another workspace, use the dashboard. For a new one, send `apiKey` on `POST /v1/workspaces`. 

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
    public class CreateWorkspaceApiKeyExample
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
            var apiInstance = new WorkspacesApi(httpClient, config, httpClientHandler);
            var workspaceId = "workspaceId_example";  // string | 
            var createWorkspaceApiKeyRequest = new CreateWorkspaceApiKeyRequest(); // CreateWorkspaceApiKeyRequest | 

            try
            {
                // Create workspace key
                CreateWorkspaceApiKey201Response result = apiInstance.CreateWorkspaceApiKey(workspaceId, createWorkspaceApiKeyRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.CreateWorkspaceApiKey: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateWorkspaceApiKeyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create workspace key
    ApiResponse<CreateWorkspaceApiKey201Response> response = apiInstance.CreateWorkspaceApiKeyWithHttpInfo(workspaceId, createWorkspaceApiKeyRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.CreateWorkspaceApiKeyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceId** | **string** |  |  |
| **createWorkspaceApiKeyRequest** | [**CreateWorkspaceApiKeyRequest**](CreateWorkspaceApiKeyRequest.md) |  |  |

### Return type

[**CreateWorkspaceApiKey201Response**](CreateWorkspaceApiKey201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | The calling key acts in a workspace without billing, which cannot make changes through the API. Error code: workspace_billing_required. Set billing up for that workspace in the dashboard. |  -  |
| **403** | The caller is not owner or admin there (workspace_forbidden), or the calling credential is not a full-access key of this workspace (insufficient_permissions). |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteworkspace"></a>
# **DeleteWorkspace**
> GetWorkspace200Response DeleteWorkspace (string workspaceId, string? moveBalanceTo = null, bool? forfeitBalance = null)

Delete workspace

Schedules the workspace for deletion 48 hours ahead, as the dashboard does. Members keep working, publishing is paused, and the owner or an admin can cancel from the dashboard until then. Only this workspace's data is deleted, never its members' accounts.  - Owner only, with a full-access key of this workspace. A key of another workspace gets 403; delete it from the dashboard. - A Personal workspace is never deleted. - Refused while the workspace owes a payment or holds a phone number or carrier registration (409 `deletion_blocked`). - With a balance above $0, send `moveBalanceTo` (another billed workspace you own) or `forfeitBalance=true`. Balances are never refunded. Without either the call returns 422 `deletion_balance_choice`. 

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
    public class DeleteWorkspaceExample
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
            var apiInstance = new WorkspacesApi(httpClient, config, httpClientHandler);
            var workspaceId = "workspaceId_example";  // string | 
            var moveBalanceTo = "moveBalanceTo_example";  // string? | A billed workspace you own that receives the remaining balance. (optional) 
            var forfeitBalance = true;  // bool? | Leave the remaining balance; it is written off when the workspace is deleted. (optional) 

            try
            {
                // Delete workspace
                GetWorkspace200Response result = apiInstance.DeleteWorkspace(workspaceId, moveBalanceTo, forfeitBalance);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.DeleteWorkspace: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteWorkspaceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete workspace
    ApiResponse<GetWorkspace200Response> response = apiInstance.DeleteWorkspaceWithHttpInfo(workspaceId, moveBalanceTo, forfeitBalance);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.DeleteWorkspaceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceId** | **string** |  |  |
| **moveBalanceTo** | **string?** | A billed workspace you own that receives the remaining balance. | [optional]  |
| **forfeitBalance** | **bool?** | Leave the remaining balance; it is written off when the workspace is deleted. | [optional]  |

### Return type

[**GetWorkspace200Response**](GetWorkspace200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deletion scheduled |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | The calling key acts in a workspace without billing, which cannot make changes through the API. Error code: workspace_billing_required. Set billing up for that workspace in the dashboard. |  -  |
| **403** | Only the owner can delete a workspace (workspace_forbidden), with a full-access key of this workspace (insufficient_permissions otherwise). |  -  |
| **404** | Resource not found |  -  |
| **409** | Refused: personal_workspace, deletion_already_scheduled, or deletion_blocked (a payment due, a phone number or a carrier registration; the message names it). |  -  |
| **422** | The workspace has a balance: send moveBalanceTo or forfeitBalance. Error code: deletion_balance_choice. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getworkspace"></a>
# **GetWorkspace**
> GetWorkspace200Response GetWorkspace (string workspaceId)

Get workspace

Returns one workspace the key's owner belongs to, with their role. Owners, admins and billing admins also get `billing` (whether it is set up, and where to set it up); members and viewers do not.

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
    public class GetWorkspaceExample
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
            var apiInstance = new WorkspacesApi(httpClient, config, httpClientHandler);
            var workspaceId = "workspaceId_example";  // string | 

            try
            {
                // Get workspace
                GetWorkspace200Response result = apiInstance.GetWorkspace(workspaceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.GetWorkspace: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWorkspaceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get workspace
    ApiResponse<GetWorkspace200Response> response = apiInstance.GetWorkspaceWithHttpInfo(workspaceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.GetWorkspaceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceId** | **string** |  |  |

### Return type

[**GetWorkspace200Response**](GetWorkspace200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Workspace |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listworkspaces"></a>
# **ListWorkspaces**
> ListWorkspaces200Response ListWorkspaces (int? limit = null, int? skip = null)

List workspaces

Lists every workspace the key's owner belongs to, with their role in each: teams first by name, their Personal workspace last. Any key of the owner lists them all, whatever workspace that key acts in.

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
    public class ListWorkspacesExample
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
            var apiInstance = new WorkspacesApi(httpClient, config, httpClientHandler);
            var limit = 50;  // int? | Page size. (optional)  (default to 50)
            var skip = 0;  // int? | Number of workspaces to skip. (optional)  (default to 0)

            try
            {
                // List workspaces
                ListWorkspaces200Response result = apiInstance.ListWorkspaces(limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.ListWorkspaces: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWorkspacesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List workspaces
    ApiResponse<ListWorkspaces200Response> response = apiInstance.ListWorkspacesWithHttpInfo(limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.ListWorkspacesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int?** | Page size. | [optional] [default to 50] |
| **skip** | **int?** | Number of workspaces to skip. | [optional] [default to 0] |

### Return type

[**ListWorkspaces200Response**](ListWorkspaces200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Workspaces |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateworkspace"></a>
# **UpdateWorkspace**
> GetWorkspace200Response UpdateWorkspace (string workspaceId, UpdateWorkspaceRequest updateWorkspaceRequest)

Rename workspace

Renames a workspace. Owner or admin there, with a full-access key of this workspace (a key of another workspace gets 403: rename it from the dashboard). Only a Personal workspace can be called \"Personal\".

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
    public class UpdateWorkspaceExample
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
            var apiInstance = new WorkspacesApi(httpClient, config, httpClientHandler);
            var workspaceId = "workspaceId_example";  // string | 
            var updateWorkspaceRequest = new UpdateWorkspaceRequest(); // UpdateWorkspaceRequest | 

            try
            {
                // Rename workspace
                GetWorkspace200Response result = apiInstance.UpdateWorkspace(workspaceId, updateWorkspaceRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.UpdateWorkspace: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateWorkspaceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Rename workspace
    ApiResponse<GetWorkspace200Response> response = apiInstance.UpdateWorkspaceWithHttpInfo(workspaceId, updateWorkspaceRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.UpdateWorkspaceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceId** | **string** |  |  |
| **updateWorkspaceRequest** | [**UpdateWorkspaceRequest**](UpdateWorkspaceRequest.md) |  |  |

### Return type

[**GetWorkspace200Response**](GetWorkspace200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Renamed |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | The calling key acts in a workspace without billing, which cannot make changes through the API. Error code: workspace_billing_required. Set billing up for that workspace in the dashboard. |  -  |
| **403** | The role there cannot rename it (workspace_forbidden), the key is not a full-access key, or the key acts in another workspace (insufficient_permissions: use a key of this workspace or the dashboard). |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

