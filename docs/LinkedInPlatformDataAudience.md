# Zernio.Model.LinkedInPlatformDataAudience
Organization pages only. Audience targeting for the post (Ads Manager's \"Targeted audience\"), sent as LinkedIn's distribution.targetEntities: OR inside a facet, AND across facets. LinkedIn rejects the post when the targeted audience is under 300 members, and Zernio rejects it on a personal profile. URN facets accept a full urn:li:<type>:<id> or the bare numeric id; find ids with GET /v1/ads/targeting/search?platform=linkedin (types country, region, industry, jobFunction, seniority, companySize).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Countries** | **List&lt;string&gt;** | ISO 3166-1 alpha-2 codes with a built-in LinkedIn geo URN (same list as geoRestriction.countries, merged with it). Other countries and sub-country regions go in geoLocations. | [optional] 
**GeoLocations** | **List&lt;string&gt;** | LinkedIn geo URNs or ids (urn:li:geo:103644278 or 103644278): countries, states, regions, cities. | [optional] 
**InterfaceLocales** | [**List&lt;LinkedInPlatformDataAudienceInterfaceLocalesInner&gt;**](LinkedInPlatformDataAudienceInterfaceLocalesInner.md) | Members&#39; LinkedIn interface locale, e.g. { language: es, country: ES }. | [optional] 
**Industries** | **List&lt;string&gt;** | urn:li:industry:&lt;id&gt; or id. | [optional] 
**JobFunctions** | **List&lt;string&gt;** | urn:li:function:&lt;id&gt; or id. | [optional] 
**Seniorities** | **List&lt;string&gt;** | urn:li:seniority:&lt;id&gt; or id. | [optional] 
**StaffCountRanges** | **List&lt;LinkedInPlatformDataAudience.StaffCountRangesEnum&gt;** | Company size of the member&#39;s current employer. | [optional] 
**Degrees** | **List&lt;string&gt;** | urn:li:degree:&lt;id&gt; or id (LinkedIn standardized degrees). | [optional] 
**FieldsOfStudy** | **List&lt;string&gt;** | urn:li:fieldOfStudy:&lt;id&gt; or id (LinkedIn standardized fields of study). | [optional] 
**Organizations** | **List&lt;string&gt;** | Schools, as urn:li:organization:&lt;id&gt; or id (LinkedIn&#39;s Organization Lookup). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

