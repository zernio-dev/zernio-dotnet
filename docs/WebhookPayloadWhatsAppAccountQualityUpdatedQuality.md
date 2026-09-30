# Zernio.Model.WebhookPayloadWhatsAppAccountQualityUpdatedQuality

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Source** | **string** | The Meta webhook field that reported the change. | 
**MetaEvent** | **string** | Meta&#39;s &#x60;event&#x60; on phone_number_quality_update (for example FLAGGED, UNFLAGGED, UPGRADE, DOWNGRADE, ONBOARDING, THROUGHPUT_UPGRADE). Null on business_capability_update. | 
**QualityRating** | **string** | Current quality rating (GREEN, YELLOW, RED, UNKNOWN), read live from Meta on FLAGGED/UNFLAGGED. | 
**PreviousQualityRating** | **string** |  | 
**MessagingLimitTier** | **string** | Current messaging limit tier, for example TIER_250, TIER_2K, TIER_10K, TIER_100K, TIER_UNLIMITED. | 
**PreviousMessagingLimitTier** | **string** |  | 
**DisplayPhoneNumber** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

