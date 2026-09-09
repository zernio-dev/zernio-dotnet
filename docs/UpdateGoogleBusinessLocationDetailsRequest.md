# Zernio.Model.UpdateGoogleBusinessLocationDetailsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UpdateMask** | **string** | Required. Comma-separated fields to update (e.g. &#39;regularHours&#39;, &#39;specialHours&#39;, &#39;profile.description&#39;, &#39;categories&#39;, &#39;serviceItems&#39;). Any valid Google Business Information API updateMask field is supported. | 
**RegularHours** | [**UpdateGoogleBusinessLocationDetailsRequestRegularHours**](UpdateGoogleBusinessLocationDetailsRequestRegularHours.md) |  | [optional] 
**SpecialHours** | [**GetGoogleBusinessLocationDetails200ResponseSpecialHours**](GetGoogleBusinessLocationDetails200ResponseSpecialHours.md) |  | [optional] 
**Profile** | [**UpdateGoogleBusinessLocationDetailsRequestProfile**](UpdateGoogleBusinessLocationDetailsRequestProfile.md) |  | [optional] 
**WebsiteUri** | **string** |  | [optional] 
**PhoneNumbers** | [**GetGoogleBusinessLocationDetails200ResponsePhoneNumbers**](GetGoogleBusinessLocationDetails200ResponsePhoneNumbers.md) |  | [optional] 
**Categories** | [**UpdateGoogleBusinessLocationDetailsRequestCategories**](UpdateGoogleBusinessLocationDetailsRequestCategories.md) |  | [optional] 
**ServiceItems** | [**List&lt;UpdateGoogleBusinessLocationDetailsRequestServiceItemsInner&gt;**](UpdateGoogleBusinessLocationDetailsRequestServiceItemsInner.md) | Services offered by the business. Use updateMask&#x3D;&#39;serviceItems&#39; to update. | [optional] 
**Title** | **string** | Business name. Use updateMask&#x3D;&#39;title&#39;. | [optional] 
**StoreCode** | **string** | External store identifier, unique within the account. Use updateMask&#x3D;&#39;storeCode&#39;. | [optional] 
**Labels** | **List&lt;string&gt;** | Free-form, internal-only labels for grouping (1-255 characters each). Use updateMask&#x3D;&#39;labels&#39;. | [optional] 
**StorefrontAddress** | [**UpdateGoogleBusinessLocationDetailsRequestStorefrontAddress**](UpdateGoogleBusinessLocationDetailsRequestStorefrontAddress.md) |  | [optional] 
**ServiceArea** | [**UpdateGoogleBusinessLocationDetailsRequestServiceArea**](UpdateGoogleBusinessLocationDetailsRequestServiceArea.md) |  | [optional] 
**OpenInfo** | [**UpdateGoogleBusinessLocationDetailsRequestOpenInfo**](UpdateGoogleBusinessLocationDetailsRequestOpenInfo.md) |  | [optional] 
**MoreHours** | [**List&lt;UpdateGoogleBusinessLocationDetailsRequestMoreHoursInner&gt;**](UpdateGoogleBusinessLocationDetailsRequestMoreHoursInner.md) | Additional hours for specific services (delivery, drive-through, etc.). Use updateMask&#x3D;&#39;moreHours&#39;. | [optional] 
**Latlng** | [**UpdateGoogleBusinessLocationDetailsRequestLatlng**](UpdateGoogleBusinessLocationDetailsRequestLatlng.md) |  | [optional] 
**AdWordsLocationExtensions** | [**UpdateGoogleBusinessLocationDetailsRequestAdWordsLocationExtensions**](UpdateGoogleBusinessLocationDetailsRequestAdWordsLocationExtensions.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

