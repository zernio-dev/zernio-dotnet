# Zernio.Api.AccountSettingsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteInstagramIceBreakers**](AccountSettingsApi.md#deleteinstagramicebreakers) | **DELETE** /v1/accounts/{accountId}/instagram-ice-breakers | Delete IG ice breakers |
| [**DeleteMessengerGetStarted**](AccountSettingsApi.md#deletemessengergetstarted) | **DELETE** /v1/accounts/{accountId}/messenger-get-started | Delete FB Get Started button |
| [**DeleteMessengerGreeting**](AccountSettingsApi.md#deletemessengergreeting) | **DELETE** /v1/accounts/{accountId}/messenger-greeting | Delete FB greeting text |
| [**DeleteMessengerIceBreakers**](AccountSettingsApi.md#deletemessengericebreakers) | **DELETE** /v1/accounts/{accountId}/messenger-ice-breakers | Delete FB ice breakers |
| [**DeleteMessengerMenu**](AccountSettingsApi.md#deletemessengermenu) | **DELETE** /v1/accounts/{accountId}/messenger-menu | Delete persistent menu |
| [**DeleteTelegramCommands**](AccountSettingsApi.md#deletetelegramcommands) | **DELETE** /v1/accounts/{accountId}/telegram-commands | Delete TG bot commands |
| [**GetInstagramIceBreakers**](AccountSettingsApi.md#getinstagramicebreakers) | **GET** /v1/accounts/{accountId}/instagram-ice-breakers | Get IG ice breakers |
| [**GetMessengerGetStarted**](AccountSettingsApi.md#getmessengergetstarted) | **GET** /v1/accounts/{accountId}/messenger-get-started | Get FB Get Started button |
| [**GetMessengerGreeting**](AccountSettingsApi.md#getmessengergreeting) | **GET** /v1/accounts/{accountId}/messenger-greeting | Get FB greeting text |
| [**GetMessengerIceBreakers**](AccountSettingsApi.md#getmessengericebreakers) | **GET** /v1/accounts/{accountId}/messenger-ice-breakers | Get FB ice breakers |
| [**GetMessengerMenu**](AccountSettingsApi.md#getmessengermenu) | **GET** /v1/accounts/{accountId}/messenger-menu | Get persistent menu |
| [**GetTelegramCommands**](AccountSettingsApi.md#gettelegramcommands) | **GET** /v1/accounts/{accountId}/telegram-commands | Get TG bot commands |
| [**SetInstagramIceBreakers**](AccountSettingsApi.md#setinstagramicebreakers) | **PUT** /v1/accounts/{accountId}/instagram-ice-breakers | Set IG ice breakers |
| [**SetMessengerGetStarted**](AccountSettingsApi.md#setmessengergetstarted) | **PUT** /v1/accounts/{accountId}/messenger-get-started | Set FB Get Started button |
| [**SetMessengerGreeting**](AccountSettingsApi.md#setmessengergreeting) | **PUT** /v1/accounts/{accountId}/messenger-greeting | Set FB greeting text |
| [**SetMessengerIceBreakers**](AccountSettingsApi.md#setmessengericebreakers) | **PUT** /v1/accounts/{accountId}/messenger-ice-breakers | Set FB ice breakers |
| [**SetMessengerMenu**](AccountSettingsApi.md#setmessengermenu) | **PUT** /v1/accounts/{accountId}/messenger-menu | Set persistent menu |
| [**SetTelegramCommands**](AccountSettingsApi.md#settelegramcommands) | **PUT** /v1/accounts/{accountId}/telegram-commands | Set TG bot commands |

<a id="deleteinstagramicebreakers"></a>
# **DeleteInstagramIceBreakers**
> void DeleteInstagramIceBreakers (string accountId)

Delete IG ice breakers

Removes the ice breaker questions from an Instagram account's Messenger experience.

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
    public class DeleteInstagramIceBreakersExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Delete IG ice breakers
                apiInstance.DeleteInstagramIceBreakers(accountId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.DeleteInstagramIceBreakers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteInstagramIceBreakersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete IG ice breakers
    apiInstance.DeleteInstagramIceBreakersWithHttpInfo(accountId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.DeleteInstagramIceBreakersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

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
| **200** | Ice breakers deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletemessengergetstarted"></a>
# **DeleteMessengerGetStarted**
> UpdateYoutubeDefaultPlaylist200Response DeleteMessengerGetStarted (string accountId)

Delete FB Get Started button

Remove the Get Started button. Meta refuses while a persistent menu is set, so delete the menu first.

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
    public class DeleteMessengerGetStartedExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Delete FB Get Started button
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.DeleteMessengerGetStarted(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.DeleteMessengerGetStarted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteMessengerGetStartedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete FB Get Started button
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.DeleteMessengerGetStartedWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.DeleteMessengerGetStartedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

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
| **200** | Get Started button deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **409** | A persistent menu is still set. Delete it with DELETE /v1/accounts/{accountId}/messenger-menu first. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletemessengergreeting"></a>
# **DeleteMessengerGreeting**
> UpdateYoutubeDefaultPlaylist200Response DeleteMessengerGreeting (string accountId)

Delete FB greeting text

Remove the greeting text from every locale.

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
    public class DeleteMessengerGreetingExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Delete FB greeting text
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.DeleteMessengerGreeting(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.DeleteMessengerGreeting: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteMessengerGreetingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete FB greeting text
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.DeleteMessengerGreetingWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.DeleteMessengerGreetingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

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
| **200** | Greeting deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletemessengericebreakers"></a>
# **DeleteMessengerIceBreakers**
> UpdateYoutubeDefaultPlaylist200Response DeleteMessengerIceBreakers (string accountId)

Delete FB ice breakers

Remove the ice breakers from every locale.

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
    public class DeleteMessengerIceBreakersExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Delete FB ice breakers
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.DeleteMessengerIceBreakers(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.DeleteMessengerIceBreakers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteMessengerIceBreakersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete FB ice breakers
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.DeleteMessengerIceBreakersWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.DeleteMessengerIceBreakersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

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
| **200** | Ice breakers deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletemessengermenu"></a>
# **DeleteMessengerMenu**
> void DeleteMessengerMenu (string accountId)

Delete persistent menu

Removes the persistent menu from this Facebook Messenger or Instagram account.

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
    public class DeleteMessengerMenuExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Delete persistent menu
                apiInstance.DeleteMessengerMenu(accountId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.DeleteMessengerMenu: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteMessengerMenuWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete persistent menu
    apiInstance.DeleteMessengerMenuWithHttpInfo(accountId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.DeleteMessengerMenuWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

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
| **200** | Menu deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletetelegramcommands"></a>
# **DeleteTelegramCommands**
> void DeleteTelegramCommands (string accountId)

Delete TG bot commands

Clears all bot commands configured for a Telegram bot account.

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
    public class DeleteTelegramCommandsExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Delete TG bot commands
                apiInstance.DeleteTelegramCommands(accountId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.DeleteTelegramCommands: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTelegramCommandsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete TG bot commands
    apiInstance.DeleteTelegramCommandsWithHttpInfo(accountId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.DeleteTelegramCommandsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

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
| **200** | Commands deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getinstagramicebreakers"></a>
# **GetInstagramIceBreakers**
> GetMessengerMenu200Response GetInstagramIceBreakers (string accountId)

Get IG ice breakers

Get the ice breaker configuration for an Instagram account.

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
    public class GetInstagramIceBreakersExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get IG ice breakers
                GetMessengerMenu200Response result = apiInstance.GetInstagramIceBreakers(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.GetInstagramIceBreakers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInstagramIceBreakersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get IG ice breakers
    ApiResponse<GetMessengerMenu200Response> response = apiInstance.GetInstagramIceBreakersWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.GetInstagramIceBreakersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetMessengerMenu200Response**](GetMessengerMenu200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ice breaker configuration |  -  |
| **400** | Not an Instagram account |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getmessengergetstarted"></a>
# **GetMessengerGetStarted**
> GetMessengerGetStarted200Response GetMessengerGetStarted (string accountId)

Get FB Get Started button

Get the Get Started button payload for a Facebook Messenger account. `data` is null when the page has none.

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
    public class GetMessengerGetStartedExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get FB Get Started button
                GetMessengerGetStarted200Response result = apiInstance.GetMessengerGetStarted(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.GetMessengerGetStarted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetMessengerGetStartedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get FB Get Started button
    ApiResponse<GetMessengerGetStarted200Response> response = apiInstance.GetMessengerGetStartedWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.GetMessengerGetStartedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetMessengerGetStarted200Response**](GetMessengerGetStarted200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Get Started button configuration |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getmessengergreeting"></a>
# **GetMessengerGreeting**
> GetMessengerGreeting200Response GetMessengerGreeting (string accountId)

Get FB greeting text

Get the greeting text a Facebook page shows on its Messenger welcome screen, one entry per locale. `data` is empty when the page has none.

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
    public class GetMessengerGreetingExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get FB greeting text
                GetMessengerGreeting200Response result = apiInstance.GetMessengerGreeting(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.GetMessengerGreeting: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetMessengerGreetingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get FB greeting text
    ApiResponse<GetMessengerGreeting200Response> response = apiInstance.GetMessengerGreetingWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.GetMessengerGreetingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetMessengerGreeting200Response**](GetMessengerGreeting200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Greeting locales |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getmessengericebreakers"></a>
# **GetMessengerIceBreakers**
> GetMessengerIceBreakers200Response GetMessengerIceBreakers (string accountId)

Get FB ice breakers

Get the ice breakers (FAQ questions shown when a person opens a new Messenger thread) for a Facebook page, one entry per locale. Instagram ice breakers live at /v1/accounts/{accountId}/instagram-ice-breakers.

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
    public class GetMessengerIceBreakersExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get FB ice breakers
                GetMessengerIceBreakers200Response result = apiInstance.GetMessengerIceBreakers(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.GetMessengerIceBreakers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetMessengerIceBreakersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get FB ice breakers
    ApiResponse<GetMessengerIceBreakers200Response> response = apiInstance.GetMessengerIceBreakersWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.GetMessengerIceBreakersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetMessengerIceBreakers200Response**](GetMessengerIceBreakers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ice breakers per locale |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getmessengermenu"></a>
# **GetMessengerMenu**
> GetMessengerMenu200Response GetMessengerMenu (string accountId)

Get persistent menu

Get the persistent menu configuration for a Facebook Messenger or Instagram account. Instagram accounts connected through Facebook Login are read through their linked Page (Meta's `platform=instagram`), Instagram Login accounts through the Instagram API.

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
    public class GetMessengerMenuExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get persistent menu
                GetMessengerMenu200Response result = apiInstance.GetMessengerMenu(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.GetMessengerMenu: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetMessengerMenuWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get persistent menu
    ApiResponse<GetMessengerMenu200Response> response = apiInstance.GetMessengerMenuWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.GetMessengerMenuWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetMessengerMenu200Response**](GetMessengerMenu200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Persistent menu configuration |  -  |
| **400** | Not a Facebook or Instagram account |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettelegramcommands"></a>
# **GetTelegramCommands**
> GetTelegramCommands200Response GetTelegramCommands (string accountId)

Get TG bot commands

Get the bot commands configuration for a Telegram account.

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
    public class GetTelegramCommandsExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get TG bot commands
                GetTelegramCommands200Response result = apiInstance.GetTelegramCommands(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.GetTelegramCommands: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTelegramCommandsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get TG bot commands
    ApiResponse<GetTelegramCommands200Response> response = apiInstance.GetTelegramCommandsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.GetTelegramCommandsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetTelegramCommands200Response**](GetTelegramCommands200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Bot commands list |  -  |
| **400** | Not a Telegram account |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setinstagramicebreakers"></a>
# **SetInstagramIceBreakers**
> void SetInstagramIceBreakers (string accountId, SetInstagramIceBreakersRequest setInstagramIceBreakersRequest)

Set IG ice breakers

Set ice breakers for an Instagram account. Max 4 ice breakers, question max 80 chars.

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
    public class SetInstagramIceBreakersExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var setInstagramIceBreakersRequest = new SetInstagramIceBreakersRequest(); // SetInstagramIceBreakersRequest | 

            try
            {
                // Set IG ice breakers
                apiInstance.SetInstagramIceBreakers(accountId, setInstagramIceBreakersRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.SetInstagramIceBreakers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetInstagramIceBreakersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set IG ice breakers
    apiInstance.SetInstagramIceBreakersWithHttpInfo(accountId, setInstagramIceBreakersRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.SetInstagramIceBreakersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **setInstagramIceBreakersRequest** | [**SetInstagramIceBreakersRequest**](SetInstagramIceBreakersRequest.md) |  |  |

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
| **200** | Ice breakers set successfully |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setmessengergetstarted"></a>
# **SetMessengerGetStarted**
> UpdateYoutubeDefaultPlaylist200Response SetMessengerGetStarted (string accountId, SetMessengerGetStartedRequest setMessengerGetStartedRequest)

Set FB Get Started button

Set the Get Started button shown on a Facebook page's Messenger welcome screen. Meta requires it before a persistent menu can be set. Tapping it sends a postback with `payload`, which arrives as a `message.received` webhook carrying it in `metadata.postbackPayload`. Use `zernio:workflow:<workflowId>` to start a workflow on the tap; the workflow must be active on this account and profile.

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
    public class SetMessengerGetStartedExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var setMessengerGetStartedRequest = new SetMessengerGetStartedRequest(); // SetMessengerGetStartedRequest | 

            try
            {
                // Set FB Get Started button
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.SetMessengerGetStarted(accountId, setMessengerGetStartedRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.SetMessengerGetStarted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetMessengerGetStartedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set FB Get Started button
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.SetMessengerGetStartedWithHttpInfo(accountId, setMessengerGetStartedRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.SetMessengerGetStartedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **setMessengerGetStartedRequest** | [**SetMessengerGetStartedRequest**](SetMessengerGetStartedRequest.md) |  |  |

### Return type

[**UpdateYoutubeDefaultPlaylist200Response**](UpdateYoutubeDefaultPlaylist200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Get Started button set |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setmessengergreeting"></a>
# **SetMessengerGreeting**
> UpdateYoutubeDefaultPlaylist200Response SetMessengerGreeting (string accountId, SetMessengerGreetingRequest setMessengerGreetingRequest)

Set FB greeting text

Set the greeting text on a Facebook page's Messenger welcome screen (Meta's `greeting` Messenger Profile field). One entry must use locale `default`; add more for other locales. Meta personalises `{{user_first_name}}`, `{{user_last_name}}` and `{{user_full_name}}`. Replaces every locale already set.

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
    public class SetMessengerGreetingExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var setMessengerGreetingRequest = new SetMessengerGreetingRequest(); // SetMessengerGreetingRequest | 

            try
            {
                // Set FB greeting text
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.SetMessengerGreeting(accountId, setMessengerGreetingRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.SetMessengerGreeting: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetMessengerGreetingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set FB greeting text
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.SetMessengerGreetingWithHttpInfo(accountId, setMessengerGreetingRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.SetMessengerGreetingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **setMessengerGreetingRequest** | [**SetMessengerGreetingRequest**](SetMessengerGreetingRequest.md) |  |  |

### Return type

[**UpdateYoutubeDefaultPlaylist200Response**](UpdateYoutubeDefaultPlaylist200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Greeting set |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setmessengericebreakers"></a>
# **SetMessengerIceBreakers**
> UpdateYoutubeDefaultPlaylist200Response SetMessengerIceBreakers (string accountId, SetMessengerIceBreakersRequest setMessengerIceBreakersRequest)

Set FB ice breakers

Set up to 4 ice breakers per locale for a Facebook page (Meta's `ice_breakers` Messenger Profile field). One entry must use locale `default`. A tap sends a postback with the question's `payload`, which arrives as `message.received` with `metadata.postbackPayload`; use `zernio:workflow:<workflowId>` to start a workflow (it must be active on this account and profile). Replaces every locale already set.

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
    public class SetMessengerIceBreakersExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var setMessengerIceBreakersRequest = new SetMessengerIceBreakersRequest(); // SetMessengerIceBreakersRequest | 

            try
            {
                // Set FB ice breakers
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.SetMessengerIceBreakers(accountId, setMessengerIceBreakersRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.SetMessengerIceBreakers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetMessengerIceBreakersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set FB ice breakers
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.SetMessengerIceBreakersWithHttpInfo(accountId, setMessengerIceBreakersRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.SetMessengerIceBreakersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **setMessengerIceBreakersRequest** | [**SetMessengerIceBreakersRequest**](SetMessengerIceBreakersRequest.md) |  |  |

### Return type

[**UpdateYoutubeDefaultPlaylist200Response**](UpdateYoutubeDefaultPlaylist200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ice breakers set |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setmessengermenu"></a>
# **SetMessengerMenu**
> void SetMessengerMenu (string accountId, SetMessengerMenuRequest setMessengerMenuRequest)

Set persistent menu

Set the persistent menu for a Facebook Messenger or Instagram account. Max 3 top-level items, max 5 nested items. On Facebook, Meta only shows a persistent menu on a page that has a Get Started button, so set one first with PUT /v1/accounts/{accountId}/messenger-get-started. A postback button whose payload is `zernio:workflow:<workflowId>` starts that workflow when tapped; the workflow must be active on this account and profile.

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
    public class SetMessengerMenuExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var setMessengerMenuRequest = new SetMessengerMenuRequest(); // SetMessengerMenuRequest | 

            try
            {
                // Set persistent menu
                apiInstance.SetMessengerMenu(accountId, setMessengerMenuRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.SetMessengerMenu: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetMessengerMenuWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set persistent menu
    apiInstance.SetMessengerMenuWithHttpInfo(accountId, setMessengerMenuRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.SetMessengerMenuWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **setMessengerMenuRequest** | [**SetMessengerMenuRequest**](SetMessengerMenuRequest.md) |  |  |

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
| **200** | Menu set successfully |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **409** | The page has no Get Started button. Set one with PUT /v1/accounts/{accountId}/messenger-get-started and retry. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="settelegramcommands"></a>
# **SetTelegramCommands**
> void SetTelegramCommands (string accountId, SetTelegramCommandsRequest setTelegramCommandsRequest)

Set TG bot commands

Set bot commands for a Telegram account.

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
    public class SetTelegramCommandsExample
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
            var apiInstance = new AccountSettingsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var setTelegramCommandsRequest = new SetTelegramCommandsRequest(); // SetTelegramCommandsRequest | 

            try
            {
                // Set TG bot commands
                apiInstance.SetTelegramCommands(accountId, setTelegramCommandsRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccountSettingsApi.SetTelegramCommands: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetTelegramCommandsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set TG bot commands
    apiInstance.SetTelegramCommandsWithHttpInfo(accountId, setTelegramCommandsRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccountSettingsApi.SetTelegramCommandsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **setTelegramCommandsRequest** | [**SetTelegramCommandsRequest**](SetTelegramCommandsRequest.md) |  |  |

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
| **200** | Commands set successfully |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

