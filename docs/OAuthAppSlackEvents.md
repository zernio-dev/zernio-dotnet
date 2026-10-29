# Zernio.Model.OAuthAppSlackEvents
Slack only; null on other platforms. Slack delivers messages and mentions to your app's own Request URL.  Save the app's signing secret first (`slackSigningSecret`), then set this Request URL under Event Subscriptions and subscribe the listed bot events. Zernio checks each delivery against that secret. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RequestUrl** | **string** |  | 
**BotEvents** | **List&lt;string&gt;** | Subscribe the app to these bot events. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

