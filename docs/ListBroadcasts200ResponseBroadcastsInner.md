# Zernio.Model.ListBroadcasts200ResponseBroadcastsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**AccountName** | **string** | Display name of the sending account | [optional] 
**Status** | **string** |  | [optional] 
**MessagePreview** | **string** | Template name or message text snippet | [optional] 
**ScheduledAt** | **DateTime** |  | [optional] 
**StartedAt** | **DateTime** |  | [optional] 
**CompletedAt** | **DateTime** |  | [optional] 
**RecipientCount** | **int** |  | [optional] 
**SentCount** | **int** | Recipients whose latest status is &#x60;sent&#x60;: the platform accepted the message and has not confirmed delivery yet. Each recipient counts once, under its latest status, so everyone the broadcast went out to is sentCount + deliveredCount + readCount. | [optional] 
**DeliveredCount** | **int** | Recipients whose latest status is &#x60;delivered&#x60;, not read yet. Everyone it was delivered to is deliveredCount + readCount. | [optional] 
**ReadCount** | **int** | Recipients whose latest status is &#x60;read&#x60;. | [optional] 
**FailedCount** | **int** | Recipients whose send failed. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

