# Zernio.Model.GetEventsOverviewDaily200ResponseTotals
The period's figures, shaped like the overview's `today`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Conversions** | **int** | Stored events that occurred in the period, retracted ones excluded. | [optional] 
**Value** | **decimal** | Value of those events in &#x60;currency&#x60;. Events in other currencies are left out. | [optional] 
**ValueSent** | **decimal** | Value in &#x60;currency&#x60; of those events at least one platform accepted. | [optional] 
**Currency** | **string** | The currency most of the period&#39;s events use; &#x60;null&#x60; when none carried a value. | [optional] 
**Sent** | **int** | Events first sent to a destination in the period, one per event and destination. | [optional] 
**Accepted** | **int** | Those whose latest send the platform accepted. | [optional] 
**Matched** | **int** | The period&#39;s events matched to an ad campaign. | [optional] 
**Counted** | **int** | The period&#39;s events that count as campaign results, the ones looked up for a campaign. | [optional] 
**FromAds** | **int** | Of the counted events, those that came from an ad: they named a campaign or carried a UTM campaign, a Google click id or a Zernio ad id (&#x60;zrn&#x60;), their own or the website visit&#39;s behind them. &#x60;matched&#x60; over &#x60;fromAds&#x60; is the share tied to a campaign. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

