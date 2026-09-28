# Zernio.Model.TrackingTagDiagnostic
One health check the platform runs on a tracking tag.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Key** | **string** | Platform check id (Meta: e.g. &#x60;pixel_missing_param_in_events&#x60;). | 
**Title** | **string** |  | 
**Description** | **string** |  | [optional] 
**Result** | **string** | The platform verdict (Meta: &#x60;passed&#x60;, &#x60;failed&#x60;, &#x60;warning&#x60;). | 
**ActionUrl** | **string** | Where to fix it in the platform UI (Meta: Events Manager). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

