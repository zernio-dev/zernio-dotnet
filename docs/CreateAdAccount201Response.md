# Zernio.Model.CreateAdAccount201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdAccountId** | **string** | New Meta ad account ID for subsequent ads calls. | 
**BusinessId** | **string** | Owning business portfolio ID. | 
**ConnectionUpdated** | **bool** | Whether the connection scope and discovery schedule were updated. | 
**PaymentMethodRequired** | **bool** | Always true as a delivery prerequisite. This is not a live funding-source check. Confirm payment or invoicing in Ads Manager. | 
**AdsManagerUrl** | **string** | Open the created account in Ads Manager. | 
**NextSteps** | **string** | Payment setup instructions for the user. | 
**Warnings** | **List&lt;string&gt;** | Recovery instructions if the account could not be attached to the connection. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

