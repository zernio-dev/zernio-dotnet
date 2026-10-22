# Zernio.Model.CommerceOrderVisit
A store session that led to the order.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**OccurredAt** | **DateTime?** | Null on WooCommerce, which records the session start without a timezone. | [optional] 
**LandingUrl** | **string** | The first page of the session, with its query string. | [optional] 
**ReferrerUrl** | **string** |  | [optional] 
**Source** | **string** | Where the visit came from, as the platform names it. | [optional] 
**SourceType** | **string** | Shopify marketing tactic (e.g. SOCIAL, AD, SEARCH) or WooCommerce source type (utm, organic, referral, typein, admin). | [optional] 
**Utm** | [**CommerceOrderVisitUtm**](CommerceOrderVisitUtm.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

