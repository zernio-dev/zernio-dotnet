# Zernio.Model.CreatorPortalPayoutSetup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Mode** | **string** | How the campaign pays: treasury means through Zernio, so the creator onboards for payouts, which they can do from the moment they join. Earnings wait until it is done. | 
**Status** | **string** |  | 
**Country** | **string** |  | 
**SuggestedCountry** | **string** | The country the request came from, to preselect before payout setup starts. Null once the payout account has a country, and outside treasury mode. | 
**Transfers** | [**List&lt;CreatorPortalPayoutSetupTransfersInner&gt;**](CreatorPortalPayoutSetupTransfersInner.md) | Treasury payouts sent to the creator. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

