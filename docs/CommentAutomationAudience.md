# Zernio.Model.CommentAutomationAudience
Who a comment automation answers. Instagram only - Meta exposes the follow relationship on no other platform, and only for people who have MESSAGED the account (a comment grants no consent). `whenUnknown` is therefore the important setting: it decides what happens for a first-time commenter. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FollowerStatus** | **string** |  | [optional] [default to FollowerStatusEnum.Any]
**MinFollowerCount** | **int** | Skip commenters with fewer followers than this. Omit for no size rule. | [optional] 
**WhenUnknown** | **string** | What to do when Instagram will not reveal the follow relationship.   * &#x60;send&#x60; (default) - deliver the DM anyway (fails open).   * &#x60;skip&#x60; - stay silent.   * &#x60;verify&#x60; - send &#x60;followGate.message&#x60; with a confirm button. Tapping it is a     message, which grants consent, so the re-check on the tap resolves and the     real DM (or &#x60;followGate.notFollowingMessage&#x60;) follows automatically.  | [optional] [default to WhenUnknownEnum.Send]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

