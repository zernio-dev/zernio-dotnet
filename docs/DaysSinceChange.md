# Zernio.Model.DaysSinceChange
Days since the campaign's budget, bidding, status or conversion goal last changed, on the campaign or, on Meta, one of its ad sets. Read from the platform's change history, Meta and Google only.  A campaign with no such change in the history passes `>=` and fails `<`. Google records an edit of conversion goals as a campaign update naming no field, so `goal` reads those.  On Google, a change to a shared (portfolio) bid strategy does not count as a `bidding` change of its campaigns. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Field** | **string** |  | 
**Change** | **string** |  | 
**Op** | **string** |  | 
**Value** | **int** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

