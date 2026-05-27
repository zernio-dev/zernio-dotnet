# Zernio.Model.GetWhatsAppNumberInfo200ResponsePhone

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DisplayPhoneNumber** | **string** |  | [optional] 
**VerifiedName** | **string** |  | [optional] 
**NameStatus** | **string** | APPROVED, AVAILABLE_WITHOUT_REVIEW, PENDING_REVIEW, DECLINED, EXPIRED, NONE | [optional] 
**QualityRating** | **string** | GREEN, YELLOW, RED, UNKNOWN | [optional] 
**MessagingLimitTier** | **string** | e.g. TIER_250, TIER_1K, TIER_UNLIMITED | [optional] 
**Throughput** | [**GetWhatsAppNumberInfo200ResponsePhoneThroughput**](GetWhatsAppNumberInfo200ResponsePhoneThroughput.md) |  | [optional] 
**Status** | **string** | e.g. CONNECTED | [optional] 
**IsOfficialBusinessAccount** | **bool** |  | [optional] 
**PlatformType** | **string** | e.g. CLOUD_API | [optional] 
**HealthStatus** | **Object** | Meta&#39;s can_send_message health object (messaging + calling signals) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

