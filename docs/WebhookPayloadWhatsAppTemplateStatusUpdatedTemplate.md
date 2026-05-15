# Zernio.Model.WebhookPayloadWhatsAppTemplateStatusUpdatedTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TemplateId** | **string** | Meta&#39;s &#x60;message_template_id&#x60;, returned as a string. | 
**Name** | **string** | Meta&#39;s &#x60;message_template_name&#x60;. | 
**Language** | **string** | Meta&#39;s &#x60;message_template_language&#x60; (e.g. &#x60;en_US&#x60;). | 
**Status** | **string** | New status. Forwarded verbatim from Meta&#39;s &#x60;event&#x60; field. &#x60;PENDING_DELETION&#x60; is the 24h-grace state after a delete request before the template is actually removed.  | 
**Reason** | **string** | Meta&#39;s free-form reason for the transition. &#x60;\&quot;NONE\&quot;&#x60; on approval; an explanation string on rejection.  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

