# Zernio.Model.CalendarFreeBusy200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | [optional] 
**From** | **DateTime** |  | [optional] 
**To** | **DateTime** |  | [optional] 
**Busy** | [**List&lt;BusyBlock&gt;**](BusyBlock.md) | The account&#39;s own busy time across the calendars read, merged. Null when the account could not be read. | [optional] 
**Calendars** | [**List&lt;CalendarFreeBusy200ResponseDataInnerCalendarsInner&gt;**](CalendarFreeBusy200ResponseDataInnerCalendarsInner.md) |  | [optional] 
**People** | [**List&lt;CalendarFreeBusy200ResponseDataInnerPeopleInner&gt;**](CalendarFreeBusy200ResponseDataInnerPeopleInner.md) |  | [optional] 
**Error** | [**FreeBusyError**](FreeBusyError.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

