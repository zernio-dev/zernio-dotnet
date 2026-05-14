# Zernio.Model.WebhookPayloadAdStatusChanged
Webhook payload for the `ad.status_changed` event. Currently emitted only for Meta (`metaads`).  Sourced from two Meta `ad_account` webhook fields:   - `in_process_ad_objects` - the ad object finished processing and     exited `IN_PROCESS`. `status.raw` carries Meta's `status_name`.   - `with_issues_ad_objects` - the ad object entered `WITH_ISSUES`.     `status.raw` is `WITH_ISSUES` and the `error` block is populated     from Meta's `error_code` / `error_summary` / `error_message`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Account** | [**WebhookPayloadAdStatusChangedAccount**](WebhookPayloadAdStatusChangedAccount.md) |  | 
**AdObject** | [**WebhookPayloadAdStatusChangedAdObject**](WebhookPayloadAdStatusChangedAdObject.md) |  | 
**Status** | [**WebhookPayloadAdStatusChangedStatus**](WebhookPayloadAdStatusChangedStatus.md) |  | 
**Error** | [**WebhookPayloadAdStatusChangedError**](WebhookPayloadAdStatusChangedError.md) |  | [optional] 
**Timestamp** | **DateTime** | ISO-8601 timestamp the webhook was produced. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

