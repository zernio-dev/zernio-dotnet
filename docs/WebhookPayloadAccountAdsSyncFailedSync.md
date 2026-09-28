# Zernio.Model.WebhookPayloadAccountAdsSyncFailedSync

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**LastSuccessfulSyncAt** | **DateTime** |  | 
**FailureCount** | **int** | Consecutive failed sync attempts on the ad account&#39;s ads. | 
**ErrorCategory** | **string** | ad_account_not_listed &#x3D; the platform no longer returns the ad account to this connection (access removed, or a platform-side change); sync_error &#x3D; the platform returned an error, see &#x60;error&#x60;; stale &#x3D; no sync succeeded and no error was recorded. New values may be added.  | 
**Error** | **string** | Human-readable detail, for display and debugging. Branch on errorCategory. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

