# Zernio.Model.AdRuleActionOneOf2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | Reactivate a campaign, ad set or ad a rule paused, once &#x60;cooldownMinutes&#x60; has passed since the pause. Objects you paused yourself are left alone unless &#x60;includeManuallyPaused&#x60; is true. | 
**IncludeManuallyPaused** | **bool** | Also reactivate paused objects that no rule paused, as soon as they match. | [optional] 
**MaxChangesPerDay** | **int** | At most this many objects changed in any 24 hours, across runs. Matches over the limit are skipped with &#x60;daily_limit_reached&#x60; and tried again later. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

