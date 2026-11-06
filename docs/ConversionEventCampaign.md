# Zernio.Model.ConversionEventCampaign
The ad campaign behind the event, when you know it. Read only by `POST /v1/events`, which ties the event to the campaign named by `campaign.id`, then by the `utm_campaign` of `sourceUrl`, then by `campaign.name`. See its Storage notes for how the event then counts.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform campaign ID. | [optional] 
**Name** | **string** | Campaign name as it appears on the ad platform (case-insensitive). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

