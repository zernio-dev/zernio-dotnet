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
**Type** | **string** | &#x60;series&#x60; is a recurring master, &#x60;occurrence&#x60; one of its instances, and &#x60;exception&#x60; an instance changed on its own. Google flags an instance as an exception only when it was moved off its slot. | [optional] 
**OriginalStart** | **string** | For an occurrence or exception, the start it has in the series pattern. | [optional] 
**HtmlLink** | **string** |  | [optional] 
**ReadOnly** | **bool** |  | [optional] 
**Metadata** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**CreatedAt** | **DateTime?** |  | [optional] 
**UpdatedAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

