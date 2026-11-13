# Zernio.Model.ListEmailFolders200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Data** | [**List&lt;EmailFolder&gt;**](EmailFolder.md) |  | [optional] 
**Stale** | **bool** | Always true when present. Present only when the provider did not answer and &#x60;data&#x60; is the last folder list Zernio read for the same account within the past 24 hours (&#x60;unreadCount&#x60; and &#x60;totalCount&#x60; may be out of date). | [optional] 
**AsOf** | **DateTime** | When a stale list was read from the provider. Present only with &#x60;stale&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

