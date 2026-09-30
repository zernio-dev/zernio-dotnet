# Zernio.Model.GetAllAccountsHealth200ResponseAccountsInnerMessagingRestriction
Observed from Meta's own errors on our own sends, not a live probe. Facebook/Instagram: error subcodes 2534122, 1893063, 2534029, set on the first refused send and cleared when a later send succeeds. WhatsApp: Cloud API error codes 131042 (payment or eligibility issue), 131031 (Business Account locked) and 368 (policy block), set when a send or a delivery status fails with one and cleared when a later message is delivered. It lags reality by one message in each direction. After subcode 1893063 (Meta refusing the Page's messages), comment automation DMs are held and one is retried at `pausedUntil`: 30 minutes, doubling per refused retry up to 4 hours; held DMs stay pending and are sent once Meta accepts again, within the 7-day private-reply window.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int?** | WhatsApp Cloud API error code. Null on Facebook and Instagram. | [optional] 
**Subcode** | **int?** | Meta error subcode (Facebook and Instagram). Null on WhatsApp. | [optional] 
**Message** | **string** |  | [optional] 
**FirstSeenAt** | **DateTime** |  | [optional] 
**LastSeenAt** | **DateTime** |  | [optional] 
**PausedUntil** | **DateTime?** | When held automation DMs are next retried. Null when nothing is held. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

