# Zernio.Model.GoogleDemandGenInput
Creative, channel and audience settings for a Google Demand Gen campaign (campaignType demand_gen). Creates one ad group with one ad: a multi-asset image ad, or a video responsive ad when youtubeVideoIds is sent.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdGroupName** | **string** | Defaults to the ad name. | [optional] 
**FinalUrl** | **string** |  | 
**BusinessName** | **string** |  | 
**Headlines** | **List&lt;string&gt;** | Distinct texts. | 
**LongHeadlines** | **List&lt;string&gt;** | Video ads only, and required there. | [optional] 
**Descriptions** | **List&lt;string&gt;** |  | 
**CallToAction** | **string** | Image ads only. Call to action text such as &#39;Learn more&#39;; Google picks one when omitted. | [optional] 
**Images** | [**GoogleDemandGenInputImages**](GoogleDemandGenInputImages.md) |  | 
**YoutubeVideoIds** | **List&lt;string&gt;** | Makes the ad a video responsive ad. | [optional] 
**Channels** | **List&lt;GoogleDemandGenInput.ChannelsEnum&gt;** | Channel controls on the ad group. Only the listed channels serve; omit to serve on all of them. | [optional] 
**Audience** | [**GoogleDemandGenInputAudience**](GoogleDemandGenInputAudience.md) |  | [optional] 
**AudienceId** | **string** | Attach an existing Google Audience by numeric id instead of audience. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

