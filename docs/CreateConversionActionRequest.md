# Zernio.Model.CreateConversionActionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | SocialAccount ID. Must be a &#x60;googleads&#x60; account. | 
**AdAccountId** | **string** | Platform ad account ID (Google customer ID, digits only). Resolved automatically when the connection has exactly one accessible customer. | [optional] 
**CustomerId** | **string** | Alias of adAccountId, kept for existing callers | [optional] 
**Name** | **string** |  | 
**Type** | **string** | Only WEBPAGE is supported for creation today. | 
**DefaultValue** | **decimal** | Default conversion value used when an event doesn&#39;t carry its own value. | [optional] 
**AlwaysUseDefaultValue** | **bool** | When true, always use defaultValue and ignore any value sent with the event. Defaults to true when defaultValue is set. | [optional] 
**Category** | **string** | conversion_action.category. Defaults to DEFAULT on create. | [optional] 
**CountingType** | **string** | ONE_PER_CLICK counts one conversion per ad click (leads); MANY_PER_CLICK counts every one (purchases). | [optional] 
**DefaultCurrency** | **string** | ISO 4217 currency of defaultValue (value_settings.default_currency_code). | [optional] 
**ClickThroughLookbackWindowDays** | **int** | Days after an ad click a conversion still counts. | [optional] 
**ViewThroughLookbackWindowDays** | **int** | Days after an ad view a view-through conversion still counts. | [optional] 
**PrimaryForGoal** | **bool** | true &#x3D; primary (counts toward bidding when its goal is biddable), false &#x3D; secondary. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

