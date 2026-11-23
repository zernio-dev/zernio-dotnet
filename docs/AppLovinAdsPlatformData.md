# Zernio.Model.AppLovinAdsPlatformData
AppLovin options in platformSpecificData. Campaign fields apply to a new campaign; assets, languages and brandInfo to the creative set (the ad).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CampaignType** | **string** | Required for a new campaign. | [optional] 
**Os** | **string** | APP campaigns. Required. | [optional] 
**PackageName** | **string** | APP campaigns. Required. | [optional] 
**ItunesId** | **int** | iOS APP campaigns. Required. | [optional] 
**WebsiteUrl** | **string** | WEB campaigns. Required unless linkUrl is sent. | [optional] 
**BiddingStrategy** | **string** | Defaults to CPI billing for a CPI goal, CPM billing otherwise. TARGET_GOAL_WITH_CPI_BILLING takes an APP campaign with a CPI goal only. Set at creation only. | [optional] 
**GoalType** | **string** | APP takes all, WEB takes CPE, CPP and CHK_ROAS. Defaults from goal: app_promotion is CPI, conversions CPP, lead_generation CPE. Set at creation only. | [optional] 
**GoalValue** | **decimal** | The goal for every country (a cost, or a ROAS ratio). APP limits: CPI below 200, CPE and CPP below 500, AD_ROAS at least 0.1, CHK_ROAS at least 0.01, BLD_ROAS at least 0.05. Send this or countryGoalValues. | [optional] 
**CountryGoalValues** | **Dictionary&lt;string, decimal&gt;** | Per-country goal values for targeted countries. | [optional] 
**RoasDayTarget** | **string** | Required for ROAS goals (and WEB CPP). APP takes DAY7 or DAY28, WEB DAY0 or DAY7. | [optional] 
**EventTarget** | **string** | Required for a CPE goal. | [optional] 
**CountryBudgets** | **Dictionary&lt;string, decimal&gt;** | Per-country daily budgets, instead of budgetAmount. AppLovin budgets are daily only. | [optional] 
**Tracking** | [**AppLovinAdsPlatformDataTracking**](AppLovinAdsPlatformDataTracking.md) |  | [optional] 
**AudienceStrategy** | **string** | WEB campaigns. | [optional] 
**Assets** | [**List&lt;AppLovinAdsPlatformDataAssetsInner&gt;**](AppLovinAdsPlatformDataAssetsInner.md) | The creative set media: URLs Zernio uploads to AppLovin, or ids of assets already there. Needs a HOSTED_HTML asset, or an IMG_INTER_P image plus a VID_LONG_P or VID_SHORT_P video. | [optional] 
**Languages** | **List&lt;string&gt;** | Creative set languages as AppLovin names them. All languages by default. | [optional] 
**BrandInfo** | [**AppLovinAdsPlatformDataBrandInfo**](AppLovinAdsPlatformDataBrandInfo.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

