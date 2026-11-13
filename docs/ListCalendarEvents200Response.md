# Zernio.Model.ListCalendarEvents200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Data** | [**List&lt;CalendarEvent&gt;**](CalendarEvent.md) |  | [optional] 
**Pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] 
**Stale** | **bool** | Always true when present. Present only when the provider did not answer and this is the last list Zernio read for the same account and query within the past six hours. | [optional] 
**AsOf** | **DateTime** | When a stale list was read from the provider. Present only with &#x60;stale&#x60;. | [optional] 
**Partial** | **bool** | Always true when present. This response is one slice of the requested window because the provider did not answer for the whole of it. Follow &#x60;pagination.nextCursor&#x60; until it is null. Present only on a degraded read. | [optional] 
**CoveredFrom** | **DateTime** | Start of the part of the window this slice covers. Present only with &#x60;partial&#x60;. | [optional] 
**CoveredTo** | **DateTime** | End of the part of the window this slice covers. Present only with &#x60;partial&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

