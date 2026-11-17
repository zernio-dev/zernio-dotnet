# Zernio.Model.ListAdAccountRuleAlerts200ResponseAlertsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RuleId** | **string** | The rule the alert belongs to. | 
**Id** | **string** |  | 
**ObjectId** | **string** | Platform campaign, ad set or ad ID, or the id of the keyword or search term. | 
**State** | **string** |  | 
**Severity** | **string** |  | 
**ConsecutiveMatches** | **int** |  | 
**OpenedAt** | **DateTime?** |  | 
**LastMatchedAt** | **DateTime** |  | 
**LastEvaluatedAt** | **DateTime** | When a run last evaluated the object of this alert. Older than the latest run of its rule means that run did not evaluate it. | 
**ResolvedAt** | **DateTime?** | Always null here: only open alerts are listed. | 
**ResolvedReason** | **string** | Always null here: only open alerts are listed. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

