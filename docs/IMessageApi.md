# Zernio.Api.IMessageApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddImessageGroupParticipant**](IMessageApi.md#addimessagegroupparticipant) | **POST** /v1/imessage/groups/{conversationId}/participants | Add a participant to an iMessage group |
| [**CancelImessageSender**](IMessageApi.md#cancelimessagesender) | **DELETE** /v1/imessage/senders/{senderId} | Cancel an iMessage sender |
| [**CreateImessageGroup**](IMessageApi.md#createimessagegroup) | **POST** /v1/imessage/groups | Start an iMessage group chat |
| [**CreateImessageOptInLink**](IMessageApi.md#createimessageoptinlink) | **POST** /v1/imessage/senders/{senderId}/opt-in-links | Create a tracked iMessage opt-in link |
| [**GetImessageGroup**](IMessageApi.md#getimessagegroup) | **GET** /v1/imessage/groups/{conversationId} | Get an iMessage group |
| [**GetImessageSender**](IMessageApi.md#getimessagesender) | **GET** /v1/imessage/senders/{senderId} | Get iMessage sender status |
| [**ListImessageAudience**](IMessageApi.md#listimessageaudience) | **GET** /v1/imessage/audience | List iMessage audience |
| [**ListImessageAvailableNumbers**](IMessageApi.md#listimessageavailablenumbers) | **GET** /v1/imessage/senders/available-numbers | List instantly available iMessage numbers |
| [**ListImessageSenderOrders**](IMessageApi.md#listimessagesenderorders) | **GET** /v1/imessage/senders/order | List iMessage sender orders |
| [**ListImessageSenders**](IMessageApi.md#listimessagesenders) | **GET** /v1/imessage/senders | List iMessage senders |
| [**OrderImessageSender**](IMessageApi.md#orderimessagesender) | **POST** /v1/imessage/senders/order | Order a new iMessage sender |
| [**RegisterImessageSender**](IMessageApi.md#registerimessagesender) | **POST** /v1/imessage/senders | Register an iMessage sender |
| [**RemoveImessageGroupParticipant**](IMessageApi.md#removeimessagegroupparticipant) | **DELETE** /v1/imessage/groups/{conversationId}/participants | Remove a participant from an iMessage group |
| [**ReserveImessageAvailableNumber**](IMessageApi.md#reserveimessageavailablenumber) | **POST** /v1/imessage/senders/available-numbers/{numberId}/reserve | Reserve an available iMessage number |
| [**SetImessageSubscription**](IMessageApi.md#setimessagesubscription) | **POST** /v1/imessage/audience/subscription | Subscribe or opt out an iMessage contact |
| [**UpdateImessageGroup**](IMessageApi.md#updateimessagegroup) | **PATCH** /v1/imessage/groups/{conversationId} | Rename an iMessage group or change its photo |
| [**UpdateImessageSender**](IMessageApi.md#updateimessagesender) | **PATCH** /v1/imessage/senders/{senderId} | Update an iMessage sender |

<a id="addimessagegroupparticipant"></a>
# **AddImessageGroupParticipant**
> AddImessageGroupParticipant200Response AddImessageGroupParticipant (string conversationId, AddImessageGroupParticipantRequest addImessageGroupParticipantRequest)

Add a participant to an iMessage group

Applied asynchronously by the provider; the participant list on the next group webhook reflects it.

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
    public class AddImessageGroupParticipantExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | 
            var addImessageGroupParticipantRequest = new AddImessageGroupParticipantRequest(); // AddImessageGroupParticipantRequest | 

            try
            {
                // Add a participant to an iMessage group
                AddImessageGroupParticipant200Response result = apiInstance.AddImessageGroupParticipant(conversationId, addImessageGroupParticipantRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.AddImessageGroupParticipant: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddImessageGroupParticipantWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add a participant to an iMessage group
    ApiResponse<AddImessageGroupParticipant200Response> response = apiInstance.AddImessageGroupParticipantWithHttpInfo(conversationId, addImessageGroupParticipantRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.AddImessageGroupParticipantWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** |  |  |
| **addImessageGroupParticipantRequest** | [**AddImessageGroupParticipantRequest**](AddImessageGroupParticipantRequest.md) |  |  |

### Return type

[**AddImessageGroupParticipant200Response**](AddImessageGroupParticipant200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Change accepted |  -  |
| **400** | Bad request, or the conversation is not a group thread |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account or conversation not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="cancelimessagesender"></a>
# **CancelImessageSender**
> OrderImessageSender202Response CancelImessageSender (string senderId)

Cancel an iMessage sender

Cancels the sender at the provider and deactivates its messaging account. Billing stops with the current month (no proration or refunds, matching phone numbers). 

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
    public class CancelImessageSenderExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var senderId = "senderId_example";  // string | 

            try
            {
                // Cancel an iMessage sender
                OrderImessageSender202Response result = apiInstance.CancelImessageSender(senderId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.CancelImessageSender: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CancelImessageSenderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cancel an iMessage sender
    ApiResponse<OrderImessageSender202Response> response = apiInstance.CancelImessageSenderWithHttpInfo(senderId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.CancelImessageSenderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **senderId** | **string** |  |  |

### Return type

[**OrderImessageSender202Response**](OrderImessageSender202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sender canceled |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Sender not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createimessagegroup"></a>
# **CreateImessageGroup**
> CreateImessageGroup202Response CreateImessageGroup (CreateImessageGroupRequest createImessageGroupRequest)

Start an iMessage group chat

Creates a group chat from one of your senders and sends its first message. The provider processes it asynchronously: the response carries the request id, and the thread appears in the inbox (with its group conversation id) on the first webhook. Starting a group counts as messaging new contacts, so the sender needs the provider's init-conversations add-on and the same sending intervals apply; without it the request fails with 409 `recipient_must_message_first`. WhatsApp groups need a `name`. 

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
    public class CreateImessageGroupExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var createImessageGroupRequest = new CreateImessageGroupRequest(); // CreateImessageGroupRequest | 

            try
            {
                // Start an iMessage group chat
                CreateImessageGroup202Response result = apiInstance.CreateImessageGroup(createImessageGroupRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.CreateImessageGroup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateImessageGroupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Start an iMessage group chat
    ApiResponse<CreateImessageGroup202Response> response = apiInstance.CreateImessageGroupWithHttpInfo(createImessageGroupRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.CreateImessageGroupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createImessageGroupRequest** | [**CreateImessageGroupRequest**](CreateImessageGroupRequest.md) |  |  |

### Return type

[**CreateImessageGroup202Response**](CreateImessageGroup202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Group creation accepted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account not found |  -  |
| **409** | The sender cannot start conversations (code: recipient_must_message_first) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createimessageoptinlink"></a>
# **CreateImessageOptInLink**
> CreateImessageOptInLink200Response CreateImessageOptInLink (string senderId, CreateImessageOptInLinkRequest createImessageOptInLinkRequest)

Create a tracked iMessage opt-in link

Generates a per-campaign link that opens Messages on this sender with `body` prefilled. iMessage is send-first: a sender can only message a contact who has written to it (a send to anyone else fails with `recipient_must_message_first`), and the contact's tap-and-send is what opens that door.  Each link carries a unique code in place of the `[opt-in-code]` placeholder; when the contact sends it, the resulting `message.received` webhook (and the stored inbox message's `metadata`) has `optIn: true` and your `parameters` under `optInParameters`, so you can attribute the conversation to the campaign or lead that produced it.  For an untracked link, use the sender's `optInLink` instead. 

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
    public class CreateImessageOptInLinkExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var senderId = "senderId_example";  // string | 
            var createImessageOptInLinkRequest = new CreateImessageOptInLinkRequest(); // CreateImessageOptInLinkRequest | 

            try
            {
                // Create a tracked iMessage opt-in link
                CreateImessageOptInLink200Response result = apiInstance.CreateImessageOptInLink(senderId, createImessageOptInLinkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.CreateImessageOptInLink: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateImessageOptInLinkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a tracked iMessage opt-in link
    ApiResponse<CreateImessageOptInLink200Response> response = apiInstance.CreateImessageOptInLinkWithHttpInfo(senderId, createImessageOptInLinkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.CreateImessageOptInLinkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **senderId** | **string** |  |  |
| **createImessageOptInLinkRequest** | [**CreateImessageOptInLinkRequest**](CreateImessageOptInLinkRequest.md) |  |  |

### Return type

[**CreateImessageOptInLink200Response**](CreateImessageOptInLink200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Opt-in link created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Sender not found |  -  |
| **409** | The sender is not active yet |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getimessagegroup"></a>
# **GetImessageGroup**
> GetImessageGroup200Response GetImessageGroup (string conversationId, string accountId)

Get an iMessage group

The group's name, participants and channel as the provider currently sees them. The conversation must be a group thread of the given account.

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
    public class GetImessageGroupExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | The inbox conversation id (or the provider group id)
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get an iMessage group
                GetImessageGroup200Response result = apiInstance.GetImessageGroup(conversationId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.GetImessageGroup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetImessageGroupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an iMessage group
    ApiResponse<GetImessageGroup200Response> response = apiInstance.GetImessageGroupWithHttpInfo(conversationId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.GetImessageGroupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | The inbox conversation id (or the provider group id) |  |
| **accountId** | **string** |  |  |

### Return type

[**GetImessageGroup200Response**](GetImessageGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Group details |  -  |
| **400** | Bad request, or the conversation is not a group thread |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account or conversation not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getimessagesender"></a>
# **GetImessageSender**
> GetImessageSender200Response GetImessageSender (string senderId)

Get iMessage sender status

Lifecycle status of an ordered or registered sender (poll while an order activates), plus the provider's live platform health for it.

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
    public class GetImessageSenderExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var senderId = "senderId_example";  // string | 

            try
            {
                // Get iMessage sender status
                GetImessageSender200Response result = apiInstance.GetImessageSender(senderId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.GetImessageSender: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetImessageSenderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get iMessage sender status
    ApiResponse<GetImessageSender200Response> response = apiInstance.GetImessageSenderWithHttpInfo(senderId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.GetImessageSenderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **senderId** | **string** |  |  |

### Return type

[**GetImessageSender200Response**](GetImessageSender200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sender lifecycle |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Sender not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listimessageaudience"></a>
# **ListImessageAudience**
> ListImessageAudience200Response ListImessageAudience (string? accountId = null, string? status = null, string? search = null, int? limit = null, int? skip = null)

List iMessage audience

Contacts who have messaged your iMessage senders (1:1 threads), with subscription state and, for threads opened through a tracked opt-in link, the parameters that brought them in. Newest activity first.

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
    public class ListImessageAudienceExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string? | Limit to one sender account (optional) 
            var status = "subscribed";  // string? |  (optional) 
            var search = "search_example";  // string? | Matches the contact handle or name (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List iMessage audience
                ListImessageAudience200Response result = apiInstance.ListImessageAudience(accountId, status, search, limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.ListImessageAudience: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListImessageAudienceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List iMessage audience
    ApiResponse<ListImessageAudience200Response> response = apiInstance.ListImessageAudienceWithHttpInfo(accountId, status, search, limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.ListImessageAudienceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string?** | Limit to one sender account | [optional]  |
| **status** | **string?** |  | [optional]  |
| **search** | **string?** | Matches the contact handle or name | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**ListImessageAudience200Response**](ListImessageAudience200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Audience page |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listimessageavailablenumbers"></a>
# **ListImessageAvailableNumbers**
> ListImessageAvailableNumbers200Response ListImessageAvailableNumbers (string? region = null)

List instantly available iMessage numbers

Phone numbers the provider has already registered and can assign on the spot. Order one by passing its `id` as `availableNumberId` to POST /v1/imessage/senders/order: the sender activates immediately instead of after the usual provisioning wait. Reserve it first with POST /v1/imessage/senders/available-numbers/{numberId}/reserve while the buyer decides. The list is a snapshot; a number can be taken between listing and ordering. 

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
    public class ListImessageAvailableNumbersExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var region = "US";  // string? |  (optional) 

            try
            {
                // List instantly available iMessage numbers
                ListImessageAvailableNumbers200Response result = apiInstance.ListImessageAvailableNumbers(region);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.ListImessageAvailableNumbers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListImessageAvailableNumbersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List instantly available iMessage numbers
    ApiResponse<ListImessageAvailableNumbers200Response> response = apiInstance.ListImessageAvailableNumbersWithHttpInfo(region);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.ListImessageAvailableNumbersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **region** | **string?** |  | [optional]  |

### Return type

[**ListImessageAvailableNumbers200Response**](ListImessageAvailableNumbers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Available numbers |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **502** | The provider could not list numbers; ordering without availableNumberId still works |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listimessagesenderorders"></a>
# **ListImessageSenderOrders**
> ListImessageSenderOrders200Response ListImessageSenderOrders (bool? includeCanceled = null)

List iMessage sender orders

Every sender lifecycle doc your team owns (ordered or registered), across statuses. Canceled senders are omitted unless `includeCanceled=true`.

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
    public class ListImessageSenderOrdersExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var includeCanceled = false;  // bool? |  (optional)  (default to false)

            try
            {
                // List iMessage sender orders
                ListImessageSenderOrders200Response result = apiInstance.ListImessageSenderOrders(includeCanceled);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.ListImessageSenderOrders: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListImessageSenderOrdersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List iMessage sender orders
    ApiResponse<ListImessageSenderOrders200Response> response = apiInstance.ListImessageSenderOrdersWithHttpInfo(includeCanceled);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.ListImessageSenderOrdersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **includeCanceled** | **bool?** |  | [optional] [default to false] |

### Return type

[**ListImessageSenderOrders200Response**](ListImessageSenderOrders200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sender lifecycle docs, newest first |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listimessagesenders"></a>
# **ListImessageSenders**
> ListImessageSenders200Response ListImessageSenders ()

List iMessage senders

Lists the iMessage senders registered across your accessible profiles.

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
    public class ListImessageSendersExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);

            try
            {
                // List iMessage senders
                ListImessageSenders200Response result = apiInstance.ListImessageSenders();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.ListImessageSenders: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListImessageSendersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List iMessage senders
    ApiResponse<ListImessageSenders200Response> response = apiInstance.ListImessageSendersWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.ListImessageSendersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListImessageSenders200Response**](ListImessageSenders200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Registered iMessage senders |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="orderimessagesender"></a>
# **OrderImessageSender**
> OrderImessageSender202Response OrderImessageSender (OrderImessageSenderRequest orderImessageSenderRequest)

Order a new iMessage sender

Orders a NEW dedicated iMessage sender from the delivery provider (compare with POST /v1/imessage/senders, which registers a sender you already own). Activation is asynchronous (minutes to a few hours): the response is 202 with the lifecycle object; poll GET /v1/imessage/senders/{senderId} or subscribe to the account.connected webhook. Billing starts at activation (monthly per sender, no proration). Requires usage-based billing and a valid payment method. Pass purchaseIntentId to make retries idempotent — the provider-side order is never retried automatically. Ordered phone senders include SMS/RCS fallback with call forwarding and the ability to message contacts who have not written first (sending intervals still apply). 

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
    public class OrderImessageSenderExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var orderImessageSenderRequest = new OrderImessageSenderRequest(); // OrderImessageSenderRequest | 

            try
            {
                // Order a new iMessage sender
                OrderImessageSender202Response result = apiInstance.OrderImessageSender(orderImessageSenderRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.OrderImessageSender: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OrderImessageSenderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Order a new iMessage sender
    ApiResponse<OrderImessageSender202Response> response = apiInstance.OrderImessageSenderWithHttpInfo(orderImessageSenderRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.OrderImessageSenderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orderImessageSenderRequest** | [**OrderImessageSenderRequest**](OrderImessageSenderRequest.md) |  |  |

### Return type

[**OrderImessageSender202Response**](OrderImessageSender202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Order accepted; activation continues asynchronously |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **402** | A valid payment method is required (code: payment_method_required) |  -  |
| **403** | Sender limit reached (code: imessage_sender_limit) |  -  |
| **404** | Profile not found or access denied |  -  |
| **409** | This profile already has a live iMessage sender (code: imessage_sender_conflict), or billing setup is incomplete and support must finish it (code: billing_setup_incomplete) |  -  |
| **422** | Workspace is not on usage-based billing (code: usage_billing_required) |  -  |
| **502** | The provider rejected the order; nothing was charged |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="registerimessagesender"></a>
# **RegisterImessageSender**
> RegisterImessageSender200Response RegisterImessageSender (RegisterImessageSenderRequest registerImessageSenderRequest)

Register an iMessage sender

Registers a provider-provisioned iMessage sender (a phone number or an email handle) that YOU already own on a profile, creating an `imessage` account that sends and receives through the inbox conversation endpoints. To have Zernio order a new sender for you, use POST /v1/imessage/senders/order instead. Registration attaches the monthly sender fee (billed while active) and requires a payment method (402 without one). One sender per profile: re-registering the SAME handle refreshes it; a different handle returns 409 until the existing sender is canceled. 

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
    public class RegisterImessageSenderExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var registerImessageSenderRequest = new RegisterImessageSenderRequest(); // RegisterImessageSenderRequest | 

            try
            {
                // Register an iMessage sender
                RegisterImessageSender200Response result = apiInstance.RegisterImessageSender(registerImessageSenderRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.RegisterImessageSender: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RegisterImessageSenderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Register an iMessage sender
    ApiResponse<RegisterImessageSender200Response> response = apiInstance.RegisterImessageSenderWithHttpInfo(registerImessageSenderRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.RegisterImessageSenderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **registerImessageSenderRequest** | [**RegisterImessageSenderRequest**](RegisterImessageSenderRequest.md) |  |  |

### Return type

[**RegisterImessageSender200Response**](RegisterImessageSender200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sender registered |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **402** | A valid payment method is required (code: payment_method_required) |  -  |
| **404** | Profile not found or access denied |  -  |
| **409** | Sender already registered to another profile (code: imessage_sender_conflict), or billing setup is incomplete and support must finish it (code: billing_setup_incomplete) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removeimessagegroupparticipant"></a>
# **RemoveImessageGroupParticipant**
> AddImessageGroupParticipant200Response RemoveImessageGroupParticipant (string conversationId, string accountId, string contact)

Remove a participant from an iMessage group

Applied asynchronously by the provider.

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
    public class RemoveImessageGroupParticipantExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | 
            var accountId = "accountId_example";  // string | 
            var contact = "contact_example";  // string | E.164 phone or iMessage email

            try
            {
                // Remove a participant from an iMessage group
                AddImessageGroupParticipant200Response result = apiInstance.RemoveImessageGroupParticipant(conversationId, accountId, contact);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.RemoveImessageGroupParticipant: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveImessageGroupParticipantWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove a participant from an iMessage group
    ApiResponse<AddImessageGroupParticipant200Response> response = apiInstance.RemoveImessageGroupParticipantWithHttpInfo(conversationId, accountId, contact);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.RemoveImessageGroupParticipantWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** |  |  |
| **accountId** | **string** |  |  |
| **contact** | **string** | E.164 phone or iMessage email |  |

### Return type

[**AddImessageGroupParticipant200Response**](AddImessageGroupParticipant200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Change accepted |  -  |
| **400** | Bad request, or the conversation is not a group thread |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account or conversation not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="reserveimessageavailablenumber"></a>
# **ReserveImessageAvailableNumber**
> ReserveImessageAvailableNumber200Response ReserveImessageAvailableNumber (string numberId)

Reserve an available iMessage number

Holds the number for 3 minutes so nobody else can order it while the buyer decides. Place the order (POST /v1/imessage/senders/order with availableNumberId) before the hold expires. No request body.

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
    public class ReserveImessageAvailableNumberExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var numberId = "numberId_example";  // string | 

            try
            {
                // Reserve an available iMessage number
                ReserveImessageAvailableNumber200Response result = apiInstance.ReserveImessageAvailableNumber(numberId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.ReserveImessageAvailableNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReserveImessageAvailableNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reserve an available iMessage number
    ApiResponse<ReserveImessageAvailableNumber200Response> response = apiInstance.ReserveImessageAvailableNumberWithHttpInfo(numberId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.ReserveImessageAvailableNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **numberId** | **string** |  |  |

### Return type

[**ReserveImessageAvailableNumber200Response**](ReserveImessageAvailableNumber200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Number reserved |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **409** | The number could not be reserved (already taken) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setimessagesubscription"></a>
# **SetImessageSubscription**
> SetImessageSubscription200Response SetImessageSubscription (SetImessageSubscriptionRequest setImessageSubscriptionRequest)

Subscribe or opt out an iMessage contact

Opted-out contacts are refused at send time (409 recipient_opted_out) until re-subscribed. Their inbound messages still arrive. Scoped to your account: it does not change the contact's state with other businesses.

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
    public class SetImessageSubscriptionExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var setImessageSubscriptionRequest = new SetImessageSubscriptionRequest(); // SetImessageSubscriptionRequest | 

            try
            {
                // Subscribe or opt out an iMessage contact
                SetImessageSubscription200Response result = apiInstance.SetImessageSubscription(setImessageSubscriptionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.SetImessageSubscription: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetImessageSubscriptionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Subscribe or opt out an iMessage contact
    ApiResponse<SetImessageSubscription200Response> response = apiInstance.SetImessageSubscriptionWithHttpInfo(setImessageSubscriptionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.SetImessageSubscriptionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **setImessageSubscriptionRequest** | [**SetImessageSubscriptionRequest**](SetImessageSubscriptionRequest.md) |  |  |

### Return type

[**SetImessageSubscription200Response**](SetImessageSubscription200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account or conversation not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateimessagegroup"></a>
# **UpdateImessageGroup**
> UpdateImessageGroup200Response UpdateImessageGroup (string conversationId, UpdateImessageGroupRequest updateImessageGroupRequest)

Rename an iMessage group or change its photo

One change per call: either `name` or `photoUrl` (an empty `photoUrl` removes the photo). Applied asynchronously by the provider; a rename is mirrored on the inbox conversation right away.

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
    public class UpdateImessageGroupExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | 
            var updateImessageGroupRequest = new UpdateImessageGroupRequest(); // UpdateImessageGroupRequest | 

            try
            {
                // Rename an iMessage group or change its photo
                UpdateImessageGroup200Response result = apiInstance.UpdateImessageGroup(conversationId, updateImessageGroupRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.UpdateImessageGroup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateImessageGroupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Rename an iMessage group or change its photo
    ApiResponse<UpdateImessageGroup200Response> response = apiInstance.UpdateImessageGroupWithHttpInfo(conversationId, updateImessageGroupRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.UpdateImessageGroupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** |  |  |
| **updateImessageGroupRequest** | [**UpdateImessageGroupRequest**](UpdateImessageGroupRequest.md) |  |  |

### Return type

[**UpdateImessageGroup200Response**](UpdateImessageGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Change accepted |  -  |
| **400** | Bad request, or the conversation is not a group thread |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account or conversation not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateimessagesender"></a>
# **UpdateImessageSender**
> OrderImessageSender202Response UpdateImessageSender (string senderId, UpdateImessageSenderRequest updateImessageSenderRequest)

Update an iMessage sender

Display name (inbox and API responses) and the contact card (vCard) recipients see when they save the sender. The contact card is what a contactCard send shares.

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
    public class UpdateImessageSenderExample
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
            var apiInstance = new IMessageApi(httpClient, config, httpClientHandler);
            var senderId = "senderId_example";  // string | 
            var updateImessageSenderRequest = new UpdateImessageSenderRequest(); // UpdateImessageSenderRequest | 

            try
            {
                // Update an iMessage sender
                OrderImessageSender202Response result = apiInstance.UpdateImessageSender(senderId, updateImessageSenderRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IMessageApi.UpdateImessageSender: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateImessageSenderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update an iMessage sender
    ApiResponse<OrderImessageSender202Response> response = apiInstance.UpdateImessageSenderWithHttpInfo(senderId, updateImessageSenderRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IMessageApi.UpdateImessageSenderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **senderId** | **string** |  |  |
| **updateImessageSenderRequest** | [**UpdateImessageSenderRequest**](UpdateImessageSenderRequest.md) |  |  |

### Return type

[**OrderImessageSender202Response**](OrderImessageSender202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sender updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Sender not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

