# Zernio.Model.GetCampaignResultsUpload200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UploadId** | **string** |  | 
**Status** | **string** |  | 
**Source** | **string** |  | 
**RowsReceived** | **int** |  | 
**RowsMatched** | **int** |  | 
**RowsUnmatched** | **int** |  | 
**Unmatched** | [**List&lt;GetCampaignResultsUpload200ResponseUnmatchedInner&gt;**](GetCampaignResultsUpload200ResponseUnmatchedInner.md) |  | 
**FailureReason** | **string** | Set when &#x60;status&#x60; is &#x60;failed&#x60;. &#x60;queue_unavailable&#x60;: the upload could not be queued. &#x60;processing_failed&#x60;: its rows could not be stored after several retries. Both are on our side. | 
**CreatedAt** | **DateTime** |  | 
**CompletedAt** | **DateTime?** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

