# Zernio.Model.ListEvents200ResponseEventsInnerAd
The ad behind the event, when Zernio can name it. Google: from the click behind `clickIds.gclid` (synced daily from Google Ads click_view for clicks up to 14 days before the event; gbraid/wbraid clicks are not resolved). Meta: from the `zrn` ad id, for Meta ads Zernio holds. `null` otherwise.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | [optional] 
**CustomerId** | **string** | Google Ads customer id (Google only). | [optional] 
**CampaignId** | **string** |  | [optional] 
**AdGroupId** | **string** | Google only. | [optional] 
**AdSetId** | **string** | Meta only. | [optional] 
**AdId** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

