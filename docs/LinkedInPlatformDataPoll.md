# Zernio.Model.LinkedInPlatformDataPoll
Create a LinkedIn poll with this post. Cannot be combined with media or reshareUrl. Polls cannot be edited after publishing on LinkedIn, and API-created polls are non-sponsored only (they cannot be promoted as ads).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Question** | **string** | Poll question (max 140 characters) | 
**Options** | **List&lt;string&gt;** | Poll options (2-4 choices, max 30 characters each) | 
**Duration** | **string** | How long the poll accepts votes. Defaults to SEVEN_DAYS. | [optional] [default to DurationEnum.SEVENDAYS]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

