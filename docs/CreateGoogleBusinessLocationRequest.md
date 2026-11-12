# Zernio.Model.CreateGoogleBusinessLocationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** | Business name as shown on Google. | 
**LanguageCode** | **string** | BCP-47 language of the listing (e.g. \&quot;es\&quot;). Immutable after creation. | 
**PrimaryCategory** | **string** | Category name from GET gmb-categories (e.g. \&quot;categories/gcid:cafe\&quot;). A bare \&quot;gcid:cafe\&quot; is also accepted. | 
**AdditionalCategories** | **List&lt;string&gt;** | Further category names, same format as primaryCategory. | [optional] 
**StorefrontAddress** | [**CreateGoogleBusinessLocationRequestStorefrontAddress**](CreateGoogleBusinessLocationRequestStorefrontAddress.md) |  | [optional] 
**ServiceArea** | [**CreateGoogleBusinessLocationRequestServiceArea**](CreateGoogleBusinessLocationRequestServiceArea.md) |  | [optional] 
**Phone** | **string** | Primary phone number. Required when storefrontAddress is absent and websiteUri is not set. | [optional] 
**WebsiteUri** | **string** | Website URL. Required when storefrontAddress is absent and phone is not set. | [optional] 
**Description** | **string** | Business description (Google profile.description). | [optional] 
**RegularHours** | **Dictionary&lt;string, Object&gt;** | Google &#x60;regularHours&#x60; object (periods with openDay, openTime, closeDay, closeTime). | [optional] 
**ValidateOnly** | **bool** | Validate with Google without creating the listing or attaching anything. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

