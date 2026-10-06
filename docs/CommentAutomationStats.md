# Zernio.Model.CommentAutomationStats
Running counters for the automation.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Triggered** | **int** | Matched triggers that reached the audience or send stage. | [optional] 
**DmsSent** | **int** |  | [optional] 
**DmsFailed** | **int** |  | [optional] 
**UniqueContacts** | **int** |  | [optional] 
**TrackedSends** | **int** | DMs sent with a trackable (wrapped) link. CTR denominator: divide clicks by this, not dmsSent. Lags dmsSent for campaigns that predate click tracking. | [optional] 
**LinkClicks** | **int** | Total clicks on tracked links (bots/prefetch excluded). | [optional] 
**UniqueClicks** | **int** | Distinct people who clicked a tracked link. | [optional] 
**Delivered** | **int** | DMs confirmed delivered (Messenger; IG emits no delivery receipt). | [optional] 
**Read** | **int** | DMs confirmed read (IG messaging_seen / Messenger message_reads). | [optional] 
**AudienceSkipped** | **int** | Triggers the audience rule did not answer with the DM. | [optional] 
**FollowGateSent** | **int** |  | [optional] 
**FollowGatePassed** | **int** |  | [optional] 
**FollowGateFailed** | **int** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

