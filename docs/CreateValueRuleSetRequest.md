# Zernio.Model.CreateValueRuleSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id (posting or ads variant); its platform decides where the campaign is created. | 
**AdAccountId** | **string** | Platform ad account id (Meta act_&lt;n&gt;, Google customer id, LinkedIn account id, ...). | 
**Name** | **string** |  | 
**Rules** | [**List&lt;ValueRule&gt;**](ValueRule.md) | Evaluated in order; the first matching rule wins. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

