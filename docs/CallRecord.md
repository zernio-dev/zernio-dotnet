# Zernio.Model.CallRecord
One call on a number you own, either channel. `channel` tells you which lane it took: `whatsapp` (WhatsApp Business Calling) or `pstn` (a regular phone call). List endpoints omit `transcript`; use `lastTranscriptSnippet` for a preview and the detail endpoint for the full transcript. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**AccountId** | **string** | Owning social account. The unified /v1/calls/{id} detail + recording endpoints work for any channel; the channel-specific endpoints remain for account-scoped access. | [optional] 
**ConversationId** | **string** | Inbox conversation with the counterparty, when one exists. | [optional] 
**ContactId** | **string** | CRM Contact for the counterparty, when resolved. | [optional] 
**Channel** | **string** |  | [optional] 
**Direction** | **string** |  | [optional] 
**From** | **string** | Caller number (E.164). | [optional] 
**To** | **string** | Callee number (E.164). | [optional] 
**ForwardTo** | **string** | Destination the call was routed to (tel:/sip:/wss:), snapshotted at routing time. | [optional] 
**Greeting** | **string** | Outbound PSTN only. Message spoken to the callee on answer, before the bridge. | [optional] 
**Status** | **string** |  | [optional] 
**IsVoicemail** | **bool** | True when an inbound call went to voicemail. | [optional] 
**Amd** | **bool** | Outbound answering-machine detection was requested for this call. | [optional] 
**AnsweredMachine** | **bool?** | With &#x60;amd&#x60;, whether a machine (vs a human) answered. | [optional] 
**ForwardCallerId** | **string** | Caller ID presented on the forwarded leg. | [optional] 
**RecordingEnabled** | **bool** | Effective flag for THIS call (number default + per-call override, resolved at create time). | [optional] 
**TranscriptionEnabled** | **bool** |  | [optional] 
**TranscriptionLanguage** | **string** |  | [optional] 
**StartedAt** | **DateTime** |  | [optional] 
**AnsweredAt** | **DateTime?** |  | [optional] 
**EndedAt** | **DateTime?** |  | [optional] 
**TransferredAt** | **DateTime?** | When the call was blind-transferred (POST /v1/voice/calls/{id}/transfer). | [optional] 
**DurationSeconds** | **int** |  | [optional] 
**EndReason** | **string** |  | [optional] 
**HangupCause** | **string** | Raw carrier hangup cause behind endReason (e.g. normal_clearing, not_found, time_limit) — the actual motive when endReason is a coarse bucket. | [optional] 
**SipHangupCause** | **string** | SIP response code that ended the call, when SIP-signalled (e.g. &#39;403&#39;, &#39;488&#39;). The real failure reason for SIP legs. | [optional] 
**CallErrors** | [**List&lt;CallRecordCallErrorsInner&gt;**](CallRecordCallErrorsInner.md) | Per-call failure log (dial failed, bridge failed, recording error). | [optional] 
**RecordingUrl** | **string** | May be expired. Resolve a fresh playable URL via GET /v1/calls/{id}/recording (any channel). | [optional] 
**LastTranscriptSnippet** | **string** | Most recent transcript segment, for list previews. | [optional] 
**Transcript** | [**List&lt;CallRecordTranscriptInner&gt;**](CallRecordTranscriptInner.md) | Full transcript segments (detail endpoint only; omitted from lists). | [optional] 
**Billing** | [**CallRecordBilling**](CallRecordBilling.md) |  | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**UpdatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

