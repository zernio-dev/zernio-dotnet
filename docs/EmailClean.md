# Zernio.Model.EmailClean
Only with `clean=true`. The new text of the mail, deterministic (no model): client quote markup first, then attribution lines in common languages, then boilerplate such as \"Sent from my iPhone\".  `text` is never empty when the mail has a body: when extraction leaves nothing, the whole body comes back with `status: fallback`.  The sender's signature stays in `text` and is also in `signature`. A forward keeps the forwarded content and its header block is parsed into `forwarded`. A bounce report passes through whole. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Text** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**Removed** | [**EmailCleanRemoved**](EmailCleanRemoved.md) |  | [optional] 
**Signature** | **string** |  | [optional] 
**Forwarded** | [**EmailCleanForwarded**](EmailCleanForwarded.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

