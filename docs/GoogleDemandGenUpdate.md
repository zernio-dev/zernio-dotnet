# Zernio.Model.GoogleDemandGenUpdate
Partial edit of a Google Demand Gen ad, sent in one atomic Google request. Every field you send replaces that whole field; fields you omit are kept. Which creative fields apply depends on the ad (read from Google): image ads take headlines, descriptions, businessName, callToAction and images (landscape, square, portrait, logo); video ads take headlines, longHeadlines, descriptions, businessName, youtubeVideoIds and exactly one images.logo; carousel ads take exactly one headline, one description, one logo, businessName and callToAction (their cards cannot be edited: create a new carousel ad). A field the ad does not take returns 422. New images are uploaded as new Google assets; the previous ones stay in the account's asset library.  `channels`, `audience` and `audienceId` change the ad's ad group, so they apply to every ad in it. `audience` builds a new Google Audience and attaches it in place of the current one (the previous audience is detached, not deleted); `audienceId` attaches an existing one. Ad groups of campaigns migrated from Discovery use ungrouped audience segments, and Google refuses an Audience on them. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FinalUrl** | **string** |  | [optional] 
**BusinessName** | **string** |  | [optional] 
**Headlines** | **List&lt;string&gt;** |  | [optional] 
**LongHeadlines** | **List&lt;string&gt;** | Video ads only. | [optional] 
**Descriptions** | **List&lt;string&gt;** |  | [optional] 
**CallToAction** | **string** | Image and carousel ads only. | [optional] 
**Images** | [**GoogleDemandGenUpdateImages**](GoogleDemandGenUpdateImages.md) |  | [optional] 
**YoutubeVideoIds** | **List&lt;string&gt;** | Video ads only. | [optional] 
**Channels** | **List&lt;GoogleDemandGenUpdate.ChannelsEnum&gt;** | Replaces the ad group&#39;s channel controls; only the listed channels serve. | [optional] 
**Audience** | [**GoogleDemandGenAudience**](GoogleDemandGenAudience.md) |  | [optional] 
**AudienceId** | **string** | Attach an existing Google Audience by numeric id instead of audience. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

