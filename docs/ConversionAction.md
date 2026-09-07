# Zernio.Model.ConversionAction
A Google Ads conversion action, e.g. a WEBPAGE conversion created via `createConversionAction`. Returned by `listConversionActions` and `createConversionAction`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Google Ads conversion action id. | 
**Name** | **string** |  | 
**Type** | **string** | Google&#39;s ConversionActionType, e.g. WEBPAGE, UPLOAD_CLICKS. | 
**Status** | **string** | Google&#39;s ConversionActionStatus, e.g. ENABLED, REMOVED, HIDDEN. | 
**Category** | **string** | Google&#39;s ConversionActionCategory, e.g. DEFAULT, PURCHASE, LEAD. | 
**TagSnippets** | [**List&lt;ConversionActionTagSnippetsInner&gt;**](ConversionActionTagSnippetsInner.md) | The code a customer pastes onto their site. Present for types Google generates a snippet for (e.g. WEBPAGE); empty otherwise.  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

