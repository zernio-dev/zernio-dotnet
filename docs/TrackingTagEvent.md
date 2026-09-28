# Zernio.Model.TrackingTagEvent
A conversion event tied to a tracking tag (Google conversion action, LinkedIn conversion rule, X web event tag, OpenAI event setting, TikTok pixel event, Meta custom conversion).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform-native event id, the &#x60;{eventId}&#x60; of the per-event routes. | 
**Name** | **string** |  | 
**Type** | **string** | Platform event type or category. | [optional] 
**SiteEvent** | **string** | The neutral site event this conversion is fired for, when it maps to one. | [optional] 
**SiteEventId** | **string** | What the site sends to fire this event (Google conversion label, LinkedIn conversion rule id, X &#x60;tw-&#x60; event id). | [optional] 
**Status** | **string** |  | [optional] 
**DefaultValue** | **decimal** |  | [optional] 
**Currency** | **string** |  | [optional] 
**ClickWindowDays** | **int** |  | [optional] 
**ViewWindowDays** | **int** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

