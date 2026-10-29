# Zernio.Model.BoostPost201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ad** | [**Ad**](Ad.md) |  | [optional] 
**Message** | **string** |  | [optional] 
**InstagramVideoFallback** | [**InstagramVideoFallback**](InstagramVideoFallback.md) |  | [optional] 
**Warnings** | **List&lt;string&gt;** | Human-readable notes about the boost.  - **With instagramVideoFallback:** one line saying how the Instagram video was boosted. - **&#x60;activation_failed:&#x60; (Meta):** Meta refused the final switch to ACTIVE of the campaign, ad set or ad this boost created. Nothing was deleted and &#x60;message&#x60; says not everything is ACTIVE. - **&#x60;activation_failed:&#x60; content:** names what was kept PAUSED and what was switched ACTIVE, and quotes Meta&#39;s error and the status calls that switch the PAUSED ones on later. - **&#x60;replayed_paused:&#x60;:** a retry without Idempotency-Key inside the 10-minute dedup window found the stored ad PAUSED although it asks for ACTIVE. Carries the same status calls.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

