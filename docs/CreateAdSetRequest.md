# Zernio.Model.CreateAdSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id owning the Google Ads connection. | 
**Platform** | **string** | Only \&quot;google\&quot; is implemented today; every other value returns 501. | 
**CampaignId** | **string** | Google platform campaign ID (numeric) the ad group is created under. | 
**Name** | **string** |  | 
**Status** | **string** |  | [optional] [default to StatusEnum.PAUSED]
**AdAccountId** | **string** | Platform ad account ID (Google customer ID, digits only). Only required when the connection has more than one. | [optional] 
**CustomerId** | **string** | Alias of adAccountId, kept for existing callers | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

