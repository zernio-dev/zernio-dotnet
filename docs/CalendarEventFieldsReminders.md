# Zernio.Model.CalendarEventFieldsReminders

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UseDefault** | **bool** | Use the calendar&#39;s default reminders. Ignored when &#x60;overrides&#x60; has entries. | [optional] 
**Overrides** | [**List&lt;CalendarEventFieldsRemindersOverridesInner&gt;**](CalendarEventFieldsRemindersOverridesInner.md) | Google takes up to 5 overrides, &#x60;popup&#x60; or &#x60;email&#x60;. Outlook keeps one popup reminder (the first override), and an &#x60;email&#x60; override answers 400 &#x60;reminder_method_unsupported&#x60; on a Microsoft account. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

