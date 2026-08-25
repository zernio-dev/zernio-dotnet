# Zernio.Model.SendInboxMessageRequestInteractiveActionOneOf10Parameters

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Country** | **string** | ISO 3166-1 alpha-2 country code Meta should localize the address form for (e.g. IN). Required: Meta rejects the send without it. | 
**Values** | **Dictionary&lt;string, Object&gt;** | Optional pre-filled address field values. | [optional] 
**SavedAddresses** | **List&lt;Dictionary&lt;string, Object&gt;&gt;** | Optional list of the recipient&#39;s previously saved addresses to offer as quick picks. | [optional] 
**ValidationErrors** | **Dictionary&lt;string, string&gt;** | Optional per-field error messages to show when re-prompting after a failed validation. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

