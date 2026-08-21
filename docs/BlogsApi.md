# Zernio.Api.BlogsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateBlog**](BlogsApi.md#createblog) | **POST** /v1/accounts/{accountId}/blogs | Create a blog |
| [**CreateBlogArticle**](BlogsApi.md#createblogarticle) | **POST** /v1/accounts/{accountId}/blogs/{blogId}/articles | Create a blog article |
| [**DeleteBlog**](BlogsApi.md#deleteblog) | **DELETE** /v1/accounts/{accountId}/blogs/{blogId} | Delete a blog |
| [**DeleteBlogArticle**](BlogsApi.md#deleteblogarticle) | **DELETE** /v1/accounts/{accountId}/blogs/{blogId}/articles/{articleId} | Delete a blog article |
| [**GetBlog**](BlogsApi.md#getblog) | **GET** /v1/accounts/{accountId}/blogs/{blogId} | Get a blog |
| [**GetBlogArticle**](BlogsApi.md#getblogarticle) | **GET** /v1/accounts/{accountId}/blogs/{blogId}/articles/{articleId} | Get a blog article |
| [**ListBlogArticles**](BlogsApi.md#listblogarticles) | **GET** /v1/accounts/{accountId}/blogs/{blogId}/articles | List blog articles |
| [**ListBlogs**](BlogsApi.md#listblogs) | **GET** /v1/accounts/{accountId}/blogs | List blogs |
| [**UpdateBlog**](BlogsApi.md#updateblog) | **PATCH** /v1/accounts/{accountId}/blogs/{blogId} | Update a blog |
| [**UpdateBlogArticle**](BlogsApi.md#updateblogarticle) | **PATCH** /v1/accounts/{accountId}/blogs/{blogId}/articles/{articleId} | Update a blog article |

<a id="createblog"></a>
# **CreateBlog**
> CreateBlog201Response CreateBlog (string accountId, CreateBlogRequest createBlogRequest)

Create a blog

Creates a blog on the connected store. The platform generates the URL `handle` from the title when omitted.  Supported on Shopify (platform `shopify`). Accounts on platforms without blogs support return 400; a blogs-capable platform that lacks this specific operation returns 405. 

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
    public class CreateBlogExample
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
            var apiInstance = new BlogsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected Shopify SocialAccount id.
            var createBlogRequest = new CreateBlogRequest(); // CreateBlogRequest | 

            try
            {
                // Create a blog
                CreateBlog201Response result = apiInstance.CreateBlog(accountId, createBlogRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BlogsApi.CreateBlog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBlogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a blog
    ApiResponse<CreateBlog201Response> response = apiInstance.CreateBlogWithHttpInfo(accountId, createBlogRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BlogsApi.CreateBlogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected Shopify SocialAccount id. |  |
| **createBlogRequest** | [**CreateBlogRequest**](CreateBlogRequest.md) |  |  |

### Return type

[**CreateBlog201Response**](CreateBlog201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Blog created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions); reconnect the Shopify account to restore access. |  -  |
| **404** | Account not found or not accessible (code account_not_found). |  -  |
| **405** | Platform does not support creating blogs. |  -  |
| **429** | Rate limited, either by Zernio or by Shopify. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createblogarticle"></a>
# **CreateBlogArticle**
> CreateBlogArticle201Response CreateBlogArticle (string accountId, string blogId, CreateBlogArticleRequest createBlogArticleRequest)

Create a blog article

Creates an article on the blog. Publishing behavior:  - `isPublished: false` keeps the article as a draft. - A future `publishDate` schedules publication natively on the   platform; the platform publishes it at that time with no Zernio   queue involved. - `seo.title` / `seo.description` map to Shopify's global `title_tag`   and `description_tag` metafields (the fields Shopify themes read for   the page title and meta description).  Supported on Shopify (platform `shopify`). Accounts on platforms without blogs support return 400; a blogs-capable platform that lacks this specific operation returns 405. 

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
    public class CreateBlogArticleExample
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
            var apiInstance = new BlogsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected Shopify SocialAccount id.
            var blogId = "blogId_example";  // string | Platform-native numeric blog id. Non-numeric values return 400.
            var createBlogArticleRequest = new CreateBlogArticleRequest(); // CreateBlogArticleRequest | 

            try
            {
                // Create a blog article
                CreateBlogArticle201Response result = apiInstance.CreateBlogArticle(accountId, blogId, createBlogArticleRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BlogsApi.CreateBlogArticle: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBlogArticleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a blog article
    ApiResponse<CreateBlogArticle201Response> response = apiInstance.CreateBlogArticleWithHttpInfo(accountId, blogId, createBlogArticleRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BlogsApi.CreateBlogArticleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected Shopify SocialAccount id. |  |
| **blogId** | **string** | Platform-native numeric blog id. Non-numeric values return 400. |  |
| **createBlogArticleRequest** | [**CreateBlogArticleRequest**](CreateBlogArticleRequest.md) |  |  |

### Return type

[**CreateBlogArticle201Response**](CreateBlogArticle201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Article created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions); reconnect the Shopify account to restore access. |  -  |
| **404** | Account not found or not accessible (code account_not_found), or blog not found (code blog_not_found). |  -  |
| **405** | Platform does not support creating articles. |  -  |
| **429** | Rate limited, either by Zernio or by Shopify. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteblog"></a>
# **DeleteBlog**
> void DeleteBlog (string accountId, string blogId)

Delete a blog

Deletes the blog AND every article in it. The delete happens on the platform and is permanent; Zernio stores nothing to restore it from.  Supported on Shopify (platform `shopify`). Accounts on platforms without blogs support return 400; a blogs-capable platform that lacks this specific operation returns 405. 

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
    public class DeleteBlogExample
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
            var apiInstance = new BlogsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected Shopify SocialAccount id.
            var blogId = "blogId_example";  // string | Platform-native numeric blog id. Non-numeric values return 400.

            try
            {
                // Delete a blog
                apiInstance.DeleteBlog(accountId, blogId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BlogsApi.DeleteBlog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBlogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a blog
    apiInstance.DeleteBlogWithHttpInfo(accountId, blogId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BlogsApi.DeleteBlogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected Shopify SocialAccount id. |  |
| **blogId** | **string** | Platform-native numeric blog id. Non-numeric values return 400. |  |

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
| **204** | Blog deleted (no content). |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions); reconnect the Shopify account to restore access. |  -  |
| **404** | Account not found or not accessible (code account_not_found), or blog not found (code blog_not_found). |  -  |
| **405** | Platform does not support deleting a blog. |  -  |
| **429** | Rate limited, either by Zernio or by Shopify. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteblogarticle"></a>
# **DeleteBlogArticle**
> void DeleteBlogArticle (string accountId, string blogId, string articleId)

Delete a blog article

Deletes the article. The delete happens on the platform and is permanent; Zernio stores nothing to restore it from.  Supported on Shopify (platform `shopify`). Accounts on platforms without blogs support return 400; a blogs-capable platform that lacks this specific operation returns 405. 

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
    public class DeleteBlogArticleExample
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
            var apiInstance = new BlogsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected Shopify SocialAccount id.
            var blogId = "blogId_example";  // string | Platform-native numeric blog id. Non-numeric values return 400.
            var articleId = "articleId_example";  // string | Platform-native numeric article id. Non-numeric values return 400.

            try
            {
                // Delete a blog article
                apiInstance.DeleteBlogArticle(accountId, blogId, articleId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BlogsApi.DeleteBlogArticle: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBlogArticleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a blog article
    apiInstance.DeleteBlogArticleWithHttpInfo(accountId, blogId, articleId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BlogsApi.DeleteBlogArticleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected Shopify SocialAccount id. |  |
| **blogId** | **string** | Platform-native numeric blog id. Non-numeric values return 400. |  |
| **articleId** | **string** | Platform-native numeric article id. Non-numeric values return 400. |  |

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
| **204** | Article deleted (no content). |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions); reconnect the Shopify account to restore access. |  -  |
| **404** | Account not found or not accessible (code account_not_found), blog not found (code blog_not_found), or article not found (code blog_article_not_found). |  -  |
| **405** | Platform does not support deleting an article. |  -  |
| **429** | Rate limited, either by Zernio or by Shopify. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getblog"></a>
# **GetBlog**
> CreateBlog201Response GetBlog (string accountId, string blogId)

Get a blog

Fetches a single blog. `blogId` is the platform's numeric blog id from `GET /v1/accounts/{accountId}/blogs`, not a Zernio id.  Supported on Shopify (platform `shopify`). Accounts on platforms without blogs support return 400; a blogs-capable platform that lacks this specific operation returns 405. 

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
    public class GetBlogExample
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
            var apiInstance = new BlogsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected Shopify SocialAccount id.
            var blogId = "blogId_example";  // string | Platform-native numeric blog id. Non-numeric values return 400.

            try
            {
                // Get a blog
                CreateBlog201Response result = apiInstance.GetBlog(accountId, blogId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BlogsApi.GetBlog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBlogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a blog
    ApiResponse<CreateBlog201Response> response = apiInstance.GetBlogWithHttpInfo(accountId, blogId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BlogsApi.GetBlogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected Shopify SocialAccount id. |  |
| **blogId** | **string** | Platform-native numeric blog id. Non-numeric values return 400. |  |

### Return type

[**CreateBlog201Response**](CreateBlog201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Blog fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions); reconnect the Shopify account to restore access. |  -  |
| **404** | Account not found or not accessible (code account_not_found), or blog not found (code blog_not_found). |  -  |
| **405** | Platform does not support fetching a blog. |  -  |
| **429** | Rate limited, either by Zernio or by Shopify. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getblogarticle"></a>
# **GetBlogArticle**
> CreateBlogArticle201Response GetBlogArticle (string accountId, string blogId, string articleId)

Get a blog article

Fetches a single article. An article addressed through a blog it does not belong to is a 404 (code blog_article_not_found).  Supported on Shopify (platform `shopify`). Accounts on platforms without blogs support return 400; a blogs-capable platform that lacks this specific operation returns 405. 

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
    public class GetBlogArticleExample
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
            var apiInstance = new BlogsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected Shopify SocialAccount id.
            var blogId = "blogId_example";  // string | Platform-native numeric blog id. Non-numeric values return 400.
            var articleId = "articleId_example";  // string | Platform-native numeric article id. Non-numeric values return 400.

            try
            {
                // Get a blog article
                CreateBlogArticle201Response result = apiInstance.GetBlogArticle(accountId, blogId, articleId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BlogsApi.GetBlogArticle: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBlogArticleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a blog article
    ApiResponse<CreateBlogArticle201Response> response = apiInstance.GetBlogArticleWithHttpInfo(accountId, blogId, articleId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BlogsApi.GetBlogArticleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected Shopify SocialAccount id. |  |
| **blogId** | **string** | Platform-native numeric blog id. Non-numeric values return 400. |  |
| **articleId** | **string** | Platform-native numeric article id. Non-numeric values return 400. |  |

### Return type

[**CreateBlogArticle201Response**](CreateBlogArticle201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Article fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions); reconnect the Shopify account to restore access. |  -  |
| **404** | Account not found or not accessible (code account_not_found), blog not found (code blog_not_found), or article not found (code blog_article_not_found). |  -  |
| **405** | Platform does not support fetching an article. |  -  |
| **429** | Rate limited, either by Zernio or by Shopify. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listblogarticles"></a>
# **ListBlogArticles**
> ListBlogArticles200Response ListBlogArticles (string accountId, string blogId, int? limit = null, string? cursor = null)

List blog articles

Lists the articles of a blog. Cursor-paginated: pass `limit` (1-50, default 20) and the `cursor` from a previous response's `nextCursor`; `nextCursor` is null when there are no more pages.  Supported on Shopify (platform `shopify`). Accounts on platforms without blogs support return 400; a blogs-capable platform that lacks this specific operation returns 405. 

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
    public class ListBlogArticlesExample
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
            var apiInstance = new BlogsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected Shopify SocialAccount id.
            var blogId = "blogId_example";  // string | Platform-native numeric blog id. Non-numeric values return 400.
            var limit = 20;  // int? | Page size (1-50). (optional)  (default to 20)
            var cursor = "cursor_example";  // string? | Opaque cursor from a previous response. Omit for the first page. (optional) 

            try
            {
                // List blog articles
                ListBlogArticles200Response result = apiInstance.ListBlogArticles(accountId, blogId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BlogsApi.ListBlogArticles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBlogArticlesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List blog articles
    ApiResponse<ListBlogArticles200Response> response = apiInstance.ListBlogArticlesWithHttpInfo(accountId, blogId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BlogsApi.ListBlogArticlesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected Shopify SocialAccount id. |  |
| **blogId** | **string** | Platform-native numeric blog id. Non-numeric values return 400. |  |
| **limit** | **int?** | Page size (1-50). | [optional] [default to 20] |
| **cursor** | **string?** | Opaque cursor from a previous response. Omit for the first page. | [optional]  |

### Return type

[**ListBlogArticles200Response**](ListBlogArticles200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Articles listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions); reconnect the Shopify account to restore access. |  -  |
| **404** | Account not found or not accessible (code account_not_found), or blog not found (code blog_not_found). |  -  |
| **405** | Platform does not support listing articles. |  -  |
| **429** | Rate limited, either by Zernio or by Shopify. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listblogs"></a>
# **ListBlogs**
> ListBlogs200Response ListBlogs (string accountId, int? limit = null, string? cursor = null)

List blogs

Lists the blogs on the connected store, newest-first as the platform returns them. Cursor-paginated: pass `limit` (1-50, default 20) and the `cursor` from a previous response's `nextCursor`; `nextCursor` is null when there are no more pages.  Supported on Shopify (platform `shopify`). Accounts on platforms without blogs support return 400; a blogs-capable platform that lacks this specific operation returns 405. 

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
    public class ListBlogsExample
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
            var apiInstance = new BlogsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected Shopify SocialAccount id.
            var limit = 20;  // int? | Page size (1-50). (optional)  (default to 20)
            var cursor = "cursor_example";  // string? | Opaque cursor from a previous response. Omit for the first page. (optional) 

            try
            {
                // List blogs
                ListBlogs200Response result = apiInstance.ListBlogs(accountId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BlogsApi.ListBlogs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBlogsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List blogs
    ApiResponse<ListBlogs200Response> response = apiInstance.ListBlogsWithHttpInfo(accountId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BlogsApi.ListBlogsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected Shopify SocialAccount id. |  |
| **limit** | **int?** | Page size (1-50). | [optional] [default to 20] |
| **cursor** | **string?** | Opaque cursor from a previous response. Omit for the first page. | [optional]  |

### Return type

[**ListBlogs200Response**](ListBlogs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Blogs listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions); reconnect the Shopify account to restore access. |  -  |
| **404** | Account not found or not accessible (code account_not_found). |  -  |
| **405** | Platform does not support listing blogs. |  -  |
| **429** | Rate limited, either by Zernio or by Shopify. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateblog"></a>
# **UpdateBlog**
> CreateBlog201Response UpdateBlog (string accountId, string blogId, UpdateBlogRequest updateBlogRequest)

Update a blog

Partial-updates a blog. Send any subset of `title` and `handle`; at least one field is required (an empty body returns 400).  Supported on Shopify (platform `shopify`). Accounts on platforms without blogs support return 400; a blogs-capable platform that lacks this specific operation returns 405. 

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
    public class UpdateBlogExample
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
            var apiInstance = new BlogsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected Shopify SocialAccount id.
            var blogId = "blogId_example";  // string | Platform-native numeric blog id. Non-numeric values return 400.
            var updateBlogRequest = new UpdateBlogRequest(); // UpdateBlogRequest | 

            try
            {
                // Update a blog
                CreateBlog201Response result = apiInstance.UpdateBlog(accountId, blogId, updateBlogRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BlogsApi.UpdateBlog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBlogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a blog
    ApiResponse<CreateBlog201Response> response = apiInstance.UpdateBlogWithHttpInfo(accountId, blogId, updateBlogRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BlogsApi.UpdateBlogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected Shopify SocialAccount id. |  |
| **blogId** | **string** | Platform-native numeric blog id. Non-numeric values return 400. |  |
| **updateBlogRequest** | [**UpdateBlogRequest**](UpdateBlogRequest.md) |  |  |

### Return type

[**CreateBlog201Response**](CreateBlog201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Blog updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions); reconnect the Shopify account to restore access. |  -  |
| **404** | Account not found or not accessible (code account_not_found), or blog not found (code blog_not_found). |  -  |
| **405** | Platform does not support updating a blog. |  -  |
| **429** | Rate limited, either by Zernio or by Shopify. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateblogarticle"></a>
# **UpdateBlogArticle**
> CreateBlogArticle201Response UpdateBlogArticle (string accountId, string blogId, string articleId, UpdateBlogArticleRequest updateBlogArticleRequest)

Update a blog article

Partial-updates an article. Send any subset of the create fields (`title`, `bodyHtml`, `handle`, `tags`, `author`, `excerpt`, `image`, `seo`, `isPublished`, `publishDate`); at least one field is required (an empty body returns 400). `isPublished` and `publishDate` behave as on create: `isPublished: false` unpublishes back to a draft and a future `publishDate` schedules publication natively on the platform.  Supported on Shopify (platform `shopify`). Accounts on platforms without blogs support return 400; a blogs-capable platform that lacks this specific operation returns 405. 

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
    public class UpdateBlogArticleExample
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
            var apiInstance = new BlogsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected Shopify SocialAccount id.
            var blogId = "blogId_example";  // string | Platform-native numeric blog id. Non-numeric values return 400.
            var articleId = "articleId_example";  // string | Platform-native numeric article id. Non-numeric values return 400.
            var updateBlogArticleRequest = new UpdateBlogArticleRequest(); // UpdateBlogArticleRequest | 

            try
            {
                // Update a blog article
                CreateBlogArticle201Response result = apiInstance.UpdateBlogArticle(accountId, blogId, articleId, updateBlogArticleRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BlogsApi.UpdateBlogArticle: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBlogArticleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a blog article
    ApiResponse<CreateBlogArticle201Response> response = apiInstance.UpdateBlogArticleWithHttpInfo(accountId, blogId, articleId, updateBlogArticleRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BlogsApi.UpdateBlogArticleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected Shopify SocialAccount id. |  |
| **blogId** | **string** | Platform-native numeric blog id. Non-numeric values return 400. |  |
| **articleId** | **string** | Platform-native numeric article id. Non-numeric values return 400. |  |
| **updateBlogArticleRequest** | [**UpdateBlogArticleRequest**](UpdateBlogArticleRequest.md) |  |  |

### Return type

[**CreateBlogArticle201Response**](CreateBlogArticle201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Article updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions); reconnect the Shopify account to restore access. |  -  |
| **404** | Account not found or not accessible (code account_not_found), blog not found (code blog_not_found), or article not found (code blog_article_not_found). |  -  |
| **405** | Platform does not support updating an article. |  -  |
| **429** | Rate limited, either by Zernio or by Shopify. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

