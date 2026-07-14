# Zernio.Model.LinkedInAdsPlatformDataConversation
POST /v1/ads/create only. Conversation Ad: a choose-your-path message tree delivered to the member's LinkedIn inbox. Messages are flat nodes wired by local ids; each button either opens a url or leads to nextMessageId. Cycles, unknown ids and a missing firstMessageId return a 400. LinkedIn does not deliver message ads to EU members. Mutually exclusive with the other creative sources. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Subject** | **string** | InMail subject shown in the inbox. | 
**Sender** | **string** | Person or organization URN. Defaults to the authoring Company Page. The sender must be approved for the ad account first (Campaign Manager &gt; Manage message ad senders) or LinkedIn rejects the create with SINMAIL_SENDER_NOT_APPROVED.  | [optional] 
**Body** | **string** | Optional intro body (HTML allowed). | [optional] 
**Footer** | **string** | Terms shown at the bottom of the message. | [optional] 
**Headline** | **string** | Conversation headline. Defaults to the first message&#39;s first line. | [optional] 
**FirstMessageId** | **string** |  | 
**Messages** | [**List&lt;LinkedInAdsPlatformDataConversationMessagesInner&gt;**](LinkedInAdsPlatformDataConversationMessagesInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

