# Zernio.Model.ConnectSlackChannelRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**ChannelId** | **string** | Slack channel id, C... or G.... Send this or channelIds, not both. | [optional] 
**ChannelIds** | **List&lt;string&gt;** | Several channels of the workspace to connect, each as its own account. With two or more distinct ids the response lists &#x60;accounts&#x60; and &#x60;failed&#x60; instead of &#x60;account&#x60;, and the request is refused with 400 on a reconnect. A single id behaves exactly like channelId. | [optional] 
**RedirectUrl** | **string** | channelIds only: a URL to return in &#x60;redirect_url&#x60;, with &#x60;connected&#x60;, &#x60;profileId&#x60;, &#x60;accountId&#x60; and &#x60;accountIds&#x60; appended. | [optional] 
**PendingDataToken** | **string** | Nonce from the OAuth redirect. Required unless accountId is sent. | [optional] 
**AccountId** | **string** | Existing Slack account whose workspace token is reused. Required unless pendingDataToken is sent. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

