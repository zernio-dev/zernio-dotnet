# Zernio.Model.GetBalance200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AvailableCents** | **int** | Balance you can transfer now. Negative after a dispute or refund of a top-up that was already spent; transfers are refused while it is negative. | [optional] 
**PendingCents** | **int** | Paid card top-ups still on hold. Card top-ups become available after 7 days. | [optional] 
**PendingReleases** | [**List&lt;GetBalance200ResponsePendingReleasesInner&gt;**](GetBalance200ResponsePendingReleasesInner.md) | Card top-ups on hold, each with the time it becomes available. | [optional] 
**PendingTopupCents** | **int** | Top-ups started but not paid yet. | [optional] 
**Currency** | **string** |  | [optional] 
**RecentTopups** | [**List&lt;TreasuryTopup&gt;**](TreasuryTopup.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

