# Zernio.Model.StartSmsRegistrationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RegistrationType** | **string** |  | 
**PhoneNumbers** | **List&lt;string&gt;** | Your numbers this registration covers. | 
**Brand** | [**StartSmsRegistrationRequestBrand**](StartSmsRegistrationRequestBrand.md) |  | [optional] 
**Campaign** | [**StartSmsRegistrationRequestCampaign**](StartSmsRegistrationRequestCampaign.md) |  | [optional] 
**WizardValues** | **Dictionary&lt;string, string&gt;** | Raw dashboard-wizard answers, stored only to prefill edit-and-resubmit. API integrators can omit. | [optional] 
**ResubmitRequestId** | **string** | Resubmit a registration that was returned for changes — updates it in place instead of creating a new one. | [optional] 
**TollFree** | [**StartSmsRegistrationRequestTollFree**](StartSmsRegistrationRequestTollFree.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

