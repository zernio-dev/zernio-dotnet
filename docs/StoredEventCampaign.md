# Zernio.Model.StoredEventCampaign
The campaign behind the event and how Zernio knows it, with the names Zernio holds for its campaign, ad group or ad set and ad. `null` when nothing ties the event to a campaign; a Google click shows here the day after it, once Google reports it.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Via** | **string** | &#x60;google_click&#x60;: the click behind &#x60;clickIds.gclid&#x60;. &#x60;zernio_tag&#x60;: the &#x60;zrn&#x60; ad. &#x60;matched&#x60;: the campaign Zernio matched the event to. &#x60;utm&#x60;: only its &#x60;utm_campaign&#x60;, as &#x60;name&#x60;. | [optional] 
**Id** | **string** | The ad platform campaign id; &#x60;null&#x60; for &#x60;utm&#x60;. | [optional] 
**Name** | **string** |  | [optional] 
**AdGroupName** | **string** | The Google ad group or Meta ad set. | [optional] 
**AdName** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

