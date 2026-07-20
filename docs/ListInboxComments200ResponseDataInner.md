# Zernio.Model.ListInboxComments200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**AccountUsername** | **string** |  | [optional] 
**Content** | **string** | The post text/caption. On ad rows (isAd: true) this is the AD NAME, not the underlying post&#39;s caption — the creative text isn&#39;t exposed here. | [optional] 
**Picture** | **string** | Post media thumbnail. On ad rows this is the ad creative thumbnail. | [optional] 
**Permalink** | **string** | Public URL of the post. On ad rows: the Facebook dark-post URL (facebook placement) or the IG media permalink (instagram placement); may be null when unknown. | [optional] 
**CreatedTime** | **DateTime** |  | [optional] 
**CommentCount** | **int** |  | [optional] 
**LikeCount** | **int** | Not fetched for ad rows (always 0 there). | [optional] 
**Cid** | **string** | Bluesky content identifier | [optional] 
**Subreddit** | **string** | Reddit subreddit name | [optional] 
**IsAd** | **bool** | True when this row is an ad (boosted/dark post). &#x60;platform&#x60; is then the placement (facebook &#x3D; the Page dark post / instagram &#x3D; the IG media), &#x60;id&#x60; is &#x60;{adId}:{placement}&#x60;, and the thread is at GET /v1/ads/{adId}/comments?placement&#x3D;{placement}. | [optional] 
**AdId** | **string** | Internal Zernio ad id — only on ad rows. | [optional] 
**Placement** | **string** | Which side of the ad this row&#39;s comments are on — only on ad rows. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

