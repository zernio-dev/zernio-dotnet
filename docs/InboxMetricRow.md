# Zernio.Model.InboxMetricRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **string** | Start of the period: the day or the Monday of the week, never before fromDate. With granularity&#x3D;total, fromDate. | 
**AccountId** | **string** | With groupBy&#x3D;account. | [optional] 
**Platform** | **string** | With groupBy&#x3D;account or groupBy&#x3D;platform. | [optional] 
**Source** | **string** | With groupBy&#x3D;source; null for messages with no source recorded, such as messages received. | [optional] 
**DayOfWeek** | **int** | With groupBy&#x3D;hourOfWeek: 1 is Monday, 7 is Sunday, in UTC. | [optional] 
**Hour** | **int** | With groupBy&#x3D;hourOfWeek: 0 to 23, in UTC. | [optional] 
**ResponseTimeBucket** | [**ResponseTimeBucket**](ResponseTimeBucket.md) | With groupBy&#x3D;responseTimeBucket. | [optional] 
**Account** | [**InboxMetricRowAccount**](InboxMetricRowAccount.md) |  | [optional] 
**ConversationId** | **string** | With groupBy&#x3D;conversation or conversationId: the Zernio conversation id, or the id logged with the messages when the conversation no longer exists. | [optional] 
**FirstMessageAt** | **string** | With conversation rows: first message, read receipt or failure in the period, UTC. null for a conversation read by id with no activity in the period. | [optional] 
**LastMessageAt** | **string** | With conversation rows: last message, read receipt or failure in the period, UTC. | [optional] 
**Conversation** | [**InboxMetricRowConversation**](InboxMetricRowConversation.md) |  | [optional] 
**Metrics** | **Dictionary&lt;string, decimal?&gt;** | Each metric asked; response times are null when no message received got a reply. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

