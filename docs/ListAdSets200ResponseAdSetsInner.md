# Zernio.Model.ListAdSets200ResponseAdSetsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PlatformAdSetId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**AdSetName** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**PlatformAdSetStatus** | **string** | Raw platform ad set status. On TikTok the ad group&#39;s own switch &#x60;operation_status&#x60; (ENABLE / DISABLE), independent of its campaign. | [optional] 
**PlatformCampaignId** | **string** |  | [optional] 
**PlatformAdAccountId** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**ProfileId** | **string** |  | [optional] 
**Currency** | **string** |  | [optional] 
**Budget** | [**ListAdSets200ResponseAdSetsInnerBudget**](ListAdSets200ResponseAdSetsInnerBudget.md) |  | [optional] 
**Schedule** | [**ListAdSets200ResponseAdSetsInnerSchedule**](ListAdSets200ResponseAdSetsInnerSchedule.md) |  | [optional] 
**Targeting** | [**ListAdSets200ResponseAdSetsInnerTargeting**](ListAdSets200ResponseAdSetsInnerTargeting.md) |  | [optional] 
**IsExternal** | **bool?** |  | [optional] 
**PlatformCreatedAt** | **DateTime?** |  | [optional] 
**StatusReadAt** | **DateTime?** | Only with &#x60;live&#x3D;true&#x60;. When &#x60;platformAdSetStatus&#x60; was read from the platform; null when this row was not read live. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

