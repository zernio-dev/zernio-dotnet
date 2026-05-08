# Zernio.Model.ConversionDestination
A discoverable conversion destination on an ad platform — a Meta pixel, Google conversion action, or LinkedIn conversion rule. Returned by `listConversionDestinations`, `getConversionDestination`, `createConversionDestination`, and `updateConversionDestination`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform-native identifier. Pass back as &#x60;destinationId&#x60; on event send and as the path segment on CRUD endpoints.  | 
**Name** | **string** |  | 
**Type** | **string** | Present when the platform locks the event type/category to the destination (Google conversion actions, LinkedIn conversion rules). Absent for Meta pixels (which accept any event name per request).  | [optional] 
**Status** | **string** | For LinkedIn, &#x60;inactive&#x60; means the rule is soft-deleted (&#x60;enabled: false&#x60;).  | [optional] 
**AdAccountId** | **string** | Set by adapters whose destinations are scoped to a specific ad account (LinkedIn). Pass back on subsequent CRUD calls to identify the parent ad account.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

