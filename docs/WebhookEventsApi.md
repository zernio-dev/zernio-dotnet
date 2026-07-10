# Zernio.Api.WebhookEventsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**OnAccountAdsInitialSyncCompleted**](WebhookEventsApi.md#onaccountadsinitialsynccompleted) | **POST** /account.ads.initial_sync_completed | Ads initial sync completed event |
| [**OnAccountConnected**](WebhookEventsApi.md#onaccountconnected) | **POST** /account.connected | Account connected event |
| [**OnAccountDisconnected**](WebhookEventsApi.md#onaccountdisconnected) | **POST** /account.disconnected | Account disconnected event |
| [**OnAdStatusChanged**](WebhookEventsApi.md#onadstatuschanged) | **POST** /ad.status_changed | Ad status changed event |
| [**OnCallEnded**](WebhookEventsApi.md#oncallended) | **POST** /call.ended | Call ended event |
| [**OnCallFailed**](WebhookEventsApi.md#oncallfailed) | **POST** /call.failed | Call failed event |
| [**OnCallPermissionRequest**](WebhookEventsApi.md#oncallpermissionrequest) | **POST** /call.permission_request | Call permission request reply event |
| [**OnCallReceived**](WebhookEventsApi.md#oncallreceived) | **POST** /call.received | Call received event |
| [**OnCommentReceived**](WebhookEventsApi.md#oncommentreceived) | **POST** /comment.received | Comment received event |
| [**OnConversationStarted**](WebhookEventsApi.md#onconversationstarted) | **POST** /conversation.started | Conversation started event |
| [**OnLeadReceived**](WebhookEventsApi.md#onleadreceived) | **POST** /lead.received | Lead received event |
| [**OnMessageDeleted**](WebhookEventsApi.md#onmessagedeleted) | **POST** /message.deleted | Message deleted event |
| [**OnMessageDelivered**](WebhookEventsApi.md#onmessagedelivered) | **POST** /message.delivered | Message delivered event |
| [**OnMessageEdited**](WebhookEventsApi.md#onmessageedited) | **POST** /message.edited | Message edited event |
| [**OnMessageFailed**](WebhookEventsApi.md#onmessagefailed) | **POST** /message.failed | Message delivery failed event |
| [**OnMessageRead**](WebhookEventsApi.md#onmessageread) | **POST** /message.read | Message read event |
| [**OnMessageReceived**](WebhookEventsApi.md#onmessagereceived) | **POST** /message.received | Message received event |
| [**OnMessageSent**](WebhookEventsApi.md#onmessagesent) | **POST** /message.sent | Message sent event |
| [**OnPostCancelled**](WebhookEventsApi.md#onpostcancelled) | **POST** /post.cancelled | Post cancelled event |
| [**OnPostExternalCreated**](WebhookEventsApi.md#onpostexternalcreated) | **POST** /post.external.created | External post created event |
| [**OnPostExternalDeleted**](WebhookEventsApi.md#onpostexternaldeleted) | **POST** /post.external.deleted | External post deleted event |
| [**OnPostExternalUpdated**](WebhookEventsApi.md#onpostexternalupdated) | **POST** /post.external.updated | External post updated event |
| [**OnPostFailed**](WebhookEventsApi.md#onpostfailed) | **POST** /post.failed | Post failed event |
| [**OnPostPartial**](WebhookEventsApi.md#onpostpartial) | **POST** /post.partial | Post partial event |
| [**OnPostPlatformFailed**](WebhookEventsApi.md#onpostplatformfailed) | **POST** /post.platform.failed | Post platform failed event |
| [**OnPostPlatformPublished**](WebhookEventsApi.md#onpostplatformpublished) | **POST** /post.platform.published | Post platform published event |
| [**OnPostPublished**](WebhookEventsApi.md#onpostpublished) | **POST** /post.published | Post published event |
| [**OnPostRecycled**](WebhookEventsApi.md#onpostrecycled) | **POST** /post.recycled | Post recycled event |
| [**OnPostScheduled**](WebhookEventsApi.md#onpostscheduled) | **POST** /post.scheduled | Post scheduled event |
| [**OnPostTikTokUrlResolved**](WebhookEventsApi.md#onposttiktokurlresolved) | **POST** /post.tiktok.url_resolved | TikTok post URL resolved event |
| [**OnReactionReceived**](WebhookEventsApi.md#onreactionreceived) | **POST** /reaction.received | Reaction received event |
| [**OnReviewNew**](WebhookEventsApi.md#onreviewnew) | **POST** /review.new | Review new event |
| [**OnReviewUpdated**](WebhookEventsApi.md#onreviewupdated) | **POST** /review.updated | Review updated event |
| [**OnWebhookTest**](WebhookEventsApi.md#onwebhooktest) | **POST** /webhook.test | Webhook test event |
| [**OnWhatsAppAutomaticEvent**](WebhookEventsApi.md#onwhatsappautomaticevent) | **POST** /whatsapp.automatic_event | WhatsApp automatic event detected |
| [**OnWhatsAppNumberActionRequired**](WebhookEventsApi.md#onwhatsappnumberactionrequired) | **POST** /whatsapp.number.action_required | WhatsApp number action required event |
| [**OnWhatsAppNumberActivated**](WebhookEventsApi.md#onwhatsappnumberactivated) | **POST** /whatsapp.number.activated | WhatsApp number activated event |
| [**OnWhatsAppNumberDeclined**](WebhookEventsApi.md#onwhatsappnumberdeclined) | **POST** /whatsapp.number.declined | WhatsApp number declined event |
| [**OnWhatsAppNumberKycSubmitted**](WebhookEventsApi.md#onwhatsappnumberkycsubmitted) | **POST** /whatsapp.number.kyc_submitted | WhatsApp number KYC submitted event |
| [**OnWhatsAppNumberReactivated**](WebhookEventsApi.md#onwhatsappnumberreactivated) | **POST** /whatsapp.number.reactivated | WhatsApp number reactivated event |
| [**OnWhatsAppNumberReleased**](WebhookEventsApi.md#onwhatsappnumberreleased) | **POST** /whatsapp.number.released | WhatsApp number released event |
| [**OnWhatsAppNumberSuspended**](WebhookEventsApi.md#onwhatsappnumbersuspended) | **POST** /whatsapp.number.suspended | WhatsApp number suspended event |
| [**OnWhatsAppNumberVerificationRequired**](WebhookEventsApi.md#onwhatsappnumberverificationrequired) | **POST** /whatsapp.number.verification_required | WhatsApp number verification-required event |
| [**OnWhatsAppTemplateStatusUpdated**](WebhookEventsApi.md#onwhatsapptemplatestatusupdated) | **POST** /whatsapp.template.status_updated | WhatsApp template status updated event |

<a id="onaccountadsinitialsynccompleted"></a>
# **OnAccountAdsInitialSyncCompleted**
> void OnAccountAdsInitialSyncCompleted (WebhookPayloadAccountAdsInitialSyncCompleted webhookPayloadAccountAdsInitialSyncCompleted)

Ads initial sync completed event

Fired once per ads-enabled account when the initial sync (ad-account discovery + 90-day historical ad backfill) completes. The `sync` block reports whether the backfill succeeded and how many ads were synced. 

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
    public class OnAccountAdsInitialSyncCompletedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadAccountAdsInitialSyncCompleted = new WebhookPayloadAccountAdsInitialSyncCompleted(); // WebhookPayloadAccountAdsInitialSyncCompleted | 

            try
            {
                // Ads initial sync completed event
                apiInstance.OnAccountAdsInitialSyncCompleted(webhookPayloadAccountAdsInitialSyncCompleted);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAccountAdsInitialSyncCompleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAccountAdsInitialSyncCompletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ads initial sync completed event
    apiInstance.OnAccountAdsInitialSyncCompletedWithHttpInfo(webhookPayloadAccountAdsInitialSyncCompleted);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAccountAdsInitialSyncCompletedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAccountAdsInitialSyncCompleted** | [**WebhookPayloadAccountAdsInitialSyncCompleted**](WebhookPayloadAccountAdsInitialSyncCompleted.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onaccountconnected"></a>
# **OnAccountConnected**
> void OnAccountConnected (WebhookPayloadAccountConnected webhookPayloadAccountConnected)

Account connected event

Fired when a social account is successfully connected.

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
    public class OnAccountConnectedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadAccountConnected = new WebhookPayloadAccountConnected(); // WebhookPayloadAccountConnected | 

            try
            {
                // Account connected event
                apiInstance.OnAccountConnected(webhookPayloadAccountConnected);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAccountConnected: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAccountConnectedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Account connected event
    apiInstance.OnAccountConnectedWithHttpInfo(webhookPayloadAccountConnected);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAccountConnectedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAccountConnected** | [**WebhookPayloadAccountConnected**](WebhookPayloadAccountConnected.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onaccountdisconnected"></a>
# **OnAccountDisconnected**
> void OnAccountDisconnected (WebhookPayloadAccountDisconnected webhookPayloadAccountDisconnected)

Account disconnected event

Fired when a connected social account becomes disconnected.

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
    public class OnAccountDisconnectedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadAccountDisconnected = new WebhookPayloadAccountDisconnected(); // WebhookPayloadAccountDisconnected | 

            try
            {
                // Account disconnected event
                apiInstance.OnAccountDisconnected(webhookPayloadAccountDisconnected);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAccountDisconnected: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAccountDisconnectedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Account disconnected event
    apiInstance.OnAccountDisconnectedWithHttpInfo(webhookPayloadAccountDisconnected);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAccountDisconnectedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAccountDisconnected** | [**WebhookPayloadAccountDisconnected**](WebhookPayloadAccountDisconnected.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onadstatuschanged"></a>
# **OnAdStatusChanged**
> void OnAdStatusChanged (WebhookPayloadAdStatusChanged webhookPayloadAdStatusChanged)

Ad status changed event

Fired when a campaign, ad set, or ad on a connected ad platform changes status. Currently emitted only for Meta (`metaads`).  Subscribed to two Meta `ad_account` webhook fields:   - `in_process_ad_objects` - the ad object finished processing and exited     the `IN_PROCESS` state. `status.raw` carries Meta's `status_name`     (e.g. `ACTIVE`, `PAUSED`, `ARCHIVED`, `DELETED`).   - `with_issues_ad_objects` - the ad object entered the `WITH_ISSUES`     state. `status.raw` is set to `WITH_ISSUES` and the `error` block is     populated from Meta's `error_code` / `error_summary` / `error_message`.  `adObject.level` mirrors Meta's `level` and is one of `CAMPAIGN`, `AD_SET`, or `AD`. Creative-level events are not forwarded.  Branch on `status.raw` to handle each transition; use `error.code` (when present) as the stable discriminator — `error.summary` and `error.message` are localized to the ad-account owner's Meta locale.  The `error` block is optional. It's present on most `WITH_ISSUES` events but can be absent (Meta does not always include diagnostics), and is never present on any other status. Always null-check `error` before reading `error.code`.  **Fan-out:** matching is keyed on `adObject.platformAdAccountId`. When multiple connected Zernio `metaads` accounts are linked to the same Meta ad account, each receives its own delivery. 

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
    public class OnAdStatusChangedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadAdStatusChanged = new WebhookPayloadAdStatusChanged(); // WebhookPayloadAdStatusChanged | 

            try
            {
                // Ad status changed event
                apiInstance.OnAdStatusChanged(webhookPayloadAdStatusChanged);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAdStatusChanged: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAdStatusChangedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad status changed event
    apiInstance.OnAdStatusChangedWithHttpInfo(webhookPayloadAdStatusChanged);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAdStatusChangedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAdStatusChanged** | [**WebhookPayloadAdStatusChanged**](WebhookPayloadAdStatusChanged.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="oncallended"></a>
# **OnCallEnded**
> void OnCallEnded (WebhookPayloadCallEnded webhookPayloadCallEnded)

Call ended event

Fired on call hangup with the duration and a zero-markup billing breakdown (Meta cost, Telnyx cost, recording surcharge, total). Costs are pass-through; no margin is applied. 

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
    public class OnCallEndedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadCallEnded = new WebhookPayloadCallEnded(); // WebhookPayloadCallEnded | 

            try
            {
                // Call ended event
                apiInstance.OnCallEnded(webhookPayloadCallEnded);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCallEnded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCallEndedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Call ended event
    apiInstance.OnCallEndedWithHttpInfo(webhookPayloadCallEnded);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCallEndedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCallEnded** | [**WebhookPayloadCallEnded**](WebhookPayloadCallEnded.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="oncallfailed"></a>
# **OnCallFailed**
> void OnCallFailed (WebhookPayloadCallFailed webhookPayloadCallFailed)

Call failed event

Fired when a call setup or in-progress call fails (Meta rejected the connect, Telnyx returned an error, etc.). Payload carries the upstream error code and message. 

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
    public class OnCallFailedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadCallFailed = new WebhookPayloadCallFailed(); // WebhookPayloadCallFailed | 

            try
            {
                // Call failed event
                apiInstance.OnCallFailed(webhookPayloadCallFailed);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCallFailed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCallFailedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Call failed event
    apiInstance.OnCallFailedWithHttpInfo(webhookPayloadCallFailed);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCallFailedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCallFailed** | [**WebhookPayloadCallFailed**](WebhookPayloadCallFailed.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="oncallpermissionrequest"></a>
# **OnCallPermissionRequest**
> void OnCallPermissionRequest (WebhookPayloadCallPermissionRequest webhookPayloadCallPermissionRequest)

Call permission request reply event

Fired when a consumer replies to a `call_permission_request` interactive message (or its marketing-template variant). Carries the response (`accept` / `reject`), whether the grant is permanent, and the expiration timestamp when it is temporary. 

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
    public class OnCallPermissionRequestExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadCallPermissionRequest = new WebhookPayloadCallPermissionRequest(); // WebhookPayloadCallPermissionRequest | 

            try
            {
                // Call permission request reply event
                apiInstance.OnCallPermissionRequest(webhookPayloadCallPermissionRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCallPermissionRequest: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCallPermissionRequestWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Call permission request reply event
    apiInstance.OnCallPermissionRequestWithHttpInfo(webhookPayloadCallPermissionRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCallPermissionRequestWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCallPermissionRequest** | [**WebhookPayloadCallPermissionRequest**](WebhookPayloadCallPermissionRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="oncallreceived"></a>
# **OnCallReceived**
> void OnCallReceived (WebhookPayloadCallReceived webhookPayloadCallReceived)

Call received event

Fired when a WhatsApp Business Call connects. For inbound (UIC) calls the event fires at the moment our Telnyx trunk bridges the consumer leg to the customer&apos;s forward-to destination; for outbound (BIC) calls it fires immediately after Meta accepts the connect. Branch on `call.direction` to distinguish. 

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
    public class OnCallReceivedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadCallReceived = new WebhookPayloadCallReceived(); // WebhookPayloadCallReceived | 

            try
            {
                // Call received event
                apiInstance.OnCallReceived(webhookPayloadCallReceived);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCallReceived: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCallReceivedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Call received event
    apiInstance.OnCallReceivedWithHttpInfo(webhookPayloadCallReceived);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCallReceivedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCallReceived** | [**WebhookPayloadCallReceived**](WebhookPayloadCallReceived.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="oncommentreceived"></a>
# **OnCommentReceived**
> void OnCommentReceived (WebhookPayloadComment webhookPayloadComment)

Comment received event

Fired when a new comment is received on a tracked post.

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
    public class OnCommentReceivedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadComment = new WebhookPayloadComment(); // WebhookPayloadComment | 

            try
            {
                // Comment received event
                apiInstance.OnCommentReceived(webhookPayloadComment);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCommentReceived: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCommentReceivedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Comment received event
    apiInstance.OnCommentReceivedWithHttpInfo(webhookPayloadComment);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCommentReceivedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadComment** | [**WebhookPayloadComment**](WebhookPayloadComment.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onconversationstarted"></a>
# **OnConversationStarted**
> void OnConversationStarted (WebhookPayloadConversationStarted webhookPayloadConversationStarted)

Conversation started event

Fired once when a new conversation begins between one of your connected accounts and a contact, in either direction. Works across every DM platform (Instagram, Messenger/Facebook, Telegram, WhatsApp, Twitter, Reddit, Bluesky). Naturally deduped — a given conversation only fires this event the very first time it appears. 

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
    public class OnConversationStartedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadConversationStarted = new WebhookPayloadConversationStarted(); // WebhookPayloadConversationStarted | 

            try
            {
                // Conversation started event
                apiInstance.OnConversationStarted(webhookPayloadConversationStarted);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnConversationStarted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnConversationStartedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Conversation started event
    apiInstance.OnConversationStartedWithHttpInfo(webhookPayloadConversationStarted);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnConversationStartedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadConversationStarted** | [**WebhookPayloadConversationStarted**](WebhookPayloadConversationStarted.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onleadreceived"></a>
# **OnLeadReceived**
> void OnLeadReceived (WebhookPayloadLead webhookPayloadLead)

Lead received event

Fired when a new lead is submitted against a Meta Lead Gen (Instant) Form and ingested via the Page `leadgen` webhook. `lead.fields` is the question-key to answer map; `lead.formId` / `lead.adId` give provenance. Requires the Ads add-on. 

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
    public class OnLeadReceivedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadLead = new WebhookPayloadLead(); // WebhookPayloadLead | 

            try
            {
                // Lead received event
                apiInstance.OnLeadReceived(webhookPayloadLead);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnLeadReceived: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnLeadReceivedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Lead received event
    apiInstance.OnLeadReceivedWithHttpInfo(webhookPayloadLead);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnLeadReceivedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadLead** | [**WebhookPayloadLead**](WebhookPayloadLead.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onmessagedeleted"></a>
# **OnMessageDeleted**
> void OnMessageDeleted (WebhookPayloadMessageDeleted webhookPayloadMessageDeleted)

Message deleted event

Fired when a sender deletes (unsends) a message. Supported on Instagram (incoming unsend) and WhatsApp (when the business deletes an outgoing message via the Cloud API). The payload retains the pre-delete text and attachments so API consumers can access the original content for moderation or compliance — the Zernio dashboard UI hides it. 

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
    public class OnMessageDeletedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadMessageDeleted = new WebhookPayloadMessageDeleted(); // WebhookPayloadMessageDeleted | 

            try
            {
                // Message deleted event
                apiInstance.OnMessageDeleted(webhookPayloadMessageDeleted);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnMessageDeleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnMessageDeletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Message deleted event
    apiInstance.OnMessageDeletedWithHttpInfo(webhookPayloadMessageDeleted);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnMessageDeletedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadMessageDeleted** | [**WebhookPayloadMessageDeleted**](WebhookPayloadMessageDeleted.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onmessagedelivered"></a>
# **OnMessageDelivered**
> void OnMessageDelivered (WebhookPayloadMessageDeliveryStatus webhookPayloadMessageDeliveryStatus)

Message delivered event

Fired when an outgoing message is delivered to the recipient. Supported on WhatsApp and Facebook Messenger. 

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
    public class OnMessageDeliveredExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadMessageDeliveryStatus = new WebhookPayloadMessageDeliveryStatus(); // WebhookPayloadMessageDeliveryStatus | 

            try
            {
                // Message delivered event
                apiInstance.OnMessageDelivered(webhookPayloadMessageDeliveryStatus);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnMessageDelivered: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnMessageDeliveredWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Message delivered event
    apiInstance.OnMessageDeliveredWithHttpInfo(webhookPayloadMessageDeliveryStatus);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnMessageDeliveredWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadMessageDeliveryStatus** | [**WebhookPayloadMessageDeliveryStatus**](WebhookPayloadMessageDeliveryStatus.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onmessageedited"></a>
# **OnMessageEdited**
> void OnMessageEdited (WebhookPayloadMessageEdited webhookPayloadMessageEdited)

Message edited event

Fired when a sender edits a previously-sent message. Supported on Instagram, Facebook Messenger, and Telegram. The payload includes the full editHistory so consumers can show prior versions. 

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
    public class OnMessageEditedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadMessageEdited = new WebhookPayloadMessageEdited(); // WebhookPayloadMessageEdited | 

            try
            {
                // Message edited event
                apiInstance.OnMessageEdited(webhookPayloadMessageEdited);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnMessageEdited: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnMessageEditedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Message edited event
    apiInstance.OnMessageEditedWithHttpInfo(webhookPayloadMessageEdited);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnMessageEditedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadMessageEdited** | [**WebhookPayloadMessageEdited**](WebhookPayloadMessageEdited.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onmessagefailed"></a>
# **OnMessageFailed**
> void OnMessageFailed (WebhookPayloadMessageDeliveryStatus webhookPayloadMessageDeliveryStatus)

Message delivery failed event

Fired when an outgoing message fails to deliver. Currently only emitted for WhatsApp (other platforms don't expose per-message failure via webhook). The payload error object contains code, title, and message from the platform. 

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
    public class OnMessageFailedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadMessageDeliveryStatus = new WebhookPayloadMessageDeliveryStatus(); // WebhookPayloadMessageDeliveryStatus | 

            try
            {
                // Message delivery failed event
                apiInstance.OnMessageFailed(webhookPayloadMessageDeliveryStatus);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnMessageFailed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnMessageFailedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Message delivery failed event
    apiInstance.OnMessageFailedWithHttpInfo(webhookPayloadMessageDeliveryStatus);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnMessageFailedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadMessageDeliveryStatus** | [**WebhookPayloadMessageDeliveryStatus**](WebhookPayloadMessageDeliveryStatus.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onmessageread"></a>
# **OnMessageRead**
> void OnMessageRead (WebhookPayloadMessageDeliveryStatus webhookPayloadMessageDeliveryStatus)

Message read event

Fired when an outgoing message is read by the recipient. Supported on WhatsApp, Facebook Messenger, and Instagram. 

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
    public class OnMessageReadExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadMessageDeliveryStatus = new WebhookPayloadMessageDeliveryStatus(); // WebhookPayloadMessageDeliveryStatus | 

            try
            {
                // Message read event
                apiInstance.OnMessageRead(webhookPayloadMessageDeliveryStatus);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnMessageRead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnMessageReadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Message read event
    apiInstance.OnMessageReadWithHttpInfo(webhookPayloadMessageDeliveryStatus);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnMessageReadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadMessageDeliveryStatus** | [**WebhookPayloadMessageDeliveryStatus**](WebhookPayloadMessageDeliveryStatus.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onmessagereceived"></a>
# **OnMessageReceived**
> void OnMessageReceived (WebhookPayloadMessage webhookPayloadMessage)

Message received event

Fired when a new inbox message is received.

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
    public class OnMessageReceivedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadMessage = new WebhookPayloadMessage(); // WebhookPayloadMessage | 

            try
            {
                // Message received event
                apiInstance.OnMessageReceived(webhookPayloadMessage);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnMessageReceived: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnMessageReceivedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Message received event
    apiInstance.OnMessageReceivedWithHttpInfo(webhookPayloadMessage);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnMessageReceivedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadMessage** | [**WebhookPayloadMessage**](WebhookPayloadMessage.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onmessagesent"></a>
# **OnMessageSent**
> void OnMessageSent (WebhookPayloadMessageSent webhookPayloadMessageSent)

Message sent event

Fired when a message is sent via the API.

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
    public class OnMessageSentExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadMessageSent = new WebhookPayloadMessageSent(); // WebhookPayloadMessageSent | 

            try
            {
                // Message sent event
                apiInstance.OnMessageSent(webhookPayloadMessageSent);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnMessageSent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnMessageSentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Message sent event
    apiInstance.OnMessageSentWithHttpInfo(webhookPayloadMessageSent);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnMessageSentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadMessageSent** | [**WebhookPayloadMessageSent**](WebhookPayloadMessageSent.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onpostcancelled"></a>
# **OnPostCancelled**
> void OnPostCancelled (WebhookPayloadPost webhookPayloadPost)

Post cancelled event

Fired when a post publishing job is cancelled.

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
    public class OnPostCancelledExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadPost = new WebhookPayloadPost(); // WebhookPayloadPost | 

            try
            {
                // Post cancelled event
                apiInstance.OnPostCancelled(webhookPayloadPost);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostCancelled: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostCancelledWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Post cancelled event
    apiInstance.OnPostCancelledWithHttpInfo(webhookPayloadPost);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostCancelledWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadPost** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onpostexternalcreated"></a>
# **OnPostExternalCreated**
> void OnPostExternalCreated (WebhookPayloadExternalPost webhookPayloadExternalPost)

External post created event

Fired when Zernio's background sync detects a natively-authored post (created outside Zernio, e.g. a Google Business Profile localPost made in the Google UI) for the first time. Poll-driven (~hourly), not real-time. `post.source` is always \"external\". 

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
    public class OnPostExternalCreatedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadExternalPost = new WebhookPayloadExternalPost(); // WebhookPayloadExternalPost | 

            try
            {
                // External post created event
                apiInstance.OnPostExternalCreated(webhookPayloadExternalPost);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostExternalCreated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostExternalCreatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // External post created event
    apiInstance.OnPostExternalCreatedWithHttpInfo(webhookPayloadExternalPost);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostExternalCreatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadExternalPost** | [**WebhookPayloadExternalPost**](WebhookPayloadExternalPost.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onpostexternaldeleted"></a>
# **OnPostExternalDeleted**
> void OnPostExternalDeleted (WebhookPayloadExternalPost webhookPayloadExternalPost)

External post deleted event

Fired when a tracked native post is detected as removed from the platform. `post.deletedAt` carries the detection time. Coverage is bounded to the most recent posts the platform listing returns. 

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
    public class OnPostExternalDeletedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadExternalPost = new WebhookPayloadExternalPost(); // WebhookPayloadExternalPost | 

            try
            {
                // External post deleted event
                apiInstance.OnPostExternalDeleted(webhookPayloadExternalPost);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostExternalDeleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostExternalDeletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // External post deleted event
    apiInstance.OnPostExternalDeletedWithHttpInfo(webhookPayloadExternalPost);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostExternalDeletedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadExternalPost** | [**WebhookPayloadExternalPost**](WebhookPayloadExternalPost.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onpostexternalupdated"></a>
# **OnPostExternalUpdated**
> void OnPostExternalUpdated (WebhookPayloadExternalPost webhookPayloadExternalPost)

External post updated event

Fired when a tracked native post's text or media changed on the platform. Detected by comparing text/media structure and, where available, the platform's own edit timestamp; a media-URL-only refresh does not fire this. 

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
    public class OnPostExternalUpdatedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadExternalPost = new WebhookPayloadExternalPost(); // WebhookPayloadExternalPost | 

            try
            {
                // External post updated event
                apiInstance.OnPostExternalUpdated(webhookPayloadExternalPost);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostExternalUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostExternalUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // External post updated event
    apiInstance.OnPostExternalUpdatedWithHttpInfo(webhookPayloadExternalPost);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostExternalUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadExternalPost** | [**WebhookPayloadExternalPost**](WebhookPayloadExternalPost.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onpostfailed"></a>
# **OnPostFailed**
> void OnPostFailed (WebhookPayloadPost webhookPayloadPost)

Post failed event

Fired when a post fails to publish on all target platforms.

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
    public class OnPostFailedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadPost = new WebhookPayloadPost(); // WebhookPayloadPost | 

            try
            {
                // Post failed event
                apiInstance.OnPostFailed(webhookPayloadPost);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostFailed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostFailedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Post failed event
    apiInstance.OnPostFailedWithHttpInfo(webhookPayloadPost);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostFailedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadPost** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onpostpartial"></a>
# **OnPostPartial**
> void OnPostPartial (WebhookPayloadPost webhookPayloadPost)

Post partial event

Fired when a post publishes on some platforms and fails on others.

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
    public class OnPostPartialExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadPost = new WebhookPayloadPost(); // WebhookPayloadPost | 

            try
            {
                // Post partial event
                apiInstance.OnPostPartial(webhookPayloadPost);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostPartial: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostPartialWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Post partial event
    apiInstance.OnPostPartialWithHttpInfo(webhookPayloadPost);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostPartialWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadPost** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onpostplatformfailed"></a>
# **OnPostPlatformFailed**
> void OnPostPlatformFailed (WebhookPayloadPostPlatform webhookPayloadPostPlatform)

Post platform failed event

Fired once per platform target inside a post as that platform fails permanently. Temporary/retryable failures do NOT fire this event — only permanent ones, so retry loops stay quiet. The envelope event (`post.failed` / `post.partial`) fires separately AFTER all platforms have terminated. 

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
    public class OnPostPlatformFailedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadPostPlatform = new WebhookPayloadPostPlatform(); // WebhookPayloadPostPlatform | 

            try
            {
                // Post platform failed event
                apiInstance.OnPostPlatformFailed(webhookPayloadPostPlatform);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostPlatformFailed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostPlatformFailedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Post platform failed event
    apiInstance.OnPostPlatformFailedWithHttpInfo(webhookPayloadPostPlatform);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostPlatformFailedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadPostPlatform** | [**WebhookPayloadPostPlatform**](WebhookPayloadPostPlatform.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onpostplatformpublished"></a>
# **OnPostPlatformPublished**
> void OnPostPlatformPublished (WebhookPayloadPostPlatform webhookPayloadPostPlatform)

Post platform published event

Fired once per platform target inside a post as that platform finishes publishing successfully. Does NOT wait for the post-level rollup — consumers building incremental UIs get notified immediately, even when other platforms on the same post are still processing. The envelope event (`post.published` / `post.partial`) fires separately AFTER all platforms have terminated. 

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
    public class OnPostPlatformPublishedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadPostPlatform = new WebhookPayloadPostPlatform(); // WebhookPayloadPostPlatform | 

            try
            {
                // Post platform published event
                apiInstance.OnPostPlatformPublished(webhookPayloadPostPlatform);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostPlatformPublished: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostPlatformPublishedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Post platform published event
    apiInstance.OnPostPlatformPublishedWithHttpInfo(webhookPayloadPostPlatform);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostPlatformPublishedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadPostPlatform** | [**WebhookPayloadPostPlatform**](WebhookPayloadPostPlatform.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onpostpublished"></a>
# **OnPostPublished**
> void OnPostPublished (WebhookPayloadPost webhookPayloadPost)

Post published event

Fired when a post is successfully published.

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
    public class OnPostPublishedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadPost = new WebhookPayloadPost(); // WebhookPayloadPost | 

            try
            {
                // Post published event
                apiInstance.OnPostPublished(webhookPayloadPost);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostPublished: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostPublishedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Post published event
    apiInstance.OnPostPublishedWithHttpInfo(webhookPayloadPost);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostPublishedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadPost** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onpostrecycled"></a>
# **OnPostRecycled**
> void OnPostRecycled (WebhookPayloadPost webhookPayloadPost)

Post recycled event

Fired when a post is recycled (cloned and re-scheduled for publishing).

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
    public class OnPostRecycledExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadPost = new WebhookPayloadPost(); // WebhookPayloadPost | 

            try
            {
                // Post recycled event
                apiInstance.OnPostRecycled(webhookPayloadPost);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostRecycled: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostRecycledWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Post recycled event
    apiInstance.OnPostRecycledWithHttpInfo(webhookPayloadPost);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostRecycledWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadPost** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onpostscheduled"></a>
# **OnPostScheduled**
> void OnPostScheduled (WebhookPayloadPost webhookPayloadPost)

Post scheduled event

Fired when a post is created and scheduled for publishing.

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
    public class OnPostScheduledExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadPost = new WebhookPayloadPost(); // WebhookPayloadPost | 

            try
            {
                // Post scheduled event
                apiInstance.OnPostScheduled(webhookPayloadPost);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostScheduled: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostScheduledWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Post scheduled event
    apiInstance.OnPostScheduledWithHttpInfo(webhookPayloadPost);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostScheduledWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadPost** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onposttiktokurlresolved"></a>
# **OnPostTikTokUrlResolved**
> void OnPostTikTokUrlResolved (WebhookPayloadPostPlatform webhookPayloadPostPlatform)

TikTok post URL resolved event

Fired when an already-published TikTok platform entry gets its public URL backfilled. TikTok exposes the numeric video id asynchronously (often minutes after PUBLISH_COMPLETE), so the terminal events can carry an empty `publishedUrl` for TikTok. This event delivers `platform.publishedUrl` and the resolved `platform.platformPostId` once available. At most once per platform target; never fires for drafts or private posts (no public URL exists). Payload shape is identical to `post.platform.published`. 

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
    public class OnPostTikTokUrlResolvedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadPostPlatform = new WebhookPayloadPostPlatform(); // WebhookPayloadPostPlatform | 

            try
            {
                // TikTok post URL resolved event
                apiInstance.OnPostTikTokUrlResolved(webhookPayloadPostPlatform);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostTikTokUrlResolved: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostTikTokUrlResolvedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // TikTok post URL resolved event
    apiInstance.OnPostTikTokUrlResolvedWithHttpInfo(webhookPayloadPostPlatform);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostTikTokUrlResolvedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadPostPlatform** | [**WebhookPayloadPostPlatform**](WebhookPayloadPostPlatform.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onreactionreceived"></a>
# **OnReactionReceived**
> void OnReactionReceived (WebhookPayloadReaction webhookPayloadReaction)

Reaction received event

Fired when a participant adds or removes an emoji reaction on a message. Supported on WhatsApp and Telegram. Distinct from message.received so a reaction (e.g. a thumbs-up) is not mistaken for an inbound message. The `reaction.action` field is `added` or `removed`. On WhatsApp removals the platform does not report which emoji was removed, so `reaction.emoji` may be an empty string. Requires the Inbox add-on. 

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
    public class OnReactionReceivedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadReaction = new WebhookPayloadReaction(); // WebhookPayloadReaction | 

            try
            {
                // Reaction received event
                apiInstance.OnReactionReceived(webhookPayloadReaction);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnReactionReceived: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnReactionReceivedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reaction received event
    apiInstance.OnReactionReceivedWithHttpInfo(webhookPayloadReaction);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnReactionReceivedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadReaction** | [**WebhookPayloadReaction**](WebhookPayloadReaction.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onreviewnew"></a>
# **OnReviewNew**
> void OnReviewNew (WebhookPayloadReviewNew webhookPayloadReviewNew)

Review new event

Fired when a new review is posted on a connected account. Currently supported for Google Business Profile (real-time via Pub/Sub). Requires the Inbox add-on. 

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
    public class OnReviewNewExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadReviewNew = new WebhookPayloadReviewNew(); // WebhookPayloadReviewNew | 

            try
            {
                // Review new event
                apiInstance.OnReviewNew(webhookPayloadReviewNew);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnReviewNew: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnReviewNewWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Review new event
    apiInstance.OnReviewNewWithHttpInfo(webhookPayloadReviewNew);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnReviewNewWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadReviewNew** | [**WebhookPayloadReviewNew**](WebhookPayloadReviewNew.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onreviewupdated"></a>
# **OnReviewUpdated**
> void OnReviewUpdated (WebhookPayloadReviewUpdated webhookPayloadReviewUpdated)

Review updated event

Fired when a review changes: the reviewer edits their text or rating, or a reply is added (via the API or directly through the Google Business dashboard). Payload shape matches review.new. Requires the Inbox add-on. 

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
    public class OnReviewUpdatedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadReviewUpdated = new WebhookPayloadReviewUpdated(); // WebhookPayloadReviewUpdated | 

            try
            {
                // Review updated event
                apiInstance.OnReviewUpdated(webhookPayloadReviewUpdated);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnReviewUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnReviewUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Review updated event
    apiInstance.OnReviewUpdatedWithHttpInfo(webhookPayloadReviewUpdated);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnReviewUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadReviewUpdated** | [**WebhookPayloadReviewUpdated**](WebhookPayloadReviewUpdated.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onwebhooktest"></a>
# **OnWebhookTest**
> void OnWebhookTest (WebhookPayloadTest webhookPayloadTest)

Webhook test event

Fired when sending a test webhook to verify the endpoint configuration.

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
    public class OnWebhookTestExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadTest = new WebhookPayloadTest(); // WebhookPayloadTest | 

            try
            {
                // Webhook test event
                apiInstance.OnWebhookTest(webhookPayloadTest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWebhookTest: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWebhookTestWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Webhook test event
    apiInstance.OnWebhookTestWithHttpInfo(webhookPayloadTest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWebhookTestWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadTest** | [**WebhookPayloadTest**](WebhookPayloadTest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onwhatsappautomaticevent"></a>
# **OnWhatsAppAutomaticEvent**
> void OnWhatsAppAutomaticEvent (OnWhatsAppAutomaticEventRequest onWhatsAppAutomaticEventRequest)

WhatsApp automatic event detected

Fired when Meta's automatic event identification (opt-in during Embedded Signup; not available for EU/UK/JP businesses) detects a lead or purchase in a Click-to-WhatsApp conversation. Branch on `eventName` (`LeadSubmitted` | `Purchase`). Carries the `ctwa_clid` even on coexistence numbers where the inbound referral omits it (this webhook is the only surface that delivers it there); the clid is also written back onto the conversation, so POST /v1/whatsapp/conversions becomes usable for the thread. 

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
    public class OnWhatsAppAutomaticEventExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var onWhatsAppAutomaticEventRequest = new OnWhatsAppAutomaticEventRequest(); // OnWhatsAppAutomaticEventRequest | 

            try
            {
                // WhatsApp automatic event detected
                apiInstance.OnWhatsAppAutomaticEvent(onWhatsAppAutomaticEventRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppAutomaticEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppAutomaticEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp automatic event detected
    apiInstance.OnWhatsAppAutomaticEventWithHttpInfo(onWhatsAppAutomaticEventRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppAutomaticEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onWhatsAppAutomaticEventRequest** | [**OnWhatsAppAutomaticEventRequest**](OnWhatsAppAutomaticEventRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onwhatsappnumberactionrequired"></a>
# **OnWhatsAppNumberActionRequired**
> void OnWhatsAppNumberActionRequired (OnWhatsAppNumberActionRequiredRequest onWhatsAppNumberActionRequiredRequest)

WhatsApp number action required event

Fired when the regulator asks for more information on an already-placed regulated number order. The number stays pending (nothing was rejected); the customer can provide the missing information from the dashboard, or via the remediation endpoint. `reason` carries the regulator's request verbatim when available. 

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
    public class OnWhatsAppNumberActionRequiredExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var onWhatsAppNumberActionRequiredRequest = new OnWhatsAppNumberActionRequiredRequest(); // OnWhatsAppNumberActionRequiredRequest | 

            try
            {
                // WhatsApp number action required event
                apiInstance.OnWhatsAppNumberActionRequired(onWhatsAppNumberActionRequiredRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberActionRequired: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppNumberActionRequiredWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp number action required event
    apiInstance.OnWhatsAppNumberActionRequiredWithHttpInfo(onWhatsAppNumberActionRequiredRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberActionRequiredWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onWhatsAppNumberActionRequiredRequest** | [**OnWhatsAppNumberActionRequiredRequest**](OnWhatsAppNumberActionRequiredRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onwhatsappnumberactivated"></a>
# **OnWhatsAppNumberActivated**
> void OnWhatsAppNumberActivated (OnWhatsAppNumberActivatedRequest onWhatsAppNumberActivatedRequest)

WhatsApp number activated event

Fired when a purchased WhatsApp number becomes active and usable — both the synchronous (Tier 1/2) path and the asynchronous regulated (Tier 3/4) path land here. Lets integrators react without polling GET /v1/phone-numbers. 

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
    public class OnWhatsAppNumberActivatedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var onWhatsAppNumberActivatedRequest = new OnWhatsAppNumberActivatedRequest(); // OnWhatsAppNumberActivatedRequest | 

            try
            {
                // WhatsApp number activated event
                apiInstance.OnWhatsAppNumberActivated(onWhatsAppNumberActivatedRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberActivated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppNumberActivatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp number activated event
    apiInstance.OnWhatsAppNumberActivatedWithHttpInfo(onWhatsAppNumberActivatedRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberActivatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onWhatsAppNumberActivatedRequest** | [**OnWhatsAppNumberActivatedRequest**](OnWhatsAppNumberActivatedRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onwhatsappnumberdeclined"></a>
# **OnWhatsAppNumberDeclined**
> void OnWhatsAppNumberDeclined (OnWhatsAppNumberDeclinedRequest onWhatsAppNumberDeclinedRequest)

WhatsApp number declined event

Fired when a regulated (Tier 3/4) number order is declined or fails review. The number is never billed. `reason` carries the reviewer's rejection reason when available. 

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
    public class OnWhatsAppNumberDeclinedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var onWhatsAppNumberDeclinedRequest = new OnWhatsAppNumberDeclinedRequest(); // OnWhatsAppNumberDeclinedRequest | 

            try
            {
                // WhatsApp number declined event
                apiInstance.OnWhatsAppNumberDeclined(onWhatsAppNumberDeclinedRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberDeclined: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppNumberDeclinedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp number declined event
    apiInstance.OnWhatsAppNumberDeclinedWithHttpInfo(onWhatsAppNumberDeclinedRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberDeclinedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onWhatsAppNumberDeclinedRequest** | [**OnWhatsAppNumberDeclinedRequest**](OnWhatsAppNumberDeclinedRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onwhatsappnumberkycsubmitted"></a>
# **OnWhatsAppNumberKycSubmitted**
> void OnWhatsAppNumberKycSubmitted (OnWhatsAppNumberKycSubmittedRequest onWhatsAppNumberKycSubmittedRequest)

WhatsApp number KYC submitted event

Fired when an end customer completes a hosted KYC share link (POST /v1/phone-numbers/kyc/share). The number enters review (pending_regulatory) under your account; `whatsapp.number.activated` or `whatsapp.number.declined` follows once the provider rules on it. 

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
    public class OnWhatsAppNumberKycSubmittedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var onWhatsAppNumberKycSubmittedRequest = new OnWhatsAppNumberKycSubmittedRequest(); // OnWhatsAppNumberKycSubmittedRequest | 

            try
            {
                // WhatsApp number KYC submitted event
                apiInstance.OnWhatsAppNumberKycSubmitted(onWhatsAppNumberKycSubmittedRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberKycSubmitted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppNumberKycSubmittedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp number KYC submitted event
    apiInstance.OnWhatsAppNumberKycSubmittedWithHttpInfo(onWhatsAppNumberKycSubmittedRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberKycSubmittedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onWhatsAppNumberKycSubmittedRequest** | [**OnWhatsAppNumberKycSubmittedRequest**](OnWhatsAppNumberKycSubmittedRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onwhatsappnumberreactivated"></a>
# **OnWhatsAppNumberReactivated**
> void OnWhatsAppNumberReactivated (OnWhatsAppNumberReactivatedRequest onWhatsAppNumberReactivatedRequest)

WhatsApp number reactivated event

Fired when a suspended number is reactivated (e.g. the payment recovered) and is usable again. 

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
    public class OnWhatsAppNumberReactivatedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var onWhatsAppNumberReactivatedRequest = new OnWhatsAppNumberReactivatedRequest(); // OnWhatsAppNumberReactivatedRequest | 

            try
            {
                // WhatsApp number reactivated event
                apiInstance.OnWhatsAppNumberReactivated(onWhatsAppNumberReactivatedRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberReactivated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppNumberReactivatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp number reactivated event
    apiInstance.OnWhatsAppNumberReactivatedWithHttpInfo(onWhatsAppNumberReactivatedRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberReactivatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onWhatsAppNumberReactivatedRequest** | [**OnWhatsAppNumberReactivatedRequest**](OnWhatsAppNumberReactivatedRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onwhatsappnumberreleased"></a>
# **OnWhatsAppNumberReleased**
> void OnWhatsAppNumberReleased (OnWhatsAppNumberReleasedRequest onWhatsAppNumberReleasedRequest)

WhatsApp number released event

Fired when a number is released and is no longer usable (by the user, a billing cleanup, or an admin). Terminal. `reason` carries the cause (e.g. `user_requested`, `cleanup_suspended`). 

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
    public class OnWhatsAppNumberReleasedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var onWhatsAppNumberReleasedRequest = new OnWhatsAppNumberReleasedRequest(); // OnWhatsAppNumberReleasedRequest | 

            try
            {
                // WhatsApp number released event
                apiInstance.OnWhatsAppNumberReleased(onWhatsAppNumberReleasedRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberReleased: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppNumberReleasedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp number released event
    apiInstance.OnWhatsAppNumberReleasedWithHttpInfo(onWhatsAppNumberReleasedRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberReleasedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onWhatsAppNumberReleasedRequest** | [**OnWhatsAppNumberReleasedRequest**](OnWhatsAppNumberReleasedRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onwhatsappnumbersuspended"></a>
# **OnWhatsAppNumberSuspended**
> void OnWhatsAppNumberSuspended (OnWhatsAppNumberSuspendedRequest onWhatsAppNumberSuspendedRequest)

WhatsApp number suspended event

Fired when an active number is suspended (e.g. a failed payment). The number stops working until the issue is resolved, after which a `whatsapp.number.reactivated` event is sent. `reason` carries the cause (e.g. `payment_failed`, `subscription_ended`). 

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
    public class OnWhatsAppNumberSuspendedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var onWhatsAppNumberSuspendedRequest = new OnWhatsAppNumberSuspendedRequest(); // OnWhatsAppNumberSuspendedRequest | 

            try
            {
                // WhatsApp number suspended event
                apiInstance.OnWhatsAppNumberSuspended(onWhatsAppNumberSuspendedRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberSuspended: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppNumberSuspendedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp number suspended event
    apiInstance.OnWhatsAppNumberSuspendedWithHttpInfo(onWhatsAppNumberSuspendedRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberSuspendedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onWhatsAppNumberSuspendedRequest** | [**OnWhatsAppNumberSuspendedRequest**](OnWhatsAppNumberSuspendedRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onwhatsappnumberverificationrequired"></a>
# **OnWhatsAppNumberVerificationRequired**
> void OnWhatsAppNumberVerificationRequired (OnWhatsAppNumberVerificationRequiredRequest onWhatsAppNumberVerificationRequiredRequest)

WhatsApp number verification-required event

Fired when a regulated number has an out-of-band identity-verification step (e.g. Onfido). `verificationUrl` is the link to forward to the number's end user; the order completes once they pass. 

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
    public class OnWhatsAppNumberVerificationRequiredExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var onWhatsAppNumberVerificationRequiredRequest = new OnWhatsAppNumberVerificationRequiredRequest(); // OnWhatsAppNumberVerificationRequiredRequest | 

            try
            {
                // WhatsApp number verification-required event
                apiInstance.OnWhatsAppNumberVerificationRequired(onWhatsAppNumberVerificationRequiredRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberVerificationRequired: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppNumberVerificationRequiredWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp number verification-required event
    apiInstance.OnWhatsAppNumberVerificationRequiredWithHttpInfo(onWhatsAppNumberVerificationRequiredRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppNumberVerificationRequiredWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onWhatsAppNumberVerificationRequiredRequest** | [**OnWhatsAppNumberVerificationRequiredRequest**](OnWhatsAppNumberVerificationRequiredRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onwhatsapptemplatestatusupdated"></a>
# **OnWhatsAppTemplateStatusUpdated**
> void OnWhatsAppTemplateStatusUpdated (WebhookPayloadWhatsAppTemplateStatusUpdated webhookPayloadWhatsAppTemplateStatusUpdated)

WhatsApp template status updated event

Fired when Meta finishes (re)reviewing a WhatsApp Business template attached to a connected WABA. Forwarded from Meta's `message_template_status_update` webhook field on the WhatsApp Business Account. Consumers branch on `template.status` (APPROVED, REJECTED, PENDING, PAUSED, DISABLED, IN_APPEAL, PENDING_DELETION). Meta does not include the previous status or the template's category in this event. 

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
    public class OnWhatsAppTemplateStatusUpdatedExample
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
            var apiInstance = new WebhookEventsApi(httpClient, config, httpClientHandler);
            var webhookPayloadWhatsAppTemplateStatusUpdated = new WebhookPayloadWhatsAppTemplateStatusUpdated(); // WebhookPayloadWhatsAppTemplateStatusUpdated | 

            try
            {
                // WhatsApp template status updated event
                apiInstance.OnWhatsAppTemplateStatusUpdated(webhookPayloadWhatsAppTemplateStatusUpdated);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppTemplateStatusUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppTemplateStatusUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp template status updated event
    apiInstance.OnWhatsAppTemplateStatusUpdatedWithHttpInfo(webhookPayloadWhatsAppTemplateStatusUpdated);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppTemplateStatusUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadWhatsAppTemplateStatusUpdated** | [**WebhookPayloadWhatsAppTemplateStatusUpdated**](WebhookPayloadWhatsAppTemplateStatusUpdated.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

