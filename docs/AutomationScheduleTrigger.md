# Zernio.Model.AutomationScheduleTrigger
When an ad rule runs: `every` an interval or at set weekly `times` (send one), optionally only between `startsAt` and `endsAt` and never inside `quietHours`. Times and quiet hours are in the ad account timezone. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Every** | **string** | Run every interval. Send this or &#x60;times&#x60;, not both. | [optional] 
**Times** | [**List&lt;AutomationScheduleTriggerTimesInner&gt;**](AutomationScheduleTriggerTimesInner.md) | Set weekly times. Send this or &#x60;every&#x60;, not both. | [optional] 
**StartsAt** | **DateTime** | Runs from this time on. | [optional] 
**EndsAt** | **DateTime** | Stops running after this time. Must be after &#x60;startsAt&#x60;. | [optional] 
**QuietHours** | [**AutomationScheduleTriggerQuietHours**](AutomationScheduleTriggerQuietHours.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

