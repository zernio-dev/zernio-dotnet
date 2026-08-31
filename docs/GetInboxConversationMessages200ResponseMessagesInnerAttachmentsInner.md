# Zernio.Model.GetInboxConversationMessages200ResponseMessagesInnerAttachmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Type** | **string** |  | [optional] 
**OriginalType** | **string** | Instagram and Facebook only, and present only when it differs from &#x60;type&#x60;. Meta&#39;s own type before normalization: &#x60;ig_reel&#x60; and &#x60;reel&#x60; become &#x60;video&#x60;, while &#x60;ig_post&#x60;, &#x60;post&#x60;, &#x60;ig_story&#x60; and &#x60;story_mention&#x60; become &#x60;share&#x60;. A story mention is &#x60;type: \&quot;share\&quot;&#x60; with &#x60;originalType: \&quot;story_mention\&quot;&#x60;; render on this field, since &#x60;share&#x60; alone is ambiguous. | [optional] 
**Url** | **string** | Direct media link. On Instagram and Facebook this is a signed Meta CDN url that EXPIRES: use it now, do not store it. Persist &#x60;refreshUrl&#x60; instead. | [optional] 
**RefreshUrl** | **string** | Instagram and Facebook only. Endpoint that resolves this attachment to a working url every time, re-minting it from Meta when the stored one has expired. Safe to store and render indefinitely. | [optional] 
**Filename** | **string** |  | [optional] 
**PreviewUrl** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

