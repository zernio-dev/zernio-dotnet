# Zernio.Api.RCSApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddRcsTestDevice**](RCSApi.md#addrcstestdevice) | **POST** /v1/rcs/agents/{agentId}/test-devices | Invite an RCS test phone |
| [**CreateRcsAgent**](RCSApi.md#creatercsagent) | **POST** /v1/rcs/agents | Request an RCS agent |
| [**DeactivateRcsAgent**](RCSApi.md#deactivatercsagent) | **DELETE** /v1/rcs/agents/{agentId} | Deactivate an RCS agent |
| [**GetRcsAgent**](RCSApi.md#getrcsagent) | **GET** /v1/rcs/agents/{agentId} | Get an RCS agent |
| [**GetRcsCapabilities**](RCSApi.md#getrcscapabilities) | **GET** /v1/rcs/capabilities | Check RCS capability |
| [**ListRcsAgents**](RCSApi.md#listrcsagents) | **GET** /v1/rcs/agents | List RCS agents |
| [**ListRcsBrands**](RCSApi.md#listrcsbrands) | **GET** /v1/rcs/brands | List RCS brands |
| [**ListRcsTestDevices**](RCSApi.md#listrcstestdevices) | **GET** /v1/rcs/agents/{agentId}/test-devices | List RCS test phones |
| [**RemoveRcsTestDevice**](RCSApi.md#removercstestdevice) | **DELETE** /v1/rcs/agents/{agentId}/test-devices/{testDeviceId} | Remove an RCS test phone |
| [**RequestRcsAgentLaunch**](RCSApi.md#requestrcsagentlaunch) | **POST** /v1/rcs/agents/{agentId}/launch-request | Send the launch filing |
| [**SendRcsMessage**](RCSApi.md#sendrcsmessage) | **POST** /v1/rcs/messages | Send an RCS message |
| [**UpdateRcsAgent**](RCSApi.md#updatercsagent) | **PATCH** /v1/rcs/agents/{agentId} | Update an RCS agent |
| [**UploadRcsAsset**](RCSApi.md#uploadrcsasset) | **POST** /v1/rcs/assets | Upload an RCS logo or banner |

<a id="addrcstestdevice"></a>
# **AddRcsTestDevice**
> AddRcsTestDevice201Response AddRcsTestDevice (string agentId, AddRcsTestDeviceRequest addRcsTestDeviceRequest)

Invite an RCS test phone

Invites a phone to try the agent before launch. It must accept the invite in its messaging app. Available once the agent exists with the carriers (after brand vetting). T-Mobile and AT&T numbers cannot be test phones. 

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
    public class AddRcsTestDeviceExample
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
            var apiInstance = new RCSApi(httpClient, config, httpClientHandler);
            var agentId = "agentId_example";  // string | 
            var addRcsTestDeviceRequest = new AddRcsTestDeviceRequest(); // AddRcsTestDeviceRequest | 

            try
            {
                // Invite an RCS test phone
                AddRcsTestDevice201Response result = apiInstance.AddRcsTestDevice(agentId, addRcsTestDeviceRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RCSApi.AddRcsTestDevice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddRcsTestDeviceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Invite an RCS test phone
    ApiResponse<AddRcsTestDevice201Response> response = apiInstance.AddRcsTestDeviceWithHttpInfo(agentId, addRcsTestDeviceRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RCSApi.AddRcsTestDeviceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **agentId** | **string** |  |  |
| **addRcsTestDeviceRequest** | [**AddRcsTestDeviceRequest**](AddRcsTestDeviceRequest.md) |  |  |

### Return type

[**AddRcsTestDevice201Response**](AddRcsTestDevice201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Invite sent. |  -  |
| **400** | Invalid phone number, or the carrier refused it as a test phone |  -  |
| **401** | Unauthorized |  -  |
| **403** | Your plan does not include the inbox, which RCS requires. |  -  |
| **404** | Agent not found |  -  |
| **409** | The agent does not exist with the carriers yet |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="creatercsagent"></a>
# **CreateRcsAgent**
> CreateRcsAgent201Response CreateRcsAgent (CreateRcsAgentRequest createRcsAgentRequest, string? idempotencyKey = null)

Request an RCS agent

Requests a new agent for a profile, with a new company (`brand`) or an existing one (`brandId`, skips vetting when it is already verified). The request lands in our review: nothing is filed with the carriers or billed until we submit it. One open agent per profile. Requires usage-based billing and a card on file. Send an `Idempotency-Key` header to make retries safe. 

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
    public class CreateRcsAgentExample
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
            var apiInstance = new RCSApi(httpClient, config, httpClientHandler);
            var createRcsAgentRequest = new CreateRcsAgentRequest(); // CreateRcsAgentRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. (optional) 

            try
            {
                // Request an RCS agent
                CreateRcsAgent201Response result = apiInstance.CreateRcsAgent(createRcsAgentRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RCSApi.CreateRcsAgent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateRcsAgentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Request an RCS agent
    ApiResponse<CreateRcsAgent201Response> response = apiInstance.CreateRcsAgentWithHttpInfo(createRcsAgentRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RCSApi.CreateRcsAgentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createRcsAgentRequest** | [**CreateRcsAgentRequest**](CreateRcsAgentRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. | [optional]  |

### Return type

[**CreateRcsAgent201Response**](CreateRcsAgent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Agent requested. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **402** | No payment method on file (payment_method_required). Add a card and retry. |  -  |
| **403** | Your plan does not include the inbox, which RCS requires. |  -  |
| **404** | Profile or brand not found |  -  |
| **409** | The profile already has an open agent, the brand was rejected, or the Idempotency-Key is still in flight |  -  |
| **422** | Usage-based billing is not enabled for the workspace (USAGE_BILLING_REQUIRED), or the Idempotency-Key was reused with a different body |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deactivatercsagent"></a>
# **DeactivateRcsAgent**
> CreateRcsAgent201Response DeactivateRcsAgent (string agentId)

Deactivate an RCS agent

Stops sending, disconnects its inbox account and stops monthly billing. Fees already charged are not refunded.

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
    public class DeactivateRcsAgentExample
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
            var apiInstance = new RCSApi(httpClient, config, httpClientHandler);
            var agentId = "agentId_example";  // string | 

            try
            {
                // Deactivate an RCS agent
                CreateRcsAgent201Response result = apiInstance.DeactivateRcsAgent(agentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RCSApi.DeactivateRcsAgent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeactivateRcsAgentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deactivate an RCS agent
    ApiResponse<CreateRcsAgent201Response> response = apiInstance.DeactivateRcsAgentWithHttpInfo(agentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RCSApi.DeactivateRcsAgentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **agentId** | **string** |  |  |

### Return type

[**CreateRcsAgent201Response**](CreateRcsAgent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The deactivated agent. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Your plan does not include the inbox, which RCS requires. |  -  |
| **404** | Agent not found |  -  |
| **409** | The agent is already rejected or deactivated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getrcsagent"></a>
# **GetRcsAgent**
> CreateRcsAgent201Response GetRcsAgent (string agentId)

Get an RCS agent

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
    public class GetRcsAgentExample
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
            var apiInstance = new RCSApi(httpClient, config, httpClientHandler);
            var agentId = "agentId_example";  // string | 

            try
            {
                // Get an RCS agent
                CreateRcsAgent201Response result = apiInstance.GetRcsAgent(agentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RCSApi.GetRcsAgent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetRcsAgentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an RCS agent
    ApiResponse<CreateRcsAgent201Response> response = apiInstance.GetRcsAgentWithHttpInfo(agentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RCSApi.GetRcsAgentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **agentId** | **string** |  |  |

### Return type

[**CreateRcsAgent201Response**](CreateRcsAgent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The agent with its brand, carrier approvals and test devices. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Your plan does not include the inbox, which RCS requires. |  -  |
| **404** | Agent not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getrcscapabilities"></a>
# **GetRcsCapabilities**
> GetRcsCapabilities200Response GetRcsCapabilities (string agentId, string numbers)

Check RCS capability

Which recipients can receive RCS from the agent and which rich features their phones support. Up to 100 numbers.

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
    public class GetRcsCapabilitiesExample
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
            var apiInstance = new RCSApi(httpClient, config, httpClientHandler);
            var agentId = "agentId_example";  // string | 
            var numbers = "numbers_example";  // string | Comma-separated E.164 numbers, max 100.

            try
            {
                // Check RCS capability
                GetRcsCapabilities200Response result = apiInstance.GetRcsCapabilities(agentId, numbers);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RCSApi.GetRcsCapabilities: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetRcsCapabilitiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check RCS capability
    ApiResponse<GetRcsCapabilities200Response> response = apiInstance.GetRcsCapabilitiesWithHttpInfo(agentId, numbers);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RCSApi.GetRcsCapabilitiesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **agentId** | **string** |  |  |
| **numbers** | **string** | Comma-separated E.164 numbers, max 100. |  |

### Return type

[**GetRcsCapabilities200Response**](GetRcsCapabilities200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One entry per number, in input order. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Your plan does not include the inbox, which RCS requires. |  -  |
| **404** | Agent not found |  -  |
| **409** | The agent does not exist with the carriers yet |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listrcsagents"></a>
# **ListRcsAgents**
> ListRcsAgents200Response ListRcsAgents (bool? includeClosed = null)

List RCS agents

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
    public class ListRcsAgentsExample
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
            var apiInstance = new RCSApi(httpClient, config, httpClientHandler);
            var includeClosed = true;  // bool? | Include rejected and deactivated agents. (optional) 

            try
            {
                // List RCS agents
                ListRcsAgents200Response result = apiInstance.ListRcsAgents(includeClosed);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RCSApi.ListRcsAgents: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListRcsAgentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List RCS agents
    ApiResponse<ListRcsAgents200Response> response = apiInstance.ListRcsAgentsWithHttpInfo(includeClosed);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RCSApi.ListRcsAgentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **includeClosed** | **bool?** | Include rejected and deactivated agents. | [optional]  |

### Return type

[**ListRcsAgents200Response**](ListRcsAgents200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Agents, newest first. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Your plan does not include the inbox, which RCS requires. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listrcsbrands"></a>
# **ListRcsBrands**
> ListRcsBrands200Response ListRcsBrands ()

List RCS brands

The team's RCS brands (vetted companies), to reuse one for another agent with `brandId`.

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
    public class ListRcsBrandsExample
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
            var apiInstance = new RCSApi(httpClient, config, httpClientHandler);

            try
            {
                // List RCS brands
                ListRcsBrands200Response result = apiInstance.ListRcsBrands();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RCSApi.ListRcsBrands: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListRcsBrandsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List RCS brands
    ApiResponse<ListRcsBrands200Response> response = apiInstance.ListRcsBrandsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RCSApi.ListRcsBrandsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListRcsBrands200Response**](ListRcsBrands200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Brands, newest first. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Your plan does not include the inbox, which RCS requires. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listrcstestdevices"></a>
# **ListRcsTestDevices**
> ListRcsTestDevices200Response ListRcsTestDevices (string agentId)

List RCS test phones

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
    public class ListRcsTestDevicesExample
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
            var apiInstance = new RCSApi(httpClient, config, httpClientHandler);
            var agentId = "agentId_example";  // string | 

            try
            {
                // List RCS test phones
                ListRcsTestDevices200Response result = apiInstance.ListRcsTestDevices(agentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RCSApi.ListRcsTestDevices: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListRcsTestDevicesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List RCS test phones
    ApiResponse<ListRcsTestDevices200Response> response = apiInstance.ListRcsTestDevicesWithHttpInfo(agentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RCSApi.ListRcsTestDevicesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **agentId** | **string** |  |  |

### Return type

[**ListRcsTestDevices200Response**](ListRcsTestDevices200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Invited test phones. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Your plan does not include the inbox, which RCS requires. |  -  |
| **404** | Agent not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removercstestdevice"></a>
# **RemoveRcsTestDevice**
> UpdateYoutubeDefaultPlaylist200Response RemoveRcsTestDevice (string agentId, Guid testDeviceId)

Remove an RCS test phone

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
    public class RemoveRcsTestDeviceExample
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
            var apiInstance = new RCSApi(httpClient, config, httpClientHandler);
            var agentId = "agentId_example";  // string | 
            var testDeviceId = "testDeviceId_example";  // Guid | 

            try
            {
                // Remove an RCS test phone
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.RemoveRcsTestDevice(agentId, testDeviceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RCSApi.RemoveRcsTestDevice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveRcsTestDeviceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove an RCS test phone
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.RemoveRcsTestDeviceWithHttpInfo(agentId, testDeviceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RCSApi.RemoveRcsTestDeviceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **agentId** | **string** |  |  |
| **testDeviceId** | **Guid** |  |  |

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
| **200** | Removed. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Your plan does not include the inbox, which RCS requires. |  -  |
| **404** | Agent or test phone not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="requestrcsagentlaunch"></a>
# **RequestRcsAgentLaunch**
> CreateRcsAgent201Response RequestRcsAgentLaunch (string agentId, RcsLaunchRequest rcsLaunchRequest)

Send the launch filing

Sends the launch details the carriers review (campaign, consent and a public test video). US agents send them once they are in `testing`; we review them before they reach the carriers. Agents in other markets send them while still in review (`requested`, `changes_requested` or `brand_vetting`), because we file everything with the carriers at once; this saves the details without changing the status. 

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
    public class RequestRcsAgentLaunchExample
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
            var apiInstance = new RCSApi(httpClient, config, httpClientHandler);
            var agentId = "agentId_example";  // string | 
            var rcsLaunchRequest = new RcsLaunchRequest(); // RcsLaunchRequest | 

            try
            {
                // Send the launch filing
                CreateRcsAgent201Response result = apiInstance.RequestRcsAgentLaunch(agentId, rcsLaunchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RCSApi.RequestRcsAgentLaunch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RequestRcsAgentLaunchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send the launch filing
    ApiResponse<CreateRcsAgent201Response> response = apiInstance.RequestRcsAgentLaunchWithHttpInfo(agentId, rcsLaunchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RCSApi.RequestRcsAgentLaunchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **agentId** | **string** |  |  |
| **rcsLaunchRequest** | [**RcsLaunchRequest**](RcsLaunchRequest.md) |  |  |

### Return type

[**CreateRcsAgent201Response**](CreateRcsAgent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The agent, now in launch_review. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Your plan does not include the inbox, which RCS requires. |  -  |
| **404** | Agent not found |  -  |
| **409** | The agent is not in testing |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sendrcsmessage"></a>
# **SendRcsMessage**
> SendRcsMessage200Response SendRcsMessage (SendRcsMessageRequest sendRcsMessageRequest, string? idempotencyKey = null)

Send an RCS message

Sends from one of your agents. Use `text` for a plain message or `content` for rich content (card, carousel, media, suggestion chips). Before launch an agent only reaches test phones that accepted the invite. With the agent's `smsFallbackFrom` set, phones without RCS get `fallbackText` (default: the message's readable text) as SMS.  Replies and status arrive as webhooks with `platform: \"rcs\"`: `message.received` (a tapped chip carries its postback in `metadata.postbackPayload`), `message.delivered`, `message.read` and `message.failed`. Send an `Idempotency-Key` header to make retries safe. 

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
    public class SendRcsMessageExample
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
            var apiInstance = new RCSApi(httpClient, config, httpClientHandler);
            var sendRcsMessageRequest = new SendRcsMessageRequest(); // SendRcsMessageRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. (optional) 

            try
            {
                // Send an RCS message
                SendRcsMessage200Response result = apiInstance.SendRcsMessage(sendRcsMessageRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RCSApi.SendRcsMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendRcsMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send an RCS message
    ApiResponse<SendRcsMessage200Response> response = apiInstance.SendRcsMessageWithHttpInfo(sendRcsMessageRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RCSApi.SendRcsMessageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sendRcsMessageRequest** | [**SendRcsMessageRequest**](SendRcsMessageRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. | [optional]  |

### Return type

[**SendRcsMessage200Response**](SendRcsMessage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Message accepted. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The plan does not include the inbox, the recipient is not an accepted test phone before launch, or usage billing is not enabled |  -  |
| **404** | Agent not found |  -  |
| **409** | The agent cannot send yet, the recipient opted out (replied STOP), or the Idempotency-Key is still in flight |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |
| **502** | Carrier-side send failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatercsagent"></a>
# **UpdateRcsAgent**
> CreateRcsAgent201Response UpdateRcsAgent (string agentId, UpdateRcsAgentRequest updateRcsAgentRequest)

Update an RCS agent

Edits the filing while the agent is `requested` or `changes_requested`; answering a change request puts it back in our review. The company can only change until it is filed. `smsFallbackFrom` stays editable in any status (null removes it). 

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
    public class UpdateRcsAgentExample
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
            var apiInstance = new RCSApi(httpClient, config, httpClientHandler);
            var agentId = "agentId_example";  // string | 
            var updateRcsAgentRequest = new UpdateRcsAgentRequest(); // UpdateRcsAgentRequest | 

            try
            {
                // Update an RCS agent
                CreateRcsAgent201Response result = apiInstance.UpdateRcsAgent(agentId, updateRcsAgentRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RCSApi.UpdateRcsAgent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateRcsAgentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update an RCS agent
    ApiResponse<CreateRcsAgent201Response> response = apiInstance.UpdateRcsAgentWithHttpInfo(agentId, updateRcsAgentRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RCSApi.UpdateRcsAgentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **agentId** | **string** |  |  |
| **updateRcsAgentRequest** | [**UpdateRcsAgentRequest**](UpdateRcsAgentRequest.md) |  |  |

### Return type

[**CreateRcsAgent201Response**](CreateRcsAgent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated agent. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Your plan does not include the inbox, which RCS requires. |  -  |
| **404** | Agent not found |  -  |
| **409** | The filing is locked because it is already with the carriers |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="uploadrcsasset"></a>
# **UploadRcsAsset**
> ListInboxReviews200ResponseDataInnerPhotosInner UploadRcsAsset (FileParameter file, string kind)

Upload an RCS logo or banner

Uploads an image and returns a public URL for `profile.logoUrl` or `profile.heroUrl`. The image is cropped and compressed to the carriers' exact rules (logo 224x224 under 50 KB, banner 1440x448 under 200 KB). 

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
    public class UploadRcsAssetExample
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
            var apiInstance = new RCSApi(httpClient, config, httpClientHandler);
            var file = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // FileParameter | PNG, JPEG or WebP.
            var kind = "logo";  // string | 

            try
            {
                // Upload an RCS logo or banner
                ListInboxReviews200ResponseDataInnerPhotosInner result = apiInstance.UploadRcsAsset(file, kind);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RCSApi.UploadRcsAsset: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadRcsAssetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload an RCS logo or banner
    ApiResponse<ListInboxReviews200ResponseDataInnerPhotosInner> response = apiInstance.UploadRcsAssetWithHttpInfo(file, kind);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RCSApi.UploadRcsAssetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **file** | **FileParameter****FileParameter** | PNG, JPEG or WebP. |  |
| **kind** | **string** |  |  |

### Return type

[**ListInboxReviews200ResponseDataInnerPhotosInner**](ListInboxReviews200ResponseDataInnerPhotosInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Hosted URL. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Your plan does not include the inbox, which RCS requires. |  -  |
| **422** | The image is unreadable, too small, or could not be compressed under the limit |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

