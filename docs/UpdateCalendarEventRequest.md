# Zernio.Model.UpdateCalendarEventRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** |  | [optional] 
**Description** | **string** | HTML. | [optional] 
**Location** | **string** |  | [optional] 
**Start** | **string** | ISO date-time, or a date (&#x60;YYYY-MM-DD&#x60;) for all-day events. | [optional] 
**End** | **string** | Exclusive for all-day events. | [optional] 
**AllDay** | **bool** |  | [optional] 
**Timezone** | **string** | IANA zone the event is scheduled in. Default UTC. | [optional] 
**Participants** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**Recurrence** | **List&lt;string&gt;** | RRULE lines, e.g. &#x60;RRULE:FREQ&#x3D;WEEKLY;BYDAY&#x3D;MO,WE;COUNT&#x3D;10&#x60;. | [optional] 
**Reminders** | [**CalendarEventFieldsReminders**](CalendarEventFieldsReminders.md) |  | [optional] 
**Conferencing** | **string** |  | [optional] 
**Busy** | **bool** |  | [optional] 
**Visibility** | **string** |  | [optional] 
**Metadata** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**AccountId** | **string** |  | 
**CalendarId** | **string** | The calendar holding the event (an id from GET /v1/calendar/calendars). Defaults to the primary calendar. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

