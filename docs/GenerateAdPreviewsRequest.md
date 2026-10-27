# Zernio.Model.GenerateAdPreviewsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id used to resolve the Meta token. | 
**AdAccountId** | **string** | Platform ad account id (Meta act_&lt;n&gt;, Google customer id, LinkedIn account id, ...). | 
**Formats** | **List&lt;string&gt;** | Meta ad_format values, one preview per format. Defaults to [DESKTOP_FEED_STANDARD]. | [optional] 
**ExistingCreativeId** | **string** | Preview an existing ad-account creative by id. Mutually exclusive with creativeSpec. | [optional] 
**CreativeSpec** | **Dictionary&lt;string, Object&gt;** | Raw Meta creative spec forwarded to /generatepreviews. Mutually exclusive with existingCreativeId. An &#x60;object_story_spec&#x60; without &#x60;page_id&#x60; or &#x60;instagram_user_id&#x60;, and a &#x60;source_instagram_media_id&#x60; spec without &#x60;instagram_user_id&#x60;, get the connection&#39;s Facebook Page and Instagram account, as a create would. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

