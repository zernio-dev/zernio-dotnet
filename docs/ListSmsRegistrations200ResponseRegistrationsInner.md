# Zernio.Model.ListSmsRegistrations200ResponseRegistrationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**RegistrationType** | **string** |  | [optional] 
**DisplayName** | **string** |  | [optional] 
**Status** | **string** | requested/changes_requested &#x3D; pre-submission review states; customers see them as pending / needs changes. | [optional] 
**BrandStatus** | **string** | Carrier-registry brand status (e.g. VERIFIED). | [optional] 
**CampaignStatus** | **string** |  | [optional] 
**BrandId** | **string** | TCR brand id, useful when referencing the brand in carrier support threads. | [optional] 
**CampaignId** | **string** | TCR campaign id. | [optional] 
**DeclineReason** | **string** |  | [optional] 
**TfActionRequiredAt** | **DateTime?** | Toll-free only: when the carrier requested changes (\&quot;Waiting For Customer\&quot;). The request must be resubmitted within 7 days of this timestamp or it expires. | [optional] 
**PhoneNumbers** | **List&lt;string&gt;** |  | [optional] 
**AwaitingOtp** | **bool** | Sole-prop 10DLC only; the OTP step is still pending. | [optional] 
**AdminReviewNote** | **string** | The open change request as text (status changes_requested). | [optional] 
**LastResponseAt** | **DateTime?** | When you last answered a change request. | [optional] 
**PreviouslyRejected** | **bool** | Rejected by the carriers at least once. A pending registration with this set is our fix, back with the carriers. | [optional] 
**LastRejectedAt** | **DateTime?** | When the carriers last rejected it. | [optional] 
**RejectedBeforeSubmission** | **bool** | Rejected in our review before anything was filed with the carriers (not a carrier rejection; nothing to fix or appeal). | [optional] 
**OtpExpired** | **bool** | Sole proprietor only: the verification code was never entered within 30 days. Start SMS setup again; it revives the same brand with no second brand fee. | [optional] 
**ReviewRequest** | [**SmsRegistrationReviewRequest**](SmsRegistrationReviewRequest.md) |  | [optional] 
**TrustScore** | **decimal?** | Carrier-assigned brand trust score; drives throughput. | [optional] 
**Throughput** | [**ListSmsRegistrations200ResponseRegistrationsInnerThroughput**](ListSmsRegistrations200ResponseRegistrationsInnerThroughput.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

