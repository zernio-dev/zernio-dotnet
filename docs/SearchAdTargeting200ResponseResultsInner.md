# Zernio.Model.SearchAdTargeting200ResponseResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The platform&#39;s opaque id. Use as a geo &#x60;key&#x60; (regions/cities/zips/metros) or an entity &#x60;id&#x60; (interests/behaviors) in TargetingSpec. | 
**Name** | **string** | Human-readable label. | 
**Type** | **string** | What the result is (e.g. city, region, country, zip, metro, interest, behavior, income). | 
**Path** | **List&lt;string&gt;** | Optional breadcrumb of parent labels (e.g. [&#39;United States&#39;, &#39;California&#39;, &#39;Los Angeles&#39;]). Disambiguates same-named results. | [optional] 
**AudienceSize** | **int?** | Optional estimated reachable users for this option, when the platform returns it. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

