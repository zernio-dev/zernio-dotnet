# Zernio.Api.FilesApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateFilePickerSession**](FilesApi.md#createfilepickersession) | **POST** /v1/files/picker-sessions | Create a hosted Google Picker session |
| [**CreateFolder**](FilesApi.md#createfolder) | **POST** /v1/files/folders | Create a folder |
| [**DownloadFile**](FilesApi.md#downloadfile) | **GET** /v1/files/{fileId}/download | Download a file |
| [**GetFile**](FilesApi.md#getfile) | **GET** /v1/files/{fileId} | Get a file or folder |
| [**GetFileShareLink**](FilesApi.md#getfilesharelink) | **GET** /v1/files/{fileId}/share-link | Get an anyone-with-the-link share link |
| [**ListFiles**](FilesApi.md#listfiles) | **GET** /v1/files | List files in a folder or search the drive |
| [**TrashFile**](FilesApi.md#trashfile) | **DELETE** /v1/files/{fileId} | Move a file to the trash |
| [**UpdateFile**](FilesApi.md#updatefile) | **PATCH** /v1/files/{fileId} | Rename or move a file |
| [**UploadFile**](FilesApi.md#uploadfile) | **POST** /v1/files | Upload a file |

<a id="createfilepickersession"></a>
# **CreateFilePickerSession**
> CreateFilePickerSession201Response CreateFilePickerSession (CreateFilePickerSessionRequest createFilePickerSessionRequest)

Create a hosted Google Picker session

Google accounts are connected with `drive.file`, so Zernio opens only files it created or the user picked (see the Files tag). This is how your end user grants files: create a session, send the user to `url`, and they pick files in Google Picker on a Zernio-hosted page.  When they finish, the browser is sent to `redirectUrl` with these query params added (existing params are kept):    - `status=picked`, `pickerSessionId`, `fileIds` (comma-separated Drive file ids, already checked against Drive), or   - `status=cancelled`, `pickerSessionId` when the user pressed Cancel.  A `file.picked` webhook fires on every successful pick, so `redirectUrl` is optional for server-side integrations. Closing the picker without picking keeps the session open; the user can try again until it expires.  The URL is single-use and expires after 30 minutes; create a new session for every pick. Google accounts only: Microsoft accounts answer 400 `platform_not_supported` because OneDrive needs no picker. Picks are permanent grants: once picked, a file stays readable through the Files endpoints until the user removes Zernio from their Google account. 

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
    public class CreateFilePickerSessionExample
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
            var apiInstance = new FilesApi(httpClient, config, httpClientHandler);
            var createFilePickerSessionRequest = new CreateFilePickerSessionRequest(); // CreateFilePickerSessionRequest | 

            try
            {
                // Create a hosted Google Picker session
                CreateFilePickerSession201Response result = apiInstance.CreateFilePickerSession(createFilePickerSessionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FilesApi.CreateFilePickerSession: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateFilePickerSessionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a hosted Google Picker session
    ApiResponse<CreateFilePickerSession201Response> response = apiInstance.CreateFilePickerSessionWithHttpInfo(createFilePickerSessionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FilesApi.CreateFilePickerSessionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createFilePickerSessionRequest** | [**CreateFilePickerSessionRequest**](CreateFilePickerSessionRequest.md) |  |  |

### Return type

[**CreateFilePickerSession201Response**](CreateFilePickerSession201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The session |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:    - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;.   - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval; &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one. It opens in a browser with no API key and stays valid for one hour; &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createfolder"></a>
# **CreateFolder**
> UploadFile201Response CreateFolder (CreateFolderRequest createFolderRequest)

Create a folder

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
    public class CreateFolderExample
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
            var apiInstance = new FilesApi(httpClient, config, httpClientHandler);
            var createFolderRequest = new CreateFolderRequest(); // CreateFolderRequest | 

            try
            {
                // Create a folder
                UploadFile201Response result = apiInstance.CreateFolder(createFolderRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FilesApi.CreateFolder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateFolderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a folder
    ApiResponse<UploadFile201Response> response = apiInstance.CreateFolderWithHttpInfo(createFolderRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FilesApi.CreateFolderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createFolderRequest** | [**CreateFolderRequest**](CreateFolderRequest.md) |  |  |

### Return type

[**UploadFile201Response**](UploadFile201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The folder |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:    - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;.   - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval; &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one. It opens in a browser with no API key and stays valid for one hour; &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="downloadfile"></a>
# **DownloadFile**
> FileParameter DownloadFile (string fileId, string accountId)

Download a file

Streams the bytes with `Content-Disposition: attachment`. Google Docs, Slides and Drawings arrive as PDF/PNG and Sheets as XLSX, named with the export extension. Folders answer 400.

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
    public class DownloadFileExample
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
            var apiInstance = new FilesApi(httpClient, config, httpClientHandler);
            var fileId = "fileId_example";  // string | 
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.

            try
            {
                // Download a file
                FileParameter result = apiInstance.DownloadFile(fileId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FilesApi.DownloadFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DownloadFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Download a file
    ApiResponse<FileParameter> response = apiInstance.DownloadFileWithHttpInfo(fileId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FilesApi.DownloadFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fileId** | **string** |  |  |
| **accountId** | **string** | The connected Google or Microsoft account. |  |

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
| **200** | The file bytes |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:    - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;.   - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval; &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one. It opens in a browser with no API key and stays valid for one hour; &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getfile"></a>
# **GetFile**
> UploadFile201Response GetFile (string fileId, string accountId)

Get a file or folder

On Google Drive, a file Zernio neither created nor was given through Google Picker answers 404 `resource_not_found` with `details: { fileId, reason: file_not_granted }`; send the user through `POST /v1/files/picker-sessions` (pass the id in `fileIds` to show it first). The same 404 applies to download, update, trash and share-link.

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
    public class GetFileExample
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
            var apiInstance = new FilesApi(httpClient, config, httpClientHandler);
            var fileId = "fileId_example";  // string | 
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.

            try
            {
                // Get a file or folder
                UploadFile201Response result = apiInstance.GetFile(fileId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FilesApi.GetFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a file or folder
    ApiResponse<UploadFile201Response> response = apiInstance.GetFileWithHttpInfo(fileId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FilesApi.GetFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fileId** | **string** |  |  |
| **accountId** | **string** | The connected Google or Microsoft account. |  |

### Return type

[**UploadFile201Response**](UploadFile201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The item |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:    - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;.   - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval; &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one. It opens in a browser with no API key and stays valid for one hour; &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getfilesharelink"></a>
# **GetFileShareLink**
> GetFileShareLink200Response GetFileShareLink (string fileId, string accountId)

Get an anyone-with-the-link share link

Grants read access to anyone holding the link (Drive `anyone` permission, OneDrive anonymous view link) and returns it. The grant stays until it is revoked on the provider.

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
    public class GetFileShareLinkExample
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
            var apiInstance = new FilesApi(httpClient, config, httpClientHandler);
            var fileId = "fileId_example";  // string | 
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.

            try
            {
                // Get an anyone-with-the-link share link
                GetFileShareLink200Response result = apiInstance.GetFileShareLink(fileId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FilesApi.GetFileShareLink: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFileShareLinkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an anyone-with-the-link share link
    ApiResponse<GetFileShareLink200Response> response = apiInstance.GetFileShareLinkWithHttpInfo(fileId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FilesApi.GetFileShareLinkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fileId** | **string** |  |  |
| **accountId** | **string** | The connected Google or Microsoft account. |  |

### Return type

[**GetFileShareLink200Response**](GetFileShareLink200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The link |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:    - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;.   - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval; &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one. It opens in a browser with no API key and stays valid for one hour; &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listfiles"></a>
# **ListFiles**
> ListFiles200Response ListFiles (string accountId, string? folderId = null, string? q = null, string? cursor = null, int? limit = null)

List files in a folder or search the drive

Children of `folderId` (the root by default), folders first. With `q` and no `folderId` the whole drive is searched by name (on Google, every drive the app can see, shared drives included). The account must have been connected with `scopes=files` (412 `account_scope_missing` otherwise). Cursors are opaque and provider-issued. Google Drive returns only files Zernio created or the user picked (see the Files tag): an unpicked folder lists empty.

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
    public class ListFilesExample
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
            var apiInstance = new FilesApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.
            var folderId = "folderId_example";  // string? | Provider folder id; omit for the root. (optional) 
            var q = "q_example";  // string? | Name search. (optional) 
            var cursor = "cursor_example";  // string? |  (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)

            try
            {
                // List files in a folder or search the drive
                ListFiles200Response result = apiInstance.ListFiles(accountId, folderId, q, cursor, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FilesApi.ListFiles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListFilesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List files in a folder or search the drive
    ApiResponse<ListFiles200Response> response = apiInstance.ListFilesWithHttpInfo(accountId, folderId, q, cursor, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FilesApi.ListFilesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected Google or Microsoft account. |  |
| **folderId** | **string?** | Provider folder id; omit for the root. | [optional]  |
| **q** | **string?** | Name search. | [optional]  |
| **cursor** | **string?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |

### Return type

[**ListFiles200Response**](ListFiles200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Files |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:    - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;.   - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval; &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one. It opens in a browser with no API key and stays valid for one hour; &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="trashfile"></a>
# **TrashFile**
> TrashFile200Response TrashFile (string fileId, string accountId)

Move a file to the trash

Drive trash or the OneDrive recycle bin; nothing is destroyed and the user can restore it on the provider.

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
    public class TrashFileExample
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
            var apiInstance = new FilesApi(httpClient, config, httpClientHandler);
            var fileId = "fileId_example";  // string | 
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.

            try
            {
                // Move a file to the trash
                TrashFile200Response result = apiInstance.TrashFile(fileId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FilesApi.TrashFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TrashFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Move a file to the trash
    ApiResponse<TrashFile200Response> response = apiInstance.TrashFileWithHttpInfo(fileId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FilesApi.TrashFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fileId** | **string** |  |  |
| **accountId** | **string** | The connected Google or Microsoft account. |  |

### Return type

[**TrashFile200Response**](TrashFile200Response.md)

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
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:    - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;.   - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval; &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one. It opens in a browser with no API key and stays valid for one hour; &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatefile"></a>
# **UpdateFile**
> UploadFile201Response UpdateFile (string fileId, UpdateFileRequest updateFileRequest)

Rename or move a file

`parentId` moves the item into another folder; `name` renames it. At least one is required.

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
    public class UpdateFileExample
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
            var apiInstance = new FilesApi(httpClient, config, httpClientHandler);
            var fileId = "fileId_example";  // string | 
            var updateFileRequest = new UpdateFileRequest(); // UpdateFileRequest | 

            try
            {
                // Rename or move a file
                UploadFile201Response result = apiInstance.UpdateFile(fileId, updateFileRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FilesApi.UpdateFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Rename or move a file
    ApiResponse<UploadFile201Response> response = apiInstance.UpdateFileWithHttpInfo(fileId, updateFileRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FilesApi.UpdateFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fileId** | **string** |  |  |
| **updateFileRequest** | [**UpdateFileRequest**](UpdateFileRequest.md) |  |  |

### Return type

[**UploadFile201Response**](UploadFile201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated item |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:    - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;.   - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval; &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one. It opens in a browser with no API key and stays valid for one hour; &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="uploadfile"></a>
# **UploadFile**
> UploadFile201Response UploadFile (UploadFileRequest uploadFileRequest)

Upload a file

Either `multipart/form-data` with the file under `file` plus `accountId`, `name` (defaults to the file name) and `parentId`, or JSON with a public `url` the file is fetched from (100 MB cap). Large files go through the provider's resumable upload.

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
    public class UploadFileExample
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
            var apiInstance = new FilesApi(httpClient, config, httpClientHandler);
            var uploadFileRequest = new UploadFileRequest(); // UploadFileRequest | 

            try
            {
                // Upload a file
                UploadFile201Response result = apiInstance.UploadFile(uploadFileRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FilesApi.UploadFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload a file
    ApiResponse<UploadFile201Response> response = apiInstance.UploadFileWithHttpInfo(uploadFileRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FilesApi.UploadFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **uploadFileRequest** | [**UploadFileRequest**](UploadFileRequest.md) |  |  |

### Return type

[**UploadFile201Response**](UploadFile201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json, multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The stored file |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:    - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;.   - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval; &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one. It opens in a browser with no API key and stays valid for one hour; &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

