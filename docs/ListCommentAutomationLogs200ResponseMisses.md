# Zernio.Model.ListCommentAutomationLogs200ResponseMisses
Comments that reached this automation but matched none of its keywords. These produce no log entry, so this is the only signal that a keyword is catching nothing. Retained for a short window, then dropped.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Total** | **int** | Number of non-matching comments in the retention window | [optional] 
**RetentionDays** | **int** | How many days of non-matching comments the total covers | [optional] 
**Samples** | [**List&lt;ListCommentAutomationLogs200ResponseMissesSamplesInner&gt;**](ListCommentAutomationLogs200ResponseMissesSamplesInner.md) | A few of the most recent non-matching comments, for diagnosing a keyword setup. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

