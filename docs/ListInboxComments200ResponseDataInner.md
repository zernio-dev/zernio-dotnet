# Zernio.Model.ListInboxComments200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**AccountUsername** | **string** |  | [optional] 
**Content** | **string** |  | [optional] 
**Picture** | **string** |  | [optional] 
**Permalink** | **string** |  | [optional] 
**CreatedTime** | **DateTime** |  | [optional] 
**CommentCount** | **int** |  | [optional] 
**LikeCount** | **int** |  | [optional] 
**Cid** | **string** | Bluesky content identifier | [optional] 
**Subreddit** | **string** | Reddit subreddit name | [optional] 
**IsAd** | **bool** | True when this row is an ad (boosted/dark post). &#x60;platform&#x60; is then the comment platform (facebook or instagram), &#x60;id&#x60; equals &#x60;adId&#x60;, and the thread is at GET /v1/ads/{adId}/comments. | [optional] 
**AdId** | **string** | Internal Zernio ad id — only on ad rows (same value as &#x60;id&#x60;). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

