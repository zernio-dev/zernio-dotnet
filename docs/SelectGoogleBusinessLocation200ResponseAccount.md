# Zernio.Model.SelectGoogleBusinessLocation200ResponseAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | ID of the created SocialAccount | [optional] 
**Platform** | **string** |  | [optional] 
**Username** | **string** |  | [optional] 
**DisplayName** | **string** |  | [optional] 
**IsActive** | **bool** |  | [optional] 
**SelectedLocationName** | **string** | Human-readable location display name, NOT a resource name. Do not use it to build API paths. Null when connected with no location. | [optional] 
**SelectedLocationId** | **string** | Bare Google Business Profile location id. Combine with the Google Business Profile account id as accounts/{gbpAccountId}/locations/{selectedLocationId} to form the location resource names that gmb-reviews/batch expects in locationNames. Null when connected with no location. | [optional] 
**NeedsLocation** | **bool** | Present and true when the account was connected with no location (allowNoLocation&#x3D;true). Create one with POST /v1/accounts/{accountId}/gmb-locations before using the location endpoints. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

