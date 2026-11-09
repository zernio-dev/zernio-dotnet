# Zernio.Model.ResyncPageWebhookSubscription200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Resubscribed** | **bool** |  | [optional] 
**PageId** | **string** |  | [optional] 
**AppSubscribed** | **bool** |  | [optional] 
**Leadgen** | **bool** |  | [optional] 
**SubscribedFields** | **List&lt;string&gt;** |  | [optional] 
**Warning** | **string** |  | [optional] 
**InstagramUserId** | **string** | Instagram accounts only. | [optional] 
**SubscriptionId** | **string** | Instagram accounts only. Id of the subscription record after the repair. | [optional] 
**PreviousSubscriptionId** | **string** | Instagram accounts only. Id of the record before the repair; null when there was none. | [optional] 
**Recreated** | **bool** | Instagram accounts only. True when the subscription record id changed. | [optional] 
**MissingFields** | **List&lt;string&gt;** | Instagram accounts only. Webhook fields Zernio expects that Meta did not subscribe. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

