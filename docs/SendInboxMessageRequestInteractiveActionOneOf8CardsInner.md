# Zernio.Model.SendInboxMessageRequestInteractiveActionOneOf8CardsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CardIndex** | **int** | Card position. Auto-filled sequentially when omitted. | [optional] 
**Type** | **string** | &#x60;product&#x60; for a product card; media cards use &#x60;cta_url&#x60; or a quick-reply type. | [optional] 
**Header** | **Object** | Media cards only, required. Carries the card&#39;s image or video. | [optional] 
**Body** | **Object** | Optional card body text. | [optional] 
**Action** | **Object** | Product cards: &#x60;{ catalog_id, product_retailer_id }&#x60; (required). Media cards: the card&#39;s button action (e.g. &#x60;cta_url&#x60; with &#x60;parameters.display_text&#x60; and &#x60;parameters.url&#x60;). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

