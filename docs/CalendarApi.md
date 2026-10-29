# Zernio.Api.CalendarApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CalendarAvailability**](CalendarApi.md#calendaravailability) | **POST** /v1/calendar/availability | Find meeting slots across accounts |
| [**CalendarFreeBusy**](CalendarApi.md#calendarfreebusy) | **POST** /v1/calendar/free-busy | Busy blocks for one or more accounts |
| [**CreateCalendarEvent**](CalendarApi.md#createcalendarevent) | **POST** /v1/calendar/events | Create an event |
| [**DeleteCalendarEvent**](CalendarApi.md#deletecalendarevent) | **DELETE** /v1/calendar/events/{eventId} | Delete an event |
| [**GetCalendarEvent**](CalendarApi.md#getcalendarevent) | **GET** /v1/calendar/events/{eventId} | Get an event |
| [**ListCalendarEvents**](CalendarApi.md#listcalendarevents) | **GET** /v1/calendar/events | List events in a window |
| [**ListCalendars**](CalendarApi.md#listcalendars) | **GET** /v1/calendar/calendars | List calendars |
| [**RsvpCalendarEvent**](CalendarApi.md#rsvpcalendarevent) | **POST** /v1/calendar/events/{eventId}/rsvp | Respond to an invitation |
| [**UpdateCalendarEvent**](CalendarApi.md#updatecalendarevent) | **PATCH** /v1/calendar/events/{eventId} | Update an event |

<a id="calendaravailability"></a>
# **CalendarAvailability**
> CalendarAvailability200Response CalendarAvailability (CalendarAvailabilityRequest calendarAvailabilityRequest)

Find meeting slots across accounts

Slots of `durationMinutes` every `intervalMinutes` between `from` and `to` that are free for every participant (`collective`) or for at least one (`max_availability`). Buffers pad the participants' existing meetings. Open hours are evaluated in each participant's own timezone; `defaultOpenHours` applies to participants without their own.

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
    public class CalendarAvailabilityExample
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
            var apiInstance = new CalendarApi(httpClient, config, httpClientHandler);
            var calendarAvailabilityRequest = new CalendarAvailabilityRequest(); // CalendarAvailabilityRequest | 

            try
            {
                // Find meeting slots across accounts
                CalendarAvailability200Response result = apiInstance.CalendarAvailability(calendarAvailabilityRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CalendarApi.CalendarAvailability: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CalendarAvailabilityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Find meeting slots across accounts
    ApiResponse<CalendarAvailability200Response> response = apiInstance.CalendarAvailabilityWithHttpInfo(calendarAvailabilityRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CalendarApi.CalendarAvailabilityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **calendarAvailabilityRequest** | [**CalendarAvailabilityRequest**](CalendarAvailabilityRequest.md) |  |  |

### Return type

[**CalendarAvailability200Response**](CalendarAvailability200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Candidate slots |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="calendarfreebusy"></a>
# **CalendarFreeBusy**
> CalendarFreeBusy200Response CalendarFreeBusy (CalendarFreeBusyRequest calendarFreeBusyRequest)

Busy blocks for one or more accounts

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
    public class CalendarFreeBusyExample
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
            var apiInstance = new CalendarApi(httpClient, config, httpClientHandler);
            var calendarFreeBusyRequest = new CalendarFreeBusyRequest(); // CalendarFreeBusyRequest | 

            try
            {
                // Busy blocks for one or more accounts
                CalendarFreeBusy200Response result = apiInstance.CalendarFreeBusy(calendarFreeBusyRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CalendarApi.CalendarFreeBusy: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CalendarFreeBusyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Busy blocks for one or more accounts
    ApiResponse<CalendarFreeBusy200Response> response = apiInstance.CalendarFreeBusyWithHttpInfo(calendarFreeBusyRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CalendarApi.CalendarFreeBusyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **calendarFreeBusyRequest** | [**CalendarFreeBusyRequest**](CalendarFreeBusyRequest.md) |  |  |

### Return type

[**CalendarFreeBusy200Response**](CalendarFreeBusy200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One entry per account, busy blocks in UTC |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcalendarevent"></a>
# **CreateCalendarEvent**
> CreateCalendarEvent201Response CreateCalendarEvent (CreateCalendarEventRequest createCalendarEventRequest)

Create an event

Creates a calendar event. Conferencing and recurrence behave differently on Microsoft and Google accounts.  ### Microsoft accounts  - `conferencing: teams` adds a Teams meeting. The created event comes back with `conferencing: null` when the tenant has no Teams (the EEA Business Basic SKUs ship without it). - `google_meet` is rejected with 400 (`param: conferencing`).  ### Google accounts  - `conferencing: google_meet` adds a Meet link. - `teams` is rejected with 400. - `recurrence` accepts any RRULE Google Calendar supports.  ### Recurrence  `recurrence` takes one RRULE line with FREQ, INTERVAL, COUNT, UNTIL, BYDAY and BYSETPOS. Other parts are rejected with 400 (`param: recurrence`). 

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
    public class CreateCalendarEventExample
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
            var apiInstance = new CalendarApi(httpClient, config, httpClientHandler);
            var createCalendarEventRequest = new CreateCalendarEventRequest(); // CreateCalendarEventRequest | 

            try
            {
                // Create an event
                CreateCalendarEvent201Response result = apiInstance.CreateCalendarEvent(createCalendarEventRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CalendarApi.CreateCalendarEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCalendarEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create an event
    ApiResponse<CreateCalendarEvent201Response> response = apiInstance.CreateCalendarEventWithHttpInfo(createCalendarEventRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CalendarApi.CreateCalendarEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCalendarEventRequest** | [**CreateCalendarEventRequest**](CreateCalendarEventRequest.md) |  |  |

### Return type

[**CreateCalendarEvent201Response**](CreateCalendarEvent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The created event |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletecalendarevent"></a>
# **DeleteCalendarEvent**
> DeleteCalendarEvent200Response DeleteCalendarEvent (string eventId, string accountId, string? calendarId = null)

Delete an event

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
    public class DeleteCalendarEventExample
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
            var apiInstance = new CalendarApi(httpClient, config, httpClientHandler);
            var eventId = "eventId_example";  // string | 
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.
            var calendarId = "calendarId_example";  // string? | The calendar holding the event (an id from GET /v1/calendar/calendars). Defaults to the primary calendar. (optional) 

            try
            {
                // Delete an event
                DeleteCalendarEvent200Response result = apiInstance.DeleteCalendarEvent(eventId, accountId, calendarId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CalendarApi.DeleteCalendarEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCalendarEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete an event
    ApiResponse<DeleteCalendarEvent200Response> response = apiInstance.DeleteCalendarEventWithHttpInfo(eventId, accountId, calendarId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CalendarApi.DeleteCalendarEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **eventId** | **string** |  |  |
| **accountId** | **string** | The connected Google or Microsoft account. |  |
| **calendarId** | **string?** | The calendar holding the event (an id from GET /v1/calendar/calendars). Defaults to the primary calendar. | [optional]  |

### Return type

[**DeleteCalendarEvent200Response**](DeleteCalendarEvent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcalendarevent"></a>
# **GetCalendarEvent**
> CreateCalendarEvent201Response GetCalendarEvent (string eventId, string accountId, string? calendarId = null, string? timezone = null)

Get an event

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
    public class GetCalendarEventExample
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
            var apiInstance = new CalendarApi(httpClient, config, httpClientHandler);
            var eventId = "eventId_example";  // string | 
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.
            var calendarId = "calendarId_example";  // string? | The calendar holding the event (an id from GET /v1/calendar/calendars). Defaults to the primary calendar. (optional) 
            var timezone = "timezone_example";  // string? |  (optional) 

            try
            {
                // Get an event
                CreateCalendarEvent201Response result = apiInstance.GetCalendarEvent(eventId, accountId, calendarId, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CalendarApi.GetCalendarEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCalendarEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an event
    ApiResponse<CreateCalendarEvent201Response> response = apiInstance.GetCalendarEventWithHttpInfo(eventId, accountId, calendarId, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CalendarApi.GetCalendarEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **eventId** | **string** |  |  |
| **accountId** | **string** | The connected Google or Microsoft account. |  |
| **calendarId** | **string?** | The calendar holding the event (an id from GET /v1/calendar/calendars). Defaults to the primary calendar. | [optional]  |
| **timezone** | **string?** |  | [optional]  |

### Return type

[**CreateCalendarEvent201Response**](CreateCalendarEvent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The event |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcalendarevents"></a>
# **ListCalendarEvents**
> ListCalendarEvents200Response ListCalendarEvents (string accountId, DateTime from, DateTime to, string? calendarId = null, string? title = null, string? location = null, bool? showCancelled = null, bool? expandRecurring = null, string? icalUid = null, string? sortOrder = null, string? cursor = null, int? limit = null, string? timezone = null)

List events in a window

Recurring series are expanded into their occurrences inside the window by default (`expandRecurring=false` lists the masters instead). `title` and `location` are substring matches applied to the fetched page.

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
    public class ListCalendarEventsExample
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
            var apiInstance = new CalendarApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.
            var from = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var to = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var calendarId = "calendarId_example";  // string? | Defaults to the primary calendar. (optional) 
            var title = "title_example";  // string? |  (optional) 
            var location = "location_example";  // string? |  (optional) 
            var showCancelled = false;  // bool? |  (optional)  (default to false)
            var expandRecurring = true;  // bool? |  (optional)  (default to true)
            var icalUid = "icalUid_example";  // string? |  (optional) 
            var sortOrder = "asc";  // string? |  (optional)  (default to asc)
            var cursor = "cursor_example";  // string? |  (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var timezone = "timezone_example";  // string? | IANA zone the `start` and `end` offsets are rendered in. Default UTC. (optional) 

            try
            {
                // List events in a window
                ListCalendarEvents200Response result = apiInstance.ListCalendarEvents(accountId, from, to, calendarId, title, location, showCancelled, expandRecurring, icalUid, sortOrder, cursor, limit, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CalendarApi.ListCalendarEvents: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCalendarEventsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List events in a window
    ApiResponse<ListCalendarEvents200Response> response = apiInstance.ListCalendarEventsWithHttpInfo(accountId, from, to, calendarId, title, location, showCancelled, expandRecurring, icalUid, sortOrder, cursor, limit, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CalendarApi.ListCalendarEventsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected Google or Microsoft account. |  |
| **from** | **DateTime** |  |  |
| **to** | **DateTime** |  |  |
| **calendarId** | **string?** | Defaults to the primary calendar. | [optional]  |
| **title** | **string?** |  | [optional]  |
| **location** | **string?** |  | [optional]  |
| **showCancelled** | **bool?** |  | [optional] [default to false] |
| **expandRecurring** | **bool?** |  | [optional] [default to true] |
| **icalUid** | **string?** |  | [optional]  |
| **sortOrder** | **string?** |  | [optional] [default to asc] |
| **cursor** | **string?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **timezone** | **string?** | IANA zone the &#x60;start&#x60; and &#x60;end&#x60; offsets are rendered in. Default UTC. | [optional]  |

### Return type

[**ListCalendarEvents200Response**](ListCalendarEvents200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Events |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted. Behavior per platform:  - **Reddit:** rate-limits per connected Reddit user (1000 requests per 10-minute window), shared by every operation on that account. Retry after the window resets; repeated calls while exhausted do not succeed and keep the budget spent. - **Google Ads:** writes and reports run on one developer token shared by every Google Ads account on Zernio. It holds Standard access (no daily operations cap), so this only happens when Google throttles the token or your ad account. - **Google Ads envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60; (&#x60;ACCOUNT&#x60; when it is your own ad account&#39;s quota), &#x60;details.resetsAt&#x60; (ISO instant when Google accepts requests again) and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **YouTube Analytics:** reads (channel-insights, demographics, daily-views, video-retention) use the \&quot;Queries per day\&quot; quota of the Google Cloud project the account is connected through, shared with other Zernio customers, so a 429 is not your own volume. Resets at midnight Pacific Time. - **YouTube Analytics envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaExhausted: true&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60;, &#x60;details.resetsAt&#x60; and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **Meta ads:** every Meta throttle (codes 4, 17, 32, 613 and business-use-case codes 80000-80014) returns 429 &#x60;rate_limited&#x60;, even when Meta answers HTTP 400. &#x60;Retry-After&#x60; comes from Meta&#39;s &#x60;x-business-use-case-usage&#x60; estimate when sent, else Meta&#39;s 60-second minimum (30 seconds for the one-write-per-30-seconds limit on one object). - **Pinterest ads:** limits per user and app, per category (ads_read, ads_write, ads_analytics). &#x60;Retry-After&#x60; comes from Pinterest&#39;s &#x60;x-ratelimit-reset&#x60; when sent, otherwise 60 seconds. - **TikTok ads:** limits per app and per endpoint (per second, minute and day), answering overage with code 40100 or code 40002 &#x60;OVER_QPS_LIMIT&#x60;. Both return 429 &#x60;rate_limited&#x60; with &#x60;platform: tiktok&#x60; and &#x60;Retry-After: 10&#x60;. Space out bulk reads (e.g. one ad at a time per advertiser) instead of retrying at once.  **TikTok Smart+ review read** (&#x60;GET /v1/ads/{adId}/tiktok-smart-plus-review&#x60;) has its own stricter TikTok quota. After an overage, Zernio answers 429 for that advertiser and connection without calling TikTok for about 60 seconds, then 120, up to 240 while TikTok keeps refusing, each with up to 10% random jitter.  A successful call holds nothing back; the next overage pauses about 60 seconds again. &#x60;Retry-After&#x60; is the time left. The advertiser-wide read (&#x60;GET /v1/ads/tiktok-smart-plus-reviews&#x60;) answers 200 with &#x60;retryAfterSeconds&#x60; and &#x60;refreshState&#x60; instead. Keep one request in flight per advertiser there.  |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcalendars"></a>
# **ListCalendars**
> ListCalendars200Response ListCalendars (string accountId)

List calendars

The account must have been connected with `scopes=calendar` (412 `account_scope_missing` otherwise).

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
    public class ListCalendarsExample
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
            var apiInstance = new CalendarApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected Google or Microsoft account.

            try
            {
                // List calendars
                ListCalendars200Response result = apiInstance.ListCalendars(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CalendarApi.ListCalendars: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCalendarsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List calendars
    ApiResponse<ListCalendars200Response> response = apiInstance.ListCalendarsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CalendarApi.ListCalendarsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected Google or Microsoft account. |  |

### Return type

[**ListCalendars200Response**](ListCalendars200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Calendars |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="rsvpcalendarevent"></a>
# **RsvpCalendarEvent**
> CreateCalendarEvent201Response RsvpCalendarEvent (string eventId, RsvpCalendarEventRequest rsvpCalendarEventRequest)

Respond to an invitation

Accepts, declines or tentatively accepts on behalf of the mailbox and notifies the organizer.

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
    public class RsvpCalendarEventExample
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
            var apiInstance = new CalendarApi(httpClient, config, httpClientHandler);
            var eventId = "eventId_example";  // string | 
            var rsvpCalendarEventRequest = new RsvpCalendarEventRequest(); // RsvpCalendarEventRequest | 

            try
            {
                // Respond to an invitation
                CreateCalendarEvent201Response result = apiInstance.RsvpCalendarEvent(eventId, rsvpCalendarEventRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CalendarApi.RsvpCalendarEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RsvpCalendarEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Respond to an invitation
    ApiResponse<CreateCalendarEvent201Response> response = apiInstance.RsvpCalendarEventWithHttpInfo(eventId, rsvpCalendarEventRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CalendarApi.RsvpCalendarEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **eventId** | **string** |  |  |
| **rsvpCalendarEventRequest** | [**RsvpCalendarEventRequest**](RsvpCalendarEventRequest.md) |  |  |

### Return type

[**CreateCalendarEvent201Response**](CreateCalendarEvent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The event after the response |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecalendarevent"></a>
# **UpdateCalendarEvent**
> CreateCalendarEvent201Response UpdateCalendarEvent (string eventId, UpdateCalendarEventRequest updateCalendarEventRequest)

Update an event

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
    public class UpdateCalendarEventExample
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
            var apiInstance = new CalendarApi(httpClient, config, httpClientHandler);
            var eventId = "eventId_example";  // string | 
            var updateCalendarEventRequest = new UpdateCalendarEventRequest(); // UpdateCalendarEventRequest | 

            try
            {
                // Update an event
                CreateCalendarEvent201Response result = apiInstance.UpdateCalendarEvent(eventId, updateCalendarEventRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CalendarApi.UpdateCalendarEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCalendarEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update an event
    ApiResponse<CreateCalendarEvent201Response> response = apiInstance.UpdateCalendarEventWithHttpInfo(eventId, updateCalendarEventRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CalendarApi.UpdateCalendarEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **eventId** | **string** |  |  |
| **updateCalendarEventRequest** | [**UpdateCalendarEventRequest**](UpdateCalendarEventRequest.md) |  |  |

### Return type

[**CreateCalendarEvent201Response**](CreateCalendarEvent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated event |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **412** | The connected account cannot serve this request until something outside the request changes. Two codes:  - &#x60;account_scope_missing&#x60;: the account was connected without the area this endpoint needs (&#x60;details.grantedAreas&#x60;, &#x60;details.missingArea&#x60;), or Google reports the grant lacks a permission. Reconnect with a wider &#x60;scopes&#x3D;&#x60;. - &#x60;admin_consent_required&#x60; (Microsoft): the tenant requires an administrator&#39;s approval. &#x60;details.adminConsentUrl&#x60; is the Microsoft Entra admin-consent link to hand to one; it opens in a browser with no API key and stays valid for one hour. &#x60;GET /v1/connect/microsoft/admin-consent&#x60; mints a fresh one.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

