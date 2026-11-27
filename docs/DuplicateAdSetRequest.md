# Zernio.Model.DuplicateAdSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**Platform** | **string** |  | 
**CampaignId** | **string** | Destination platform campaign id (defaults to the source&#39;s campaign) | [optional] 
**DeepCopy** | **bool** | Copy child ads + creatives | [optional] [default to true]
**StatusOption** | **string** |  | [optional] [default to StatusOptionEnum.PAUSED]
**StartTime** | **DateTime** | Reschedule the copy&#39;s start (ISO 8601). A value without an offset (&#x60;YYYY-MM-DD&#x60;, &#x60;YYYY-MM-DD HH:MM:SS&#x60; or &#x60;YYYY-MM-DDTHH:MM:SS&#x60;) is read in the ad account timezone. | [optional] 
**EndTime** | **DateTime** | Reschedule the copy&#39;s end, read like &#x60;startTime&#x60;; a date-only end runs to 23:59:59 local. | [optional] 
**RenameStrategy** | **string** | Meta&#39;s native &#x60;rename_strategy&#x60; values:  - &#x60;DEEP_RENAME&#x60;: renames the copied ad set and its copied ads with &#x60;renamePrefix&#x60; / &#x60;renameSuffix&#x60;. - &#x60;ONLY_TOP_LEVEL_RENAME&#x60;: renames only the copied ad set; its ads keep their source names. - &#x60;NO_RENAME&#x60;: keeps every source name.  With no rename option at all, Meta appends its own &#x60; - Copy&#x60; suffix. Ignored on TikTok, where &#x60;renamePrefix&#x60; / &#x60;renameSuffix&#x60; still apply.  | [optional] 
**RenamePrefix** | **string** | Text prepended to each renamed object&#39;s name. | [optional] 
**RenameSuffix** | **string** | Text appended to each renamed object&#39;s name. | [optional] 
**SyncAfter** | **bool** |  | [optional] [default to true]
**WebsiteOnly** | **bool** | Meta only. Rebuilds each copied ad (new creative and ad) instead of using Meta&#39;s native copy, so the creative carries applink_treatment web_only and Ads Manager shows Website as the only destination.  - Omitted or false: keeps the native copy. - 400 with &#x60;deepCopy: false&#x60;, and when an ad runs an existing post (its creative cannot be rebuilt). - Meta rejects it when the campaign uses Website and App conversion locations.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

