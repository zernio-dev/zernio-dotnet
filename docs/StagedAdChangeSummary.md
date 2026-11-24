# Zernio.Model.StagedAdChangeSummary
A staged ad change as the list returns it: what it targets and who staged it, without the diff.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The change id, used in /v1/ads/changes/{changeId}. | 
**Type** | **string** | Which write was staged. | 
**Platform** | **string** | The ad platform of the object, as the write route names it. | 
**AccountId** | **string** | The connected account the write goes through. | 
**AdAccountId** | **string** | The ad account id on the platform. | 
**TargetId** | **string** | The object the change applies to. Null for a create, whose object does not exist yet. | 
**TargetName** | **string** | The name of the object when the change was staged, or the name a create will give it. Null when it is not known. | 
**Creates** | **bool** | True when the change creates a new object. | 
**CreatedBy** | **string** | The user who staged the change. | 
**CreatedAt** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

