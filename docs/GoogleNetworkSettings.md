# Zernio.Model.GoogleNetworkSettings
Google Search campaigns only. Which networks the campaign serves on besides Google Search. When omitted at creation, search partners are ON and the Display Network is OFF (the defaults Zernio has always used); on an update only the fields sent change.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SearchPartners** | **bool** | campaign.network_settings.target_search_network | [optional] 
**DisplayNetwork** | **bool** | campaign.network_settings.target_content_network (Search with Display expansion) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

