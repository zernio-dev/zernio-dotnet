# Zernio.Model.EventConsent
Google Consent Mode's four signals as the visitor gave them. Leave a signal out when the visitor was never asked or never answered.  For a visitor in the EEA, the UK or Switzerland (from `user.country`), a signal left out counts as `DENIED`. See \"Consent\" on `POST /v1/events`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdStorage** | **string** | Ad cookies and click ids (&#x60;ad_storage&#x60;). | [optional] 
**AdUserData** | **string** | Sending personal data to ad platforms (&#x60;ad_user_data&#x60;). | [optional] 
**AdPersonalization** | **string** | Personalized advertising and remarketing (&#x60;ad_personalization&#x60;). | [optional] 
**AnalyticsStorage** | **string** | Analytics cookies (&#x60;analytics_storage&#x60;): Google Analytics only. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

