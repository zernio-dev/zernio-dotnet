# Zernio.Model.ListCalendarEvents200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Data** | [**List&lt;CalendarEvent&gt;**](CalendarEvent.md) |  | [optional] 
**Pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] 
**Stale** | **bool** | Always true when present. Present only when the provider did not answer and this is the last list Zernio read for the same account and query within the past hour. | [optional] 
**AsOf** | **DateTime** | When a stale list was read from the provider. Present only with &#x60;stale&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

