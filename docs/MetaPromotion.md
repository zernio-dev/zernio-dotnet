# Zernio.Model.MetaPromotion
Meta explicit Promotion offer. Maps to creative_sourcing_spec.promotion_metadata_spec with promotion_source ADVERTISER_INPUT. Dates become Unix seconds. Send null to omit an explicit offer on a new creative or remove it when rebuilding. Creation success alone does not confirm application: inspect promotionStatus in the response.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | Promotion type accepted by Meta. PERCENTAGE_OFF values cannot exceed 100. | 
**Value** | **decimal** | Nonnegative promotion value passed to Meta unchanged. AMOUNT_OFF units are not confirmed, including major versus minor currency units. For PERCENTAGE_OFF this is the percentage discount, at most 100. | 
**Code** | **string** | Optional promotion code. | [optional] 
**StartDate** | **DateTime** | Optional ISO 8601 start timestamp with a timezone offset or Z. | [optional] 
**EndDate** | **DateTime** | Optional ISO 8601 end timestamp with a timezone offset or Z. Must be after startDate when both are set. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

