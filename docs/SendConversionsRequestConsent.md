# Zernio.Model.SendConversionsRequestConsent
Batch-level user consent. Required by Google for EEA/UK events under the Feb 2026 restrictions.  - **Meta:** any DENIED flag enables Limited Data Use on every event in the batch (data_processing_options [\"LDU\"] with geolocation, country 0 / state 0). GRANTED or absent consent sends events with Meta's default processing. - **Reddit:** `adUserData: DENIED` drops every user field from the events. - **LinkedIn:** ignored. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdUserData** | **string** |  | [optional] 
**AdPersonalization** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

