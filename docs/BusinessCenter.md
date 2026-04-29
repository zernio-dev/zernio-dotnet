# Zernio.Model.BusinessCenter
TikTok Business Center entity. Returned by `GET /v1/ads/business-centers`. BCs are TikTok's agency container — one BC owns N advertisers (ad accounts). Most solo advertisers don't have one; the agency token uses BCs to roll up multi-client access. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BcId** | **string** | Business Center ID | [optional] 
**Name** | **string** | Display name set by the BC owner | [optional] 
**AdvertiserCount** | **int** | Number of advertisers (ad accounts) reachable under this BC for the calling token | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

