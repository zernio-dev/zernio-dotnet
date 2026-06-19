# Zernio.Model.ListInboxConversations200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**AccountUsername** | **string** |  | [optional] 
**ParticipantId** | **string** |  | [optional] 
**ParticipantName** | **string** |  | [optional] 
**ParticipantPicture** | **string** |  | [optional] 
**ParticipantVerifiedType** | **string** | X/Twitter verified badge type. Only present for Twitter/X conversations. | [optional] 
**LastMessage** | **string** |  | [optional] 
**UpdatedTime** | **DateTime** |  | [optional] 
**Status** | **string** |  | [optional] 
**UnreadCount** | **int** | Number of unread messages | [optional] 
**Url** | **string** | Direct link to open the conversation on the platform (if available) | [optional] 
**InstagramProfile** | [**ListInboxConversations200ResponseDataInnerInstagramProfile**](ListInboxConversations200ResponseDataInnerInstagramProfile.md) |  | [optional] 
**Metadata** | **Dictionary&lt;string, string&gt;** | Ad-click attribution captured on the first inbound message of the conversation. Only present when the conversation originated from a click-to-message ad. Absent on organic conversations.  Two sources populate this field:   - WhatsApp CTWA (Click-to-WhatsApp): &#x60;ctwa_clid&#x60;, &#x60;ctwa_source_id&#x60;,     &#x60;ctwa_source_url&#x60;, &#x60;ctwa_headline&#x60;, &#x60;ctwa_source_type&#x60;, &#x60;ctwa_captured_at&#x60;.   - Facebook Messenger CTM / Instagram CTD: &#x60;meta_ad_id&#x60;, &#x60;meta_ad_title&#x60;,     &#x60;meta_ad_source&#x60;, &#x60;meta_ad_type&#x60;, &#x60;meta_ad_ref&#x60;, &#x60;meta_ad_captured_at&#x60;,     &#x60;meta_ad_photo_url&#x60;, &#x60;meta_ad_video_url&#x60;, &#x60;meta_ad_post_id&#x60;,     &#x60;meta_ad_product_id&#x60;, &#x60;meta_ad_flow_id&#x60;.  Note: &#x60;meta_ad_photo_url&#x60; and &#x60;meta_ad_video_url&#x60; are Facebook CDN URLs that may expire. Use &#x60;meta_ad_id&#x60; for a permanent reference to the ad.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

