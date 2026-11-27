# Zernio.Model.AssignAdAccountUserRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**AccountId** | **string** | Zernio SocialAccount id used to resolve the Meta token. | 
**AdAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). | 
**UserId** | **string** | Business-scoped user id from GET /v1/ads/businesses/users. | 
**Tasks** | **List&lt;AssignAdAccountUserRequest.TasksEnum&gt;** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

