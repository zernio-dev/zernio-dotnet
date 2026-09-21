# Zernio.Model.ListAdSets200ResponseAdSetsInnerTargeting
The audience this ad set delivers to, as the platform reports it. LinkedIn only today; null for every other platform and for LinkedIn ad sets not yet re-synced.  `include` and `exclude` are the campaign's `targetingCriteria` verbatim, so they can be read, edited and sent back without reconstructing them from our normalized targeting spec. Exclusions were previously not readable at all. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Include** | **Object** | LinkedIn &#x60;targetingCriteria.include&#x60;, verbatim (an &#x60;and&#x60; of &#x60;or&#x60; facet clauses). | [optional] 
**Exclude** | **Object** | LinkedIn &#x60;targetingCriteria.exclude&#x60;, verbatim. Absent when the campaign excludes nothing. | [optional] 
**AudienceExpansionEnabled** | **bool** | LinkedIn audience expansion: whether LinkedIn may also serve to members similar to the criteria. | [optional] 
**OffsiteDeliveryEnabled** | **bool** | Whether the campaign may deliver on the LinkedIn Audience Network, off LinkedIn itself. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

