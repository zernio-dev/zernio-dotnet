# Zernio.Model.ListCommentAutomations200ResponseAutomationsInnerStats

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Triggered** | **int** |  | [optional] 
**DmsSent** | **int** |  | [optional] 
**DmsFailed** | **int** |  | [optional] 
**UniqueContacts** | **int** |  | [optional] 
**TrackedSends** | **int** | DMs sent with a trackable (wrapped) link. CTR denominator: divide clicks by this, not dmsSent. Lags dmsSent for campaigns that predate click tracking. | [optional] 
**LinkClicks** | **int** | Total clicks on tracked links (bots/prefetch excluded). | [optional] 
**UniqueClicks** | **int** | Distinct people who clicked a tracked link. | [optional] 
**Delivered** | **int** | DMs confirmed delivered (Messenger; IG emits no delivery receipt). | [optional] 
**Read** | **int** | DMs confirmed read (IG messaging_seen / Messenger message_reads). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

