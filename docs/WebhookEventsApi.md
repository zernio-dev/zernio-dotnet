# Zernio.Api.WebhookEventsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**OnAccountAdsInitialSyncCompleted**](WebhookEventsApi.md#onaccountadsinitialsynccompleted) | **POST** /account.ads.initial_sync_completed | Ads initial sync completed event |
| [**OnAccountAdsSyncFailed**](WebhookEventsApi.md#onaccountadssyncfailed) | **POST** /account.ads.sync_failed | Ads sync failed event |
| [**OnAccountAdsSyncRecovered**](WebhookEventsApi.md#onaccountadssyncrecovered) | **POST** /account.ads.sync_recovered | Ads sync recovered event |
| [**OnAccountConnected**](WebhookEventsApi.md#onaccountconnected) | **POST** /account.connected | Account connected event |
| [**OnAccountDisconnected**](WebhookEventsApi.md#onaccountdisconnected) | **POST** /account.disconnected | Account disconnected event |
| [**OnAccountPermissionsChanged**](WebhookEventsApi.md#onaccountpermissionschanged) | **POST** /account.permissions_changed | Account permissions changed event |
| [**OnAccountRateLimited**](WebhookEventsApi.md#onaccountratelimited) | **POST** /account.rate_limited | Mailbox sending cooldown started |
| [**OnAdAccountStatusChanged**](WebhookEventsApi.md#onadaccountstatuschanged) | **POST** /ad_account.status_changed | Ad account status changed event |
| [**OnAdCreated**](WebhookEventsApi.md#onadcreated) | **POST** /ad.created | Ad created event |
| [**OnAdDeliveryIssue**](WebhookEventsApi.md#onaddeliveryissue) | **POST** /ad.delivery_issue | Ad delivery issue event |
| [**OnAdReviewApproved**](WebhookEventsApi.md#onadreviewapproved) | **POST** /ad.review.approved | Ad review approved event |
| [**OnAdReviewRejected**](WebhookEventsApi.md#onadreviewrejected) | **POST** /ad.review.rejected | Ad review rejected event |
| [**OnAdRuleTriggered**](WebhookEventsApi.md#onadruletriggered) | **POST** /ad_rule.triggered | Ad rule triggered event |
| [**OnAdSetCreated**](WebhookEventsApi.md#onadsetcreated) | **POST** /ad_set.created | Ad set created event |
| [**OnAdSetUpdated**](WebhookEventsApi.md#onadsetupdated) | **POST** /ad_set.updated | Ad set updated event |
| [**OnAdStatusChanged**](WebhookEventsApi.md#onadstatuschanged) | **POST** /ad.status_changed | Ad status changed event |
| [**OnAdUpdated**](WebhookEventsApi.md#onadupdated) | **POST** /ad.updated | Ad updated event |
| [**OnAdVideoProcessed**](WebhookEventsApi.md#onadvideoprocessed) | **POST** /ad.video.processed | Ad video processed event |
| [**OnAnalyticsSynced**](WebhookEventsApi.md#onanalyticssynced) | **POST** /analytics.synced | Analytics synced event |
| [**OnApiChangelogPublished**](WebhookEventsApi.md#onapichangelogpublished) | **POST** /api.changelog.published | API changelog entry published event |
| [**OnAutomationActionApplied**](WebhookEventsApi.md#onautomationactionapplied) | **POST** /automation.action.applied | Automation action applied event |
| [**OnAutomationActionFailed**](WebhookEventsApi.md#onautomationactionfailed) | **POST** /automation.action.failed | Automation action failed event |
| [**OnAutomationActionUnknown**](WebhookEventsApi.md#onautomationactionunknown) | **POST** /automation.action.unknown | Automation action unknown event |
| [**OnAutomationAlertEscalated**](WebhookEventsApi.md#onautomationalertescalated) | **POST** /automation.alert.escalated | Automation alert escalated event |
| [**OnAutomationAlertOpened**](WebhookEventsApi.md#onautomationalertopened) | **POST** /automation.alert.opened | Automation alert opened event |
| [**OnAutomationAlertResolved**](WebhookEventsApi.md#onautomationalertresolved) | **POST** /automation.alert.resolved | Automation alert resolved event |
| [**OnAutomationCheckCompleted**](WebhookEventsApi.md#onautomationcheckcompleted) | **POST** /automation.check.completed | Automation check completed event |
| [**OnBalanceCharged**](WebhookEventsApi.md#onbalancecharged) | **POST** /balance.charged | Balance charged event |
| [**OnBalanceEmpty**](WebhookEventsApi.md#onbalanceempty) | **POST** /balance.empty | Balance empty event |
| [**OnBalanceLow**](WebhookEventsApi.md#onbalancelow) | **POST** /balance.low | Balance low event |
| [**OnBrandedCallingIdentityActionRequired**](WebhookEventsApi.md#onbrandedcallingidentityactionrequired) | **POST** /branded_calling.identity.action_required | Caller identity action required event |
| [**OnBrandedCallingIdentityStatusUpdated**](WebhookEventsApi.md#onbrandedcallingidentitystatusupdated) | **POST** /branded_calling.identity.status_updated | Caller identity status updated event |
| [**OnBrandedCallingNumberStatusUpdated**](WebhookEventsApi.md#onbrandedcallingnumberstatusupdated) | **POST** /branded_calling.number.status_updated | Branded number status updated event |
| [**OnCalendarEventCreated**](WebhookEventsApi.md#oncalendareventcreated) | **POST** /calendar.event.created | Calendar event created |
| [**OnCalendarEventDeleted**](WebhookEventsApi.md#oncalendareventdeleted) | **POST** /calendar.event.deleted | Calendar event deleted |
| [**OnCalendarEventUpdated**](WebhookEventsApi.md#oncalendareventupdated) | **POST** /calendar.event.updated | Calendar event updated |
| [**OnCallEnded**](WebhookEventsApi.md#oncallended) | **POST** /call.ended | Call ended event |
| [**OnCallFailed**](WebhookEventsApi.md#oncallfailed) | **POST** /call.failed | Call failed event |
| [**OnCallPermissionRequest**](WebhookEventsApi.md#oncallpermissionrequest) | **POST** /call.permission_request | Call permission request reply event |
| [**OnCallReceived**](WebhookEventsApi.md#oncallreceived) | **POST** /call.received | Call received event |
| [**OnCallRecordingReady**](WebhookEventsApi.md#oncallrecordingready) | **POST** /call.recording_ready | Call recording ready event |
| [**OnCallTranscriptSegment**](WebhookEventsApi.md#oncalltranscriptsegment) | **POST** /call.transcript_segment | Call transcript segment event |
| [**OnCampaignBudgetDepleted**](WebhookEventsApi.md#oncampaignbudgetdepleted) | **POST** /campaign.budget.depleted | Campaign budget depleted event |
| [**OnCampaignCreated**](WebhookEventsApi.md#oncampaigncreated) | **POST** /campaign.created | Campaign created event |
| [**OnCampaignParticipantJoined**](WebhookEventsApi.md#oncampaignparticipantjoined) | **POST** /campaign_participant.joined | Campaign participant joined event |
| [**OnCampaignParticipantRemoved**](WebhookEventsApi.md#oncampaignparticipantremoved) | **POST** /campaign_participant.removed | Campaign participant removed event |
| [**OnCampaignParticipantSuspended**](WebhookEventsApi.md#oncampaignparticipantsuspended) | **POST** /campaign_participant.suspended | Campaign participant suspended event |
| [**OnCampaignPayoutFailed**](WebhookEventsApi.md#oncampaignpayoutfailed) | **POST** /campaign_payout.failed | Campaign payout failed event |
| [**OnCampaignPayoutPayable**](WebhookEventsApi.md#oncampaignpayoutpayable) | **POST** /campaign_payout.payable | Campaign payout payable event |
| [**OnCampaignPayoutSettled**](WebhookEventsApi.md#oncampaignpayoutsettled) | **POST** /campaign_payout.settled | Campaign payout settled event |
| [**OnCampaignSubmissionApproved**](WebhookEventsApi.md#oncampaignsubmissionapproved) | **POST** /campaign_submission.approved | Campaign submission approved event |
| [**OnCampaignSubmissionFlagged**](WebhookEventsApi.md#oncampaignsubmissionflagged) | **POST** /campaign_submission.flagged | Campaign submission flagged event |
| [**OnCampaignSubmissionPendingReview**](WebhookEventsApi.md#oncampaignsubmissionpendingreview) | **POST** /campaign_submission.pending_review | Campaign submission pending review event |
| [**OnCampaignSubmissionReceived**](WebhookEventsApi.md#oncampaignsubmissionreceived) | **POST** /campaign_submission.received | Campaign submission received event |
| [**OnCampaignSubmissionRejected**](WebhookEventsApi.md#oncampaignsubmissionrejected) | **POST** /campaign_submission.rejected | Campaign submission rejected event |
| [**OnCampaignUpdated**](WebhookEventsApi.md#oncampaignupdated) | **POST** /campaign.updated | Campaign updated event |
| [**OnCommentReceived**](WebhookEventsApi.md#oncommentreceived) | **POST** /comment.received | Comment received event |
| [**OnCommerceOrderCreated**](WebhookEventsApi.md#oncommerceordercreated) | **POST** /commerce.order.created | Commerce order created event |
| [**OnCommerceOrderRefunded**](WebhookEventsApi.md#oncommerceorderrefunded) | **POST** /commerce.order.refunded | Commerce order refunded event |
| [**OnCommerceOrderUpdated**](WebhookEventsApi.md#oncommerceorderupdated) | **POST** /commerce.order.updated | Commerce order updated event |
| [**OnCommerceProductCreated**](WebhookEventsApi.md#oncommerceproductcreated) | **POST** /commerce.product.created | Commerce product created event |
| [**OnCommerceProductDeleted**](WebhookEventsApi.md#oncommerceproductdeleted) | **POST** /commerce.product.deleted | Commerce product deleted event |
| [**OnCommerceProductUpdated**](WebhookEventsApi.md#oncommerceproductupdated) | **POST** /commerce.product.updated | Commerce product updated event |
| [**OnContactDeleted**](WebhookEventsApi.md#oncontactdeleted) | **POST** /contact.deleted | Contact deleted |
| [**OnContactFieldChanged**](WebhookEventsApi.md#oncontactfieldchanged) | **POST** /contact.field_changed | Contact field changed event |
| [**OnContactTagAdded**](WebhookEventsApi.md#oncontacttagadded) | **POST** /contact.tag_added | Contact tag added event |
| [**OnContactTagRemoved**](WebhookEventsApi.md#oncontacttagremoved) | **POST** /contact.tag_removed | Contact tag removed event |
| [**OnContactUpdated**](WebhookEventsApi.md#oncontactupdated) | **POST** /contact.updated | Contact updated |
| [**OnConversationControlChanged**](WebhookEventsApi.md#onconversationcontrolchanged) | **POST** /conversation.control_changed | Conversation control changed event |
| [**OnConversationStarted**](WebhookEventsApi.md#onconversationstarted) | **POST** /conversation.started | Conversation started event |
| [**OnCreatorCampaignBudgetExhausted**](WebhookEventsApi.md#oncreatorcampaignbudgetexhausted) | **POST** /creator_campaign.budget_exhausted | Creator campaign budget exhausted event |
| [**OnCreatorCampaignClosed**](WebhookEventsApi.md#oncreatorcampaignclosed) | **POST** /creator_campaign.closed | Creator campaign closed event |
| [**OnEmailLinkClicked**](WebhookEventsApi.md#onemaillinkclicked) | **POST** /email.link_clicked | Email link clicked |
| [**OnEmailOpened**](WebhookEventsApi.md#onemailopened) | **POST** /email.opened | Email opened |
| [**OnEmailSendFailed**](WebhookEventsApi.md#onemailsendfailed) | **POST** /email.send_failed | Scheduled email failed |
| [**OnEmailThreadReplied**](WebhookEventsApi.md#onemailthreadreplied) | **POST** /email.thread_replied | Email thread replied |
| [**OnFileCreated**](WebhookEventsApi.md#onfilecreated) | **POST** /file.created | File created |
| [**OnFileDeleted**](WebhookEventsApi.md#onfiledeleted) | **POST** /file.deleted | File deleted |
| [**OnFilePicked**](WebhookEventsApi.md#onfilepicked) | **POST** /file.picked | Files picked |
| [**OnFileUpdated**](WebhookEventsApi.md#onfileupdated) | **POST** /file.updated | File updated |
| [**OnLeadReceived**](WebhookEventsApi.md#onleadreceived) | **POST** /lead.received | Lead received event |
| [**OnMentionReceived**](WebhookEventsApi.md#onmentionreceived) | **POST** /mention.received | Mention received event |
| [**OnMessageDeleted**](WebhookEventsApi.md#onmessagedeleted) | **POST** /message.deleted | Message deleted event |
| [**OnMessageDelivered**](WebhookEventsApi.md#onmessagedelivered) | **POST** /message.delivered | Message delivered event |
| [**OnMessageEdited**](WebhookEventsApi.md#onmessageedited) | **POST** /message.edited | Message edited event |
| [**OnMessageFailed**](WebhookEventsApi.md#onmessagefailed) | **POST** /message.failed | Message delivery failed event |
| [**OnMessagePlayed**](WebhookEventsApi.md#onmessageplayed) | **POST** /message.played | Message played event |
| [**OnMessageRead**](WebhookEventsApi.md#onmessageread) | **POST** /message.read | Message read event |
| [**OnMessageReceived**](WebhookEventsApi.md#onmessagereceived) | **POST** /message.received | Message received event |
| [**OnMessageSent**](WebhookEventsApi.md#onmessagesent) | **POST** /message.sent | Message sent event |
| [**OnPhoneNumberStockAvailable**](WebhookEventsApi.md#onphonenumberstockavailable) | **POST** /phone_number.stock_available | Phone-number stock available event |
| [**OnPostAuthenticityChanged**](WebhookEventsApi.md#onpostauthenticitychanged) | **POST** /post.authenticity_changed | Post authenticity changed event |
| [**OnPostCancelled**](WebhookEventsApi.md#onpostcancelled) | **POST** /post.cancelled | Post cancelled event |
| [**OnPostExternalCreated**](WebhookEventsApi.md#onpostexternalcreated) | **POST** /post.external.created | External post created event |
| [**OnPostExternalDeleted**](WebhookEventsApi.md#onpostexternaldeleted) | **POST** /post.external.deleted | External post deleted event |
| [**OnPostExternalUpdated**](WebhookEventsApi.md#onpostexternalupdated) | **POST** /post.external.updated | External post updated event |
| [**OnPostFailed**](WebhookEventsApi.md#onpostfailed) | **POST** /post.failed | Post failed event |
| [**OnPostPartial**](WebhookEventsApi.md#onpostpartial) | **POST** /post.partial | Post partial event |
| [**OnPostPlatformDeleted**](WebhookEventsApi.md#onpostplatformdeleted) | **POST** /post.platform.deleted | Post platform deleted event |
| [**OnPostPlatformFailed**](WebhookEventsApi.md#onpostplatformfailed) | **POST** /post.platform.failed | Post platform failed event |
| [**OnPostPlatformPublished**](WebhookEventsApi.md#onpostplatformpublished) | **POST** /post.platform.published | Post platform published event |
| [**OnPostPublished**](WebhookEventsApi.md#onpostpublished) | **POST** /post.published | Post published event |
| [**OnPostRecycled**](WebhookEventsApi.md#onpostrecycled) | **POST** /post.recycled | Post recycled event |
| [**OnPostScheduled**](WebhookEventsApi.md#onpostscheduled) | **POST** /post.scheduled | Post scheduled event |
| [**OnPostTikTokUrlResolved**](WebhookEventsApi.md#onposttiktokurlresolved) | **POST** /post.tiktok.url_resolved | TikTok post URL resolved event |
| [**OnPostTrackingCompleted**](WebhookEventsApi.md#onposttrackingcompleted) | **POST** /post.tracking_completed | Post tracking completed event |
| [**OnRcsAgentStatusUpdated**](WebhookEventsApi.md#onrcsagentstatusupdated) | **POST** /rcs.agent.status_updated | RCS agent status updated event |
| [**OnReactionReceived**](WebhookEventsApi.md#onreactionreceived) | **POST** /reaction.received | Reaction received event |
| [**OnReferralReceived**](WebhookEventsApi.md#onreferralreceived) | **POST** /referral.received | Referral received event |
| [**OnReviewDeleted**](WebhookEventsApi.md#onreviewdeleted) | **POST** /review.deleted | Review deleted event |
| [**OnReviewNew**](WebhookEventsApi.md#onreviewnew) | **POST** /review.new | Review new event |
| [**OnReviewRestored**](WebhookEventsApi.md#onreviewrestored) | **POST** /review.restored | Review restored event |
| [**OnReviewUpdated**](WebhookEventsApi.md#onreviewupdated) | **POST** /review.updated | Review updated event |
| [**OnSequenceEnrolled**](WebhookEventsApi.md#onsequenceenrolled) | **POST** /sequence.enrolled | Sequence enrolled event |
| [**OnSequenceExited**](WebhookEventsApi.md#onsequenceexited) | **POST** /sequence.exited | Sequence exited event |
| [**OnSmsRegistrationActionRequired**](WebhookEventsApi.md#onsmsregistrationactionrequired) | **POST** /sms.registration.action_required | SMS registration action required event |
| [**OnSmsRegistrationStatusUpdated**](WebhookEventsApi.md#onsmsregistrationstatusupdated) | **POST** /sms.registration.status_updated | SMS registration status updated event |
| [**OnSupportRunCompleted**](WebhookEventsApi.md#onsupportruncompleted) | **POST** /support.run.completed | Support Assistant finished event |
| [**OnSupportRunFailed**](WebhookEventsApi.md#onsupportrunfailed) | **POST** /support.run.failed | Support Assistant failed event |
| [**OnVerificationApproved**](WebhookEventsApi.md#onverificationapproved) | **POST** /verification.approved | Verification approved event |
| [**OnVerificationFailed**](WebhookEventsApi.md#onverificationfailed) | **POST** /verification.failed | Verification failed event |
| [**OnWebhookTest**](WebhookEventsApi.md#onwebhooktest) | **POST** /webhook.test | Webhook test event |
| [**OnWhatsAppAccountAlertReceived**](WebhookEventsApi.md#onwhatsappaccountalertreceived) | **POST** /whatsapp.account.alert_received | WhatsApp account alert received |
| [**OnWhatsAppAccountNameStatusUpdated**](WebhookEventsApi.md#onwhatsappaccountnamestatusupdated) | **POST** /whatsapp.account.name_status_updated | WhatsApp display-name review outcome event |
| [**OnWhatsAppAccountQualityUpdated**](WebhookEventsApi.md#onwhatsappaccountqualityupdated) | **POST** /whatsapp.account.quality_updated | WhatsApp quality rating or messaging limit changed |
| [**OnWhatsAppAccountStatusUpdated**](WebhookEventsApi.md#onwhatsappaccountstatusupdated) | **POST** /whatsapp.account.status_updated | WhatsApp Business Account restricted or reinstated |
| [**OnWhatsAppAutomaticEvent**](WebhookEventsApi.md#onwhatsappautomaticevent) | **POST** /whatsapp.automatic_event | WhatsApp automatic event detected |
| [**OnWhatsAppContactIdentityChanged**](WebhookEventsApi.md#onwhatsappcontactidentitychanged) | **POST** /whatsapp.contact.identity_changed | WhatsApp contact identity changed event |
| [**OnWhatsAppNumberActionRequired**](WebhookEventsApi.md#onwhatsappnumberactionrequired) | **POST** /whatsapp.number.action_required | WhatsApp number action required event |
| [**OnWhatsAppNumberActivated**](WebhookEventsApi.md#onwhatsappnumberactivated) | **POST** /whatsapp.number.activated | WhatsApp number activated event |
| [**OnWhatsAppNumberDeclined**](WebhookEventsApi.md#onwhatsappnumberdeclined) | **POST** /whatsapp.number.declined | WhatsApp number declined event |
| [**OnWhatsAppNumberKycSubmitted**](WebhookEventsApi.md#onwhatsappnumberkycsubmitted) | **POST** /whatsapp.number.kyc_submitted | WhatsApp number KYC submitted event |
| [**OnWhatsAppNumberReactivated**](WebhookEventsApi.md#onwhatsappnumberreactivated) | **POST** /whatsapp.number.reactivated | WhatsApp number reactivated event |
| [**OnWhatsAppNumberReleased**](WebhookEventsApi.md#onwhatsappnumberreleased) | **POST** /whatsapp.number.released | WhatsApp number released event |
| [**OnWhatsAppNumberSuspended**](WebhookEventsApi.md#onwhatsappnumbersuspended) | **POST** /whatsapp.number.suspended | WhatsApp number suspended event |
| [**OnWhatsAppNumberVerificationRequired**](WebhookEventsApi.md#onwhatsappnumberverificationrequired) | **POST** /whatsapp.number.verification_required | WhatsApp number verification-required event |
| [**OnWhatsAppTemplateCategoryUpdated**](WebhookEventsApi.md#onwhatsapptemplatecategoryupdated) | **POST** /whatsapp.template.category_updated | WhatsApp template category updated event |
| [**OnWhatsAppTemplateStatusUpdated**](WebhookEventsApi.md#onwhatsapptemplatestatusupdated) | **POST** /whatsapp.template.status_updated | WhatsApp template status updated event |
| [**OnWorkflowRunCompleted**](WebhookEventsApi.md#onworkflowruncompleted) | **POST** /workflow.run.completed | Workflow run completed event |
| [**OnWorkflowRunFailed**](WebhookEventsApi.md#onworkflowrunfailed) | **POST** /workflow.run.failed | Workflow run failed event |
| [**OnWorkflowRunStarted**](WebhookEventsApi.md#onworkflowrunstarted) | **POST** /workflow.run.started | Workflow run started event |

<a id="onaccountadsinitialsynccompleted"></a>
# **OnAccountAdsInitialSyncCompleted**
> void OnAccountAdsInitialSyncCompleted (WebhookPayloadAccountAdsInitialSyncCompleted webhookPayloadAccountAdsInitialSyncCompleted)

Ads initial sync completed event

The initial sync, ad-account discovery plus a 90-day ad backfill, completed for an ads-enabled account.  ### When it fires  Fires once per ads-enabled account. `sync` reports whether the backfill succeeded fully or partially, and how many ads were synced versus failed.  ### Scoped connects  When scoping was applied at connect time, `account.platformAdAccountId` echoes the chosen ad account when the scope is exactly one. `account.platformAdAccountIds` lists every `act_*` synced.  ### On failure  When `sync.status` is `\"failure\"`, the payload adds `sync.error` (raw platform error, about 2 KB), `sync.errorCode` and `sync.errorSubcode` when parseable, and `sync.errorCategory`.  ### Error categories  `sync.errorCategory` is `token_invalid`, `permission_denied`, `no_ad_accounts`, `rate_limited`, `discovery_failed` or `unknown`. New values may be added; existing ones are stable.  ### Retrying  Reconnecting re-queues the backfill and the event fires again. It fixes `token_invalid`, `permission_denied` and `rate_limited`; `no_ad_accounts` needs an ad account on the grant first.  ### When a retry is skipped  Zernio skips the re-queue only when a backfill already completed with at least one ad, or one started less than 20 minutes ago. 

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

<a id="onaccountadssyncfailed"></a>
# **OnAccountAdsSyncFailed**
> void OnAccountAdsSyncFailed (WebhookPayloadAccountAdsSyncFailed webhookPayloadAccountAdsSyncFailed)

Ads sync failed event

An ad account's ads stopped syncing: no success for 24 hours, or every live ad at the retry cap.  ### When it fires  An hourly check covers every ad account with live ads on a connected account, on any ads platform. Fires once per ad account until `account.ads.sync_recovered`.  ### Stale metrics  Metrics for the ad account are stale in between. Use this signal to flag the numbers in your UI rather than to poll.  ### Payload notes  `adAccount.platformAdAccountId` names the ad account (`act_*` on Meta). `account.accountId` names its connection, so one connection with several ad accounts reports each separately.  ### Sync fields  `sync.lastSuccessfulSyncAt` is the last good sync and `sync.failureCount` the consecutive failed attempts.  ### Error categories  Branch on `sync.errorCategory`: `ad_account_not_listed` (access removed or platform change; check permissions, reconnect), `sync_error` (see `sync.error`) or `stale` (no error recorded; retries usually clear it). New values may be added.  ### When it does not fire  A disconnected connection gets `account.disconnected` instead, and no recovery event follows. An ad account that never synced successfully, or whose last good sync is over 3 days old, is not announced. 

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
    public class OnAccountAdsSyncFailedExample
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
            var webhookPayloadAccountAdsSyncFailed = new WebhookPayloadAccountAdsSyncFailed(); // WebhookPayloadAccountAdsSyncFailed | 

            try
            {
                // Ads sync failed event
                apiInstance.OnAccountAdsSyncFailed(webhookPayloadAccountAdsSyncFailed);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAccountAdsSyncFailed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAccountAdsSyncFailedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ads sync failed event
    apiInstance.OnAccountAdsSyncFailedWithHttpInfo(webhookPayloadAccountAdsSyncFailed);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAccountAdsSyncFailedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAccountAdsSyncFailed** | [**WebhookPayloadAccountAdsSyncFailed**](WebhookPayloadAccountAdsSyncFailed.md) |  |  |

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

<a id="onaccountadssyncrecovered"></a>
# **OnAccountAdsSyncRecovered**
> void OnAccountAdsSyncRecovered (WebhookPayloadAccountAdsSyncRecovered webhookPayloadAccountAdsSyncRecovered)

Ads sync recovered event

An ad account previously reported by `account.ads.sync_failed` synced successfully again.  ### When it fires  Fires once when a sync succeeds again, found by an hourly check.  ### Payload notes  `sync.failingSince` is the last successful sync before the failure started. 

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
    public class OnAccountAdsSyncRecoveredExample
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
            var webhookPayloadAccountAdsSyncRecovered = new WebhookPayloadAccountAdsSyncRecovered(); // WebhookPayloadAccountAdsSyncRecovered | 

            try
            {
                // Ads sync recovered event
                apiInstance.OnAccountAdsSyncRecovered(webhookPayloadAccountAdsSyncRecovered);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAccountAdsSyncRecovered: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAccountAdsSyncRecoveredWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ads sync recovered event
    apiInstance.OnAccountAdsSyncRecoveredWithHttpInfo(webhookPayloadAccountAdsSyncRecovered);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAccountAdsSyncRecoveredWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAccountAdsSyncRecovered** | [**WebhookPayloadAccountAdsSyncRecovered**](WebhookPayloadAccountAdsSyncRecovered.md) |  |  |

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

An account was connected to a profile, through OAuth or credentials.  ### Repeat events  Reconnecting an account you already hold fires it again with the same `accountId`, since the connect flow upserts per profile and platform. Key your upsert on `accountId`. 

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

A connected account stopped working or was removed.  ### Intentional  Removed on purpose, such as `DELETE /v1/accounts/{id}` or a switch to the Free plan. Kept 1 hour (`gracePeriodEndsAt`), then deleted with no further event. Reconnecting within the hour restores the same `accountId`.  ### Unintentional  The connection broke (token expired or revoked, access lost). The account stays inactive until reconnected, keeping its `accountId`. Removing it instead sends a second event with `intentional`.  ### Immediate paths  An API removal emits at once with `disconnectionType: \"intentional\"`. A phone-side WhatsApp disconnect emits within seconds of Meta's notification, with `unintentional`.  ### WhatsApp reason  `reason` carries Meta's explanation. Deliberate: `BUSINESS_DOWNGRADE`, `CHANGE_NUMBER`, `USER_RE_REGISTERED`. Idle number dropped by Meta: `PRIMARY_INACTIVITY` after about 14 days, `COMPANION_INACTIVITY` after about 30.  ### Expired or revoked grants  A publish or analytics sync getting a definitive auth error deactivates the account. Publish tries a token refresh first, so the event means the refresh failed too. `reason` carries the platform's message.  ### Reconnection flags  A dead token on an ads or blog call flags the account, and the posting account sharing its token (`needsReconnection: true`). Each flagged account emits once; a later deactivation emits again, then not until reconnected.  ### Lead forms while disconnected  While a Facebook Page is flagged or deactivated, `GET /v1/ads/lead-forms/{formId}/leads` answers `409` with `code: \"account_disconnected\"`.  ### Reconciliation  Anything else (a number deleted in WhatsApp Manager, a channel Meta silently stops serving) is caught by periodic reconciliation, not a notification. It lags minutes to about a day.  ### Do not rely on its absence  Meta's notifications are best-effort. For WhatsApp, poll `GET /v1/whatsapp/number-info` or account health, which runs a live Meta link probe.  ### Subscribing  A webhook only receives the events it lists, so add `account.disconnected` explicitly. 

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

<a id="onaccountpermissionschanged"></a>
# **OnAccountPermissionsChanged**
> void OnAccountPermissionsChanged (WebhookPayloadAccountPermissionsChanged webhookPayloadAccountPermissionsChanged)

Account permissions changed event

A publish on an account connected through your own OAuth app failed for a missing permission.  ### Behaviour  The account stays connected and its token still works. `account.missingScopeAreas` accumulates the affected areas, today `posting`. Each area sends one event, however many posts fail afterwards.  ### When it does not fire  Accounts not connected through your own OAuth app. 

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
    public class OnAccountPermissionsChangedExample
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
            var webhookPayloadAccountPermissionsChanged = new WebhookPayloadAccountPermissionsChanged(); // WebhookPayloadAccountPermissionsChanged | 

            try
            {
                // Account permissions changed event
                apiInstance.OnAccountPermissionsChanged(webhookPayloadAccountPermissionsChanged);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAccountPermissionsChanged: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAccountPermissionsChangedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Account permissions changed event
    apiInstance.OnAccountPermissionsChangedWithHttpInfo(webhookPayloadAccountPermissionsChanged);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAccountPermissionsChangedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAccountPermissionsChanged** | [**WebhookPayloadAccountPermissionsChanged**](WebhookPayloadAccountPermissionsChanged.md) |  |  |

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

<a id="onaccountratelimited"></a>
# **OnAccountRateLimited**
> void OnAccountRateLimited (WebhookPayloadAccountRateLimited webhookPayloadAccountRateLimited)

Mailbox sending cooldown started

A Google or Microsoft mailbox was paused after sending one body to over 50 recipients in an hour.  ### Payload notes  `account.reason` says why and `account.resetsAt` says when sending resumes. Sends answer 429 until then. A later trigger can also start a cooldown. 

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
    public class OnAccountRateLimitedExample
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
            var webhookPayloadAccountRateLimited = new WebhookPayloadAccountRateLimited(); // WebhookPayloadAccountRateLimited | 

            try
            {
                // Mailbox sending cooldown started
                apiInstance.OnAccountRateLimited(webhookPayloadAccountRateLimited);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAccountRateLimited: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAccountRateLimitedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mailbox sending cooldown started
    apiInstance.OnAccountRateLimitedWithHttpInfo(webhookPayloadAccountRateLimited);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAccountRateLimitedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAccountRateLimited** | [**WebhookPayloadAccountRateLimited**](WebhookPayloadAccountRateLimited.md) |  |  |

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

<a id="onadaccountstatuschanged"></a>
# **OnAdAccountStatusChanged**
> void OnAdAccountStatusChanged (WebhookPayloadAdAccountStatusChanged webhookPayloadAdAccountStatusChanged)

Ad account status changed event

An ad account Zernio already tracked became `active`, `restricted`, `disabled` or `closed`.  ### When it fires  Fires when ad account discovery sees a tracked ad account change status, at most once per account per 24 hours. Covers Meta, Google, TikTok and X.  ### Status values  `restricted` needs something settled first (unpaid Meta balance, risk review, TikTok limit or pending verification, X review). `disabled` means the platform disabled or rejected it; `closed` means closed or pending closure.  ### Payload notes  `status.current` and `status.previous` use one vocabulary on every network. `status.raw` is the platform's own value, for example Meta's `account_status` code `2`.  ### When it does not fire  An account seen for the first time, an account Zernio has not seen in the last 48 hours, or a platform status Zernio does not recognize. 

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
    public class OnAdAccountStatusChangedExample
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
            var webhookPayloadAdAccountStatusChanged = new WebhookPayloadAdAccountStatusChanged(); // WebhookPayloadAdAccountStatusChanged | 

            try
            {
                // Ad account status changed event
                apiInstance.OnAdAccountStatusChanged(webhookPayloadAdAccountStatusChanged);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAdAccountStatusChanged: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAdAccountStatusChangedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad account status changed event
    apiInstance.OnAdAccountStatusChangedWithHttpInfo(webhookPayloadAdAccountStatusChanged);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAdAccountStatusChangedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAdAccountStatusChanged** | [**WebhookPayloadAdAccountStatusChanged**](WebhookPayloadAdAccountStatusChanged.md) |  |  |

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

<a id="onadcreated"></a>
# **OnAdCreated**
> void OnAdCreated (WebhookPayloadAdCreated webhookPayloadAdCreated)

Ad created event

An ad was created through Zernio (`source: \"zernio\"`) or detected by the sync (`source: \"platform\"`).  ### When it fires  Fires once the ad's campaign and ad set are recorded. A detected ad arrives up to one sync interval late; Meta ads entering review usually arrive within minutes.  ### When it does not fire  History loaded when an account connects, and ads created more than 7 days ago, are never announced. 

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
    public class OnAdCreatedExample
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
            var webhookPayloadAdCreated = new WebhookPayloadAdCreated(); // WebhookPayloadAdCreated | 

            try
            {
                // Ad created event
                apiInstance.OnAdCreated(webhookPayloadAdCreated);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAdCreated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAdCreatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad created event
    apiInstance.OnAdCreatedWithHttpInfo(webhookPayloadAdCreated);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAdCreatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAdCreated** | [**WebhookPayloadAdCreated**](WebhookPayloadAdCreated.md) |  |  |

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

<a id="onaddeliveryissue"></a>
# **OnAdDeliveryIssue**
> void OnAdDeliveryIssue (WebhookPayloadAdDeliveryIssue webhookPayloadAdDeliveryIssue)

Ad delivery issue event

An ad Zernio already tracked moved into the platform's error state and stopped delivering.  ### What triggers it  Meta `WITH_ISSUES` (payment, policy or account problems), TikTok account punishment or missing balance, or any platform status Zernio does not recognize yet (check `issue.raw`).  ### When it fires  Fires at most once per ad per 24 hours. Ads seen for the first time by a sync never fire it.  ### Payload notes  `issue.raw` is the platform's status string. On Meta, `issue.reasons` carries Meta's messages for the campaign; other networks send none, so it is empty.  ### Platform notes  On Meta the same problem can also arrive as `ad.status_changed` with `WITH_ISSUES`, straight from Meta's webhook and usually sooner. Pick one of the two to act on. 

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
    public class OnAdDeliveryIssueExample
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
            var webhookPayloadAdDeliveryIssue = new WebhookPayloadAdDeliveryIssue(); // WebhookPayloadAdDeliveryIssue | 

            try
            {
                // Ad delivery issue event
                apiInstance.OnAdDeliveryIssue(webhookPayloadAdDeliveryIssue);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAdDeliveryIssue: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAdDeliveryIssueWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad delivery issue event
    apiInstance.OnAdDeliveryIssueWithHttpInfo(webhookPayloadAdDeliveryIssue);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAdDeliveryIssueWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAdDeliveryIssue** | [**WebhookPayloadAdDeliveryIssue**](WebhookPayloadAdDeliveryIssue.md) |  |  |

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

<a id="onadreviewapproved"></a>
# **OnAdReviewApproved**
> void OnAdReviewApproved (WebhookPayloadAdReview webhookPayloadAdReview)

Ad review approved event

An ad Zernio already tracked passed platform review, or a rejected ad was approved on appeal.  ### When it fires  Fires within one sync cycle of the platform's decision, not instantly; on Meta the review poll usually reports sooner. Each outcome is delivered at most once per ad per 24 hours.  ### When it does not fire  Ads seen for the first time by a sync never fire it, including history loaded at connect. On Meta, Google, TikTok and Reddit an ad that leaves review while paused sends no `approved`.  ### Platform notes  Covers every ad network Zernio syncs, with one payload shape. On X, Pinterest and LinkedIn the review is read apart from delivery status, so an ad leaving review while paused still sends `approved`.  ### Payload notes  `review.raw` is the platform's own status string. `adObject.adId` is the Zernio ad id, ready for `GET /v1/ads/{adId}`. Deduplicate on the event `id`. 

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
    public class OnAdReviewApprovedExample
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
            var webhookPayloadAdReview = new WebhookPayloadAdReview(); // WebhookPayloadAdReview | 

            try
            {
                // Ad review approved event
                apiInstance.OnAdReviewApproved(webhookPayloadAdReview);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAdReviewApproved: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAdReviewApprovedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad review approved event
    apiInstance.OnAdReviewApprovedWithHttpInfo(webhookPayloadAdReview);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAdReviewApprovedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAdReview** | [**WebhookPayloadAdReview**](WebhookPayloadAdReview.md) |  |  |

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

<a id="onadreviewrejected"></a>
# **OnAdReviewRejected**
> void OnAdReviewRejected (WebhookPayloadAdReview webhookPayloadAdReview)

Ad review rejected event

The platform rejected an ad Zernio already tracked; `review.reasons` carries its reason when it gives one.  ### When it fires  Fires within one sync cycle of the platform's decision, not instantly; on Meta the review poll usually reports sooner. Each outcome is delivered at most once per ad per 24 hours.  ### When it does not fire  Ads seen for the first time by a sync never fire it, including history loaded at connect.  ### Platform notes  Covers every ad network Zernio syncs. Pinterest, LinkedIn and Reddit send their own reasons, X sends none, and most other networks return a generic message.  ### Payload notes  `review.raw` is the platform's own status string. Show `review.reasons` rather than branching on it. `adObject.adId` is the Zernio ad id. Deduplicate on the event `id`. 

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
    public class OnAdReviewRejectedExample
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
            var webhookPayloadAdReview = new WebhookPayloadAdReview(); // WebhookPayloadAdReview | 

            try
            {
                // Ad review rejected event
                apiInstance.OnAdReviewRejected(webhookPayloadAdReview);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAdReviewRejected: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAdReviewRejectedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad review rejected event
    apiInstance.OnAdReviewRejectedWithHttpInfo(webhookPayloadAdReview);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAdReviewRejectedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAdReview** | [**WebhookPayloadAdReview**](WebhookPayloadAdReview.md) |  |  |

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

<a id="onadruletriggered"></a>
# **OnAdRuleTriggered**
> void OnAdRuleTriggered (WebhookPayloadAdRuleTriggered webhookPayloadAdRuleTriggered)

Ad rule triggered event

A scheduled run of an ad rule with a `notify` action found campaigns or ad sets meeting every condition.  ### When it fires  Each object is announced at most once per rule cooldown. A run where every object is still in cooldown sends nothing.  ### Failed actions  An object whose action `failed` gets no cooldown, so the next run retries it and reports it again.  ### Payload notes  `objects` lists only the objects the run acted on. `objects[].conditions` repeats every condition of the rule with `actual`, the value the object reached.  ### Actions  `objects[].actions` says what the rule did: `done`, `skipped` (with a `reason` such as `already_paused` or `at_limit`) or `failed`. On `adjust_budget` it carries `previousDailyBudget` and `newDailyBudget`; empty on a notify-only rule.  ### Run context  `run.today` and `run.timezone` give the ad account's calendar date the windows used. `run.timezoneAssumed` is `true` when UTC was assumed. `run.currency` is the currency of money metrics, or `null` when unknown. 

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
    public class OnAdRuleTriggeredExample
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
            var webhookPayloadAdRuleTriggered = new WebhookPayloadAdRuleTriggered(); // WebhookPayloadAdRuleTriggered | 

            try
            {
                // Ad rule triggered event
                apiInstance.OnAdRuleTriggered(webhookPayloadAdRuleTriggered);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAdRuleTriggered: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAdRuleTriggeredWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad rule triggered event
    apiInstance.OnAdRuleTriggeredWithHttpInfo(webhookPayloadAdRuleTriggered);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAdRuleTriggeredWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAdRuleTriggered** | [**WebhookPayloadAdRuleTriggered**](WebhookPayloadAdRuleTriggered.md) |  |  |

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

<a id="onadsetcreated"></a>
# **OnAdSetCreated**
> void OnAdSetCreated (WebhookPayloadAdSetCreated webhookPayloadAdSetCreated)

Ad set created event

An ad set was created through Zernio (`source: \"zernio\"`) or detected by the sync (`source: \"platform\"`).  ### When it fires  Fires once the ad set row is recorded, so `GET /v1/ads/ad-sets/{adSetId}` finds it. A detected ad set arrives up to one sync interval late.  ### Payload notes  `adObject.campaign` is the campaign the ad set belongs to, or null when the platform has none.  ### When it does not fire  History loaded when an account connects, and ad sets created more than 7 days ago, are never announced. 

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
    public class OnAdSetCreatedExample
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
            var webhookPayloadAdSetCreated = new WebhookPayloadAdSetCreated(); // WebhookPayloadAdSetCreated | 

            try
            {
                // Ad set created event
                apiInstance.OnAdSetCreated(webhookPayloadAdSetCreated);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAdSetCreated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAdSetCreatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad set created event
    apiInstance.OnAdSetCreatedWithHttpInfo(webhookPayloadAdSetCreated);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAdSetCreatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAdSetCreated** | [**WebhookPayloadAdSetCreated**](WebhookPayloadAdSetCreated.md) |  |  |

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

<a id="onadsetupdated"></a>
# **OnAdSetUpdated**
> void OnAdSetUpdated (WebhookPayloadAdSetUpdated webhookPayloadAdSetUpdated)

Ad set updated event

An ad set was edited through Zernio (`source: \"zernio\"`), or outside Zernio and detected by the sync (`source: \"platform\"`).  ### When it fires  Fires after the platform and Zernio both accepted the edit. Outside edits arrive up to one sync interval late, and only to the user whose sync saw them.  ### Deduplication  Events are not deduplicated, so every edit is announced. Use the event `id` to drop repeats.  ### Payload notes  `changes` lists the edited fields: `name`, `status` (the ad set's own on/off switch), `budget`, `bid`, `schedule`, `targeting` or `settings`. Ignore unknown values. It never carries old or new values, so read the ad set.  ### What the sync detects  From the sync, `changes` covers only `name` and `status`. Status is not detected on Reddit.  ### When it does not fire  History loaded when an account connects is never announced. Budget and targeting edits made through `PUT /v1/ads/{adId}` arrive as `ad.updated`. 

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
    public class OnAdSetUpdatedExample
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
            var webhookPayloadAdSetUpdated = new WebhookPayloadAdSetUpdated(); // WebhookPayloadAdSetUpdated | 

            try
            {
                // Ad set updated event
                apiInstance.OnAdSetUpdated(webhookPayloadAdSetUpdated);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAdSetUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAdSetUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad set updated event
    apiInstance.OnAdSetUpdatedWithHttpInfo(webhookPayloadAdSetUpdated);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAdSetUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAdSetUpdated** | [**WebhookPayloadAdSetUpdated**](WebhookPayloadAdSetUpdated.md) |  |  |

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

A campaign, ad set or ad on a connected Meta ad account (`metaads`) changed status.  ### Sources  Two Meta `ad_account` fields feed it: `in_process_ad_objects` (finished processing, `status.raw` is Meta's `status_name`) and `with_issues_ad_objects` (`status.raw` is `WITH_ISSUES`, `error` filled from Meta).  ### Payload notes  `adObject.level` is `CAMPAIGN`, `AD_SET` or `AD`; creative-level events are not forwarded. Branch on `status.raw`. Use `error.code` as the stable discriminator, since `error.summary` and `error.message` are localized to the owner's Meta locale.  ### The error block  `error` is present on most `WITH_ISSUES` events but can be absent, and never appears on any other status. Null-check it before reading `error.code`.  ### Fan-out  Matching is keyed on `adObject.platformAdAccountId`. When several connected `metaads` accounts point at the same Meta ad account, each receives its own delivery. 

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

<a id="onadupdated"></a>
# **OnAdUpdated**
> void OnAdUpdated (WebhookPayloadAdUpdated webhookPayloadAdUpdated)

Ad updated event

An ad was edited through Zernio (`source: \"zernio\"`), or outside Zernio and detected by the sync (`source: \"platform\"`).  ### When it fires  Fires once, to the owner of the edited ad. Outside edits arrive up to one sync interval late. Every edit is announced, so use the event `id` to drop repeats.  ### Payload notes  `changes` lists the edited fields: `name`, `status` (the ad's own on/off switch), `budget`, `targeting` or `creative`. Ignore unknown values; new ones can be added.  ### Reading the change  The event never carries old or new values, so read the ad. `platformId` can change when a LinkedIn creative is replaced, while `adId` stays stable.  ### When it does not fire  From the sync, `changes` covers only `name` and `status`. Budget, bid, schedule and targeting edits made outside Zernio, tracking tag edits and history loaded at connect are not announced. Ad rule changes arrive as `ad_rule.triggered`. 

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
    public class OnAdUpdatedExample
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
            var webhookPayloadAdUpdated = new WebhookPayloadAdUpdated(); // WebhookPayloadAdUpdated | 

            try
            {
                // Ad updated event
                apiInstance.OnAdUpdated(webhookPayloadAdUpdated);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAdUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAdUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad updated event
    apiInstance.OnAdUpdatedWithHttpInfo(webhookPayloadAdUpdated);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAdUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAdUpdated** | [**WebhookPayloadAdUpdated**](WebhookPayloadAdUpdated.md) |  |  |

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

<a id="onadvideoprocessed"></a>
# **OnAdVideoProcessed**
> void OnAdVideoProcessed (WebhookPayloadAdVideoProcessed webhookPayloadAdVideoProcessed)

Ad video processed event

Meta finished processing a video uploaded with `async: true` on `POST /v1/ads/videos`.  ### Payload notes  `video.status` is `ready` (reference it as `video.id` on the create endpoints) or `error`, with `video.error` carrying the reason.  ### When it fires  Fires once per upload, when the video leaves `processing`. Zernio polls every 10 seconds for about 13 minutes; after that no event is sent, so read `GET /v1/ads/videos/{videoId}` for long videos. 

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
    public class OnAdVideoProcessedExample
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
            var webhookPayloadAdVideoProcessed = new WebhookPayloadAdVideoProcessed(); // WebhookPayloadAdVideoProcessed | 

            try
            {
                // Ad video processed event
                apiInstance.OnAdVideoProcessed(webhookPayloadAdVideoProcessed);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAdVideoProcessed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAdVideoProcessedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad video processed event
    apiInstance.OnAdVideoProcessedWithHttpInfo(webhookPayloadAdVideoProcessed);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAdVideoProcessedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAdVideoProcessed** | [**WebhookPayloadAdVideoProcessed**](WebhookPayloadAdVideoProcessed.md) |  |  |

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

<a id="onanalyticssynced"></a>
# **OnAnalyticsSynced**
> void OnAnalyticsSynced (WebhookPayloadAnalyticsSynced webhookPayloadAnalyticsSynced)

Analytics synced event

One connected account's analytics sync cycle completed successfully.  ### Payload notes  It is a trigger: no metrics and no cursor. On receipt, call `GET /v1/analytics/delta` with your own last `nextCursor` to read what changed across every account.  ### When it fires  Per account, per successful sync cycle, roughly hourly. It does not fire for a failed or skipped cycle, an inactive or disconnected account, or a platform without analytics sync.  ### Empty page  The feed is a materialized view, so an immediate read can return an empty `data` array. Re-poll with the same cursor. Advancing on an empty page can lose changes permanently.  ### Use a dedicated endpoint  Volume is about one event per account per hour. The consecutive-failure count is shared by every event on an endpoint, so an outage here can disable it and silence events like `post.published`. 

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
    public class OnAnalyticsSyncedExample
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
            var webhookPayloadAnalyticsSynced = new WebhookPayloadAnalyticsSynced(); // WebhookPayloadAnalyticsSynced | 

            try
            {
                // Analytics synced event
                apiInstance.OnAnalyticsSynced(webhookPayloadAnalyticsSynced);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAnalyticsSynced: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAnalyticsSyncedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Analytics synced event
    apiInstance.OnAnalyticsSyncedWithHttpInfo(webhookPayloadAnalyticsSynced);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAnalyticsSyncedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAnalyticsSynced** | [**WebhookPayloadAnalyticsSynced**](WebhookPayloadAnalyticsSynced.md) |  |  |

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

<a id="onapichangelogpublished"></a>
# **OnApiChangelogPublished**
> void OnApiChangelogPublished (WebhookPayloadApiChangelogPublished webhookPayloadApiChangelogPublished)

API changelog entry published event

An entry was published to the API changelog when a change to the OpenAPI spec went live.  ### Who receives it  It belongs to no profile or account. Every active endpoint subscribed to it receives it; endpoints scoped with `profileIds` or `accountIds` do not. One subscription per integration is enough.  ### Payload notes  `entry.type`, `entry.message` (the announcement), `entry.url`, `entry.specVersion`, `entry.impact` (`action_required`, `additive` or `none`) and `entry.changes` (the spec diff as data).  ### How to act  Automate on `impact`, `changes` and `type`; read `message` for the reason. `GET /v1/changelog` lists entries newest first, to back-fill after downtime. 

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
    public class OnApiChangelogPublishedExample
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
            var webhookPayloadApiChangelogPublished = new WebhookPayloadApiChangelogPublished(); // WebhookPayloadApiChangelogPublished | 

            try
            {
                // API changelog entry published event
                apiInstance.OnApiChangelogPublished(webhookPayloadApiChangelogPublished);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnApiChangelogPublished: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnApiChangelogPublishedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // API changelog entry published event
    apiInstance.OnApiChangelogPublishedWithHttpInfo(webhookPayloadApiChangelogPublished);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnApiChangelogPublishedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadApiChangelogPublished** | [**WebhookPayloadApiChangelogPublished**](WebhookPayloadApiChangelogPublished.md) |  |  |

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

<a id="onautomationactionapplied"></a>
# **OnAutomationActionApplied**
> void OnAutomationActionApplied (WebhookPayloadAutomationAction webhookPayloadAutomationAction)

Automation action applied event

An automation changed something, such as an ad set paused or a budget raised.  ### Payload notes  `previous` and `target` carry the value before and the value set. Each action sends one event; dedupe on `id`, which stays the same if the event is sent again. 

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
    public class OnAutomationActionAppliedExample
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
            var webhookPayloadAutomationAction = new WebhookPayloadAutomationAction(); // WebhookPayloadAutomationAction | 

            try
            {
                // Automation action applied event
                apiInstance.OnAutomationActionApplied(webhookPayloadAutomationAction);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAutomationActionApplied: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAutomationActionAppliedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Automation action applied event
    apiInstance.OnAutomationActionAppliedWithHttpInfo(webhookPayloadAutomationAction);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAutomationActionAppliedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAutomationAction** | [**WebhookPayloadAutomationAction**](WebhookPayloadAutomationAction.md) |  |  |

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
| **200** | Webhook received |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onautomationactionfailed"></a>
# **OnAutomationActionFailed**
> void OnAutomationActionFailed (WebhookPayloadAutomationAction webhookPayloadAutomationAction)

Automation action failed event

An automation change failed or was refused; `reason` says why.  ### Skipped changes  A change refused before any platform call has `status: skipped`, for example no live ads or a budget at its limit. 

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
    public class OnAutomationActionFailedExample
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
            var webhookPayloadAutomationAction = new WebhookPayloadAutomationAction(); // WebhookPayloadAutomationAction | 

            try
            {
                // Automation action failed event
                apiInstance.OnAutomationActionFailed(webhookPayloadAutomationAction);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAutomationActionFailed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAutomationActionFailedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Automation action failed event
    apiInstance.OnAutomationActionFailedWithHttpInfo(webhookPayloadAutomationAction);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAutomationActionFailedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAutomationAction** | [**WebhookPayloadAutomationAction**](WebhookPayloadAutomationAction.md) |  |  |

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
| **200** | Webhook received |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onautomationactionunknown"></a>
# **OnAutomationActionUnknown**
> void OnAutomationActionUnknown (WebhookPayloadAutomationAction webhookPayloadAutomationAction)

Automation action unknown event

The platform did not answer, so it is unknown whether the automation's change happened.  ### What happens next  The next check reads the object back and sends `applied` or `failed`. 

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
    public class OnAutomationActionUnknownExample
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
            var webhookPayloadAutomationAction = new WebhookPayloadAutomationAction(); // WebhookPayloadAutomationAction | 

            try
            {
                // Automation action unknown event
                apiInstance.OnAutomationActionUnknown(webhookPayloadAutomationAction);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAutomationActionUnknown: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAutomationActionUnknownWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Automation action unknown event
    apiInstance.OnAutomationActionUnknownWithHttpInfo(webhookPayloadAutomationAction);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAutomationActionUnknownWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAutomationAction** | [**WebhookPayloadAutomationAction**](WebhookPayloadAutomationAction.md) |  |  |

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
| **200** | Webhook received |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onautomationalertescalated"></a>
# **OnAutomationAlertEscalated**
> void OnAutomationAlertEscalated (WebhookPayloadAutomationAlert webhookPayloadAutomationAlert)

Automation alert escalated event

An open alert's `critical` conditions held.  ### When it fires  Sent once per episode. 

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
    public class OnAutomationAlertEscalatedExample
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
            var webhookPayloadAutomationAlert = new WebhookPayloadAutomationAlert(); // WebhookPayloadAutomationAlert | 

            try
            {
                // Automation alert escalated event
                apiInstance.OnAutomationAlertEscalated(webhookPayloadAutomationAlert);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAutomationAlertEscalated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAutomationAlertEscalatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Automation alert escalated event
    apiInstance.OnAutomationAlertEscalatedWithHttpInfo(webhookPayloadAutomationAlert);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAutomationAlertEscalatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAutomationAlert** | [**WebhookPayloadAutomationAlert**](WebhookPayloadAutomationAlert.md) |  |  |

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
| **200** | Webhook received |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onautomationalertopened"></a>
# **OnAutomationAlertOpened**
> void OnAutomationAlertOpened (WebhookPayloadAutomationAlert webhookPayloadAutomationAlert)

Automation alert opened event

An object matched the rule's conditions for `confirmChecks` runs in a row and its action was recorded.  ### When it fires  Sent once per episode. 

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
    public class OnAutomationAlertOpenedExample
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
            var webhookPayloadAutomationAlert = new WebhookPayloadAutomationAlert(); // WebhookPayloadAutomationAlert | 

            try
            {
                // Automation alert opened event
                apiInstance.OnAutomationAlertOpened(webhookPayloadAutomationAlert);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAutomationAlertOpened: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAutomationAlertOpenedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Automation alert opened event
    apiInstance.OnAutomationAlertOpenedWithHttpInfo(webhookPayloadAutomationAlert);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAutomationAlertOpenedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAutomationAlert** | [**WebhookPayloadAutomationAlert**](WebhookPayloadAutomationAlert.md) |  |  |

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
| **200** | Webhook received |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onautomationalertresolved"></a>
# **OnAutomationAlertResolved**
> void OnAutomationAlertResolved (WebhookPayloadAutomationAlert webhookPayloadAutomationAlert)

Automation alert resolved event

An open alert ended; `reason` says which way.  ### Reasons  Its conditions cleared, a pause or reactivation applied, the rule changed, or nothing checked the object for 7 days. 

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
    public class OnAutomationAlertResolvedExample
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
            var webhookPayloadAutomationAlert = new WebhookPayloadAutomationAlert(); // WebhookPayloadAutomationAlert | 

            try
            {
                // Automation alert resolved event
                apiInstance.OnAutomationAlertResolved(webhookPayloadAutomationAlert);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAutomationAlertResolved: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAutomationAlertResolvedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Automation alert resolved event
    apiInstance.OnAutomationAlertResolvedWithHttpInfo(webhookPayloadAutomationAlert);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAutomationAlertResolvedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAutomationAlert** | [**WebhookPayloadAutomationAlert**](WebhookPayloadAutomationAlert.md) |  |  |

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
| **200** | Webhook received |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onautomationcheckcompleted"></a>
# **OnAutomationCheckCompleted**
> void OnAutomationCheckCompleted (WebhookPayloadAutomationCheckCompleted webhookPayloadAutomationCheckCompleted)

Automation check completed event

One scheduled check of an automation finished, including checks where nothing matched.  ### Payload notes  `automation.kind` names the product: `ad_rule` today, more as other automations move onto the same engine. 

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
    public class OnAutomationCheckCompletedExample
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
            var webhookPayloadAutomationCheckCompleted = new WebhookPayloadAutomationCheckCompleted(); // WebhookPayloadAutomationCheckCompleted | 

            try
            {
                // Automation check completed event
                apiInstance.OnAutomationCheckCompleted(webhookPayloadAutomationCheckCompleted);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnAutomationCheckCompleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnAutomationCheckCompletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Automation check completed event
    apiInstance.OnAutomationCheckCompletedWithHttpInfo(webhookPayloadAutomationCheckCompleted);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnAutomationCheckCompletedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadAutomationCheckCompleted** | [**WebhookPayloadAutomationCheckCompleted**](WebhookPayloadAutomationCheckCompleted.md) |  |  |

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
| **200** | Webhook received |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onbalancecharged"></a>
# **OnBalanceCharged**
> void OnBalanceCharged (WebhookPayloadBalanceCharged webhookPayloadBalanceCharged)

Balance charged event

Balance billing only. Funds were added to the balance by card: by someone (`trigger: manual`) or by the auto top-up rule (`trigger: auto_top_up`).  ### When it fires  Once per card payment into the balance, when it is credited. Stripe emails the billing owner its receipt for the charge.  ### Payload notes  `topup.amountCents` was added to the balance; the card was charged `topup.chargedCents`, which is that plus `topup.taxCents` (VAT, 0 when none applies). The invoice and receipt are at `GET /v1/balance/top-ups/{topupId}/invoice` and `/receipt`.  ### Who receives it  The billing owner's endpoints, like `balance.low`. Restricted keys need the `money` resource group. 

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
    public class OnBalanceChargedExample
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
            var webhookPayloadBalanceCharged = new WebhookPayloadBalanceCharged(); // WebhookPayloadBalanceCharged | 

            try
            {
                // Balance charged event
                apiInstance.OnBalanceCharged(webhookPayloadBalanceCharged);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnBalanceCharged: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnBalanceChargedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Balance charged event
    apiInstance.OnBalanceChargedWithHttpInfo(webhookPayloadBalanceCharged);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnBalanceChargedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadBalanceCharged** | [**WebhookPayloadBalanceCharged**](WebhookPayloadBalanceCharged.md) |  |  |

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

<a id="onbalanceempty"></a>
# **OnBalanceEmpty**
> void OnBalanceEmpty (WebhookPayloadBalanceEmpty webhookPayloadBalanceEmpty)

Balance empty event

Balance billing only. The balance reached $0 and no auto top-up covered it (auto top-up off, the card declined, or the monthly limit reached), so new pay-per-use (SMS, calls, numbers, X and the rest) answers 402 with `code` until the balance is funded.  ### When it fires  Once per time the balance runs out, within about a minute of the usage that emptied it. Funding the balance and running out again fires it again.  ### Who receives it  The billing owner's endpoints, like `balance.low`. Restricted keys need the `money` resource group.  ### How to act  Send the user to `fundingUrl`, or, for `usage_limit_reached`, raise `monthlyLimitCents` with `PATCH /v1/balance/auto-recharge`. 

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
    public class OnBalanceEmptyExample
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
            var webhookPayloadBalanceEmpty = new WebhookPayloadBalanceEmpty(); // WebhookPayloadBalanceEmpty | 

            try
            {
                // Balance empty event
                apiInstance.OnBalanceEmpty(webhookPayloadBalanceEmpty);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnBalanceEmpty: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnBalanceEmptyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Balance empty event
    apiInstance.OnBalanceEmptyWithHttpInfo(webhookPayloadBalanceEmpty);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnBalanceEmptyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadBalanceEmpty** | [**WebhookPayloadBalanceEmpty**](WebhookPayloadBalanceEmpty.md) |  |  |

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

<a id="onbalancelow"></a>
# **OnBalanceLow**
> void OnBalanceLow (WebhookPayloadBalanceLow webhookPayloadBalanceLow)

Balance low event

Balance billing only. The balance dropped below the low-balance alert set on auto top-up (`alertBelowCents` on `GET /v1/balance/auto-recharge`).  ### When it fires  Once per drop below the threshold; a balance back at or above it re-arms the next one. It does not fire when an auto top-up is already covering the drop, and never when no alert is set.  ### Who receives it  It belongs to the billing owner, not to a profile or account: endpoints scoped with `profileIds` or `accountIds` do not receive it. Restricted keys need the `money` resource group.  ### How to act  Send the user to `fundingUrl` (Billing with the Add funds drawer open), or add funds through the API. 

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
    public class OnBalanceLowExample
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
            var webhookPayloadBalanceLow = new WebhookPayloadBalanceLow(); // WebhookPayloadBalanceLow | 

            try
            {
                // Balance low event
                apiInstance.OnBalanceLow(webhookPayloadBalanceLow);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnBalanceLow: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnBalanceLowWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Balance low event
    apiInstance.OnBalanceLowWithHttpInfo(webhookPayloadBalanceLow);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnBalanceLowWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadBalanceLow** | [**WebhookPayloadBalanceLow**](WebhookPayloadBalanceLow.md) |  |  |

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

<a id="onbrandedcallingidentityactionrequired"></a>
# **OnBrandedCallingIdentityActionRequired**
> void OnBrandedCallingIdentityActionRequired (OnBrandedCallingIdentityActionRequiredRequest onBrandedCallingIdentityActionRequiredRequest)

Caller identity action required event

A Branded Calling caller identity is waiting on you; `reason` says what.  ### When it fires  Every `action_required` is paired with a `status_updated`.  ### Reasons  - `changes_requested`: answer the review with `PATCH`. - `email_code`: confirm the code the carrier emailed the authorizer. - `rejected`: fix and `PATCH`. - `expired`: resubmit.  ### Infringement claim  `infringement_claim`: a third party filed a trademark or impersonation claim and the carrier suspended the identity. Calls show a plain number and the monthly fee pauses until it is resolved.  Reply to our email with evidence that the name and logo are yours. If the claim is upheld, the identity is rejected for good. 

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
    public class OnBrandedCallingIdentityActionRequiredExample
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
            var onBrandedCallingIdentityActionRequiredRequest = new OnBrandedCallingIdentityActionRequiredRequest(); // OnBrandedCallingIdentityActionRequiredRequest | 

            try
            {
                // Caller identity action required event
                apiInstance.OnBrandedCallingIdentityActionRequired(onBrandedCallingIdentityActionRequiredRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnBrandedCallingIdentityActionRequired: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnBrandedCallingIdentityActionRequiredWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Caller identity action required event
    apiInstance.OnBrandedCallingIdentityActionRequiredWithHttpInfo(onBrandedCallingIdentityActionRequiredRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnBrandedCallingIdentityActionRequiredWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onBrandedCallingIdentityActionRequiredRequest** | [**OnBrandedCallingIdentityActionRequiredRequest**](OnBrandedCallingIdentityActionRequiredRequest.md) |  |  |

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

<a id="onbrandedcallingidentitystatusupdated"></a>
# **OnBrandedCallingIdentityStatusUpdated**
> void OnBrandedCallingIdentityStatusUpdated (OnBrandedCallingIdentityStatusUpdatedRequest onBrandedCallingIdentityStatusUpdatedRequest)

Caller identity status updated event

A Branded Calling caller identity changed status.  ### When it fires  Fires once per transition of the identity's `status`, the value `GET /v1/branded-calling/identities/{id}` returns. Never on a re-check that found nothing new.  ### Statuses  `requested`, `changes_requested`, `rejected` (`reason` says why), `pending_email_verification`, `in_review`, `verified` (live for a year, attach numbers), `suspended` (infringement claim open), `expired`, `permanently_rejected`. 

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
    public class OnBrandedCallingIdentityStatusUpdatedExample
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
            var onBrandedCallingIdentityStatusUpdatedRequest = new OnBrandedCallingIdentityStatusUpdatedRequest(); // OnBrandedCallingIdentityStatusUpdatedRequest | 

            try
            {
                // Caller identity status updated event
                apiInstance.OnBrandedCallingIdentityStatusUpdated(onBrandedCallingIdentityStatusUpdatedRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnBrandedCallingIdentityStatusUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnBrandedCallingIdentityStatusUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Caller identity status updated event
    apiInstance.OnBrandedCallingIdentityStatusUpdatedWithHttpInfo(onBrandedCallingIdentityStatusUpdatedRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnBrandedCallingIdentityStatusUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onBrandedCallingIdentityStatusUpdatedRequest** | [**OnBrandedCallingIdentityStatusUpdatedRequest**](OnBrandedCallingIdentityStatusUpdatedRequest.md) |  |  |

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

<a id="onbrandedcallingnumberstatusupdated"></a>
# **OnBrandedCallingNumberStatusUpdated**
> void OnBrandedCallingNumberStatusUpdated (OnBrandedCallingNumberStatusUpdatedRequest onBrandedCallingNumberStatusUpdatedRequest)

Branded number status updated event

A number attached to a Branded Calling identity changed vetting status.  ### When it fires  Only starts once the identity is `verified` and you attached numbers. A batch is vetted as a unit; each number reports its own status.  ### Statuses  `submitted`, `in_review`, `verified` (calls from it show the identity), `unsuccessful` (refused; detach and re-add to retry), `suspended`, `expired`, `permanently_rejected` (can never be branded again). 

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
    public class OnBrandedCallingNumberStatusUpdatedExample
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
            var onBrandedCallingNumberStatusUpdatedRequest = new OnBrandedCallingNumberStatusUpdatedRequest(); // OnBrandedCallingNumberStatusUpdatedRequest | 

            try
            {
                // Branded number status updated event
                apiInstance.OnBrandedCallingNumberStatusUpdated(onBrandedCallingNumberStatusUpdatedRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnBrandedCallingNumberStatusUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnBrandedCallingNumberStatusUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Branded number status updated event
    apiInstance.OnBrandedCallingNumberStatusUpdatedWithHttpInfo(onBrandedCallingNumberStatusUpdatedRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnBrandedCallingNumberStatusUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onBrandedCallingNumberStatusUpdatedRequest** | [**OnBrandedCallingNumberStatusUpdatedRequest**](OnBrandedCallingNumberStatusUpdatedRequest.md) |  |  |

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

<a id="oncalendareventcreated"></a>
# **OnCalendarEventCreated**
> void OnCalendarEventCreated (WebhookPayloadCalendarEvent webhookPayloadCalendarEvent)

Calendar event created

An event was added to the primary calendar of a connected mailbox, by the user, an invitation or the API.  ### Platform notes  On Microsoft the change is pushed seconds after it happens. 

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
    public class OnCalendarEventCreatedExample
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
            var webhookPayloadCalendarEvent = new WebhookPayloadCalendarEvent(); // WebhookPayloadCalendarEvent | 

            try
            {
                // Calendar event created
                apiInstance.OnCalendarEventCreated(webhookPayloadCalendarEvent);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCalendarEventCreated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCalendarEventCreatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Calendar event created
    apiInstance.OnCalendarEventCreatedWithHttpInfo(webhookPayloadCalendarEvent);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCalendarEventCreatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCalendarEvent** | [**WebhookPayloadCalendarEvent**](WebhookPayloadCalendarEvent.md) |  |  |

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

<a id="oncalendareventdeleted"></a>
# **OnCalendarEventDeleted**
> void OnCalendarEventDeleted (WebhookPayloadCalendarEvent webhookPayloadCalendarEvent)

Calendar event deleted

An event was deleted from the primary calendar.  ### Platform notes  On Google, a cancelled event counts as deleted. 

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
    public class OnCalendarEventDeletedExample
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
            var webhookPayloadCalendarEvent = new WebhookPayloadCalendarEvent(); // WebhookPayloadCalendarEvent | 

            try
            {
                // Calendar event deleted
                apiInstance.OnCalendarEventDeleted(webhookPayloadCalendarEvent);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCalendarEventDeleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCalendarEventDeletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Calendar event deleted
    apiInstance.OnCalendarEventDeletedWithHttpInfo(webhookPayloadCalendarEvent);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCalendarEventDeletedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCalendarEvent** | [**WebhookPayloadCalendarEvent**](WebhookPayloadCalendarEvent.md) |  |  |

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

<a id="oncalendareventupdated"></a>
# **OnCalendarEventUpdated**
> void OnCalendarEventUpdated (WebhookPayloadCalendarEvent webhookPayloadCalendarEvent)

Calendar event updated

An event on the primary calendar changed: its time, details or participants' answers. 

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
    public class OnCalendarEventUpdatedExample
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
            var webhookPayloadCalendarEvent = new WebhookPayloadCalendarEvent(); // WebhookPayloadCalendarEvent | 

            try
            {
                // Calendar event updated
                apiInstance.OnCalendarEventUpdated(webhookPayloadCalendarEvent);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCalendarEventUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCalendarEventUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Calendar event updated
    apiInstance.OnCalendarEventUpdatedWithHttpInfo(webhookPayloadCalendarEvent);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCalendarEventUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCalendarEvent** | [**WebhookPayloadCalendarEvent**](WebhookPayloadCalendarEvent.md) |  |  |

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

A phone or WhatsApp call ended; carries duration, end reason and a zero-markup cost breakdown.  ### Payload notes  `durationSeconds`; `endReason` is `hangup`, `no_answer`, `rejected` or `error`; `call.billing` holds Meta cost, Telnyx cost, recording surcharge and total. Costs are pass-through, with no margin.  ### When it fires  Unanswered, busy and rejected calls end here too. Branch on `endReason`; `call.failed` is for hard errors.  ### Recordings  With recording enabled, the payload carries `recordingUrl`, a signed URL expiring at `recordingExpiresAt`. Fetch a fresh one with `GET /v1/calls/{id}/recording` and `call.id`.  ### Missed-call follow-up  Check for `endReason: \"no_answer\"`, then text the caller over the linked `conversationId`. 

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

A call failed with a hard error before or during bridging, for example the destination rejected the SIP INVITE.  ### Payload notes  Carries the upstream error `code` and `message`, for example when Meta rejected the connect or Telnyx returned an error. 

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

A WhatsApp user accepted or rejected your call-permission request.  ### When it fires  Independent of any call: it reports a reply to a permission prompt. Meta permits a business-initiated call only after the consumer taps Allow, and the accept can land days before the call.  ### Payload notes  `response` is `accept` or `reject`. Also carries the user's number, whether the grant is permanent, and the expiry when it is not. 

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

An inbound phone or WhatsApp call reached your number, or an outbound WhatsApp call was placed.  ### When it fires  Fires at ring time, before anyone answers; an unanswered call still emits it, then `call.ended` with `endReason: \"no_answer\"`. Outbound WhatsApp calls fire at origination with `direction: \"outbound\"`. Outbound phone calls never emit it.  ### Payload notes  Carries the Zernio call id, the caller and business numbers, the destination snapshot (`forwardTo`), and `contactId` and `conversationId` to message the caller with the regular send endpoints. 

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

<a id="oncallrecordingready"></a>
# **OnCallRecordingReady**
> void OnCallRecordingReady (WebhookPayloadCallRecordingReady webhookPayloadCallRecordingReady)

Call recording ready event

A call recording is ready to download.  ### When it fires  Only for teams with zero content retention, on calls with recording on, and only while a webhook listens to it. Zernio keeps no recording for these teams, and the copy behind the link expires after about 3 days. Download the file before `recording.expiresAt`.  ### Payload notes  `call.isVoicemail` tells a voicemail from a recorded call. If the recording could not be copied, no event fires and `call.ended` lists it in `callErrors`. 

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
    public class OnCallRecordingReadyExample
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
            var webhookPayloadCallRecordingReady = new WebhookPayloadCallRecordingReady(); // WebhookPayloadCallRecordingReady | 

            try
            {
                // Call recording ready event
                apiInstance.OnCallRecordingReady(webhookPayloadCallRecordingReady);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCallRecordingReady: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCallRecordingReadyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Call recording ready event
    apiInstance.OnCallRecordingReadyWithHttpInfo(webhookPayloadCallRecordingReady);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCallRecordingReadyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCallRecordingReady** | [**WebhookPayloadCallRecordingReady**](WebhookPayloadCallRecordingReady.md) |  |  |

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

<a id="oncalltranscriptsegment"></a>
# **OnCallTranscriptSegment**
> void OnCallTranscriptSegment (WebhookPayloadCallTranscriptSegment webhookPayloadCallTranscriptSegment)

Call transcript segment event

One final segment of a live call transcript.  ### When it fires  Only for teams with zero content retention, on calls with transcription on: once per final segment, while the call is live. Zernio stores no transcript for these teams, so it cannot be fetched later. Store each segment when it arrives.  ### Payload notes  `segment.text` is the final text, `segment.confidence` the recognition confidence and `segment.at` when it was transcribed. 

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
    public class OnCallTranscriptSegmentExample
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
            var webhookPayloadCallTranscriptSegment = new WebhookPayloadCallTranscriptSegment(); // WebhookPayloadCallTranscriptSegment | 

            try
            {
                // Call transcript segment event
                apiInstance.OnCallTranscriptSegment(webhookPayloadCallTranscriptSegment);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCallTranscriptSegment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCallTranscriptSegmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Call transcript segment event
    apiInstance.OnCallTranscriptSegmentWithHttpInfo(webhookPayloadCallTranscriptSegment);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCallTranscriptSegmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCallTranscriptSegment** | [**WebhookPayloadCallTranscriptSegment**](WebhookPayloadCallTranscriptSegment.md) |  |  |

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

<a id="oncampaignbudgetdepleted"></a>
# **OnCampaignBudgetDepleted**
> void OnCampaignBudgetDepleted (WebhookPayloadCampaignBudgetDepleted webhookPayloadCampaignBudgetDepleted)

Campaign budget depleted event

A campaign Zernio already tracked ran out of budget. TikTok only.  ### When it fires  Fires once per campaign when its budget runs out, at most once per 6 hours, so a daily budget that runs out again the next day is announced again.  ### When it does not fire  Ads seen for the first time by a sync never fire it.  ### Platform notes  Only TikTok reports this on the ad. Meta and Google keep such ads `ACTIVE`, so they never fire it. 

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
    public class OnCampaignBudgetDepletedExample
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
            var webhookPayloadCampaignBudgetDepleted = new WebhookPayloadCampaignBudgetDepleted(); // WebhookPayloadCampaignBudgetDepleted | 

            try
            {
                // Campaign budget depleted event
                apiInstance.OnCampaignBudgetDepleted(webhookPayloadCampaignBudgetDepleted);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignBudgetDepleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignBudgetDepletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign budget depleted event
    apiInstance.OnCampaignBudgetDepletedWithHttpInfo(webhookPayloadCampaignBudgetDepleted);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignBudgetDepletedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignBudgetDepleted** | [**WebhookPayloadCampaignBudgetDepleted**](WebhookPayloadCampaignBudgetDepleted.md) |  |  |

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

<a id="oncampaigncreated"></a>
# **OnCampaignCreated**
> void OnCampaignCreated (WebhookPayloadCampaignCreated webhookPayloadCampaignCreated)

Campaign created event

A campaign was created through Zernio (`source: \"zernio\"`) or detected by the sync (`source: \"platform\"`).  ### When it fires  Fires once the campaign row is recorded. A detected campaign arrives up to one sync interval late.  ### When it does not fire  History loaded when an account connects, and campaigns created more than 7 days ago, are never announced. 

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
    public class OnCampaignCreatedExample
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
            var webhookPayloadCampaignCreated = new WebhookPayloadCampaignCreated(); // WebhookPayloadCampaignCreated | 

            try
            {
                // Campaign created event
                apiInstance.OnCampaignCreated(webhookPayloadCampaignCreated);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignCreated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignCreatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign created event
    apiInstance.OnCampaignCreatedWithHttpInfo(webhookPayloadCampaignCreated);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignCreatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignCreated** | [**WebhookPayloadCampaignCreated**](WebhookPayloadCampaignCreated.md) |  |  |

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

<a id="oncampaignparticipantjoined"></a>
# **OnCampaignParticipantJoined**
> void OnCampaignParticipantJoined (WebhookPayloadCampaignParticipant webhookPayloadCampaignParticipant)

Campaign participant joined event

A creator joined a campaign from their invite link or the open link.  ### When it fires  It fires once per participant, and `participant.joinedAt` says when. 

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
    public class OnCampaignParticipantJoinedExample
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
            var webhookPayloadCampaignParticipant = new WebhookPayloadCampaignParticipant(); // WebhookPayloadCampaignParticipant | 

            try
            {
                // Campaign participant joined event
                apiInstance.OnCampaignParticipantJoined(webhookPayloadCampaignParticipant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignParticipantJoined: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignParticipantJoinedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign participant joined event
    apiInstance.OnCampaignParticipantJoinedWithHttpInfo(webhookPayloadCampaignParticipant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignParticipantJoinedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignParticipant** | [**WebhookPayloadCampaignParticipant**](WebhookPayloadCampaignParticipant.md) |  |  |

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

<a id="oncampaignparticipantremoved"></a>
# **OnCampaignParticipantRemoved**
> void OnCampaignParticipantRemoved (WebhookPayloadCampaignParticipant webhookPayloadCampaignParticipant)

Campaign participant removed event

You removed a participant from the campaign.  ### When it does not fire  Removing a participant twice fires the event once. 

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
    public class OnCampaignParticipantRemovedExample
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
            var webhookPayloadCampaignParticipant = new WebhookPayloadCampaignParticipant(); // WebhookPayloadCampaignParticipant | 

            try
            {
                // Campaign participant removed event
                apiInstance.OnCampaignParticipantRemoved(webhookPayloadCampaignParticipant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignParticipantRemoved: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignParticipantRemovedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign participant removed event
    apiInstance.OnCampaignParticipantRemovedWithHttpInfo(webhookPayloadCampaignParticipant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignParticipantRemovedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignParticipant** | [**WebhookPayloadCampaignParticipant**](WebhookPayloadCampaignParticipant.md) |  |  |

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

<a id="oncampaignparticipantsuspended"></a>
# **OnCampaignParticipantSuspended**
> void OnCampaignParticipantSuspended (WebhookPayloadCampaignParticipant webhookPayloadCampaignParticipant)

Campaign participant suspended event

You suspended a participant.  ### Effect  They can no longer connect accounts or submit posts to this campaign. Posts they already submitted keep earning until you reject them. 

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
    public class OnCampaignParticipantSuspendedExample
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
            var webhookPayloadCampaignParticipant = new WebhookPayloadCampaignParticipant(); // WebhookPayloadCampaignParticipant | 

            try
            {
                // Campaign participant suspended event
                apiInstance.OnCampaignParticipantSuspended(webhookPayloadCampaignParticipant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignParticipantSuspended: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignParticipantSuspendedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign participant suspended event
    apiInstance.OnCampaignParticipantSuspendedWithHttpInfo(webhookPayloadCampaignParticipant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignParticipantSuspendedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignParticipant** | [**WebhookPayloadCampaignParticipant**](WebhookPayloadCampaignParticipant.md) |  |  |

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

<a id="oncampaignpayoutfailed"></a>
# **OnCampaignPayoutFailed**
> void OnCampaignPayoutFailed (WebhookPayloadCampaignPayout webhookPayloadCampaignPayout)

Campaign payout failed event

A payout through Zernio did not reach the creator.  ### When it fires  Stripe refused it, it stayed unconfirmed for 24 hours, or it was reversed. The amount is payable again, minus anything a rejection claws back. 

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
    public class OnCampaignPayoutFailedExample
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
            var webhookPayloadCampaignPayout = new WebhookPayloadCampaignPayout(); // WebhookPayloadCampaignPayout | 

            try
            {
                // Campaign payout failed event
                apiInstance.OnCampaignPayoutFailed(webhookPayloadCampaignPayout);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignPayoutFailed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignPayoutFailedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign payout failed event
    apiInstance.OnCampaignPayoutFailedWithHttpInfo(webhookPayloadCampaignPayout);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignPayoutFailedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignPayout** | [**WebhookPayloadCampaignPayout**](WebhookPayloadCampaignPayout.md) |  |  |

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

<a id="oncampaignpayoutpayable"></a>
# **OnCampaignPayoutPayable**
> void OnCampaignPayoutPayable (WebhookPayloadCampaignPayout webhookPayloadCampaignPayout)

Campaign payout payable event

A participant's held earnings matured and became payable.  ### Payload notes  `payout.payableCents` is the participant's whole payable balance, the amount to pay when you pay from your own rails. 

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
    public class OnCampaignPayoutPayableExample
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
            var webhookPayloadCampaignPayout = new WebhookPayloadCampaignPayout(); // WebhookPayloadCampaignPayout | 

            try
            {
                // Campaign payout payable event
                apiInstance.OnCampaignPayoutPayable(webhookPayloadCampaignPayout);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignPayoutPayable: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignPayoutPayableWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign payout payable event
    apiInstance.OnCampaignPayoutPayableWithHttpInfo(webhookPayloadCampaignPayout);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignPayoutPayableWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignPayout** | [**WebhookPayloadCampaignPayout**](WebhookPayloadCampaignPayout.md) |  |  |

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

<a id="oncampaignpayoutsettled"></a>
# **OnCampaignPayoutSettled**
> void OnCampaignPayoutSettled (WebhookPayloadCampaignPayout webhookPayloadCampaignPayout)

Campaign payout settled event

A payout to a participant was recorded.  ### Payload notes  `payout.settlement` holds the amount and the reference. `recorded` is true when the money moved outside Zernio. 

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
    public class OnCampaignPayoutSettledExample
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
            var webhookPayloadCampaignPayout = new WebhookPayloadCampaignPayout(); // WebhookPayloadCampaignPayout | 

            try
            {
                // Campaign payout settled event
                apiInstance.OnCampaignPayoutSettled(webhookPayloadCampaignPayout);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignPayoutSettled: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignPayoutSettledWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign payout settled event
    apiInstance.OnCampaignPayoutSettledWithHttpInfo(webhookPayloadCampaignPayout);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignPayoutSettledWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignPayout** | [**WebhookPayloadCampaignPayout**](WebhookPayloadCampaignPayout.md) |  |  |

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

<a id="oncampaignsubmissionapproved"></a>
# **OnCampaignSubmissionApproved**
> void OnCampaignSubmissionApproved (WebhookPayloadCampaignSubmission webhookPayloadCampaignSubmission)

Campaign submission approved event

You approved a submission.  ### Earnings  What the submission earned so far moves to owed with the campaign hold. Later earnings post straight to owed. 

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
    public class OnCampaignSubmissionApprovedExample
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
            var webhookPayloadCampaignSubmission = new WebhookPayloadCampaignSubmission(); // WebhookPayloadCampaignSubmission | 

            try
            {
                // Campaign submission approved event
                apiInstance.OnCampaignSubmissionApproved(webhookPayloadCampaignSubmission);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignSubmissionApproved: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignSubmissionApprovedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign submission approved event
    apiInstance.OnCampaignSubmissionApprovedWithHttpInfo(webhookPayloadCampaignSubmission);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignSubmissionApprovedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignSubmission** | [**WebhookPayloadCampaignSubmission**](WebhookPayloadCampaignSubmission.md) |  |  |

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

<a id="oncampaignsubmissionflagged"></a>
# **OnCampaignSubmissionFlagged**
> void OnCampaignSubmissionFlagged (WebhookPayloadCampaignSubmission webhookPayloadCampaignSubmission)

Campaign submission flagged event

A submission gained a fraud flag it did not carry before, at submission or on a later sync.  ### Flags  Flags include `duplicate_post`, `view_spike`, `low_authenticity` and `x_read_cap` (the campaign's X read budget is spent). `submission.flags` lists every flag it carries. Zernio never rejects on its own; the decision is yours. 

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
    public class OnCampaignSubmissionFlaggedExample
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
            var webhookPayloadCampaignSubmission = new WebhookPayloadCampaignSubmission(); // WebhookPayloadCampaignSubmission | 

            try
            {
                // Campaign submission flagged event
                apiInstance.OnCampaignSubmissionFlagged(webhookPayloadCampaignSubmission);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignSubmissionFlagged: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignSubmissionFlaggedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign submission flagged event
    apiInstance.OnCampaignSubmissionFlaggedWithHttpInfo(webhookPayloadCampaignSubmission);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignSubmissionFlaggedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignSubmission** | [**WebhookPayloadCampaignSubmission**](WebhookPayloadCampaignSubmission.md) |  |  |

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

<a id="oncampaignsubmissionpendingreview"></a>
# **OnCampaignSubmissionPendingReview**
> void OnCampaignSubmissionPendingReview (WebhookPayloadCampaignSubmission webhookPayloadCampaignSubmission)

Campaign submission pending review event

A submission is ready for your review.  ### When it fires  A CPM submission reached `minViewsToEarn`, a pool submission reached `minViewsToQualify`, and per post submissions arrive here after their first accrual. 

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
    public class OnCampaignSubmissionPendingReviewExample
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
            var webhookPayloadCampaignSubmission = new WebhookPayloadCampaignSubmission(); // WebhookPayloadCampaignSubmission | 

            try
            {
                // Campaign submission pending review event
                apiInstance.OnCampaignSubmissionPendingReview(webhookPayloadCampaignSubmission);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignSubmissionPendingReview: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignSubmissionPendingReviewWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign submission pending review event
    apiInstance.OnCampaignSubmissionPendingReviewWithHttpInfo(webhookPayloadCampaignSubmission);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignSubmissionPendingReviewWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignSubmission** | [**WebhookPayloadCampaignSubmission**](WebhookPayloadCampaignSubmission.md) |  |  |

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

<a id="oncampaignsubmissionreceived"></a>
# **OnCampaignSubmissionReceived**
> void OnCampaignSubmissionReceived (WebhookPayloadCampaignSubmission webhookPayloadCampaignSubmission)

Campaign submission received event

A creator submitted a post to a campaign, Zernio opened its tracking window and took the first view sample. 

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
    public class OnCampaignSubmissionReceivedExample
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
            var webhookPayloadCampaignSubmission = new WebhookPayloadCampaignSubmission(); // WebhookPayloadCampaignSubmission | 

            try
            {
                // Campaign submission received event
                apiInstance.OnCampaignSubmissionReceived(webhookPayloadCampaignSubmission);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignSubmissionReceived: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignSubmissionReceivedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign submission received event
    apiInstance.OnCampaignSubmissionReceivedWithHttpInfo(webhookPayloadCampaignSubmission);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignSubmissionReceivedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignSubmission** | [**WebhookPayloadCampaignSubmission**](WebhookPayloadCampaignSubmission.md) |  |  |

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

<a id="oncampaignsubmissionrejected"></a>
# **OnCampaignSubmissionRejected**
> void OnCampaignSubmissionRejected (WebhookPayloadCampaignSubmission webhookPayloadCampaignSubmission)

Campaign submission rejected event

You rejected a submission and its tracking window was cancelled.  ### Earnings  Its unsettled earnings go back to the campaign budget. 

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
    public class OnCampaignSubmissionRejectedExample
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
            var webhookPayloadCampaignSubmission = new WebhookPayloadCampaignSubmission(); // WebhookPayloadCampaignSubmission | 

            try
            {
                // Campaign submission rejected event
                apiInstance.OnCampaignSubmissionRejected(webhookPayloadCampaignSubmission);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignSubmissionRejected: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignSubmissionRejectedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign submission rejected event
    apiInstance.OnCampaignSubmissionRejectedWithHttpInfo(webhookPayloadCampaignSubmission);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignSubmissionRejectedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignSubmission** | [**WebhookPayloadCampaignSubmission**](WebhookPayloadCampaignSubmission.md) |  |  |

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

<a id="oncampaignupdated"></a>
# **OnCampaignUpdated**
> void OnCampaignUpdated (WebhookPayloadCampaignUpdated webhookPayloadCampaignUpdated)

Campaign updated event

A campaign was edited through Zernio (`source: \"zernio\"`), or outside Zernio and detected by the sync (`source: \"platform\"`).  ### When it fires  Fires after the platform and Zernio both accepted the edit. Outside edits arrive up to one sync interval late, and only to the user whose sync saw them.  ### Deduplication  Events are not deduplicated, so every edit is announced. Use the event `id` to drop repeats.  ### Payload notes  `changes` lists the edited fields: `name`, `status` (the campaign's own on/off switch), `budget`, `bid` or `settings`. Ignore unknown values. It never carries old or new values, so read the campaign.  ### What the sync detects  From the sync, `changes` covers only `name`, `status` and `schedule`. Schedule is detected only on Google, LinkedIn, Pinterest and OpenAI Ads.  ### When it does not fire  Budget edits made outside Zernio and history loaded at connect are not announced. Ad set edits arrive as `ad_set.updated`. Ad rule changes arrive as `ad_rule.triggered`.  ### Google sub-resources  Edits to ad schedule, targeting, negative keywords, conversion goals, assets, asset groups and listing group filters are not announced. 

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
    public class OnCampaignUpdatedExample
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
            var webhookPayloadCampaignUpdated = new WebhookPayloadCampaignUpdated(); // WebhookPayloadCampaignUpdated | 

            try
            {
                // Campaign updated event
                apiInstance.OnCampaignUpdated(webhookPayloadCampaignUpdated);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCampaignUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCampaignUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Campaign updated event
    apiInstance.OnCampaignUpdatedWithHttpInfo(webhookPayloadCampaignUpdated);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCampaignUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCampaignUpdated** | [**WebhookPayloadCampaignUpdated**](WebhookPayloadCampaignUpdated.md) |  |  |

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

A new comment arrived on a tracked post.  ### Platform notes  Delivered for Instagram, Facebook, Threads, YouTube, LinkedIn, Bluesky, Reddit and TikTok. X/Twitter does not fire it. TikTok needs an account connected through the TikTok for Business app.  ### Delivery timing  Instagram, Facebook, Threads and TikTok arrive in real time from the platform's webhook. The rest are poll-driven, so delivery is not instant.  ### Live comments  On Instagram, `comment.isLive: true` marks a comment made during a live broadcast. The key is absent on every other comment.  ### Ads  `comment.ad` is present only on comments made on paid content, so `if (comment.ad)` filters ad-driven comments.  ### Ad fields  Instagram carries `ad.id` and `ad.title`. Facebook carries `ad.promotionStatus`: `active` for boosted organic posts, `ineligible` for dark post creatives.  ### Instagram author profile  Comments may carry `comment.author.instagramProfile` (`isFollower`, `isFollowing`, `followerCount`, `isVerified`). An absent object means unknown, never \"not a follower\".  ### Why the profile is often absent  Meta reveals the follow relationship only for people who have messaged the account, and commenting does not grant that consent. The object is absent for most first-time commenters. 

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

<a id="oncommerceordercreated"></a>
# **OnCommerceOrderCreated**
> void OnCommerceOrderCreated (WebhookPayloadCommerceOrder webhookPayloadCommerceOrder)

Commerce order created event

An order was placed in the store.  ### Payload notes  `resource.status` is its normalized state at that moment. Read the order with `GET /v1/commerce/orders/{orderId}?accountId=...`. Fires once per Zernio account. 

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
    public class OnCommerceOrderCreatedExample
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
            var webhookPayloadCommerceOrder = new WebhookPayloadCommerceOrder(); // WebhookPayloadCommerceOrder | 

            try
            {
                // Commerce order created event
                apiInstance.OnCommerceOrderCreated(webhookPayloadCommerceOrder);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCommerceOrderCreated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCommerceOrderCreatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Commerce order created event
    apiInstance.OnCommerceOrderCreatedWithHttpInfo(webhookPayloadCommerceOrder);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCommerceOrderCreatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCommerceOrder** | [**WebhookPayloadCommerceOrder**](WebhookPayloadCommerceOrder.md) |  |  |

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

<a id="oncommerceorderrefunded"></a>
# **OnCommerceOrderRefunded**
> void OnCommerceOrderRefunded (WebhookPayloadCommerceOrder webhookPayloadCommerceOrder)

Commerce order refunded event

A refund was issued on an order.  ### Payload notes  `resource.id` is the order id, not the refund id. `resource.status` and `resource.platformStatus` are `null`. A `commerce.order.updated` usually follows for the same change. 

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
    public class OnCommerceOrderRefundedExample
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
            var webhookPayloadCommerceOrder = new WebhookPayloadCommerceOrder(); // WebhookPayloadCommerceOrder | 

            try
            {
                // Commerce order refunded event
                apiInstance.OnCommerceOrderRefunded(webhookPayloadCommerceOrder);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCommerceOrderRefunded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCommerceOrderRefundedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Commerce order refunded event
    apiInstance.OnCommerceOrderRefundedWithHttpInfo(webhookPayloadCommerceOrder);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCommerceOrderRefundedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCommerceOrder** | [**WebhookPayloadCommerceOrder**](WebhookPayloadCommerceOrder.md) |  |  |

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

<a id="oncommerceorderupdated"></a>
# **OnCommerceOrderUpdated**
> void OnCommerceOrderUpdated (WebhookPayloadCommerceOrder webhookPayloadCommerceOrder)

Commerce order updated event

An order changed in the store, such as payment, fulfilment, cancellation or edits.  ### Payload notes  `resource.status` is the new state. Refunds also fire it. Fires once per Zernio account connected to the store. 

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
    public class OnCommerceOrderUpdatedExample
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
            var webhookPayloadCommerceOrder = new WebhookPayloadCommerceOrder(); // WebhookPayloadCommerceOrder | 

            try
            {
                // Commerce order updated event
                apiInstance.OnCommerceOrderUpdated(webhookPayloadCommerceOrder);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCommerceOrderUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCommerceOrderUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Commerce order updated event
    apiInstance.OnCommerceOrderUpdatedWithHttpInfo(webhookPayloadCommerceOrder);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCommerceOrderUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCommerceOrder** | [**WebhookPayloadCommerceOrder**](WebhookPayloadCommerceOrder.md) |  |  |

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

<a id="oncommerceproductcreated"></a>
# **OnCommerceProductCreated**
> void OnCommerceProductCreated (WebhookPayloadCommerceProduct webhookPayloadCommerceProduct)

Commerce product created event

A product was created in a connected Shopify store or WooCommerce site.  ### Payload notes  `resource.id` is the store's product id. Read the product with `GET /v1/commerce/products/{productId}?accountId=...`. Fires once per Zernio account connected to the store. 

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
    public class OnCommerceProductCreatedExample
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
            var webhookPayloadCommerceProduct = new WebhookPayloadCommerceProduct(); // WebhookPayloadCommerceProduct | 

            try
            {
                // Commerce product created event
                apiInstance.OnCommerceProductCreated(webhookPayloadCommerceProduct);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCommerceProductCreated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCommerceProductCreatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Commerce product created event
    apiInstance.OnCommerceProductCreatedWithHttpInfo(webhookPayloadCommerceProduct);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCommerceProductCreatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCommerceProduct** | [**WebhookPayloadCommerceProduct**](WebhookPayloadCommerceProduct.md) |  |  |

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

<a id="oncommerceproductdeleted"></a>
# **OnCommerceProductDeleted**
> void OnCommerceProductDeleted (WebhookPayloadCommerceProduct webhookPayloadCommerceProduct)

Commerce product deleted event

A product was deleted in the store.  ### Payload notes  `resource.status` and `resource.platformStatus` are `null`. Fires once per Zernio account connected to the store. 

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
    public class OnCommerceProductDeletedExample
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
            var webhookPayloadCommerceProduct = new WebhookPayloadCommerceProduct(); // WebhookPayloadCommerceProduct | 

            try
            {
                // Commerce product deleted event
                apiInstance.OnCommerceProductDeleted(webhookPayloadCommerceProduct);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCommerceProductDeleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCommerceProductDeletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Commerce product deleted event
    apiInstance.OnCommerceProductDeletedWithHttpInfo(webhookPayloadCommerceProduct);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCommerceProductDeletedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCommerceProduct** | [**WebhookPayloadCommerceProduct**](WebhookPayloadCommerceProduct.md) |  |  |

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

<a id="oncommerceproductupdated"></a>
# **OnCommerceProductUpdated**
> void OnCommerceProductUpdated (WebhookPayloadCommerceProduct webhookPayloadCommerceProduct)

Commerce product updated event

A product changed in the store, or WooCommerce restored it from the trash.  ### Payload notes  Fields, status, variants or prices changed; read the product for what. There is no restored event. Fires once per Zernio account connected to the store. 

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
    public class OnCommerceProductUpdatedExample
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
            var webhookPayloadCommerceProduct = new WebhookPayloadCommerceProduct(); // WebhookPayloadCommerceProduct | 

            try
            {
                // Commerce product updated event
                apiInstance.OnCommerceProductUpdated(webhookPayloadCommerceProduct);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCommerceProductUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCommerceProductUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Commerce product updated event
    apiInstance.OnCommerceProductUpdatedWithHttpInfo(webhookPayloadCommerceProduct);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCommerceProductUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCommerceProduct** | [**WebhookPayloadCommerceProduct**](WebhookPayloadCommerceProduct.md) |  |  |

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

<a id="oncontactdeleted"></a>
# **OnContactDeleted**
> void OnContactDeleted (WebhookPayloadContact webhookPayloadContact)

Contact deleted

A contact was deleted in Google Contacts or Outlook.  ### Effect  Zernio removes its email channel for that account; the contact stays when other channels remain. It arrives up to a day after the change, from the daily sync. 

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
    public class OnContactDeletedExample
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
            var webhookPayloadContact = new WebhookPayloadContact(); // WebhookPayloadContact | 

            try
            {
                // Contact deleted
                apiInstance.OnContactDeleted(webhookPayloadContact);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnContactDeleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnContactDeletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Contact deleted
    apiInstance.OnContactDeletedWithHttpInfo(webhookPayloadContact);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnContactDeletedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadContact** | [**WebhookPayloadContact**](WebhookPayloadContact.md) |  |  |

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

<a id="oncontactfieldchanged"></a>
# **OnContactFieldChanged**
> void OnContactFieldChanged (WebhookPayloadContactFieldChanged webhookPayloadContactFieldChanged)

Contact field changed event

A contact custom field changed value; `field` is the field slug.  ### When it fires  Once per custom field whose value a write changed. Writing the current value fires nothing.  ### Payload notes  `previousValue` is `null` when the field was not set. `value` is `null` when it was removed. 

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
    public class OnContactFieldChangedExample
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
            var webhookPayloadContactFieldChanged = new WebhookPayloadContactFieldChanged(); // WebhookPayloadContactFieldChanged | 

            try
            {
                // Contact field changed event
                apiInstance.OnContactFieldChanged(webhookPayloadContactFieldChanged);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnContactFieldChanged: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnContactFieldChangedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Contact field changed event
    apiInstance.OnContactFieldChangedWithHttpInfo(webhookPayloadContactFieldChanged);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnContactFieldChangedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadContactFieldChanged** | [**WebhookPayloadContactFieldChanged**](WebhookPayloadContactFieldChanged.md) |  |  |

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

<a id="oncontacttagadded"></a>
# **OnContactTagAdded**
> void OnContactTagAdded (WebhookPayloadContactTag webhookPayloadContactTag)

Contact tag added event

A tag was added to a contact by the API, a workflow `add_tag` node or a comment-automation click.  ### When it fires  Once per tag a write actually added. Re-adding a tag the contact already has fires nothing.  ### When it does not fire  Creating a contact with tags fires nothing. Only changes to an existing contact do. 

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
    public class OnContactTagAddedExample
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
            var webhookPayloadContactTag = new WebhookPayloadContactTag(); // WebhookPayloadContactTag | 

            try
            {
                // Contact tag added event
                apiInstance.OnContactTagAdded(webhookPayloadContactTag);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnContactTagAdded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnContactTagAddedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Contact tag added event
    apiInstance.OnContactTagAddedWithHttpInfo(webhookPayloadContactTag);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnContactTagAddedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadContactTag** | [**WebhookPayloadContactTag**](WebhookPayloadContactTag.md) |  |  |

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

<a id="oncontacttagremoved"></a>
# **OnContactTagRemoved**
> void OnContactTagRemoved (WebhookPayloadContactTag webhookPayloadContactTag)

Contact tag removed event

A tag was removed from a contact.  ### When it fires  Once per tag a write actually removed. 

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
    public class OnContactTagRemovedExample
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
            var webhookPayloadContactTag = new WebhookPayloadContactTag(); // WebhookPayloadContactTag | 

            try
            {
                // Contact tag removed event
                apiInstance.OnContactTagRemoved(webhookPayloadContactTag);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnContactTagRemoved: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnContactTagRemovedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Contact tag removed event
    apiInstance.OnContactTagRemovedWithHttpInfo(webhookPayloadContactTag);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnContactTagRemovedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadContactTag** | [**WebhookPayloadContactTag**](WebhookPayloadContactTag.md) |  |  |

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

<a id="oncontactupdated"></a>
# **OnContactUpdated**
> void OnContactUpdated (WebhookPayloadContact webhookPayloadContact)

Contact updated

A contact sync added or changed a contact; `contact.id` is the Zernio contact id.  ### When it fires  It fires from the daily sync of a Google Contacts or Outlook account, so up to a day after the change. It also fires when a WhatsApp coexistence address book adds or renames a contact. 

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
    public class OnContactUpdatedExample
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
            var webhookPayloadContact = new WebhookPayloadContact(); // WebhookPayloadContact | 

            try
            {
                // Contact updated
                apiInstance.OnContactUpdated(webhookPayloadContact);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnContactUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnContactUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Contact updated
    apiInstance.OnContactUpdatedWithHttpInfo(webhookPayloadContact);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnContactUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadContact** | [**WebhookPayloadContact**](WebhookPayloadContact.md) |  |  |

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

<a id="onconversationcontrolchanged"></a>
# **OnConversationControlChanged**
> void OnConversationControlChanged (WebhookPayloadConversationControlChanged webhookPayloadConversationControlChanged)

Conversation control changed event

Control of a conversation moved under Meta's handover protocol (`messaging_handovers`).  ### Owner values  `control.owner` is `ai_agent` (Meta Business Agent, WhatsApp), `app` (you) or `other` (a WhatsApp partner app, or a receiver such as Page Inbox on Messenger and Instagram).  ### Control fields  `control.previousOwner` is `null` when no handover touched the thread. `control.ownerAppId` is the new owner's Meta app id when named (Page Inbox is `263902037430900`). `control.metadata` is the transferring app's note, verbatim.  ### WhatsApp  Meta Business Agent took the conversation, handed it to you, or another partner app took it. While `ai_agent` owns it, its replies arrive on `message.sent` with `source: \"meta_business_agent\"`.  ### Taking control on WhatsApp  Sending any message through the inbox takes control back. To hand it to the agent without sending, call `POST /v1/inbox/conversations/{conversationId}/thread-control` with `action: \"release\"`.  ### Facebook and Instagram  Another app on the Page passed the thread to you, or took or received it. While you are not the owner, sends answer `409` `not_thread_owner`.  ### Taking control on Facebook and Instagram  Call `POST /v1/inbox/conversations/{conversationId}/thread-control` with `action: \"take\"`, or `\"request\"` to ask the owner to pass it. Both answer 400 `platform_not_supported` on Instagram Login connections.  ### When it does not fire  A repeat report of the same owner fires nothing. A `request` changes nothing until the owner passes the thread.  ### Standby messages  While another app owns the conversation, inbound messages arrive on `message.received` with `metadata.standby: true`. 

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
    public class OnConversationControlChangedExample
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
            var webhookPayloadConversationControlChanged = new WebhookPayloadConversationControlChanged(); // WebhookPayloadConversationControlChanged | 

            try
            {
                // Conversation control changed event
                apiInstance.OnConversationControlChanged(webhookPayloadConversationControlChanged);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnConversationControlChanged: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnConversationControlChangedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Conversation control changed event
    apiInstance.OnConversationControlChangedWithHttpInfo(webhookPayloadConversationControlChanged);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnConversationControlChangedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadConversationControlChanged** | [**WebhookPayloadConversationControlChanged**](WebhookPayloadConversationControlChanged.md) |  |  |

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

A new conversation began between a connected account and a contact, in either direction, on any DM platform.  ### When it fires  Once per conversation, the first time it appears. Covers Instagram, Messenger, WhatsApp, Telegram, X, Reddit, Bluesky, TikTok, SMS, RCS, iMessage, Slack and email.  ### When it does not fire  DM history replayed when an Instagram or Facebook account connects never fires it. 

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

<a id="oncreatorcampaignbudgetexhausted"></a>
# **OnCreatorCampaignBudgetExhausted**
> void OnCreatorCampaignBudgetExhausted (WebhookPayloadCreatorCampaign webhookPayloadCreatorCampaign)

Creator campaign budget exhausted event

A campaign's earnings reached its budget.  ### When it fires  Nothing more accrues until budget is freed. It fires once per campaign. 

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
    public class OnCreatorCampaignBudgetExhaustedExample
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
            var webhookPayloadCreatorCampaign = new WebhookPayloadCreatorCampaign(); // WebhookPayloadCreatorCampaign | 

            try
            {
                // Creator campaign budget exhausted event
                apiInstance.OnCreatorCampaignBudgetExhausted(webhookPayloadCreatorCampaign);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCreatorCampaignBudgetExhausted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCreatorCampaignBudgetExhaustedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creator campaign budget exhausted event
    apiInstance.OnCreatorCampaignBudgetExhaustedWithHttpInfo(webhookPayloadCreatorCampaign);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCreatorCampaignBudgetExhaustedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCreatorCampaign** | [**WebhookPayloadCreatorCampaign**](WebhookPayloadCreatorCampaign.md) |  |  |

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

<a id="oncreatorcampaignclosed"></a>
# **OnCreatorCampaignClosed**
> void OnCreatorCampaignClosed (WebhookPayloadCreatorCampaign webhookPayloadCreatorCampaign)

Creator campaign closed event

A campaign closed, either because you closed it or because `endsAt` passed.  ### When it fires  After `endsAt`, the campaign closes once every tracking window had its final read. A pool campaign is split among participants at this moment. 

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
    public class OnCreatorCampaignClosedExample
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
            var webhookPayloadCreatorCampaign = new WebhookPayloadCreatorCampaign(); // WebhookPayloadCreatorCampaign | 

            try
            {
                // Creator campaign closed event
                apiInstance.OnCreatorCampaignClosed(webhookPayloadCreatorCampaign);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnCreatorCampaignClosed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnCreatorCampaignClosedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creator campaign closed event
    apiInstance.OnCreatorCampaignClosedWithHttpInfo(webhookPayloadCreatorCampaign);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnCreatorCampaignClosedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadCreatorCampaign** | [**WebhookPayloadCreatorCampaign**](WebhookPayloadCreatorCampaign.md) |  |  |

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

<a id="onemaillinkclicked"></a>
# **OnEmailLinkClicked**
> void OnEmailLinkClicked (WebhookPayloadEmailLinkClicked webhookPayloadEmailLinkClicked)

Email link clicked

A recipient followed a link of a message sent with `trackLinks: true`. Every http(s) link in the html was rewritten to a Zernio redirect that records the click and sends the reader on to `click.url`.  Security scanners in corporate mail gateways sometimes follow links on delivery, which reports as a click. 

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
    public class OnEmailLinkClickedExample
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
            var webhookPayloadEmailLinkClicked = new WebhookPayloadEmailLinkClicked(); // WebhookPayloadEmailLinkClicked | 

            try
            {
                // Email link clicked
                apiInstance.OnEmailLinkClicked(webhookPayloadEmailLinkClicked);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnEmailLinkClicked: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnEmailLinkClickedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Email link clicked
    apiInstance.OnEmailLinkClickedWithHttpInfo(webhookPayloadEmailLinkClicked);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnEmailLinkClickedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadEmailLinkClicked** | [**WebhookPayloadEmailLinkClicked**](WebhookPayloadEmailLinkClicked.md) |  |  |

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

<a id="onemailopened"></a>
# **OnEmailOpened**
> void OnEmailOpened (WebhookPayloadEmailOpened webhookPayloadEmailOpened)

Email opened

A mail client loaded the open pixel of a message sent with `trackOpens: true`.  Opens are a signal, not proof of reading:  - Gmail and Apple Mail fetch images through their own proxies, some as soon as the mail arrives. - Clients that block images never report an open. - The sender viewing the message in their own Sent folder counts too.  Repeat fetches within 10 seconds raise `count` without firing again. 

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
    public class OnEmailOpenedExample
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
            var webhookPayloadEmailOpened = new WebhookPayloadEmailOpened(); // WebhookPayloadEmailOpened | 

            try
            {
                // Email opened
                apiInstance.OnEmailOpened(webhookPayloadEmailOpened);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnEmailOpened: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnEmailOpenedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Email opened
    apiInstance.OnEmailOpenedWithHttpInfo(webhookPayloadEmailOpened);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnEmailOpenedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadEmailOpened** | [**WebhookPayloadEmailOpened**](WebhookPayloadEmailOpened.md) |  |  |

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

<a id="onemailsendfailed"></a>
# **OnEmailSendFailed**
> void OnEmailSendFailed (WebhookPayloadEmailSendFailed webhookPayloadEmailSendFailed)

Scheduled email failed

A send scheduled with `scheduledFor` could not leave at its time. Nothing reached the recipients. `error` says why, for example the mailbox was disconnected, the daily send cap was reached or the provider refused the mail. The send stays listed with `status: failed`; schedule it again to retry. 

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
    public class OnEmailSendFailedExample
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
            var webhookPayloadEmailSendFailed = new WebhookPayloadEmailSendFailed(); // WebhookPayloadEmailSendFailed | 

            try
            {
                // Scheduled email failed
                apiInstance.OnEmailSendFailed(webhookPayloadEmailSendFailed);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnEmailSendFailed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnEmailSendFailedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Scheduled email failed
    apiInstance.OnEmailSendFailedWithHttpInfo(webhookPayloadEmailSendFailed);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnEmailSendFailedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadEmailSendFailed** | [**WebhookPayloadEmailSendFailed**](WebhookPayloadEmailSendFailed.md) |  |  |

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

<a id="onemailthreadreplied"></a>
# **OnEmailThreadReplied**
> void OnEmailThreadReplied (WebhookPayloadEmailThreadReplied webhookPayloadEmailThreadReplied)

Email thread replied

Mail from someone other than the mailbox arrived in the thread of a message sent with `trackReplies: true`. Works on text and html sends. Auto-replies and bounce reports in the thread count as replies.  The reply also arrives as `message.received` with its full content. 

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
    public class OnEmailThreadRepliedExample
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
            var webhookPayloadEmailThreadReplied = new WebhookPayloadEmailThreadReplied(); // WebhookPayloadEmailThreadReplied | 

            try
            {
                // Email thread replied
                apiInstance.OnEmailThreadReplied(webhookPayloadEmailThreadReplied);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnEmailThreadReplied: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnEmailThreadRepliedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Email thread replied
    apiInstance.OnEmailThreadRepliedWithHttpInfo(webhookPayloadEmailThreadReplied);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnEmailThreadRepliedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadEmailThreadReplied** | [**WebhookPayloadEmailThreadReplied**](WebhookPayloadEmailThreadReplied.md) |  |  |

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

<a id="onfilecreated"></a>
# **OnFileCreated**
> void OnFileCreated (WebhookPayloadFile webhookPayloadFile)

File created

A file the account can reach was created in Google Drive or OneDrive.  ### Platform notes  A folder counts as a file. The event is pushed seconds after the change. 

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
    public class OnFileCreatedExample
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
            var webhookPayloadFile = new WebhookPayloadFile(); // WebhookPayloadFile | 

            try
            {
                // File created
                apiInstance.OnFileCreated(webhookPayloadFile);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnFileCreated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnFileCreatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // File created
    apiInstance.OnFileCreatedWithHttpInfo(webhookPayloadFile);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnFileCreatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadFile** | [**WebhookPayloadFile**](WebhookPayloadFile.md) |  |  |

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

<a id="onfiledeleted"></a>
# **OnFileDeleted**
> void OnFileDeleted (WebhookPayloadFile webhookPayloadFile)

File deleted

A file the account could reach was deleted or moved to the trash. 

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
    public class OnFileDeletedExample
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
            var webhookPayloadFile = new WebhookPayloadFile(); // WebhookPayloadFile | 

            try
            {
                // File deleted
                apiInstance.OnFileDeleted(webhookPayloadFile);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnFileDeleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnFileDeletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // File deleted
    apiInstance.OnFileDeletedWithHttpInfo(webhookPayloadFile);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnFileDeletedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadFile** | [**WebhookPayloadFile**](WebhookPayloadFile.md) |  |  |

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

<a id="onfilepicked"></a>
# **OnFilePicked**
> void OnFilePicked (WebhookPayloadFilePicked webhookPayloadFilePicked)

Files picked

The user picked files in a picker session; `picker.files` lists each one's `id`, `name`, `mimeType` and `kind`.  ### When it fires  It fires when the user finishes a hosted picker session (`POST /v1/files/picker-sessions`) and picks at least one file. Not sent on cancel. The files are readable from then on. 

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
    public class OnFilePickedExample
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
            var webhookPayloadFilePicked = new WebhookPayloadFilePicked(); // WebhookPayloadFilePicked | 

            try
            {
                // Files picked
                apiInstance.OnFilePicked(webhookPayloadFilePicked);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnFilePicked: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnFilePickedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Files picked
    apiInstance.OnFilePickedWithHttpInfo(webhookPayloadFilePicked);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnFilePickedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadFilePicked** | [**WebhookPayloadFilePicked**](WebhookPayloadFilePicked.md) |  |  |

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

<a id="onfileupdated"></a>
# **OnFileUpdated**
> void OnFileUpdated (WebhookPayloadFile webhookPayloadFile)

File updated

A file the account can reach was changed, renamed or moved. 

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
    public class OnFileUpdatedExample
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
            var webhookPayloadFile = new WebhookPayloadFile(); // WebhookPayloadFile | 

            try
            {
                // File updated
                apiInstance.OnFileUpdated(webhookPayloadFile);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnFileUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnFileUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // File updated
    apiInstance.OnFileUpdatedWithHttpInfo(webhookPayloadFile);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnFileUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadFile** | [**WebhookPayloadFile**](WebhookPayloadFile.md) |  |  |

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

A new lead was submitted against a Meta Lead Gen (Instant) form or a TikTok Instant Form (both pushed by the network), or a Google Ads or LinkedIn lead form (read every 15 minutes). `lead.platform` names the network.  Leads older than 7 days when Zernio first reads them are stored without this event.  ### Payload notes  `lead.fields` maps question key to answer; multiple-choice values are the option key (for example `k1`), not the display label.  ### Provenance  `lead.formId`, `lead.adId` and `lead.campaignId` give provenance. `lead.adId` is null for organic or test leads.  ### Consents  `lead.consents` lists the answer to every custom disclaimer checkbox, for example `{ \"checkboxKey\": \"call_consent\", \"isChecked\": true }`. Route call and SMS consent into your CRM from it. Empty when the form has no checkboxes.  ### Checkbox keys  When no key was set on the checkbox, Meta derives `checkboxKey` from its text, so match on the full key. `GET /v1/ads/leads` and `GET /v1/ads/lead-forms/{formId}/leads` return the same array.  ### Deduplication  Deduplicate on `lead.leadgenId` (Meta's lead id) or the event `id`.  ### Routing  `account.profileId` names the Zernio profile of the Facebook account that received the lead, for multi-tenant routing. Always present, `null` only when no profile is on record.  ### Requires ads enabled  Needs ads enabled on the team. Zernio asks for `leads_retrieval` at Facebook consent only then; without it Meta refuses the Page's `leadgen` subscription. Accounts connected earlier need a reconnect.  ### Lost subscription  A Page can lose its `leadgen` subscription while other events keep arriving. `leadgen: false` (with a `warning`) on the Page's webhook subscription means leads are not reaching Zernio; re-subscribe the Page. 

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

<a id="onmentionreceived"></a>
# **OnMentionReceived**
> void OnMentionReceived (WebhookPayloadMention webhookPayloadMention)

Mention received event

A connected Instagram, Facebook or LinkedIn account was mentioned in a post, caption or comment.  ### When it fires  Once per mention, the first time Zernio sees it. Delivery is at most once: reconcile with `GET /v1/inbox/mentions`.  - Instagram and Facebook arrive in real time from the platform's webhook. - LinkedIn arrives from its webhook or from polling, so delivery can take minutes. A newly connected account can receive mentions from the last 48 hours once.  ### Payload notes  Carries the same fields as `GET /v1/inbox/mentions`. Fields a platform does not provide are null. A LinkedIn mention found by polling for a team that does not retain content has no author, and an Instagram mention has no content if the live read fails. 

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
    public class OnMentionReceivedExample
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
            var webhookPayloadMention = new WebhookPayloadMention(); // WebhookPayloadMention | 

            try
            {
                // Mention received event
                apiInstance.OnMentionReceived(webhookPayloadMention);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnMentionReceived: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnMentionReceivedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mention received event
    apiInstance.OnMentionReceivedWithHttpInfo(webhookPayloadMention);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnMentionReceivedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadMention** | [**WebhookPayloadMention**](WebhookPayloadMention.md) |  |  |

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

A sender deleted (unsent) a message on Instagram or WhatsApp.  ### Platform notes  Instagram reports incoming unsends. WhatsApp reports both directions, including business deletions through the Cloud API or a Coexistence app. `message.direction` tells them apart.  ### Payload notes  The payload keeps the pre-delete `text` and `attachments` for moderation, compliance or archival. The Zernio dashboard does not show this content. 

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

An outgoing message was delivered to the recipient on WhatsApp, Facebook Messenger, SMS, RCS or iMessage.  ### Platform notes  On WhatsApp, `pricing` and `billingConversation` carry Meta's billing context for the message. 

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

A sender edited a previously sent message on Instagram, Facebook Messenger, Telegram or WhatsApp.  ### Payload notes  `editHistory` holds every prior version, oldest first. `message.text` is the latest version. 

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

An outgoing message failed to deliver on WhatsApp, SMS, RCS or iMessage.  ### Payload notes  `error` carries `code`, `title` and `message` from the platform, for example `131026` for an unreachable WhatsApp recipient. On SMS it carries the carrier's error code. 

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

<a id="onmessageplayed"></a>
# **OnMessagePlayed**
> void OnMessagePlayed (WebhookPayloadMessageDeliveryStatus webhookPayloadMessageDeliveryStatus)

Message played event

A WhatsApp recipient played a voice message you sent, reported the first time they play it. 

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
    public class OnMessagePlayedExample
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
                // Message played event
                apiInstance.OnMessagePlayed(webhookPayloadMessageDeliveryStatus);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnMessagePlayed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnMessagePlayedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Message played event
    apiInstance.OnMessagePlayedWithHttpInfo(webhookPayloadMessageDeliveryStatus);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnMessagePlayedWithHttpInfo: " + e.Message);
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

An outgoing message was read by the recipient on WhatsApp, Facebook Messenger, Instagram or RCS. 

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

A new message arrived in the inbox; `message.text`, `message.attachments[]` and `message.sender` describe it.  ### Standby  While another app owns the conversation it carries `metadata.standby: true`. Zernio runs no workflow or keyword automation on it. A bot must skip standby messages, or on WhatsApp it takes the conversation from the agent.  ### Interactive replies  Button and list taps, flow responses and orders arrive under `metadata` (`interactiveType`, `interactiveId`, `flowResponseData`, `order`). Only a referral that arrives without a message becomes `referral.received`.  ### Platform notes  New email from Google and Microsoft mailboxes arrives as this event. 

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

A message was sent through the API, the dashboard, or the WhatsApp Business app on Coexistence numbers.  ### Sender  `message.sentVia` is one of `human`, `api`, `broadcast`, `sequence`, `workflow`, `comment_automation` or `bulk-api`. It is `null` for sends from the platform's own app and for older messages; treat `null` as unknown, never as human.  ### Attribution keys  `automationId`, `workflowId`, `executionId`, `broadcastId` and `sequenceId` are always present. Each is `null` unless that kind of sender produced the message.  ### Quote replies  A quote-reply sent through the API carries `metadata.quotedMessageId`. One sent from the WhatsApp Business or Instagram app does not.  ### Platform notes  On Instagram and Facebook the attribution can be missing when Meta's echo of a send reaches Zernio before the send is recorded. On WhatsApp, Meta Business Agent replies carry `source: \"meta_business_agent\"`. 

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

<a id="onphonenumberstockavailable"></a>
# **OnPhoneNumberStockAvailable**
> void OnPhoneNumberStockAvailable (WebhookPayloadPhoneNumberStockAvailable webhookPayloadPhoneNumberStockAvailable)

Phone-number stock available event

A country you watch has deliverable phone numbers again; fires once per watch.  ### When it fires  Fired by the 6-hourly stock sweep, before you own a number in that country. The watch (`POST /v1/phone-numbers/stock-watches`) is then consumed.  ### Payload notes  `stock.country` is the watched country. `stock.types[]` lists each number type in stock with its `availableCount` at sweep time. Numbers are first come, first served; buy with `POST /v1/phone-numbers/purchase`. 

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
    public class OnPhoneNumberStockAvailableExample
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
            var webhookPayloadPhoneNumberStockAvailable = new WebhookPayloadPhoneNumberStockAvailable(); // WebhookPayloadPhoneNumberStockAvailable | 

            try
            {
                // Phone-number stock available event
                apiInstance.OnPhoneNumberStockAvailable(webhookPayloadPhoneNumberStockAvailable);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPhoneNumberStockAvailable: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPhoneNumberStockAvailableWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Phone-number stock available event
    apiInstance.OnPhoneNumberStockAvailableWithHttpInfo(webhookPayloadPhoneNumberStockAvailable);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPhoneNumberStockAvailableWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadPhoneNumberStockAvailable** | [**WebhookPayloadPhoneNumberStockAvailable**](WebhookPayloadPhoneNumberStockAvailable.md) |  |  |

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

<a id="onpostauthenticitychanged"></a>
# **OnPostAuthenticityChanged**
> void OnPostAuthenticityChanged (WebhookPayloadPostAuthenticityChanged webhookPayloadPostAuthenticityChanged)

Post authenticity changed event

A tracked post's authenticity score crossed 40, in either direction.  ### When it fires  Only while the tracking window is open. A post's first score never fires it.  ### Payload notes  Carries `score`, `previousScore`, `confidence` and `reasons`. 

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
    public class OnPostAuthenticityChangedExample
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
            var webhookPayloadPostAuthenticityChanged = new WebhookPayloadPostAuthenticityChanged(); // WebhookPayloadPostAuthenticityChanged | 

            try
            {
                // Post authenticity changed event
                apiInstance.OnPostAuthenticityChanged(webhookPayloadPostAuthenticityChanged);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostAuthenticityChanged: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostAuthenticityChangedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Post authenticity changed event
    apiInstance.OnPostAuthenticityChangedWithHttpInfo(webhookPayloadPostAuthenticityChanged);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostAuthenticityChangedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadPostAuthenticityChanged** | [**WebhookPayloadPostAuthenticityChanged**](WebhookPayloadPostAuthenticityChanged.md) |  |  |

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

A scheduled post was cancelled because its account was disconnected, and nothing published.  ### When it fires  A multi-platform post fires it only once every platform entry is cancelled. If a platform already published, the rollup is `post.partial` instead.  ### When it does not fire  `DELETE /v1/posts/{postId}` removes the post without sending this event. 

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

A post authored natively on the platform, outside Zernio, was detected for the first time.  ### When it fires  Detected by a background sync roughly hourly, not in real time. Example: a Google Business Profile post created in the Google interface.  ### Payload notes  `post.source` is always `\"external\"` and `post.id` is the platform-native post id.  ### First sync backfill  On a freshly connected account, every existing native post fires it once. Treat it as an idempotent upsert keyed on `post.id`. 

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

A tracked native post was removed from the platform.  ### Payload notes  `post.deletedAt` is the detection time.  ### Detection limits  Coverage is bounded to the most recent posts the platform listing returns, so very old deletions may go undetected.  ### When it does not fire  Detection diffs against posts a prior sync already indexed. An account with no indexed post never emits it. 

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

A tracked native post's text or media changed on the platform.  ### How edits are detected  Zernio compares text and media structure and, where available, the platform's own edit timestamp. A media-URL-only refresh (rotated CDN URLs) does not fire it. 

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

A post failed on every target platform.  ### When it fires  Once per publishing job, after every platform target ends. Exactly one of `post.published`, `post.partial` or `post.failed` fires.  A TikTok target TikTok is still processing (status `uploading`) holds it for up to 48 hours. Meanwhile `post.platform.published` and `post.platform.failed` report the other targets.  ### Payload notes  Each `platforms[]` entry carries `error`, `errorCategory` and `errorSource`, the same taxonomy as `platforms[]` on Get post. Branch on `errorCategory`, not on the message text. 

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

A post published on some platforms and failed on others.  ### When it fires  Once per publishing job, after every platform target ends. Exactly one of `post.published`, `post.partial` or `post.failed` fires.  A TikTok target TikTok is still processing (status `uploading`) holds it for up to 48 hours. Meanwhile `post.platform.published` and `post.platform.failed` report the other targets.  It can follow a `post.failed` for the same post when TikTok later reports a failed TikTok target as published.  ### Payload notes  Read `platforms[].status` to tell them apart. Failed entries carry `error`, `errorCategory` and `errorSource`. 

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

<a id="onpostplatformdeleted"></a>
# **OnPostPlatformDeleted**
> void OnPostPlatformDeleted (WebhookPayloadPostPlatform webhookPayloadPostPlatform)

Post platform deleted event

A published platform target was deleted on the platform.  ### When it fires  Detected by a background sync roughly hourly, once per platform target. Platforms push no deletion notice, so it can trail the rollup by days.  ### Payload notes  `platform.status` is `deleted`. `platform.deletedAt` is the detection time, not the moment of deletion.  ### Detection limits  Detection is listing-based: coverage is bounded to the posts the listing returns, and rare false positives happen. The event is not retracted when the post reappears. Re-check before deleting.  ### When it does not fire  Detection diffs against posts a prior sync already indexed. An account with no indexed post never emits it. 

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
    public class OnPostPlatformDeletedExample
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
                // Post platform deleted event
                apiInstance.OnPostPlatformDeleted(webhookPayloadPostPlatform);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostPlatformDeleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostPlatformDeletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Post platform deleted event
    apiInstance.OnPostPlatformDeletedWithHttpInfo(webhookPayloadPostPlatform);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostPlatformDeletedWithHttpInfo: " + e.Message);
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

<a id="onpostplatformfailed"></a>
# **OnPostPlatformFailed**
> void OnPostPlatformFailed (WebhookPayloadPostPlatform webhookPayloadPostPlatform)

Post platform failed event

One platform target failed permanently.  ### When it fires  Only on permanent failure; retryable errors stay silent. The rollup (`post.failed` or `post.partial`) fires separately once every platform ends.  ### After a publish  It can fire for a target that already emitted `post.platform.published`, if background reconciliation finds the publish never completed.  ### Payload notes  `platform.error` carries the platform's message. `platform.errorCategory` and `platform.errorSource` classify it, so a reconnect (`auth_expired`) separates from a content fix (`user_content`). 

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

One platform target finished publishing, without waiting for the other targets.  ### When it fires  Once per platform target, as soon as it finishes. A cross-post to 2 accounts on the same platform produces 2 events. Use `post.published` for the post-level rollup.  ### Payload notes  `platform` carries the platform post id and URL. `account` identifies the connected account.  ### TikTok targets still processing  TikTok can keep processing a post for up to 48 hours (entry status `uploading`). That target fires when TikTok finishes. The other targets fire as they finish, and the post rollup waits for TikTok.  ### Later reconciliation  If a target later fails background reconciliation, `post.platform.failed` fires for the same target afterward.  A failed TikTok target that TikTok later reports as published fires `post.platform.published` afterward, and the rollup fires again. 

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

Every platform target of a post published.  ### When it fires  Once per publishing job, after every platform target ends. Exactly one of `post.published`, `post.partial` or `post.failed` fires.  A TikTok target TikTok is still processing (status `uploading`) holds it for up to 48 hours. Meanwhile `post.platform.published` and `post.platform.failed` report the other targets.  It can follow a `post.partial` or `post.failed` for the same post when TikTok later reports a failed TikTok target as published.  ### Payload notes  Each `platforms[]` entry carries the `platformPostId` and `publishedUrl`. 

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

A recycling schedule cloned a published post for republishing.  ### Payload notes  `post.id` is the new clone's id. The clone emits its own `post.scheduled`. 

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

A post entered the scheduled state.  ### When it fires  Created with a schedule (with `publishNow`, accepted and queued), promoted from draft, added to a queue, retried after failing, or created as a recycled clone.  ### Approval and repeats  A post saved with `requiresApproval: true` fires it on approval, not at creation. One post can emit it more than once.  ### When it does not fire  Editing or moving an already-scheduled post to another time does not fire it. 

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

A published TikTok post's public URL became available.  ### When it fires  TikTok exposes the video id asynchronously, often minutes after upload, so `post.published` can carry an empty `publishedUrl`. Fires at most once per platform target. For a draft, it fires when the creator posts the draft publicly from the TikTok app.  ### Payload notes  Delivers `platform.publishedUrl` and the resolved `platform.platformPostId`. Same shape as `post.platform.published`.  ### When it does not fire  Private posts, which have no public URL, and drafts the creator never posts. 

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

<a id="onposttrackingcompleted"></a>
# **OnPostTrackingCompleted**
> void OnPostTrackingCompleted (WebhookPayloadPostTrackingCompleted webhookPayloadPostTrackingCompleted)

Post tracking completed event

A post's tracking window ended and its final analytics read finished.  ### When it fires  Once per window. A cancelled window never fires it.  ### Payload notes  `final` holds the closing metrics, or is null when no sample could be read. When the post was deleted, it is the last sample held, if any.  ### Completion reasons  `window.completionReason` is `final_read` (the read succeeded), `unreachable` (the sync failed or no sample exists) or `post_deleted` (the post is gone). 

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
    public class OnPostTrackingCompletedExample
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
            var webhookPayloadPostTrackingCompleted = new WebhookPayloadPostTrackingCompleted(); // WebhookPayloadPostTrackingCompleted | 

            try
            {
                // Post tracking completed event
                apiInstance.OnPostTrackingCompleted(webhookPayloadPostTrackingCompleted);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnPostTrackingCompleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnPostTrackingCompletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Post tracking completed event
    apiInstance.OnPostTrackingCompletedWithHttpInfo(webhookPayloadPostTrackingCompleted);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnPostTrackingCompletedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadPostTrackingCompleted** | [**WebhookPayloadPostTrackingCompleted**](WebhookPayloadPostTrackingCompleted.md) |  |  |

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

<a id="onrcsagentstatusupdated"></a>
# **OnRcsAgentStatusUpdated**
> void OnRcsAgentStatusUpdated (OnRcsAgentStatusUpdatedRequest onRcsAgentStatusUpdatedRequest)

RCS agent status updated event

An RCS agent moved into a new customer-visible status; `status` is the new one.  ### Statuses  `changes_requested` (note in `reason`), `brand_vetting`, `agent_review`, `testing`, `launch_review`, `launching`, `live`, `rejected` (`reason` says why), `deactivated`. In `testing`, add test phones, then file the launch; a `reason` means it bounced.  ### When it fires  Fires once per move into a status. `requested` sends nothing. Overlapping status checks never send the same status twice in a row.  ### Payload notes  `agent.profileId` is the owning profile. `agent.accountId` is `null` when the agent has no linked account. 

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
    public class OnRcsAgentStatusUpdatedExample
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
            var onRcsAgentStatusUpdatedRequest = new OnRcsAgentStatusUpdatedRequest(); // OnRcsAgentStatusUpdatedRequest | 

            try
            {
                // RCS agent status updated event
                apiInstance.OnRcsAgentStatusUpdated(onRcsAgentStatusUpdatedRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnRcsAgentStatusUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnRcsAgentStatusUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // RCS agent status updated event
    apiInstance.OnRcsAgentStatusUpdatedWithHttpInfo(onRcsAgentStatusUpdatedRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnRcsAgentStatusUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onRcsAgentStatusUpdatedRequest** | [**OnRcsAgentStatusUpdatedRequest**](OnRcsAgentStatusUpdatedRequest.md) |  |  |

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

A participant added or removed an emoji reaction on a message on Instagram, Facebook, WhatsApp, Telegram, Slack or TikTok.  ### Payload notes  Sent as its own event, never as `message.received`. `reaction.action` is `added` or `removed`. `reaction.platformMessageId` is always present; `reaction.messageId` is the Zernio id when resolvable.  ### Removals  On WhatsApp, Instagram and Facebook removals, `reaction.emoji` is an empty string because the platform does not say which emoji went away. Match on `platformMessageId` to clear a mirrored reaction.  ### TikTok  A like or emoji reaction on a DM arrives only as this event, never as an empty `message.received`. `platformMessageId` is the TikTok id of the liked message. AI emoji reactions can have an empty `emoji`.  ### Telegram  The bot must be an administrator in the chat. Telegram does not send reactions in private chats to bots.  ### Accounts connected before August 2026  Instagram and Facebook accounts connected before August 2026 do not receive this event until their webhook subscription is refreshed. Reconnect them, or re-subscribe a Facebook Page without a reconnect. 

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

<a id="onreferralreceived"></a>
# **OnReferralReceived**
> void OnReferralReceived (WebhookPayloadReferral webhookPayloadReferral)

Referral received event

Someone opened an existing Instagram or Messenger thread through an ig.me or m.me `ref` link or returning ad click.  ### Payload notes  Meta's referral object is forwarded verbatim: `ref` and `source` for links, `ad_id` and `ads_context_data` for ad clicks.  ### When it does not fire  A referral that rides an inbound message arrives on `message.received` under `metadata.referral` instead. The two never fire for the same click.  ### Stored referral  The first referral captured on a conversation is also persisted on it (`metadata` on `GET /v1/inbox/conversations`). 

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
    public class OnReferralReceivedExample
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
            var webhookPayloadReferral = new WebhookPayloadReferral(); // WebhookPayloadReferral | 

            try
            {
                // Referral received event
                apiInstance.OnReferralReceived(webhookPayloadReferral);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnReferralReceived: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnReferralReceivedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Referral received event
    apiInstance.OnReferralReceivedWithHttpInfo(webhookPayloadReferral);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnReferralReceivedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadReferral** | [**WebhookPayloadReferral**](WebhookPayloadReferral.md) |  |  |

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

<a id="onreviewdeleted"></a>
# **OnReviewDeleted**
> void OnReviewDeleted (WebhookPayloadReviewDeleted webhookPayloadReviewDeleted)

Review deleted event

Google Business Profile stopped returning a review, for example after its spam filter removed it.  ### When it fires  Zernio detects it by polling, so it usually fires 6 to 12 hours after the review disappears. Only locations covered by a webhook subscribed to `review.deleted` or `review.restored` are checked.  ### Restores  If the review comes back, `review.restored` fires, so a hidden then restored review produces `review.deleted` then `review.restored`. A `review.updated` can arrive for a deleted review; the next check restores it.  ### Payload notes  `review.id` is the full review name, the same value `review.new` sent. It may arrive for a review id you never received `review.new` for, so ignore ids you do not know. 

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
    public class OnReviewDeletedExample
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
            var webhookPayloadReviewDeleted = new WebhookPayloadReviewDeleted(); // WebhookPayloadReviewDeleted | 

            try
            {
                // Review deleted event
                apiInstance.OnReviewDeleted(webhookPayloadReviewDeleted);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnReviewDeleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnReviewDeletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Review deleted event
    apiInstance.OnReviewDeletedWithHttpInfo(webhookPayloadReviewDeleted);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnReviewDeletedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadReviewDeleted** | [**WebhookPayloadReviewDeleted**](WebhookPayloadReviewDeleted.md) |  |  |

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

A new review was posted on a connected Google Business Profile account, in real time through Pub/Sub. 

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

<a id="onreviewrestored"></a>
# **OnReviewRestored**
> void OnReviewRestored (WebhookPayloadReviewRestored webhookPayloadReviewRestored)

Review restored event

Google returned a review previously reported by `review.deleted`; the payload has the same shape as `review.new`.  ### When it fires  It may reach a webhook that subscribed after the deletion, so ignore ids you do not know. 

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
    public class OnReviewRestoredExample
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
            var webhookPayloadReviewRestored = new WebhookPayloadReviewRestored(); // WebhookPayloadReviewRestored | 

            try
            {
                // Review restored event
                apiInstance.OnReviewRestored(webhookPayloadReviewRestored);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnReviewRestored: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnReviewRestoredWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Review restored event
    apiInstance.OnReviewRestoredWithHttpInfo(webhookPayloadReviewRestored);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnReviewRestoredWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadReviewRestored** | [**WebhookPayloadReviewRestored**](WebhookPayloadReviewRestored.md) |  |  |

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

A Google Business Profile review changed: the reviewer edited it, or its reply was added, edited or removed.  ### Reply through the API  A reply sent through the Zernio API fires the event immediately. The periodic check then reports it again with the full review payload, so expect a second delivery.  ### Replies written in Google  Google sends no notification for replies written in its interface. The periodic check detects them, usually within 6 hours for reviews updated in the last 30 days, about 7 days for older.  ### Checks  Only teams with a webhook subscribed to `review.updated` are checked. A removed reply, through the API or in Google, fires from the periodic check with `review.hasReply` set to `false`.  ### Payload notes  Same shape as `review.new`. When a reply is present, `review.hasReply` is `true` and `review.reply` is populated. 

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

<a id="onsequenceenrolled"></a>
# **OnSequenceEnrolled**
> void OnSequenceEnrolled (WebhookPayloadSequenceEnrollment webhookPayloadSequenceEnrollment)

Sequence enrolled event

A contact was enrolled in a sequence, through the API or a workflow `enroll_sequence` node. 

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
    public class OnSequenceEnrolledExample
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
            var webhookPayloadSequenceEnrollment = new WebhookPayloadSequenceEnrollment(); // WebhookPayloadSequenceEnrollment | 

            try
            {
                // Sequence enrolled event
                apiInstance.OnSequenceEnrolled(webhookPayloadSequenceEnrollment);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnSequenceEnrolled: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnSequenceEnrolledWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sequence enrolled event
    apiInstance.OnSequenceEnrolledWithHttpInfo(webhookPayloadSequenceEnrollment);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnSequenceEnrolledWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadSequenceEnrollment** | [**WebhookPayloadSequenceEnrollment**](WebhookPayloadSequenceEnrollment.md) |  |  |

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

<a id="onsequenceexited"></a>
# **OnSequenceExited**
> void OnSequenceExited (WebhookPayloadSequenceEnrollment webhookPayloadSequenceEnrollment)

Sequence exited event

A contact left a sequence; `exitReason` says why.  ### Exit reasons  - `completed`: the last step was sent. - `replied` - `manual`: unenrolled through the API. - `failed`: the step kept failing to send. - `unsubscribed` 

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
    public class OnSequenceExitedExample
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
            var webhookPayloadSequenceEnrollment = new WebhookPayloadSequenceEnrollment(); // WebhookPayloadSequenceEnrollment | 

            try
            {
                // Sequence exited event
                apiInstance.OnSequenceExited(webhookPayloadSequenceEnrollment);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnSequenceExited: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnSequenceExitedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sequence exited event
    apiInstance.OnSequenceExitedWithHttpInfo(webhookPayloadSequenceEnrollment);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnSequenceExitedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadSequenceEnrollment** | [**WebhookPayloadSequenceEnrollment**](WebhookPayloadSequenceEnrollment.md) |  |  |

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

<a id="onsmsregistrationactionrequired"></a>
# **OnSmsRegistrationActionRequired**
> void OnSmsRegistrationActionRequired (OnSmsRegistrationActionRequiredRequest onSmsRegistrationActionRequiredRequest)

SMS registration action required event

An SMS registration is waiting on its owner; `reason` says why.  ### Reasons  - `changes_requested`: answer `message` via `POST /v1/sms/registrations/{id}/respond`. - `otp_required`: submit the texted code via `POST /v1/sms/registrations/{id}/verify-otp`; no `message`. - `carrier_info_required`: expires after 7 days.  ### When it fires  Fires once per new request and once per OTP or carrier request, not on follow-up messages. A carrier rejection alone does not fire it. 

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
    public class OnSmsRegistrationActionRequiredExample
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
            var onSmsRegistrationActionRequiredRequest = new OnSmsRegistrationActionRequiredRequest(); // OnSmsRegistrationActionRequiredRequest | 

            try
            {
                // SMS registration action required event
                apiInstance.OnSmsRegistrationActionRequired(onSmsRegistrationActionRequiredRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnSmsRegistrationActionRequired: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnSmsRegistrationActionRequiredWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // SMS registration action required event
    apiInstance.OnSmsRegistrationActionRequiredWithHttpInfo(onSmsRegistrationActionRequiredRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnSmsRegistrationActionRequiredWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onSmsRegistrationActionRequiredRequest** | [**OnSmsRegistrationActionRequiredRequest**](OnSmsRegistrationActionRequiredRequest.md) |  |  |

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

<a id="onsmsregistrationstatusupdated"></a>
# **OnSmsRegistrationStatusUpdated**
> void OnSmsRegistrationStatusUpdated (OnSmsRegistrationStatusUpdatedRequest onSmsRegistrationStatusUpdatedRequest)

SMS registration status updated event

An SMS registration changed status; `status` is the new one.  ### Statuses  - `changes_requested`: answers needed. - `requested`: submitted, resubmitted, or your answers are back in review. - `pending`: with the carriers. - `approved`: live, attach numbers. - `rejected`: `reason` is the carriers' words. - `deactivated`  ### Rejections  A carrier rejection needs nothing from you. Zernio handles the fix and resends it, so the status returns to `pending`. 

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
    public class OnSmsRegistrationStatusUpdatedExample
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
            var onSmsRegistrationStatusUpdatedRequest = new OnSmsRegistrationStatusUpdatedRequest(); // OnSmsRegistrationStatusUpdatedRequest | 

            try
            {
                // SMS registration status updated event
                apiInstance.OnSmsRegistrationStatusUpdated(onSmsRegistrationStatusUpdatedRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnSmsRegistrationStatusUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnSmsRegistrationStatusUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // SMS registration status updated event
    apiInstance.OnSmsRegistrationStatusUpdatedWithHttpInfo(onSmsRegistrationStatusUpdatedRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnSmsRegistrationStatusUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onSmsRegistrationStatusUpdatedRequest** | [**OnSmsRegistrationStatusUpdatedRequest**](OnSmsRegistrationStatusUpdatedRequest.md) |  |  |

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

<a id="onsupportruncompleted"></a>
# **OnSupportRunCompleted**
> void OnSupportRunCompleted (WebhookPayloadSupportRun webhookPayloadSupportRun)

Support Assistant finished event

A support run finished with an answer, or handed the question to a person.  ### Payload notes  `run.status` is `completed`, or `needs_human` when Ana handed the question to a person. `run.answer` holds the answer; `run.stopReason` says why it stopped (`answered` or `human_review`, among others). 

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
    public class OnSupportRunCompletedExample
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
            var webhookPayloadSupportRun = new WebhookPayloadSupportRun(); // WebhookPayloadSupportRun | 

            try
            {
                // Support Assistant finished event
                apiInstance.OnSupportRunCompleted(webhookPayloadSupportRun);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnSupportRunCompleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnSupportRunCompletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Support Assistant finished event
    apiInstance.OnSupportRunCompletedWithHttpInfo(webhookPayloadSupportRun);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnSupportRunCompletedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadSupportRun** | [**WebhookPayloadSupportRun**](WebhookPayloadSupportRun.md) |  |  |

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

<a id="onsupportrunfailed"></a>
# **OnSupportRunFailed**
> void OnSupportRunFailed (WebhookPayloadSupportRun webhookPayloadSupportRun)

Support Assistant failed event

A support run failed or expired, and is not billed.  ### Payload notes  `run.status` is `failed` and `run.answer` is `null`. `run.stopReason` is `expired` when the run never finished. `run.costUsd` is 0. 

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
    public class OnSupportRunFailedExample
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
            var webhookPayloadSupportRun = new WebhookPayloadSupportRun(); // WebhookPayloadSupportRun | 

            try
            {
                // Support Assistant failed event
                apiInstance.OnSupportRunFailed(webhookPayloadSupportRun);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnSupportRunFailed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnSupportRunFailedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Support Assistant failed event
    apiInstance.OnSupportRunFailedWithHttpInfo(webhookPayloadSupportRun);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnSupportRunFailedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadSupportRun** | [**WebhookPayloadSupportRun**](WebhookPayloadSupportRun.md) |  |  |

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

<a id="onverificationapproved"></a>
# **OnVerificationApproved**
> void OnVerificationApproved (OnVerificationApprovedRequest onVerificationApprovedRequest)

Verification approved event

The recipient submitted the right verification code.  ### Payload notes  Carries `verification.verificationId`, `verification.channel` (`sms`) and `verification.to`. 

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
    public class OnVerificationApprovedExample
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
            var onVerificationApprovedRequest = new OnVerificationApprovedRequest(); // OnVerificationApprovedRequest | 

            try
            {
                // Verification approved event
                apiInstance.OnVerificationApproved(onVerificationApprovedRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnVerificationApproved: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnVerificationApprovedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Verification approved event
    apiInstance.OnVerificationApprovedWithHttpInfo(onVerificationApprovedRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnVerificationApprovedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onVerificationApprovedRequest** | [**OnVerificationApprovedRequest**](OnVerificationApprovedRequest.md) |  |  |

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

<a id="onverificationfailed"></a>
# **OnVerificationFailed**
> void OnVerificationFailed (OnVerificationFailedRequest onVerificationFailedRequest)

Verification failed event

A verification ran out of attempts without a correct code.  ### Payload notes  `reason` is `max_attempts_reached`. Carries the same `verification` fields as `verification.approved`. 

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
    public class OnVerificationFailedExample
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
            var onVerificationFailedRequest = new OnVerificationFailedRequest(); // OnVerificationFailedRequest | 

            try
            {
                // Verification failed event
                apiInstance.OnVerificationFailed(onVerificationFailedRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnVerificationFailed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnVerificationFailedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Verification failed event
    apiInstance.OnVerificationFailedWithHttpInfo(onVerificationFailedRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnVerificationFailedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **onVerificationFailedRequest** | [**OnVerificationFailedRequest**](OnVerificationFailedRequest.md) |  |  |

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

Zernio sent a test event to an endpoint.  ### When it fires  Sent when you call Test webhook or press test in the dashboard, whatever events the endpoint subscribes to. Sent once, synchronously, and never retried. 

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

<a id="onwhatsappaccountalertreceived"></a>
# **OnWhatsAppAccountAlertReceived**
> void OnWhatsAppAccountAlertReceived (WebhookPayloadWhatsAppAccountAlertReceived webhookPayloadWhatsAppAccountAlertReceived)

WhatsApp account alert received

Meta sent an account alert for a connected WhatsApp Business Account.  ### Payload notes  Forwards Meta's `account_alerts` as is. `alert.severity` is `CRITICAL`, `WARNING` or `INFORMATIONAL`; `alert.type` is Meta's alert type; `alert.description` is the text.  ### Who receives it  An alert about one number goes to that number's account. A business-level alert goes to every connected number on the WABA. 

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
    public class OnWhatsAppAccountAlertReceivedExample
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
            var webhookPayloadWhatsAppAccountAlertReceived = new WebhookPayloadWhatsAppAccountAlertReceived(); // WebhookPayloadWhatsAppAccountAlertReceived | 

            try
            {
                // WhatsApp account alert received
                apiInstance.OnWhatsAppAccountAlertReceived(webhookPayloadWhatsAppAccountAlertReceived);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppAccountAlertReceived: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppAccountAlertReceivedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp account alert received
    apiInstance.OnWhatsAppAccountAlertReceivedWithHttpInfo(webhookPayloadWhatsAppAccountAlertReceived);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppAccountAlertReceivedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadWhatsAppAccountAlertReceived** | [**WebhookPayloadWhatsAppAccountAlertReceived**](WebhookPayloadWhatsAppAccountAlertReceived.md) |  |  |

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

<a id="onwhatsappaccountnamestatusupdated"></a>
# **OnWhatsAppAccountNameStatusUpdated**
> void OnWhatsAppAccountNameStatusUpdated (WebhookPayloadWhatsAppAccountNameStatusUpdated webhookPayloadWhatsAppAccountNameStatusUpdated)

WhatsApp display-name review outcome event

Meta finished reviewing a WhatsApp display-name change on a connected number.  ### When it fires  Fires only on a review outcome, forwarded from Meta's `phone_number_name_update` field. A name applied without review (`AVAILABLE_WITHOUT_REVIEW`) produces no event.  ### Payload notes  Branch on `name.status` (`APPROVED`, `DECLINED`, `PENDING_REVIEW`). Meta's `REJECTED` maps to `DECLINED` and `DEFERRED` to `PENDING_REVIEW`, because the review is still open. `name.requestedName` and `name.rejectionReason` are Meta's values or null.  ### Delivery  Delivery is at-least-once; dedupe on `(account.accountId, name.status, name.requestedName)`. 

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
    public class OnWhatsAppAccountNameStatusUpdatedExample
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
            var webhookPayloadWhatsAppAccountNameStatusUpdated = new WebhookPayloadWhatsAppAccountNameStatusUpdated(); // WebhookPayloadWhatsAppAccountNameStatusUpdated | 

            try
            {
                // WhatsApp display-name review outcome event
                apiInstance.OnWhatsAppAccountNameStatusUpdated(webhookPayloadWhatsAppAccountNameStatusUpdated);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppAccountNameStatusUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppAccountNameStatusUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp display-name review outcome event
    apiInstance.OnWhatsAppAccountNameStatusUpdatedWithHttpInfo(webhookPayloadWhatsAppAccountNameStatusUpdated);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppAccountNameStatusUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadWhatsAppAccountNameStatusUpdated** | [**WebhookPayloadWhatsAppAccountNameStatusUpdated**](WebhookPayloadWhatsAppAccountNameStatusUpdated.md) |  |  |

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

<a id="onwhatsappaccountqualityupdated"></a>
# **OnWhatsAppAccountQualityUpdated**
> void OnWhatsAppAccountQualityUpdated (WebhookPayloadWhatsAppAccountQualityUpdated webhookPayloadWhatsAppAccountQualityUpdated)

WhatsApp quality rating or messaging limit changed

A connected number's quality rating or messaging limit tier changed.  ### When it fires  Fires only when the rating or tier differs from the value Zernio held. A tier change Meta applies to the whole business portfolio fires once per connected number.  ### Payload notes  `quality.source` says which Meta signal reported it. Compare `quality.previousQualityRating` with `quality.qualityRating`, and the previous and current messaging limit tier. `quality.qualityRating` is Meta's live value (`GREEN`, `YELLOW`, `RED`).  ### Delivery  Delivery is at-least-once; dedupe on the event `id`. 

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
    public class OnWhatsAppAccountQualityUpdatedExample
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
            var webhookPayloadWhatsAppAccountQualityUpdated = new WebhookPayloadWhatsAppAccountQualityUpdated(); // WebhookPayloadWhatsAppAccountQualityUpdated | 

            try
            {
                // WhatsApp quality rating or messaging limit changed
                apiInstance.OnWhatsAppAccountQualityUpdated(webhookPayloadWhatsAppAccountQualityUpdated);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppAccountQualityUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppAccountQualityUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp quality rating or messaging limit changed
    apiInstance.OnWhatsAppAccountQualityUpdatedWithHttpInfo(webhookPayloadWhatsAppAccountQualityUpdated);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppAccountQualityUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadWhatsAppAccountQualityUpdated** | [**WebhookPayloadWhatsAppAccountQualityUpdated**](WebhookPayloadWhatsAppAccountQualityUpdated.md) |  |  |

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

<a id="onwhatsappaccountstatusupdated"></a>
# **OnWhatsAppAccountStatusUpdated**
> void OnWhatsAppAccountStatusUpdated (WebhookPayloadWhatsAppAccountStatusUpdated webhookPayloadWhatsAppAccountStatusUpdated)

WhatsApp Business Account restricted or reinstated

Meta restricted, disabled, deleted or reinstated a connected WhatsApp Business Account, or flagged a violation on it.  ### When it fires  Mirrors Meta's `account_update` events. They apply to the whole WhatsApp Business Account, so every connected number on it receives one event.  ### Payload notes  Branch on `status.status` (`restricted` or `active`) and `status.metaEvent`. `status.restrictions` lists what Meta restricted (for example `RESTRICTED_BIZ_INITIATED_MESSAGING`) and when each lifts. The same status is on the account as `platformStatus`. 

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
    public class OnWhatsAppAccountStatusUpdatedExample
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
            var webhookPayloadWhatsAppAccountStatusUpdated = new WebhookPayloadWhatsAppAccountStatusUpdated(); // WebhookPayloadWhatsAppAccountStatusUpdated | 

            try
            {
                // WhatsApp Business Account restricted or reinstated
                apiInstance.OnWhatsAppAccountStatusUpdated(webhookPayloadWhatsAppAccountStatusUpdated);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppAccountStatusUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppAccountStatusUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp Business Account restricted or reinstated
    apiInstance.OnWhatsAppAccountStatusUpdatedWithHttpInfo(webhookPayloadWhatsAppAccountStatusUpdated);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppAccountStatusUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadWhatsAppAccountStatusUpdated** | [**WebhookPayloadWhatsAppAccountStatusUpdated**](WebhookPayloadWhatsAppAccountStatusUpdated.md) |  |  |

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

Meta's automatic event identification detected a lead or purchase in a Click-to-WhatsApp conversation.  ### Payload notes  Branch on `eventName` (`LeadSubmitted` or `Purchase`). `Purchase` may carry the detected amount in `customData` (`currency`, `value`). It carries the `ctwaClid`.  ### Conversions API match key  Meta omits the clid on a minority of referrals, most often WhatsApp Status placements; this event can supply it. Zernio writes it onto the conversation, so `POST /v1/whatsapp/conversions` becomes usable for it.  ### Availability  Detection is not available for EU, UK and JP businesses. Elsewhere the owner opts in during Embedded Signup. An endpoint subscribed on a number whose owner did not opt in receives nothing. 

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

<a id="onwhatsappcontactidentitychanged"></a>
# **OnWhatsAppContactIdentityChanged**
> void OnWhatsAppContactIdentityChanged (WebhookPayloadWhatsAppContactIdentityChanged webhookPayloadWhatsAppContactIdentityChanged)

WhatsApp contact identity changed event

A WhatsApp user changed phone number or Meta regenerated their business-scoped user id (BSUID).  ### When it fires  Fires when Meta reports the user under a new phone number (`reason: \"user_changed_number\"`) or a new BSUID (`user_changed_user_id`, `user_identity_changed` or `user_id_update`).  ### Payload notes  `previous` and `current` carry the phone number, BSUID, parent BSUID and username. Use them to re-key records stored against the old value.  ### Already applied  Zernio has already moved the inbox conversation and the contact when the event arrives. `conversationId` and `contactId` point at them, or are null when there was none.  ### Delivery  Delivery is at-least-once; dedupe on the event `id`. 

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
    public class OnWhatsAppContactIdentityChangedExample
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
            var webhookPayloadWhatsAppContactIdentityChanged = new WebhookPayloadWhatsAppContactIdentityChanged(); // WebhookPayloadWhatsAppContactIdentityChanged | 

            try
            {
                // WhatsApp contact identity changed event
                apiInstance.OnWhatsAppContactIdentityChanged(webhookPayloadWhatsAppContactIdentityChanged);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppContactIdentityChanged: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppContactIdentityChangedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp contact identity changed event
    apiInstance.OnWhatsAppContactIdentityChangedWithHttpInfo(webhookPayloadWhatsAppContactIdentityChanged);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppContactIdentityChangedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadWhatsAppContactIdentityChanged** | [**WebhookPayloadWhatsAppContactIdentityChanged**](WebhookPayloadWhatsAppContactIdentityChanged.md) |  |  |

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

The regulator asked for more information on a placed number order; nothing was rejected.  ### When it fires  The order stays pending, and the number stays `pending_regulatory`, until you provide the information. The status does not change.  ### Payload notes  `reason` carries the regulator's request verbatim when available. `requirements` lists every requirement with the reviewer's current verdict; the `declined` ones are what to fix, keyed by `requirementId`. Verdicts describe the review at `reviewedAt`.  ### How to resolve  Provide the missing details from the dashboard's phone-numbers page, or re-submit the fields through the remediation endpoint. The review resumes automatically. 

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

A number you provisioned through Zernio finished setup and is ready to connect.  ### When it fires  Regulated (non-US) numbers can take 1 to 3 business days after the order is approved. In instant-provisioning countries this is the first event, with no review states before it. 

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

A regulated number order was declined in regulatory review and no number was activated.  ### Payload notes  `reason` carries the reviewer's rejection reason when available. You are never billed for a declined number.  ### Remediation  Resubmit corrected details and the number returns to `pending_regulatory`. It is the same number, with no new billing. 

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

An end customer completed a hosted KYC share link and the number entered regulatory review.  ### When it fires  Fires only for hosted share links (`POST /v1/phone-numbers/kyc/share`). When you submit KYC over the API, no event fires.  ### What follows  The number is `pending_regulatory` under your account. `whatsapp.number.activated` or `whatsapp.number.declined` follows once the provider rules on it. Update your own UI from this event instead of polling. 

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

A suspended number was reactivated, for example after the payment recovered, and is usable again. 

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

A number was released and is no longer usable.  ### Payload notes  Released by you, a billing cleanup or an admin. `reason` is a value such as `user_requested` or `cleanup_suspended`. This is the only terminal status. 

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

An active number was suspended, for example after a failed payment.  ### Payload notes  `reason` is a value such as `payment_failed` or `subscription_ended`. The number stops working until the issue is resolved, then `whatsapp.number.reactivated` follows.  ### When it does not recover  A suspension left unresolved ends in release. 

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

A regulated number requires the end user to complete an identity check.  ### Payload notes  `verificationUrl` is a one-time link to forward to the person whose ID is on file, for example for Australian mobile numbers. The order completes once they pass. The number stays `pending_regulatory`. 

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

<a id="onwhatsapptemplatecategoryupdated"></a>
# **OnWhatsAppTemplateCategoryUpdated**
> void OnWhatsAppTemplateCategoryUpdated (WebhookPayloadWhatsAppTemplateCategoryUpdated webhookPayloadWhatsAppTemplateCategoryUpdated)

WhatsApp template category updated event

Meta reclassified a WhatsApp template's category, first as a 24-hour advance notice and again when applied.  ### When it fires  Sent with `template.changeType: \"scheduled\"` for Meta's 24-hour advance notice, and again with `\"applied\"` when the change takes effect.  ### Payload notes  `template.category` is always the category right now. Meta clears a custom delivery window when it recategorises a template, so read `message_send_ttl_seconds` back after an `applied` change.  ### Platform notes  Forwarded from Meta's `template_category_update` field. The category decides Meta's per-delivery rate and the delivery window the template can carry. 

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
    public class OnWhatsAppTemplateCategoryUpdatedExample
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
            var webhookPayloadWhatsAppTemplateCategoryUpdated = new WebhookPayloadWhatsAppTemplateCategoryUpdated(); // WebhookPayloadWhatsAppTemplateCategoryUpdated | 

            try
            {
                // WhatsApp template category updated event
                apiInstance.OnWhatsAppTemplateCategoryUpdated(webhookPayloadWhatsAppTemplateCategoryUpdated);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppTemplateCategoryUpdated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWhatsAppTemplateCategoryUpdatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // WhatsApp template category updated event
    apiInstance.OnWhatsAppTemplateCategoryUpdatedWithHttpInfo(webhookPayloadWhatsAppTemplateCategoryUpdated);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWhatsAppTemplateCategoryUpdatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadWhatsAppTemplateCategoryUpdated** | [**WebhookPayloadWhatsAppTemplateCategoryUpdated**](WebhookPayloadWhatsAppTemplateCategoryUpdated.md) |  |  |

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

Meta finished reviewing or re-reviewing a WhatsApp Business template on a connected WABA.  ### Payload notes  Branch on `template.status` (`APPROVED`, `REJECTED`, `PENDING`, `PAUSED`, `DISABLED`, `IN_APPEAL`, `PENDING_DELETION`). `template.reason` is Meta's free-form reason or `\"NONE\"`.  ### Platform notes  Forwarded from Meta's `message_template_status_update` field. Meta includes neither the previous status nor the template's category. 

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

<a id="onworkflowruncompleted"></a>
# **OnWorkflowRunCompleted**
> void OnWorkflowRunCompleted (WebhookPayloadWorkflowRun webhookPayloadWorkflowRun)

Workflow run completed event

A workflow run ended, with `execution.status` `completed`, or `exited` when it ended on purpose before its last node.  ### Exits  An exit is a handoff, or a button that switched the contact to another workflow. 

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
    public class OnWorkflowRunCompletedExample
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
            var webhookPayloadWorkflowRun = new WebhookPayloadWorkflowRun(); // WebhookPayloadWorkflowRun | 

            try
            {
                // Workflow run completed event
                apiInstance.OnWorkflowRunCompleted(webhookPayloadWorkflowRun);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWorkflowRunCompleted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWorkflowRunCompletedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Workflow run completed event
    apiInstance.OnWorkflowRunCompletedWithHttpInfo(webhookPayloadWorkflowRun);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWorkflowRunCompletedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadWorkflowRun** | [**WebhookPayloadWorkflowRun**](WebhookPayloadWorkflowRun.md) |  |  |

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

<a id="onworkflowrunfailed"></a>
# **OnWorkflowRunFailed**
> void OnWorkflowRunFailed (WebhookPayloadWorkflowRun webhookPayloadWorkflowRun)

Workflow run failed event

A workflow run failed; `error` names the node that failed and why. 

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
    public class OnWorkflowRunFailedExample
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
            var webhookPayloadWorkflowRun = new WebhookPayloadWorkflowRun(); // WebhookPayloadWorkflowRun | 

            try
            {
                // Workflow run failed event
                apiInstance.OnWorkflowRunFailed(webhookPayloadWorkflowRun);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWorkflowRunFailed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWorkflowRunFailedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Workflow run failed event
    apiInstance.OnWorkflowRunFailedWithHttpInfo(webhookPayloadWorkflowRun);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWorkflowRunFailedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadWorkflowRun** | [**WebhookPayloadWorkflowRun**](WebhookPayloadWorkflowRun.md) |  |  |

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

<a id="onworkflowrunstarted"></a>
# **OnWorkflowRunStarted**
> void OnWorkflowRunStarted (WebhookPayloadWorkflowRun webhookPayloadWorkflowRun)

Workflow run started event

A workflow run started for a conversation; `trigger.type` is the trigger node's type.  ### Payload notes  `trigger.text` is the inbound message that started the run, when there was one. 

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
    public class OnWorkflowRunStartedExample
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
            var webhookPayloadWorkflowRun = new WebhookPayloadWorkflowRun(); // WebhookPayloadWorkflowRun | 

            try
            {
                // Workflow run started event
                apiInstance.OnWorkflowRunStarted(webhookPayloadWorkflowRun);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEventsApi.OnWorkflowRunStarted: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnWorkflowRunStartedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Workflow run started event
    apiInstance.OnWorkflowRunStartedWithHttpInfo(webhookPayloadWorkflowRun);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEventsApi.OnWorkflowRunStartedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPayloadWorkflowRun** | [**WebhookPayloadWorkflowRun**](WebhookPayloadWorkflowRun.md) |  |  |

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

