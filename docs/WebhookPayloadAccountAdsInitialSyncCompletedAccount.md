# Zernio.Model.WebhookPayloadAccountAdsInitialSyncCompletedAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | The account&#39;s unique identifier (same as used in /v1/accounts/{accountId}) | 
**ProfileId** | **string** | The profile&#39;s unique identifier this account belongs to | 
**Platform** | **string** |  | 
**Username** | **string** |  | 
**DisplayName** | **string** |  | [optional] 
**PlatformUserId** | **string** | The platform-side account/ad-account ID (e.g. Meta ad account ID). | [optional] 
**ProfilePicture** | **string** | URL of the account&#39;s profile picture, when available. | [optional] 
**PlatformAdAccountId** | **string** | When the consumer scoped the connect call to a single ad account, this echoes that ID back so the webhook can be correlated to the originating connect request without consulting the consumer&#39;s DB. Meta uses the &#x60;act_*&#x60; shape.  | [optional] 
**PlatformAdAccountIds** | **List&lt;string&gt;** | Every ad-account ID that the connected token could see at discovery time. Useful for \&quot;we synced ads from these accounts\&quot; UX without a follow-up API call. Empty array when the token had no ad-account visibility.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

