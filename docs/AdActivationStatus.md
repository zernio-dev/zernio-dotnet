# Zernio.Model.AdActivationStatus
Request-side publish switch for `adStatus` on ad creation endpoints only (`status`, `campaignStatus` and `adSetStatus` carry their own inline ACTIVE/PAUSED enum there; the status-update endpoints are a separate lowercase `active`/`paused` enum). Distinct from `AdStatus` (the platform-reported delivery status returned on reads).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

