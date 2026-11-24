# Zernio.Model.StagedAdChangeDiffInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Field** | **string** | The dotted path of the value in the request body. | 
**Before** | **Object** |  | 
**After** | **Object** |  | 
**BeforeAvailable** | **bool** | False when &#x60;before&#x60; is unknown: the live read of the object does not return this field, or the change creates the object. The field is still staged. | 
**Added** | **List&lt;Object&gt;** | Only on a list of plain values (strings or numbers) with &#x60;beforeAvailable&#x60; true: the values in &#x60;after&#x60; that are not in &#x60;before&#x60;. Order is ignored. | [optional] 
**Removed** | **List&lt;Object&gt;** | Only on a list of plain values (strings or numbers) with &#x60;beforeAvailable&#x60; true: the values in &#x60;before&#x60; that are not in &#x60;after&#x60;. Order is ignored. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

