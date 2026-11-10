# Zernio.Model.LaunchCampaignAdsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SubmissionIds** | **List&lt;string&gt;** | Approved submissions to run as ads. | 
**Network** | **string** | Meta runs Instagram and Facebook posts; TikTok runs TikTok posts. | 
**AccountId** | **string** | The brand&#39;s connected ads account (Facebook or TikTok) the ads run from, as in &#x60;/v1/accounts&#x60;. | 
**AdAccountId** | **string** | Platform ad account ID. | 
**AdSetId** | **string** | Existing Meta ad set the ads go into. Required when &#x60;network&#x60; is &#x60;meta&#x60;. | [optional] 
**ExistingCampaignId** | **string** | Existing TikTok campaign that gets one ad group per post. Required when &#x60;network&#x60; is &#x60;tiktok&#x60;. | [optional] 
**DailyBudget** | **decimal** | Daily budget of each TikTok ad group, in the ad account currency. Required when &#x60;network&#x60; is &#x60;tiktok&#x60;. | [optional] 
**Identity** | **string** | Whose handle the ad runs under. TikTok takes &#x60;creator&#x60; only. | 
**Body** | **string** | Primary text of brand ads. Defaults to the post caption. | [optional] 
**Headline** | **string** |  | [optional] 
**CallToAction** | **string** | Call to action, as in &#x60;POST /v1/ads/create&#x60;. | [optional] 
**LinkUrl** | **string** | Destination URL (http or https). | [optional] 
**Status** | **string** | Ads launch paused unless set to &#x60;ACTIVE&#x60;. | [optional] [default to StatusEnum.PAUSED]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

