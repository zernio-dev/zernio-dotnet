# Zernio.Model.MessagingCarouselCard
One card of a messaging ad carousel (Meta link_data.child_attachments). Every card opens the same conversation, so a card has no link of its own.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ImageUrl** | **string** | Card image. Uploaded to the ad account and sent as the card image_hash (by URL on validateOnly). | 
**Headline** | **string** | Card title (Meta name). | [optional] 
**Description** | **string** | Card description, under the title. | [optional] 
**CallToAction** | **string** | Optional. Must equal the destination&#39;s messaging call to action (WHATSAPP_MESSAGE for whatsapp, MESSAGE_PAGE for messenger, INSTAGRAM_MESSAGE for instagram_direct; with &#x60;destinations&#x60; the first one listed). Any other value is a 400 naming the card, because Meta refuses a carousel whose cards do not all open the destination. | [optional] 
**LinkUrl** | **string** | Not accepted: a 400. The card tap opens the conversation, not a website. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

