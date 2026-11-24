# Zernio.Model.TrackingSitePeriodTotals
A tracking site's page views over a period, as approximate distinct counts.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Visits** | **int** | Page views without bots. | [optional] 
**Bots** | **int** | Page views from bots. | [optional] 
**Consented** | **int** | Page views with ad storage consent, at most &#x60;visits&#x60;. | [optional] 
**Purchases** | **int** | Purchases recorded on the site. | [optional] 
**Recovered** | **int** | Purchases with ad consent for which no browser pixel fired, so only the server reported them. | [optional] 
**Leads** | **int** | Leads recorded on the site without bots. | [optional] 
**Checkouts** | **int** | Checkouts started on the site without bots. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

