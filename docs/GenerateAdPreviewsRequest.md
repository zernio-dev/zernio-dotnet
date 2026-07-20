# Zernio.Model.GenerateAdPreviewsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id used to resolve the Meta token. | 
**AdAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). | 
**Formats** | **List&lt;string&gt;** | Meta ad_format values, one preview per format. Defaults to [DESKTOP_FEED_STANDARD]. | [optional] 
**ExistingCreativeId** | **string** | Preview an existing ad-account creative by id. Mutually exclusive with creativeSpec. | [optional] 
**CreativeSpec** | **Dictionary&lt;string, Object&gt;** | Raw Meta creative spec forwarded verbatim to /generatepreviews. Mutually exclusive with existingCreativeId. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

