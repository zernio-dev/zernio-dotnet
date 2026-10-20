# Zernio.Model.CreateAdAccount201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdAccountId** | **string** | New Google Ads customer id for subsequent ads calls. | 
**BusinessId** | **string** | Owning business portfolio ID. | 
**ConnectionUpdated** | **bool** | Whether the customer was added to the connection and discovery was scheduled. When false the account exists: reconnect Google Ads instead of creating it again. | 
**PaymentMethodRequired** | **bool** | Always true. The account has no billing until it is set up in Google Ads. | 
**AdsManagerUrl** | **string** | Open the created account in Ads Manager. | 
**NextSteps** | **string** | Billing setup instructions for the user. | 
**Warnings** | **List&lt;string&gt;** | Recovery instructions if the account could not be attached to the connection. | 
**Platform** | **string** |  | 
**ManagerCustomerId** | **string** | Manager the account was created under. | 
**ValidateOnly** | **bool** | Always false on a 201. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

