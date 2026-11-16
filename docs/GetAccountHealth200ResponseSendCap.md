# Zernio.Model.GetAccountHealth200ResponseSendCap
Google and Microsoft only: today's outbound mail allowance for the mailbox.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Limit** | **int** | Today&#39;s cap: the base cap, doubled after 14 days of sending with no spam signal. | [optional] 
**BaseLimit** | **int** | The cap before doubling. | [optional] 
**Doubled** | **bool** |  | [optional] 
**DoublesAt** | **DateTime?** | When the cap doubles if the mailbox sends every day from now on and raises no spam signal. Null once doubled, with a manual limit, and on IMAP. | [optional] 
**Used** | **int** |  | [optional] 
**ResetsAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

