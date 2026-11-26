# Zernio.Model.StagedAdChange
An ad write that was validated and stored with `stage: true`, waiting to be confirmed or discarded.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The change id, used in /v1/ads/changes/{changeId}. | 
**Type** | **string** | Which write was staged: a status route, an update route (campaign, ad set, ad), the campaign targeting route or a create route. &#x60;operation&#x60; is any other ads write, staged as its request and named by &#x60;request&#x60;. It has no live read, so its diff shows the new values only. | 
**Request** | [**StagedAdChangeRequest**](StagedAdChangeRequest.md) |  | [optional] 
**Platform** | **string** | The ad platform of the object, as the write route names it. | 
**AccountId** | **string** | The connected account the write goes through. | 
**AdAccountId** | **string** | The ad account id on the platform. | 
**TargetId** | **string** | The object the change applies to: the platform campaign id, the platform ad set id, or the Zernio ad id. Null for a create, whose object does not exist yet. | 
**TargetName** | **string** | The name of the object when the change was staged, or the name a create will give it. Null when it is not known. | [optional] 
**Creates** | **bool** | Present and true when the change creates a new object. Every diff entry then has &#x60;before: null&#x60; and &#x60;beforeAvailable: false&#x60;. | [optional] 
**Status** | **string** | - &#x60;staged&#x60;: waiting to be confirmed or discarded. - &#x60;confirming&#x60;: a confirm is running. A change left here for 15 minutes ends as &#x60;failed&#x60; with error code &#x60;change_outcome_unknown&#x60;, and is never applied again automatically. - &#x60;confirmed&#x60;: applied. &#x60;result&#x60; holds what the write returned. - &#x60;failed&#x60;: not applied. &#x60;error&#x60; says why.  | 
**Diff** | [**List&lt;StagedAdChangeDiffInner&gt;**](StagedAdChangeDiffInner.md) | One entry per value of the staged request that the write would change.  - A nested field is flattened: each leaf is one entry under its dotted path (&#x60;budget.amount&#x60;, &#x60;targeting.ageMin&#x60;, &#x60;creative.headline&#x60;). - A list is one entry. - A leaf whose value on the ad network already equals the requested value is left out, so the list can be empty. - &#x60;stage&#x60; and other flags that only steer the write are never listed.  | 
**CreatedBy** | **string** | The user who staged the change. | 
**ConfirmedBy** | **string** | The user who confirmed the change. Null while nobody has, and after a confirm that left the change staged. | [optional] 
**Stale** | **bool** | Present and true on a staged change whose last confirm was refused with &#x60;change_target_changed&#x60;. &#x60;error&#x60; then says why. Refresh it with PATCH /v1/ads/changes/{changeId} (no body), or discard it and stage it again. | [optional] 
**CreatedAt** | **DateTime** |  | 
**FinishedAt** | **DateTime?** | When the confirm ended, as &#x60;confirmed&#x60; or &#x60;failed&#x60;. A finished change is deleted 7 days later, a failed create 30 days later. | 
**Result** | **Dictionary&lt;string, Object&gt;** | Present once &#x60;confirmed&#x60;: the response body of the write. | [optional] 
**Error** | [**StagedAdChangeError**](StagedAdChangeError.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

