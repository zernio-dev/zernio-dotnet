# Zernio.Api.ConnectedAppsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ListConnectedApps**](ConnectedAppsApi.md#listconnectedapps) | **GET** /v1/me/connected-apps | List connected apps |
| [**RevokeConnectedApp**](ConnectedAppsApi.md#revokeconnectedapp) | **DELETE** /v1/me/connected-apps/{clientId} | Revoke connected app |

<a id="listconnectedapps"></a>
# **ListConnectedApps**
> ListConnectedApps200Response ListConnectedApps ()

List connected apps

Returns the OAuth clients (AI assistants and MCP connectors) the authenticated user has authorized and that still hold a live token.  Requires a session or a full-scope API key. A profile-scoped API key or an OAuth access token is rejected with 403: an app must not be able to enumerate its sibling authorizations. 

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
    public class ListConnectedAppsExample
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
            var apiInstance = new ConnectedAppsApi(httpClient, config, httpClientHandler);

            try
            {
                // List connected apps
                ListConnectedApps200Response result = apiInstance.ListConnectedApps();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectedAppsApi.ListConnectedApps: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListConnectedAppsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List connected apps
    ApiResponse<ListConnectedApps200Response> response = apiInstance.ListConnectedAppsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectedAppsApi.ListConnectedAppsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListConnectedApps200Response**](ListConnectedApps200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connected apps |  -  |
| **401** | Unauthorized |  -  |
| **403** | The calling credential may not manage OAuth authorizations (profile-scoped API key or OAuth access token). Error code: insufficient_permissions. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="revokeconnectedapp"></a>
# **RevokeConnectedApp**
> RevokeConnectedApp200Response RevokeConnectedApp (string clientId)

Revoke connected app

Ends an app's access: invalidates the client's pending authorization codes and revokes every live token it holds for the authenticated user. Takes effect on the app's next request.  Idempotent while the authorization is still on record: revoking an app that was already revoked returns 200 with `revokedTokens: 0`. 

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
    public class RevokeConnectedAppExample
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
            var apiInstance = new ConnectedAppsApi(httpClient, config, httpClientHandler);
            var clientId = "clientId_example";  // string | OAuth client id, as returned by GET /v1/me/connected-apps.

            try
            {
                // Revoke connected app
                RevokeConnectedApp200Response result = apiInstance.RevokeConnectedApp(clientId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectedAppsApi.RevokeConnectedApp: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RevokeConnectedAppWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Revoke connected app
    ApiResponse<RevokeConnectedApp200Response> response = apiInstance.RevokeConnectedAppWithHttpInfo(clientId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectedAppsApi.RevokeConnectedAppWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **clientId** | **string** | OAuth client id, as returned by GET /v1/me/connected-apps. |  |

### Return type

[**RevokeConnectedApp200Response**](RevokeConnectedApp200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Revoked |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The calling credential may not manage OAuth authorizations (profile-scoped API key or OAuth access token). Error code: insufficient_permissions. |  -  |
| **404** | The authenticated user has never authorized this client. Error code: oauth_client_not_found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

