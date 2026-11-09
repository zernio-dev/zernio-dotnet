# Zernio.Model.ReplyEmailMessageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**To** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | 
**Cc** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**Bcc** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**ReplyTo** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**FromName** | **string** |  | [optional] 
**Subject** | **string** | Optional on replies; the provider keeps the thread subject. | 
**Text** | **string** | Plain-text body. One of &#x60;text&#x60; or &#x60;html&#x60; is required. | [optional] 
**Html** | **string** |  | [optional] 
**Attachments** | [**List&lt;SendEmailRequestAttachmentsInner&gt;**](SendEmailRequestAttachmentsInner.md) | 25 MB in total; 3 MB per attachment on Microsoft. | [optional] 
**Headers** | **Dictionary&lt;string, string&gt;** | Custom &#x60;X-&#x60; headers only. &#x60;List-Unsubscribe&#x60; is dropped on Microsoft and reported in &#x60;metadata.droppedHeaders&#x60;. | [optional] 
**Metadata** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**ScheduledFor** | **DateTime** | Send later, between 1 minute and 30 days from now. The request answers 202 with the scheduled send; it leaves within a minute of this time through the same caps as an immediate send. List or cancel it under &#x60;/v1/email/messages/scheduled&#x60;. | [optional] 
**HoldAsDraft** | **bool** | Reserved; currently rejected. | [optional] 
**TrackOpens** | **bool** | Adds an open pixel to the html and fires &#x60;email.opened&#x60;. Needs &#x60;html&#x60;. | [optional] 
**TrackLinks** | **bool** | Rewrites every http(s) link in the html through a Zernio redirect and fires &#x60;email.link_clicked&#x60;. Needs &#x60;html&#x60;. | [optional] 
**TrackReplies** | **bool** | Fires &#x60;email.thread_replied&#x60; when someone else writes in this message&#39;s thread. Works with text or html. | [optional] 
**Mode** | **string** |  | [optional] [default to ModeEnum.Reply]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

