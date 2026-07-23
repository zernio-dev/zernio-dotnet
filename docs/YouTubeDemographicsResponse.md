# Zernio.Model.YouTubeDemographicsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Success** | **bool** |  | [optional] 
**AccountId** | **string** | The Zernio SocialAccount ID | [optional] 
**Platform** | **string** |  | [optional] 
**VideoId** | **string** | Present only when demographics are scoped to a single video | [optional] 
**Title** | **string** | Video title (video mode only) | [optional] 
**PublishedAt** | **DateTime?** | Video publish date (video mode only) | [optional] 
**Demographics** | **Dictionary&lt;string, List&lt;YouTubeDemographicsResponseDemographicsValueInner&gt;&gt;** | Object keyed by breakdown dimension (age, gender, country) | [optional] 
**DateRange** | [**YouTubeDemographicsResponseDateRange**](YouTubeDemographicsResponseDateRange.md) |  | [optional] 
**ProvisionalSince** | **DateOnly** | Present only when the range reaches into YouTube&#39;s ~3-day processing window: the first date whose numbers are provisional and may still be revised by YouTube. | [optional] 
**Note** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

