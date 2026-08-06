# Zernio.Model.AdFunnelCounts
Named conversion-funnel steps, resolved from the same data as `actions` so you never have to parse action-type strings yourself.  Meta reports one event under several action types at once (`offsite_conversion.fb_pixel_purchase`, `omni_purchase`, `purchase`, …). Each field below takes the FIRST family member present rather than summing them, which is what makes these counts safe to add up — summing the raw `actions` keys yourself double or triple counts. The same priority order backs `conversions`, so a purchase-optimised campaign reports the identical number in `conversions` and `funnel.purchases`.  Every field is 0 when that step never fired. Populated for Meta ads; other platforms report a different action taxonomy and generally leave these at 0 (read `actions` for those). At ad-set and campaign level each step is summed from its per-ad values. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**LandingPageViews** | **int** | Landing page views — the visitor actually loaded the destination, unlike a link click. Meta &#x60;landing_page_view&#x60;. | [optional] 
**ContentViews** | **int** | Content views (Meta &#x60;ViewContent&#x60; pixel event). | [optional] 
**Searches** | **int** | On-site searches (Meta &#x60;Search&#x60; pixel event). | [optional] 
**WishlistAdds** | **int** | Adds to wishlist (Meta &#x60;AddToWishlist&#x60; pixel event). | [optional] 
**CartAdds** | **int** | Adds to cart (Meta &#x60;AddToCart&#x60; pixel event). | [optional] 
**CheckoutsInitiated** | **int** | Checkouts started (Meta &#x60;InitiateCheckout&#x60; pixel event). | [optional] 
**PaymentInfoAdds** | **int** | Payment details added at checkout (Meta &#x60;AddPaymentInfo&#x60; pixel event). | [optional] 
**Purchases** | **int** | Purchases (Meta &#x60;Purchase&#x60; pixel event). Pair with &#x60;purchaseValue&#x60; for revenue. | [optional] 
**Leads** | **int** | Leads, from either the website pixel or an instant form — whichever the ad uses. | [optional] 
**RegistrationsCompleted** | **int** | Completed registrations (Meta &#x60;CompleteRegistration&#x60; pixel event). | [optional] 
**AppInstalls** | **int** | Mobile app installs attributed to the ad. | [optional] 
**MessagingConversationsStarted** | **int** | Messaging conversations started within 7 days — the headline metric for click-to-WhatsApp and click-to-Messenger ads. | [optional] 
**MessagingFirstReplies** | **int** | Messaging threads where the person sent a first reply. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

