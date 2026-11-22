# Zernio.Model.WorkspaceWithBilling
A workspace, plus `billing` for owners, admins and billing admins.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Personal** | **bool** | True for the caller&#39;s own Personal workspace, which is never shared, renamed or deleted. | [optional] 
**Role** | **string** | The caller&#39;s role in this workspace. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**DeletionScheduledAt** | **DateTime** | When a scheduled deletion runs; null when none is scheduled. | [optional] 
**Billing** | [**WorkspaceWithBillingAllOfBilling**](WorkspaceWithBillingAllOfBilling.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

