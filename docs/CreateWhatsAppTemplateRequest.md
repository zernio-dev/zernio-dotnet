# Zernio.Model.CreateWhatsAppTemplateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | WhatsApp account ID | 
**Name** | **string** | Template name (lowercase, letters/numbers/underscores, must start with a letter) | 
**Category** | **string** | Template category | 
**Language** | **string** | Template language code (e.g., en_US) | 
**ParameterFormat** | **string** | Variable style: POSITIONAL ({{1}}, the default) or NAMED ({{customer_name}}). Named templates provide examples via body_text_named_params / header_text_named_params. Inferred as NAMED when omitted but a named-params example is present. | [optional] 
**Components** | [**List&lt;WhatsAppTemplateComponent&gt;**](WhatsAppTemplateComponent.md) | Template components (header, body, footer, buttons, carousel, limited_time_offer). Required for custom templates, omit when using library_template_name. | [optional] 
**LibraryTemplateName** | **string** | Name of a pre-built template from Meta&#39;s template library (e.g., \&quot;appointment_reminder\&quot;, \&quot;auto_pay_reminder_1\&quot;, \&quot;address_update\&quot;). When provided, the template is pre-approved by Meta with no review wait. Omit components when using this field.  | [optional] 
**LibraryTemplateBodyInputs** | **Object** | Optional body customizations for library templates. Available options depend on the template (e.g., add_contact_number, add_learn_more_link, add_security_recommendation, add_track_package_link, code_expiration_minutes).  | [optional] 
**LibraryTemplateButtonInputs** | [**List&lt;CreateWhatsAppTemplateRequestLibraryTemplateButtonInputsInner&gt;**](CreateWhatsAppTemplateRequestLibraryTemplateButtonInputsInner.md) | Optional button customizations for library templates. Each item specifies button type and configuration (e.g., URL, phone number, quick reply).  | [optional] 
**MessageSendTtlSeconds** | **int** | Delivery validity window in seconds: a message not delivered within it is dropped. Range depends on category: AUTHENTICATION 30 to 900, UTILITY 30 to 43200 (12h), MARKETING 43200 to 2592000 (30 days); -1 (create only) keeps the 30-day default on AUTHENTICATION and UTILITY. Meta defaults to 600 for AUTHENTICATION and 30 days otherwise. If Meta later recategorises the template, it clears the TTL (read it back to check). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

