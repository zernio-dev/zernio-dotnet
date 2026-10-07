# Zernio.Model.UpdateConversionActionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id (Google Ads) | 
**AdAccountId** | **string** | Google customer id. Required when the connection has multiple customers. | [optional] 
**CustomerId** | **string** | Alias of adAccountId | [optional] 
**Name** | **string** |  | [optional] 
**Status** | **string** | REMOVED removes the action and must be sent alone; ENABLED restores a removed one. | [optional] 
**DefaultValue** | **decimal** |  | [optional] 
**AlwaysUseDefaultValue** | **bool** |  | [optional] 
**Category** | **string** | conversion_action.category. Defaults to DEFAULT on create. | [optional] 
**CountingType** | **string** | ONE_PER_CLICK counts one conversion per ad click (leads); MANY_PER_CLICK counts every one (purchases). | [optional] 
**DefaultCurrency** | **string** | ISO 4217 currency of defaultValue (value_settings.default_currency_code). | [optional] 
**ClickThroughLookbackWindowDays** | **int** | Days after an ad click a conversion still counts. | [optional] 
**ViewThroughLookbackWindowDays** | **int** | Days after an ad view a view-through conversion still counts. | [optional] 
**PrimaryForGoal** | **bool** | true &#x3D; primary (counts toward bidding when its goal is biddable), false &#x3D; secondary. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

