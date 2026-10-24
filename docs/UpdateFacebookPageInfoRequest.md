# Zernio.Model.UpdateFacebookPageInfoRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**About** | **string** | Short description, shown as Description in the Page&#39;s Edit Page Info. | [optional] 
**Description** | **string** | Longer text, shown as Additional Information. | [optional] 
**Website** | **string** | URL of the Page&#39;s website. | [optional] 
**Phone** | **string** |  | [optional] 
**Emails** | **List&lt;string&gt;** | Replaces every email listed on the Page. | [optional] 
**Hours** | **Dictionary&lt;string, string&gt;** | Replaces the opening hours. Keys are &#x60;{day}_{slot}_{open|close}&#x60; with day &#x60;mon&#x60; to &#x60;sun&#x60; and slot 1 or 2, values are 24h &#x60;HH:MM&#x60; times. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

