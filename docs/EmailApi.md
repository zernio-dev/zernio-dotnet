# Zernio.Api.EmailApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CancelScheduledEmail**](EmailApi.md#cancelscheduledemail) | **DELETE** /v1/email/messages/scheduled/{scheduleId} | Cancel a scheduled email |
| [**CreateEmailLabel**](EmailApi.md#createemaillabel) | **POST** /v1/email/labels | Create a label |
| [**DeleteEmailLabel**](EmailApi.md#deleteemaillabel) | **DELETE** /v1/email/labels/{labelId} | Delete a label |
| [**DownloadEmailAttachment**](EmailApi.md#downloademailattachment) | **GET** /v1/email/attachments/{attachmentId} | Download an attachment |
| [**GetEmailMessage**](EmailApi.md#getemailmessage) | **GET** /v1/email/messages/{messageId} | Get an email message |
| [**GetEmailThread**](EmailApi.md#getemailthread) | **GET** /v1/email/threads/{threadId} | Get an email thread with its messages |
| [**GetScheduledEmail**](EmailApi.md#getscheduledemail) | **GET** /v1/email/messages/scheduled/{scheduleId} | Get a scheduled email |
| [**ListEmailFolders**](EmailApi.md#listemailfolders) | **GET** /v1/email/folders | List mailbox folders |
| [**ListEmailLabels**](EmailApi.md#listemaillabels) | **GET** /v1/email/labels | List labels |
| [**ListEmailMessages**](EmailApi.md#listemailmessages) | **GET** /v1/email/messages | List email messages |
| [**ListEmailThreads**](EmailApi.md#listemailthreads) | **GET** /v1/email/threads | List email threads |
| [**ListScheduledEmails**](EmailApi.md#listscheduledemails) | **GET** /v1/email/messages/scheduled | List scheduled emails |
| [**ReplyEmailMessage**](EmailApi.md#replyemailmessage) | **POST** /v1/email/messages/{messageId}/reply | Reply to a message |
| [**SendEmailMessage**](EmailApi.md#sendemailmessage) | **POST** /v1/email/messages | Send an email |
| [**TrashEmailMessage**](EmailApi.md#trashemailmessage) | **DELETE** /v1/email/messages/{messageId} | Move a message to trash |
| [**UpdateEmailMessage**](EmailApi.md#updateemailmessage) | **PATCH** /v1/email/messages/{messageId} | Mark read or starred, label, or move a message |
| [**UpdateEmailThread**](EmailApi.md#updateemailthread) | **PATCH** /v1/email/threads/{threadId} | Update every message in a thread |

<a id="cancelscheduledemail"></a>
# **CancelScheduledEmail**
> SendEmailMessage202Response CancelScheduledEmail (string scheduleId, string accountId)

Cancel a scheduled email

Cancels a send still waiting for its time and returns it with `status: cancelled`. One that is sending, sent or failed answers 409.

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
    public class CancelScheduledEmailExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var scheduleId = "scheduleId_example";  // string | 
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.

            try
            {
                // Cancel a scheduled email
                SendEmailMessage202Response result = apiInstance.CancelScheduledEmail(scheduleId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.CancelScheduledEmail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CancelScheduledEmailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cancel a scheduled email
    ApiResponse<SendEmailMessage202Response> response = apiInstance.CancelScheduledEmailWithHttpInfo(scheduleId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.CancelScheduledEmailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **scheduleId** | **string** |  |  |
| **accountId** | **string** | The connected Google or Microsoft account. |  |

### Return type

[**SendEmailMessage202Response**](SendEmailMessage202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The cancelled email |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **409** | The send already left, failed or was cancelled; the message names its status. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createemaillabel"></a>
# **CreateEmailLabel**
> CreateEmailLabel200Response CreateEmailLabel (CreateEmailLabelRequest createEmailLabelRequest)

Create a label

Creates a Gmail label or an Outlook category. Safe to repeat: when the name already exists (case-insensitive) the existing label comes back with 200.

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
    public class CreateEmailLabelExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var createEmailLabelRequest = new CreateEmailLabelRequest(); // CreateEmailLabelRequest | 

            try
            {
                // Create a label
                CreateEmailLabel200Response result = apiInstance.CreateEmailLabel(createEmailLabelRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.CreateEmailLabel: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateEmailLabelWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a label
    ApiResponse<CreateEmailLabel200Response> response = apiInstance.CreateEmailLabelWithHttpInfo(createEmailLabelRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.CreateEmailLabelWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createEmailLabelRequest** | [**CreateEmailLabelRequest**](CreateEmailLabelRequest.md) |  |  |

### Return type

[**CreateEmailLabel200Response**](CreateEmailLabel200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A label with this name already existed |  -  |
| **201** | The label was created |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteemaillabel"></a>
# **DeleteEmailLabel**
> DeleteEmailLabel200Response DeleteEmailLabel (string labelId, string accountId)

Delete a label

Deletes a Gmail user label or an Outlook category, by id or name (URL-encode a slash). Gmail removes the label from every message. Outlook keeps a deleted category on messages that already carry it; 412 when the organization blocks the category list.

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
    public class DeleteEmailLabelExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var labelId = "labelId_example";  // string | 
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.

            try
            {
                // Delete a label
                DeleteEmailLabel200Response result = apiInstance.DeleteEmailLabel(labelId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.DeleteEmailLabel: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteEmailLabelWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a label
    ApiResponse<DeleteEmailLabel200Response> response = apiInstance.DeleteEmailLabelWithHttpInfo(labelId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.DeleteEmailLabelWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **labelId** | **string** |  |  |
| **accountId** | **string** | The connected Google or Microsoft account. |  |

### Return type

[**DeleteEmailLabel200Response**](DeleteEmailLabel200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The label was deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="downloademailattachment"></a>
# **DownloadEmailAttachment**
> FileParameter DownloadEmailAttachment (string attachmentId, string accountId, string messageId)

Download an attachment

Streams the attachment bytes with its `Content-Type` and a `Content-Disposition` carrying the filename.

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
    public class DownloadEmailAttachmentExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var attachmentId = "attachmentId_example";  // string | 
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.
            var messageId = "messageId_example";  // string | 

            try
            {
                // Download an attachment
                FileParameter result = apiInstance.DownloadEmailAttachment(attachmentId, accountId, messageId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.DownloadEmailAttachment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DownloadEmailAttachmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Download an attachment
    ApiResponse<FileParameter> response = apiInstance.DownloadEmailAttachmentWithHttpInfo(attachmentId, accountId, messageId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.DownloadEmailAttachmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **attachmentId** | **string** |  |  |
| **accountId** | **string** | The connected Google or Microsoft account. |  |
| **messageId** | **string** |  |  |

### Return type

[**FileParameter**](FileParameter.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The attachment bytes |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getemailmessage"></a>
# **GetEmailMessage**
> SendEmailMessage201Response GetEmailMessage (string messageId, string accountId, bool? includeHeaders = null, bool? raw = null)

Get an email message

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
    public class GetEmailMessageExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var messageId = "messageId_example";  // string | 
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.
            var includeHeaders = false;  // bool? | Include the raw internet headers under `headers`. (optional)  (default to false)
            var raw = false;  // bool? | Include the MIME source under `raw`. (optional)  (default to false)

            try
            {
                // Get an email message
                SendEmailMessage201Response result = apiInstance.GetEmailMessage(messageId, accountId, includeHeaders, raw);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.GetEmailMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEmailMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an email message
    ApiResponse<SendEmailMessage201Response> response = apiInstance.GetEmailMessageWithHttpInfo(messageId, accountId, includeHeaders, raw);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.GetEmailMessageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **messageId** | **string** |  |  |
| **accountId** | **string** | The connected Google or Microsoft account. |  |
| **includeHeaders** | **bool?** | Include the raw internet headers under &#x60;headers&#x60;. | [optional] [default to false] |
| **raw** | **bool?** | Include the MIME source under &#x60;raw&#x60;. | [optional] [default to false] |

### Return type

[**SendEmailMessage201Response**](SendEmailMessage201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The message with its bodies |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getemailthread"></a>
# **GetEmailThread**
> GetEmailThread200Response GetEmailThread (string threadId, string accountId)

Get an email thread with its messages

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
    public class GetEmailThreadExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var threadId = "threadId_example";  // string | 
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.

            try
            {
                // Get an email thread with its messages
                GetEmailThread200Response result = apiInstance.GetEmailThread(threadId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.GetEmailThread: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEmailThreadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an email thread with its messages
    ApiResponse<GetEmailThread200Response> response = apiInstance.GetEmailThreadWithHttpInfo(threadId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.GetEmailThreadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **threadId** | **string** |  |  |
| **accountId** | **string** | The connected Google or Microsoft account. |  |

### Return type

[**GetEmailThread200Response**](GetEmailThread200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The thread and every message in it, oldest first |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getscheduledemail"></a>
# **GetScheduledEmail**
> SendEmailMessage202Response GetScheduledEmail (string scheduleId, string accountId)

Get a scheduled email

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
    public class GetScheduledEmailExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var scheduleId = "scheduleId_example";  // string | 
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.

            try
            {
                // Get a scheduled email
                SendEmailMessage202Response result = apiInstance.GetScheduledEmail(scheduleId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.GetScheduledEmail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetScheduledEmailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a scheduled email
    ApiResponse<SendEmailMessage202Response> response = apiInstance.GetScheduledEmailWithHttpInfo(scheduleId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.GetScheduledEmailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **scheduleId** | **string** |  |  |
| **accountId** | **string** | The connected Google or Microsoft account. |  |

### Return type

[**SendEmailMessage202Response**](SendEmailMessage202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The scheduled email |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listemailfolders"></a>
# **ListEmailFolders**
> ListEmailFolders200Response ListEmailFolders (string accountId)

List mailbox folders

On Google, folders are Gmail labels (system labels carry `wellKnown`; `unreadCount` and `totalCount` are present only where Gmail reports them). There is no archive folder on Google; archived mail is listed with `folder=archive`.

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
    public class ListEmailFoldersExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.

            try
            {
                // List mailbox folders
                ListEmailFolders200Response result = apiInstance.ListEmailFolders(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.ListEmailFolders: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListEmailFoldersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List mailbox folders
    ApiResponse<ListEmailFolders200Response> response = apiInstance.ListEmailFoldersWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.ListEmailFoldersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected Google or Microsoft account. |  |

### Return type

[**ListEmailFolders200Response**](ListEmailFolders200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Folders, with &#x60;wellKnown&#x60; set on the provider&#39;s system folders |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listemaillabels"></a>
# **ListEmailLabels**
> ListEmailLabels200Response ListEmailLabels (string accountId)

List labels

Gmail labels, system and user, or the Outlook category list. If an organization blocks reading the Outlook list, it comes back empty and categories still apply to messages by name.

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
    public class ListEmailLabelsExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.

            try
            {
                // List labels
                ListEmailLabels200Response result = apiInstance.ListEmailLabels(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.ListEmailLabels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListEmailLabelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List labels
    ApiResponse<ListEmailLabels200Response> response = apiInstance.ListEmailLabelsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.ListEmailLabelsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected Google or Microsoft account. |  |

### Return type

[**ListEmailLabels200Response**](ListEmailLabels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The mailbox&#39;s labels |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listemailmessages"></a>
# **ListEmailMessages**
> ListEmailMessages200Response ListEmailMessages (string accountId, string? folder = null, bool? unread = null, bool? starred = null, bool? hasAttachment = null, string? subject = null, string? from = null, string? to = null, string? cc = null, string? bcc = null, string? anyEmail = null, DateTime? after = null, DateTime? before = null, string? searchQueryNative = null, string? sortOrder = null, string? cursor = null, int? limit = null)

List email messages

Same filters and envelope as `GET /v1/email/threads`, one row per message. Bodies are omitted; fetch a message to read `text` and `html`.  ### On Google  - List rows also omit `attachments` (Gmail's metadata pages carry headers only); `hasAttachment=true` still filters server-side. - `sortOrder=asc` reverses the fetched page. - `archive` means mail without the inbox, trash or spam labels. 

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
    public class ListEmailMessagesExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.
            var folder = "folder_example";  // string? |  (optional) 
            var unread = true;  // bool? |  (optional) 
            var starred = true;  // bool? |  (optional) 
            var hasAttachment = true;  // bool? |  (optional) 
            var subject = "subject_example";  // string? |  (optional) 
            var from = "from_example";  // string? |  (optional) 
            var to = "to_example";  // string? |  (optional) 
            var cc = "cc_example";  // string? |  (optional) 
            var bcc = "bcc_example";  // string? |  (optional) 
            var anyEmail = "anyEmail_example";  // string? |  (optional) 
            var after = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var before = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var searchQueryNative = "searchQueryNative_example";  // string? |  (optional) 
            var sortOrder = "asc";  // string? |  (optional)  (default to desc)
            var cursor = "cursor_example";  // string? |  (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)

            try
            {
                // List email messages
                ListEmailMessages200Response result = apiInstance.ListEmailMessages(accountId, folder, unread, starred, hasAttachment, subject, from, to, cc, bcc, anyEmail, after, before, searchQueryNative, sortOrder, cursor, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.ListEmailMessages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListEmailMessagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List email messages
    ApiResponse<ListEmailMessages200Response> response = apiInstance.ListEmailMessagesWithHttpInfo(accountId, folder, unread, starred, hasAttachment, subject, from, to, cc, bcc, anyEmail, after, before, searchQueryNative, sortOrder, cursor, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.ListEmailMessagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected Google or Microsoft account. |  |
| **folder** | **string?** |  | [optional]  |
| **unread** | **bool?** |  | [optional]  |
| **starred** | **bool?** |  | [optional]  |
| **hasAttachment** | **bool?** |  | [optional]  |
| **subject** | **string?** |  | [optional]  |
| **from** | **string?** |  | [optional]  |
| **to** | **string?** |  | [optional]  |
| **cc** | **string?** |  | [optional]  |
| **bcc** | **string?** |  | [optional]  |
| **anyEmail** | **string?** |  | [optional]  |
| **after** | **DateTime?** |  | [optional]  |
| **before** | **DateTime?** |  | [optional]  |
| **searchQueryNative** | **string?** |  | [optional]  |
| **sortOrder** | **string?** |  | [optional] [default to desc] |
| **cursor** | **string?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |

### Return type

[**ListEmailMessages200Response**](ListEmailMessages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Messages |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted. Behavior per platform:  - **Reddit:** rate-limits per connected Reddit user (1000 requests per 10-minute window), shared by every operation on that account. Retry after the window resets; repeated calls while exhausted do not succeed and keep the budget spent. - **Google Ads:** writes and reports run on one developer token shared by every Google Ads account on Zernio. It holds Standard access (no daily operations cap), so this only happens when Google throttles the token or your ad account. - **Google Ads envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60; (&#x60;ACCOUNT&#x60; when it is your own ad account&#39;s quota), &#x60;details.resetsAt&#x60; (ISO instant when Google accepts requests again) and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **YouTube Analytics:** reads (channel-insights, demographics, daily-views, video-retention) use the \&quot;Queries per day\&quot; quota of the Google Cloud project the account is connected through, shared with other Zernio customers, so a 429 is not your own volume. Resets at midnight Pacific Time. - **YouTube Analytics envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaExhausted: true&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60;, &#x60;details.resetsAt&#x60; and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **Meta ads:** every Meta throttle (codes 4, 17, 32, 613 and business-use-case codes 80000-80014) returns 429 &#x60;rate_limited&#x60;, even when Meta answers HTTP 400. &#x60;Retry-After&#x60; comes from Meta&#39;s &#x60;x-business-use-case-usage&#x60; estimate when sent, else Meta&#39;s 60-second minimum (30 seconds for the one-write-per-30-seconds limit on one object). - **Pinterest ads:** limits per user and app, per category (ads_read, ads_write, ads_analytics). &#x60;Retry-After&#x60; comes from Pinterest&#39;s &#x60;x-ratelimit-reset&#x60; when sent, otherwise 60 seconds. - **TikTok ads:** limits per app and per endpoint (per second, minute and day), answering overage with code 40100 or code 40002 &#x60;OVER_QPS_LIMIT&#x60;. Both return 429 &#x60;rate_limited&#x60; with &#x60;platform: tiktok&#x60; and &#x60;Retry-After: 10&#x60;. Space out bulk reads (e.g. one ad at a time per advertiser) instead of retrying at once.  **TikTok Smart+ review read** (&#x60;GET /v1/ads/{adId}/tiktok-smart-plus-review&#x60;) has its own stricter TikTok quota. After an overage, Zernio answers 429 for that advertiser and connection without calling TikTok for about 60 seconds, then 120, up to 240 while TikTok keeps refusing, each with up to 10% random jitter.  A successful call holds nothing back; the next overage pauses about 60 seconds again. &#x60;Retry-After&#x60; is the time left. The advertiser-wide read (&#x60;GET /v1/ads/tiktok-smart-plus-reviews&#x60;) answers 200 with &#x60;retryAfterSeconds&#x60; and &#x60;refreshState&#x60; instead. Keep one request in flight per advertiser there.  |  * Retry-After - Seconds until card payments are tried again. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listemailthreads"></a>
# **ListEmailThreads**
> ListEmailThreads200Response ListEmailThreads (string accountId, string? folder = null, bool? unread = null, bool? starred = null, bool? hasAttachment = null, string? subject = null, string? from = null, string? to = null, string? cc = null, string? bcc = null, string? anyEmail = null, DateTime? after = null, DateTime? before = null, string? searchQueryNative = null, string? sortOrder = null, string? cursor = null, int? limit = null)

List email threads

Threads of a connected Google or Microsoft mailbox, newest first. Every filter that the provider cannot apply server-side is applied to the fetched page instead and named in `meta.filteredClientSide`, so a filtered page can hold fewer than `limit` items while `pagination.hasMore` stays true.  On Google, folders are Gmail labels: `folder` takes a well-known name or a label id, `archive` means mail carrying none of the inbox, trash or spam labels, and `sortOrder=asc` reverses the fetched page (Gmail lists newest first only).  The account must have been connected with `scopes=email` (412 `account_scope_missing` otherwise). 

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
    public class ListEmailThreadsExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.
            var folder = "folder_example";  // string? | Well-known folder (`inbox`, `sent`, `drafts`, `trash`, `spam`, `archive`) or a provider folder id from `GET /v1/email/folders`. Default inbox. (optional) 
            var unread = true;  // bool? |  (optional) 
            var starred = true;  // bool? |  (optional) 
            var hasAttachment = true;  // bool? |  (optional) 
            var subject = "subject_example";  // string? | Substring match on the subject. (optional) 
            var from = "from_example";  // string? | Sender address. (optional) 
            var to = "to_example";  // string? | A recipient address. (optional) 
            var cc = "cc_example";  // string? |  (optional) 
            var bcc = "bcc_example";  // string? | Applied client-side on Microsoft. (optional) 
            var anyEmail = "anyEmail_example";  // string? | Matches from, to, cc or bcc. Applied client-side on Microsoft. (optional) 
            var after = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var before = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var searchQueryNative = "searchQueryNative_example";  // string? | The provider's own search syntax (Gmail search operators, Microsoft KQL). On Microsoft it cannot be combined with other filters or server-side ordering; those are applied to the page. (optional) 
            var sortOrder = "asc";  // string? |  (optional)  (default to desc)
            var cursor = "cursor_example";  // string? |  (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)

            try
            {
                // List email threads
                ListEmailThreads200Response result = apiInstance.ListEmailThreads(accountId, folder, unread, starred, hasAttachment, subject, from, to, cc, bcc, anyEmail, after, before, searchQueryNative, sortOrder, cursor, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.ListEmailThreads: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListEmailThreadsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List email threads
    ApiResponse<ListEmailThreads200Response> response = apiInstance.ListEmailThreadsWithHttpInfo(accountId, folder, unread, starred, hasAttachment, subject, from, to, cc, bcc, anyEmail, after, before, searchQueryNative, sortOrder, cursor, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.ListEmailThreadsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected Google or Microsoft account. |  |
| **folder** | **string?** | Well-known folder (&#x60;inbox&#x60;, &#x60;sent&#x60;, &#x60;drafts&#x60;, &#x60;trash&#x60;, &#x60;spam&#x60;, &#x60;archive&#x60;) or a provider folder id from &#x60;GET /v1/email/folders&#x60;. Default inbox. | [optional]  |
| **unread** | **bool?** |  | [optional]  |
| **starred** | **bool?** |  | [optional]  |
| **hasAttachment** | **bool?** |  | [optional]  |
| **subject** | **string?** | Substring match on the subject. | [optional]  |
| **from** | **string?** | Sender address. | [optional]  |
| **to** | **string?** | A recipient address. | [optional]  |
| **cc** | **string?** |  | [optional]  |
| **bcc** | **string?** | Applied client-side on Microsoft. | [optional]  |
| **anyEmail** | **string?** | Matches from, to, cc or bcc. Applied client-side on Microsoft. | [optional]  |
| **after** | **DateTime?** |  | [optional]  |
| **before** | **DateTime?** |  | [optional]  |
| **searchQueryNative** | **string?** | The provider&#39;s own search syntax (Gmail search operators, Microsoft KQL). On Microsoft it cannot be combined with other filters or server-side ordering; those are applied to the page. | [optional]  |
| **sortOrder** | **string?** |  | [optional] [default to desc] |
| **cursor** | **string?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |

### Return type

[**ListEmailThreads200Response**](ListEmailThreads200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Threads |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted. Behavior per platform:  - **Reddit:** rate-limits per connected Reddit user (1000 requests per 10-minute window), shared by every operation on that account. Retry after the window resets; repeated calls while exhausted do not succeed and keep the budget spent. - **Google Ads:** writes and reports run on one developer token shared by every Google Ads account on Zernio. It holds Standard access (no daily operations cap), so this only happens when Google throttles the token or your ad account. - **Google Ads envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60; (&#x60;ACCOUNT&#x60; when it is your own ad account&#39;s quota), &#x60;details.resetsAt&#x60; (ISO instant when Google accepts requests again) and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **YouTube Analytics:** reads (channel-insights, demographics, daily-views, video-retention) use the \&quot;Queries per day\&quot; quota of the Google Cloud project the account is connected through, shared with other Zernio customers, so a 429 is not your own volume. Resets at midnight Pacific Time. - **YouTube Analytics envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaExhausted: true&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60;, &#x60;details.resetsAt&#x60; and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **Meta ads:** every Meta throttle (codes 4, 17, 32, 613 and business-use-case codes 80000-80014) returns 429 &#x60;rate_limited&#x60;, even when Meta answers HTTP 400. &#x60;Retry-After&#x60; comes from Meta&#39;s &#x60;x-business-use-case-usage&#x60; estimate when sent, else Meta&#39;s 60-second minimum (30 seconds for the one-write-per-30-seconds limit on one object). - **Pinterest ads:** limits per user and app, per category (ads_read, ads_write, ads_analytics). &#x60;Retry-After&#x60; comes from Pinterest&#39;s &#x60;x-ratelimit-reset&#x60; when sent, otherwise 60 seconds. - **TikTok ads:** limits per app and per endpoint (per second, minute and day), answering overage with code 40100 or code 40002 &#x60;OVER_QPS_LIMIT&#x60;. Both return 429 &#x60;rate_limited&#x60; with &#x60;platform: tiktok&#x60; and &#x60;Retry-After: 10&#x60;. Space out bulk reads (e.g. one ad at a time per advertiser) instead of retrying at once.  **TikTok Smart+ review read** (&#x60;GET /v1/ads/{adId}/tiktok-smart-plus-review&#x60;) has its own stricter TikTok quota. After an overage, Zernio answers 429 for that advertiser and connection without calling TikTok for about 60 seconds, then 120, up to 240 while TikTok keeps refusing, each with up to 10% random jitter.  A successful call holds nothing back; the next overage pauses about 60 seconds again. &#x60;Retry-After&#x60; is the time left. The advertiser-wide read (&#x60;GET /v1/ads/tiktok-smart-plus-reviews&#x60;) answers 200 with &#x60;retryAfterSeconds&#x60; and &#x60;refreshState&#x60; instead. Keep one request in flight per advertiser there.  |  * Retry-After - Seconds until card payments are tried again. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listscheduledemails"></a>
# **ListScheduledEmails**
> ListScheduledEmails200Response ListScheduledEmails (string accountId, string? status = null, string? cursor = null, int? limit = null)

List scheduled emails

Sends made with `scheduledFor` on this mailbox, in send order. Sent, failed and cancelled ones stay listed; filter with `status`.

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
    public class ListScheduledEmailsExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.
            var status = "scheduled";  // string? |  (optional) 
            var cursor = "cursor_example";  // string? | `pagination.nextCursor` of the previous page. (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)

            try
            {
                // List scheduled emails
                ListScheduledEmails200Response result = apiInstance.ListScheduledEmails(accountId, status, cursor, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.ListScheduledEmails: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListScheduledEmailsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List scheduled emails
    ApiResponse<ListScheduledEmails200Response> response = apiInstance.ListScheduledEmailsWithHttpInfo(accountId, status, cursor, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.ListScheduledEmailsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected Google or Microsoft account. |  |
| **status** | **string?** |  | [optional]  |
| **cursor** | **string?** | &#x60;pagination.nextCursor&#x60; of the previous page. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |

### Return type

[**ListScheduledEmails200Response**](ListScheduledEmails200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Scheduled emails |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="replyemailmessage"></a>
# **ReplyEmailMessage**
> SendEmailMessage201Response ReplyEmailMessage (string messageId, ReplyEmailMessageRequest replyEmailMessageRequest)

Reply to a message

Replies inside the provider's thread: the provider builds the quoted original and threading headers, your `html` or `text` goes above the quote. `to`, `cc`, `bcc`, `replyTo`, `subject`, `headers` and `attachments` are honoured.  `scheduledFor` schedules the reply (202) and `trackOpens`, `trackLinks` and `trackReplies` track it, as on send; `holdAsDraft` holds it as a reply draft in the thread until then. Same protection, caps and headers as sending. 

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
    public class ReplyEmailMessageExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var messageId = "messageId_example";  // string | 
            var replyEmailMessageRequest = new ReplyEmailMessageRequest(); // ReplyEmailMessageRequest | 

            try
            {
                // Reply to a message
                SendEmailMessage201Response result = apiInstance.ReplyEmailMessage(messageId, replyEmailMessageRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.ReplyEmailMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReplyEmailMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reply to a message
    ApiResponse<SendEmailMessage201Response> response = apiInstance.ReplyEmailMessageWithHttpInfo(messageId, replyEmailMessageRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.ReplyEmailMessageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **messageId** | **string** |  |  |
| **replyEmailMessageRequest** | [**ReplyEmailMessageRequest**](ReplyEmailMessageRequest.md) |  |  |

### Return type

[**SendEmailMessage201Response**](SendEmailMessage201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The sent reply |  -  |
| **202** | Scheduled: the send leaves at &#x60;scheduledFor&#x60; |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file, even the 1st one, because X API calls are passed through per call. Prepaid-balance accounts never get it: they pay X calls from the balance. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |
| **429** | The send was refused before reaching the provider.  - &#x60;email_send_cap_reached&#x60;: today&#39;s cap for the mailbox is spent. &#x60;details.cap&#x60; names the limit and &#x60;resetsAt&#x60;; &#x60;retryAfterSeconds&#x60; counts to midnight UTC. - &#x60;rate_limited&#x60;: the mailbox is in a sending cooldown, either from a same-body burst to more than 50 recipients in an hour (&#x60;details.cap.kind: recipient_burst&#x60;) or an earlier trigger. &#x60;retryAfterSeconds&#x60; says when it lifts, and &#x60;account.rate_limited&#x60; fired when it started.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sendemailmessage"></a>
# **SendEmailMessage**
> SendEmailMessage201Response SendEmailMessage (SendEmailRequest sendEmailRequest)

Send an email

Sends from the connected mailbox and returns the stored sent copy.  The message is mirrored into the inbox (`message.sent` fires once) and counted against the mailbox's daily cap. The cap is reported in the `X-Zernio-Send-Limit`, `X-Zernio-Send-Remaining` and `X-Zernio-Send-Reset` response headers.  ### Sending limits  These mailboxes are for one-to-one mail, not bulk sends. Protection on every mailbox:  - Daily cap: Microsoft 1,000; Google Workspace 500; Gmail consumer 200. Reaching it answers 429 `email_send_cap_reached` with `details.cap`. - The same body reaching more than 50 distinct recipients within an hour pauses the mailbox with an escalating cooldown (429 `rate_limited`, `account.rate_limited` webhook).  ### Scheduling  With `scheduledFor` the request answers 202 with a `ScheduledEmail` instead of sending. The account and payment method are checked now; the caps, cooldowns and the send itself run at `scheduledFor`. A send that fails then fires `email.send_failed`. List, read and cancel scheduled sends under `/v1/email/messages/scheduled`.  ### Tracking  - `trackOpens` adds a 1x1 image to the html and fires `email.opened`. - `trackLinks` rewrites every http(s) link in the html through a Zernio redirect and fires `email.link_clicked`. - `trackReplies` fires `email.thread_replied` when someone else writes in the thread.  Tracking costs nothing extra. Opens are approximate: image proxies prefetch and image blocking hides them.  ### Other errors  - 402: Gmail sends need a payment method on the workspace. Reading, calendar and files do not. - 400: `holdAsDraft` without `scheduledFor`; `trackOpens` or `trackLinks` without `html`; `scheduledFor` outside 1 minute to 30 days. 

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
    public class SendEmailMessageExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var sendEmailRequest = new SendEmailRequest(); // SendEmailRequest | 

            try
            {
                // Send an email
                SendEmailMessage201Response result = apiInstance.SendEmailMessage(sendEmailRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.SendEmailMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendEmailMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send an email
    ApiResponse<SendEmailMessage201Response> response = apiInstance.SendEmailMessageWithHttpInfo(sendEmailRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.SendEmailMessageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sendEmailRequest** | [**SendEmailRequest**](SendEmailRequest.md) |  |  |

### Return type

[**SendEmailMessage201Response**](SendEmailMessage201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The sent message |  * X-Zernio-Send-Limit - Today&#39;s cap for this mailbox. <br>  * X-Zernio-Send-Remaining -  <br>  * X-Zernio-Send-Reset - When the daily window resets (midnight UTC). <br>  |
| **202** | Scheduled: the send leaves at &#x60;scheduledFor&#x60; |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file, even the 1st one, because X API calls are passed through per call. Prepaid-balance accounts never get it: they pay X calls from the balance. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |
| **429** | The send was refused before reaching the provider.  - &#x60;email_send_cap_reached&#x60;: today&#39;s cap for the mailbox is spent. &#x60;details.cap&#x60; names the limit and &#x60;resetsAt&#x60;; &#x60;retryAfterSeconds&#x60; counts to midnight UTC. - &#x60;rate_limited&#x60;: the mailbox is in a sending cooldown, either from a same-body burst to more than 50 recipients in an hour (&#x60;details.cap.kind: recipient_burst&#x60;) or an earlier trigger. &#x60;retryAfterSeconds&#x60; says when it lifts, and &#x60;account.rate_limited&#x60; fired when it started.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="trashemailmessage"></a>
# **TrashEmailMessage**
> TrashEmailMessage200Response TrashEmailMessage (string messageId, string accountId)

Move a message to trash

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
    public class TrashEmailMessageExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var messageId = "messageId_example";  // string | 
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.

            try
            {
                // Move a message to trash
                TrashEmailMessage200Response result = apiInstance.TrashEmailMessage(messageId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.TrashEmailMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TrashEmailMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Move a message to trash
    ApiResponse<TrashEmailMessage200Response> response = apiInstance.TrashEmailMessageWithHttpInfo(messageId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.TrashEmailMessageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **messageId** | **string** |  |  |
| **accountId** | **string** | The connected Google or Microsoft account. |  |

### Return type

[**TrashEmailMessage200Response**](TrashEmailMessage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Trashed |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateemailmessage"></a>
# **UpdateEmailMessage**
> SendEmailMessage201Response UpdateEmailMessage (string messageId, EmailMessagePatch emailMessagePatch)

Mark read or starred, label, or move a message

`addLabels` and `removeLabels` tag the message without moving it. `folder` moves it: on Google a move files the mail in one place, so it drops the inbox, trash, spam and user labels it held; `archive` removes the inbox label.

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
    public class UpdateEmailMessageExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var messageId = "messageId_example";  // string | 
            var emailMessagePatch = new EmailMessagePatch(); // EmailMessagePatch | 

            try
            {
                // Mark read or starred, label, or move a message
                SendEmailMessage201Response result = apiInstance.UpdateEmailMessage(messageId, emailMessagePatch);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.UpdateEmailMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateEmailMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mark read or starred, label, or move a message
    ApiResponse<SendEmailMessage201Response> response = apiInstance.UpdateEmailMessageWithHttpInfo(messageId, emailMessagePatch);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.UpdateEmailMessageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **messageId** | **string** |  |  |
| **emailMessagePatch** | [**EmailMessagePatch**](EmailMessagePatch.md) |  |  |

### Return type

[**SendEmailMessage201Response**](SendEmailMessage201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated message. A move on Microsoft changes the message id; read it from &#x60;data.id&#x60;. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateemailthread"></a>
# **UpdateEmailThread**
> UpdateEmailThread200Response UpdateEmailThread (string threadId, EmailMessagePatch emailMessagePatch)

Update every message in a thread

Applies `unread`, `starred`, `addLabels`, `removeLabels` or a `folder` move to each message of the thread.

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
    public class UpdateEmailThreadExample
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
            var apiInstance = new EmailApi(httpClient, config, httpClientHandler);
            var threadId = "threadId_example";  // string | 
            var emailMessagePatch = new EmailMessagePatch(); // EmailMessagePatch | 

            try
            {
                // Update every message in a thread
                UpdateEmailThread200Response result = apiInstance.UpdateEmailThread(threadId, emailMessagePatch);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailApi.UpdateEmailThread: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateEmailThreadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update every message in a thread
    ApiResponse<UpdateEmailThread200Response> response = apiInstance.UpdateEmailThreadWithHttpInfo(threadId, emailMessagePatch);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailApi.UpdateEmailThreadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **threadId** | **string** |  |  |
| **emailMessagePatch** | [**EmailMessagePatch**](EmailMessagePatch.md) |  |  |

### Return type

[**UpdateEmailThread200Response**](UpdateEmailThread200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated thread |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

