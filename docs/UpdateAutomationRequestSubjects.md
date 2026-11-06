# Zernio.Model.UpdateAutomationRequestSubjects

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Each** | **string** |  | 
**AdAccounts** | [**List&lt;AutomationSubjectsAdAccountsInner&gt;**](AutomationSubjectsAdAccountsInner.md) | The ad account to check. One per ad rule, and an edit cannot move it to another. | 
**CampaignIds** | **List&lt;string&gt;** | Only these platform campaigns or their ad sets and ads. Leave out to check the whole ad account. | [optional] 
**Filters** | [**List&lt;AutomationAdFilter&gt;**](AutomationAdFilter.md) | All must hold. | [optional] 
**Groups** | [**List&lt;AutomationSubjectsGroupsInner&gt;**](AutomationSubjectsGroupsInner.md) | Judges campaigns together (campaign rules only): each group&#39;s numbers are summed and its rates computed on the totals, and a matching group acts on each of its campaigns.  A group with no filters holds every campaign the rule checks. &#x60;reach&#x60; and &#x60;frequency&#x60; cannot be used with groups.  | [optional] 
**ProfileId** | **string** | The profile whose posts are checked. | 
**AccountIds** | **List&lt;string&gt;** | Only posts of these accounts. Each must be active on the profile. | [optional] 
**PublishedWithin** | **string** | How far back posts are checked, by when they were published. Whole days, from &#x60;1d&#x60; to &#x60;30d&#x60; (&#x60;48h&#x60; is 2 days). | [optional] [default to "7d"]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

