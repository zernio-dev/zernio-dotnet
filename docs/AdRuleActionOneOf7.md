# Zernio.Model.AdRuleActionOneOf7
Exactly one of `add` and `remove`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | Tag the object by its name. Meta, TikTok and Reddit campaigns, ad sets and ads, and Google, LinkedIn and Pinterest campaigns and ad sets. An object whose name already has the tag (or lacks it, for &#x60;remove&#x60;) is skipped with &#x60;name_unchanged&#x60;. | 
**Add** | **string** | Text to add, like &#x60;[WINNER]&#x60;. Compared without case. | [optional] 
**At** | **string** | Where &#x60;add&#x60; goes. Defaults to &#x60;start&#x60;. | [optional] 
**Remove** | **string** | Text to take out of the name, every copy of it. | [optional] 
**MaxChangesPerDay** | **int** | At most this many objects changed in any 24 hours, across runs. Matches over the limit are skipped with &#x60;daily_limit_reached&#x60; and tried again later. | [optional] 
**MaxChangesPerObject** | **int** | At most this many changes to one object by this rule, counted over the last 400 days. An object at the limit is left alone like one in cooldown. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

