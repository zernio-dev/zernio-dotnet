# Zernio.Model.FacebookPostEarningsResponse
Lifetime monetization earnings for one Facebook post. Same \"unit\" / \"currency\" contract and same unavailable-vs-zero contract as the Page-level response; there is no date range, no metricType, and no daily \"values\", because the single lifetime bucket IS the total. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Success** | **bool** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**PostId** | **string** | The platform post ID that was queried, echoed back. | [optional] 
**Platform** | **string** |  | [optional] 
**Period** | **string** | Always \&quot;lifetime\&quot;: the total is cumulative since publication and must not be summed across dates or across posts.  | [optional] 
**Metrics** | [**Dictionary&lt;string, FacebookPostEarningsResponseMetricsValue&gt;**](FacebookPostEarningsResponseMetricsValue.md) | One entry per served metric. A metric reported here with \&quot;total\&quot;: 0 genuinely earned nothing (or its Page is not enrolled, which Meta reports identically).  | [optional] 
**UnavailableMetrics** | [**List&lt;FacebookPostEarningsResponseUnavailableMetricsInner&gt;**](FacebookPostEarningsResponseUnavailableMetricsInner.md) | Requested metrics Meta could not serve. Present only when at least one metric is unavailable, and absent otherwise. Each listed metric is OMITTED from \&quot;metrics\&quot; rather than reported as 0. The request itself still succeeds with HTTP 200.  | [optional] 
**DataDelay** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

