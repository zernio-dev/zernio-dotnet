# Zernio.Model.WebhookPayloadAdRuleTriggeredRun

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | ID of the rule run that triggered. | 
**RanAt** | **DateTime** | Scheduled time of the run (UTC). | 
**Today** | **DateOnly** | The ad account&#39;s calendar date (YYYY-MM-DD) the condition windows were resolved against, so &#x60;today&#x60; and &#x60;last_7d&#x60; mean the account&#39;s days, not UTC days. | 
**Timezone** | **string** | IANA timezone used for &#x60;today&#x60;, for example &#x60;Europe/Madrid&#x60;. | 
**TimezoneAssumed** | **bool** | True when the ad account has no known timezone and UTC was assumed. | 
**Currency** | **string** | ISO 4217 currency of the ad account, which money metrics (&#x60;spend&#x60;, &#x60;cpc&#x60;, &#x60;cpm&#x60;, &#x60;cpa&#x60;) and condition values are in. Null when unknown. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

