# Zernio.Model.XArticle
Long-form X Article payload. X Articles require an eligible X Premium+ account. Articles are mutually exclusive with top-level/custom tweet media and with threadItems, poll, quoteTweetId, replyToTweetId, inReplyToTweetId, replySettings, sensitiveMedia, paidPartnership, and madeWithAi. Publishing normally performs two billable X API requests at $0.010 each (draft + publish, $0.020 total); mode `draft` performs only the $0.010 draft request. `articleDraftId` is an internal recovery checkpoint and must not be supplied by API clients. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** |  | 
**ContentState** | [**XArticleContentState**](XArticleContentState.md) |  | 
**Mode** | **string** | Publish creates an X Article draft and then publishes it. Draft stops after draft creation and returns the X draft ID without a public URL. | [optional] [default to ModeEnum.Publish]
**Cover** | [**XArticleCover**](XArticleCover.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

