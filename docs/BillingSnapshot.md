# Zernio.Model.BillingSnapshot
Account billing state — plan, cycle, balance, spend caps, and payment / access status. Returned by `GET /v1/billing`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BillingSystem** | **string** |  | [optional] 
**Plan** | [**BillingSnapshotPlan**](BillingSnapshotPlan.md) |  | [optional] 
**Period** | [**BillingSnapshotPeriod**](BillingSnapshotPeriod.md) |  | [optional] 
**Balance** | [**BillingSnapshotBalance**](BillingSnapshotBalance.md) |  | [optional] 
**Caps** | [**BillingSnapshotCaps**](BillingSnapshotCaps.md) |  | [optional] 
**Status** | [**BillingSnapshotStatus**](BillingSnapshotStatus.md) |  | [optional] 
**Legacy** | [**BillingSnapshotLegacy**](BillingSnapshotLegacy.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

