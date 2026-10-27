# Zernio.Model.AdLeadConsent
One custom disclaimer checkbox on a Meta lead form (for example a TCPA call or SMS consent), as Meta returns it in custom_disclaimer_responses.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CheckboxKey** | **string** | The checkbox key as Meta returns it: the one set in platformSpecificData.customDisclaimer.checkboxes[].key on POST /v1/ads/lead-forms, or otherwise a key Meta derives from the checkbox text, which can be long and contain spaces and punctuation. | 
**IsChecked** | **bool** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

