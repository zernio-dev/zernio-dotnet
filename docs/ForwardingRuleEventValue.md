# Zernio.Model.ForwardingRuleEventValue
How one event is valued. `original` sends its own value. `fixed` sends `amount` in `currency`, even when the event came without a value. `percent` sends `amount` percent of its own value (10 sends 10%, rounded to cents) in its own currency, and leaves an event without a value without one.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Mode** | **string** |  | 
**Amount** | **decimal** |  | 
**Currency** | **string** | ISO 4217 code, saved in capitals. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

