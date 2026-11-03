# Zernio.Model.InboundActivity
When inbound messages and comments were first and last seen for the account. Only events matched to this account count. WhatsApp delivery statuses for outbound messages do not count, so the stamps of a number that only sends stay null. The stamps reset on every connect.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FirstMessageAt** | **DateTime?** | First inbound message since the latest connect, or since tracking began for an account connected before it. Null when none yet. | 
**LastMessageAt** | **DateTime?** | Latest inbound message, precise to about one hour. Null when none yet. | 
**FirstCommentAt** | **DateTime?** | First inbound comment since the latest connect, or since tracking began for an account connected before it. Null when none yet. | 
**LastCommentAt** | **DateTime?** | Latest inbound comment, precise to about one hour. Null when none yet. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

