# Late.Model.CreateInboxConversationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | The social account ID to send from | 
**ParticipantId** | **string** | Twitter numeric user ID of the recipient. Provide either this or &#x60;participantUsername&#x60;. | [optional] 
**ParticipantUsername** | **string** | Twitter username (with or without @) of the recipient. Resolved to a user ID via lookup. Provide either this or &#x60;participantId&#x60;. | [optional] 
**Message** | **string** | Text content of the message. At least one of &#x60;message&#x60; or attachment is required. | [optional] 
**SkipDmCheck** | **bool** | Skip the &#x60;receives_your_dm&#x60; eligibility check before sending. Use if you have already verified the recipient accepts DMs. | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

