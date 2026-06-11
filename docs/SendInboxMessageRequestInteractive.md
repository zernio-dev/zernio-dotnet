# Zernio.Model.SendInboxMessageRequestInteractive
WhatsApp-only. Rich interactive payload for list messages, CTA URL buttons, Flow prompts, and location requests. When set, takes priority over `buttons` and `quickReplies`. The shape mirrors Meta's Cloud API `interactive` object verbatim, so any payload that works against Meta directly will also work here.  Use `buttons` / `quickReplies` for simple button replies (WhatsApp's `interactive.type: \"button\"`) — the abstraction caps at 3 buttons and handles the auto-conversion for you. Use this field only for `list`, `cta_url`, `flow`, or `location_request_message` messages.  For `location_request_message`, `action` may be omitted (we default it to `{ \"name\": \"send_location\" }`). WhatsApp renders a localized \"Send location\" button; the user's reply arrives as a regular location message in the conversation.  Tap events come back via the `message.received` webhook with `metadata.interactiveType` set to `list_reply` or `nfm_reply`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | Which interactive layout to render. | 
**Header** | [**SendInboxMessageRequestInteractiveHeader**](SendInboxMessageRequestInteractiveHeader.md) |  | [optional] 
**Body** | [**SendInboxMessageRequestInteractiveBody**](SendInboxMessageRequestInteractiveBody.md) |  | 
**Footer** | [**SendInboxMessageRequestInteractiveFooter**](SendInboxMessageRequestInteractiveFooter.md) |  | [optional] 
**Action** | [**SendInboxMessageRequestInteractiveAction**](SendInboxMessageRequestInteractiveAction.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

