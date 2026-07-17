# Zernio.Model.AssignGoogleBusinessLocationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** | Target profile to connect the location onto. | 
**SelectedLocationId** | **string** | The Google Business location ID to assign (e.g. \&quot;locations/123\&quot;). | 
**GoogleAccountId** | **string** | Optional but recommended. The Google Business Account resource name (\&quot;accounts/123\&quot;) that owns the location (from GET gmb-locations). When provided the location is resolved directly instead of by enumerating the account, required for accounts with many locations.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

