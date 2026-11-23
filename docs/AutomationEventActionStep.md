# Zernio.Model.AutomationEventActionStep
A step of an event automation that acts on its own. `messages.send`, `contacts.tag` and `sequences.enroll` need an event about a conversation or a call: they act on that person.  `workflows.start` also takes an order event, reaching its customer by the phone the store holds. A step that does not fit its event is refused at its `type`.  Only `webhook.call` and `notify.send` run on `message.sent` and `message.failed`, which an automation's own messages fire. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Type** | **string** |  | 
**Text** | **string** |  | 
**WorkflowId** | **string** |  | 
**SequenceId** | **string** |  | 
**Url** | **string** |  | 
**Method** | **string** |  | [optional] [default to MethodEnum.POST]
**Headers** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**Body** | **string** | May read &#x60;{{event.&lt;fact&gt;}}&#x60;. | [optional] 
**Action** | **string** |  | 
**Tag** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

