# Zernio.Model.MetaAdScheduleInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DayOfWeek** | **string** |  | 
**StartHour** | **int** |  | 
**EndHour** | **int** | Must be after startHour. 24 is midnight at the end of the day. | 
**TimezoneType** | **string** | Meta &#x60;timezone_type&#x60;: USER runs the hours in each viewer&#39;s time zone, ADVERTISER in the ad account time zone. | [optional] [default to TimezoneTypeEnum.USER]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

