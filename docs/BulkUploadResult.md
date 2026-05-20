# Zernio.Model.BulkUploadResult
Result of a CSV bulk upload. The same shape is returned for `200` (all rows succeeded or all failed) and `207` (mixed). Per-row outcomes live in `results`; the row's success is `ok`, and failures carry machine-readable codes in `errors`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Total** | **int** | Number of data rows processed from the CSV | [optional] 
**Valid** | **int** | Count of rows that succeeded (results[].ok &#x3D;&#x3D;&#x3D; true) | [optional] 
**Invalid** | **int** | Count of rows that failed (total - valid) | [optional] 
**Results** | [**List&lt;BulkUploadResultResultsInner&gt;**](BulkUploadResultResultsInner.md) | One entry per CSV data row, in row order. | [optional] 
**Warnings** | **List&lt;string&gt;** | Top-level advisory warnings (e.g. &#x60;rows_exceed_advisory_limit:500&#x60;). Empty when none. | [optional] 
**RateLimitedAccounts** | [**List&lt;BulkUploadResultRateLimitedAccountsInner&gt;**](BulkUploadResultRateLimitedAccountsInner.md) | Present only when one or more rows targeted an account currently in cooldown. Lets callers map &#x60;rate_limited:*&#x60; row errors back to structured metadata without parsing the error strings.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

