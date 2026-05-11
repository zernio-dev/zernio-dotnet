# Zernio.Model.UpdateTrackingTagRequest
At least one field is required; the route returns 400 if the body is empty.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | [optional] 
**EnableAutomaticMatching** | **bool** | Meta Advanced Matching toggle (&#x60;enable_automatic_matching&#x60;). | [optional] 
**AutomaticMatchingFields** | **List&lt;UpdateTrackingTagRequest.AutomaticMatchingFieldsEnum&gt;** | Which user fields Advanced Matching may collect. Meta&#39;s terse codes: em&#x3D;email, ph&#x3D;phone, fn&#x3D;first name, ln&#x3D;last name, ge&#x3D;gender, db&#x3D;date of birth, ct&#x3D;city, st&#x3D;state, zp&#x3D;zip.  | [optional] 
**FirstPartyCookieStatus** | **string** |  | [optional] 
**DataUseSetting** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

