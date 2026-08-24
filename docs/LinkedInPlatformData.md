# Zernio.Model.LinkedInPlatformData
Up to 20 images, no multi-video. Single PDF supported (max 100MB). Link previews auto-generated when no media attached. Use organizationUrn for multi-org posting. Geo-restriction only works for organization pages (not personal profiles) and requires the targeted audience to exceed 300 followers. Polls are supported via the poll object: 2-4 options, cannot be combined with media or reshareUrl, cannot be edited after publishing, and API-created polls are non-sponsored only. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DocumentTitle** | **string** | Title displayed on LinkedIn document (PDF/carousel) posts. Required by LinkedIn for document posts. If omitted, falls back to the media item title, then the filename. | [optional] 
**OrganizationUrn** | **string** | Target LinkedIn Organization URN (e.g. \&quot;urn:li:organization:123456789\&quot;). If omitted, uses the default org. Use GET /v1/accounts/{id}/linkedin-organizations to list orgs. | [optional] 
**FirstComment** | **string** | Optional first comment to add after the post is created | [optional] 
**DisableLinkPreview** | **bool** | Set to true to disable automatic link previews for URLs in the post content (default is false) | [optional] 
**ReshareUrl** | **string** | LinkedIn post link to repost (use the post&#39;s \&quot;Copy link to post\&quot; action), or a urn:li:share / urn:li:ugcPost / urn:li:groupPost URN. The published post is always a reshare authored by your account with the original embedded underneath: with content your text is the commentary (LinkedIn&#39;s \&quot;repost with your thoughts\&quot;), and with no content it publishes as a text-free reshare. Note that a text-free reshare is NOT LinkedIn&#39;s one-click \&quot;Repost\&quot; (the feed treatment where the original author stays the author); LinkedIn&#39;s API exposes no way to create that, so the post still appears authored by you with the original embedded. Mutually exclusive with media. Works on personal profiles and organization pages. | [optional] 
**GeoRestriction** | [**GeoRestriction**](GeoRestriction.md) |  | [optional] 
**Poll** | [**LinkedInPlatformDataPoll**](LinkedInPlatformDataPoll.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

