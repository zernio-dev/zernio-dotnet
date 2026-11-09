# Zernio.Model.GetPageWebhookSubscription200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PageId** | **string** |  | [optional] 
**AppSubscribed** | **bool** | False when the Page carries no subscription for our app at all. | [optional] 
**Leadgen** | **bool** | Whether lead ads submitted on this Page reach Zernio in real time. | [optional] 
**SubscribedFields** | **List&lt;string&gt;** |  | [optional] 
**Warning** | **string** | Present only when leadgen is missing. | [optional] 
**InstagramUserId** | **string** | Instagram accounts only. | [optional] 
**SubscriptionId** | **string** | Instagram accounts only. Id of the subscription record on Meta; null when there is none. | [optional] 
**MissingFields** | **List&lt;string&gt;** | Instagram accounts only. Webhook fields Zernio expects that Meta did not subscribe. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

