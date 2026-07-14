# Zernio.Model.CreateAdAudienceRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Social account ID on the target ad platform. | 
**AdAccountId** | **string** | Platform ad account ID. Must start with act_ for Meta; bare platform id for others (Google customer id, X/TikTok/LinkedIn/Pinterest account id). | 
**Name** | **string** |  | 
**Description** | **string** |  | [optional] 
**Type** | **string** |  | 
**SourceType** | **string** | Required for engagement audiences (LinkedIn only): what members engaged with — a video/leadgen/single-image ad campaign, a Company Page or an Event page.  | [optional] 
**Trigger** | **string** | Required for engagement audiences. The action, validated by LinkedIn against &#x60;sourceType&#x60;. Common values: VIDEO_ADS FIRST_QUARTILE / MIDPOINT / THIRD_QUARTILE / FULL_COMPLETE; LEAD_GEN_FORMS VIEW_FORM / LEAD_FORM_SUBMIT; ORGANIZATION_PAGES VIEW / CTA_CLICK; EVENT_PAGES RSVPED / VIDEO_VIEWED / ENGAGEMENT / CLICK.  | [optional] 
**LookbackDays** | **int** | Required for engagement audiences. Rolling window. | [optional] 
**EngagementSources** | **List&lt;string&gt;** | Required for engagement audiences. Campaign URNs for the ad source types, organization URNs for pages and events. LinkedIn creates one rule per source, all sharing the same trigger and lookbackDays.  | [optional] 
**Companies** | [**List&lt;UploadedOrDerivedAudienceCompaniesInner&gt;**](UploadedOrDerivedAudienceCompaniesInner.md) | Required for company_list audiences (LinkedIn only): plain-text company rows for account targeting. Each row needs at least one identifier. LinkedIn recommends 1,000+ companies for a usable match rate and takes up to 48h to process the list.  | [optional] 
**PixelId** | **string** | Required for website audiences | [optional] 
**RetentionDays** | **int** | Required for website audiences | [optional] 
**SourceAudienceId** | **string** | Required for lookalike audiences | [optional] 
**Country** | **string** | 2-letter code, required for lookalike audiences | [optional] 
**Ratio** | **decimal** | Required for lookalike audiences | [optional] 
**Rule** | **Object** | Pixel event rule for website audiences (optional) | [optional] 
**CustomerFileSource** | **string** | Data source declaration for GDPR compliance (customer_list only) | [optional] 
**Spec** | [**TargetingSpec**](TargetingSpec.md) | The targeting spec to store. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

