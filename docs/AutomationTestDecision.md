# Zernio.Model.AutomationTestDecision
What the automation would do with the sample, decided by the code its live runs use.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**WouldRun** | **bool** |  | 
**Reason** | **string** | Why it would not run: keyword_miss, keyword_excluded, other_post, trigger_miss, not_first_message, account_not_listened, filter_miss, no_match, subject_not_matched, post_not_matched, no_accounts, no_subscribed_channel, unsubscribed, already_enrolled, runs_paused, paused or draft. | [optional] 
**Matched** | [**List&lt;AutomationTestDecisionMatchedInner&gt;**](AutomationTestDecisionMatchedInner.md) | What the sample met, such as a keyword, a filter condition, the trigger, a post or an ad. | 
**PlannedSteps** | [**List&lt;AutomationTestDecisionPlannedStepsInner&gt;**](AutomationTestDecisionPlannedStepsInner.md) | The steps it would take, in order. A flow lists its first steps up to the first branch. | 
**NextRunAt** | **DateTime?** | A scheduled automation&#39;s next check. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

