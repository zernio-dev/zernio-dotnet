# Zernio.Model.ListSmsRegistrations200ResponseRegistrationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**RegistrationType** | **string** |  | [optional] 
**DisplayName** | **string** |  | [optional] 
**Status** | **string** | requested/changes_requested &#x3D; pre-submission review states; customers see them as pending / needs changes. | [optional] 
**BrandStatus** | **string** | Carrier-registry brand status (e.g. VERIFIED). | [optional] 
**CampaignStatus** | **string** |  | [optional] 
**BrandId** | **string** | TCR brand id, useful when referencing the brand in carrier support threads. | [optional] 
**CampaignId** | **string** | TCR campaign id. | [optional] 
**DeclineReason** | **string** |  | [optional] 
**PhoneNumbers** | **List&lt;string&gt;** |  | [optional] 
**AwaitingOtp** | **bool** | Sole-prop 10DLC only; the OTP step is still pending. | [optional] 
**TrustScore** | **decimal?** | Carrier-assigned brand trust score; drives throughput. | [optional] 
**Throughput** | [**ListSmsRegistrations200ResponseRegistrationsInnerThroughput**](ListSmsRegistrations200ResponseRegistrationsInnerThroughput.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

