# Zernio.Model.AutomationPostSubjects
The posts a scheduled automation checks.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Each** | **string** |  | 
**ProfileId** | **string** | The profile whose posts are checked. | 
**AccountIds** | **List&lt;string&gt;** | Only posts of these accounts. Each must be active on the profile. | [optional] 
**PublishedWithin** | **string** | How far back posts are checked, by when they were published. Whole days, from &#x60;1d&#x60; to &#x60;30d&#x60; (&#x60;48h&#x60; is 2 days). | [optional] [default to "7d"]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

