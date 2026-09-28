# Zernio.Model.UpdateTrackingTagRequest
At least one updatable field is required; the route returns 400 if the body is empty or names a field the tag's platform cannot update.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdAccountId** | **string** | Scopes the lookup on platforms whose tag ids live inside an ad account. Ignored elsewhere. | [optional] 
**Name** | **string** |  | [optional] 
**EnableAutomaticMatching** | **bool** | Meta Advanced Matching toggle (&#x60;enable_automatic_matching&#x60;). | [optional] 
**AutomaticMatchingFields** | **List&lt;UpdateTrackingTagRequest.AutomaticMatchingFieldsEnum&gt;** | Which user fields Advanced Matching may collect. Meta&#39;s terse codes: em&#x3D;email, ph&#x3D;phone, fn&#x3D;first name, ln&#x3D;last name, ge&#x3D;gender, db&#x3D;date of birth, ct&#x3D;city, st&#x3D;state, zp&#x3D;zip.  | [optional] 
**FirstPartyCookieStatus** | **string** |  | [optional] 
**DataUseSetting** | **string** |  | [optional] 
**EnableFirstPartyCookies** | **bool** | First-party cookie on or off (TikTok, LinkedIn). Platform-neutral alternative to &#x60;firstPartyCookieStatus&#x60;. | [optional] 
**AutoTagging** | **bool** | Google Ads: turn gclid auto-tagging on or off for the ad account. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

