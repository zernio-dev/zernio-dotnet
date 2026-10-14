# Zernio.Model.GetAd200ResponseDarkPost
Only when `{adId}` is a Facebook ad dark post with no resolvable ad (then `ad` is null).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | [optional] 
**PlatformPostId** | **string** | The dark post id, &#x60;{pageId}_{postId}&#x60;. | [optional] 
**PageId** | **string** |  | [optional] 
**IsDarkPost** | **bool** | Always true. | [optional] 
**AdId** | **string** | Always null: Meta exposes no link from a placement dark post to its ad. | [optional] 
**AccountId** | **string** | Zernio Meta Ads account id for the Page, null when none is connected. | [optional] 
**FacebookAccountId** | **string** | Zernio Facebook account id of the Page. | [optional] 
**PlatformAdAccountIds** | **List&lt;string&gt;** | Meta ad accounts (&#x60;act_...&#x60;) with synced ads on this Page. | [optional] 
**FirstSeenAt** | **DateTime** |  | [optional] 
**LastActivityAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

