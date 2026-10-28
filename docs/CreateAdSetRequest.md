# Zernio.Model.CreateAdSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id owning the Google Ads or Reddit Ads connection. | 
**Platform** | **string** | \&quot;google\&quot; and \&quot;reddit\&quot; are implemented; every other value returns 501. | 
**CampaignId** | **string** | Platform campaign ID the ad group is created under (numeric on Google). | 
**Name** | **string** |  | 
**Status** | **string** |  | [optional] [default to StatusEnum.PAUSED]
**MaxCpc** | **decimal** | Max CPC of the new ad group, in the account&#39;s currency units. Send it when the campaign uses Manual CPC: Google gives an ad group without one a 0.01 bid. | [optional] 
**AdAccountId** | **string** | Platform ad account ID: the Google customer ID (digits only, only required when the connection has more than one) or the Reddit ad account id (required). | [optional] 
**CustomerId** | **string** | Google only. Alias of adAccountId, kept for existing callers | [optional] 
**BudgetAmount** | **decimal** | Reddit only. Budget of the new ad group, in the ad account&#39;s currency units. Required when the campaign has no campaign budget; 400 under campaign budget optimization, where the campaign budget funds the ad group. | [optional] 
**BudgetType** | **string** | Reddit only. Sent together with budgetAmount. | [optional] 
**StartDate** | **string** | Reddit only. ISO 8601 start of the ad group. Defaults to now, or to the campaign start when it is in the future. | [optional] 
**EndDate** | **string** | Reddit only. ISO 8601 end of the ad group. Defaults to the campaign end. | [optional] 
**Targeting** | [**TargetingSpec**](TargetingSpec.md) |  | [optional] 
**PromotedObject** | [**CreateAdSetRequestPromotedObject**](CreateAdSetRequestPromotedObject.md) |  | [optional] 
**OptimizationGoal** | **string** | Reddit only. VIDEO_VIEW_6S (default) or VIDEO_VIEW_15S on a video views campaign. | [optional] 
**BidStrategy** | **string** | Reddit only. Defaults to LOWEST_COST_WITHOUT_CAP. Not accepted under campaign budget optimization. | [optional] 
**BidAmount** | **decimal** | Reddit only. Bid cap in currency units, sent with bidStrategy. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

