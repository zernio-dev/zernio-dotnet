# Zernio.Model.RcsAgent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**ProfileId** | **string** |  | [optional] 
**AccountId** | **string** | The rcs inbox account, created once the agent exists with the carriers. | [optional] 
**Country** | **string** | Launch market (ISO 3166-1 alpha-2). US agents run through the carriers automatically; other markets are filed by our team and skip the testing and launch_review steps (send the launch request while the agent is still in review). | [optional] 
**Status** | **string** |  | [optional] 
**DisplayName** | **string** |  | [optional] 
**UseCase** | **string** |  | [optional] 
**Profile** | [**RcsAgentProfile**](RcsAgentProfile.md) |  | [optional] 
**Brand** | [**RcsBrand**](RcsBrand.md) |  | [optional] 
**LaunchRequest** | [**RcsLaunchRequest**](RcsLaunchRequest.md) |  | [optional] 
**CarrierApprovals** | [**List&lt;RcsCarrierApproval&gt;**](RcsCarrierApproval.md) |  | [optional] 
**TestDevices** | [**List&lt;RcsTestDevice&gt;**](RcsTestDevice.md) |  | [optional] 
**SmsFallbackFrom** | **string** |  | [optional] 
**ReviewNote** | **string** | Our note while status is changes_requested. | [optional] 
**DeclineReason** | **string** |  | [optional] 
**RequestedAt** | **DateTime?** |  | [optional] 
**SubmittedAt** | **DateTime?** |  | [optional] 
**LiveAt** | **DateTime?** |  | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

