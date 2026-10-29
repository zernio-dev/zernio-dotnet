# Zernio.Api.MessagesApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AcceptConversationRequest**](MessagesApi.md#acceptconversationrequest) | **POST** /v1/inbox/conversations/{conversationId}/accept | Accept a message request |
| [**AddConversationLabel**](MessagesApi.md#addconversationlabel) | **POST** /v1/inbox/conversations/{conversationId}/labels | Add a label to a conversation |
| [**AddMessageReaction**](MessagesApi.md#addmessagereaction) | **POST** /v1/inbox/conversations/{conversationId}/messages/{messageId}/reactions | Add reaction |
| [**CreateInboxConversation**](MessagesApi.md#createinboxconversation) | **POST** /v1/inbox/conversations | Create conversation |
| [**CreateInboxLabel**](MessagesApi.md#createinboxlabel) | **POST** /v1/inbox/labels | Create a conversation label |
| [**DeleteInboxConversation**](MessagesApi.md#deleteinboxconversation) | **DELETE** /v1/inbox/conversations/{conversationId} | Delete conversation |
| [**DeleteInboxLabel**](MessagesApi.md#deleteinboxlabel) | **DELETE** /v1/inbox/labels/{labelId} | Delete a conversation label |
| [**DeleteInboxMessage**](MessagesApi.md#deleteinboxmessage) | **DELETE** /v1/inbox/conversations/{conversationId}/messages/{messageId} | Delete message |
| [**EditInboxMessage**](MessagesApi.md#editinboxmessage) | **PATCH** /v1/inbox/conversations/{conversationId}/messages/{messageId} | Edit message |
| [**GetInboxConversation**](MessagesApi.md#getinboxconversation) | **GET** /v1/inbox/conversations/{conversationId} | Get conversation |
| [**GetInboxConversationMessages**](MessagesApi.md#getinboxconversationmessages) | **GET** /v1/inbox/conversations/{conversationId}/messages | List messages |
| [**GetMessageAttachment**](MessagesApi.md#getmessageattachment) | **GET** /v1/inbox/conversations/{conversationId}/messages/{messageId}/attachments/{index} | Resolve message attachment |
| [**ListConversationLabels**](MessagesApi.md#listconversationlabels) | **GET** /v1/inbox/conversations/{conversationId}/labels | List the labels on a conversation |
| [**ListInboxConversations**](MessagesApi.md#listinboxconversations) | **GET** /v1/inbox/conversations | List conversations |
| [**ListInboxLabels**](MessagesApi.md#listinboxlabels) | **GET** /v1/inbox/labels | List the Page&#39;s conversation labels |
| [**MarkConversationRead**](MessagesApi.md#markconversationread) | **POST** /v1/inbox/conversations/{conversationId}/read | Mark a conversation as read |
| [**RemoveConversationLabel**](MessagesApi.md#removeconversationlabel) | **DELETE** /v1/inbox/conversations/{conversationId}/labels/{labelId} | Remove a label from a conversation |
| [**RemoveMessageReaction**](MessagesApi.md#removemessagereaction) | **DELETE** /v1/inbox/conversations/{conversationId}/messages/{messageId}/reactions | Remove reaction |
| [**SearchInboxConversations**](MessagesApi.md#searchinboxconversations) | **GET** /v1/inbox/conversations/search | Search conversations |
| [**SendInboxMessage**](MessagesApi.md#sendinboxmessage) | **POST** /v1/inbox/conversations/{conversationId}/messages | Send message |
| [**SendTypingIndicator**](MessagesApi.md#sendtypingindicator) | **POST** /v1/inbox/conversations/{conversationId}/typing | Send typing indicator |
| [**SetConversationThreadControl**](MessagesApi.md#setconversationthreadcontrol) | **POST** /v1/inbox/conversations/{conversationId}/thread-control | Change who answers a conversation (handover) |
| [**UpdateInboxConversation**](MessagesApi.md#updateinboxconversation) | **PUT** /v1/inbox/conversations/{conversationId} | Update conversation status |
| [**UploadMediaDirect**](MessagesApi.md#uploadmediadirect) | **POST** /v1/media/upload-direct | Upload media file |

<a id="acceptconversationrequest"></a>
# **AcceptConversationRequest**
> AcceptConversationRequest200Response AcceptConversationRequest (string conversationId, AcceptConversationRequestRequest acceptConversationRequestRequest)

Accept a message request

Accept a Facebook or Instagram Message Request by replying to it.  Facebook Page requests are listed with `GET /v1/inbox/conversations?folder=requests`; Instagram answers PLATFORM_LIMITATION there.  Meta has no separate accept call: the first reply is what moves the thread into the inbox. So this sends `message` through the same path, checks and webhooks as `POST /v1/inbox/conversations/{conversationId}/messages`, and answers the same way.  Supports the `Idempotency-Key` header. 

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
    public class AcceptConversationRequestExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | The `id` of the request item from the requests folder.
            var acceptConversationRequestRequest = new AcceptConversationRequestRequest(); // AcceptConversationRequestRequest | 

            try
            {
                // Accept a message request
                AcceptConversationRequest200Response result = apiInstance.AcceptConversationRequest(conversationId, acceptConversationRequestRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.AcceptConversationRequest: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AcceptConversationRequestWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Accept a message request
    ApiResponse<AcceptConversationRequest200Response> response = apiInstance.AcceptConversationRequestWithHttpInfo(conversationId, acceptConversationRequestRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.AcceptConversationRequestWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | The &#x60;id&#x60; of the request item from the requests folder. |  |
| **acceptConversationRequestRequest** | [**AcceptConversationRequestRequest**](AcceptConversationRequestRequest.md) |  |  |

### Return type

[**AcceptConversationRequest200Response**](AcceptConversationRequest200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reply sent, the request is accepted |  -  |
| **400** | Invalid body, or an account that is not Facebook or Instagram (PLATFORM_NOT_SUPPORTED) |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required or plan limit reached |  -  |
| **404** | Account or conversation not found |  -  |
| **409** | The same Idempotency-Key is still processing, or another app owns the thread under Meta&#39;s handover protocol (code not_thread_owner, &#x60;details.ownerAppId&#x60; names it when Meta says). Take control with thread-control first (accounts connected through a Facebook Page only; an Instagram Login connection cannot take). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="addconversationlabel"></a>
# **AddConversationLabel**
> UpdateYoutubeDefaultPlaylist200Response AddConversationLabel (string conversationId, AddConversationLabelRequest addConversationLabelRequest)

Add a label to a conversation

Facebook Messenger only. Applies one of the Page's custom labels to the person in this conversation (Graph `POST /{label-id}/label?user={psid}`). The id must be one of the Page's custom labels, otherwise 404 `resource_not_found`. Other platforms answer 400 `platform_not_supported`.

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
    public class AddConversationLabelExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | Conversation ID (Zernio id or Meta platform conversation id)
            var addConversationLabelRequest = new AddConversationLabelRequest(); // AddConversationLabelRequest | 

            try
            {
                // Add a label to a conversation
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.AddConversationLabel(conversationId, addConversationLabelRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.AddConversationLabel: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddConversationLabelWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add a label to a conversation
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.AddConversationLabelWithHttpInfo(conversationId, addConversationLabelRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.AddConversationLabelWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | Conversation ID (Zernio id or Meta platform conversation id) |  |
| **addConversationLabelRequest** | [**AddConversationLabelRequest**](AddConversationLabelRequest.md) |  |  |

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
| **200** | Label added |  -  |
| **400** | Invalid body, or an account that is not Facebook (platform_not_supported), or Meta refusing for good (platform_api_error with Meta&#39;s message in platformError). A transient Meta failure answers 502 |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account or conversation not found, or the label is not one of the Page&#39;s custom labels |  -  |
| **422** | No Facebook Page is selected on this account (linked_account_required); reconnect it and select the Page |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="addmessagereaction"></a>
# **AddMessageReaction**
> AddMessageReaction200Response AddMessageReaction (string conversationId, string messageId, AddMessageReactionRequest addMessageReactionRequest)

Add reaction

Add an emoji reaction to a message.  ### Platform support  - Telegram: supports a subset of Unicode emoji reactions - WhatsApp: supports any standard emoji (one reaction per message per sender) - Instagram and Facebook Messenger: any standard emoji, subject to Meta's 24h messaging window - Slack: the emoji must have a Slack name (e.g. `:thumbsup:`); unnamed characters return 400 - iMessage: the six Apple tapbacks (❤️ 👍 👎 😂 ‼️ ❓) render natively; any other emoji is sent as a custom emoji tapback (iOS 18+ recipients) - All others: returns 400 (not supported) 

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
    public class AddMessageReactionExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | The conversation ID
            var messageId = "messageId_example";  // string | The platform message ID (as returned by GET /messages) or the Zernio message ID (as returned by the reaction webhook)
            var addMessageReactionRequest = new AddMessageReactionRequest(); // AddMessageReactionRequest | 

            try
            {
                // Add reaction
                AddMessageReaction200Response result = apiInstance.AddMessageReaction(conversationId, messageId, addMessageReactionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.AddMessageReaction: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddMessageReactionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add reaction
    ApiResponse<AddMessageReaction200Response> response = apiInstance.AddMessageReactionWithHttpInfo(conversationId, messageId, addMessageReactionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.AddMessageReactionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | The conversation ID |  |
| **messageId** | **string** | The platform message ID (as returned by GET /messages) or the Zernio message ID (as returned by the reaction webhook) |  |
| **addMessageReactionRequest** | [**AddMessageReactionRequest**](AddMessageReactionRequest.md) |  |  |

### Return type

[**AddMessageReaction200Response**](AddMessageReaction200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The platform accepted the reaction request. This does not guarantee the reaction was placed: the platform never confirms what it acted on. |  -  |
| **400** | Platform does not support reactions or invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account, conversation or message not found (message_not_found when messageId does not resolve to a message in this conversation) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createinboxconversation"></a>
# **CreateInboxConversation**
> CreateInboxConversation201Response CreateInboxConversation (CreateInboxConversationRequest createInboxConversationRequest)

Create conversation

Start a direct message conversation with a user. If a conversation with that recipient already exists, the message is added to the existing thread.  Supported platforms: X, Bluesky, Reddit, WhatsApp, SMS, Slack, iMessage, and email (Google and Microsoft accounts). Other platforms return PLATFORM_NOT_SUPPORTED.  ### Email (Google / Microsoft)  Pass the recipient address as participantId with `subject`, `message` and optionally `cc`. The mail is sent from the mailbox and mirrored into the inbox. The response names the inbox conversation it opened (the provider thread id, usable with the other inbox endpoints).  - 412 `account_scope_missing`: the account was connected without the `email` area - 409: the account is disconnected - 402 `payment_required`: Gmail accounts need a card on file  Sends count toward the mailbox's daily cap and never toward managed messages.  ### iMessage  Pass the recipient as participantId: a phone number in international format (+15551234567) or an iMessage email. Senders ordered through Zernio can message contacts who never wrote to them.  #### Opening message rules  The first message to such a contact must be plain text from an identifiable person or business opening a conversation.  A cold introduction, including a sales one, is fine (\"Hi Mark, this is John from Pratt Media. I help local roofers get more leads. Would you be open to a quick chat?\").  It may not contain links, email addresses, phone numbers, prices or attachments (the provider's own rule for opening messages). One that does returns 400 with code `invalid_content` and a message saying what was flagged, and nothing is sent.  #### New contact limits  Each sender may open at most one new conversation every 15 minutes. A new sender warms up, allowing this many new conversations per 24 hours:  - Days 1-2 after activation: 2 - Days 3-4: 5 - Days 5-7: 10 - Days 8-14: 20 - Days 15-21: 30 - After that: 50  Beyond that the request returns 429 with code `new_contact_limit` and a time to retry. The warm-up counts from when a sender ordered through Zernio went live. Senders registered from your own provider account are not warmed up by Zernio.  #### Follow-ups before the contact replies  Until the contact replies, the thread accepts the opening and at most two follow-ups, at least 24 hours apart.  - A follow-up sooner returns 429 `new_contact_limit` with the time to retry. - A fourth message returns 409 `recipient_must_message_first`.  The provider treats every message to a contact who has not replied as a new conversation.  Follow-ups therefore follow the same content rule and count toward the 15-minute spacing and the daily warm-up like an opening. Once the contact has written, the thread behaves like any other and is not limited.  #### Sender safety  Recipients can report a first message as junk, and reports can get a sender blocked permanently, so keep the reply rate high (above roughly 30%).  - A sender registered with your own provider account may lack the add-on for new contacts. Its sends to them return 409 `recipient_must_message_first`, and an opt-in link is the way in. - A contact who opted out returns 409 `recipient_opted_out`.  ### Slack  Pass a workspace member id as participantId (list them with GET /v1/accounts/{accountId}/slack-members). Zernio opens the DM channel with that member and sends the message. The thread then behaves like any other Slack conversation in the inbox. The member must belong to the connected workspace.  ### WhatsApp  This is the endpoint for sending an approved template message to a phone number. Put the recipient phone in participantId and provide:  - templateName - templateLanguage - templateParams: variable values for the text header, body and dynamic URL buttons, in that order  A template is required because WhatsApp does not permit freeform messages to open a conversation. A missing template returns TEMPLATE_REQUIRED.  #### Template lookup  Before sending, Zernio must resolve an exact APPROVED template definition matching both templateName and templateLanguage. If Meta rejects that lookup, or the exact approved definition is absent, Zernio sends no message and returns the canonical platform error instead.  Lookup errors use code `platform_api_error`, type `platform_error`, and platform `whatsapp`. Sanitized Meta code, message, and `error_data.details` are returned in `platformError`. `details` identifies `phase: template_lookup`, the query-free endpoint, upstream status, and only safe provider usage or retry headers.  #### Template headers, buttons and cards  - Templates with media headers (image, video, document) are handled automatically: Zernio fills the header at send time with the approved template's sample asset. - To send a DIFFERENT asset per message (e.g. a distinct invoice PDF for each recipient), pass headerMedia with a public link (or a Meta media id); it overrides the sample for that send. - A template whose approved header format is LOCATION has no header asset to reconstruct: Meta only accepts the location at send time. Pass headerLocation (latitude and longitude required) whenever such a template is sent. headerMedia and headerLocation cannot both be supplied. - A button that carries its own value at send time (a copy-code button holding a Pix payment code or a coupon, a flow token) is sent with templateButtonParams, addressed by the button's index. templateParams covers text variables and dynamic URL buttons only. - CAROUSEL templates take per-card overrides via templateCards, each addressed by the card's card_index. Card body variables restart at {{1}} per card and cannot be expressed in the flat templateParams order. - Template fields are accepted on the JSON body only, not on multipart requests.  #### Existing threads and the 24-hour window  For a number you already have a thread with, this sends the template into that thread. That makes it the way to re-engage a contact after the 24-hour customer-service window has closed. Once the recipient replies (opening the 24h window), send freeform messages with the send-message endpoint (POST /v1/inbox/conversations/{conversationId}/messages).  #### Meta Direct Send  WhatsApp Business Accounts eligible for Meta Direct Send can instead open a conversation with a business-initiated utility text message and no template. Pass category: 'utility' together with message (and no templateName). See the category field below.  ### X  #### DM eligibility  Before sending, the endpoint checks if the recipient accepts DMs from your account (via the receives_your_dm field). If not, a 422 error with code DM_NOT_ALLOWED is returned. Skip this check with skipDmCheck: true if you have already verified eligibility.  #### API tier requirement  DM write endpoints require X API Pro tier ($5,000/month) or Enterprise access. This applies to BYOK (Bring Your Own Key) users who provide their own X API credentials.  #### Rate limits (X only)  X's DM API enforces, shared across all DM endpoints:  - 200 requests per 15 minutes per connected X account - 1,000 per 24 hours per connected X account - 15,000 per 24 hours per X developer app  These limits do NOT apply to other platforms. WhatsApp sends are governed by Meta's per-number messaging tiers (unique business-initiated conversations per 24 hours) and per-number throughput instead. 

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
    public class CreateInboxConversationExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var createInboxConversationRequest = new CreateInboxConversationRequest(); // CreateInboxConversationRequest | 

            try
            {
                // Create conversation
                CreateInboxConversation201Response result = apiInstance.CreateInboxConversation(createInboxConversationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.CreateInboxConversation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateInboxConversationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create conversation
    ApiResponse<CreateInboxConversation201Response> response = apiInstance.CreateInboxConversationWithHttpInfo(createInboxConversationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.CreateInboxConversationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createInboxConversationRequest** | [**CreateInboxConversationRequest**](CreateInboxConversationRequest.md) |  |  |

### Return type

[**CreateInboxConversation201Response**](CreateInboxConversation201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json, multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Conversation created successfully |  -  |
| **400** | Validation error or platform not supported. Specific cases:  - PLATFORM_LIMITATION: an attachment the platform does not accept. - TEMPLATE_REQUIRED: a template is required to start a WhatsApp conversation. - INVALID_TEMPLATE_PARAMS, INVALID_TEMPLATE_BUTTON_PARAM: template variables do not match the approved definition. - INVALID_TEMPLATE_HEADER: a required template header is missing or incompatible. - INVALID_TEMPLATE_CARD_PARAM: templateCards do not match the approved carousel definition. - category combined with templateName, or used on a non-WhatsApp account. - DIRECT_SEND_NOT_ELIGIBLE, DIRECT_SEND_BLOCKED: the WhatsApp Business Account is not eligible for Direct Send; Meta must grant or restore access. - DIRECT_SEND_LIMITED: temporary, lifts on its own. - invalid_content: an iMessage first message to a new contact breaks the content rule.  |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required, profile limit reached, or a sandbox send with a template other than the locked sandbox template |  -  |
| **404** | Account or recipient user not found (Reddit: PARTICIPANT_NOT_FOUND when the u/username does not exist) |  -  |
| **409** | iMessage only. The contact opted out of this sender (recipient_opted_out); or this contact has never written to the sender and either the sender lacks the add-on for new contacts or three messages already went out and the contact has not replied (recipient_must_message_first). |  -  |
| **422** | Recipient does not accept DMs from this account (X), or does not accept direct messages from you (Reddit) |  -  |
| **429** | X API rate limit exceeded, Reddit rate limit reached, Meta rejected the WhatsApp template-definition lookup (a lookup failure sends no message), or an iMessage sender reached its new-contact pacing or warm-up limit (new_contact_limit; the error says when to retry). |  -  |
| **502** | The WhatsApp account has no Business Account ID, so the template definition cannot be looked up (a template with no approved variant in that language is a 400). No message was sent. |  -  |
| **0** | Meta rejected the WhatsApp template-definition lookup with another upstream status. No message was sent. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createinboxlabel"></a>
# **CreateInboxLabel**
> CreateInboxLabel201Response CreateInboxLabel (CreateInboxLabelRequest createInboxLabelRequest)

Create a conversation label

Facebook Messenger only. Creates a custom label on the Page (Graph `POST /{page-id}/custom_labels`). Other platforms answer 400 `platform_not_supported`.

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
    public class CreateInboxLabelExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var createInboxLabelRequest = new CreateInboxLabelRequest(); // CreateInboxLabelRequest | 

            try
            {
                // Create a conversation label
                CreateInboxLabel201Response result = apiInstance.CreateInboxLabel(createInboxLabelRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.CreateInboxLabel: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateInboxLabelWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a conversation label
    ApiResponse<CreateInboxLabel201Response> response = apiInstance.CreateInboxLabelWithHttpInfo(createInboxLabelRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.CreateInboxLabelWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createInboxLabelRequest** | [**CreateInboxLabelRequest**](CreateInboxLabelRequest.md) |  |  |

### Return type

[**CreateInboxLabel201Response**](CreateInboxLabel201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Label created |  -  |
| **400** | Invalid body, or an account that is not Facebook (platform_not_supported), or Meta refusing for good (platform_api_error with Meta&#39;s error_user_title and error_user_msg in the message, e.g. the Page has not accepted the label privacy terms, subcode 2018344, in platformError). A transient Meta failure answers 502 |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account not found |  -  |
| **422** | No Facebook Page is selected on this account (linked_account_required); reconnect it and select the Page |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteinboxconversation"></a>
# **DeleteInboxConversation**
> DeleteInboxConversation200Response DeleteInboxConversation (string conversationId, string accountId)

Delete conversation

Permanently deletes Zernio's stored copy of one conversation and every message in it, in one transaction, and unlinks the contact channel that pointed at it.  ### What is kept  - Nothing is deleted on the platform (the thread stays in WhatsApp, Messenger or Instagram). - The contact record is kept: call DELETE /v1/contacts/{contactId} to erase the person's name and number as well.  Inbound media copies Zernio stored are removed on a best-effort basis.  ### Re-imports  A platform re-sync can import the thread again:  - WhatsApp coexistence numbers receive their messaging history from Meta repeatedly. - A Facebook or Instagram account whose DM history walk has not finished imports it on that walk. 

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
    public class DeleteInboxConversationExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed.
            var accountId = "accountId_example";  // string | Account ID

            try
            {
                // Delete conversation
                DeleteInboxConversation200Response result = apiInstance.DeleteInboxConversation(conversationId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.DeleteInboxConversation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteInboxConversationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete conversation
    ApiResponse<DeleteInboxConversation200Response> response = apiInstance.DeleteInboxConversationWithHttpInfo(conversationId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.DeleteInboxConversationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed. |  |
| **accountId** | **string** | Account ID |  |

### Return type

[**DeleteInboxConversation200Response**](DeleteInboxConversation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Conversation deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account or conversation not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteinboxlabel"></a>
# **DeleteInboxLabel**
> UpdateYoutubeDefaultPlaylist200Response DeleteInboxLabel (string labelId, string accountId)

Delete a conversation label

Facebook Messenger only. Deletes a custom label from the Page (Graph `DELETE /{label-id}`), which also removes it from every conversation. The id must be one of the Page's custom labels, otherwise 404 `resource_not_found`. Other platforms answer 400 `platform_not_supported`.

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
    public class DeleteInboxLabelExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var labelId = "labelId_example";  // string | Meta label id
            var accountId = "accountId_example";  // string | Facebook social account ID

            try
            {
                // Delete a conversation label
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.DeleteInboxLabel(labelId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.DeleteInboxLabel: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteInboxLabelWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a conversation label
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.DeleteInboxLabelWithHttpInfo(labelId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.DeleteInboxLabelWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **labelId** | **string** | Meta label id |  |
| **accountId** | **string** | Facebook social account ID |  |

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
| **200** | Label deleted |  -  |
| **400** | Invalid id, or an account that is not Facebook (platform_not_supported), or Meta refusing for good (platform_api_error with Meta&#39;s error_user_title and error_user_msg in the message, e.g. the Page has not accepted the label privacy terms, subcode 2018344, in platformError). A transient Meta failure answers 502 |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account not found, or the label is not one of the Page&#39;s custom labels |  -  |
| **422** | No Facebook Page is selected on this account (linked_account_required); reconnect it and select the Page |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteinboxmessage"></a>
# **DeleteInboxMessage**
> UpdateYoutubeDefaultPlaylist200Response DeleteInboxMessage (string conversationId, string messageId, string accountId)

Delete message

Delete a message from a conversation. Platform support varies:  - Telegram: full delete (bot's own messages anytime, others if admin) - X: full delete (own DM events only) - Bluesky: delete for self only (recipient still sees it) - Reddit: delete from sender's view only - iMessage: unsend (the bubble disappears for the recipient) within 2 minutes of sending (Apple's limit; 409 `unsend_window_expired` after that). Own outbound messages only. - Facebook, Instagram, WhatsApp: not supported (returns 400) 

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
    public class DeleteInboxMessageExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | The conversation ID
            var messageId = "messageId_example";  // string | The platform message ID to delete
            var accountId = "accountId_example";  // string | Account ID

            try
            {
                // Delete message
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.DeleteInboxMessage(conversationId, messageId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.DeleteInboxMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteInboxMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete message
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.DeleteInboxMessageWithHttpInfo(conversationId, messageId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.DeleteInboxMessageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | The conversation ID |  |
| **messageId** | **string** | The platform message ID to delete |  |
| **accountId** | **string** | Account ID |  |

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
| **200** | Message deleted |  -  |
| **400** | Platform does not support deletion or invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account or conversation not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="editinboxmessage"></a>
# **EditInboxMessage**
> EditInboxMessage200Response EditInboxMessage (string conversationId, string messageId, EditInboxMessageRequest editInboxMessageRequest)

Edit message

Edit a previously sent message. Platform support: - Telegram: text and/or reply markup, any time - 'iMessage: text only, within 15 minutes of sending (Apple''s limit; 409 `edit_window_expired` after that). Group messages included. The stored message keeps its edit history.' - All others: returns 400 

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
    public class EditInboxMessageExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | The conversation ID
            var messageId = "messageId_example";  // string | The platform message ID to edit (iMessage also accepts the Zernio message id)
            var editInboxMessageRequest = new EditInboxMessageRequest(); // EditInboxMessageRequest | 

            try
            {
                // Edit message
                EditInboxMessage200Response result = apiInstance.EditInboxMessage(conversationId, messageId, editInboxMessageRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.EditInboxMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EditInboxMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Edit message
    ApiResponse<EditInboxMessage200Response> response = apiInstance.EditInboxMessageWithHttpInfo(conversationId, messageId, editInboxMessageRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.EditInboxMessageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | The conversation ID |  |
| **messageId** | **string** | The platform message ID to edit (iMessage also accepts the Zernio message id) |  |
| **editInboxMessageRequest** | [**EditInboxMessageRequest**](EditInboxMessageRequest.md) |  |  |

### Return type

[**EditInboxMessage200Response**](EditInboxMessage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Message edited |  -  |
| **400** | Not supported or invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getinboxconversation"></a>
# **GetInboxConversation**
> GetInboxConversation200Response GetInboxConversation (string conversationId, string accountId)

Get conversation

Retrieve details and metadata for a specific conversation. Requires accountId query parameter.

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
    public class GetInboxConversationExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed.
            var accountId = "accountId_example";  // string | The account ID

            try
            {
                // Get conversation
                GetInboxConversation200Response result = apiInstance.GetInboxConversation(conversationId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.GetInboxConversation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInboxConversationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get conversation
    ApiResponse<GetInboxConversation200Response> response = apiInstance.GetInboxConversationWithHttpInfo(conversationId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.GetInboxConversationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed. |  |
| **accountId** | **string** | The account ID |  |

### Return type

[**GetInboxConversation200Response**](GetInboxConversation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Conversation details |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Conversation not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getinboxconversationmessages"></a>
# **GetInboxConversationMessages**
> GetInboxConversationMessages200Response GetInboxConversationMessages (string conversationId, string accountId, int? limit = null, string? cursor = null, string? sortOrder = null)

List messages

Fetch messages for a specific conversation, with cursor-based pagination and ordering control.  ### Pagination  Pass `pagination.nextCursor` from a prior response back as the `cursor` query param to fetch the next page. The cursor is opaque; do not parse or construct it client-side.  ### Sort order  Defaults to `asc` (oldest first, chat style). For the \"show me the latest messages\" pattern, pass `?sortOrder=desc&limit=N`.  - X, Instagram, Telegram, WhatsApp and Reddit honor the requested order from the local message store. - Facebook and Bluesky upstream APIs only return newest-first and have no order parameter. Sort order is best-effort and only reverses items within a single page (pages still walk newest→oldest).  The response field `sortOrderApplied` tells you what was actually applied.  ### Platform limits  - **Reddit**: threads are paginated client-side because Reddit's API has no per-thread cursor. Very long threads may be upstream-truncated by Reddit's inbox/sent windows (~100 most-recent items each); this is a Reddit platform limitation. - **Instagram and Facebook**: conversations include history from before the account was connected, replayed from Meta. See below. - **X**: X's encrypted \"X Chat\" messages are not accessible via the API. Conversations where the other participant uses encrypted X Chat may only show your outgoing messages. See the list conversations endpoint for more details.  The Meta replay covers the 500 most recent messages per conversation: a longer thread keeps its newest 500 and older messages are not retrievable. Messages that arrived after the account was connected are unaffected. Replayed messages are stored as already read and emit no webhooks.  ### Read state  This endpoint is read-only and does NOT mark messages as read or send read receipts. To mark a conversation read (and send WhatsApp blue ticks on eligible accounts), call `POST /v1/inbox/conversations/{conversationId}/read`. 

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
    public class GetInboxConversationMessagesExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed.
            var accountId = "accountId_example";  // string | Account ID
            var limit = 100;  // int? | Number of messages to return per page. Default 100, max 100. (optional)  (default to 100)
            var cursor = "cursor_example";  // string? | Opaque pagination cursor. Pass `pagination.nextCursor` from a prior response verbatim: a cursor we cannot parse returns 400 rather than silently restarting from the first page. (optional) 
            var sortOrder = "asc";  // string? | Order of returned messages. Default `asc` (oldest first, chat style). X, Instagram, Telegram, WhatsApp and Reddit honor this order across cursor pages. For Facebook and Bluesky, only intra-page ordering is affected. Pages always walk newest→oldest. See `sortOrderApplied` in the response.  (optional)  (default to asc)

            try
            {
                // List messages
                GetInboxConversationMessages200Response result = apiInstance.GetInboxConversationMessages(conversationId, accountId, limit, cursor, sortOrder);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.GetInboxConversationMessages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInboxConversationMessagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List messages
    ApiResponse<GetInboxConversationMessages200Response> response = apiInstance.GetInboxConversationMessagesWithHttpInfo(conversationId, accountId, limit, cursor, sortOrder);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.GetInboxConversationMessagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed. |  |
| **accountId** | **string** | Account ID |  |
| **limit** | **int?** | Number of messages to return per page. Default 100, max 100. | [optional] [default to 100] |
| **cursor** | **string?** | Opaque pagination cursor. Pass &#x60;pagination.nextCursor&#x60; from a prior response verbatim: a cursor we cannot parse returns 400 rather than silently restarting from the first page. | [optional]  |
| **sortOrder** | **string?** | Order of returned messages. Default &#x60;asc&#x60; (oldest first, chat style). X, Instagram, Telegram, WhatsApp and Reddit honor this order across cursor pages. For Facebook and Bluesky, only intra-page ordering is affected. Pages always walk newest→oldest. See &#x60;sortOrderApplied&#x60; in the response.  | [optional] [default to asc] |

### Return type

[**GetInboxConversationMessages200Response**](GetInboxConversationMessages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Messages in conversation |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **502** | The platform returned a server error. |  -  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getmessageattachment"></a>
# **GetMessageAttachment**
> GetMessageAttachment200Response GetMessageAttachment (string conversationId, string messageId, int index, string accountId, string? format = null)

Resolve message attachment

Resolve one attachment on a message to a media url that works right now.  ### Why it exists  Instagram and Facebook sign DM media urls per request and expire them. So the `url` on a message is a snapshot: it works when you read the message and stops working later.  This endpoint checks the stored url and, when it has gone stale, re-mints the message's media from Meta and persists it before answering.  The message id never expires, so this URL is the one to store. It is returned ready-made on each attachment as `refreshUrl` when you read a message over REST.  ### Building the URL from a webhook  **Webhook payloads do not carry `refreshUrl`**, so a webhook-driven integration builds this URL itself. Every piece is in the event:  - `message.conversationId` - `message.platformMessageId` - the attachment's zero-based position - `account.accountId`  **`accountId` is a required query parameter**. Omitting it returns `400` `missing_required_field`, which is the same requirement `GET /v1/whatsapp/media/{mediaId}` has.  ### Response format  - By default it responds `302` to the live media url, so it can be used directly as an `<img src>` on a browser session. - API-key integrators should pass `?format=json` and read `url` off the body, since a browser cannot attach an Authorization header to an image request.  ### Other platforms  Only Instagram and Facebook media can be re-minted. On other platforms the stored url is returned as-is when it still resolves, and `404` otherwise. 

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
    public class GetMessageAttachmentExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | The conversation ID (Zernio id or platform conversation id)
            var messageId = "messageId_example";  // string | The message id as returned by the list-messages endpoint (the platform message id)
            var index = 56;  // int | Zero-based position of the attachment in the message's attachments array
            var accountId = "accountId_example";  // string | Account ID. Required: without it the request returns 400 missing_required_field.
            var format = "redirect";  // string? | `redirect` (default) answers 302 to the media; `json` returns the url in the body (optional)  (default to redirect)

            try
            {
                // Resolve message attachment
                GetMessageAttachment200Response result = apiInstance.GetMessageAttachment(conversationId, messageId, index, accountId, format);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.GetMessageAttachment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetMessageAttachmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resolve message attachment
    ApiResponse<GetMessageAttachment200Response> response = apiInstance.GetMessageAttachmentWithHttpInfo(conversationId, messageId, index, accountId, format);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.GetMessageAttachmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | The conversation ID (Zernio id or platform conversation id) |  |
| **messageId** | **string** | The message id as returned by the list-messages endpoint (the platform message id) |  |
| **index** | **int** | Zero-based position of the attachment in the message&#39;s attachments array |  |
| **accountId** | **string** | Account ID. Required: without it the request returns 400 missing_required_field. |  |
| **format** | **string?** | &#x60;redirect&#x60; (default) answers 302 to the media; &#x60;json&#x60; returns the url in the body | [optional] [default to redirect] |

### Return type

[**GetMessageAttachment200Response**](GetMessageAttachment200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Resolved url (only when format&#x3D;json) |  -  |
| **302** | Redirect to the live media url |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account, conversation, message or attachment not found, or the platform no longer serves the media |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listconversationlabels"></a>
# **ListConversationLabels**
> ListInboxLabels200Response ListConversationLabels (string conversationId, string accountId)

List the labels on a conversation

Facebook Messenger only. Lists the Page's custom labels applied to the person in this conversation (Graph `/{psid}/custom_labels`). Other platforms answer 400 `platform_not_supported`.

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
    public class ListConversationLabelsExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | Conversation ID (Zernio id or Meta platform conversation id)
            var accountId = "accountId_example";  // string | Facebook social account ID

            try
            {
                // List the labels on a conversation
                ListInboxLabels200Response result = apiInstance.ListConversationLabels(conversationId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.ListConversationLabels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListConversationLabelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List the labels on a conversation
    ApiResponse<ListInboxLabels200Response> response = apiInstance.ListConversationLabelsWithHttpInfo(conversationId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.ListConversationLabelsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | Conversation ID (Zernio id or Meta platform conversation id) |  |
| **accountId** | **string** | Facebook social account ID |  |

### Return type

[**ListInboxLabels200Response**](ListInboxLabels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The labels on the conversation&#39;s participant |  -  |
| **400** | Invalid accountId, or an account that is not Facebook (platform_not_supported), or Meta refusing for good (platform_api_error with Meta&#39;s message, e.g. the Page has not accepted the label privacy terms, subcode 2018344, in platformError). A transient Meta failure answers 502 |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account or conversation not found |  -  |
| **422** | No Facebook Page is selected on this account (linked_account_required); reconnect it and select the Page |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listinboxconversations"></a>
# **ListInboxConversations**
> ListInboxConversations200Response ListInboxConversations (string? profileId = null, string? platform = null, string? status = null, string? folder = null, string? sortOrder = null, int? limit = null, string? cursor = null, string? accountId = null, string? tags = null)

List conversations

Fetch conversations (DMs) from all connected messaging accounts in a single API call. Supports filtering by profile and platform. Results are aggregated and deduplicated.  Supported platforms: Facebook, Instagram, X, Bluesky, Reddit, Telegram, WhatsApp, iMessage and SMS.  ### X limitation  X has replaced traditional DMs with encrypted \"X Chat\" for many accounts. Messages sent or received through encrypted X Chat are not accessible via X's API (the /2/dm_events endpoint only returns legacy unencrypted DMs).  This means some X conversations may show only outgoing messages or appear empty. This is an X platform limitation that affects all third-party applications. See X's docs on encrypted messaging for more details.  ### Instagram and Facebook pre-connect history  When one of these accounts is connected, Zernio replays the DM history the account already holds on Meta, so conversations that began before the account was connected appear here. Up to 500 conversations per account are replayed.  - The replay runs in the background and can finish after a listing you have already taken. - Replayed conversations keep their original lastMessageAt, so they sort into date order rather than appearing at the top. - If you mirror this endpoint into your own store, re-run the sweep rather than relying on a single pass at connect time. - Replayed history emits no webhooks and is stored as already read, so it never affects unread counts. - Threads that Meta refuses to serve are skipped. - An account whose Instagram \"connected tools\" message access is turned off is not replayed at all. 

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
    public class ListInboxConversationsExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? | Filter by profile ID (optional) 
            var platform = "facebook";  // string? | Filter by platform (optional) 
            var status = "active";  // string? | Filter by conversation status (optional) 
            var folder = "inbox";  // string? | `requests` lists Facebook Page Message Requests (threads from people the account has not accepted) live from Meta, each item with `folder: requests`.  Meta has no accept call: replying moves a thread to the inbox, which is what POST /v1/inbox/conversations/{conversationId}/accept does.  - When Meta will not list the folder for the one account asked (`accountId`), the call answers 400 PLATFORM_LIMITATION. Across several accounts, the refusal is reported per account in meta.failedAccounts. - Instagram accounts (Instagram Login and Facebook Login) answer PLATFORM_LIMITATION, because Meta does not separate the folder on Instagram. Only Facebook Pages are served.  One page of up to `limit` threads. `pagination.hasMore` is true when threads past `limit` were cut (narrow with `accountId`). `pagination.nextCursor` is always null and a `cursor` answers 400.  (optional)  (default to inbox)
            var sortOrder = "asc";  // string? | Sort order by updated time (optional)  (default to desc)
            var limit = 50;  // int? | Maximum number of conversations to return; values above 100 are served as 100. (optional)  (default to 50)
            var cursor = "cursor_example";  // string? | Pagination cursor for next page (optional) 
            var accountId = "accountId_example";  // string? | Filter by specific account ID (optional) 
            var tags = "tags_example";  // string? | Comma-separated contact tags. Returns only conversations whose contact has any of them. Cannot be combined with folder=requests. (optional) 

            try
            {
                // List conversations
                ListInboxConversations200Response result = apiInstance.ListInboxConversations(profileId, platform, status, folder, sortOrder, limit, cursor, accountId, tags);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.ListInboxConversations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListInboxConversationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List conversations
    ApiResponse<ListInboxConversations200Response> response = apiInstance.ListInboxConversationsWithHttpInfo(profileId, platform, status, folder, sortOrder, limit, cursor, accountId, tags);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.ListInboxConversationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** | Filter by profile ID | [optional]  |
| **platform** | **string?** | Filter by platform | [optional]  |
| **status** | **string?** | Filter by conversation status | [optional]  |
| **folder** | **string?** | &#x60;requests&#x60; lists Facebook Page Message Requests (threads from people the account has not accepted) live from Meta, each item with &#x60;folder: requests&#x60;.  Meta has no accept call: replying moves a thread to the inbox, which is what POST /v1/inbox/conversations/{conversationId}/accept does.  - When Meta will not list the folder for the one account asked (&#x60;accountId&#x60;), the call answers 400 PLATFORM_LIMITATION. Across several accounts, the refusal is reported per account in meta.failedAccounts. - Instagram accounts (Instagram Login and Facebook Login) answer PLATFORM_LIMITATION, because Meta does not separate the folder on Instagram. Only Facebook Pages are served.  One page of up to &#x60;limit&#x60; threads. &#x60;pagination.hasMore&#x60; is true when threads past &#x60;limit&#x60; were cut (narrow with &#x60;accountId&#x60;). &#x60;pagination.nextCursor&#x60; is always null and a &#x60;cursor&#x60; answers 400.  | [optional] [default to inbox] |
| **sortOrder** | **string?** | Sort order by updated time | [optional] [default to desc] |
| **limit** | **int?** | Maximum number of conversations to return; values above 100 are served as 100. | [optional] [default to 50] |
| **cursor** | **string?** | Pagination cursor for next page | [optional]  |
| **accountId** | **string?** | Filter by specific account ID | [optional]  |
| **tags** | **string?** | Comma-separated contact tags. Returns only conversations whose contact has any of them. Cannot be combined with folder&#x3D;requests. | [optional]  |

### Return type

[**ListInboxConversations200Response**](ListInboxConversations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Aggregated conversations |  -  |
| **400** | Invalid query, a platform without direct messages (PLATFORM_NOT_SUPPORTED), or folder&#x3D;requests on one account Meta will not list the folder for (PLATFORM_LIMITATION). |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listinboxlabels"></a>
# **ListInboxLabels**
> ListInboxLabels200Response ListInboxLabels (string accountId)

List the Page's conversation labels

Facebook Messenger only. Lists the custom labels defined on the Page (Graph `/{page-id}/custom_labels`). Other platforms answer 400 `platform_not_supported`.

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
    public class ListInboxLabelsExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Facebook social account ID

            try
            {
                // List the Page's conversation labels
                ListInboxLabels200Response result = apiInstance.ListInboxLabels(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.ListInboxLabels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListInboxLabelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List the Page's conversation labels
    ApiResponse<ListInboxLabels200Response> response = apiInstance.ListInboxLabelsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.ListInboxLabelsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Facebook social account ID |  |

### Return type

[**ListInboxLabels200Response**](ListInboxLabels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The Page&#39;s labels |  -  |
| **400** | Invalid accountId, or an account that is not Facebook (platform_not_supported), or Meta refusing for good (platform_api_error with Meta&#39;s error_user_title and error_user_msg in the message, e.g. the Page has not accepted the label privacy terms, subcode 2018344, in platformError). A transient Meta failure answers 502 |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account not found |  -  |
| **422** | No Facebook Page is selected on this account (linked_account_required); reconnect it and select the Page |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="markconversationread"></a>
# **MarkConversationRead**
> MarkConversationRead200Response MarkConversationRead (string conversationId, SendTypingIndicatorRequest sendTypingIndicatorRequest)

Mark a conversation as read

Marks all unread incoming messages in the conversation as read.  For WhatsApp, this also sends read receipts (blue ticks) to the contact, EXCEPT on coexistence accounts (where the WhatsApp Business app on the customer's phone owns read state and we never override it).  For iMessage, this also marks the conversation read with the contact (1:1 conversations only). Best-effort.  For Instagram (Instagram Login and Facebook Login) and Facebook Messenger, this also sends a `mark_seen` read receipt to the contact, so they see the conversation as seen. Best-effort: a Meta failure never fails the request.  This is the explicit, human-driven counterpart to `GET .../messages`, which is side-effect-free and does NOT mark anything read. Call this when a user actually views the conversation. 

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
    public class MarkConversationReadExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | The conversation ID
            var sendTypingIndicatorRequest = new SendTypingIndicatorRequest(); // SendTypingIndicatorRequest | 

            try
            {
                // Mark a conversation as read
                MarkConversationRead200Response result = apiInstance.MarkConversationRead(conversationId, sendTypingIndicatorRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.MarkConversationRead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MarkConversationReadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mark a conversation as read
    ApiResponse<MarkConversationRead200Response> response = apiInstance.MarkConversationReadWithHttpInfo(conversationId, sendTypingIndicatorRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.MarkConversationReadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | The conversation ID |  |
| **sendTypingIndicatorRequest** | [**SendTypingIndicatorRequest**](SendTypingIndicatorRequest.md) |  |  |

### Return type

[**MarkConversationRead200Response**](MarkConversationRead200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Conversation marked read |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account or conversation not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removeconversationlabel"></a>
# **RemoveConversationLabel**
> UpdateYoutubeDefaultPlaylist200Response RemoveConversationLabel (string conversationId, string labelId, string accountId)

Remove a label from a conversation

Facebook Messenger only. Removes one of the Page's custom labels from the person in this conversation (Graph `DELETE /{label-id}/label?user={psid}`). The label itself stays on the Page. The id must be one of the Page's custom labels, otherwise 404 `resource_not_found`. Other platforms answer 400 `platform_not_supported`.

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
    public class RemoveConversationLabelExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | Conversation ID (Zernio id or Meta platform conversation id)
            var labelId = "labelId_example";  // string | Meta label id
            var accountId = "accountId_example";  // string | Facebook social account ID

            try
            {
                // Remove a label from a conversation
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.RemoveConversationLabel(conversationId, labelId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.RemoveConversationLabel: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveConversationLabelWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove a label from a conversation
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.RemoveConversationLabelWithHttpInfo(conversationId, labelId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.RemoveConversationLabelWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | Conversation ID (Zernio id or Meta platform conversation id) |  |
| **labelId** | **string** | Meta label id |  |
| **accountId** | **string** | Facebook social account ID |  |

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
| **200** | Label removed |  -  |
| **400** | Invalid id, or an account that is not Facebook (platform_not_supported), or Meta refusing for good (platform_api_error with Meta&#39;s message in platformError). A transient Meta failure answers 502 |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account or conversation not found, or the label is not one of the Page&#39;s custom labels |  -  |
| **422** | No Facebook Page is selected on this account (linked_account_required); reconnect it and select the Page |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removemessagereaction"></a>
# **RemoveMessageReaction**
> RemoveMessageReaction200Response RemoveMessageReaction (string conversationId, string messageId, string accountId)

Remove reaction

Remove a reaction from a message.  ### Platform support  - Telegram: send empty reaction array to clear - WhatsApp: send empty emoji to remove - Instagram and Facebook Messenger: sends Meta's `unreact` action; the emoji does not need to be repeated - Slack: removes the reaction we previously sent on that message - iMessage: retracts your existing tapback or emoji reaction on the message (400 when you have none) - All others: returns 400 (not supported) 

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
    public class RemoveMessageReactionExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | The conversation ID
            var messageId = "messageId_example";  // string | The platform message ID (as returned by GET /messages) or the Zernio message ID (as returned by the reaction webhook)
            var accountId = "accountId_example";  // string | Account ID

            try
            {
                // Remove reaction
                RemoveMessageReaction200Response result = apiInstance.RemoveMessageReaction(conversationId, messageId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.RemoveMessageReaction: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveMessageReactionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove reaction
    ApiResponse<RemoveMessageReaction200Response> response = apiInstance.RemoveMessageReactionWithHttpInfo(conversationId, messageId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.RemoveMessageReactionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | The conversation ID |  |
| **messageId** | **string** | The platform message ID (as returned by GET /messages) or the Zernio message ID (as returned by the reaction webhook) |  |
| **accountId** | **string** | Account ID |  |

### Return type

[**RemoveMessageReaction200Response**](RemoveMessageReaction200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The platform accepted the removal request. This does not guarantee a reaction was removed: the platform never confirms what it acted on, and a reaction placed by the other participant cannot be removed (platform rule). Check &#x60;fromMe&#x60; on GET /messages to know who placed a reaction. |  -  |
| **400** | Platform does not support reactions or invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account, conversation or message not found (message_not_found when messageId does not resolve to a message in this conversation) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="searchinboxconversations"></a>
# **SearchInboxConversations**
> SearchInboxConversations200Response SearchInboxConversations (string query, string? direction = null, string? profileId = null, string? platform = null, string? accountId = null, int? limit = null, string? cursor = null)

Search conversations

Search your conversations two ways at once, and get back the matching conversations, most-recent match first.  ### Message text  Matches words inside message bodies. Case-insensitive and accent-insensitive, exact tokens only (no substrings, no stemming). Each hit carries up to 3 most-recent matching messages.  With direction=outgoing you can collect examples of how you write to customers, for example to teach an AI agent your tone of voice.  ### Contact identity  Matches the participant's name, username, or phone number as a case-insensitive substring. These hits have matchCount 0 and an empty matches array.  A conversation that matches both ways is returned once, carrying its message matches.  ### Searchable platforms  Only platforms whose messages are stored by Zernio are searchable: WhatsApp, SMS, Telegram, Facebook, Instagram, X and Reddit.  Bluesky conversations are fetched live from the platform and cannot be searched; those accounts are listed in meta.accountsSkipped. 

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
    public class SearchInboxConversationsExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Text to search for, in message content and in the contact's name, username, or phone number
            var direction = "incoming";  // string? | Only match messages sent to you (incoming) or by you (outgoing). Contact-identity matching is not applied when this is set. (optional) 
            var profileId = "profileId_example";  // string? | Filter by profile ID (optional) 
            var platform = "facebook";  // string? | Filter by platform (searchable platforms only) (optional) 
            var accountId = "accountId_example";  // string? | Filter by specific account ID (optional) 
            var limit = 20;  // int? | Maximum number of conversations to return (optional)  (default to 20)
            var cursor = "cursor_example";  // string? | Opaque pagination cursor. Pass back pagination.nextCursor verbatim; do not construct one. (optional) 

            try
            {
                // Search conversations
                SearchInboxConversations200Response result = apiInstance.SearchInboxConversations(query, direction, profileId, platform, accountId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.SearchInboxConversations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchInboxConversationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search conversations
    ApiResponse<SearchInboxConversations200Response> response = apiInstance.SearchInboxConversationsWithHttpInfo(query, direction, profileId, platform, accountId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.SearchInboxConversationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Text to search for, in message content and in the contact&#39;s name, username, or phone number |  |
| **direction** | **string?** | Only match messages sent to you (incoming) or by you (outgoing). Contact-identity matching is not applied when this is set. | [optional]  |
| **profileId** | **string?** | Filter by profile ID | [optional]  |
| **platform** | **string?** | Filter by platform (searchable platforms only) | [optional]  |
| **accountId** | **string?** | Filter by specific account ID | [optional]  |
| **limit** | **int?** | Maximum number of conversations to return | [optional] [default to 20] |
| **cursor** | **string?** | Opaque pagination cursor. Pass back pagination.nextCursor verbatim; do not construct one. | [optional]  |

### Return type

[**SearchInboxConversations200Response**](SearchInboxConversations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Conversations containing the query, most recent match first |  -  |
| **400** | Invalid query, unsupported platform, or malformed cursor |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sendinboxmessage"></a>
# **SendInboxMessage**
> SendInboxMessage200Response SendInboxMessage (string conversationId, SendInboxMessageRequest sendInboxMessageRequest, string? idempotencyKey = null)

Send message

Send a message in a conversation. Supports text, attachments, quick replies, buttons, templates, and message tags. Attachment and interactive message support varies by platform.  ### Email threads (Google / Microsoft accounts)  The text is sent as a reply to the latest mail of the thread, in either direction, with its recipients and a \"Re:\" subject. `cc` adds recipients. `message` is required.  - 400: attachments and `replyTo` are rejected here (use POST /v1/email/messages/{messageId}/reply for a reply with attachments) - 412 `account_scope_missing`: the account was connected without the `email` area - 409: the account is disconnected - 402: a Gmail account without a card on file  Mail sends count toward the mailbox's daily cap, never toward managed messages.  ### WhatsApp per-recipient rate limit  WhatsApp caps how many messages you may send to the same recipient in a short window. It rejects the excess with error code `131056` (\"Too many messages sent to this recipient\").  Pace sends to a single recipient at roughly 10 per minute; bursts above that return a `400` with code `131056`. Sends to other recipients are unaffected, so parallelise across recipients rather than flooding one.  ### iMessage pacing  Messages to contacts who have not written to the sender in the last 24 hours must be at least 2 minutes apart per sender.  A send inside that window returns `429` with code `new_contact_limit` and the time to retry. Replies to contacts who wrote within the last day are not paced.  A thread opened with `POST /v1/inbox/conversations` takes at most two follow-ups before the contact replies, at least 24 hours apart:  - `429 new_contact_limit`: a follow-up sent sooner - `409 recipient_must_message_first`: a fourth message  Each such follow-up counts as a new conversation:  - No links, emails, phone numbers, prices or attachments (`400 invalid_content`). - It uses the sender's 15-minute spacing and daily warm-up (`429 new_contact_limit`).  Text must be shorter than 10,000 characters.  ### WhatsApp template messages  To send an approved template into this conversation (required when the 24-hour customer-service window is closed), use the `template` field with a single element carrying the template reference: `{ \"elements\": [{ \"name\": ..., \"language\": ..., \"components\": [...] }] }`. See the `template` field below for the exact shape.  To send a template to a phone number you have no conversation with yet, use the create-conversation endpoint (POST /v1/inbox/conversations) instead.  #### Template lookup  Zernio resolves the exact APPROVED template name and language before any WhatsApp template send. A failed lookup or missing exact definition sends no message and returns code `platform_api_error`, type `platform_error`, and platform `whatsapp`.  Sanitized Meta code, message, and `error_data.details` are returned in `platformError`. `details` identifies `phase: template_lookup`, the query-free endpoint, upstream status, and only safe provider usage or retry headers.  ### WhatsApp interactive messages  Rich interactive messages (list, CTA URL, Flow, location request) are available via the `interactive` field. Tap events are delivered through the `message.received` webhook with WhatsApp-specific `metadata` fields (`interactiveType`, `interactiveId`, `flowResponseJson`, `flowResponseData`).  ### Idempotency  Send an `Idempotency-Key` header to make retries safe (e.g. after a client-side timeout where delivery is unknown). Works for JSON and multipart (file upload) requests alike. Keys are retained for 24 hours.  - Same key + same body: replays the original response (with `Idempotent-Replayed: true`) instead of sending the message a second time. - Same key + different body: returns 422. - A key still in flight: returns 409.  Only successful (2xx) responses are stored for replay. If the request throws or returns a non-2xx status, the key is released so the same key can be retried once the problem is fixed. The header therefore protects the \"request succeeded but the response was lost\" case.  For an ambiguous failure (a 5xx or a network timeout), reconcile before retrying. A failure after the platform already accepted the message also releases the key, so a blind retry could send it twice.  List the conversation's messages first. Treat an empty result as inconclusive rather than as proof nothing was sent, since a send that failed while being recorded leaves no trace on our side. 

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
    public class SendInboxMessageExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed.
            var sendInboxMessageRequest = new SendInboxMessageRequest(); // SendInboxMessageRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  (optional) 

            try
            {
                // Send message
                SendInboxMessage200Response result = apiInstance.SendInboxMessage(conversationId, sendInboxMessageRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.SendInboxMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendInboxMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send message
    ApiResponse<SendInboxMessage200Response> response = apiInstance.SendInboxMessageWithHttpInfo(conversationId, sendInboxMessageRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.SendInboxMessageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed. |  |
| **sendInboxMessageRequest** | [**SendInboxMessageRequest**](SendInboxMessageRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  | [optional]  |

### Return type

[**SendInboxMessage200Response**](SendInboxMessage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json, multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Message sent |  -  |
| **400** | Bad request, e.g.:  - Attachment not supported for the platform, or a validation error. - Category combined with a template or attachment, or used on a non-WhatsApp account. - The WhatsApp Business Account is not eligible for Direct Send.  Meta rejections (e.g. sending outside the messaging window) and TikTok business-account rejections arrive with code platform_api_error, type platform_error, and platform + platformError set.  |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required, a sandbox send with a template other than the locked sandbox template, or Meta rejected the send outside the messaging window (type platform_error, code platform_api_error, platform, platformError with code/subcode/fbtraceId/type) |  -  |
| **409** | Conflict. One of:  - The same Idempotency-Key is still processing. Retry after a short backoff. - On Facebook and Instagram, another app owns the thread under Meta&#39;s handover protocol (code not_thread_owner, Meta subcode 2534037 in platformError). &#x60;details.ownerAppId&#x60; names the owner when Meta reports it.  To fix not_thread_owner, take control with POST /v1/inbox/conversations/{conversationId}/thread-control, then resend. Only accounts connected through a Facebook Page can take; an Instagram Login connection cannot.  |  -  |
| **422** | Idempotency-Key reused with a different request, or the audio at attachmentUrl could not be downloaded (code attachment_fetch_failed, param attachmentUrl, the upstream HTTP status in the message): the URL is private, expired or gone. Nothing was sent. |  -  |
| **429** | Rate limited. Either the connected account&#39;s upstream platform quota is exhausted (code rate_limited, see Retry-After; Reddit allows 1000 requests per 10 minutes per connected user; TikTok code 40100 also lands here with platform and platformError set), or Meta rejected the WhatsApp template-definition lookup (code platform_api_error). No message was sent. |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |
| **500** | The platform rejected or failed the send. Meta 5xx failures also arrive as a platform_error envelope (code platform_api_error, with platform and platformError set).  Zernio does NOT retry a send internally: a message send is not idempotent, and an opaque upstream failure (e.g. WhatsApp 131000) does not say whether the message was delivered. Retrying may deliver the message twice, so retry only if your use case tolerates a duplicate.  |  -  |
| **502** | The WhatsApp account has no Business Account ID, or the platform returned an upstream failure (a template with no approved variant in that language is a 400). No WhatsApp template message is sent when definition lookup fails. |  -  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |
| **0** | Meta rejected the WhatsApp template-definition lookup with another upstream status. No message was sent. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sendtypingindicator"></a>
# **SendTypingIndicator**
> UpdateYoutubeDefaultPlaylist200Response SendTypingIndicator (string conversationId, SendTypingIndicatorRequest sendTypingIndicatorRequest)

Send typing indicator

Show a typing indicator in a conversation.  ### Platform support  - Facebook Messenger: shows \"Page is typing...\" for 20 seconds. - Instagram: shows \"typing...\" to the recipient (works for both Instagram Login and Facebook Login accounts). The recipient must be signed in to Instagram to see it. - Telegram: shows \"Bot is typing...\" for 5 seconds. - WhatsApp: shows \"typing...\" for up to 25 seconds. Requires a recent inbound message in the conversation (Meta references the inbound message id) and also marks that message as read as a side-effect. - iMessage: shows a typing bubble for ~15 seconds (1:1 conversations only; requires a recent two-way exchange). - All others: returns 200 but no-op (platform doesn't support it).  ### Response  Typing indicators are best-effort. The endpoint always returns 200 even if the platform call fails.  `success` reports whether a typing indicator was actually sent to the platform (`false` on unsupported platforms or when the platform call failed). 

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
    public class SendTypingIndicatorExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | The conversation ID
            var sendTypingIndicatorRequest = new SendTypingIndicatorRequest(); // SendTypingIndicatorRequest | 

            try
            {
                // Send typing indicator
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.SendTypingIndicator(conversationId, sendTypingIndicatorRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.SendTypingIndicator: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendTypingIndicatorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send typing indicator
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.SendTypingIndicatorWithHttpInfo(conversationId, sendTypingIndicatorRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.SendTypingIndicatorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | The conversation ID |  |
| **sendTypingIndicatorRequest** | [**SendTypingIndicatorRequest**](SendTypingIndicatorRequest.md) |  |  |

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
| **200** | Typing indicator sent (or no-op on unsupported platforms) |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account or conversation not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setconversationthreadcontrol"></a>
# **SetConversationThreadControl**
> SetConversationThreadControl200Response SetConversationThreadControl (string conversationId, SetConversationThreadControlRequest setConversationThreadControlRequest)

Change who answers a conversation (handover)

Changes who answers a conversation, using Meta's handover protocol on WhatsApp, Facebook and Instagram.  **WhatsApp**, on numbers with Meta Business Agent enabled:  - `release`: hand the conversation back to the agent so it resumes answering. You must currently hold control (sending any message takes it implicitly). - `take`: take control before sending anything, so the agent stops replying while an operator reads the thread. Meta accepts this only from the business configured as the number's escalation partner; other apps take control by sending a message. - `pass`: transfer control to the number's configured escalation partner, or to the agent with `target: ai_agent`. Meta's Cloud API currently rejects it (\"Pass action is not supported\", verified 2026-09-08); use `release` to hand a thread back to the agent.  **Facebook and Instagram** (Messenger Platform handover between the apps on the Page, such as Page Inbox):  - `pass` with `targetAppId`: give the thread to another app (`pass_thread_control`). Page Inbox is 263902037430900. - `take`: take the thread back (`take_thread_control`). Meta allows it only to the Page's primary receiver, and only on accounts connected through a Facebook Page. On an Instagram Login connection it answers 400 `platform_not_supported`. - `request`: ask the current owner to pass the thread (`request_thread_control`); nothing changes until it does. Not available on Instagram Login connections (400 `platform_not_supported`). - `release`: give the thread back to the primary receiver (`release_thread_control`).  ### While another app owns the thread  While another app owns a Facebook or Instagram thread, inbound messages arrive with `metadata.standby: true` and a send answers 409 `not_thread_owner`.  The conversation's `threadControl` follows the result. A `conversation.control_changed` webhook fires when Meta later reports the change. 

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
    public class SetConversationThreadControlExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | The conversation ID
            var setConversationThreadControlRequest = new SetConversationThreadControlRequest(); // SetConversationThreadControlRequest | 

            try
            {
                // Change who answers a conversation (handover)
                SetConversationThreadControl200Response result = apiInstance.SetConversationThreadControl(conversationId, setConversationThreadControlRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.SetConversationThreadControl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetConversationThreadControlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Change who answers a conversation (handover)
    ApiResponse<SetConversationThreadControl200Response> response = apiInstance.SetConversationThreadControlWithHttpInfo(conversationId, setConversationThreadControlRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.SetConversationThreadControlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | The conversation ID |  |
| **setConversationThreadControlRequest** | [**SetConversationThreadControlRequest**](SetConversationThreadControlRequest.md) |  |  |

### Return type

[**SetConversationThreadControl200Response**](SetConversationThreadControl200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Control transferred (or, for request, asked for) |  -  |
| **400** | Invalid field, or take / request on an Instagram account connected with Instagram Login (code platform_not_supported) |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Account or conversation not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateinboxconversation"></a>
# **UpdateInboxConversation**
> UpdateInboxConversation200Response UpdateInboxConversation (string conversationId, UpdateInboxConversationRequest updateInboxConversationRequest)

Update conversation status

Archive or activate a conversation. Requires accountId in request body.

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
    public class UpdateInboxConversationExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed.
            var updateInboxConversationRequest = new UpdateInboxConversationRequest(); // UpdateInboxConversationRequest | 

            try
            {
                // Update conversation status
                UpdateInboxConversation200Response result = apiInstance.UpdateInboxConversation(conversationId, updateInboxConversationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.UpdateInboxConversation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateInboxConversationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update conversation status
    ApiResponse<UpdateInboxConversation200Response> response = apiInstance.UpdateInboxConversationWithHttpInfo(conversationId, updateInboxConversationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.UpdateInboxConversationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed. |  |
| **updateInboxConversationRequest** | [**UpdateInboxConversationRequest**](UpdateInboxConversationRequest.md) |  |  |

### Return type

[**UpdateInboxConversation200Response**](UpdateInboxConversation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Conversation updated |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Inbox addon required |  -  |
| **404** | Conversation not found (WhatsApp only; other platforms upsert) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="uploadmediadirect"></a>
# **UploadMediaDirect**
> UploadMediaDirect200Response UploadMediaDirect (FileParameter file, string? contentType = null)

Upload media file

Upload a media file using API key authentication and get back a publicly accessible URL. The URL can be used as attachmentUrl when sending inbox messages.  Files are stored in temporary storage and auto-delete after 7 days.  ### Size limit  The effective maximum is about 4.5 MB. The multipart body goes through the hosting platform's request body limit, which answers 413 before the endpoint's own 25 MB check is reached.  For larger files use POST /v1/media/presign and upload straight to storage.  ### Compared with /v1/media/upload  /v1/media/upload uses upload tokens for end-user flows. This endpoint takes your API key in the Authorization header, for programmatic use. 

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
    public class UploadMediaDirectExample
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
            var apiInstance = new MessagesApi(httpClient, config, httpClientHandler);
            var file = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // FileParameter | The file to upload (about 4.5 MB at most in practice; use POST /v1/media/presign for larger files)
            var contentType = "contentType_example";  // string? | Override MIME type (e.g. \\\"image/jpeg\\\"). Auto-detected from file if not provided. (optional) 

            try
            {
                // Upload media file
                UploadMediaDirect200Response result = apiInstance.UploadMediaDirect(file, contentType);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagesApi.UploadMediaDirect: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadMediaDirectWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload media file
    ApiResponse<UploadMediaDirect200Response> response = apiInstance.UploadMediaDirectWithHttpInfo(file, contentType);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagesApi.UploadMediaDirectWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **file** | **FileParameter****FileParameter** | The file to upload (about 4.5 MB at most in practice; use POST /v1/media/presign for larger files) |  |
| **contentType** | **string?** | Override MIME type (e.g. \\\&quot;image/jpeg\\\&quot;). Auto-detected from file if not provided. | [optional]  |

### Return type

[**UploadMediaDirect200Response**](UploadMediaDirect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | File uploaded successfully |  -  |
| **400** | No file provided or file too large |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

