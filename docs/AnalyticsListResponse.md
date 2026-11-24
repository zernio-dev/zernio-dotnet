# Zernio.Model.AnalyticsListResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Overview** | [**AnalyticsOverview**](AnalyticsOverview.md) |  | [optional] 
**Posts** | [**List&lt;AnalyticsListResponsePostsInner&gt;**](AnalyticsListResponsePostsInner.md) |  | [optional] 
**Pagination** | [**Pagination**](Pagination.md) |  | [optional] 
**Accounts** | [**List&lt;SocialAccount&gt;**](SocialAccount.md) | Connected accounts (followerCount and followersLastUpdated only included if user has analytics add-on) | [optional] 
**HasAnalyticsAccess** | **bool** | Whether user has analytics add-on access | [optional] 
**AnalyticsOff** | [**List&lt;AnalyticsOffAccount&gt;**](AnalyticsOffAccount.md) | The X accounts this list covers (after its platform, profile and account filters) whose analytics sync does not run: their numbers stay as of the last read. Also sent with &#x60;view&#x3D;summary&#x60;. Absent when there are none. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

