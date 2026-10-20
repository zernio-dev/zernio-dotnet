# Zernio.Model.CreatedGoogleAdAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**AdAccountId** | **string** | New Google Ads customer id for subsequent ads calls. | 
**ManagerCustomerId** | **string** | Manager the account was created under. | 
**ConnectionUpdated** | **bool** | Whether the customer was added to the connection and discovery was scheduled. When false the account exists: reconnect Google Ads instead of creating it again. | 
**Warnings** | **List&lt;string&gt;** | Recovery instructions if the account could not be attached to the connection. | 
**PaymentMethodRequired** | **bool** | Always true. The account has no billing until it is set up in Google Ads. | 
**NextSteps** | **string** | Billing setup instructions for the user. | 
**ValidateOnly** | **bool** | Always false on a 201. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

