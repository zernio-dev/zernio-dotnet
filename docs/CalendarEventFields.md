# Zernio.Model.CalendarEventFields

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** |  | [optional] 
**Description** | **string** | HTML. | [optional] 
**Location** | **string** |  | [optional] 
**Start** | **string** | ISO date-time, or a date (&#x60;YYYY-MM-DD&#x60;) for all-day events. | [optional] 
**End** | **string** | Exclusive for all-day events. | [optional] 
**AllDay** | **bool** |  | [optional] 
**Timezone** | **string** | IANA zone the event is scheduled in. Defaults to the calendar&#39;s zone on Google and the mailbox&#39;s working-hours zone on Microsoft (UTC when Outlook has none, as on personal accounts). A PATCH that moves an event without a zone keeps the zone the event already has. | [optional] 
**Participants** | [**List&lt;CalendarEventFieldsParticipantsInner&gt;**](CalendarEventFieldsParticipantsInner.md) |  | [optional] 
**Recurrence** | **List&lt;string&gt;** | RRULE lines, e.g. &#x60;RRULE:FREQ&#x3D;WEEKLY;BYDAY&#x3D;MO,WE;COUNT&#x3D;10&#x60;. Microsoft takes one RRULE plus EXDATE lines; Zernio removes the EXDATE occurrences after saving the series. | [optional] 
**Reminders** | [**CalendarEventFieldsReminders**](CalendarEventFieldsReminders.md) |  | [optional] 
**Conferencing** | **string** |  | [optional] 
**Busy** | **bool** |  | [optional] 
**Visibility** | **string** |  | [optional] 
**Metadata** | **Dictionary&lt;string, string&gt;** | String pairs stored on the event and returned on reads, on Google and Microsoft. | [optional] 
**NotifyParticipants** | **string** | Who gets an invitation or update email for this write: everyone, only guests outside the organizer&#39;s domain, or nobody. Google only; Outlook always notifies, so &#x60;external&#x60; and &#x60;none&#x60; answer 400 &#x60;unsupported_for_provider&#x60; on a Microsoft account. | [optional] [default to NotifyParticipantsEnum.All]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

