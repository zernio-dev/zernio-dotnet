# Zernio.Model.SmsRegistrationReviewRequest
An open change request written as points. Answer each point with POST /v1/sms/registrations/{id}/respond: `answer` says what each point needs (text, a link, a hosted document, or a link or a document).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Changes with every request. Send it back as &#x60;requestId&#x60; when answering, so a reply to a replaced request is refused (409) instead of filed under the new points. | [optional] 
**Intro** | **string** | Context from the reviewer, e.g. what was already fixed on our side. | [optional] 
**Points** | [**List&lt;SmsRegistrationReviewRequestPointsInner&gt;**](SmsRegistrationReviewRequestPointsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

