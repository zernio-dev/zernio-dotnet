# Zernio.Model.AutomationBoostStep
Promotes each matched Facebook or Instagram post once, as a Meta ad with a lifetime budget. Posts on other platforms are not boosted. It needs the Ads add-on.  One boost step per automation, and `limits.maxChangesPerDay` (up to 20) is required: the most posts boosted in a day. At most 5 posts are boosted per check. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Type** | **string** |  | 
**AdAccountId** | **string** | The Meta ad account that pays, from &#x60;GET /v1/ads/accounts&#x60;. | 
**Budget** | **decimal** | The whole spend of one boost, in the ad account currency. | 
**Days** | **int** | How long each boost runs. | 
**Goal** | **string** |  | [optional] [default to GoalEnum.Engagement]
**Countries** | **List&lt;string&gt;** | ISO 3166 alpha-2 codes. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

