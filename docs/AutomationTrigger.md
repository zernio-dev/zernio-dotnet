# Zernio.Model.AutomationTrigger
When the automation runs. Its shape decides the kind:  - A Zernio event name in `type` makes an event automation. - A `schedule` over `subjects.each: post` makes a scheduled automation. - Any other `schedule` makes an ad rule. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Every** | **string** |  | 
**Times** | [**List&lt;AutomationScheduleTriggerTimesInner&gt;**](AutomationScheduleTriggerTimesInner.md) | Set weekly times. Send this or &#x60;every&#x60;, not both. | [optional] 
**StartsAt** | **DateTime** | Runs from this time on. | [optional] 
**EndsAt** | **DateTime** | Stops running after this time. | [optional] 
**QuietHours** | [**AutomationScheduleTriggerQuietHours**](AutomationScheduleTriggerQuietHours.md) |  | [optional] 
**ProfileId** | **string** | The profile whose events start it, from &#x60;GET /v1/profiles&#x60;. | 
**AccountIds** | **List&lt;string&gt;** | Only events of these accounts. Leave out for every account of the profile. | [optional] 
**Filter** | [**AutomationFactCondition**](AutomationFactCondition.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

