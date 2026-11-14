# Zernio.Model.ConnectLineCredentials200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Message** | **string** |  | [optional] 
**Account** | [**ConnectedMessagingAccount**](ConnectedMessagingAccount.md) |  | [optional] 
**Webhook** | [**ConnectLineCredentials200ResponseWebhook**](ConnectLineCredentials200ResponseWebhook.md) |  | [optional] 
**NextSteps** | **List&lt;string&gt;** | Settings the account owner still has to change in LINE Official Account Manager. Led by the turn-on-Webhooks step when &#x60;webhook.active&#x60; is &#x60;false&#x60;, then by a warning when &#x60;webhook.previousUrl&#x60; is set. The turn-on-Webhooks step is left out when &#x60;webhook.active&#x60; is &#x60;true&#x60;. | [optional] 
**RedirectUrl** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

