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
**Origin** | **string** | Google&#39;s ConversionOrigin, e.g. WEBSITE, APP. Together with category it names the goal the action belongs to (see GET /v1/ads/conversions/goals). | [optional] 
**PrimaryForGoal** | **bool** | true &#x3D; primary (counts toward bidding when its goal is biddable), false &#x3D; secondary. Change it with PATCH /v1/ads/conversions/actions/{actionId}. | [optional] 
**DefaultValue** | **decimal** | Value recorded when the conversion carries none. | [optional] 
**DefaultCurrency** | **string** | ISO 4217 currency of defaultValue. | [optional] 
**AlwaysUseDefaultValue** | **bool** | true &#x3D; defaultValue is used even when the conversion sends its own value. | [optional] 
**CountingType** | **string** | Google&#39;s ConversionActionCountingType: ONE_PER_CLICK or MANY_PER_CLICK. | [optional] 
**ClickThroughLookbackWindowDays** | **int** | Days after an ad click a conversion is still credited (1 to 90). | [optional] 
**ViewThroughLookbackWindowDays** | **int** | Days after an ad view a conversion is still credited (1 to 30). | [optional] 
**TagSnippets** | [**List&lt;ConversionActionTagSnippetsInner&gt;**](ConversionActionTagSnippetsInner.md) | The code a customer pastes onto their site. Present for types Google generates a snippet for (e.g. WEBPAGE); empty otherwise.  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

