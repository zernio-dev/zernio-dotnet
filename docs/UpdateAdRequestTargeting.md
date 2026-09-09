# Zernio.Model.UpdateAdRequestTargeting
Meta + TikTok (demographics/interests), Google (keyword and device bid adjustment edits only), and LinkedIn (countries or regions required). Pinterest / X return 501. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Keywords** | [**List&lt;UpdateAdRequestTargetingKeywordsInner&gt;**](UpdateAdRequestTargetingKeywordsInner.md) | Google only. The FULL desired set of positive keywords for the entire ad group. Omit to leave positives unchanged; [] removes all positives. Negatives are independent. Entries are strings (BROAD) or { text, matchType } with matchType exact | phrase | broad; an omitted matchType also defaults to BROAD. Matching case-insensitive text AND match type retains the existing criterion ID, status, bid overrides, labels and history without a mutation. A changed text or match type uses remove/create, without transferring the old criterion&#39;s attributes or history. See Google keyword replacement above for an EXACT-to-BROAD example. Mirrored to GET /v1/ads/keywords immediately.  | [optional] 
**NegativeKeywords** | [**List&lt;UpdateAdRequestTargetingKeywordsInner&gt;**](UpdateAdRequestTargetingKeywordsInner.md) | Google only. The FULL desired set of negative keywords for the entire ad group, independent of positives. Omit to leave negatives unchanged; [] removes all negatives. Uses the same text/match-type identity and preservation contract as keywords above. Strings and objects without matchType default to BROAD, so resending an EXACT or PHRASE negative as a bare string requests a different criterion. Campaign negatives are separate: use /v1/ads/campaigns/{campaignId}/negative-keywords to manage those.  | [optional] 
**Devices** | [**List&lt;UpdateAdRequestTargetingDevicesInner&gt;**](UpdateAdRequestTargetingDevicesInner.md) | Google only. The FULL new set of device criteria for the campaign; devices not listed are excluded. Entries are a device name alone (included, no bid adjustment) or { device, bidModifier }. | [optional] 
**AgeMin** | **int** |  | [optional] 
**AgeMax** | **int** |  | [optional] 
**Countries** | **List&lt;string&gt;** |  | [optional] 
**Interests** | [**List&lt;UpdateAdRequestTargetingInterestsInner&gt;**](UpdateAdRequestTargetingInterestsInner.md) | Interest objects from /v1/ads/interests. Each must include id and name. | [optional] 
**AdvantageAudience** | **int** | Meta only. Omit to preserve the existing setting on update. 0 &#x3D; disabled, 1 &#x3D; enabled. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

