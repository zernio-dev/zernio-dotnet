# Zernio.Model.DeleteAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**AccountId** | **string** | Zernio SocialAccount id owning the ad account. Required only to delete an EMPTY campaign (zero ads), which has no local Ad documents to resolve a token from. | [optional] 
**AdAccountId** | **string** | X only, for an EMPTY campaign that was never synced: the X ad account id the campaign belongs to (lowercase letters and digits). The synced campaign&#39;s ad account wins when there is one. Also accepted on the query string. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

