# Zernio.Model.CalendarEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**Provider** | **string** |  | [optional] 
**CalendarId** | **string** |  | [optional] 
**Title** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**Location** | **string** |  | [optional] 
**Start** | **string** | ISO date-time with the rendered offset, or a date for all-day events. | [optional] 
**End** | **string** |  | [optional] 
**AllDay** | **bool** |  | [optional] 
**Timezone** | **string** |  | [optional] 
**Participants** | [**List&lt;CalendarEventParticipantsInner&gt;**](CalendarEventParticipantsInner.md) |  | [optional] 
**Organizer** | [**EmailAddress**](EmailAddress.md) |  | [optional] 
**Recurrence** | **List&lt;string&gt;** |  | [optional] 
**Reminders** | [**CalendarEventReminders**](CalendarEventReminders.md) |  | [optional] 
**Conferencing** | [**CalendarEventConferencing**](CalendarEventConferencing.md) |  | [optional] 
**Busy** | **bool** |  | [optional] 
**Visibility** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**IcalUid** | **string** |  | [optional] 
**MasterEventId** | **string** |  | [optional] 
**HtmlLink** | **string** |  | [optional] 
**ReadOnly** | **bool** |  | [optional] 
**Metadata** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**CreatedAt** | **DateTime?** |  | [optional] 
**UpdatedAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

