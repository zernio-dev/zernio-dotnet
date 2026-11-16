# Zernio.Model.GetAccountHealth200ResponseMailbox
Microsoft only: present while the login has no Exchange Online mailbox (no Exchange license, inactive, soft-deleted or on-premises). Mail and calendar requests then answer 412 `mailbox_not_available`; files are not affected. Absent when the mailbox works. `status` is also `warning`, with the reason in `issues`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | **string** |  | [optional] 
**Reason** | **string** |  | [optional] 
**Message** | **string** |  | [optional] 
**DetectedAt** | **DateTime** | When Microsoft last answered that the login has no mailbox. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

