# Zernio.Api.DiscordApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddDiscordMemberRole**](DiscordApi.md#adddiscordmemberrole) | **PUT** /v1/discord/guilds/{guildId}/members/{userId}/roles/{roleId} | Assign a role to a guild member |
| [**CreateDiscordScheduledEvent**](DiscordApi.md#creatediscordscheduledevent) | **POST** /v1/discord/guilds/{guildId}/events | Create a Discord scheduled event |
| [**DeleteDiscordScheduledEvent**](DiscordApi.md#deletediscordscheduledevent) | **DELETE** /v1/discord/guilds/{guildId}/events/{eventId} | Delete a Discord scheduled event |
| [**GetDiscordChannels**](DiscordApi.md#getdiscordchannels) | **GET** /v1/accounts/{accountId}/discord-channels | List Discord guild channels |
| [**GetDiscordScheduledEvent**](DiscordApi.md#getdiscordscheduledevent) | **GET** /v1/discord/guilds/{guildId}/events/{eventId} | Get a Discord scheduled event |
| [**GetDiscordSettings**](DiscordApi.md#getdiscordsettings) | **GET** /v1/accounts/{accountId}/discord-settings | Get Discord account settings |
| [**ListDiscordGuildMembers**](DiscordApi.md#listdiscordguildmembers) | **GET** /v1/discord/guilds/{guildId}/members | List Discord guild members |
| [**ListDiscordGuildRoles**](DiscordApi.md#listdiscordguildroles) | **GET** /v1/discord/guilds/{guildId}/roles | List Discord guild roles |
| [**ListDiscordPinnedMessages**](DiscordApi.md#listdiscordpinnedmessages) | **GET** /v1/discord/channels/{channelId}/pins | List pinned messages in a Discord channel |
| [**ListDiscordScheduledEvents**](DiscordApi.md#listdiscordscheduledevents) | **GET** /v1/discord/guilds/{guildId}/events | List Discord scheduled events |
| [**PinDiscordMessage**](DiscordApi.md#pindiscordmessage) | **PUT** /v1/discord/channels/{channelId}/pins/{messageId} | Pin a Discord message |
| [**RemoveDiscordMemberRole**](DiscordApi.md#removediscordmemberrole) | **DELETE** /v1/discord/guilds/{guildId}/members/{userId}/roles/{roleId} | Remove a role from a guild member |
| [**SendDiscordDirectMessage**](DiscordApi.md#senddiscorddirectmessage) | **POST** /v1/discord/dms | Send a Discord Direct Message |
| [**UnpinDiscordMessage**](DiscordApi.md#unpindiscordmessage) | **DELETE** /v1/discord/channels/{channelId}/pins/{messageId} | Unpin a Discord message |
| [**UpdateDiscordScheduledEvent**](DiscordApi.md#updatediscordscheduledevent) | **PATCH** /v1/discord/guilds/{guildId}/events/{eventId} | Update a Discord scheduled event |
| [**UpdateDiscordSettings**](DiscordApi.md#updatediscordsettings) | **PATCH** /v1/accounts/{accountId}/discord-settings | Update Discord settings |

<a id="adddiscordmemberrole"></a>
# **AddDiscordMemberRole**
> AddDiscordMemberRole200Response AddDiscordMemberRole (string guildId, string userId, string roleId, string accountId)

Assign a role to a guild member

Assign one role to one member. Idempotent on Discord's side — re-running on a member who already has the role is a 204 no-op.  Path shape mirrors Discord's own API (`PUT /guilds/{guild}/members/{user}/roles/{role}`) for zero-translation mental mapping.  Bot needs MANAGE_ROLES permission in the guild AND its highest role must be above the target role (Discord hierarchy rule). The `@everyone` role (where roleId == guildId) cannot be assigned. 

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
    public class AddDiscordMemberRoleExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var guildId = "guildId_example";  // string | 
            var userId = "userId_example";  // string | Discord user snowflake to assign the role to.
            var roleId = "roleId_example";  // string | 
            var accountId = "accountId_example";  // string | 

            try
            {
                // Assign a role to a guild member
                AddDiscordMemberRole200Response result = apiInstance.AddDiscordMemberRole(guildId, userId, roleId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.AddDiscordMemberRole: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddDiscordMemberRoleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Assign a role to a guild member
    ApiResponse<AddDiscordMemberRole200Response> response = apiInstance.AddDiscordMemberRoleWithHttpInfo(guildId, userId, roleId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.AddDiscordMemberRoleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **guildId** | **string** |  |  |
| **userId** | **string** | Discord user snowflake to assign the role to. |  |
| **roleId** | **string** |  |  |
| **accountId** | **string** |  |  |

### Return type

[**AddDiscordMemberRole200Response**](AddDiscordMemberRole200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Role assigned (or already present — idempotent). |  -  |
| **400** | Validation error (malformed snowflake) or @everyone manipulation attempt. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Discord account not found or not in this guild. |  -  |
| **502** | Discord rejected the request: bot lacks MANAGE_ROLES, or target role is above the bot&#39;s highest role. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="creatediscordscheduledevent"></a>
# **CreateDiscordScheduledEvent**
> CreateDiscordScheduledEvent200Response CreateDiscordScheduledEvent (string guildId, CreateDiscordScheduledEventRequest createDiscordScheduledEventRequest)

Create a Discord scheduled event

Create a guild scheduled event. Three event types, selected via the discriminator on `entity.type`:    - `external` — off-platform (Zoom, in-person, livestream). Requires     both `location` and `endsAt`. Most common type for scheduler     integrations.   - `voice` — hosted in a Discord voice channel. Requires `channelId`.   - `stage` — hosted in a Discord stage channel. Requires `channelId`.  Bot needs MANAGE_EVENTS in the guild. Existing installs (pre-events PR) need a re-invite OR a server admin manually granting the permission — see route header for details. 

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
    public class CreateDiscordScheduledEventExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var guildId = "guildId_example";  // string | 
            var createDiscordScheduledEventRequest = new CreateDiscordScheduledEventRequest(); // CreateDiscordScheduledEventRequest | 

            try
            {
                // Create a Discord scheduled event
                CreateDiscordScheduledEvent200Response result = apiInstance.CreateDiscordScheduledEvent(guildId, createDiscordScheduledEventRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.CreateDiscordScheduledEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateDiscordScheduledEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a Discord scheduled event
    ApiResponse<CreateDiscordScheduledEvent200Response> response = apiInstance.CreateDiscordScheduledEventWithHttpInfo(guildId, createDiscordScheduledEventRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.CreateDiscordScheduledEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **guildId** | **string** |  |  |
| **createDiscordScheduledEventRequest** | [**CreateDiscordScheduledEventRequest**](CreateDiscordScheduledEventRequest.md) |  |  |

### Return type

[**CreateDiscordScheduledEvent200Response**](CreateDiscordScheduledEvent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Event created. |  -  |
| **400** | Validation error (missing required fields for the chosen entity type, malformed snowflake, past startsAt, etc.). |  -  |
| **401** | Unauthorized |  -  |
| **404** | Discord account not found. |  -  |
| **502** | Bot lacks MANAGE_EVENTS in the guild. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletediscordscheduledevent"></a>
# **DeleteDiscordScheduledEvent**
> DeleteDiscordScheduledEvent200Response DeleteDiscordScheduledEvent (string guildId, string eventId, string accountId)

Delete a Discord scheduled event

Hard-delete an event. Use PATCH with `status: 'cancelled'` instead if you want the event preserved in the guild's history. 

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
    public class DeleteDiscordScheduledEventExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var guildId = "guildId_example";  // string | 
            var eventId = "eventId_example";  // string | 
            var accountId = "accountId_example";  // string | 

            try
            {
                // Delete a Discord scheduled event
                DeleteDiscordScheduledEvent200Response result = apiInstance.DeleteDiscordScheduledEvent(guildId, eventId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.DeleteDiscordScheduledEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteDiscordScheduledEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a Discord scheduled event
    ApiResponse<DeleteDiscordScheduledEvent200Response> response = apiInstance.DeleteDiscordScheduledEventWithHttpInfo(guildId, eventId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.DeleteDiscordScheduledEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **guildId** | **string** |  |  |
| **eventId** | **string** |  |  |
| **accountId** | **string** |  |  |

### Return type

[**DeleteDiscordScheduledEvent200Response**](DeleteDiscordScheduledEvent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Event deleted. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Event or Discord account not found. |  -  |
| **502** | Bot lacks MANAGE_EVENTS in the guild. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getdiscordchannels"></a>
# **GetDiscordChannels**
> GetDiscordChannels200Response GetDiscordChannels (string accountId)

List Discord guild channels

Returns the text, announcement, and forum channels in the connected Discord guild. Use this to discover available channels when switching the connected channel via PATCH /v1/accounts/{accountId}/discord-settings.

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
    public class GetDiscordChannelsExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // List Discord guild channels
                GetDiscordChannels200Response result = apiInstance.GetDiscordChannels(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.GetDiscordChannels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDiscordChannelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Discord guild channels
    ApiResponse<GetDiscordChannels200Response> response = apiInstance.GetDiscordChannelsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.GetDiscordChannelsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetDiscordChannels200Response**](GetDiscordChannels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Channel list |  -  |
| **400** | Not a Discord account or missing guild info |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getdiscordscheduledevent"></a>
# **GetDiscordScheduledEvent**
> CreateDiscordScheduledEvent200Response GetDiscordScheduledEvent (string guildId, string eventId, string accountId)

Get a Discord scheduled event

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
    public class GetDiscordScheduledEventExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var guildId = "guildId_example";  // string | 
            var eventId = "eventId_example";  // string | 
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get a Discord scheduled event
                CreateDiscordScheduledEvent200Response result = apiInstance.GetDiscordScheduledEvent(guildId, eventId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.GetDiscordScheduledEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDiscordScheduledEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a Discord scheduled event
    ApiResponse<CreateDiscordScheduledEvent200Response> response = apiInstance.GetDiscordScheduledEventWithHttpInfo(guildId, eventId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.GetDiscordScheduledEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **guildId** | **string** |  |  |
| **eventId** | **string** |  |  |
| **accountId** | **string** |  |  |

### Return type

[**CreateDiscordScheduledEvent200Response**](CreateDiscordScheduledEvent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Event. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Event or Discord account not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getdiscordsettings"></a>
# **GetDiscordSettings**
> GetDiscordSettings200Response GetDiscordSettings (string accountId)

Get Discord account settings

Returns the current Discord account settings including webhook identity (display name and avatar), connected channel, and guild information.

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
    public class GetDiscordSettingsExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get Discord account settings
                GetDiscordSettings200Response result = apiInstance.GetDiscordSettings(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.GetDiscordSettings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDiscordSettingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Discord account settings
    ApiResponse<GetDiscordSettings200Response> response = apiInstance.GetDiscordSettingsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.GetDiscordSettingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetDiscordSettings200Response**](GetDiscordSettings200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Discord account settings |  -  |
| **400** | Not a Discord account |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listdiscordguildmembers"></a>
# **ListDiscordGuildMembers**
> ListDiscordGuildMembers200Response ListDiscordGuildMembers (string guildId, string accountId, int? limit = null, string? after = null)

List Discord guild members

Cursor-paginated list of guild members. Returns Discord's raw member objects so callers can build community-ops automation (e.g. \"add role to all members joined in the last 7 days\") on the actual platform shape.  **Important:** this endpoint requires the privileged \"Server Members Intent\" enabled on the Discord app (Developer Portal → Bot tab → toggle \"Server Members Intent\" ON, then Save). Without it, Discord returns an empty array with no error. Verify the intent is enabled before relying on this endpoint.  Pagination: pass `after` = the last `user.id` from the previous page. Omit on the first call. Response includes a `nextCursor` and `hasMore` flag so callers don't need to know Discord's pagination shape. 

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
    public class ListDiscordGuildMembersExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var guildId = "guildId_example";  // string | 
            var accountId = "accountId_example";  // string | 
            var limit = 100;  // int? | Page size (1-1000). (optional)  (default to 100)
            var after = "after_example";  // string? | Snowflake of the last member from the previous page. (optional) 

            try
            {
                // List Discord guild members
                ListDiscordGuildMembers200Response result = apiInstance.ListDiscordGuildMembers(guildId, accountId, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.ListDiscordGuildMembers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListDiscordGuildMembersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Discord guild members
    ApiResponse<ListDiscordGuildMembers200Response> response = apiInstance.ListDiscordGuildMembersWithHttpInfo(guildId, accountId, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.ListDiscordGuildMembersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **guildId** | **string** |  |  |
| **accountId** | **string** |  |  |
| **limit** | **int?** | Page size (1-1000). | [optional] [default to 100] |
| **after** | **string?** | Snowflake of the last member from the previous page. | [optional]  |

### Return type

[**ListDiscordGuildMembers200Response**](ListDiscordGuildMembers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of guild members. |  -  |
| **400** | Invalid query params. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Discord account not found or not in this guild. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listdiscordguildroles"></a>
# **ListDiscordGuildRoles**
> ListDiscordGuildRoles200Response ListDiscordGuildRoles (string guildId, string accountId)

List Discord guild roles

Returns all roles in a Discord guild. Useful for building role-mention pickers, role-permission UIs, or finding the role ID before calling the role-assign endpoint.  Roles are returned unordered — sort client-side by `position` if you need Discord's UI ordering.  Caller must pass `accountId` of a Discord SocialAccount bound to this guild (route verifies team access + guild match). 

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
    public class ListDiscordGuildRolesExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var guildId = "guildId_example";  // string | Discord guild snowflake ID
            var accountId = "accountId_example";  // string | SocialAccount _id of the Discord account bound to this guild

            try
            {
                // List Discord guild roles
                ListDiscordGuildRoles200Response result = apiInstance.ListDiscordGuildRoles(guildId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.ListDiscordGuildRoles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListDiscordGuildRolesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Discord guild roles
    ApiResponse<ListDiscordGuildRoles200Response> response = apiInstance.ListDiscordGuildRolesWithHttpInfo(guildId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.ListDiscordGuildRolesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **guildId** | **string** | Discord guild snowflake ID |  |
| **accountId** | **string** | SocialAccount _id of the Discord account bound to this guild |  |

### Return type

[**ListDiscordGuildRoles200Response**](ListDiscordGuildRoles200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of guild roles. |  -  |
| **400** | Invalid accountId or guildId format. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Discord account not found, not accessible, or not bound to this guild. |  -  |
| **502** | Discord rejected the request (bot lacks View Channels permission in the guild). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listdiscordpinnedmessages"></a>
# **ListDiscordPinnedMessages**
> ListDiscordPinnedMessages200Response ListDiscordPinnedMessages (string channelId, string accountId)

List pinned messages in a Discord channel

Returns the channel's pinned messages, sorted most-recently-pinned first. Discord caps a channel at 50 pinned messages and returns the full list unpaginated.  Bot needs READ_MESSAGE_HISTORY in the channel (granted by default BOT_PERMISSIONS). 

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
    public class ListDiscordPinnedMessagesExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var channelId = "channelId_example";  // string | Discord channel snowflake.
            var accountId = "accountId_example";  // string | SocialAccount _id of any Discord account in the same guild.

            try
            {
                // List pinned messages in a Discord channel
                ListDiscordPinnedMessages200Response result = apiInstance.ListDiscordPinnedMessages(channelId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.ListDiscordPinnedMessages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListDiscordPinnedMessagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List pinned messages in a Discord channel
    ApiResponse<ListDiscordPinnedMessages200Response> response = apiInstance.ListDiscordPinnedMessagesWithHttpInfo(channelId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.ListDiscordPinnedMessagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **channelId** | **string** | Discord channel snowflake. |  |
| **accountId** | **string** | SocialAccount _id of any Discord account in the same guild. |  |

### Return type

[**ListDiscordPinnedMessages200Response**](ListDiscordPinnedMessages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pinned messages. |  -  |
| **400** | Invalid channelId or accountId format. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Discord account not found or not accessible. |  -  |
| **502** | Bot lacks access to the channel. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listdiscordscheduledevents"></a>
# **ListDiscordScheduledEvents**
> ListDiscordScheduledEvents200Response ListDiscordScheduledEvents (string guildId, string accountId, bool? withUserCount = null)

List Discord scheduled events

Return all scheduled events in the guild. Events are distinct from messages — they appear in the server's Events panel and Discord auto-notifies interested members ahead of start time.  Pass `withUserCount=true` to include `user_count` (number of members who RSVP'd) on each event. Useful for surfacing engagement. 

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
    public class ListDiscordScheduledEventsExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var guildId = "guildId_example";  // string | 
            var accountId = "accountId_example";  // string | 
            var withUserCount = true;  // bool? | Include user_count on each event. (optional) 

            try
            {
                // List Discord scheduled events
                ListDiscordScheduledEvents200Response result = apiInstance.ListDiscordScheduledEvents(guildId, accountId, withUserCount);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.ListDiscordScheduledEvents: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListDiscordScheduledEventsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Discord scheduled events
    ApiResponse<ListDiscordScheduledEvents200Response> response = apiInstance.ListDiscordScheduledEventsWithHttpInfo(guildId, accountId, withUserCount);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.ListDiscordScheduledEventsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **guildId** | **string** |  |  |
| **accountId** | **string** |  |  |
| **withUserCount** | **bool?** | Include user_count on each event. | [optional]  |

### Return type

[**ListDiscordScheduledEvents200Response**](ListDiscordScheduledEvents200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of scheduled events. |  -  |
| **400** | Invalid params. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Discord account not found or not in this guild. |  -  |
| **502** | Bot lacks access to the guild&#39;s events. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="pindiscordmessage"></a>
# **PinDiscordMessage**
> PinDiscordMessage200Response PinDiscordMessage (string channelId, string messageId, string accountId)

Pin a Discord message

Pin a specific message in a channel. Path shape mirrors Discord's own API (`PUT /channels/{cid}/pins/{mid}`).  Idempotent — re-pinning an already-pinned message is a 204 no-op.  Constraints:   - Bot needs MANAGE_MESSAGES in the channel.   - 50-pin cap per channel — hitting it returns 400 (Discord-side).     Caller should unpin one first. 

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
    public class PinDiscordMessageExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var channelId = "channelId_example";  // string | 
            var messageId = "messageId_example";  // string | 
            var accountId = "accountId_example";  // string | 

            try
            {
                // Pin a Discord message
                PinDiscordMessage200Response result = apiInstance.PinDiscordMessage(channelId, messageId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.PinDiscordMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PinDiscordMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pin a Discord message
    ApiResponse<PinDiscordMessage200Response> response = apiInstance.PinDiscordMessageWithHttpInfo(channelId, messageId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.PinDiscordMessageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **channelId** | **string** |  |  |
| **messageId** | **string** |  |  |
| **accountId** | **string** |  |  |

### Return type

[**PinDiscordMessage200Response**](PinDiscordMessage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Message pinned (or was already pinned — idempotent). |  -  |
| **400** | Validation error or pin cap (50) reached. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Discord account not found. |  -  |
| **502** | Bot lacks MANAGE_MESSAGES in the channel. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removediscordmemberrole"></a>
# **RemoveDiscordMemberRole**
> RemoveDiscordMemberRole200Response RemoveDiscordMemberRole (string guildId, string userId, string roleId, string accountId)

Remove a role from a guild member

Remove one role from one member. Idempotent — removing a role the member doesn't have returns 204 no-op.  Same permission + hierarchy constraints as the PUT counterpart. 

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
    public class RemoveDiscordMemberRoleExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var guildId = "guildId_example";  // string | 
            var userId = "userId_example";  // string | 
            var roleId = "roleId_example";  // string | 
            var accountId = "accountId_example";  // string | 

            try
            {
                // Remove a role from a guild member
                RemoveDiscordMemberRole200Response result = apiInstance.RemoveDiscordMemberRole(guildId, userId, roleId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.RemoveDiscordMemberRole: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveDiscordMemberRoleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove a role from a guild member
    ApiResponse<RemoveDiscordMemberRole200Response> response = apiInstance.RemoveDiscordMemberRoleWithHttpInfo(guildId, userId, roleId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.RemoveDiscordMemberRoleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **guildId** | **string** |  |  |
| **userId** | **string** |  |  |
| **roleId** | **string** |  |  |
| **accountId** | **string** |  |  |

### Return type

[**RemoveDiscordMemberRole200Response**](RemoveDiscordMemberRole200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Role removed (or was already absent — idempotent). |  -  |
| **400** | Validation error. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Discord account not found or not in this guild. |  -  |
| **502** | Discord rejected the request (permission or hierarchy issue). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="senddiscorddirectmessage"></a>
# **SendDiscordDirectMessage**
> SendDiscordDirectMessage200Response SendDiscordDirectMessage (SendDiscordDirectMessageRequest sendDiscordDirectMessageRequest)

Send a Discord Direct Message

Send a 1:1 Direct Message from the bot to a Discord user (by snowflake ID). Supports the same payload shape as channel posts — content, embeds, media attachments, and TTS.  Constraints (Discord platform limits):   - The bot can only DM users it shares at least one guild with.   - If the recipient has DMs disabled for non-friends, Discord returns 403     (surfaces as a 502 platform error).   - `content` capped at 2,000 chars.   - At least one of `content`, `embeds`, or `attachments` is required.   - The recipient must be identified by Discord snowflake ID (not username).  This is a dedicated endpoint rather than a `POST /v1/posts` variant because DMs are 1:1 operational messages (onboarding, billing reminders, support pings) with a different lifecycle than scheduled channel posts. DMs are not persisted to `Post` / `ExternalPost` and are always sent immediately. 

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
    public class SendDiscordDirectMessageExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var sendDiscordDirectMessageRequest = new SendDiscordDirectMessageRequest(); // SendDiscordDirectMessageRequest | 

            try
            {
                // Send a Discord Direct Message
                SendDiscordDirectMessage200Response result = apiInstance.SendDiscordDirectMessage(sendDiscordDirectMessageRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.SendDiscordDirectMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendDiscordDirectMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send a Discord Direct Message
    ApiResponse<SendDiscordDirectMessage200Response> response = apiInstance.SendDiscordDirectMessageWithHttpInfo(sendDiscordDirectMessageRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.SendDiscordDirectMessageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sendDiscordDirectMessageRequest** | [**SendDiscordDirectMessageRequest**](SendDiscordDirectMessageRequest.md) |  |  |

### Return type

[**SendDiscordDirectMessage200Response**](SendDiscordDirectMessage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | DM sent successfully. |  -  |
| **400** | Validation error (missing required fields, content &gt; 2000 chars, malformed snowflake, or all of content/embeds/attachments missing). |  -  |
| **401** | Unauthorized |  -  |
| **404** | Discord account not found or not accessible to this user. |  -  |
| **502** | Discord rejected the message (most commonly: bot doesn&#39;t share a guild with the recipient, OR the recipient has DMs disabled). Error body contains Discord&#39;s response. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="unpindiscordmessage"></a>
# **UnpinDiscordMessage**
> UnpinDiscordMessage200Response UnpinDiscordMessage (string channelId, string messageId, string accountId)

Unpin a Discord message

Unpin a message. Same MANAGE_MESSAGES permission requirement as pin. Idempotent — unpinning a non-pinned message is a 204 no-op. 

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
    public class UnpinDiscordMessageExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var channelId = "channelId_example";  // string | 
            var messageId = "messageId_example";  // string | 
            var accountId = "accountId_example";  // string | 

            try
            {
                // Unpin a Discord message
                UnpinDiscordMessage200Response result = apiInstance.UnpinDiscordMessage(channelId, messageId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.UnpinDiscordMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UnpinDiscordMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Unpin a Discord message
    ApiResponse<UnpinDiscordMessage200Response> response = apiInstance.UnpinDiscordMessageWithHttpInfo(channelId, messageId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.UnpinDiscordMessageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **channelId** | **string** |  |  |
| **messageId** | **string** |  |  |
| **accountId** | **string** |  |  |

### Return type

[**UnpinDiscordMessage200Response**](UnpinDiscordMessage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Message unpinned (or was not pinned — idempotent). |  -  |
| **400** | Validation error. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Discord account not found. |  -  |
| **502** | Bot lacks MANAGE_MESSAGES in the channel. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatediscordscheduledevent"></a>
# **UpdateDiscordScheduledEvent**
> CreateDiscordScheduledEvent200Response UpdateDiscordScheduledEvent (string guildId, string eventId, UpdateDiscordScheduledEventRequest updateDiscordScheduledEventRequest)

Update a Discord scheduled event

Patch any subset of fields. Passing `status: 'cancelled'` is how you cancel an event — Discord doesn't have a dedicated cancel endpoint, it's a status transition.  Most status transitions Discord enforces (you can't go SCHEDULED → COMPLETED directly). The common consumer case is SCHEDULED → CANCELED. 

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
    public class UpdateDiscordScheduledEventExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var guildId = "guildId_example";  // string | 
            var eventId = "eventId_example";  // string | 
            var updateDiscordScheduledEventRequest = new UpdateDiscordScheduledEventRequest(); // UpdateDiscordScheduledEventRequest | 

            try
            {
                // Update a Discord scheduled event
                CreateDiscordScheduledEvent200Response result = apiInstance.UpdateDiscordScheduledEvent(guildId, eventId, updateDiscordScheduledEventRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.UpdateDiscordScheduledEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateDiscordScheduledEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a Discord scheduled event
    ApiResponse<CreateDiscordScheduledEvent200Response> response = apiInstance.UpdateDiscordScheduledEventWithHttpInfo(guildId, eventId, updateDiscordScheduledEventRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.UpdateDiscordScheduledEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **guildId** | **string** |  |  |
| **eventId** | **string** |  |  |
| **updateDiscordScheduledEventRequest** | [**UpdateDiscordScheduledEventRequest**](UpdateDiscordScheduledEventRequest.md) |  |  |

### Return type

[**CreateDiscordScheduledEvent200Response**](CreateDiscordScheduledEvent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Event updated. |  -  |
| **400** | Validation error, OR no updatable fields beyond accountId provided. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Event or Discord account not found. |  -  |
| **502** | Discord rejected the update (invalid status transition, bot permissions, etc.). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatediscordsettings"></a>
# **UpdateDiscordSettings**
> UpdateDiscordSettings200Response UpdateDiscordSettings (string accountId, UpdateDiscordSettingsRequest updateDiscordSettingsRequest)

Update Discord settings

Update Discord account settings. Supports two operations (can be combined):  1. **Webhook identity** - Set the default display name and avatar that appear as the message author on every post. These are account-level defaults; individual posts can override them via platformSpecificData.webhookUsername / webhookAvatarUrl.  2. **Switch channel** - Move the connection to a different channel in the same guild. A new webhook is automatically created in the target channel. 

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
    public class UpdateDiscordSettingsExample
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
            var apiInstance = new DiscordApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var updateDiscordSettingsRequest = new UpdateDiscordSettingsRequest(); // UpdateDiscordSettingsRequest | 

            try
            {
                // Update Discord settings
                UpdateDiscordSettings200Response result = apiInstance.UpdateDiscordSettings(accountId, updateDiscordSettingsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordApi.UpdateDiscordSettings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateDiscordSettingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Discord settings
    ApiResponse<UpdateDiscordSettings200Response> response = apiInstance.UpdateDiscordSettingsWithHttpInfo(accountId, updateDiscordSettingsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordApi.UpdateDiscordSettingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **updateDiscordSettingsRequest** | [**UpdateDiscordSettingsRequest**](UpdateDiscordSettingsRequest.md) |  |  |

### Return type

[**UpdateDiscordSettings200Response**](UpdateDiscordSettings200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Settings updated |  -  |
| **400** | Invalid request (no changes, invalid channel type, or bot cannot access channel) |  -  |
| **401** | Unauthorized |  -  |
| **404** | Discord account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

