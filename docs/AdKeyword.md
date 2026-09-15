# Zernio.Model.AdKeyword

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**AccountId** | **string** | Account ID owning the sync | [optional] 
**ProfileId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**AdAccountId** | **string** | Google customer ID | [optional] 
**CampaignId** | **string** |  | [optional] 
**CampaignName** | **string** |  | [optional] 
**CampaignStatus** | **string** |  | [optional] 
**AdSetId** | **string** | Google ad group ID | [optional] 
**AdSetName** | **string** |  | [optional] 
**AdSetStatus** | **string** |  | [optional] 
**Keyword** | **string** |  | [optional] 
**MatchType** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**Negative** | **bool** |  | [optional] 
**QualityScore** | **int?** | Deprecated, use &#x60;quality.score&#x60;. Google Quality Score, 1-10. Null when unrated. | [optional] 
**Quality** | [**AdKeywordQuality**](AdKeywordQuality.md) |  | [optional] 
**SyncedAt** | **DateTime?** |  | [optional] 
**Metrics** | [**AdKeywordMetrics**](AdKeywordMetrics.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

