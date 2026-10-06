# Zernio.Model.CommentAutomationRepeatPolicy
Whether a commenter can receive this automation's DM more than once.   * `once` (default) - one DM per person per door, ever.   * `every_comment` - every new matching comment is eligible again. One comment     is still answered at most once. `cooldownHours` suppresses a repeat sent to the     same person within that many hours. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Mode** | **string** |  | [default to ModeEnum.Once]
**CooldownHours** | **int** | every_comment only (400 with once). Hours after a DM during which the same person is not DMed again. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

