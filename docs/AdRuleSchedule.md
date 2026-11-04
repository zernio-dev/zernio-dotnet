# Zernio.Model.AdRuleSchedule
Either `everyMinutes` or `times`. Sending a schedule replaces the rule's whole timing. Without one, a new rule runs every 60 minutes.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EveryMinutes** | **int?** | How often the rule runs, in minutes. Null on a rule that runs at set times. | [optional] 
**Times** | [**List&lt;AdRuleScheduleTimesInner&gt;**](AdRuleScheduleTimesInner.md) | Set weekly times in the ad account timezone, instead of an interval. A rule that changes ads needs a cooldown of at least the shortest gap between two times. | [optional] 
**StartsAt** | **DateTime?** | The rule runs from this time on. | [optional] 
**EndsAt** | **DateTime?** | The rule stops running after this time. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

