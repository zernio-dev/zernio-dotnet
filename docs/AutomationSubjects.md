# Zernio.Model.AutomationSubjects
What an ad rule checks, and where.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Each** | **string** | The objects judged one by one. | 
**AdAccounts** | [**List&lt;AutomationSubjectsAdAccountsInner&gt;**](AutomationSubjectsAdAccountsInner.md) | The ad account to check. One per ad rule, and an edit cannot move it to another. | 
**CampaignIds** | **List&lt;string&gt;** | Only these platform campaigns or their ad sets and ads. Leave out to check the whole ad account. | [optional] 
**Filters** | [**List&lt;AutomationAdFilter&gt;**](AutomationAdFilter.md) | All must hold. | [optional] 
**Groups** | [**List&lt;AutomationSubjectsGroupsInner&gt;**](AutomationSubjectsGroupsInner.md) | Judges campaigns together (campaign rules only): each group&#39;s numbers are summed and its rates computed on the totals, and a matching group acts on each of its campaigns.  A group with no filters holds every campaign the rule checks. &#x60;reach&#x60; and &#x60;frequency&#x60; cannot be used with groups.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

