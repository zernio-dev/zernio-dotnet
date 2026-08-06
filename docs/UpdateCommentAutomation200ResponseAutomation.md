# Zernio.Model.UpdateCommentAutomation200ResponseAutomation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Keywords** | **List&lt;string&gt;** |  | [optional] 
**MatchMode** | **string** | How a keyword is compared with the comment. &#39;contains&#39; (default) matches anywhere, even inside another word (keyword &#39;app&#39; fires on &#39;happy&#39;). &#39;word&#39; matches the keyword only as a standalone word. &#39;exact&#39; requires the whole comment to be exactly the keyword. | [optional] 
**ExcludeKeywords** | **List&lt;string&gt;** | Comments containing one of these never trigger the automation, even when a trigger keyword also matches. Compared using the same matchMode. | [optional] 
**TypoTolerance** | **bool** | Only with matchMode&#x3D;word: also fire on close misspellings of a keyword (one edit for 4-7 character keywords, two from 8 up). Keywords shorter than 4 characters are never fuzzy-matched. | [optional] 
**DmMessage** | **string** |  | [optional] 
**Buttons** | [**List&lt;DmButton&gt;**](DmButton.md) | Inline DM buttons (up to 3). Omitted when none are set. | [optional] 
**CommentReply** | **string** |  | [optional] 
**DmMessageVariations** | **List&lt;string&gt;** | Alternate DM texts rotated at random with dmMessage. Omitted when none. | [optional] 
**CommentReplyVariations** | **List&lt;string&gt;** | Alternate public replies rotated at random with commentReply. Omitted when none. | [optional] 
**IsActive** | **bool** |  | [optional] 
**UpdatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

