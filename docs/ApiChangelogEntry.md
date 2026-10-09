# Zernio.Model.ApiChangelogEntry
One API changelog entry, as shown on https://docs.zernio.com/changelog.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable entry id; the same entry is never published twice. | 
**Type** | **string** | When &#x60;impact&#x60; is set, &#x60;breaking_change&#x60; means exactly &#x60;impact: action_required&#x60;. | 
**Impact** | **string** | What an integrator has to do, computed from the OpenAPI diff rather than from the prose. &#x60;action_required&#x60;: an existing call or parser can break (an operation, parameter or field removed, a field newly required, a type narrowed, an enum value removed, or authentication changed). &#x60;additive&#x60;: only new or looser things, existing integrations keep working. &#x60;none&#x60;: descriptions or examples only. Null on entries published before October 2026. | 
**Platforms** | **List&lt;string&gt;** | Platform and area slugs the entry is about: a platform (&#x60;instagram&#x60;, &#x60;facebook&#x60;, &#x60;threads&#x60;, &#x60;tiktok&#x60;, &#x60;x&#x60;, &#x60;linkedin&#x60;, &#x60;youtube&#x60;, &#x60;pinterest&#x60;, &#x60;reddit&#x60;, &#x60;bluesky&#x60;, &#x60;telegram&#x60;, &#x60;snapchat&#x60;, &#x60;whatsapp&#x60;, &#x60;discord&#x60;, &#x60;slack&#x60;, &#x60;google-business&#x60;, &#x60;imessage&#x60;), an ads platform (&#x60;meta-ads&#x60;, &#x60;google-ads&#x60;, &#x60;tiktok-ads&#x60;, &#x60;linkedin-ads&#x60;, &#x60;pinterest-ads&#x60;, &#x60;x-ads&#x60;) or an area (&#x60;ads&#x60;, &#x60;publishing&#x60;, &#x60;inbox&#x60;, &#x60;telephony&#x60;, &#x60;commerce&#x60;, &#x60;analytics&#x60;, &#x60;webhooks&#x60;, &#x60;general&#x60;). Filter with the &#x60;platform&#x60; query parameter. | 
**Message** | **string** | The announcement, in Markdown. | 
**PublishedAt** | **DateTime** |  | 
**SpecVersion** | **string** | The &#x60;info.version&#x60; of the OpenAPI spec the entry describes, when known. | 
**Url** | **string** | The entry on the docs changelog. | 
**Changes** | [**ApiChangelogEntryChanges**](ApiChangelogEntryChanges.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

