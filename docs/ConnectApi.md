# Zernio.Api.ConnectApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AssignGoogleBusinessLocation**](ConnectApi.md#assigngooglebusinesslocation) | **POST** /v1/accounts/{accountId}/gmb-locations/assign | Assign Google Business Profile location to another profile |
| [**CompleteMetaAdsBusinessLogin**](ConnectApi.md#completemetaadsbusinesslogin) | **GET** /v1/connect/meta-ads/callback | Complete Meta business login |
| [**CompleteTelegramConnect**](ConnectApi.md#completetelegramconnect) | **PATCH** /v1/connect/telegram | Check Telegram status |
| [**CompleteWhatsAppPhoneSelection**](ConnectApi.md#completewhatsappphoneselection) | **POST** /v1/connect/whatsapp/select-phone-number | Complete number selection |
| [**ConfigureTikTokAdsBrandIdentity**](ConnectApi.md#configuretiktokadsbrandidentity) | **PATCH** /v1/connect/tiktok-ads | Set TikTok brand identity |
| [**ConnectAds**](ConnectApi.md#connectads) | **GET** /v1/connect/{platform}/ads | Connect ads for a platform |
| [**ConnectBlueskyCredentials**](ConnectApi.md#connectblueskycredentials) | **POST** /v1/connect/bluesky/credentials | Connect Bluesky account |
| [**ConnectDiscordChannel**](ConnectApi.md#connectdiscordchannel) | **POST** /v1/connect/discord | Connect a Discord channel |
| [**ConnectOpenAIAdsCredentials**](ConnectApi.md#connectopenaiadscredentials) | **POST** /v1/connect/openai-ads/credentials | Connect an OpenAI Ads account |
| [**ConnectShopifyWithToken**](ConnectApi.md#connectshopifywithtoken) | **POST** /v1/connect/shopify/token | Connect a Shopify store with a custom-app Admin token |
| [**ConnectSlackChannel**](ConnectApi.md#connectslackchannel) | **POST** /v1/connect/slack | Connect a Slack channel |
| [**ConnectWebflowWithSiteToken**](ConnectApi.md#connectwebflowwithsitetoken) | **POST** /v1/connect/webflow/token | Connect Webflow with a site API token |
| [**ConnectWhatsAppCredentials**](ConnectApi.md#connectwhatsappcredentials) | **POST** /v1/connect/whatsapp/credentials | Connect WhatsApp via credentials |
| [**ConnectWhatsAppEmbeddedSignup**](ConnectApi.md#connectwhatsappembeddedsignup) | **POST** /v1/connect/whatsapp/embedded-signup | Connect WhatsApp from Embedded Signup |
| [**ConnectWhopAdsCredentials**](ConnectApi.md#connectwhopadscredentials) | **POST** /v1/connect/whop-ads/credentials | Connect a Whop account |
| [**ConnectWordPressWithApplicationPassword**](ConnectApi.md#connectwordpresswithapplicationpassword) | **POST** /v1/connect/wordpress/token | Connect self-hosted WordPress with an application password |
| [**CreateOAuthApp**](ConnectApi.md#createoauthapp) | **POST** /v1/connect/oauth-apps | Add an OAuth app |
| [**CreatePinterestBoard**](ConnectApi.md#createpinterestboard) | **POST** /v1/accounts/{accountId}/pinterest-boards | Create Pinterest board |
| [**CreateYoutubePlaylist**](ConnectApi.md#createyoutubeplaylist) | **POST** /v1/accounts/{accountId}/youtube-playlists | Create YouTube playlist |
| [**DeleteOAuthApp**](ConnectApi.md#deleteoauthapp) | **DELETE** /v1/connect/oauth-apps/{appId} | Remove an OAuth app |
| [**GetConnectHandoff**](ConnectApi.md#getconnecthandoff) | **GET** /v1/connect/handoffs/{handoffId} | Get a phone handoff |
| [**GetConnectUrl**](ConnectApi.md#getconnecturl) | **GET** /v1/connect/{platform} | Get OAuth connect URL |
| [**GetConnectWelcomeScreen**](ConnectApi.md#getconnectwelcomescreen) | **GET** /v1/connect/welcome-screen | Get the saved welcome screen |
| [**GetFacebookPages**](ConnectApi.md#getfacebookpages) | **GET** /v1/accounts/{accountId}/facebook-page | List Facebook pages |
| [**GetGmbLocations**](ConnectApi.md#getgmblocations) | **GET** /v1/accounts/{accountId}/gmb-locations | List Google Business Profile locations |
| [**GetGoogleAnalyticsConnectUrl**](ConnectApi.md#getgoogleanalyticsconnecturl) | **GET** /v1/connect/googleanalytics | Get Google Analytics OAuth connect URL |
| [**GetHubSpotConnectUrl**](ConnectApi.md#gethubspotconnecturl) | **GET** /v1/connect/hubspot | Get HubSpot OAuth connect URL |
| [**GetLinkedInOrganizations**](ConnectApi.md#getlinkedinorganizations) | **GET** /v1/accounts/{accountId}/linkedin-organizations | List LinkedIn orgs |
| [**GetOAuthApp**](ConnectApi.md#getoauthapp) | **GET** /v1/connect/oauth-apps/{appId} | Get an OAuth app |
| [**GetPageWebhookSubscription**](ConnectApi.md#getpagewebhooksubscription) | **GET** /v1/accounts/{accountId}/webhook-subscription | Read a Facebook Page&#39;s webhook subscription |
| [**GetPendingOAuthData**](ConnectApi.md#getpendingoauthdata) | **GET** /v1/connect/pending-data | Get pending OAuth data |
| [**GetPinterestBoards**](ConnectApi.md#getpinterestboards) | **GET** /v1/accounts/{accountId}/pinterest-boards | List Pinterest boards |
| [**GetRedditFlairs**](ConnectApi.md#getredditflairs) | **GET** /v1/accounts/{accountId}/reddit-flairs | List subreddit flairs |
| [**GetRedditSubreddits**](ConnectApi.md#getredditsubreddits) | **GET** /v1/accounts/{accountId}/reddit-subreddits | List Reddit subreddits |
| [**GetShopifyConnectUrl**](ConnectApi.md#getshopifyconnecturl) | **GET** /v1/connect/shopify | Get Shopify OAuth connect URL |
| [**GetSubredditRules**](ConnectApi.md#getsubredditrules) | **GET** /v1/accounts/{accountId}/reddit-subreddits/{subreddit}/rules | Get subreddit rules |
| [**GetTelegramConnectStatus**](ConnectApi.md#gettelegramconnectstatus) | **GET** /v1/connect/telegram | Generate Telegram code |
| [**GetWebflowConnectUrl**](ConnectApi.md#getwebflowconnecturl) | **GET** /v1/connect/webflow | Get Webflow OAuth URL |
| [**GetWhatsAppSdkConfig**](ConnectApi.md#getwhatsappsdkconfig) | **GET** /v1/connect/whatsapp/sdk-config | Get Embedded Signup SDK config |
| [**GetWixConnectUrl**](ConnectApi.md#getwixconnecturl) | **GET** /v1/connect/wix | Get Wix site install URL |
| [**GetWordPressAuthUrl**](ConnectApi.md#getwordpressauthurl) | **GET** /v1/connect/wordpress | Get WordPress.com OAuth connect URL |
| [**GetYoutubeCaptions**](ConnectApi.md#getyoutubecaptions) | **GET** /v1/accounts/{accountId}/youtube-captions | Get a YouTube video transcript |
| [**GetYoutubePlaylists**](ConnectApi.md#getyoutubeplaylists) | **GET** /v1/accounts/{accountId}/youtube-playlists | List YouTube playlists |
| [**HandleOAuthCallback**](ConnectApi.md#handleoauthcallback) | **POST** /v1/connect/{platform} | Complete OAuth callback |
| [**InitiateTelegramConnect**](ConnectApi.md#initiatetelegramconnect) | **POST** /v1/connect/telegram | Connect Telegram directly |
| [**ListFacebookPages**](ConnectApi.md#listfacebookpages) | **GET** /v1/connect/facebook/select-page | List Facebook pages |
| [**ListGoogleAnalyticsProperties**](ConnectApi.md#listgoogleanalyticsproperties) | **GET** /v1/connect/googleanalytics/properties | List Google Analytics properties for a pending connect |
| [**ListGoogleBusinessLocations**](ConnectApi.md#listgooglebusinesslocations) | **GET** /v1/connect/googlebusiness/locations | List Google Business Profile locations |
| [**ListInstagramPages**](ConnectApi.md#listinstagrampages) | **GET** /v1/connect/instagram/select-account | List Pages with a linked Instagram account |
| [**ListLinkedInOrganizations**](ConnectApi.md#listlinkedinorganizations) | **GET** /v1/connect/linkedin/organizations | List LinkedIn orgs |
| [**ListOAuthApps**](ConnectApi.md#listoauthapps) | **GET** /v1/connect/oauth-apps | List your OAuth apps |
| [**ListPinterestBoardsForSelection**](ConnectApi.md#listpinterestboardsforselection) | **GET** /v1/connect/pinterest/select-board | List Pinterest boards |
| [**ListSlackChannels**](ConnectApi.md#listslackchannels) | **GET** /v1/connect/slack | List Slack channels for the channel picker |
| [**ListSnapchatProfiles**](ConnectApi.md#listsnapchatprofiles) | **GET** /v1/connect/snapchat/select-profile | List Snapchat profiles |
| [**ListWhatsAppPhoneNumbers**](ConnectApi.md#listwhatsappphonenumbers) | **GET** /v1/connect/whatsapp/select-phone-number | List numbers for selection |
| [**ResyncPageWebhookSubscription**](ConnectApi.md#resyncpagewebhooksubscription) | **POST** /v1/accounts/{accountId}/webhook-subscription | Re-subscribe a Facebook Page to Zernio&#39;s webhooks |
| [**SelectFacebookPage**](ConnectApi.md#selectfacebookpage) | **POST** /v1/connect/facebook/select-page | Select Facebook page |
| [**SelectGoogleAnalyticsProperty**](ConnectApi.md#selectgoogleanalyticsproperty) | **POST** /v1/connect/googleanalytics/select-property | Connect the chosen Google Analytics property |
| [**SelectGoogleBusinessLocation**](ConnectApi.md#selectgooglebusinesslocation) | **POST** /v1/connect/googlebusiness/select-location | Select Google Business Profile location |
| [**SelectInstagramAccount**](ConnectApi.md#selectinstagramaccount) | **POST** /v1/connect/instagram/select-account | Select the Page whose Instagram account to connect |
| [**SelectLinkedInOrganization**](ConnectApi.md#selectlinkedinorganization) | **POST** /v1/connect/linkedin/select-organization | Select LinkedIn org |
| [**SelectPinterestBoard**](ConnectApi.md#selectpinterestboard) | **POST** /v1/connect/pinterest/select-board | Select Pinterest board |
| [**SelectSnapchatProfile**](ConnectApi.md#selectsnapchatprofile) | **POST** /v1/connect/snapchat/select-profile | Select Snapchat profile |
| [**SetRedditPostFlair**](ConnectApi.md#setredditpostflair) | **POST** /v1/accounts/{accountId}/reddit-flairs | Set Reddit post flair |
| [**StartMicrosoftAdminConsent**](ConnectApi.md#startmicrosoftadminconsent) | **GET** /v1/connect/microsoft/admin-consent | Admin-consent link for a Microsoft tenant |
| [**TestOAuthApp**](ConnectApi.md#testoauthapp) | **POST** /v1/connect/oauth-apps/{appId}/test | Check an OAuth app&#39;s keys |
| [**UpdateConnectWelcomeScreen**](ConnectApi.md#updateconnectwelcomescreen) | **PUT** /v1/connect/welcome-screen | Save the welcome screen |
| [**UpdateFacebookPage**](ConnectApi.md#updatefacebookpage) | **PUT** /v1/accounts/{accountId}/facebook-page | Update Facebook page |
| [**UpdateGmbLocation**](ConnectApi.md#updategmblocation) | **PUT** /v1/accounts/{accountId}/gmb-locations | Update Google Business Profile location |
| [**UpdateLinkedInOrganization**](ConnectApi.md#updatelinkedinorganization) | **PUT** /v1/accounts/{accountId}/linkedin-organization | Switch LinkedIn account type |
| [**UpdateOAuthApp**](ConnectApi.md#updateoauthapp) | **PATCH** /v1/connect/oauth-apps/{appId} | Update an OAuth app |
| [**UpdatePinterestBoards**](ConnectApi.md#updatepinterestboards) | **PUT** /v1/accounts/{accountId}/pinterest-boards | Set default Pinterest board |
| [**UpdateRedditSubreddits**](ConnectApi.md#updateredditsubreddits) | **PUT** /v1/accounts/{accountId}/reddit-subreddits | Set default subreddit |
| [**UpdateYoutubeDefaultPlaylist**](ConnectApi.md#updateyoutubedefaultplaylist) | **PUT** /v1/accounts/{accountId}/youtube-playlists | Set default YouTube playlist |
| [**VoteRedditThing**](ConnectApi.md#voteredditthing) | **POST** /v1/accounts/{accountId}/reddit-vote | Vote on a Reddit post or comment |

<a id="assigngooglebusinesslocation"></a>
# **AssignGoogleBusinessLocation**
> AssignGoogleBusinessLocation200Response AssignGoogleBusinessLocation (string accountId, AssignGoogleBusinessLocationRequest assignGoogleBusinessLocationRequest)

Assign Google Business Profile location to another profile

Connect a Google Business Profile location onto a DIFFERENT profile by reusing the OAuth grant from an already-connected Google Business Profile account, with no browser and no re-authorization.  Built for agencies whose single Google account has manager access to many client locations and who run one profile per client:  1. Connect one location the normal way (browser OAuth). 2. Bulk-assign the rest onto each client's profile via this endpoint.  ### Parameters  - The path `accountId` is a SOURCE connected Google Business Profile account (the token holder). - The body `profileId` is the TARGET profile, which may already hold other locations.  Assigning a location the target profile already holds refreshes that account. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class AssignGoogleBusinessLocationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | A source connected Google Business Profile account whose OAuth grant is reused.
            var assignGoogleBusinessLocationRequest = new AssignGoogleBusinessLocationRequest(); // AssignGoogleBusinessLocationRequest | 

            try
            {
                // Assign Google Business Profile location to another profile
                AssignGoogleBusinessLocation200Response result = apiInstance.AssignGoogleBusinessLocation(accountId, assignGoogleBusinessLocationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.AssignGoogleBusinessLocation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AssignGoogleBusinessLocationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Assign Google Business Profile location to another profile
    ApiResponse<AssignGoogleBusinessLocation200Response> response = apiInstance.AssignGoogleBusinessLocationWithHttpInfo(accountId, assignGoogleBusinessLocationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.AssignGoogleBusinessLocationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | A source connected Google Business Profile account whose OAuth grant is reused. |  |
| **assignGoogleBusinessLocationRequest** | [**AssignGoogleBusinessLocationRequest**](AssignGoogleBusinessLocationRequest.md) |  |  |

### Return type

[**AssignGoogleBusinessLocation200Response**](AssignGoogleBusinessLocation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Location assigned to the target profile |  -  |
| **400** | Invalid body, selected location not found under the Google account, or the provided googleAccountId is not one of the accounts this connection manages |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Payment required, or target profile exceeds plan limit |  -  |
| **404** | Source Google Business Profile account not found |  -  |
| **409** | Conflict with an existing connection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="completemetaadsbusinesslogin"></a>
# **CompleteMetaAdsBusinessLogin**
> void CompleteMetaAdsBusinessLogin (string state, string? code = null, string? error = null)

Complete Meta business login

Finishes a Meta business login after the user approves access, connects the Meta ads account and sends them back to your app.  This is the Facebook Login for Business redirect target. Meta supplies the single-use authorization code and the authenticated state returned by connectAds. No bearer token is sent by the browser.  The state expires after 30 minutes and binds the user, profile, Page selection and ad-account scope.  ### Outcomes  - Success reconnects only metaads and redirects to the original redirect_url. - Invalid state returns 400. - Inaccessible profiles or missing ads access cannot connect. - Dashboard logins with several Pages redirect to the Facebook Page picker with an encrypted selectionToken valid for ten minutes. Listing and selecting require the initiating user and current profile access.  No plaintext platform token is returned to the browser. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class CompleteMetaAdsBusinessLoginExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var state = ENCRYPTED_STATE;  // string | Authenticated state from the initial connectAds response.
            var code = "code_example";  // string? | Single-use authorization code returned by Meta. (optional) 
            var error = "error_example";  // string? | Meta authorization error when the user declines the dialog. (optional) 

            try
            {
                // Complete Meta business login
                apiInstance.CompleteMetaAdsBusinessLogin(state, code, error);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.CompleteMetaAdsBusinessLogin: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CompleteMetaAdsBusinessLoginWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Complete Meta business login
    apiInstance.CompleteMetaAdsBusinessLoginWithHttpInfo(state, code, error);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.CompleteMetaAdsBusinessLoginWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **state** | **string** | Authenticated state from the initial connectAds response. |  |
| **code** | **string?** | Single-use authorization code returned by Meta. | [optional]  |
| **error** | **string?** | Meta authorization error when the user declines the dialog. | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **307** | Redirect to the original callback URL with connected&#x3D;metaads, profileId and accountId on success; authorization denial redirects with an error. Dashboard logins requiring a Page choice redirect to /connect/facebook/select-page with selectionToken. |  * Location -  <br>  |
| **400** | Invalid request |  -  |
| **403** | Ads access or profile access required. |  -  |
| **409** | The new token grants do not match the existing connection, or its previous grants cannot be verified. |  -  |
| **503** | Business login state signing is not configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="completetelegramconnect"></a>
# **CompleteTelegramConnect**
> CompleteTelegramConnect200Response CompleteTelegramConnect (string code)

Check Telegram status

Poll this endpoint to check if a Telegram access code has been used to connect a channel/group. Recommended polling interval: 3 seconds. Status values: pending (waiting for user), connected (channel/group linked), expired (generate a new code). 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class CompleteTelegramConnectExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var code = ZRN-ABC123;  // string | The access code to check status for

            try
            {
                // Check Telegram status
                CompleteTelegramConnect200Response result = apiInstance.CompleteTelegramConnect(code);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.CompleteTelegramConnect: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CompleteTelegramConnectWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check Telegram status
    ApiResponse<CompleteTelegramConnect200Response> response = apiInstance.CompleteTelegramConnectWithHttpInfo(code);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.CompleteTelegramConnectWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The access code to check status for |  |

### Return type

[**CompleteTelegramConnect200Response**](CompleteTelegramConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connection status |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Code not found |  -  |
| **500** | Internal error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="completewhatsappphoneselection"></a>
# **CompleteWhatsAppPhoneSelection**
> CompleteWhatsAppPhoneSelection200Response CompleteWhatsAppPhoneSelection (CompleteWhatsAppPhoneSelectionRequest completeWhatsAppPhoneSelectionRequest, string? xConnectToken = null)

Complete number selection

Bind a specific WhatsApp phone number to the Zernio profile after the user picks one from `listWhatsAppPhoneNumbers`. Exchanges the short-lived OAuth token for a long-lived token, subscribes the WABA to webhooks, and creates the SocialAccount. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class CompleteWhatsAppPhoneSelectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var completeWhatsAppPhoneSelectionRequest = new CompleteWhatsAppPhoneSelectionRequest(); // CompleteWhatsAppPhoneSelectionRequest | 
            var xConnectToken = "xConnectToken_example";  // string? | Alternative auth for API users' end customers (optional) 

            try
            {
                // Complete number selection
                CompleteWhatsAppPhoneSelection200Response result = apiInstance.CompleteWhatsAppPhoneSelection(completeWhatsAppPhoneSelectionRequest, xConnectToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.CompleteWhatsAppPhoneSelection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CompleteWhatsAppPhoneSelectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Complete number selection
    ApiResponse<CompleteWhatsAppPhoneSelection200Response> response = apiInstance.CompleteWhatsAppPhoneSelectionWithHttpInfo(completeWhatsAppPhoneSelectionRequest, xConnectToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.CompleteWhatsAppPhoneSelectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **completeWhatsAppPhoneSelectionRequest** | [**CompleteWhatsAppPhoneSelectionRequest**](CompleteWhatsAppPhoneSelectionRequest.md) |  |  |
| **xConnectToken** | **string?** | Alternative auth for API users&#39; end customers | [optional]  |

### Return type

[**CompleteWhatsAppPhoneSelection200Response**](CompleteWhatsAppPhoneSelection200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Phone number connected successfully |  -  |
| **400** | Missing required fields (profileId, phoneNumberId, wabaId, or tempToken) |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Profile limit exceeded for the user&#39;s plan (PROFILE_LIMIT_EXCEEDED) |  -  |
| **404** | Selected phone number not found in the specified WABA |  -  |
| **409** | Conflict with an existing connection. A number can only be live on one profile. One of:  - **WHATSAPP_NUMBER_PINNED_TO_PROFILE:** the number is a Zernio-provisioned number pinned to a different profile. Connect it from that profile, or move it first with PATCH /v1/whatsapp/phone-numbers/{id}/profile. - **WHATSAPP_NUMBER_ALREADY_CONNECTED:** the number is already actively connected on another profile or team. Disconnect it there first. - **WHATSAPP_COEXISTENCE_NOT_REGISTERED:** for a number connected from the WhatsApp Business app (coexistence), the phone never registered the number on the Cloud API. Meta reported it as platform_type ON_PREMISE and refused the contacts/history sync with error 133010.  In the coexistence case no account is created. The customer opens WhatsApp Business on the phone, keeps it open and updated, and runs the same Embedded Signup again, which in practice succeeds on the second attempt.  |  -  |
| **500** | Failed to bind phone number |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="configuretiktokadsbrandidentity"></a>
# **ConfigureTikTokAdsBrandIdentity**
> ConfigureTikTokAdsBrandIdentity200Response ConfigureTikTokAdsBrandIdentity (ConfigureTikTokAdsBrandIdentityRequest configureTikTokAdsBrandIdentityRequest)

Set TikTok brand identity

Set or update the Brand Identity (display name + avatar) for a `tiktokads` SocialAccount.  TikTok requires every ad to carry an `identity_id + identity_type` pair. The Brand Identity is the CUSTOMIZED_USER alternative to attributing ads to a real @username (TT_USER).  ### What this route does  1. Uploads the supplied image to TikTok. 2. Creates the identity via `/v2/identity/create/`. 3. Caches the resulting `identity_id` on the account, so subsequent `POST /v1/ads/create` calls can opt into it via `identityType: 'CUSTOMIZED_USER'`.  ### Linked accounts  Configurable on every `tiktokads` account, including linked-mode ones (those with a posting account on the same profile).  Configuration is idempotent and harmless when posting is also connected. The default ad-create path still prefers TT_USER, and CUSTOMIZED_USER is only used per-ad when the caller explicitly opts in.  ### Updating an identity  TikTok identities are immutable post-creation. Re-saving creates a new identity on TikTok and swaps the cached id. The old identity stays orphaned on TikTok's side (harmless, no billing impact).  Alternative: pass `brandIdentity` directly on `POST /v1/ads/create` to configure on first ad creation in a single round-trip. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ConfigureTikTokAdsBrandIdentityExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var configureTikTokAdsBrandIdentityRequest = new ConfigureTikTokAdsBrandIdentityRequest(); // ConfigureTikTokAdsBrandIdentityRequest | 

            try
            {
                // Set TikTok brand identity
                ConfigureTikTokAdsBrandIdentity200Response result = apiInstance.ConfigureTikTokAdsBrandIdentity(configureTikTokAdsBrandIdentityRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ConfigureTikTokAdsBrandIdentity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConfigureTikTokAdsBrandIdentityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set TikTok brand identity
    ApiResponse<ConfigureTikTokAdsBrandIdentity200Response> response = apiInstance.ConfigureTikTokAdsBrandIdentityWithHttpInfo(configureTikTokAdsBrandIdentityRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ConfigureTikTokAdsBrandIdentityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **configureTikTokAdsBrandIdentityRequest** | [**ConfigureTikTokAdsBrandIdentityRequest**](ConfigureTikTokAdsBrandIdentityRequest.md) |  |  |

### Return type

[**ConfigureTikTokAdsBrandIdentity200Response**](ConfigureTikTokAdsBrandIdentity200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Brand identity configured (or updated) |  -  |
| **400** | Missing fields, invalid JSON body, invalid accountId format, invalid lengths, or no advertiser found on the account |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | TikTok Ads account not found |  -  |
| **500** | Unexpected server error while caching the identity |  -  |
| **502** | TikTok rejected the image upload or the identity creation (type: platform_error; an upstream 4xx status is forwarded instead of 502) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="connectads"></a>
# **ConnectAds**
> ConnectAds200Response ConnectAds (string platform, string profileId, string? loginMode = null, string? permissionLevel = null, string? pageId = null, string? accountId = null, string? redirectUrl = null, bool? headless = null, bool? force = null, string? adAccountId = null, List<string>? adAccountIds = null)

Connect ads for a platform

Starts connecting a platform's ads account, giving you a dedicated ads connection to manage campaigns without touching posting accounts. It creates a dedicated ads SocialAccount for the specified platform.  Ads accounts appear as regular SocialAccount documents with ads platform values (e.g., metaads, tiktokads) in GET /v1/accounts.  ### Meta business login (opt-in)  Set `loginMode=business` for `facebook` or `instagram` to use Facebook Login for Business and a Business Integration System User token. No posting account is created or required.  This mode always returns an authUrl. It returns 503 when the server has no META_ADS_CONFIG_ID. Complete the dialog in a browser.  The callback creates or reconnects only the metaads account, preserving its ID and history. Non-empty successful subscription results replace subscribedAdAccountIds to remove stale grants; an empty result leaves routing unchanged.  #### Reconnecting  A reconnect is accepted when the new grant shares at least one ad account with the existing connection, so re-running the dialog can add, drop or swap ad accounts.  The existing connection's ad accounts are its scopedAdAccountIds plus the previous grant, or the ad accounts its old token can read when neither is stored.  - A grant with zero overlap is refused before changing the account and redirects with `error=invalid_field_value` and `error_reason=reconnect_mismatch` (disconnect and connect again to switch). - When the previous ad accounts cannot be read at all, it redirects with `error=reconnect_required`.  On an accepted reconnect the scope is rebuilt from the new grant:  - `adAccountIds` passed on the re-auth become the scope. - Otherwise a stored scope keeps its ad accounts that are still granted, plus any granted for the first time. - An unscoped connection follows the new grant.  #### Page selection  Pass `pageId` to select a granted Page for creatives and lead forms. API integrations otherwise reuse the previous Page or the sole granted Page.  Multiple Pages without a selection return 400 with available Page IDs for API integrations; restart with pageId. Dashboard session logins use the sole current grant automatically, or open the existing Facebook Page picker for several grants, including reconnects. Selection completes the Meta Ads connection.  #### Result redirects  Success redirects with connected=metaads, profileId and accountId.  Every failure after Meta's dialog redirects to redirect_url (or the dashboard) with `error`, `platform=metaads`, `error_message`, `request_id` and `stage`, plus `is_user_fixable` and `error_reason` when known. `error` is the API error code:  - `invalid_field_value`, with `error_reason`:   - `no_pages_granted`: no Page ticked   - `page_not_granted`: pageId not in the grant   - `ad_accounts_not_granted`   - `reconnect_mismatch`: the grant shares no ad account with the existing connection - `reconnect_required`, `ads_addon_required`, `payment_required` and the profile gates of GET /v1/connect/{platform} - `invalid_state` with `error_reason=state_expired`: after the 30-minute window - `connection_failed`: Meta refuses the code (e.g. a replayed callback) - `meta_ads_authorization_denied`: a denial in the dialog, with the `platform_error*` params  Only a state that cannot be decrypted at all still answers 400 JSON, since it names no redirect_url.  #### Tokens  Business login reports metadata.tokenType=system-user in GET /v1/accounts. An absent Meta expires_in leaves tokenExpiresAt absent; no personal-token re-exchange occurs.  Subsequent classic requests can change the ad-account scope using the business token. force=true (or disconnecting the business connection first) switches the profile to the standard Facebook login; the ads account is then held by the user token.  ### Same-token platforms (facebook, instagram, linkedin, pinterest)  The ads SocialAccount (metaads, linkedinads, pinterestads) reuses the OAuth token of the parent posting account, but only when:  - an active parent exists, and - for facebook and instagram, its stored token carries ads_management and ads_read (linkedin and pinterest need no extra scope).  In that case no extra OAuth happens and the response is alreadyConnected: true.  When no such parent exists, or the scopes are missing, the endpoint returns an authUrl and a full OAuth round trip is required.  Errors:  - 400 RECONNECT_REQUIRED: a parent exists but carries no token usable for ad accounts - 403 ADS_ADDON_REQUIRED: no ads add-on (independently of the branch) - 402 PAYMENT_REQUIRED: the billing gate is closed (independently of the branch)  #### Meta Ads needs a Facebook Page  Connecting Meta Ads (via facebook or instagram) requires a Facebook Page. Not because the ad account is read through a Page, but because both parent posting accounts are:  - the facebook flow only offers Pages you manage - the instagram flow with loginMethod=facebook_login only offers Instagram accounts linked to one of those Pages  Without a Page there is no parent account to inherit a token from. A user who manages no Facebook Page cannot complete this connection, and the facebook flow ends with error=no_facebook_pages.  ### Separate-token platforms (tiktok, twitter)  Starts the platform-specific marketing API OAuth flow and creates an ads SocialAccount (tiktokads, xads) with its own token. If the ads account already exists, returns alreadyConnected: true.  - twitter (X Ads): accountId is REQUIRED. There's no ads-only mode, because tweets need to be authored by a real X user. - tiktok: accountId is OPTIONAL.  #### TikTok with or without accountId  - With accountId, the new tiktokads account links to that posting account (parentAccountId set), so Spark Ads + standalone ads using the posting TT_USER identity become available. - Without accountId, ads-only mode kicks in: the new tiktokads account has parentAccountId=null and standalone ads use a synthetic CUSTOMIZED_USER (\"Brand Identity\"). Spark Ads are unavailable because TikTok requires a posting account for them.  The Brand Identity is configured separately via PATCH /v1/connect/tiktok-ads (or inline on POST /v1/ads/create via the brandIdentity field).  ### Standalone platforms (googleads)  Starts the Google Ads OAuth flow and creates a standalone ads SocialAccount (googleads) with no parent.  - If the account already exists and has at least one discovered Google Ads customer account, returns alreadyConnected: true. - When the existing connection has zero customer accounts (metadata.googleAdsCustomerIds is empty) or is flagged needsReconnection, it returns an authUrl instead. Completing it reconnects the same account (same accountId) and re-runs ad account discovery.  Discovery includes the client accounts under every manager (MCC) the Google user can reach. It also includes Google Ads test accounts, which Google always reports with status CLOSED.  When discovery finds no usable customer account, the callback saves nothing and redirects with `error=google_ads_no_ad_accounts`, `platform=googleads` and an `error_message`.  The message names each customer the Google user can reach and why it was left out (for example CUSTOMER_NOT_ENABLED). Sign in with a Google user that has access to the ad account or to its manager account.  When the user unticks the Google Ads permission on Google's consent screen, the callback saves nothing and redirects with `error=missing_google_permissions`, `platform=googleads`, `is_user_fixable=true` and `missing_scopes`.  An existing connection whose token lacks that permission is flagged needsReconnection, and the health endpoints report \"Google Ads permission not granted\". This endpoint then returns an authUrl for it.  ### Standalone platforms (redditads)  Starts the Reddit Ads OAuth flow (Reddit permissions `adsread`, `adsedit` and `adsconversions`) and creates a standalone ads SocialAccount (redditads) with no parent, separate from any organic `reddit` posting account. It is reached only as `redditads` in the path.  If an active Reddit Ads connection already exists on the profile, is not flagged needsReconnection and holds every one of those permissions, returns alreadyConnected: true. Otherwise it returns an authUrl; completing it reconnects the same account (same accountId).  A connection authorized without `adsconversions` keeps managing ads, but:  - the health endpoints list an issue asking to reconnect Reddit Ads and allow every permission - the Conversions API answers 403 `reconnect_required` - this endpoint returns an authUrl for it  Discovery lists every Reddit ad account the Reddit user can reach. The callback redirects with `platform=redditads` and:  - `error=reddit_ads_scope_not_granted`: the user unticks `adsread` or `adsedit` on Reddit's consent screen (nothing is saved) - `error=reddit_ads_no_ad_accounts`: the user reaches no Reddit ad account  Without `redirect_url` the browser lands on the Zernio dashboard's ad account picker for the new connection. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ConnectAdsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var platform = "facebook";  // string | Platform to connect ads for. Only platforms with ads support are accepted.  In classic mode, `instagram` requires an Instagram account connected with loginMethod=facebook_login whose token carries ads_management and ads_read. With an account connected through the default instagram_login flow no ads account can be created; do not use this value for those accounts. 
            var profileId = "profileId_example";  // string | Your Zernio profile ID
            var loginMode = business;  // string? | Meta ads authorization mode. Business login is opt-in for Facebook and Instagram; classic preserves the posting-account flow. (optional)  (default to classic)
            var permissionLevel = advertise;  // string? | Business login only. Ad-account permission the connection's system user will hold.  - `full`: asks the owner for Full control (MANAGE). Required to create pixels and other account-level assets through Zernio. - `advertise`: asks for Manage campaigns (ADVERTISE), enough for campaigns, ad sets, creatives, ads, media and reporting. For owners who will not grant billing-level control to an integration.  Either way, Meta only lets a business admin complete the grant. 503 if the advertise configuration is not set up.  (optional)  (default to full)
            var pageId = 811889972008357;  // string? | Business login only. Facebook Page ID to select from the token grants for ad creatives and lead forms. (optional) 
            var accountId = "accountId_example";  // string? | Existing SocialAccount ID.  - `twitter` (X Ads): required. - `tiktok`: optional. Omit it for ads-only mode (no TikTok posting account linked; ad creation uses a Brand Identity instead of a TT_USER). - Same-token platforms (`facebook`, `instagram`, `linkedin`, `pinterest`): picks which posting account the ads connection uses when the profile holds several of that platform. With one, it can be omitted. - Standalone platforms (`googleads`, `redditads`): ignored.  On same-token platforms, an id that names no active account of the platform on the profile is ignored. Exception: with `force=true`, when it names the posting account the profile's ads connection hangs off, that account is no longer connected.  In that case the call returns 409 `reconnect_required` instead of reconnecting another account. Reconnect it via GET /v1/connect/{platform} first.  (optional) 
            var redirectUrl = "redirectUrl_example";  // string? | Custom URL the browser is sent to once the OAuth flow finishes. When omitted, the browser lands on the Zernio dashboard. Honored on every ads platform, including the separate-token (`tiktok`, `twitter`) and standalone (`googleads`, `redditads`) flows.  MUST be an absolute http(s) URL or a custom app scheme for mobile deeplinks (e.g. myapp://callback). A relative path is rejected with 400 INVALID_REDIRECT_URL.  On success:  - `tiktok`: lands on the URL unchanged. - `twitter`, `googleads` and `redditads`: append `connected` (the ads platform id: `xads`, `googleads` or `redditads`), `profileId`, `accountId` (the ads connection) and `username`. - Same-token platforms (`facebook`, `instagram`, `linkedin`, `pinterest`): append `connected`, `profileId`, `accountId`, `username` and, on API-key calls, `connect_token`.  On failure the same error contract applies as on GET /v1/connect/{platform}: `error` and `platform` are always appended, other params are optional, and the value list there is not exhaustive.  On the tiktok, twitter, googleads and redditads flows, `platform` carries the ads platform id (`tiktokads`, `xads`, `googleads`, `redditads`), not the value used in the request path.  (optional) 
            var headless = false;  // bool? | Enable headless mode (same-token platforms only) (optional)  (default to false)
            var force = false;  // bool? | Force a fresh OAuth even when an account already exists.  Normally the endpoint returns `alreadyConnected: true` whenever a connected account is found, keyed off its active state rather than token liveness. Set `force=true` to bypass that and always receive an `authUrl`. Completing the returned OAuth refreshes the stored token on the existing posting and ads accounts in place.  An `alreadyConnected` response re-runs ad discovery and webhook subscriptions in the background at most once every 15 minutes per ads account (always when the call changes the ad-account scope), so it is not a sync trigger.  To check the connection's health, read GET /v1/ads/accounts?accountId=<ads account ID>.  (optional)  (default to false)
            var adAccountId = act_1330190928038136;  // string? | Scopes ad sync to a single platform ad account. Without it, sync covers every ad account the connected token can see. For multiple accounts use `adAccountIds` instead.  Supported on:  - `facebook`/`instagram` (Meta): `act_<digits>`. - `linkedin`: bare numeric sponsored-account id. - `googleads`: bare customer id digits. - `redditads`: Reddit ad account id, `a2_<id>` or `t2_<id>`. - `twitter` (X Ads): base36 account id.  `tiktok` scopes advertisers at OAuth and `pinterest` has no ads discovery, so both ignore it.  **Meta validation** against the connected token:  - An id the token cannot see returns 400 `invalid_field_value`. - An id it can see but that Meta marks unusable for ads (disabled, closed, under risk review, settlement pending) returns 400 `ad_account_unusable` with `details.accountStatus` (Meta's `account_status`) and, when Meta gives one, `details.disableReason`. - Unsettled and in-grace accounts are accepted, matching the `selectable` flag of `GET /v1/ads/accounts`.  **Effects**: setting a scope removes already synced ads, campaigns, ad sets and keywords from de-scoped ad accounts. On Meta it also decides which ad accounts Zernio subscribes to ad-account webhooks: only the scoped ones, instead of every ad account the login can reach.  **Through OAuth**: on Meta the scope is kept when this call returns an `authUrl`, so the Meta Ads account created after OAuth is scoped (only its scoped ad accounts synced and subscribed) from the start.  On `googleads` and `redditads` it is kept through OAuth when `redirect_url` is set, so the new connection syncs only scoped ad accounts from the first sync.  **Reconnects**: business-login reconnects preserve the existing scope; supplied IDs are checked against the new grant. To change the scope after migration, call this endpoint with the IDs and omit loginMode.  (optional) 
            var adAccountIds = new List<string>?(); // List<string>? | Scope ad sync to multiple platform ad accounts (same platform support and id shapes as `adAccountId`). Repeat the param (`?adAccountIds=act_1&adAccountIds=act_2`) or comma-separate (`?adAccountIds=act_1,act_2`).  - Persisted server-side; the latest call wins. De-scoped ad accounts have their synced ads, campaigns, ad sets and keywords removed. - On Meta only the scoped ad accounts get webhook subscriptions, including when the call starts a fresh OAuth. - Omitting both `adAccountId` and `adAccountIds` keeps any previously persisted scope unchanged (no scope means every reachable ad account).  (optional) 

            try
            {
                // Connect ads for a platform
                ConnectAds200Response result = apiInstance.ConnectAds(platform, profileId, loginMode, permissionLevel, pageId, accountId, redirectUrl, headless, force, adAccountId, adAccountIds);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ConnectAds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConnectAdsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Connect ads for a platform
    ApiResponse<ConnectAds200Response> response = apiInstance.ConnectAdsWithHttpInfo(platform, profileId, loginMode, permissionLevel, pageId, accountId, redirectUrl, headless, force, adAccountId, adAccountIds);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ConnectAdsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **platform** | **string** | Platform to connect ads for. Only platforms with ads support are accepted.  In classic mode, &#x60;instagram&#x60; requires an Instagram account connected with loginMethod&#x3D;facebook_login whose token carries ads_management and ads_read. With an account connected through the default instagram_login flow no ads account can be created; do not use this value for those accounts.  |  |
| **profileId** | **string** | Your Zernio profile ID |  |
| **loginMode** | **string?** | Meta ads authorization mode. Business login is opt-in for Facebook and Instagram; classic preserves the posting-account flow. | [optional] [default to classic] |
| **permissionLevel** | **string?** | Business login only. Ad-account permission the connection&#39;s system user will hold.  - &#x60;full&#x60;: asks the owner for Full control (MANAGE). Required to create pixels and other account-level assets through Zernio. - &#x60;advertise&#x60;: asks for Manage campaigns (ADVERTISE), enough for campaigns, ad sets, creatives, ads, media and reporting. For owners who will not grant billing-level control to an integration.  Either way, Meta only lets a business admin complete the grant. 503 if the advertise configuration is not set up.  | [optional] [default to full] |
| **pageId** | **string?** | Business login only. Facebook Page ID to select from the token grants for ad creatives and lead forms. | [optional]  |
| **accountId** | **string?** | Existing SocialAccount ID.  - &#x60;twitter&#x60; (X Ads): required. - &#x60;tiktok&#x60;: optional. Omit it for ads-only mode (no TikTok posting account linked; ad creation uses a Brand Identity instead of a TT_USER). - Same-token platforms (&#x60;facebook&#x60;, &#x60;instagram&#x60;, &#x60;linkedin&#x60;, &#x60;pinterest&#x60;): picks which posting account the ads connection uses when the profile holds several of that platform. With one, it can be omitted. - Standalone platforms (&#x60;googleads&#x60;, &#x60;redditads&#x60;): ignored.  On same-token platforms, an id that names no active account of the platform on the profile is ignored. Exception: with &#x60;force&#x3D;true&#x60;, when it names the posting account the profile&#39;s ads connection hangs off, that account is no longer connected.  In that case the call returns 409 &#x60;reconnect_required&#x60; instead of reconnecting another account. Reconnect it via GET /v1/connect/{platform} first.  | [optional]  |
| **redirectUrl** | **string?** | Custom URL the browser is sent to once the OAuth flow finishes. When omitted, the browser lands on the Zernio dashboard. Honored on every ads platform, including the separate-token (&#x60;tiktok&#x60;, &#x60;twitter&#x60;) and standalone (&#x60;googleads&#x60;, &#x60;redditads&#x60;) flows.  MUST be an absolute http(s) URL or a custom app scheme for mobile deeplinks (e.g. myapp://callback). A relative path is rejected with 400 INVALID_REDIRECT_URL.  On success:  - &#x60;tiktok&#x60;: lands on the URL unchanged. - &#x60;twitter&#x60;, &#x60;googleads&#x60; and &#x60;redditads&#x60;: append &#x60;connected&#x60; (the ads platform id: &#x60;xads&#x60;, &#x60;googleads&#x60; or &#x60;redditads&#x60;), &#x60;profileId&#x60;, &#x60;accountId&#x60; (the ads connection) and &#x60;username&#x60;. - Same-token platforms (&#x60;facebook&#x60;, &#x60;instagram&#x60;, &#x60;linkedin&#x60;, &#x60;pinterest&#x60;): append &#x60;connected&#x60;, &#x60;profileId&#x60;, &#x60;accountId&#x60;, &#x60;username&#x60; and, on API-key calls, &#x60;connect_token&#x60;.  On failure the same error contract applies as on GET /v1/connect/{platform}: &#x60;error&#x60; and &#x60;platform&#x60; are always appended, other params are optional, and the value list there is not exhaustive.  On the tiktok, twitter, googleads and redditads flows, &#x60;platform&#x60; carries the ads platform id (&#x60;tiktokads&#x60;, &#x60;xads&#x60;, &#x60;googleads&#x60;, &#x60;redditads&#x60;), not the value used in the request path.  | [optional]  |
| **headless** | **bool?** | Enable headless mode (same-token platforms only) | [optional] [default to false] |
| **force** | **bool?** | Force a fresh OAuth even when an account already exists.  Normally the endpoint returns &#x60;alreadyConnected: true&#x60; whenever a connected account is found, keyed off its active state rather than token liveness. Set &#x60;force&#x3D;true&#x60; to bypass that and always receive an &#x60;authUrl&#x60;. Completing the returned OAuth refreshes the stored token on the existing posting and ads accounts in place.  An &#x60;alreadyConnected&#x60; response re-runs ad discovery and webhook subscriptions in the background at most once every 15 minutes per ads account (always when the call changes the ad-account scope), so it is not a sync trigger.  To check the connection&#39;s health, read GET /v1/ads/accounts?accountId&#x3D;&lt;ads account ID&gt;.  | [optional] [default to false] |
| **adAccountId** | **string?** | Scopes ad sync to a single platform ad account. Without it, sync covers every ad account the connected token can see. For multiple accounts use &#x60;adAccountIds&#x60; instead.  Supported on:  - &#x60;facebook&#x60;/&#x60;instagram&#x60; (Meta): &#x60;act_&lt;digits&gt;&#x60;. - &#x60;linkedin&#x60;: bare numeric sponsored-account id. - &#x60;googleads&#x60;: bare customer id digits. - &#x60;redditads&#x60;: Reddit ad account id, &#x60;a2_&lt;id&gt;&#x60; or &#x60;t2_&lt;id&gt;&#x60;. - &#x60;twitter&#x60; (X Ads): base36 account id.  &#x60;tiktok&#x60; scopes advertisers at OAuth and &#x60;pinterest&#x60; has no ads discovery, so both ignore it.  **Meta validation** against the connected token:  - An id the token cannot see returns 400 &#x60;invalid_field_value&#x60;. - An id it can see but that Meta marks unusable for ads (disabled, closed, under risk review, settlement pending) returns 400 &#x60;ad_account_unusable&#x60; with &#x60;details.accountStatus&#x60; (Meta&#39;s &#x60;account_status&#x60;) and, when Meta gives one, &#x60;details.disableReason&#x60;. - Unsettled and in-grace accounts are accepted, matching the &#x60;selectable&#x60; flag of &#x60;GET /v1/ads/accounts&#x60;.  **Effects**: setting a scope removes already synced ads, campaigns, ad sets and keywords from de-scoped ad accounts. On Meta it also decides which ad accounts Zernio subscribes to ad-account webhooks: only the scoped ones, instead of every ad account the login can reach.  **Through OAuth**: on Meta the scope is kept when this call returns an &#x60;authUrl&#x60;, so the Meta Ads account created after OAuth is scoped (only its scoped ad accounts synced and subscribed) from the start.  On &#x60;googleads&#x60; and &#x60;redditads&#x60; it is kept through OAuth when &#x60;redirect_url&#x60; is set, so the new connection syncs only scoped ad accounts from the first sync.  **Reconnects**: business-login reconnects preserve the existing scope; supplied IDs are checked against the new grant. To change the scope after migration, call this endpoint with the IDs and omit loginMode.  | [optional]  |
| **adAccountIds** | [**List&lt;string&gt;?**](string.md) | Scope ad sync to multiple platform ad accounts (same platform support and id shapes as &#x60;adAccountId&#x60;). Repeat the param (&#x60;?adAccountIds&#x3D;act_1&amp;adAccountIds&#x3D;act_2&#x60;) or comma-separate (&#x60;?adAccountIds&#x3D;act_1,act_2&#x60;).  - Persisted server-side; the latest call wins. De-scoped ad accounts have their synced ads, campaigns, ad sets and keywords removed. - On Meta only the scoped ad accounts get webhook subscriptions, including when the call starts a fresh OAuth. - Omitting both &#x60;adAccountId&#x60; and &#x60;adAccountIds&#x60; keeps any previously persisted scope unchanged (no scope means every reachable ad account).  | [optional]  |

### Return type

[**ConnectAds200Response**](ConnectAds200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Either an OAuth URL to redirect to, or confirmation that ads are already connected |  -  |
| **400** | Platform doesn&#39;t support ads, missing accountId for X Ads, or a non-absolute redirect_url |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or no access to profile |  -  |
| **404** | Profile or posting account not found |  -  |
| **409** | Conflict. One of:  - The Business Login connection needs reconnecting: reconnect it with loginMode&#x3D;business, or pass force&#x3D;true or disconnect it first to switch to the standard login. - ambiguous_account: the profile holds several active accounts of the platform and no accountId names one. - reconnect_required: force&#x3D;true names the posting account the ads connection hangs off, and it is no longer connected.  |  -  |
| **503** | Business login is not configured or the platform is temporarily unavailable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="connectblueskycredentials"></a>
# **ConnectBlueskyCredentials**
> ConnectBlueskyCredentials200Response ConnectBlueskyCredentials (ConnectBlueskyCredentialsRequest connectBlueskyCredentialsRequest)

Connect Bluesky account

Connect a Bluesky account using identifier (handle or email) and an app password. To get your userId for the state parameter, call GET /v1/users which includes a currentUserId field. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ConnectBlueskyCredentialsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var connectBlueskyCredentialsRequest = new ConnectBlueskyCredentialsRequest(); // ConnectBlueskyCredentialsRequest | 

            try
            {
                // Connect Bluesky account
                ConnectBlueskyCredentials200Response result = apiInstance.ConnectBlueskyCredentials(connectBlueskyCredentialsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ConnectBlueskyCredentials: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConnectBlueskyCredentialsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Connect Bluesky account
    ApiResponse<ConnectBlueskyCredentials200Response> response = apiInstance.ConnectBlueskyCredentialsWithHttpInfo(connectBlueskyCredentialsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ConnectBlueskyCredentialsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectBlueskyCredentialsRequest** | [**ConnectBlueskyCredentialsRequest**](ConnectBlueskyCredentialsRequest.md) |  |  |

### Return type

[**ConnectBlueskyCredentials200Response**](ConnectBlueskyCredentials200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Bluesky connected successfully |  -  |
| **400** | Invalid request - missing fields or invalid state format |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The connect token was issued for a different profile or platform (INSUFFICIENT_PERMISSIONS). |  -  |
| **500** | Internal error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="connectdiscordchannel"></a>
# **ConnectDiscordChannel**
> void ConnectDiscordChannel (ConnectDiscordChannelRequest connectDiscordChannelRequest)

Connect a Discord channel

Finalize a Discord connect by binding channels to a profile. Served by a dedicated route, so it is not reachable through POST /v1/connect/{platform}. One connected account per channel: send channelIds to connect several channels of the server at once, or repeat the call with a different channelId.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ConnectDiscordChannelExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var connectDiscordChannelRequest = new ConnectDiscordChannelRequest(); // ConnectDiscordChannelRequest | 

            try
            {
                // Connect a Discord channel
                apiInstance.ConnectDiscordChannel(connectDiscordChannelRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ConnectDiscordChannel: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConnectDiscordChannelWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Connect a Discord channel
    apiInstance.ConnectDiscordChannelWithHttpInfo(connectDiscordChannelRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ConnectDiscordChannelWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectDiscordChannelRequest** | [**ConnectDiscordChannelRequest**](ConnectDiscordChannelRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Channel connected |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **404** | Profile not found |  -  |
| **422** | channelIds only. None of the channels could be connected; &#x60;details.failed&#x60; lists each one with its reason. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="connectopenaiadscredentials"></a>
# **ConnectOpenAIAdsCredentials**
> ConnectOpenAIAdsCredentials200Response ConnectOpenAIAdsCredentials (ConnectOpenAIAdsCredentialsRequest connectOpenAIAdsCredentialsRequest)

Connect an OpenAI Ads account

Connect an OpenAI Ads account using an API key from ChatGPT Ads Manager.  The key grants full campaign write access on OpenAI's side (OpenAI does not offer a read-only key scope).  Zernio uses it to:  - read ads and performance - create and manage campaigns you set up through Zernio (create, status, budget, and cancel)  Campaigns created directly in ChatGPT Ads Manager can still be managed there. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ConnectOpenAIAdsCredentialsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var connectOpenAIAdsCredentialsRequest = new ConnectOpenAIAdsCredentialsRequest(); // ConnectOpenAIAdsCredentialsRequest | 

            try
            {
                // Connect an OpenAI Ads account
                ConnectOpenAIAdsCredentials200Response result = apiInstance.ConnectOpenAIAdsCredentials(connectOpenAIAdsCredentialsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ConnectOpenAIAdsCredentials: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConnectOpenAIAdsCredentialsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Connect an OpenAI Ads account
    ApiResponse<ConnectOpenAIAdsCredentials200Response> response = apiInstance.ConnectOpenAIAdsCredentialsWithHttpInfo(connectOpenAIAdsCredentialsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ConnectOpenAIAdsCredentialsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectOpenAIAdsCredentialsRequest** | [**ConnectOpenAIAdsCredentialsRequest**](ConnectOpenAIAdsCredentialsRequest.md) |  |  |

### Return type

[**ConnectOpenAIAdsCredentials200Response**](ConnectOpenAIAdsCredentials200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OpenAI Ads connected successfully |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized, or the API key could not read an OpenAI ad account (code invalid_credentials). |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | Ads add-on required. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="connectshopifywithtoken"></a>
# **ConnectShopifyWithToken**
> ConnectShopifyWithToken200Response ConnectShopifyWithToken (ConnectShopifyWithTokenRequest connectShopifyWithTokenRequest)

Connect a Shopify store with a custom-app Admin token

Token-paste alternative to the OAuth flow: connect a store using the Admin API access token of a custom app the merchant created in their own Shopify admin.  The custom app is created under Settings → Apps and sales channels → Develop apps, with the `read_content`, `write_content`, `read_products` and `write_products` scopes.  Use this when the one-click OAuth connect is unavailable or when your users prefer not to install a third-party app on their store.  - The token is validated against the store before anything is saved. - Custom-app tokens do not expire. - Connecting the same profile to a store again replaces the stored token in place. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ConnectShopifyWithTokenExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var connectShopifyWithTokenRequest = new ConnectShopifyWithTokenRequest(); // ConnectShopifyWithTokenRequest | 

            try
            {
                // Connect a Shopify store with a custom-app Admin token
                ConnectShopifyWithToken200Response result = apiInstance.ConnectShopifyWithToken(connectShopifyWithTokenRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ConnectShopifyWithToken: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConnectShopifyWithTokenWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Connect a Shopify store with a custom-app Admin token
    ApiResponse<ConnectShopifyWithToken200Response> response = apiInstance.ConnectShopifyWithTokenWithHttpInfo(connectShopifyWithTokenRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ConnectShopifyWithTokenWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectShopifyWithTokenRequest** | [**ConnectShopifyWithTokenRequest**](ConnectShopifyWithTokenRequest.md) |  |  |

### Return type

[**ConnectShopifyWithToken200Response**](ConnectShopifyWithToken200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Store connected as a platform account |  -  |
| **400** | Invalid &#x60;profileId&#x60; format, &#x60;shop&#x60; is not a myshopify.com store domain, or Shopify rejected the access token for that store. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | API key does not have access to this profile. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="connectslackchannel"></a>
# **ConnectSlackChannel**
> void ConnectSlackChannel (ConnectSlackChannelRequest connectSlackChannelRequest)

Connect a Slack channel

Finalize a Slack connect by creating the per-channel account. Served by a dedicated route, so it is not reachable through POST /v1/connect/{platform}. Send pendingDataToken for a first connect (the nonce from the OAuth redirect) or accountId to add another channel to a workspace already connected.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ConnectSlackChannelExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var connectSlackChannelRequest = new ConnectSlackChannelRequest(); // ConnectSlackChannelRequest | 

            try
            {
                // Connect a Slack channel
                apiInstance.ConnectSlackChannel(connectSlackChannelRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ConnectSlackChannel: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConnectSlackChannelWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Connect a Slack channel
    apiInstance.ConnectSlackChannelWithHttpInfo(connectSlackChannelRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ConnectSlackChannelWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectSlackChannelRequest** | [**ConnectSlackChannelRequest**](ConnectSlackChannelRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Channel connected |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | Slack connections are temporarily unavailable |  -  |
| **404** | Profile not found |  -  |
| **422** | channelIds only. None of the channels could be connected; &#x60;details.failed&#x60; lists each one with its reason. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="connectwebflowwithsitetoken"></a>
# **ConnectWebflowWithSiteToken**
> ConnectWebflowWithSiteToken200Response ConnectWebflowWithSiteToken (ConnectWebflowWithSiteTokenRequest connectWebflowWithSiteTokenRequest)

Connect Webflow with a site API token

Connects one Webflow site using a site API token. Zernio checks the token's scopes, reads its site, and stores the token encrypted.  Create the token in the site's Site settings > Apps & integrations > API access, with Sites read-only and CMS read and write access.  ### What it supports  Webflow is a connect-only blog platform: each CMS collection with a rich text field is a blog in the Blogs API (`/v1/accounts/{accountId}/blogs`). It does not support social posts, inbox, analytics or ads.  - Publishing an article needs a site that has been published once. - Reconnecting the same site and profile updates the connection in place. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ConnectWebflowWithSiteTokenExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var connectWebflowWithSiteTokenRequest = new ConnectWebflowWithSiteTokenRequest(); // ConnectWebflowWithSiteTokenRequest | 

            try
            {
                // Connect Webflow with a site API token
                ConnectWebflowWithSiteToken200Response result = apiInstance.ConnectWebflowWithSiteToken(connectWebflowWithSiteTokenRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ConnectWebflowWithSiteToken: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConnectWebflowWithSiteTokenWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Connect Webflow with a site API token
    ApiResponse<ConnectWebflowWithSiteToken200Response> response = apiInstance.ConnectWebflowWithSiteTokenWithHttpInfo(connectWebflowWithSiteTokenRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ConnectWebflowWithSiteTokenWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectWebflowWithSiteTokenRequest** | [**ConnectWebflowWithSiteTokenRequest**](ConnectWebflowWithSiteTokenRequest.md) |  |  |

### Return type

[**ConnectWebflowWithSiteToken200Response**](ConnectWebflowWithSiteToken200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webflow site connected as a platform account |  -  |
| **400** | Malformed body, or a token Webflow rejects, that is not scoped to one site, or that lacks Sites read or CMS write access. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | API key does not have access to this profile. |  -  |
| **404** | Profile not found or access denied. |  -  |
| **502** | Webflow returned an unclassified upstream error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="connectwhatsappcredentials"></a>
# **ConnectWhatsAppCredentials**
> ConnectWhatsAppCredentials200Response ConnectWhatsAppCredentials (ConnectWhatsAppCredentialsRequest connectWhatsAppCredentialsRequest)

Connect WhatsApp via credentials

Connect a WhatsApp Business Account by providing Meta credentials directly. This is the headless alternative to the Embedded Signup browser flow.  ### Getting the credentials  1. Go to Meta Business Suite (business.facebook.com) 2. Create or select a WhatsApp Business Account 3. In Business Settings > System Users, create a System User 4. Assign it the whatsapp_business_management and whatsapp_business_messaging permissions 5. Generate a permanent access token 6. Get the WABA ID from WhatsApp Manager > Account Tools > Phone Numbers 7. Get the Phone Number ID from the same page (click on the number)  ### Warning: webhook delivery moves to Zernio  Connecting subscribes your own Meta app to this WABA with an override callback that redirects its webhook delivery to Zernio.  This WABA's events stop reaching any callback URL you had configured before, immediately and with no overlap window.  Do not unsubscribe your app from the WABA afterward: that also cuts off Zernio's delivery, and recovery requires calling this endpoint again. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ConnectWhatsAppCredentialsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var connectWhatsAppCredentialsRequest = new ConnectWhatsAppCredentialsRequest(); // ConnectWhatsAppCredentialsRequest | 

            try
            {
                // Connect WhatsApp via credentials
                ConnectWhatsAppCredentials200Response result = apiInstance.ConnectWhatsAppCredentials(connectWhatsAppCredentialsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ConnectWhatsAppCredentials: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConnectWhatsAppCredentialsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Connect WhatsApp via credentials
    ApiResponse<ConnectWhatsAppCredentials200Response> response = apiInstance.ConnectWhatsAppCredentialsWithHttpInfo(connectWhatsAppCredentialsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ConnectWhatsAppCredentialsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectWhatsAppCredentialsRequest** | [**ConnectWhatsAppCredentialsRequest**](ConnectWhatsAppCredentialsRequest.md) |  |  |

### Return type

[**ConnectWhatsAppCredentials200Response**](ConnectWhatsAppCredentials200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | WhatsApp connected successfully |  -  |
| **400** | Invalid request. Missing fields, a &#x60;pin&#x60; that is not 6 digits, or the phoneNumberId was not found in the specified WABA. If the phone was not found, the response includes availablePhoneNumbers to help identify the correct ID.  |  -  |
| **401** | Invalid or expired access token |  -  |
| **403** | Profile limit exceeded for this plan |  -  |
| **409** | Conflict with an existing connection. A number can only be live on one profile. Cases:  - WHATSAPP_NUMBER_PINNED_TO_PROFILE: a Zernio-provisioned number pinned to a different profile. Connect it from that profile, or move it first with PATCH /v1/whatsapp/phone-numbers/{id}/profile. - WHATSAPP_NUMBER_ALREADY_CONNECTED: already actively connected on another profile or team. Disconnect it there first. - WHATSAPP_COEXISTENCE_NOT_REGISTERED: a number connected from the WhatsApp Business app (coexistence) that the phone never registered on the Cloud API, so Meta reported platform_type ON_PREMISE and refused the contacts/history sync with error 133010.  In the coexistence case no account is created. The customer opens WhatsApp Business on the phone, keeps it open and updated, and runs the same Embedded Signup again, which succeeds on the second attempt in practice.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="connectwhatsappembeddedsignup"></a>
# **ConnectWhatsAppEmbeddedSignup**
> ConnectWhatsAppEmbeddedSignup200Response ConnectWhatsAppEmbeddedSignup (ConnectWhatsAppEmbeddedSignupRequest connectWhatsAppEmbeddedSignupRequest, string? xConnectToken = null)

Connect WhatsApp from Embedded Signup

Exchange the authorization code Meta's Embedded Signup popup returned.  This is the call the Zernio-hosted signup page makes after the popup closes (`GET /v1/connect/whatsapp?signup=hosted`). It sends the `wabaId` and `phoneNumberId` Meta reported, so exactly the chosen number is connected. When both are omitted, the first number the token can see is used.  The code never passes through a `redirect_uri`, so `POST /v1/connect/{platform}` cannot accept it.  Authenticates with an API key, or with the connect token the hosted flow issues (`X-Connect-Token` header). 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ConnectWhatsAppEmbeddedSignupExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var connectWhatsAppEmbeddedSignupRequest = new ConnectWhatsAppEmbeddedSignupRequest(); // ConnectWhatsAppEmbeddedSignupRequest | 
            var xConnectToken = "xConnectToken_example";  // string? | Connect token issued by the hosted signup flow, accepted instead of an API key. (optional) 

            try
            {
                // Connect WhatsApp from Embedded Signup
                ConnectWhatsAppEmbeddedSignup200Response result = apiInstance.ConnectWhatsAppEmbeddedSignup(connectWhatsAppEmbeddedSignupRequest, xConnectToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ConnectWhatsAppEmbeddedSignup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConnectWhatsAppEmbeddedSignupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Connect WhatsApp from Embedded Signup
    ApiResponse<ConnectWhatsAppEmbeddedSignup200Response> response = apiInstance.ConnectWhatsAppEmbeddedSignupWithHttpInfo(connectWhatsAppEmbeddedSignupRequest, xConnectToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ConnectWhatsAppEmbeddedSignupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectWhatsAppEmbeddedSignupRequest** | [**ConnectWhatsAppEmbeddedSignupRequest**](ConnectWhatsAppEmbeddedSignupRequest.md) |  |  |
| **xConnectToken** | **string?** | Connect token issued by the hosted signup flow, accepted instead of an API key. | [optional]  |

### Return type

[**ConnectWhatsAppEmbeddedSignup200Response**](ConnectWhatsAppEmbeddedSignup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Number connected |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **409** | The number is already connected on another profile or team |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="connectwhopadscredentials"></a>
# **ConnectWhopAdsCredentials**
> ConnectWhopAdsCredentials200Response ConnectWhopAdsCredentials (ConnectWhopAdsCredentialsRequest connectWhopAdsCredentialsRequest)

Connect a Whop account

Connect a Whop account with an Account API key from the Whop dashboard (Developer > API keys). The key only has to be able to read its own account: Zernio calls `GET /accounts/me` once to learn the account id (`biz_...`) and name, then stores the key.  What the connection unlocks today is the Whop Pixel through the tracking-tags API: the account id is the pixel, so `GET /v1/accounts/{accountId}/tracking-tags` lists it and `POST .../tracking-tags/{biz_...}/install` puts it on a Shopify store or WordPress site. Whop campaigns are not managed through Zernio. One Whop account per profile. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ConnectWhopAdsCredentialsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var connectWhopAdsCredentialsRequest = new ConnectWhopAdsCredentialsRequest(); // ConnectWhopAdsCredentialsRequest | 

            try
            {
                // Connect a Whop account
                ConnectWhopAdsCredentials200Response result = apiInstance.ConnectWhopAdsCredentials(connectWhopAdsCredentialsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ConnectWhopAdsCredentials: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConnectWhopAdsCredentialsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Connect a Whop account
    ApiResponse<ConnectWhopAdsCredentials200Response> response = apiInstance.ConnectWhopAdsCredentialsWithHttpInfo(connectWhopAdsCredentialsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ConnectWhopAdsCredentialsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectWhopAdsCredentialsRequest** | [**ConnectWhopAdsCredentialsRequest**](ConnectWhopAdsCredentialsRequest.md) |  |  |

### Return type

[**ConnectWhopAdsCredentials200Response**](ConnectWhopAdsCredentials200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Whop account connected |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized, or the API key could not read its Whop account (code invalid_credentials). |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | Ads add-on required. |  -  |
| **409** | The profile already has a different Whop account connected (code PROFILE_PLATFORM_CONFLICT). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="connectwordpresswithapplicationpassword"></a>
# **ConnectWordPressWithApplicationPassword**
> ConnectWordPressWithApplicationPassword200Response ConnectWordPressWithApplicationPassword (ConnectWordPressWithApplicationPasswordRequest connectWordPressWithApplicationPasswordRequest)

Connect self-hosted WordPress with an application password

Connects one self-hosted WordPress site using a WordPress username and application password.  - `siteUrl` must use HTTPS and may include the path where WordPress is installed. - Create an application password in the WordPress user's profile; do not send the user's login password.  Zernio discovers the REST API, verifies the credentials and required post/media/taxonomy capabilities, then stores the password encrypted.  Reconnecting the same site and profile updates the connection in place. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ConnectWordPressWithApplicationPasswordExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var connectWordPressWithApplicationPasswordRequest = new ConnectWordPressWithApplicationPasswordRequest(); // ConnectWordPressWithApplicationPasswordRequest | 

            try
            {
                // Connect self-hosted WordPress with an application password
                ConnectWordPressWithApplicationPassword200Response result = apiInstance.ConnectWordPressWithApplicationPassword(connectWordPressWithApplicationPasswordRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ConnectWordPressWithApplicationPassword: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConnectWordPressWithApplicationPasswordWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Connect self-hosted WordPress with an application password
    ApiResponse<ConnectWordPressWithApplicationPassword200Response> response = apiInstance.ConnectWordPressWithApplicationPasswordWithHttpInfo(connectWordPressWithApplicationPasswordRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ConnectWordPressWithApplicationPasswordWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectWordPressWithApplicationPasswordRequest** | [**ConnectWordPressWithApplicationPasswordRequest**](ConnectWordPressWithApplicationPasswordRequest.md) |  |  |

### Return type

[**ConnectWordPressWithApplicationPassword200Response**](ConnectWordPressWithApplicationPassword200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | WordPress site connected as a platform account |  -  |
| **400** | Malformed body, non-HTTPS &#x60;siteUrl&#x60;, invalid username, unavailable REST API, or a site that cannot support the required WordPress operations. |  -  |
| **401** | Invalid API key or WordPress application password. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | No access to the Zernio profile, or the WordPress user lacks required capabilities. |  -  |
| **404** | Zernio profile not found or WordPress REST endpoint not found. |  -  |
| **502** | The WordPress site returned an unclassified upstream error. |  -  |
| **503** | The WordPress site could not be reached. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createoauthapp"></a>
# **CreateOAuthApp**
> CreateOAuthApp201Response CreateOAuthApp (CreateOAuthAppRequest createOAuthAppRequest)

Add an OAuth app

Saves your app's client ID and secret for a platform.  The keys are checked with the platform first:  - Keys it rejects return 400 OAUTH_APP_KEYS_REJECTED and are not saved. - Keys it could not check are saved with status `unchecked`.  Allow the returned `redirectUri` in your app's settings on the platform before connecting.  Only the account owner or a full-access team member can add apps, and not with a profile-scoped API key. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class CreateOAuthAppExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var createOAuthAppRequest = new CreateOAuthAppRequest(); // CreateOAuthAppRequest | 

            try
            {
                // Add an OAuth app
                CreateOAuthApp201Response result = apiInstance.CreateOAuthApp(createOAuthAppRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.CreateOAuthApp: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateOAuthAppWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add an OAuth app
    ApiResponse<CreateOAuthApp201Response> response = apiInstance.CreateOAuthAppWithHttpInfo(createOAuthAppRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.CreateOAuthAppWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createOAuthAppRequest** | [**CreateOAuthAppRequest**](CreateOAuthAppRequest.md) |  |  |

### Return type

[**CreateOAuthApp201Response**](CreateOAuthApp201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The app was saved. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The caller cannot change workspace settings (INSUFFICIENT_PERMISSIONS). |  -  |
| **409** | The workspace already has an app with this client ID on this platform (OAUTH_APP_ALREADY_EXISTS); &#x60;details.appId&#x60; names it. Rotate its secret with PATCH instead. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createpinterestboard"></a>
# **CreatePinterestBoard**
> CreatePinterestBoard201Response CreatePinterestBoard (string accountId, CreatePinterestBoardRequest createPinterestBoardRequest)

Create Pinterest board

Creates a new board on the connected Pinterest account. The returned board ID can be used immediately as `platformSpecificData.boardId` when creating a Pinterest post.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class CreatePinterestBoardExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var createPinterestBoardRequest = new CreatePinterestBoardRequest(); // CreatePinterestBoardRequest | 

            try
            {
                // Create Pinterest board
                CreatePinterestBoard201Response result = apiInstance.CreatePinterestBoard(accountId, createPinterestBoardRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.CreatePinterestBoard: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreatePinterestBoardWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Pinterest board
    ApiResponse<CreatePinterestBoard201Response> response = apiInstance.CreatePinterestBoardWithHttpInfo(accountId, createPinterestBoardRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.CreatePinterestBoardWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **createPinterestBoardRequest** | [**CreatePinterestBoardRequest**](CreatePinterestBoardRequest.md) |  |  |

### Return type

[**CreatePinterestBoard201Response**](CreatePinterestBoard201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Board created |  -  |
| **400** | Invalid request or not a Pinterest account |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found |  -  |
| **502** | Pinterest rejected the request (e.g. duplicate board name) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createyoutubeplaylist"></a>
# **CreateYoutubePlaylist**
> CreateYoutubePlaylist201Response CreateYoutubePlaylist (string accountId, CreateYoutubePlaylistRequest createYoutubePlaylistRequest)

Create YouTube playlist

Creates an empty playlist on the connected YouTube channel. Requires a title; privacy defaults to private.  Returns the same playlist shape as the list endpoint. Pass the returned playlist.id as platformSpecificData.playlistId when publishing a video. Does not change the account's default playlist.  ### Requirements and cost  - Requires the youtube or youtube.force-ssl OAuth scope. - Costs 50 YouTube quota units.  ### Retries  This operation is not idempotent and is not automatically retried. Repeating a request can create another playlist, including after a timeout. List playlists before retrying an ambiguous failure.  ### Official series  Official series settings are not exposed by YouTube's public API and must be enabled manually in YouTube's desktop playlist settings. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class CreateYoutubePlaylistExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var createYoutubePlaylistRequest = new CreateYoutubePlaylistRequest(); // CreateYoutubePlaylistRequest | 

            try
            {
                // Create YouTube playlist
                CreateYoutubePlaylist201Response result = apiInstance.CreateYoutubePlaylist(accountId, createYoutubePlaylistRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.CreateYoutubePlaylist: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateYoutubePlaylistWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create YouTube playlist
    ApiResponse<CreateYoutubePlaylist201Response> response = apiInstance.CreateYoutubePlaylistWithHttpInfo(accountId, createYoutubePlaylistRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.CreateYoutubePlaylistWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **createYoutubePlaylistRequest** | [**CreateYoutubePlaylistRequest**](CreateYoutubePlaylistRequest.md) |  |  |

### Return type

[**CreateYoutubePlaylist201Response**](CreateYoutubePlaylist201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Playlist created |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | API key lacks access to the account or YouTube denied permission. |  -  |
| **404** | Account not found or inaccessible. |  -  |
| **429** | YouTube rate limit exceeded. |  -  |
| **502** | YouTube request failed. Check existing playlists before retrying, because the playlist may have been created. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteoauthapp"></a>
# **DeleteOAuthApp**
> DeleteOAuthApp200Response DeleteOAuthApp (string appId, bool? confirm = null)

Remove an OAuth app

Removes the app. Accounts connected through it can no longer refresh their tokens, so when any are connected the call returns 409 OAUTH_APP_IN_USE with `details.accountCount` unless `confirm=true` is passed. With confirm, those accounts are marked as needing reconnection and each fires `account.disconnected`.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class DeleteOAuthAppExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var appId = "appId_example";  // string | 
            var confirm = false;  // bool? |  (optional)  (default to false)

            try
            {
                // Remove an OAuth app
                DeleteOAuthApp200Response result = apiInstance.DeleteOAuthApp(appId, confirm);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.DeleteOAuthApp: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteOAuthAppWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove an OAuth app
    ApiResponse<DeleteOAuthApp200Response> response = apiInstance.DeleteOAuthAppWithHttpInfo(appId, confirm);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.DeleteOAuthAppWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appId** | **string** |  |  |
| **confirm** | **bool?** |  | [optional] [default to false] |

### Return type

[**DeleteOAuthApp200Response**](DeleteOAuthApp200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The app was removed. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The caller cannot change workspace settings (INSUFFICIENT_PERMISSIONS). |  -  |
| **404** | Resource not found |  -  |
| **409** | Accounts are still connected through the app (OAUTH_APP_IN_USE); resend with confirm&#x3D;true. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getconnecthandoff"></a>
# **GetConnectHandoff**
> ConnectHandoff GetConnectHandoff (Guid handoffId)

Get a phone handoff

Shows where a connect started with `handoff=true` on `GET /v1/connect/{platform}` stands.  ### States  - `waiting`: until the QR code is scanned - `opened`: the phone opened it - `connected`: with the new accounts - `failed`: with the error the flow ended on (the same `error` codes as the redirect flow) - `expired`: nobody opened the QR code within its 30 minutes  ### Polling  Poll it every 2 to 5 seconds while your QR code is shown, and stop once it is `connected`, `failed` or `expired`.  It is readable for 60 minutes after it was created, then 404. A handoff created by another workspace is also 404. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetConnectHandoffExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var handoffId = "handoffId_example";  // Guid | `handoff.id` from the connect response.

            try
            {
                // Get a phone handoff
                ConnectHandoff result = apiInstance.GetConnectHandoff(handoffId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetConnectHandoff: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetConnectHandoffWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a phone handoff
    ApiResponse<ConnectHandoff> response = apiInstance.GetConnectHandoffWithHttpInfo(handoffId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetConnectHandoffWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **handoffId** | **Guid** | &#x60;handoff.id&#x60; from the connect response. |  |

### Return type

[**ConnectHandoff**](ConnectHandoff.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The handoff. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The handoff expired, does not exist, or belongs to another workspace (code RESOURCE_NOT_FOUND). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getconnecturl"></a>
# **GetConnectUrl**
> GetConnectUrl200Response GetConnectUrl (string platform, string profileId, string? reconnectAccountId = null, string? oauthAppId = null, string? expectedPlatformUserId = null, string? expectedUsername = null, bool? forceReauth = null, string? redirectUrl = null, string? scopes = null, string? loginHint = null, bool? headless = null, string? loginMethod = null, string? onboarding = null, string? signup = null, string? brandName = null, string? primaryColor = null, bool? welcome = null, string? welcomeTheme = null, string? logoUrl = null, string? language = null, bool? handoff = null)

Get OAuth connect URL

Initiate an OAuth connection flow. Returns an authUrl to redirect the user to.  ### Modes  - Standard flow: Zernio hosts the selection UI, then redirects to your redirect_url. - Headless mode (headless=true): user is redirected to your redirect_url with OAuth data for custom UI. Use the platform-specific selection endpoints to complete.  ### Several accounts per platform  A profile can hold several accounts of the same platform. Connecting a different account adds it as a new account, and reconnecting the SAME account keeps it and all of its history.  Ads connections stay one per profile.  On a legacy plan limited to N profiles, a new account is refused with 403 `platform_account_limit` once N accounts of its platform are connected.  ### TikTok  Every connection now goes through the TikTok for Business app.  An authorization that leaves out a permission the connected account needs changes nothing at all and comes back as `missing_tiktok_permissions`. Connect again and accept every permission on TikTok's screen. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetConnectUrlExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var platform = "facebook";  // string | Social media platform to connect. `snapchat` is a closed beta with no public release date: it returns 403 `PLATFORM_BETA_RESTRICTED` until the account is approved.
            var profileId = "profileId_example";  // string | Your Zernio profile ID (get from /v1/profiles). For WhatsApp, a Zernio-provisioned number can only be connected on the profile it was provisioned to; connecting from any other profile is rejected with a 409.
            var reconnectAccountId = "reconnectAccountId_example";  // string? | Refresh this existing account: a Zernio account id of the same platform on this profile (otherwise 400).  The OAuth callback and the selection endpoints (select-page, select-organization, select-board, select-location, Instagram and Snapchat selection) refuse with `reconnect_account_mismatch` a login that would write to a different account of the platform on this profile instead of this one.  In headless mode the marker travels in the redirect_url we hand you, so pass that URL back unchanged to the selection endpoint. On X it counts toward the OAuth state limit described under redirect_url.  (optional) 
            var oauthAppId = "oauthAppId_example";  // string? | Connect through one of your own OAuth apps (see /v1/connect/oauth-apps), so the consent screen shows your app and the platform's limits are your app's. Without it the connect runs on Zernio's app, whatever apps the workspace has saved.  - Only platforms listed in `platforms` of GET /v1/connect/oauth-apps accept an app. Any other returns 400, and so do ads connects (`adsConnect=true` in the redirect URL). - Connects that end on a destination picker also return 400, except Facebook Pages, Google Business locations, Pinterest boards and Snapchat public profiles (Instagram through Facebook Login, for example). - A LinkedIn connect through an app saves the member's own profile: organization pages, and mention lookups, stay on Zernio's app. - The connect requests the app's `scopeAreas`. `scopes` may narrow them but not add an area the app does not enable (400). - If the user does not grant every requested area, the account still connects and the redirect carries `missing_permissions=<areas>` (the headless POST returns `missingPermissions`). - If the platform refuses a permission your app is not approved for, the redirect carries `error=oauth_app_scope_not_allowed`.  The account remembers the app, and token refresh, publishing and inbox run on it. Reconnecting through another app, or without one, moves the account to that app.  (optional) 
            var expectedPlatformUserId = "expectedPlatformUserId_example";  // string? | Only connect if the login lands on this platform account. Any other account ends the flow with `error=account_mismatch` (a 409 `account_mismatch` on POST /v1/connect/instagram/select-account) and nothing is written.  Compared with every id the platform reports for the authorized account:  - Any platform: the `platformUserId` of a Zernio account on this platform. - Instagram: either the app-scoped id or the professional account id (`metadata.instagramScopedId`, the `17841...` id that Facebook Login accounts hold as platformUserId). - TikTok: open_ids are app-scoped, so an id from your own TikTok app never matches. Use expectedUsername there.  Honoured by the OAuth callback (every platform that connects without a selection step, Instagram Login included) and by the Instagram selection step. On the other selection endpoints you choose the destination yourself.  In headless mode the marker travels in the redirect_url we hand you, so pass that URL back unchanged. On X it counts toward the OAuth state limit described under redirect_url.  (optional) 
            var expectedUsername = "expectedUsername_example";  // string? | Only connect if the authorized account's handle is this one (case-insensitive, a leading @ is ignored). Otherwise the flow ends with `error=account_mismatch` and `error_message` naming the handle that was authorized, and nothing is written.  Same coverage and transport as expectedPlatformUserId; when both are sent, both must match. Use this on a first connection, where you hold the handle the user typed but no Zernio id yet.  (optional) 
            var forceReauth = false;  // bool? | Instagram Login only (the default loginMethod); ignored elsewhere. Makes Instagram show its login page and ask for the credentials of the account to connect, even when another Instagram account is logged in on the device or app. Also hides the Facebook login option on that page.  Use it when the person connecting manages several Instagram accounts on one phone: otherwise Instagram logs in, and converts to a professional account, whichever account is active, before any consent screen. Pair it with expectedUsername to also refuse a wrong account at the end.  (optional)  (default to false)
            var redirectUrl = "redirectUrl_example";  // string? | Your custom redirect URL after the connection completes. It MUST be an absolute http(s) URL or a custom app scheme for mobile deeplinks (e.g. myapp://callback). A relative path is rejected with 400 `INVALID_REDIRECT_URL`.  **Exit notice:** when `redirect_url` is an http(s) URL on another site (anything but zernio.com), every redirect of the flow lands first on `https://zernio.com/connect/continue?to=<your URL>`, a Zernio page that names your site and continues to it with one click. All params below reach your URL unchanged.  A custom app scheme (myapp://...) never goes through the notice. In headless mode the redirects we hand you (and the `redirect_url` returned by the selection endpoints) are notice URLs: pass them back or navigate to them as they are.  **X (twitter) length limit:** X caps the OAuth `state` at 500 characters and the redirect travels inside it (wrapped in the notice URL for an http(s) URL on another site). The URL-encoded form must be at most 258 characters for API callers, 310 for dashboard sessions.  In headless mode the appended `headless=true` counts toward that limit. A plain https URL on another site leaves about 165 to 190 characters of your own URL, depending on encoding. A longer one is rejected with 400 `INVALID_REDIRECT_URL`, and the error says by how much.  **Success params** are appended with the URL API, so an existing query string is preserved:  - Standard mode: connected={platform}&profileId=X&accountId=Y&username=Z. - Headless mode: OAuth data params for platforms requiring selection (e.g. LinkedIn orgs, Facebook pages). If no selection is needed, the account is created directly and the redirect includes accountId.  **Failure params:** the browser goes to the same redirect_url with `error` and `platform` appended (always present). `error_message`, `is_user_fixable`, `reason`, `dashboard_url`, `missing_scopes`, `error_reason` and the `platform_error*` params are conditional: treat them as optional.  Your own query params are kept on every redirect, but ours overwrite one of yours with the same name. On an error redirect we remove the internal `headless`, `adsConnect`, `adsScope`, `reconnectAccountId`, `expectedPlatformUserId` and `expectedUsername` markers added during the flow.  **Correlation** params appear on every redirect from an OAuth callback (success and failure) and on the `redirect_url` returned by the selection endpoints such as POST /v1/connect/facebook/select-page:  - `request_id`: the id we log that request under. Quote it when reporting a problem. - `stage`: where the flow ended. `authorize` = the platform's consent dialog returned an error or denial instead of a code. `callback` = we processed the returned code (success, a selection step, or a failure). - `stage` = `select_page`: the destination-selection endpoint (page, account, organization, board, location, profile or phone number) completed it.  **Error details:**  - `oauth_denied`: carries `error_message` and, when the platform sent them, its own `platform_error` (e.g. `access_denied`), `platform_error_reason` (e.g. `user_denied`) and `platform_error_description` (truncated to 500 characters). `is_user_fixable=true` when the platform reported that the user cancelled or declined. - `no_facebook_pages`: comes with `is_user_fixable=true`, an `error_message` telling the user to click \"Edit previous settings\" in Meta's dialog and tick the Page (or create one), and `error_reason` when Meta's token debug answered (values below). - `code_already_redeemed`: the same authorization code arrived more than once and an earlier request already processed it (the code is never sent to the platform twice). Not a failure: check GET /v1/accounts or wait for the `account.connected` webhook. - `missing_google_permissions` (YouTube, Google Business and Google Ads): the user unchecked permissions on Google's consent screen. Always with `is_user_fixable=true`. When Google reported granted scopes, `missing_scopes` lists the requested scopes not granted (comma-separated). Ask the user to connect again keeping every permission checked. - `no_youtube_channel`: Google authorized the account but it has no YouTube channel we can connect. Always with `is_user_fixable=true` and an `error_message`.  Usual causes of `no_youtube_channel`: the user picked their personal Google identity instead of the Brand Account in Google's account chooser, they only have YouTube Studio access (not Brand Account owner or manager), or the account has no channel yet.  `error_reason` values for `no_facebook_pages`:  - `pages_permission_declined`: the user declined the pages_show_list permission. - `no_pages_granted`: the permission was granted with no Page ticked. Meta reports a user who manages no Page the same way, so this covers both. - `granted_pages_not_listed`: Pages were ticked but Meta listed none the user can manage, and a direct read of each ticked Page returned no access token.  **Headless `userProfile`:** on headless Facebook success (`step=select_page`) and headless Instagram `facebook_login` success (`step=select_account`), `userProfile` is JSON percent-encoded once before being set as a query param, so it is encoded twice on the wire.  After your framework decodes the query string once, run one more decodeURIComponent (or equivalent), then JSON.parse it. `tempToken` and `connect_token` are plain values.  **Error values.** This list is NOT exhaustive and new values may be added at any time: treat an unrecognized value as a generic failure rather than matching exhaustively. Existing values are not renamed or removed without notice.  - OAuth and callback: `oauth_denied`, `invalid_callback`, `invalid_state`, `unsupported_platform`, `connection_failed`, `internal_error`, `token_exchange_failed`, `byok_config_error`, `personal_account_not_supported`, `missing_google_permissions`, `missing_tiktok_permissions`, `platform_requires_destination`, `reconnect_account_mismatch`, `account_mismatch`, `instagram_login_method_mismatch`, `invalid_request`, `code_already_redeemed`. - Access and limits: `profile_not_found`, `invalid_profile_id`, `access_denied`, `account_limit_exceeded`, `profile_limit_exceeded`, `payment_required`. - Destination selection: `no_facebook_pages`, `facebook_pages_error`, `no_google_locations`, `google_locations_error`, `google_permission_denied`, `no_snapchat_public_profiles`, `snapchat_profiles_error`, `no_youtube_channel`, `discord_no_guild`, `slack_no_team`. - WhatsApp: `whatsapp_error`, `one_whatsapp_per_profile`, `whatsapp_number_already_connected`, `whatsapp_number_pinned_to_profile`, `whatsapp_coexistence_not_registered`, `connection_cancelled`. - Google Ads (platform=googleads): `google_ads_auth_failed`, `google_ads_invalid_state`, `google_ads_config_error`, `google_ads_token_failed`, `google_ads_quota_exhausted`, `google_ads_callback_error`. - TikTok Ads (platform=tiktokads): `tiktok_ads_auth_failed`, `tiktok_ads_invalid_state`, `tiktok_ads_access_denied`, `tiktok_ads_config_error`, `tiktok_ads_token_failed`, `tiktok_ads_account_not_found`, `tiktok_ads_callback_error`. - X Ads (platform=xads): `x_ads_denied`, `x_ads_auth_failed`, `x_ads_config_error`, `x_ads_account_not_found`, `x_ads_state_error`, `x_ads_token_failed`, `x_ads_token_missing`, `x_ads_callback_error`. - Reddit Ads (platform=redditads): `reddit_ads_auth_failed`, `reddit_ads_invalid_state`, `reddit_ads_access_denied`, `reddit_ads_scope_not_granted`, `reddit_ads_no_ad_accounts`, `reddit_ads_callback_error`. - Shopify (platform=shopify): `shopify_auth_failed`, `shopify_config_error`, `shopify_invalid_state`, `shopify_invalid_hmac`, `shopify_invalid_shop`, `shopify_missing_scopes`, `shopify_callback_error`.  Notes:  1. On this endpoint every upstream OAuth error collapses into `oauth_denied`, with the provider's values in the `platform_error*` params. The dedicated ads flows differ: they use their own denial slugs, and `google_ads_auth_failed` and `tiktok_ads_auth_failed` may carry the provider's raw error string in `error_message`. 2. On the tiktok and twitter ads flows `platform` carries the ads platform id (`tiktokads`, `xads`), not the value in the request path. The googleads, redditads and shopify flows report `googleads`, `redditads` and `shopify`. 3. `missing_tiktok_permissions`: the TikTok authorization left out a permission the already-connected account needs, so nothing changed and it keeps working as before. User-fixable: connect again and accept every permission on TikTok's screen. 4. `instagram_login_method_mismatch`: an Instagram Login authorization landed on a profile whose Instagram account is connected through Facebook Login, so nothing changed. To refresh it, connect again with `loginMethod=facebook_login`. To move it to Instagram Login, disconnect it first.  (optional) 
            var scopes = posting,analytics;  // string? | Comma-separated permission areas to request instead of the platform's full permission set.  **Values:** `posting`, `analytics`, `comments`, `messaging`, `ads`; on google and microsoft, `email`, `calendar`, `files`, `contacts`.  **Default:** omit it (what the dashboard does) to request everything the platform supports. Google and microsoft REQUIRE it (400 `INVALID_FIELD_VALUE` when absent) because their consent screens are reviewed per area.  When present, the consent dialog asks only for the scopes behind those areas, plus the scopes every connection needs (identity, token refresh, listing the pages, organizations or channels the user picks from).  - Scopes never asked for are absent from the account's `permissions`, and the health endpoints report them as not granted. A `posting`-only account cannot read analytics or the inbox until reconnected with more areas. - First comments need `comments`: a `posting`-only account publishes the post and skips the first comment. - Scopes in none of the areas (X likes, bookmarks and follows, Pinterest ads-only extras) are requested only when the parameter is omitted.  **Supported on** facebook, instagram (both login methods), linkedin, twitter, tiktok, youtube, threads, reddit, pinterest, googlebusiness and slack (via `GET /v1/connect/slack`).  **Rejected** with 400 `INVALID_FIELD_VALUE` (`param: scopes`) on bluesky, telegram, discord, snapchat and whatsapp (their dialog cannot be reduced), and for an empty list or an unknown area.  What each area asks for, per platform (Google scopes shortened to their last path segment):  | Platform | `posting` | `analytics` | `comments` | `messaging` | `ads` | Always requested | |- --|- --|- --|- --|- --|- --|- --| | facebook | `pages_manage_posts` | `read_insights`, `pages_read_user_content` | `pages_manage_engagement`, `pages_read_user_content` | `pages_messaging` | `ads_management`, `ads_read`, `leads_retrieval`, `pages_manage_ads`, `instagram_basic`, `business_management` | `pages_show_list`, `pages_read_engagement`, `pages_manage_metadata` | | instagram (Instagram Login) | `instagram_business_content_publish` | `instagram_business_manage_insights` | `instagram_business_manage_comments` | `instagram_business_manage_messages` | none | `instagram_business_basic` | | instagram (`loginMethod=facebook_login`) | `instagram_content_publish` | `instagram_manage_insights` | `instagram_manage_comments` | `instagram_manage_messages` | `ads_management`, `ads_read`, `leads_retrieval`, `pages_manage_ads` | `instagram_basic`, `pages_show_list`, `pages_read_engagement`, `business_management`, `pages_messaging`, `pages_manage_metadata` | | linkedin | `w_member_social`, `w_organization_social`, `r_organization_social`, `r_organization_followers` | `r_member_postAnalytics`, `r_member_profileAnalytics`, `rw_organization_admin`, `r_organization_social`, `r_organization_followers` | `w_member_social`, `w_member_social_feed`, `w_organization_social`, `w_organization_social_feed`, `r_organization_social`, `r_organization_social_feed` | none | `r_ads`, `rw_ads`, `r_ads_reporting`, `r_marketing_leadgen_automation`, `rw_conversions` | `openid`, `profile`, `email`, `r_basicprofile`, `rw_organization_admin` | | twitter | `tweet.write`, `media.write` | (in the always-requested set) | `tweet.write`, `like.write`, `tweet.moderate.write` | `dm.read`, `dm.write`, `media.write` | none | `tweet.read`, `users.read`, `offline.access` | | tiktok | `video.publish` | `user.info.stats`, `user.insights`, `video.list`, `video.insights` | `comment.list`, `comment.list.manage`, `video.list` | `message.list.read`, `message.list.send`, `message.list.manage` | none | `user.info.basic`, `user.info.username`, `user.info.profile`, `user.account.type`, `video.publish`, `video.upload`, `video.list` | | youtube | `youtube.upload` | `yt-analytics.readonly` | `youtube.force-ssl` | none | none | `youtube` | | threads | `threads_content_publish`, `threads_manage_replies`, `threads_delete` | `threads_manage_insights` | `threads_content_publish`, `threads_read_replies`, `threads_manage_replies`, `threads_delete` | none | none | `threads_basic` | | reddit | `submit`, `read`, `mysubreddits`, `flair`, `history`, `edit` | `read`, `history` | `read`, `history`, `edit`, `vote` | `privatemessages` | none | `identity` | | pinterest | `boards:write`, `pins:read`, `pins:write` | `pins:read`, `user_accounts:read` | none | none | `ads:read`, `ads:write`, `boards:write`, `pins:read`, `pins:write` | `boards:read`, `user_accounts:read` | | googlebusiness | `business.manage` | `business.manage` | `business.manage` | none | none | `business.manage`, `userinfo.profile`, `userinfo.email` | | slack | `chat:write`, `chat:write.public`, `chat:write.customize`, `files:write`, `files:read` | none | none | `chat:write`, `chat:write.customize`, `files:write`, `files:read`, `channels:history`, `groups:history`, `im:history`, `mpim:history`, `im:read`, `im:write`, `mpim:read`, `users:read`, `reactions:read`, `reactions:write` | none | `channels:join`, `channels:read`, `groups:read`, `team:read` |  Google and Microsoft accounts use the mailbox areas instead (`scopes` is required there):  | Platform | `email` | `calendar` | `files` | `contacts` | Always requested | |- --|- --|- --|- --|- --|- --| | google | `gmail.modify` | `calendar` | `drive.file` (only files Zernio created or the user picked, see the Files tag) | `contacts.readonly` | `openid`, `userinfo.email`, `userinfo.profile` | | microsoft | `Mail.ReadWrite`, `Mail.Send` | `Calendars.ReadWrite` | `Files.ReadWrite` | `Contacts.Read` | `openid`, `profile`, `email`, `offline_access`, `User.Read` |  Areas accumulate: reconnecting with more areas widens the grant, and `GET /v1/accounts/{accountId}/health` reports the result.  (optional) 
            var loginHint = "loginHint_example";  // string? | google and microsoft only: pre-fills the account picker with this address so the user lands on the right mailbox. (optional) 
            var headless = false;  // bool? | When true, the user is redirected to your redirect_url with raw OAuth data (code, state) instead of Zernio's default account selection UI. Use this to build a custom connect experience. (optional)  (default to false)
            var loginMethod = "instagram_login";  // string? | Instagram only: which of the two Instagram connection methods to use. Ignored for every other platform.  - `instagram_login` (default when omitted): the Instagram Login dialog. The user authorizes their Instagram professional account directly, no Facebook Page required. Exception: if omitted and `reconnectAccountId` names an account connected with `facebook_login`, the reconnect keeps that method. - `facebook_login`: the Facebook Login dialog (\"Instagram API with Facebook Login\"). The user authorizes a Facebook Page with a linked Instagram professional account, and every API call for that account runs through the Page. Use it when the customer manages Instagram through a Page and expects the Facebook consent screen.  With `facebook_login` the user picks a Page, so the callback continues at the account-selection step, `/v1/connect/instagram/select-account`. The default `instagram_login` has no selection step and connects directly.  `facebook_login` supports `headless=true` like the other selection platforms. The callback redirects to your `redirect_url` with `profileId`, `tempToken`, `platform=instagram`, `step=select_account`, `userProfile` and `connect_token`.  `userProfile` is the Facebook user's profile, same shape and encoding as the Facebook `step=select_page` redirect. Pass `profileId`, `tempToken` and `connect_token` into the select-account endpoints to finish.  (optional)  (default to instagram_login)
            var onboarding = "api";  // string? | WhatsApp only. Ignored for every other platform. Controls which screen Meta's Embedded Signup popup shows.  If omitted, the connection defaults to coexistence (same as `business_app` below), preserving existing behavior for numbers already on the WhatsApp Business app.  `api`: standard Embedded Signup, showing Meta's WABA/number picker. Use this to connect a phone number already on Cloud API elsewhere.  `business_app`: coexistence, i.e. 'Connect existing WhatsApp Business app' (a number shared between Cloud API and the consumer WhatsApp Business app).  (optional) 
            var signup = "hosted";  // string? | WhatsApp only. Rejected with 400 `INVALID_FIELD_VALUE` on any other platform.  `hosted`: `authUrl` points at a Zernio-hosted page on zernio.com instead of Meta's OAuth dialog, and the response carries `authUrl` only (no `state`). That page opens Meta's Embedded Signup popup itself, so it connects exactly the WhatsApp Business Account and number the user picked in the popup.  **When to use it**: your users' Facebook logins manage several WhatsApp accounts. On the default redirect flow Meta only returns an authorization code, so when that login can see more than one number the user lands on Zernio's number picker and has to choose again.  **Flow**: nothing to embed and no domain setup. Send the user to `authUrl`; they come back to `redirect_url` with the same params as the redirect flow.  - Success: `connected=whatsapp`, `profileId`, `accountId`, `username` (plus `connect_token` for API-key callers). - Failure: `error` and `platform=whatsapp`, with the same values and extras as the redirect flow (see below), plus two of its own.  Redirect-flow failures: `one_whatsapp_per_profile`, `whatsapp_number_already_connected`, `whatsapp_number_pinned_to_profile` and `whatsapp_coexistence_not_registered` with `is_user_fixable=true`; `payment_required` with `reason` and `dashboard_url`; `whatsapp_error` with `error_message` when Meta reported one.  Hosted-only failures:  - `connection_cancelled`: the popup was closed before finishing (`error_message` carries Meta's last reported step or error when there is one). - `session_expired`: the user took longer than the 60 minute window the hosted page is valid for. Restart the flow with a new call.  **Same as the redirect flow**: `onboarding` is carried through, and a pre-verified Zernio-provisioned number is attached.  When a previously disconnected account for this profile can simply be re-enabled, this endpoint re-enables it and returns the account directly instead of a URL. `headless` has no effect, because there is no selection step left to hand you.  **The page** shows the same guidance as the Zernio dashboard: a pre-verified Zernio-provisioned number is called out by name (\"choose it in Meta's list, no code will be asked\").  Coexistence and standard signups get their explainer video, and a step-by-step checklist stays visible while Meta's popup is open. Skin it with `brandName`, `primaryColor` and `language` below.  (optional) 
            var brandName = "brandName_example";  // string? | Your product name, for the two branded pages. Trimmed; 1 to 60 characters.  - With `signup=hosted` (WhatsApp): replaces Zernio in the page title (\"Connect your WhatsApp number to <brandName>\"). - With `welcome=true`: fills the heading (\"<brandName> wants to connect to your <platform>\"). Without it the screen shows Zernio and the Zernio mark.  Both pages keep a Zernio mark: they are co-branded, not white-label. Rejected with 400 `INVALID_FIELD_VALUE` without `signup=hosted` or `welcome=true`. Sealed into the page link at issue time, so editing the URL cannot change it.  (optional) 
            var primaryColor = "primaryColor_example";  // string? | Hex colour (`#RRGGBB`) for the primary button on the hosted WhatsApp signup page (`signup=hosted`) or the welcome screen (`welcome=true`). Validated server-side; anything else is a 400 `INVALID_FIELD_VALUE`. Rejected without one of the two. (optional) 
            var welcome = true;  // bool? | Any platform. When `true`, `authUrl` points to a Zernio-hosted welcome screen showing your brand next to the platform (\"<brandName> wants to connect to your <platform>\"). Its button reads Connecting for about a second, then sends the user to the platform's authorization screen with no click.  The rest of the flow is unchanged.  - `brandName`, `logoUrl`, `primaryColor` and `welcomeTheme` are optional and default to Zernio's own name, mark and look. - The link is valid for 30 minutes; after that the page asks the user to start again. - The brand also carries to the account and channel pickers Zernio shows after authorization. - With no `redirect_url`, the flow ends on a branded Zernio-hosted page saying whether the account connected, instead of the Zernio dashboard. - Cannot be combined with `headless=true` or `signup=hosted` (400 `INVALID_FIELD_VALUE`). - The platform's authorization screen still names the Zernio app.  Recommended. When left out, the screen is shown if the workspace saved it as on by default (`PUT /v1/connect/welcome-screen`), except with `headless=true` or `signup=hosted`. Pass `false` to skip it.  Branding you leave out of the call comes from those saved settings, and a `welcomeTheme` you send is merged key by key over the saved theme.  (optional) 
            var welcomeTheme = "welcomeTheme_example";  // string? | Welcome screen only (`welcome=true`). A URL-encoded JSON object that restyles and rewords the screen. All keys are optional.  - **Copy**: `heading` (up to 120 characters); `trustLine`, `consentLine` and `statusLine` (up to 200 each, `statusLine` being the line above the button); `buttonLabel` (up to 30, the label of the link the button becomes if the redirect stalls). - **Closing page** (shown when there is no `redirect_url`): `successHeading` and `errorHeading` (up to 120), `successBody` and `errorBody` (up to 200). All copy may contain the placeholders `{brand}` and `{platform}`. - **Colors**: `primaryColor` (the button), `accentColor` (the header gradient, built as a scale of that colour, and the icons), `pageColor`, `cardColor` and `textColor`, all as `#RRGGBB`. - **Style**: `cornerRadius` as an integer from 0 to 24 (pixels); `font` as `sans`, `serif` or `mono`; `bannerStyle` as `halftone` (default), `solid` (a flat tint of `accentColor`) or `plain` (no banner fill). - **Icons**: `trustLineIcon` (default `shield`) and `consentLineIcon` (default `link`), each one of `shield`, `lock`, `link`, `check`, `user`, `sparkles` or `none`. - **Visibility**: `hide`, an array of any of `heading`, `trustLine`, `consentLine`, `statusLine`, `successBody` and `errorBody`, removes those lines from the screens. - **Links**: `termsUrl` and `privacyUrl` (https, up to 2048 characters) add small Terms and Privacy links at the bottom of every hosted screen.  A `primaryColor` here wins over the `primaryColor` parameter. Unknown keys, invalid JSON or an invalid value are a 400 `INVALID_FIELD_VALUE`. Rejected when the welcome screen is not shown.  Example: `{\"heading\":\"Link your {platform} to {brand}\",\"cardColor\":\"#FFF7ED\",\"cornerRadius\":12}`.  (optional) 
            var logoUrl = "logoUrl_example";  // string? | Welcome screen only (`welcome=true`): https URL of your logo, shown in a square tile, so use a square image. Without it the tile shows the first letter of `brandName`, or the Zernio mark when there is no `brandName` either. Rejected with 400 `INVALID_FIELD_VALUE` when the welcome screen is not shown. (optional) 
            var language = "en";  // string? | Hosted signup page only (`signup=hosted`, WhatsApp): language of the page and its follow-along guide. Explainer videos stay in English. Default `en`. Rejected without `signup=hosted`. (optional) 
            var handoff = false;  // bool? | Let the user finish on their phone. When `true`, the response also carries `handoff`. Show `handoff.url` as a QR code in your app (any QR library); the user scans it and the welcome screen opens on the phone, already carrying this connect.  They log in to the platform there without signing in to anything else. The phone ends on a Zernio result screen telling them to go back to their computer.  - Learn the outcome by polling `GET /v1/connect/handoffs/{handoffId}` (every 2 to 5 seconds is fine) or from the `account.connected` webhook. - Shows the welcome screen with your branding parameters or saved settings. - Cannot be combined with `welcome=false`, `headless=true`, `signup`, `redirect=true` or `redirect_url` (400 `INVALID_FIELD_VALUE`). - `handoff.url` works for 30 minutes. - When the account is re-enabled straight away, the response carries `account` instead, as without `handoff`.  (optional)  (default to false)

            try
            {
                // Get OAuth connect URL
                GetConnectUrl200Response result = apiInstance.GetConnectUrl(platform, profileId, reconnectAccountId, oauthAppId, expectedPlatformUserId, expectedUsername, forceReauth, redirectUrl, scopes, loginHint, headless, loginMethod, onboarding, signup, brandName, primaryColor, welcome, welcomeTheme, logoUrl, language, handoff);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetConnectUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetConnectUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get OAuth connect URL
    ApiResponse<GetConnectUrl200Response> response = apiInstance.GetConnectUrlWithHttpInfo(platform, profileId, reconnectAccountId, oauthAppId, expectedPlatformUserId, expectedUsername, forceReauth, redirectUrl, scopes, loginHint, headless, loginMethod, onboarding, signup, brandName, primaryColor, welcome, welcomeTheme, logoUrl, language, handoff);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetConnectUrlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **platform** | **string** | Social media platform to connect. &#x60;snapchat&#x60; is a closed beta with no public release date: it returns 403 &#x60;PLATFORM_BETA_RESTRICTED&#x60; until the account is approved. |  |
| **profileId** | **string** | Your Zernio profile ID (get from /v1/profiles). For WhatsApp, a Zernio-provisioned number can only be connected on the profile it was provisioned to; connecting from any other profile is rejected with a 409. |  |
| **reconnectAccountId** | **string?** | Refresh this existing account: a Zernio account id of the same platform on this profile (otherwise 400).  The OAuth callback and the selection endpoints (select-page, select-organization, select-board, select-location, Instagram and Snapchat selection) refuse with &#x60;reconnect_account_mismatch&#x60; a login that would write to a different account of the platform on this profile instead of this one.  In headless mode the marker travels in the redirect_url we hand you, so pass that URL back unchanged to the selection endpoint. On X it counts toward the OAuth state limit described under redirect_url.  | [optional]  |
| **oauthAppId** | **string?** | Connect through one of your own OAuth apps (see /v1/connect/oauth-apps), so the consent screen shows your app and the platform&#39;s limits are your app&#39;s. Without it the connect runs on Zernio&#39;s app, whatever apps the workspace has saved.  - Only platforms listed in &#x60;platforms&#x60; of GET /v1/connect/oauth-apps accept an app. Any other returns 400, and so do ads connects (&#x60;adsConnect&#x3D;true&#x60; in the redirect URL). - Connects that end on a destination picker also return 400, except Facebook Pages, Google Business locations, Pinterest boards and Snapchat public profiles (Instagram through Facebook Login, for example). - A LinkedIn connect through an app saves the member&#39;s own profile: organization pages, and mention lookups, stay on Zernio&#39;s app. - The connect requests the app&#39;s &#x60;scopeAreas&#x60;. &#x60;scopes&#x60; may narrow them but not add an area the app does not enable (400). - If the user does not grant every requested area, the account still connects and the redirect carries &#x60;missing_permissions&#x3D;&lt;areas&gt;&#x60; (the headless POST returns &#x60;missingPermissions&#x60;). - If the platform refuses a permission your app is not approved for, the redirect carries &#x60;error&#x3D;oauth_app_scope_not_allowed&#x60;.  The account remembers the app, and token refresh, publishing and inbox run on it. Reconnecting through another app, or without one, moves the account to that app.  | [optional]  |
| **expectedPlatformUserId** | **string?** | Only connect if the login lands on this platform account. Any other account ends the flow with &#x60;error&#x3D;account_mismatch&#x60; (a 409 &#x60;account_mismatch&#x60; on POST /v1/connect/instagram/select-account) and nothing is written.  Compared with every id the platform reports for the authorized account:  - Any platform: the &#x60;platformUserId&#x60; of a Zernio account on this platform. - Instagram: either the app-scoped id or the professional account id (&#x60;metadata.instagramScopedId&#x60;, the &#x60;17841...&#x60; id that Facebook Login accounts hold as platformUserId). - TikTok: open_ids are app-scoped, so an id from your own TikTok app never matches. Use expectedUsername there.  Honoured by the OAuth callback (every platform that connects without a selection step, Instagram Login included) and by the Instagram selection step. On the other selection endpoints you choose the destination yourself.  In headless mode the marker travels in the redirect_url we hand you, so pass that URL back unchanged. On X it counts toward the OAuth state limit described under redirect_url.  | [optional]  |
| **expectedUsername** | **string?** | Only connect if the authorized account&#39;s handle is this one (case-insensitive, a leading @ is ignored). Otherwise the flow ends with &#x60;error&#x3D;account_mismatch&#x60; and &#x60;error_message&#x60; naming the handle that was authorized, and nothing is written.  Same coverage and transport as expectedPlatformUserId; when both are sent, both must match. Use this on a first connection, where you hold the handle the user typed but no Zernio id yet.  | [optional]  |
| **forceReauth** | **bool?** | Instagram Login only (the default loginMethod); ignored elsewhere. Makes Instagram show its login page and ask for the credentials of the account to connect, even when another Instagram account is logged in on the device or app. Also hides the Facebook login option on that page.  Use it when the person connecting manages several Instagram accounts on one phone: otherwise Instagram logs in, and converts to a professional account, whichever account is active, before any consent screen. Pair it with expectedUsername to also refuse a wrong account at the end.  | [optional] [default to false] |
| **redirectUrl** | **string?** | Your custom redirect URL after the connection completes. It MUST be an absolute http(s) URL or a custom app scheme for mobile deeplinks (e.g. myapp://callback). A relative path is rejected with 400 &#x60;INVALID_REDIRECT_URL&#x60;.  **Exit notice:** when &#x60;redirect_url&#x60; is an http(s) URL on another site (anything but zernio.com), every redirect of the flow lands first on &#x60;https://zernio.com/connect/continue?to&#x3D;&lt;your URL&gt;&#x60;, a Zernio page that names your site and continues to it with one click. All params below reach your URL unchanged.  A custom app scheme (myapp://...) never goes through the notice. In headless mode the redirects we hand you (and the &#x60;redirect_url&#x60; returned by the selection endpoints) are notice URLs: pass them back or navigate to them as they are.  **X (twitter) length limit:** X caps the OAuth &#x60;state&#x60; at 500 characters and the redirect travels inside it (wrapped in the notice URL for an http(s) URL on another site). The URL-encoded form must be at most 258 characters for API callers, 310 for dashboard sessions.  In headless mode the appended &#x60;headless&#x3D;true&#x60; counts toward that limit. A plain https URL on another site leaves about 165 to 190 characters of your own URL, depending on encoding. A longer one is rejected with 400 &#x60;INVALID_REDIRECT_URL&#x60;, and the error says by how much.  **Success params** are appended with the URL API, so an existing query string is preserved:  - Standard mode: connected&#x3D;{platform}&amp;profileId&#x3D;X&amp;accountId&#x3D;Y&amp;username&#x3D;Z. - Headless mode: OAuth data params for platforms requiring selection (e.g. LinkedIn orgs, Facebook pages). If no selection is needed, the account is created directly and the redirect includes accountId.  **Failure params:** the browser goes to the same redirect_url with &#x60;error&#x60; and &#x60;platform&#x60; appended (always present). &#x60;error_message&#x60;, &#x60;is_user_fixable&#x60;, &#x60;reason&#x60;, &#x60;dashboard_url&#x60;, &#x60;missing_scopes&#x60;, &#x60;error_reason&#x60; and the &#x60;platform_error*&#x60; params are conditional: treat them as optional.  Your own query params are kept on every redirect, but ours overwrite one of yours with the same name. On an error redirect we remove the internal &#x60;headless&#x60;, &#x60;adsConnect&#x60;, &#x60;adsScope&#x60;, &#x60;reconnectAccountId&#x60;, &#x60;expectedPlatformUserId&#x60; and &#x60;expectedUsername&#x60; markers added during the flow.  **Correlation** params appear on every redirect from an OAuth callback (success and failure) and on the &#x60;redirect_url&#x60; returned by the selection endpoints such as POST /v1/connect/facebook/select-page:  - &#x60;request_id&#x60;: the id we log that request under. Quote it when reporting a problem. - &#x60;stage&#x60;: where the flow ended. &#x60;authorize&#x60; &#x3D; the platform&#39;s consent dialog returned an error or denial instead of a code. &#x60;callback&#x60; &#x3D; we processed the returned code (success, a selection step, or a failure). - &#x60;stage&#x60; &#x3D; &#x60;select_page&#x60;: the destination-selection endpoint (page, account, organization, board, location, profile or phone number) completed it.  **Error details:**  - &#x60;oauth_denied&#x60;: carries &#x60;error_message&#x60; and, when the platform sent them, its own &#x60;platform_error&#x60; (e.g. &#x60;access_denied&#x60;), &#x60;platform_error_reason&#x60; (e.g. &#x60;user_denied&#x60;) and &#x60;platform_error_description&#x60; (truncated to 500 characters). &#x60;is_user_fixable&#x3D;true&#x60; when the platform reported that the user cancelled or declined. - &#x60;no_facebook_pages&#x60;: comes with &#x60;is_user_fixable&#x3D;true&#x60;, an &#x60;error_message&#x60; telling the user to click \&quot;Edit previous settings\&quot; in Meta&#39;s dialog and tick the Page (or create one), and &#x60;error_reason&#x60; when Meta&#39;s token debug answered (values below). - &#x60;code_already_redeemed&#x60;: the same authorization code arrived more than once and an earlier request already processed it (the code is never sent to the platform twice). Not a failure: check GET /v1/accounts or wait for the &#x60;account.connected&#x60; webhook. - &#x60;missing_google_permissions&#x60; (YouTube, Google Business and Google Ads): the user unchecked permissions on Google&#39;s consent screen. Always with &#x60;is_user_fixable&#x3D;true&#x60;. When Google reported granted scopes, &#x60;missing_scopes&#x60; lists the requested scopes not granted (comma-separated). Ask the user to connect again keeping every permission checked. - &#x60;no_youtube_channel&#x60;: Google authorized the account but it has no YouTube channel we can connect. Always with &#x60;is_user_fixable&#x3D;true&#x60; and an &#x60;error_message&#x60;.  Usual causes of &#x60;no_youtube_channel&#x60;: the user picked their personal Google identity instead of the Brand Account in Google&#39;s account chooser, they only have YouTube Studio access (not Brand Account owner or manager), or the account has no channel yet.  &#x60;error_reason&#x60; values for &#x60;no_facebook_pages&#x60;:  - &#x60;pages_permission_declined&#x60;: the user declined the pages_show_list permission. - &#x60;no_pages_granted&#x60;: the permission was granted with no Page ticked. Meta reports a user who manages no Page the same way, so this covers both. - &#x60;granted_pages_not_listed&#x60;: Pages were ticked but Meta listed none the user can manage, and a direct read of each ticked Page returned no access token.  **Headless &#x60;userProfile&#x60;:** on headless Facebook success (&#x60;step&#x3D;select_page&#x60;) and headless Instagram &#x60;facebook_login&#x60; success (&#x60;step&#x3D;select_account&#x60;), &#x60;userProfile&#x60; is JSON percent-encoded once before being set as a query param, so it is encoded twice on the wire.  After your framework decodes the query string once, run one more decodeURIComponent (or equivalent), then JSON.parse it. &#x60;tempToken&#x60; and &#x60;connect_token&#x60; are plain values.  **Error values.** This list is NOT exhaustive and new values may be added at any time: treat an unrecognized value as a generic failure rather than matching exhaustively. Existing values are not renamed or removed without notice.  - OAuth and callback: &#x60;oauth_denied&#x60;, &#x60;invalid_callback&#x60;, &#x60;invalid_state&#x60;, &#x60;unsupported_platform&#x60;, &#x60;connection_failed&#x60;, &#x60;internal_error&#x60;, &#x60;token_exchange_failed&#x60;, &#x60;byok_config_error&#x60;, &#x60;personal_account_not_supported&#x60;, &#x60;missing_google_permissions&#x60;, &#x60;missing_tiktok_permissions&#x60;, &#x60;platform_requires_destination&#x60;, &#x60;reconnect_account_mismatch&#x60;, &#x60;account_mismatch&#x60;, &#x60;instagram_login_method_mismatch&#x60;, &#x60;invalid_request&#x60;, &#x60;code_already_redeemed&#x60;. - Access and limits: &#x60;profile_not_found&#x60;, &#x60;invalid_profile_id&#x60;, &#x60;access_denied&#x60;, &#x60;account_limit_exceeded&#x60;, &#x60;profile_limit_exceeded&#x60;, &#x60;payment_required&#x60;. - Destination selection: &#x60;no_facebook_pages&#x60;, &#x60;facebook_pages_error&#x60;, &#x60;no_google_locations&#x60;, &#x60;google_locations_error&#x60;, &#x60;google_permission_denied&#x60;, &#x60;no_snapchat_public_profiles&#x60;, &#x60;snapchat_profiles_error&#x60;, &#x60;no_youtube_channel&#x60;, &#x60;discord_no_guild&#x60;, &#x60;slack_no_team&#x60;. - WhatsApp: &#x60;whatsapp_error&#x60;, &#x60;one_whatsapp_per_profile&#x60;, &#x60;whatsapp_number_already_connected&#x60;, &#x60;whatsapp_number_pinned_to_profile&#x60;, &#x60;whatsapp_coexistence_not_registered&#x60;, &#x60;connection_cancelled&#x60;. - Google Ads (platform&#x3D;googleads): &#x60;google_ads_auth_failed&#x60;, &#x60;google_ads_invalid_state&#x60;, &#x60;google_ads_config_error&#x60;, &#x60;google_ads_token_failed&#x60;, &#x60;google_ads_quota_exhausted&#x60;, &#x60;google_ads_callback_error&#x60;. - TikTok Ads (platform&#x3D;tiktokads): &#x60;tiktok_ads_auth_failed&#x60;, &#x60;tiktok_ads_invalid_state&#x60;, &#x60;tiktok_ads_access_denied&#x60;, &#x60;tiktok_ads_config_error&#x60;, &#x60;tiktok_ads_token_failed&#x60;, &#x60;tiktok_ads_account_not_found&#x60;, &#x60;tiktok_ads_callback_error&#x60;. - X Ads (platform&#x3D;xads): &#x60;x_ads_denied&#x60;, &#x60;x_ads_auth_failed&#x60;, &#x60;x_ads_config_error&#x60;, &#x60;x_ads_account_not_found&#x60;, &#x60;x_ads_state_error&#x60;, &#x60;x_ads_token_failed&#x60;, &#x60;x_ads_token_missing&#x60;, &#x60;x_ads_callback_error&#x60;. - Reddit Ads (platform&#x3D;redditads): &#x60;reddit_ads_auth_failed&#x60;, &#x60;reddit_ads_invalid_state&#x60;, &#x60;reddit_ads_access_denied&#x60;, &#x60;reddit_ads_scope_not_granted&#x60;, &#x60;reddit_ads_no_ad_accounts&#x60;, &#x60;reddit_ads_callback_error&#x60;. - Shopify (platform&#x3D;shopify): &#x60;shopify_auth_failed&#x60;, &#x60;shopify_config_error&#x60;, &#x60;shopify_invalid_state&#x60;, &#x60;shopify_invalid_hmac&#x60;, &#x60;shopify_invalid_shop&#x60;, &#x60;shopify_missing_scopes&#x60;, &#x60;shopify_callback_error&#x60;.  Notes:  1. On this endpoint every upstream OAuth error collapses into &#x60;oauth_denied&#x60;, with the provider&#39;s values in the &#x60;platform_error*&#x60; params. The dedicated ads flows differ: they use their own denial slugs, and &#x60;google_ads_auth_failed&#x60; and &#x60;tiktok_ads_auth_failed&#x60; may carry the provider&#39;s raw error string in &#x60;error_message&#x60;. 2. On the tiktok and twitter ads flows &#x60;platform&#x60; carries the ads platform id (&#x60;tiktokads&#x60;, &#x60;xads&#x60;), not the value in the request path. The googleads, redditads and shopify flows report &#x60;googleads&#x60;, &#x60;redditads&#x60; and &#x60;shopify&#x60;. 3. &#x60;missing_tiktok_permissions&#x60;: the TikTok authorization left out a permission the already-connected account needs, so nothing changed and it keeps working as before. User-fixable: connect again and accept every permission on TikTok&#39;s screen. 4. &#x60;instagram_login_method_mismatch&#x60;: an Instagram Login authorization landed on a profile whose Instagram account is connected through Facebook Login, so nothing changed. To refresh it, connect again with &#x60;loginMethod&#x3D;facebook_login&#x60;. To move it to Instagram Login, disconnect it first.  | [optional]  |
| **scopes** | **string?** | Comma-separated permission areas to request instead of the platform&#39;s full permission set.  **Values:** &#x60;posting&#x60;, &#x60;analytics&#x60;, &#x60;comments&#x60;, &#x60;messaging&#x60;, &#x60;ads&#x60;; on google and microsoft, &#x60;email&#x60;, &#x60;calendar&#x60;, &#x60;files&#x60;, &#x60;contacts&#x60;.  **Default:** omit it (what the dashboard does) to request everything the platform supports. Google and microsoft REQUIRE it (400 &#x60;INVALID_FIELD_VALUE&#x60; when absent) because their consent screens are reviewed per area.  When present, the consent dialog asks only for the scopes behind those areas, plus the scopes every connection needs (identity, token refresh, listing the pages, organizations or channels the user picks from).  - Scopes never asked for are absent from the account&#39;s &#x60;permissions&#x60;, and the health endpoints report them as not granted. A &#x60;posting&#x60;-only account cannot read analytics or the inbox until reconnected with more areas. - First comments need &#x60;comments&#x60;: a &#x60;posting&#x60;-only account publishes the post and skips the first comment. - Scopes in none of the areas (X likes, bookmarks and follows, Pinterest ads-only extras) are requested only when the parameter is omitted.  **Supported on** facebook, instagram (both login methods), linkedin, twitter, tiktok, youtube, threads, reddit, pinterest, googlebusiness and slack (via &#x60;GET /v1/connect/slack&#x60;).  **Rejected** with 400 &#x60;INVALID_FIELD_VALUE&#x60; (&#x60;param: scopes&#x60;) on bluesky, telegram, discord, snapchat and whatsapp (their dialog cannot be reduced), and for an empty list or an unknown area.  What each area asks for, per platform (Google scopes shortened to their last path segment):  | Platform | &#x60;posting&#x60; | &#x60;analytics&#x60; | &#x60;comments&#x60; | &#x60;messaging&#x60; | &#x60;ads&#x60; | Always requested | |- --|- --|- --|- --|- --|- --|- --| | facebook | &#x60;pages_manage_posts&#x60; | &#x60;read_insights&#x60;, &#x60;pages_read_user_content&#x60; | &#x60;pages_manage_engagement&#x60;, &#x60;pages_read_user_content&#x60; | &#x60;pages_messaging&#x60; | &#x60;ads_management&#x60;, &#x60;ads_read&#x60;, &#x60;leads_retrieval&#x60;, &#x60;pages_manage_ads&#x60;, &#x60;instagram_basic&#x60;, &#x60;business_management&#x60; | &#x60;pages_show_list&#x60;, &#x60;pages_read_engagement&#x60;, &#x60;pages_manage_metadata&#x60; | | instagram (Instagram Login) | &#x60;instagram_business_content_publish&#x60; | &#x60;instagram_business_manage_insights&#x60; | &#x60;instagram_business_manage_comments&#x60; | &#x60;instagram_business_manage_messages&#x60; | none | &#x60;instagram_business_basic&#x60; | | instagram (&#x60;loginMethod&#x3D;facebook_login&#x60;) | &#x60;instagram_content_publish&#x60; | &#x60;instagram_manage_insights&#x60; | &#x60;instagram_manage_comments&#x60; | &#x60;instagram_manage_messages&#x60; | &#x60;ads_management&#x60;, &#x60;ads_read&#x60;, &#x60;leads_retrieval&#x60;, &#x60;pages_manage_ads&#x60; | &#x60;instagram_basic&#x60;, &#x60;pages_show_list&#x60;, &#x60;pages_read_engagement&#x60;, &#x60;business_management&#x60;, &#x60;pages_messaging&#x60;, &#x60;pages_manage_metadata&#x60; | | linkedin | &#x60;w_member_social&#x60;, &#x60;w_organization_social&#x60;, &#x60;r_organization_social&#x60;, &#x60;r_organization_followers&#x60; | &#x60;r_member_postAnalytics&#x60;, &#x60;r_member_profileAnalytics&#x60;, &#x60;rw_organization_admin&#x60;, &#x60;r_organization_social&#x60;, &#x60;r_organization_followers&#x60; | &#x60;w_member_social&#x60;, &#x60;w_member_social_feed&#x60;, &#x60;w_organization_social&#x60;, &#x60;w_organization_social_feed&#x60;, &#x60;r_organization_social&#x60;, &#x60;r_organization_social_feed&#x60; | none | &#x60;r_ads&#x60;, &#x60;rw_ads&#x60;, &#x60;r_ads_reporting&#x60;, &#x60;r_marketing_leadgen_automation&#x60;, &#x60;rw_conversions&#x60; | &#x60;openid&#x60;, &#x60;profile&#x60;, &#x60;email&#x60;, &#x60;r_basicprofile&#x60;, &#x60;rw_organization_admin&#x60; | | twitter | &#x60;tweet.write&#x60;, &#x60;media.write&#x60; | (in the always-requested set) | &#x60;tweet.write&#x60;, &#x60;like.write&#x60;, &#x60;tweet.moderate.write&#x60; | &#x60;dm.read&#x60;, &#x60;dm.write&#x60;, &#x60;media.write&#x60; | none | &#x60;tweet.read&#x60;, &#x60;users.read&#x60;, &#x60;offline.access&#x60; | | tiktok | &#x60;video.publish&#x60; | &#x60;user.info.stats&#x60;, &#x60;user.insights&#x60;, &#x60;video.list&#x60;, &#x60;video.insights&#x60; | &#x60;comment.list&#x60;, &#x60;comment.list.manage&#x60;, &#x60;video.list&#x60; | &#x60;message.list.read&#x60;, &#x60;message.list.send&#x60;, &#x60;message.list.manage&#x60; | none | &#x60;user.info.basic&#x60;, &#x60;user.info.username&#x60;, &#x60;user.info.profile&#x60;, &#x60;user.account.type&#x60;, &#x60;video.publish&#x60;, &#x60;video.upload&#x60;, &#x60;video.list&#x60; | | youtube | &#x60;youtube.upload&#x60; | &#x60;yt-analytics.readonly&#x60; | &#x60;youtube.force-ssl&#x60; | none | none | &#x60;youtube&#x60; | | threads | &#x60;threads_content_publish&#x60;, &#x60;threads_manage_replies&#x60;, &#x60;threads_delete&#x60; | &#x60;threads_manage_insights&#x60; | &#x60;threads_content_publish&#x60;, &#x60;threads_read_replies&#x60;, &#x60;threads_manage_replies&#x60;, &#x60;threads_delete&#x60; | none | none | &#x60;threads_basic&#x60; | | reddit | &#x60;submit&#x60;, &#x60;read&#x60;, &#x60;mysubreddits&#x60;, &#x60;flair&#x60;, &#x60;history&#x60;, &#x60;edit&#x60; | &#x60;read&#x60;, &#x60;history&#x60; | &#x60;read&#x60;, &#x60;history&#x60;, &#x60;edit&#x60;, &#x60;vote&#x60; | &#x60;privatemessages&#x60; | none | &#x60;identity&#x60; | | pinterest | &#x60;boards:write&#x60;, &#x60;pins:read&#x60;, &#x60;pins:write&#x60; | &#x60;pins:read&#x60;, &#x60;user_accounts:read&#x60; | none | none | &#x60;ads:read&#x60;, &#x60;ads:write&#x60;, &#x60;boards:write&#x60;, &#x60;pins:read&#x60;, &#x60;pins:write&#x60; | &#x60;boards:read&#x60;, &#x60;user_accounts:read&#x60; | | googlebusiness | &#x60;business.manage&#x60; | &#x60;business.manage&#x60; | &#x60;business.manage&#x60; | none | none | &#x60;business.manage&#x60;, &#x60;userinfo.profile&#x60;, &#x60;userinfo.email&#x60; | | slack | &#x60;chat:write&#x60;, &#x60;chat:write.public&#x60;, &#x60;chat:write.customize&#x60;, &#x60;files:write&#x60;, &#x60;files:read&#x60; | none | none | &#x60;chat:write&#x60;, &#x60;chat:write.customize&#x60;, &#x60;files:write&#x60;, &#x60;files:read&#x60;, &#x60;channels:history&#x60;, &#x60;groups:history&#x60;, &#x60;im:history&#x60;, &#x60;mpim:history&#x60;, &#x60;im:read&#x60;, &#x60;im:write&#x60;, &#x60;mpim:read&#x60;, &#x60;users:read&#x60;, &#x60;reactions:read&#x60;, &#x60;reactions:write&#x60; | none | &#x60;channels:join&#x60;, &#x60;channels:read&#x60;, &#x60;groups:read&#x60;, &#x60;team:read&#x60; |  Google and Microsoft accounts use the mailbox areas instead (&#x60;scopes&#x60; is required there):  | Platform | &#x60;email&#x60; | &#x60;calendar&#x60; | &#x60;files&#x60; | &#x60;contacts&#x60; | Always requested | |- --|- --|- --|- --|- --|- --| | google | &#x60;gmail.modify&#x60; | &#x60;calendar&#x60; | &#x60;drive.file&#x60; (only files Zernio created or the user picked, see the Files tag) | &#x60;contacts.readonly&#x60; | &#x60;openid&#x60;, &#x60;userinfo.email&#x60;, &#x60;userinfo.profile&#x60; | | microsoft | &#x60;Mail.ReadWrite&#x60;, &#x60;Mail.Send&#x60; | &#x60;Calendars.ReadWrite&#x60; | &#x60;Files.ReadWrite&#x60; | &#x60;Contacts.Read&#x60; | &#x60;openid&#x60;, &#x60;profile&#x60;, &#x60;email&#x60;, &#x60;offline_access&#x60;, &#x60;User.Read&#x60; |  Areas accumulate: reconnecting with more areas widens the grant, and &#x60;GET /v1/accounts/{accountId}/health&#x60; reports the result.  | [optional]  |
| **loginHint** | **string?** | google and microsoft only: pre-fills the account picker with this address so the user lands on the right mailbox. | [optional]  |
| **headless** | **bool?** | When true, the user is redirected to your redirect_url with raw OAuth data (code, state) instead of Zernio&#39;s default account selection UI. Use this to build a custom connect experience. | [optional] [default to false] |
| **loginMethod** | **string?** | Instagram only: which of the two Instagram connection methods to use. Ignored for every other platform.  - &#x60;instagram_login&#x60; (default when omitted): the Instagram Login dialog. The user authorizes their Instagram professional account directly, no Facebook Page required. Exception: if omitted and &#x60;reconnectAccountId&#x60; names an account connected with &#x60;facebook_login&#x60;, the reconnect keeps that method. - &#x60;facebook_login&#x60;: the Facebook Login dialog (\&quot;Instagram API with Facebook Login\&quot;). The user authorizes a Facebook Page with a linked Instagram professional account, and every API call for that account runs through the Page. Use it when the customer manages Instagram through a Page and expects the Facebook consent screen.  With &#x60;facebook_login&#x60; the user picks a Page, so the callback continues at the account-selection step, &#x60;/v1/connect/instagram/select-account&#x60;. The default &#x60;instagram_login&#x60; has no selection step and connects directly.  &#x60;facebook_login&#x60; supports &#x60;headless&#x3D;true&#x60; like the other selection platforms. The callback redirects to your &#x60;redirect_url&#x60; with &#x60;profileId&#x60;, &#x60;tempToken&#x60;, &#x60;platform&#x3D;instagram&#x60;, &#x60;step&#x3D;select_account&#x60;, &#x60;userProfile&#x60; and &#x60;connect_token&#x60;.  &#x60;userProfile&#x60; is the Facebook user&#39;s profile, same shape and encoding as the Facebook &#x60;step&#x3D;select_page&#x60; redirect. Pass &#x60;profileId&#x60;, &#x60;tempToken&#x60; and &#x60;connect_token&#x60; into the select-account endpoints to finish.  | [optional] [default to instagram_login] |
| **onboarding** | **string?** | WhatsApp only. Ignored for every other platform. Controls which screen Meta&#39;s Embedded Signup popup shows.  If omitted, the connection defaults to coexistence (same as &#x60;business_app&#x60; below), preserving existing behavior for numbers already on the WhatsApp Business app.  &#x60;api&#x60;: standard Embedded Signup, showing Meta&#39;s WABA/number picker. Use this to connect a phone number already on Cloud API elsewhere.  &#x60;business_app&#x60;: coexistence, i.e. &#39;Connect existing WhatsApp Business app&#39; (a number shared between Cloud API and the consumer WhatsApp Business app).  | [optional]  |
| **signup** | **string?** | WhatsApp only. Rejected with 400 &#x60;INVALID_FIELD_VALUE&#x60; on any other platform.  &#x60;hosted&#x60;: &#x60;authUrl&#x60; points at a Zernio-hosted page on zernio.com instead of Meta&#39;s OAuth dialog, and the response carries &#x60;authUrl&#x60; only (no &#x60;state&#x60;). That page opens Meta&#39;s Embedded Signup popup itself, so it connects exactly the WhatsApp Business Account and number the user picked in the popup.  **When to use it**: your users&#39; Facebook logins manage several WhatsApp accounts. On the default redirect flow Meta only returns an authorization code, so when that login can see more than one number the user lands on Zernio&#39;s number picker and has to choose again.  **Flow**: nothing to embed and no domain setup. Send the user to &#x60;authUrl&#x60;; they come back to &#x60;redirect_url&#x60; with the same params as the redirect flow.  - Success: &#x60;connected&#x3D;whatsapp&#x60;, &#x60;profileId&#x60;, &#x60;accountId&#x60;, &#x60;username&#x60; (plus &#x60;connect_token&#x60; for API-key callers). - Failure: &#x60;error&#x60; and &#x60;platform&#x3D;whatsapp&#x60;, with the same values and extras as the redirect flow (see below), plus two of its own.  Redirect-flow failures: &#x60;one_whatsapp_per_profile&#x60;, &#x60;whatsapp_number_already_connected&#x60;, &#x60;whatsapp_number_pinned_to_profile&#x60; and &#x60;whatsapp_coexistence_not_registered&#x60; with &#x60;is_user_fixable&#x3D;true&#x60;; &#x60;payment_required&#x60; with &#x60;reason&#x60; and &#x60;dashboard_url&#x60;; &#x60;whatsapp_error&#x60; with &#x60;error_message&#x60; when Meta reported one.  Hosted-only failures:  - &#x60;connection_cancelled&#x60;: the popup was closed before finishing (&#x60;error_message&#x60; carries Meta&#39;s last reported step or error when there is one). - &#x60;session_expired&#x60;: the user took longer than the 60 minute window the hosted page is valid for. Restart the flow with a new call.  **Same as the redirect flow**: &#x60;onboarding&#x60; is carried through, and a pre-verified Zernio-provisioned number is attached.  When a previously disconnected account for this profile can simply be re-enabled, this endpoint re-enables it and returns the account directly instead of a URL. &#x60;headless&#x60; has no effect, because there is no selection step left to hand you.  **The page** shows the same guidance as the Zernio dashboard: a pre-verified Zernio-provisioned number is called out by name (\&quot;choose it in Meta&#39;s list, no code will be asked\&quot;).  Coexistence and standard signups get their explainer video, and a step-by-step checklist stays visible while Meta&#39;s popup is open. Skin it with &#x60;brandName&#x60;, &#x60;primaryColor&#x60; and &#x60;language&#x60; below.  | [optional]  |
| **brandName** | **string?** | Your product name, for the two branded pages. Trimmed; 1 to 60 characters.  - With &#x60;signup&#x3D;hosted&#x60; (WhatsApp): replaces Zernio in the page title (\&quot;Connect your WhatsApp number to &lt;brandName&gt;\&quot;). - With &#x60;welcome&#x3D;true&#x60;: fills the heading (\&quot;&lt;brandName&gt; wants to connect to your &lt;platform&gt;\&quot;). Without it the screen shows Zernio and the Zernio mark.  Both pages keep a Zernio mark: they are co-branded, not white-label. Rejected with 400 &#x60;INVALID_FIELD_VALUE&#x60; without &#x60;signup&#x3D;hosted&#x60; or &#x60;welcome&#x3D;true&#x60;. Sealed into the page link at issue time, so editing the URL cannot change it.  | [optional]  |
| **primaryColor** | **string?** | Hex colour (&#x60;#RRGGBB&#x60;) for the primary button on the hosted WhatsApp signup page (&#x60;signup&#x3D;hosted&#x60;) or the welcome screen (&#x60;welcome&#x3D;true&#x60;). Validated server-side; anything else is a 400 &#x60;INVALID_FIELD_VALUE&#x60;. Rejected without one of the two. | [optional]  |
| **welcome** | **bool?** | Any platform. When &#x60;true&#x60;, &#x60;authUrl&#x60; points to a Zernio-hosted welcome screen showing your brand next to the platform (\&quot;&lt;brandName&gt; wants to connect to your &lt;platform&gt;\&quot;). Its button reads Connecting for about a second, then sends the user to the platform&#39;s authorization screen with no click.  The rest of the flow is unchanged.  - &#x60;brandName&#x60;, &#x60;logoUrl&#x60;, &#x60;primaryColor&#x60; and &#x60;welcomeTheme&#x60; are optional and default to Zernio&#39;s own name, mark and look. - The link is valid for 30 minutes; after that the page asks the user to start again. - The brand also carries to the account and channel pickers Zernio shows after authorization. - With no &#x60;redirect_url&#x60;, the flow ends on a branded Zernio-hosted page saying whether the account connected, instead of the Zernio dashboard. - Cannot be combined with &#x60;headless&#x3D;true&#x60; or &#x60;signup&#x3D;hosted&#x60; (400 &#x60;INVALID_FIELD_VALUE&#x60;). - The platform&#39;s authorization screen still names the Zernio app.  Recommended. When left out, the screen is shown if the workspace saved it as on by default (&#x60;PUT /v1/connect/welcome-screen&#x60;), except with &#x60;headless&#x3D;true&#x60; or &#x60;signup&#x3D;hosted&#x60;. Pass &#x60;false&#x60; to skip it.  Branding you leave out of the call comes from those saved settings, and a &#x60;welcomeTheme&#x60; you send is merged key by key over the saved theme.  | [optional]  |
| **welcomeTheme** | **string?** | Welcome screen only (&#x60;welcome&#x3D;true&#x60;). A URL-encoded JSON object that restyles and rewords the screen. All keys are optional.  - **Copy**: &#x60;heading&#x60; (up to 120 characters); &#x60;trustLine&#x60;, &#x60;consentLine&#x60; and &#x60;statusLine&#x60; (up to 200 each, &#x60;statusLine&#x60; being the line above the button); &#x60;buttonLabel&#x60; (up to 30, the label of the link the button becomes if the redirect stalls). - **Closing page** (shown when there is no &#x60;redirect_url&#x60;): &#x60;successHeading&#x60; and &#x60;errorHeading&#x60; (up to 120), &#x60;successBody&#x60; and &#x60;errorBody&#x60; (up to 200). All copy may contain the placeholders &#x60;{brand}&#x60; and &#x60;{platform}&#x60;. - **Colors**: &#x60;primaryColor&#x60; (the button), &#x60;accentColor&#x60; (the header gradient, built as a scale of that colour, and the icons), &#x60;pageColor&#x60;, &#x60;cardColor&#x60; and &#x60;textColor&#x60;, all as &#x60;#RRGGBB&#x60;. - **Style**: &#x60;cornerRadius&#x60; as an integer from 0 to 24 (pixels); &#x60;font&#x60; as &#x60;sans&#x60;, &#x60;serif&#x60; or &#x60;mono&#x60;; &#x60;bannerStyle&#x60; as &#x60;halftone&#x60; (default), &#x60;solid&#x60; (a flat tint of &#x60;accentColor&#x60;) or &#x60;plain&#x60; (no banner fill). - **Icons**: &#x60;trustLineIcon&#x60; (default &#x60;shield&#x60;) and &#x60;consentLineIcon&#x60; (default &#x60;link&#x60;), each one of &#x60;shield&#x60;, &#x60;lock&#x60;, &#x60;link&#x60;, &#x60;check&#x60;, &#x60;user&#x60;, &#x60;sparkles&#x60; or &#x60;none&#x60;. - **Visibility**: &#x60;hide&#x60;, an array of any of &#x60;heading&#x60;, &#x60;trustLine&#x60;, &#x60;consentLine&#x60;, &#x60;statusLine&#x60;, &#x60;successBody&#x60; and &#x60;errorBody&#x60;, removes those lines from the screens. - **Links**: &#x60;termsUrl&#x60; and &#x60;privacyUrl&#x60; (https, up to 2048 characters) add small Terms and Privacy links at the bottom of every hosted screen.  A &#x60;primaryColor&#x60; here wins over the &#x60;primaryColor&#x60; parameter. Unknown keys, invalid JSON or an invalid value are a 400 &#x60;INVALID_FIELD_VALUE&#x60;. Rejected when the welcome screen is not shown.  Example: &#x60;{\&quot;heading\&quot;:\&quot;Link your {platform} to {brand}\&quot;,\&quot;cardColor\&quot;:\&quot;#FFF7ED\&quot;,\&quot;cornerRadius\&quot;:12}&#x60;.  | [optional]  |
| **logoUrl** | **string?** | Welcome screen only (&#x60;welcome&#x3D;true&#x60;): https URL of your logo, shown in a square tile, so use a square image. Without it the tile shows the first letter of &#x60;brandName&#x60;, or the Zernio mark when there is no &#x60;brandName&#x60; either. Rejected with 400 &#x60;INVALID_FIELD_VALUE&#x60; when the welcome screen is not shown. | [optional]  |
| **language** | **string?** | Hosted signup page only (&#x60;signup&#x3D;hosted&#x60;, WhatsApp): language of the page and its follow-along guide. Explainer videos stay in English. Default &#x60;en&#x60;. Rejected without &#x60;signup&#x3D;hosted&#x60;. | [optional]  |
| **handoff** | **bool?** | Let the user finish on their phone. When &#x60;true&#x60;, the response also carries &#x60;handoff&#x60;. Show &#x60;handoff.url&#x60; as a QR code in your app (any QR library); the user scans it and the welcome screen opens on the phone, already carrying this connect.  They log in to the platform there without signing in to anything else. The phone ends on a Zernio result screen telling them to go back to their computer.  - Learn the outcome by polling &#x60;GET /v1/connect/handoffs/{handoffId}&#x60; (every 2 to 5 seconds is fine) or from the &#x60;account.connected&#x60; webhook. - Shows the welcome screen with your branding parameters or saved settings. - Cannot be combined with &#x60;welcome&#x3D;false&#x60;, &#x60;headless&#x3D;true&#x60;, &#x60;signup&#x60;, &#x60;redirect&#x3D;true&#x60; or &#x60;redirect_url&#x60; (400 &#x60;INVALID_FIELD_VALUE&#x60;). - &#x60;handoff.url&#x60; works for 30 minutes. - When the account is re-enabled straight away, the response carries &#x60;account&#x60; instead, as without &#x60;handoff&#x60;.  | [optional] [default to false] |

### Return type

[**GetConnectUrl200Response**](GetConnectUrl200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OAuth authorization URL to redirect user to |  -  |
| **400** | Missing/invalid parameters (e.g., invalid profileId format, a non-absolute redirect_url, or a redirect_url too long for X&#39;s 500-character state) |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | No access to profile, BYOK required for AppSumo X, or Snapchat closed beta (code PLATFORM_BETA_RESTRICTED) |  -  |
| **404** | Profile not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getconnectwelcomescreen"></a>
# **GetConnectWelcomeScreen**
> ConnectWelcomeScreen GetConnectWelcomeScreen ()

Get the saved welcome screen

The workspace's saved welcome screen settings, shared by the whole team. With `showByDefault` on, every `GET /v1/connect/{platform}` made with your API key shows the welcome screen before the platform's authorization screen, without `welcome=true` or any branding parameter. Connects started from the Zernio dashboard always show it, with this branding when saved.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetConnectWelcomeScreenExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);

            try
            {
                // Get the saved welcome screen
                ConnectWelcomeScreen result = apiInstance.GetConnectWelcomeScreen();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetConnectWelcomeScreen: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetConnectWelcomeScreenWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get the saved welcome screen
    ApiResponse<ConnectWelcomeScreen> response = apiInstance.GetConnectWelcomeScreenWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetConnectWelcomeScreenWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ConnectWelcomeScreen**](ConnectWelcomeScreen.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The saved settings. A workspace that never saved any gets &#x60;showByDefault&#x60; false and null fields. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getfacebookpages"></a>
# **GetFacebookPages**
> GetFacebookPages200Response GetFacebookPages (string accountId, bool? refresh = null)

List Facebook pages

Returns all Facebook Pages the connected account has access to, including the currently selected Page and the Instagram professional account linked to each Page.  Works on `facebook` accounts and on `metaads` accounts (classic and Facebook Login for Business connections).  - Business-login `metaads` connection: `selectedPageId` is the default Page ads run as, and every listed Page can be passed as `pageId` on POST /v1/ads/create. - Classic `metaads` connection: there is no default Page, so `selectedPageId` is null. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetFacebookPagesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var refresh = true;  // bool? | When true, bypasses the page cache and fetches fresh pages from Meta. Rate-limited server-side to 1 refresh per 60s. Pages no longer accessible to the connected account will be removed from the list on refresh.  (optional) 

            try
            {
                // List Facebook pages
                GetFacebookPages200Response result = apiInstance.GetFacebookPages(accountId, refresh);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetFacebookPages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFacebookPagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Facebook pages
    ApiResponse<GetFacebookPages200Response> response = apiInstance.GetFacebookPagesWithHttpInfo(accountId, refresh);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetFacebookPagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **refresh** | **bool?** | When true, bypasses the page cache and fetches fresh pages from Meta. Rate-limited server-side to 1 refresh per 60s. Pages no longer accessible to the connected account will be removed from the list on refresh.  | [optional]  |

### Return type

[**GetFacebookPages200Response**](GetFacebookPages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pages list |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found, or not a facebook or metaads account |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getgmblocations"></a>
# **GetGmbLocations**
> GetGmbLocations200Response GetGmbLocations (string accountId, string? search = null, string? filter = null, int? limit = null)

List Google Business Profile locations

Returns Google Business Profile locations the connected account can access, plus the currently selected location.  The list is bounded (see hasMore). For accounts that own many locations:  - use the search or filter query params to find a specific one instead of loading them all; - or raise limit to enumerate an account with more than 100 locations. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetGmbLocationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var search = "search_example";  // string? | Free-text search on the business name, applied server-side by Google. Use for accounts with many locations. (optional) 
            var filter = "filter_example";  // string? | Raw Google Business Information API filter expression (advanced; takes precedence over search), e.g. storeCode=\"LH279411\". (optional) 
            var limit = 100;  // int? | Max locations to return (default 100, max 500). Raise it to enumerate an account with more than 100 locations; for accounts with thousands, use search/filter instead. (optional)  (default to 100)

            try
            {
                // List Google Business Profile locations
                GetGmbLocations200Response result = apiInstance.GetGmbLocations(accountId, search, filter, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetGmbLocations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetGmbLocationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Google Business Profile locations
    ApiResponse<GetGmbLocations200Response> response = apiInstance.GetGmbLocationsWithHttpInfo(accountId, search, filter, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetGmbLocationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **search** | **string?** | Free-text search on the business name, applied server-side by Google. Use for accounts with many locations. | [optional]  |
| **filter** | **string?** | Raw Google Business Information API filter expression (advanced; takes precedence over search), e.g. storeCode&#x3D;\&quot;LH279411\&quot;. | [optional]  |
| **limit** | **int?** | Max locations to return (default 100, max 500). Raise it to enumerate an account with more than 100 locations; for accounts with thousands, use search/filter instead. | [optional] [default to 100] |

### Return type

[**GetGmbLocations200Response**](GetGmbLocations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Locations list |  -  |
| **400** | Invalid query parameter (e.g. limit out of range) |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getgoogleanalyticsconnecturl"></a>
# **GetGoogleAnalyticsConnectUrl**
> GetGoogleAnalyticsConnectUrl200Response GetGoogleAnalyticsConnectUrl (string profileId, string? redirectUrl = null, string? reconnectAccountId = null)

Get Google Analytics OAuth connect URL

Starts OAuth for Google Analytics (GA4). Each connected GA4 property becomes its own account with platform `googleanalytics`; it reads reports and does not post.  Requested scope: `https://www.googleapis.com/auth/analytics.readonly`.  ### Flow  Redirect the user to `authUrl`.  - **One readable property:** Zernio connects it and redirects to `redirect_url` (or the dashboard) with `connected=googleanalytics`, `profileId`, `accountId` and `username` (the property name). - **Several properties:** the user first picks one on a Zernio-hosted page, which then redirects the same way.  ### Your own property picker  Add `headless=true` to `redirect_url`. Zernio then redirects there with `step=select_property`, `profileId`, `platform=googleanalytics` and a `pendingDataToken` for `GET /v1/connect/googleanalytics/properties` and `POST /v1/connect/googleanalytics/select-property`.  ### Errors  On failure the redirect carries `error`, `platform=googleanalytics` and `error_message`. Errors include:  - `googleanalytics_scope_missing`: the user unticked Analytics access. - `googleanalytics_no_properties` 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetGoogleAnalyticsConnectUrlExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string | Your Zernio profile ID (get from /v1/profiles).
            var redirectUrl = "redirectUrl_example";  // string? | Custom redirect after connection. Must be an absolute http(s) URL or custom app scheme such as `myapp://callback`; relative and unsafe URLs return 400. (optional) 
            var reconnectAccountId = "reconnectAccountId_example";  // string? | Zernio account ID of the Google Analytics account being reconnected. Picking a different property then fails instead of adding a second account. (optional) 

            try
            {
                // Get Google Analytics OAuth connect URL
                GetGoogleAnalyticsConnectUrl200Response result = apiInstance.GetGoogleAnalyticsConnectUrl(profileId, redirectUrl, reconnectAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetGoogleAnalyticsConnectUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetGoogleAnalyticsConnectUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Google Analytics OAuth connect URL
    ApiResponse<GetGoogleAnalyticsConnectUrl200Response> response = apiInstance.GetGoogleAnalyticsConnectUrlWithHttpInfo(profileId, redirectUrl, reconnectAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetGoogleAnalyticsConnectUrlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** | Your Zernio profile ID (get from /v1/profiles). |  |
| **redirectUrl** | **string?** | Custom redirect after connection. Must be an absolute http(s) URL or custom app scheme such as &#x60;myapp://callback&#x60;; relative and unsafe URLs return 400. | [optional]  |
| **reconnectAccountId** | **string?** | Zernio account ID of the Google Analytics account being reconnected. Picking a different property then fails instead of adding a second account. | [optional]  |

### Return type

[**GetGoogleAnalyticsConnectUrl200Response**](GetGoogleAnalyticsConnectUrl200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OAuth authorization URL and authenticated state |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | API key does not have access to this profile, or the key is read-only. |  -  |
| **404** | Profile not found or access denied. |  -  |
| **503** | Google Analytics OAuth is not configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gethubspotconnecturl"></a>
# **GetHubSpotConnectUrl**
> GetHubSpotConnectUrl200Response GetHubSpotConnectUrl (string profileId, string? redirectUrl = null)

Get HubSpot OAuth connect URL

Initiates OAuth for a HubSpot portal. HubSpot is a connect-only CRM platform: the connected account does not post, read analytics or run ads.  One HubSpot portal can be connected per profile. Connecting a different portal to a profile that already has one redirects with `error=hubspot_profile_has_portal`.  ### Flow  1. Redirect the user to `authUrl`. 2. After authorization, HubSpot returns the browser to Zernio's internal callback. 3. Zernio redirects to `redirect_url` (or the dashboard when omitted).  On success the redirect carries `connected=hubspot`, `profileId`, `accountId` and `username` (the portal domain). On failure it carries `error`, `platform=hubspot` and `error_message`.  Reconnecting the same portal and profile updates the stored connection in place and keeps its settings.  Requested scopes: `oauth`, `crm.objects.contacts.read`, `crm.objects.contacts.write`. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetHubSpotConnectUrlExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string | Your Zernio profile ID (get from /v1/profiles).
            var redirectUrl = "redirectUrl_example";  // string? | Custom redirect after connection. Must be an absolute http(s) URL or custom app scheme such as `myapp://callback`; relative and unsafe URLs return 400. (optional) 

            try
            {
                // Get HubSpot OAuth connect URL
                GetHubSpotConnectUrl200Response result = apiInstance.GetHubSpotConnectUrl(profileId, redirectUrl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetHubSpotConnectUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetHubSpotConnectUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get HubSpot OAuth connect URL
    ApiResponse<GetHubSpotConnectUrl200Response> response = apiInstance.GetHubSpotConnectUrlWithHttpInfo(profileId, redirectUrl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetHubSpotConnectUrlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** | Your Zernio profile ID (get from /v1/profiles). |  |
| **redirectUrl** | **string?** | Custom redirect after connection. Must be an absolute http(s) URL or custom app scheme such as &#x60;myapp://callback&#x60;; relative and unsafe URLs return 400. | [optional]  |

### Return type

[**GetHubSpotConnectUrl200Response**](GetHubSpotConnectUrl200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OAuth authorization URL and authenticated state |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | API key does not have access to this profile, or the key is read-only. |  -  |
| **404** | Profile not found or access denied. |  -  |
| **503** | HubSpot OAuth is not configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getlinkedinorganizations"></a>
# **GetLinkedInOrganizations**
> GetLinkedInOrganizations200Response GetLinkedInOrganizations (string accountId)

List LinkedIn orgs

Returns LinkedIn organizations (company pages) the connected account has admin access to.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetLinkedInOrganizationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // List LinkedIn orgs
                GetLinkedInOrganizations200Response result = apiInstance.GetLinkedInOrganizations(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetLinkedInOrganizations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetLinkedInOrganizationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List LinkedIn orgs
    ApiResponse<GetLinkedInOrganizations200Response> response = apiInstance.GetLinkedInOrganizationsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetLinkedInOrganizationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetLinkedInOrganizations200Response**](GetLinkedInOrganizations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Organizations list |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getoauthapp"></a>
# **GetOAuthApp**
> CreateOAuthApp201Response GetOAuthApp (string appId)

Get an OAuth app

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetOAuthAppExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var appId = "appId_example";  // string | 

            try
            {
                // Get an OAuth app
                CreateOAuthApp201Response result = apiInstance.GetOAuthApp(appId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetOAuthApp: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetOAuthAppWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an OAuth app
    ApiResponse<CreateOAuthApp201Response> response = apiInstance.GetOAuthAppWithHttpInfo(appId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetOAuthAppWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appId** | **string** |  |  |

### Return type

[**CreateOAuthApp201Response**](CreateOAuthApp201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The app. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getpagewebhooksubscription"></a>
# **GetPageWebhookSubscription**
> GetPageWebhookSubscription200Response GetPageWebhookSubscription (string accountId)

Read a Facebook Page's webhook subscription

Returns the webhook fields Zernio's app is subscribed to on the connected Page, read live from Meta. Use it to confirm `leadgen` is present: a Page missing it keeps delivering every other event while lead ads stop arriving, with nothing to indicate it. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetPageWebhookSubscriptionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Read a Facebook Page's webhook subscription
                GetPageWebhookSubscription200Response result = apiInstance.GetPageWebhookSubscription(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetPageWebhookSubscription: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPageWebhookSubscriptionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read a Facebook Page's webhook subscription
    ApiResponse<GetPageWebhookSubscription200Response> response = apiInstance.GetPageWebhookSubscriptionWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetPageWebhookSubscriptionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetPageWebhookSubscription200Response**](GetPageWebhookSubscription200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The Page&#39;s current subscription |  -  |
| **400** | Invalid request |  -  |
| **404** | Resource not found |  -  |
| **409** | The connection has no selected Page |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getpendingoauthdata"></a>
# **GetPendingOAuthData**
> GetPendingOAuthData200Response GetPendingOAuthData (string token)

Get pending OAuth data

Fetch pending OAuth data for headless mode using the pendingDataToken from the redirect URL. No authentication required.  ### Scope  This endpoint is used where the selection list is too large to fit in URL params:  - LinkedIn organizations - Google Business Profile locations - Slack channels - Snapchat profiles - Pinterest boards  The redirect carries a `pendingDataToken` instead of the full payload. The response includes the corresponding selection array (e.g. `boards` for Pinterest).  WhatsApp, Facebook and other platforms pass selection state directly via URL query params on the redirect (`profileId`, `tempToken`, `step`), and no pending record is created. So this endpoint will return 404 for those flows. Use the platform-specific selection endpoint instead (e.g. `/v1/connect/whatsapp/select-phone-number`).  ### Token lifetime  Reading the token does not consume it, so this fetch is repeatable until the token expires 1 hour after issuance.  Completing the platform selection deletes the pending record, so the token stops working from then on. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetPendingOAuthDataExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var token = "token_example";  // string | The pending data token from the OAuth redirect URL (pendingDataToken parameter)

            try
            {
                // Get pending OAuth data
                GetPendingOAuthData200Response result = apiInstance.GetPendingOAuthData(token);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetPendingOAuthData: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPendingOAuthDataWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get pending OAuth data
    ApiResponse<GetPendingOAuthData200Response> response = apiInstance.GetPendingOAuthDataWithHttpInfo(token);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetPendingOAuthDataWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | The pending data token from the OAuth redirect URL (pendingDataToken parameter) |  |

### Return type

[**GetPendingOAuthData200Response**](GetPendingOAuthData200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OAuth data fetched successfully |  -  |
| **400** | Missing token parameter |  -  |
| **404** | Token not found or expired |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getpinterestboards"></a>
# **GetPinterestBoards**
> GetPinterestBoards200Response GetPinterestBoards (string accountId)

List Pinterest boards

Returns the boards available for a connected Pinterest account. Use this to get a board ID when creating a Pinterest post.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetPinterestBoardsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // List Pinterest boards
                GetPinterestBoards200Response result = apiInstance.GetPinterestBoards(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetPinterestBoards: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPinterestBoardsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Pinterest boards
    ApiResponse<GetPinterestBoards200Response> response = apiInstance.GetPinterestBoardsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetPinterestBoardsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetPinterestBoards200Response**](GetPinterestBoards200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Boards list |  -  |
| **400** | Not a Pinterest account |  -  |
| **401** | Missing or invalid API key (missing_credentials / invalid_credentials), or the stored Pinterest token was revoked or expired (reconnect_required): reconnect the account. |  -  |
| **404** | Account not found |  -  |
| **409** | The account has no stored access token (ads_connection_required). Reconnect it. |  -  |
| **502** | Pinterest rejected or failed the request. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getredditflairs"></a>
# **GetRedditFlairs**
> GetRedditFlairs200Response GetRedditFlairs (string accountId, string subreddit)

List subreddit flairs

Temporarily unavailable: Reddit has blocked third-party apps from its API, so this endpoint returns 503 `PLATFORM_DISABLED` until Reddit restores access. Reddit Ads is not affected.  Returns available post flairs for a subreddit. Some subreddits require a flair when posting. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetRedditFlairsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var subreddit = "subreddit_example";  // string | Subreddit name (without \"r/\" prefix) to fetch flairs for

            try
            {
                // List subreddit flairs
                GetRedditFlairs200Response result = apiInstance.GetRedditFlairs(accountId, subreddit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetRedditFlairs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetRedditFlairsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List subreddit flairs
    ApiResponse<GetRedditFlairs200Response> response = apiInstance.GetRedditFlairsWithHttpInfo(accountId, subreddit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetRedditFlairsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **subreddit** | **string** | Subreddit name (without \&quot;r/\&quot; prefix) to fetch flairs for |  |

### Return type

[**GetRedditFlairs200Response**](GetRedditFlairs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Flairs list |  -  |
| **400** | Not a Reddit account or missing subreddit parameter |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found |  -  |
| **503** | Organic Reddit is temporarily unavailable while Reddit blocks third-party API access (&#x60;PLATFORM_DISABLED&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getredditsubreddits"></a>
# **GetRedditSubreddits**
> GetRedditSubreddits200Response GetRedditSubreddits (string accountId)

List Reddit subreddits

Temporarily unavailable: Reddit has blocked third-party apps from its API, so this endpoint returns 503 `PLATFORM_DISABLED` until Reddit restores access. Reddit Ads is not affected.  Returns the subreddits the connected Reddit account can post to. Use this to get a subreddit name when creating a Reddit post. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetRedditSubredditsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // List Reddit subreddits
                GetRedditSubreddits200Response result = apiInstance.GetRedditSubreddits(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetRedditSubreddits: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetRedditSubredditsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Reddit subreddits
    ApiResponse<GetRedditSubreddits200Response> response = apiInstance.GetRedditSubredditsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetRedditSubredditsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetRedditSubreddits200Response**](GetRedditSubreddits200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Subreddits list |  -  |
| **400** | Not a Reddit account |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found |  -  |
| **503** | Organic Reddit is temporarily unavailable while Reddit blocks third-party API access (&#x60;PLATFORM_DISABLED&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getshopifyconnecturl"></a>
# **GetShopifyConnectUrl**
> GetShopifyConnectUrl200Response GetShopifyConnectUrl (string profileId, string shop, string? redirectUrl = null)

Get Shopify OAuth connect URL

Initiate the Shopify OAuth flow for a store. Returns an `authUrl` to redirect the merchant to.  Shopify is a connect-only platform: the connected account does not publish social posts. It powers the Blogs API (`/v1/accounts/{accountId}/blogs`) and the Products API (`/v1/accounts/{accountId}/products`).  ### Flow  1. Redirect the merchant to `authUrl`. 2. After they approve the install, Shopify redirects their browser to Zernio's callback, and the account is created on the profile (platform `shopify`). 3. The browser is redirected to `redirect_url` with `connected`, `profileId`, `accountId` and `username` (the store's myshopify.com domain) added, or to the Zernio dashboard when omitted.  The account is the store the merchant approved, which can differ from `shop`, so bind on `accountId`.  ### Scopes  Requested scopes are `read_content`, `write_content`, `read_products` and `write_products` (content and products only; no customer or order data).  Connecting the same profile to a store again refreshes the stored token in place. This is how a store connected under the older content-only grant picks up product access. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetShopifyConnectUrlExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string | Your Zernio profile ID (get from /v1/profiles).
            var shop = "shop_example";  // string | The myshopify.com store domain to connect, e.g. `your-store.myshopify.com` (the bare `your-store` prefix is accepted too).
            var redirectUrl = "redirectUrl_example";  // string? | Your custom redirect URL after connection completes. MUST be an absolute http(s) URL or a custom app scheme for mobile deeplinks (e.g. myapp://callback); a relative path is rejected with 400 INVALID_REDIRECT_URL. On failure an `error` query param is appended. (optional) 

            try
            {
                // Get Shopify OAuth connect URL
                GetShopifyConnectUrl200Response result = apiInstance.GetShopifyConnectUrl(profileId, shop, redirectUrl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetShopifyConnectUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetShopifyConnectUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Shopify OAuth connect URL
    ApiResponse<GetShopifyConnectUrl200Response> response = apiInstance.GetShopifyConnectUrlWithHttpInfo(profileId, shop, redirectUrl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetShopifyConnectUrlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** | Your Zernio profile ID (get from /v1/profiles). |  |
| **shop** | **string** | The myshopify.com store domain to connect, e.g. &#x60;your-store.myshopify.com&#x60; (the bare &#x60;your-store&#x60; prefix is accepted too). |  |
| **redirectUrl** | **string?** | Your custom redirect URL after connection completes. MUST be an absolute http(s) URL or a custom app scheme for mobile deeplinks (e.g. myapp://callback); a relative path is rejected with 400 INVALID_REDIRECT_URL. On failure an &#x60;error&#x60; query param is appended. | [optional]  |

### Return type

[**GetShopifyConnectUrl200Response**](GetShopifyConnectUrl200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OAuth authorization URL to redirect the merchant to |  -  |
| **400** | Invalid &#x60;profileId&#x60; format, &#x60;shop&#x60; is not a myshopify.com store domain, or &#x60;redirect_url&#x60; is not an absolute http(s) URL or custom app scheme. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | API key does not have access to this profile. |  -  |
| **404** | Profile not found or access denied. |  -  |
| **500** | Shopify API not configured (missing credentials). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getsubredditrules"></a>
# **GetSubredditRules**
> GetSubredditRules200Response GetSubredditRules (string accountId, string subreddit)

Get subreddit rules

Temporarily unavailable: Reddit has blocked third-party apps from its API, so this endpoint returns 503 `PLATFORM_DISABLED` until Reddit restores access. Reddit Ads is not affected.  Returns a subreddit's posting rules plus Reddit's site-wide rules, so you can check them before submitting and avoid a removal.  Use this alongside `GET /v1/tools/validate/subreddit`, which only confirms that a subreddit exists and reports its basic posting settings. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetSubredditRulesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The ID of the Reddit account
            var subreddit = webdev;  // string | Subreddit name (without the \"r/\" prefix)

            try
            {
                // Get subreddit rules
                GetSubredditRules200Response result = apiInstance.GetSubredditRules(accountId, subreddit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetSubredditRules: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSubredditRulesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get subreddit rules
    ApiResponse<GetSubredditRules200Response> response = apiInstance.GetSubredditRulesWithHttpInfo(accountId, subreddit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetSubredditRulesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The ID of the Reddit account |  |
| **subreddit** | **string** | Subreddit name (without the \&quot;r/\&quot; prefix) |  |

### Return type

[**GetSubredditRules200Response**](GetSubredditRules200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Subreddit and site rules |  -  |
| **400** | Not a Reddit account |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account or subreddit not found |  -  |
| **502** | Reddit was unreachable or returned an unclassified error. Reddit 4xx statuses are forwarded as-is. |  -  |
| **503** | Organic Reddit is temporarily unavailable while Reddit blocks third-party API access (&#x60;PLATFORM_DISABLED&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettelegramconnectstatus"></a>
# **GetTelegramConnectStatus**
> GetTelegramConnectStatus200Response GetTelegramConnectStatus (string profileId)

Generate Telegram code

Generate an access code (valid 15 minutes) for connecting a Telegram channel or group. Add the bot as admin, then send the code + @yourchannel to the bot. Poll PATCH /v1/connect/telegram to check status.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetTelegramConnectStatusExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string | The profile ID to connect the Telegram account to

            try
            {
                // Generate Telegram code
                GetTelegramConnectStatus200Response result = apiInstance.GetTelegramConnectStatus(profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetTelegramConnectStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTelegramConnectStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generate Telegram code
    ApiResponse<GetTelegramConnectStatus200Response> response = apiInstance.GetTelegramConnectStatusWithHttpInfo(profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetTelegramConnectStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** | The profile ID to connect the Telegram account to |  |

### Return type

[**GetTelegramConnectStatus200Response**](GetTelegramConnectStatus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Access code generated |  -  |
| **400** | Profile ID required or invalid format |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | No access to this profile |  -  |
| **404** | Profile not found |  -  |
| **500** | Internal error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getwebflowconnecturl"></a>
# **GetWebflowConnectUrl**
> GetWebflowConnectUrl200Response GetWebflowConnectUrl (string profileId, string? redirectUrl = null)

Get Webflow OAuth URL

Returns Webflow's consent URL for the Zernio Webflow app.  ### Flow  1. The user picks exactly one site on Webflow's consent screen. 2. Webflow returns the browser to Zernio's internal callback, which connects that site. 3. Zernio redirects to `redirect_url` (or the dashboard when omitted).  Picking several sites connects none and redirects with `error=webflow_pick_one_site`.  ### Notes  - Connecting a site already connected with a site token upgrades the same account. - Only an OAuth connection can install tracking tags on the site (`installTrackingTagOnStore`); blogs work with either. - The token does not expire. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetWebflowConnectUrlExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string | Your Zernio profile ID (get from /v1/profiles).
            var redirectUrl = "redirectUrl_example";  // string? | Custom redirect after connection. Must be an absolute http(s) URL or custom app scheme such as `myapp://callback`; relative and unsafe URLs return 400. (optional) 

            try
            {
                // Get Webflow OAuth URL
                GetWebflowConnectUrl200Response result = apiInstance.GetWebflowConnectUrl(profileId, redirectUrl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetWebflowConnectUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWebflowConnectUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Webflow OAuth URL
    ApiResponse<GetWebflowConnectUrl200Response> response = apiInstance.GetWebflowConnectUrlWithHttpInfo(profileId, redirectUrl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetWebflowConnectUrlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** | Your Zernio profile ID (get from /v1/profiles). |  |
| **redirectUrl** | **string?** | Custom redirect after connection. Must be an absolute http(s) URL or custom app scheme such as &#x60;myapp://callback&#x60;; relative and unsafe URLs return 400. | [optional]  |

### Return type

[**GetWebflowConnectUrl200Response**](GetWebflowConnectUrl200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webflow consent URL and authenticated state |  -  |
| **400** | Invalid &#x60;profileId&#x60; or &#x60;redirect_url&#x60;. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | API key does not have access to this profile. |  -  |
| **404** | Profile not found or access denied. |  -  |
| **503** | The Webflow app or state signing is not configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getwhatsappsdkconfig"></a>
# **GetWhatsAppSdkConfig**
> GetWhatsAppSdkConfig200Response GetWhatsAppSdkConfig (string? xConnectToken = null)

Get Embedded Signup SDK config

Returns the Meta app id and Embedded Signup configuration id the Zernio-hosted signup page uses to open Meta's popup.  Integrators do not need this endpoint: start the hosted flow with `GET /v1/connect/whatsapp?signup=hosted` and send the user to the returned `authUrl`.  Authenticates with an API key or with the connect token the hosted flow issues (`X-Connect-Token` header). 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetWhatsAppSdkConfigExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var xConnectToken = "xConnectToken_example";  // string? | Connect token issued by the hosted signup flow, accepted instead of an API key. (optional) 

            try
            {
                // Get Embedded Signup SDK config
                GetWhatsAppSdkConfig200Response result = apiInstance.GetWhatsAppSdkConfig(xConnectToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetWhatsAppSdkConfig: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWhatsAppSdkConfigWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Embedded Signup SDK config
    ApiResponse<GetWhatsAppSdkConfig200Response> response = apiInstance.GetWhatsAppSdkConfigWithHttpInfo(xConnectToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetWhatsAppSdkConfigWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xConnectToken** | **string?** | Connect token issued by the hosted signup flow, accepted instead of an API key. | [optional]  |

### Return type

[**GetWhatsAppSdkConfig200Response**](GetWhatsAppSdkConfig200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Meta app configuration for Embedded Signup |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getwixconnecturl"></a>
# **GetWixConnectUrl**
> GetWixConnectUrl200Response GetWixConnectUrl (string profileId, string? redirectUrl = null)

Get Wix site install URL

Returns the Wix installer link for the Zernio app.  ### Flow  1. The user picks one of their Wix sites there and approves the app. 2. Wix returns the browser to Zernio's internal callback, which connects that site. 3. The callback redirects to `redirect_url` (or the dashboard when omitted).  ### What the account supports  Wix is a connect-only blog platform. The connected account powers the Blogs API (`/v1/accounts/{accountId}/blogs`) and does not support social posts, inbox, analytics or ads. The site needs the Wix Blog app.  Access tokens renew by themselves. Removing the Zernio app from the site in Wix disconnects the account. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetWixConnectUrlExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string | Your Zernio profile ID (get from /v1/profiles).
            var redirectUrl = "redirectUrl_example";  // string? | Custom redirect after connection. Must be an absolute http(s) URL or custom app scheme such as `myapp://callback`; relative and unsafe URLs return 400. (optional) 

            try
            {
                // Get Wix site install URL
                GetWixConnectUrl200Response result = apiInstance.GetWixConnectUrl(profileId, redirectUrl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetWixConnectUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWixConnectUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Wix site install URL
    ApiResponse<GetWixConnectUrl200Response> response = apiInstance.GetWixConnectUrlWithHttpInfo(profileId, redirectUrl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetWixConnectUrlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** | Your Zernio profile ID (get from /v1/profiles). |  |
| **redirectUrl** | **string?** | Custom redirect after connection. Must be an absolute http(s) URL or custom app scheme such as &#x60;myapp://callback&#x60;; relative and unsafe URLs return 400. | [optional]  |

### Return type

[**GetWixConnectUrl200Response**](GetWixConnectUrl200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Wix installer URL and authenticated state |  -  |
| **400** | Invalid &#x60;profileId&#x60; or &#x60;redirect_url&#x60;. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | API key does not have access to this profile. |  -  |
| **404** | Profile not found or access denied. |  -  |
| **503** | The Wix app or state signing is not configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getwordpressauthurl"></a>
# **GetWordPressAuthUrl**
> GetWordPressAuthUrl200Response GetWordPressAuthUrl (string profileId, string? redirectUrl = null)

Get WordPress.com OAuth connect URL

Initiates OAuth for a WordPress.com site or a Jetpack-connected site.  WordPress is a connect-only blog platform: the connected account powers the Blogs API (`/v1/accounts/{accountId}/blogs`). It does not support social posts, inbox, analytics, ads, or Shopify product operations.  ### Flow  1. Redirect the user to `authUrl`. 2. After authorization, WordPress returns the browser to Zernio's internal callback. 3. Zernio redirects to `redirect_url` (or the dashboard when omitted).  Reconnecting the same site and profile updates the stored connection in place.  ### Scopes  The consent request omits `scope` to use WordPress.com's default single-site grant. Granular scopes cannot access the `/wp/v2` article API.  Zernio checks that API before saving the connection and does not request explicit `global` authorization across all sites. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetWordPressAuthUrlExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string | Your Zernio profile ID (get from /v1/profiles).
            var redirectUrl = "redirectUrl_example";  // string? | Custom redirect after connection. Must be an absolute http(s) URL or custom app scheme such as `myapp://callback`; relative and unsafe URLs return 400. (optional) 

            try
            {
                // Get WordPress.com OAuth connect URL
                GetWordPressAuthUrl200Response result = apiInstance.GetWordPressAuthUrl(profileId, redirectUrl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetWordPressAuthUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWordPressAuthUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get WordPress.com OAuth connect URL
    ApiResponse<GetWordPressAuthUrl200Response> response = apiInstance.GetWordPressAuthUrlWithHttpInfo(profileId, redirectUrl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetWordPressAuthUrlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** | Your Zernio profile ID (get from /v1/profiles). |  |
| **redirectUrl** | **string?** | Custom redirect after connection. Must be an absolute http(s) URL or custom app scheme such as &#x60;myapp://callback&#x60;; relative and unsafe URLs return 400. | [optional]  |

### Return type

[**GetWordPressAuthUrl200Response**](GetWordPressAuthUrl200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OAuth authorization URL and authenticated state |  -  |
| **400** | Invalid &#x60;profileId&#x60; or &#x60;redirect_url&#x60;. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | API key does not have access to this profile. |  -  |
| **404** | Profile not found or access denied. |  -  |
| **503** | WordPress.com OAuth or state signing is not configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getyoutubecaptions"></a>
# **GetYoutubeCaptions**
> GetYoutubeCaptions200Response GetYoutubeCaptions (string accountId, string videoId, string? language = null, string? format = null, bool? refresh = null)

Get a YouTube video transcript

Returns the caption track YouTube already holds for one of the connected channel's own videos, as plain text plus timed cues. Use it instead of downloading and transcribing the video yourself.  Auto-generated (ASR) tracks are included: YouTube serves them to the channel owner, which is what the connected account is. Uploaded tracks win over auto-generated ones when both exist for a language.  ### Caching  We store the transcript on first read and serve it from there afterwards, so you do not need to cache it yourself. A cached read costs no YouTube quota and does not call YouTube at all.  - `source` tells you which happened: `youtube` on the first read, `cache` after. - Pass `refresh=true` only when the captions actually changed on YouTube, since that re-downloads.  ### Notes  - Only videos owned by this connected channel. Anything else returns 404. - `contentDetails.caption` in YouTube's own API reads `false` on videos that DO have a serving auto-generated track, so it is not a usable availability signal. Call this endpoint and handle the 404. - YouTube generates auto-captions only for videos with recognisable speech, and can take a few hours after upload to publish them. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetYoutubeCaptionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected YouTube account.
            var videoId = "videoId_example";  // string | The YouTube video id (the `platformPostId` on a synced external post).
            var language = "language_example";  // string? | BCP-47 language tag as YouTube labels the track. `en` also matches an `en-GB` track. Omit to take the best available track. (optional) 
            var format = "json";  // string? | `json` returns timed `cues`; `srt` returns the raw SubRip body instead. `text` is present either way. (optional)  (default to json)
            var refresh = false;  // bool? | Re-download from YouTube instead of serving the stored copy. Spends 200 quota units. (optional)  (default to false)

            try
            {
                // Get a YouTube video transcript
                GetYoutubeCaptions200Response result = apiInstance.GetYoutubeCaptions(accountId, videoId, language, format, refresh);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetYoutubeCaptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetYoutubeCaptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a YouTube video transcript
    ApiResponse<GetYoutubeCaptions200Response> response = apiInstance.GetYoutubeCaptionsWithHttpInfo(accountId, videoId, language, format, refresh);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetYoutubeCaptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected YouTube account. |  |
| **videoId** | **string** | The YouTube video id (the &#x60;platformPostId&#x60; on a synced external post). |  |
| **language** | **string?** | BCP-47 language tag as YouTube labels the track. &#x60;en&#x60; also matches an &#x60;en-GB&#x60; track. Omit to take the best available track. | [optional]  |
| **format** | **string?** | &#x60;json&#x60; returns timed &#x60;cues&#x60;; &#x60;srt&#x60; returns the raw SubRip body instead. &#x60;text&#x60; is present either way. | [optional] [default to json] |
| **refresh** | **bool?** | Re-download from YouTube instead of serving the stored copy. Spends 200 quota units. | [optional] [default to false] |

### Return type

[**GetYoutubeCaptions200Response**](GetYoutubeCaptions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The transcript. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found, the video does not belong to this channel (&#x60;video_not_found&#x60;), or the video has no caption track in the requested language (&#x60;captions_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getyoutubeplaylists"></a>
# **GetYoutubePlaylists**
> GetYoutubePlaylists200Response GetYoutubePlaylists (string accountId)

List YouTube playlists

Returns the playlists available for a connected YouTube account. Use this to get a playlist ID when creating a YouTube post with the playlistId field.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetYoutubePlaylistsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // List YouTube playlists
                GetYoutubePlaylists200Response result = apiInstance.GetYoutubePlaylists(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.GetYoutubePlaylists: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetYoutubePlaylistsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List YouTube playlists
    ApiResponse<GetYoutubePlaylists200Response> response = apiInstance.GetYoutubePlaylistsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.GetYoutubePlaylistsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**GetYoutubePlaylists200Response**](GetYoutubePlaylists200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Playlists list |  -  |
| **400** | Not a YouTube account |  -  |
| **401** | Missing or invalid API key (missing_credentials / invalid_credentials), or the stored YouTube token was revoked or expired (reconnect_required): reconnect the account. |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="handleoauthcallback"></a>
# **HandleOAuthCallback**
> void HandleOAuthCallback (string platform, HandleOAuthCallbackRequest handleOAuthCallbackRequest)

Complete OAuth callback

Exchange the OAuth authorization code for tokens and connect the account to the specified profile.  Facebook, Google Business Profile, Snapchat and WhatsApp are not accepted here: their account identity is a destination chosen after OAuth, which this single-shot exchange cannot do. Connect them through the redirect flow from `GET /v1/connect/{platform}`, or, for WhatsApp Embedded Signup, through `POST /v1/connect/whatsapp/embedded-signup`. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class HandleOAuthCallbackExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var platform = "instagram";  // string | Social platform to complete the connect for. Discord, Slack and Telegram are absent because they are served by their own dedicated routes, documented separately. 
            var handleOAuthCallbackRequest = new HandleOAuthCallbackRequest(); // HandleOAuthCallbackRequest | 

            try
            {
                // Complete OAuth callback
                apiInstance.HandleOAuthCallback(platform, handleOAuthCallbackRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.HandleOAuthCallback: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the HandleOAuthCallbackWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Complete OAuth callback
    apiInstance.HandleOAuthCallbackWithHttpInfo(platform, handleOAuthCallbackRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.HandleOAuthCallbackWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **platform** | **string** | Social platform to complete the connect for. Discord, Slack and Telegram are absent because they are served by their own dedicated routes, documented separately.  |  |
| **handleOAuthCallbackRequest** | [**HandleOAuthCallbackRequest**](HandleOAuthCallbackRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account connected |  -  |
| **400** | Invalid params, the platform requires choosing a destination (code: platform_requires_destination), or an X state without the verifier or with an invalid or expired signature (code: invalid_field_value, param: state) |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | No access to the profile, or BYOK required for AppSumo X |  -  |
| **404** | Profile not found |  -  |
| **500** | Internal error while connecting the account |  -  |
| **502** | The platform rejected the token exchange (type: platform_error; an upstream 4xx status is forwarded instead of 502) |  -  |
| **503** | Connections for this platform are temporarily disabled (code: platform_disabled) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="initiatetelegramconnect"></a>
# **InitiateTelegramConnect**
> InitiateTelegramConnect200Response InitiateTelegramConnect (InitiateTelegramConnectRequest initiateTelegramConnectRequest)

Connect Telegram directly

Connect a Telegram channel/group directly using the chat ID. Alternative to the access code flow. The bot must already be an admin in the channel/group.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class InitiateTelegramConnectExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var initiateTelegramConnectRequest = new InitiateTelegramConnectRequest(); // InitiateTelegramConnectRequest | 

            try
            {
                // Connect Telegram directly
                InitiateTelegramConnect200Response result = apiInstance.InitiateTelegramConnect(initiateTelegramConnectRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.InitiateTelegramConnect: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the InitiateTelegramConnectWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Connect Telegram directly
    ApiResponse<InitiateTelegramConnect200Response> response = apiInstance.InitiateTelegramConnectWithHttpInfo(initiateTelegramConnectRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.InitiateTelegramConnectWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **initiateTelegramConnectRequest** | [**InitiateTelegramConnectRequest**](InitiateTelegramConnectRequest.md) |  |  |

### Return type

[**InitiateTelegramConnect200Response**](InitiateTelegramConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Telegram channel connected successfully |  -  |
| **400** | Chat ID required, bot not admin, or cannot access chat |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | No access to this profile |  -  |
| **404** | Profile not found |  -  |
| **500** | Internal error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listfacebookpages"></a>
# **ListFacebookPages**
> ListFacebookPages200Response ListFacebookPages (string? profileId = null, string? tempToken = null, string? xTempToken = null, string? connectFlow = null, string? selectionToken = null)

List Facebook pages

Lists the Facebook Pages a user can pick from after signing in, so they can choose which Page to connect.  ### Authorization by flow  - Classic connections require profileId and tempToken from the OAuth redirect. - Headless connections use X-Connect-Token. - The dashboard business-login picker instead sends only selectionToken, an encrypted grant valid for ten minutes. This requires the initiating user and current profile access, and returns only Page IDs and names.  X-Connect-Token cannot authorize business selection. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ListFacebookPagesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? | Profile ID from your classic connection flow. Required with tempToken. (optional) 
            var tempToken = "tempToken_example";  // string? | Temporary Facebook access token from the classic OAuth callback. Required with profileId unless sent in the X-Temp-Token header. (optional) 
            var xTempToken = "xTempToken_example";  // string? | The OAuth user token, in place of the tempToken query parameter. Prefer it: a query string is written to request logs along the way. (optional) 
            var connectFlow = "connectFlow_example";  // string? | Set by the Zernio-hosted picker, whose user token stays in an httpOnly cookie. Integrators send tempToken instead. (optional) 
            var selectionToken = ENCRYPTED_SELECTION_TOKEN;  // string? | Encrypted dashboard business-login grant. Send alone instead of profileId and tempToken. Expires after ten minutes. (optional) 

            try
            {
                // List Facebook pages
                ListFacebookPages200Response result = apiInstance.ListFacebookPages(profileId, tempToken, xTempToken, connectFlow, selectionToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ListFacebookPages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListFacebookPagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Facebook pages
    ApiResponse<ListFacebookPages200Response> response = apiInstance.ListFacebookPagesWithHttpInfo(profileId, tempToken, xTempToken, connectFlow, selectionToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ListFacebookPagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** | Profile ID from your classic connection flow. Required with tempToken. | [optional]  |
| **tempToken** | **string?** | Temporary Facebook access token from the classic OAuth callback. Required with profileId unless sent in the X-Temp-Token header. | [optional]  |
| **xTempToken** | **string?** | The OAuth user token, in place of the tempToken query parameter. Prefer it: a query string is written to request logs along the way. | [optional]  |
| **connectFlow** | **string?** | Set by the Zernio-hosted picker, whose user token stays in an httpOnly cookie. Integrators send tempToken instead. | [optional]  |
| **selectionToken** | **string?** | Encrypted dashboard business-login grant. Send alone instead of profileId and tempToken. Expires after ten minutes. | [optional]  |

### Return type

[**ListFacebookPages200Response**](ListFacebookPages200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of Facebook Pages available for connection |  -  |
| **400** | Invalid or expired selectionToken, no granted Pages, or missing classic profileId and tempToken. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The caller is not the initiating user or no longer has profile access. |  -  |
| **429** | Meta is rate limiting Page reads for this Facebook account (code &#x60;rate_limited&#x60;). Retry after &#x60;Retry-After&#x60; seconds; the listing stops at the first throttle instead of retrying. |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |
| **500** | Failed to fetch pages (e.g., invalid token, insufficient permissions) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listgoogleanalyticsproperties"></a>
# **ListGoogleAnalyticsProperties**
> ListGoogleAnalyticsProperties200Response ListGoogleAnalyticsProperties (string pendingDataToken)

List Google Analytics properties for a pending connect

For headless flows: lists the GA4 properties of a pending Google Analytics connect, so you can show your own picker.  ### Flow  1. The connect started with `redirect_url=...?headless=true`, and the Google account can read several GA4 properties. 2. Zernio redirects to your `redirect_url` with `step=select_property`, `profileId`, `platform=googleanalytics` and a `pendingDataToken`. 3. Call this to list the properties and show your own picker. 4. Call `POST /v1/connect/googleanalytics/select-property`.  ### Token  - Listing does not consume the token. - A headless token passes through your own URLs, so it is honored only together with your API key (or connect token) for the same profile. - It expires after one hour. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ListGoogleAnalyticsPropertiesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var pendingDataToken = "pendingDataToken_example";  // string | Token from the headless redirect.

            try
            {
                // List Google Analytics properties for a pending connect
                ListGoogleAnalyticsProperties200Response result = apiInstance.ListGoogleAnalyticsProperties(pendingDataToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ListGoogleAnalyticsProperties: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListGoogleAnalyticsPropertiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Google Analytics properties for a pending connect
    ApiResponse<ListGoogleAnalyticsProperties200Response> response = apiInstance.ListGoogleAnalyticsPropertiesWithHttpInfo(pendingDataToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ListGoogleAnalyticsPropertiesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pendingDataToken** | **string** | Token from the headless redirect. |  |

### Return type

[**ListGoogleAnalyticsProperties200Response**](ListGoogleAnalyticsProperties200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Properties the Google account can read |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The pending sign-in expired or was already used. Start the connect again. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listgooglebusinesslocations"></a>
# **ListGoogleBusinessLocations**
> ListGoogleBusinessLocations200Response ListGoogleBusinessLocations (string? profileId = null, string? pendingDataToken = null, string? tempToken = null, string? search = null, string? filter = null)

List Google Business Profile locations

For headless flows. Returns the list of Google Business Profile locations the user can manage. Use pendingDataToken (from the OAuth callback redirect) to list locations without consuming the token, so it remains available for select-location. Use X-Connect-Token header if connecting via API key. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ListGoogleBusinessLocationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? | Profile ID from your connection flow. Required for auth validation when provided. (optional) 
            var pendingDataToken = "pendingDataToken_example";  // string? | Token from the OAuth callback redirect. Preferred over tempToken because it preserves server-side token storage. One of pendingDataToken or tempToken is required. (optional) 
            var tempToken = "tempToken_example";  // string? | Legacy. Direct Google access token. Use pendingDataToken instead when available. (optional) 
            var search = "search_example";  // string? | Free-text search on the business name, applied server-side by Google. Use this for accounts that own many locations (the response is bounded, see hasMore) so the user can find a specific location without loading the full list.  (optional) 
            var filter = "filter_example";  // string? | Raw Google Business Information API filter expression (advanced; takes precedence over search). Supports fields such as title, storeCode, storefront_address.postal_code, labels and categories, e.g. storeCode=\"LH279411\". See Google's \"Work with location data\" guide.  (optional) 

            try
            {
                // List Google Business Profile locations
                ListGoogleBusinessLocations200Response result = apiInstance.ListGoogleBusinessLocations(profileId, pendingDataToken, tempToken, search, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ListGoogleBusinessLocations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListGoogleBusinessLocationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Google Business Profile locations
    ApiResponse<ListGoogleBusinessLocations200Response> response = apiInstance.ListGoogleBusinessLocationsWithHttpInfo(profileId, pendingDataToken, tempToken, search, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ListGoogleBusinessLocationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** | Profile ID from your connection flow. Required for auth validation when provided. | [optional]  |
| **pendingDataToken** | **string?** | Token from the OAuth callback redirect. Preferred over tempToken because it preserves server-side token storage. One of pendingDataToken or tempToken is required. | [optional]  |
| **tempToken** | **string?** | Legacy. Direct Google access token. Use pendingDataToken instead when available. | [optional]  |
| **search** | **string?** | Free-text search on the business name, applied server-side by Google. Use this for accounts that own many locations (the response is bounded, see hasMore) so the user can find a specific location without loading the full list.  | [optional]  |
| **filter** | **string?** | Raw Google Business Information API filter expression (advanced; takes precedence over search). Supports fields such as title, storeCode, storefront_address.postal_code, labels and categories, e.g. storeCode&#x3D;\&quot;LH279411\&quot;. See Google&#39;s \&quot;Work with location data\&quot; guide.  | [optional]  |

### Return type

[**ListGoogleBusinessLocations200Response**](ListGoogleBusinessLocations200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of Google Business Profile locations available for connection |  -  |
| **400** | Missing required parameters (profileId or tempToken) |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The connect token was issued for a different profile or platform (INSUFFICIENT_PERMISSIONS). |  -  |
| **500** | Failed to fetch locations (e.g., invalid token, insufficient permissions) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listinstagrampages"></a>
# **ListInstagramPages**
> ListInstagramPages200Response ListInstagramPages (string profileId, string? tempToken = null, string? xTempToken = null, string? connectFlow = null)

List Pages with a linked Instagram account

Completes the `loginMethod=facebook_login` Instagram flow, i.e. \"Instagram API with Facebook Login\".  ### Flow  1. The user authorizes on Facebook. 2. Extract `tempToken` from the redirect params (headless mode adds `step=select_account`). 3. Pass it here to list the Facebook Pages they manage.  Only Pages that have a linked Instagram professional account are returned, so an empty array means the user has no eligible Page. Use the X-Connect-Token header if connecting via API key.  Not used by the default `instagram_login` flow, which creates the account without a selection step. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ListInstagramPagesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string | Profile ID from your connection flow
            var tempToken = "tempToken_example";  // string? | Long-lived Facebook user access token from the OAuth callback redirect. Required unless sent in the X-Temp-Token header. (optional) 
            var xTempToken = "xTempToken_example";  // string? | The OAuth user token, in place of the tempToken query parameter. Prefer it: a query string is written to request logs along the way. (optional) 
            var connectFlow = "connectFlow_example";  // string? | Set by the Zernio-hosted picker, whose user token stays in an httpOnly cookie. Integrators send tempToken instead. (optional) 

            try
            {
                // List Pages with a linked Instagram account
                ListInstagramPages200Response result = apiInstance.ListInstagramPages(profileId, tempToken, xTempToken, connectFlow);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ListInstagramPages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListInstagramPagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Pages with a linked Instagram account
    ApiResponse<ListInstagramPages200Response> response = apiInstance.ListInstagramPagesWithHttpInfo(profileId, tempToken, xTempToken, connectFlow);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ListInstagramPagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** | Profile ID from your connection flow |  |
| **tempToken** | **string?** | Long-lived Facebook user access token from the OAuth callback redirect. Required unless sent in the X-Temp-Token header. | [optional]  |
| **xTempToken** | **string?** | The OAuth user token, in place of the tempToken query parameter. Prefer it: a query string is written to request logs along the way. | [optional]  |
| **connectFlow** | **string?** | Set by the Zernio-hosted picker, whose user token stays in an httpOnly cookie. Integrators send tempToken instead. | [optional]  |

### Return type

[**ListInstagramPages200Response**](ListInstagramPages200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Facebook Pages that have a linked Instagram professional account |  -  |
| **400** | Missing required parameters (profileId or tempToken) |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | User does not have access to the specified profile |  -  |
| **429** | Meta is rate limiting Page reads for this Facebook account (code &#x60;rate_limited&#x60;). Retry after &#x60;Retry-After&#x60; seconds; the listing stops at the first throttle instead of retrying. |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listlinkedinorganizations"></a>
# **ListLinkedInOrganizations**
> ListLinkedInOrganizations200Response ListLinkedInOrganizations (string tempToken, string orgIds)

List LinkedIn orgs

Fetch full LinkedIn organization details (logos, vanity names, websites) for custom UI. No authentication required, only the tempToken from OAuth.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ListLinkedInOrganizationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var tempToken = "tempToken_example";  // string | The temporary LinkedIn access token from the OAuth redirect
            var orgIds = 12345678,87654321,11111111;  // string | Comma-separated list of organization IDs to fetch details for (max 100)

            try
            {
                // List LinkedIn orgs
                ListLinkedInOrganizations200Response result = apiInstance.ListLinkedInOrganizations(tempToken, orgIds);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ListLinkedInOrganizations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListLinkedInOrganizationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List LinkedIn orgs
    ApiResponse<ListLinkedInOrganizations200Response> response = apiInstance.ListLinkedInOrganizationsWithHttpInfo(tempToken, orgIds);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ListLinkedInOrganizationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tempToken** | **string** | The temporary LinkedIn access token from the OAuth redirect |  |
| **orgIds** | **string** | Comma-separated list of organization IDs to fetch details for (max 100) |  |

### Return type

[**ListLinkedInOrganizations200Response**](ListLinkedInOrganizations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Organization details fetched successfully |  -  |
| **400** | Missing required parameters or too many organization IDs |  -  |
| **500** | Failed to fetch organization details |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listoauthapps"></a>
# **ListOAuthApps**
> ListOAuthApps200Response ListOAuthApps (int? limit = null, string? cursor = null)

List your OAuth apps

Lists your own OAuth apps on social platforms. Add as many as you need, any number per platform.  A connect runs on one when it passes its id as `oauthAppId`. The consent screen then shows your app's name and logo, and the platform's rate limits and quotas are your app's.  Also lists, in `platforms`, which platforms accept your own app and what to set up on each.  Pages are ordered by id: pass `pagination.nextCursor` back as `cursor` until it is null.  Like every OAuth-app call, it needs the account owner or a full-access team member, on a session or a full-scope API key. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ListOAuthAppsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? | `pagination.nextCursor` from the previous page. (optional) 

            try
            {
                // List your OAuth apps
                ListOAuthApps200Response result = apiInstance.ListOAuthApps(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ListOAuthApps: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListOAuthAppsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List your OAuth apps
    ApiResponse<ListOAuthApps200Response> response = apiInstance.ListOAuthAppsWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ListOAuthAppsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** | &#x60;pagination.nextCursor&#x60; from the previous page. | [optional]  |

### Return type

[**ListOAuthApps200Response**](ListOAuthApps200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Your apps, and the platforms that accept one. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listpinterestboardsforselection"></a>
# **ListPinterestBoardsForSelection**
> ListPinterestBoardsForSelection200Response ListPinterestBoardsForSelection (string xConnectToken, string profileId, string tempToken)

List Pinterest boards

For headless flows. Returns Pinterest boards the user can post to. Use X-Connect-Token from the redirect URL.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ListPinterestBoardsForSelectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var xConnectToken = "xConnectToken_example";  // string | Short-lived connect token from the OAuth redirect
            var profileId = "profileId_example";  // string | Your Zernio profile ID
            var tempToken = "tempToken_example";  // string | Temporary Pinterest access token from the OAuth callback redirect

            try
            {
                // List Pinterest boards
                ListPinterestBoardsForSelection200Response result = apiInstance.ListPinterestBoardsForSelection(xConnectToken, profileId, tempToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ListPinterestBoardsForSelection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListPinterestBoardsForSelectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Pinterest boards
    ApiResponse<ListPinterestBoardsForSelection200Response> response = apiInstance.ListPinterestBoardsForSelectionWithHttpInfo(xConnectToken, profileId, tempToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ListPinterestBoardsForSelectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xConnectToken** | **string** | Short-lived connect token from the OAuth redirect |  |
| **profileId** | **string** | Your Zernio profile ID |  |
| **tempToken** | **string** | Temporary Pinterest access token from the OAuth callback redirect |  |

### Return type

[**ListPinterestBoardsForSelection200Response**](ListPinterestBoardsForSelection200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of Pinterest Boards available for connection |  -  |
| **400** | Missing required parameters |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | No access to profile |  -  |
| **500** | Failed to fetch boards |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listslackchannels"></a>
# **ListSlackChannels**
> ListSlackChannels200Response ListSlackChannels (string profileId, string? pendingDataToken = null, string? accountId = null, string? redirectUrl = null, string? scopes = null)

List Slack channels for the channel picker

Serves the channel picker of the Slack connect flow. Slack's OAuth installs the bot into a workspace, not a channel, so after the redirect the caller lists the workspace's channels here and finalizes one with `POST /v1/connect/slack`.  Served by a dedicated route that shadows `GET /v1/connect/{platform}` for `slack`.  ### Parameters  Send exactly one of:  - `pendingDataToken`: first connect. The nonce from the OAuth redirect, bound to the same `profileId`. - `accountId`: add another channel to a workspace already connected. The existing Slack account's workspace token is reused, no re-OAuth.  With neither, the endpoint behaves like `GET /v1/connect/{platform}` and returns `authUrl` and `state` to start the OAuth flow.  ### Channels  Channels are read live from Slack (`conversations.list`, public and private, archived excluded, up to 2,000).  `isMember` says whether the Zernio bot is already in the channel. A public channel is joined automatically on finalize; a private one must be invited (`/invite @Zernio`) first. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ListSlackChannelsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string | Zernio profile the channel account will belong to. Must match the profile the OAuth flow was started on when `pendingDataToken` is used.
            var pendingDataToken = "pendingDataToken_example";  // string? | Nonce from the OAuth redirect (first connect). (optional) 
            var accountId = "accountId_example";  // string? | Existing active Slack account (yours or a team member's) whose workspace token is reused. (optional) 
            var redirectUrl = "redirectUrl_example";  // string? | Start-OAuth mode only: where to send the user after the connect completes. `redirectUrl` is accepted as an alias. (optional) 
            var scopes = posting;  // string? | Start-OAuth mode only. Comma-separated permission areas to request instead of the full Slack scope set, same semantics as `scopes` on `GET /v1/connect/{platform}`. Omit it to request everything.  - `posting`: installs the bot with the channel scopes it needs to post. - `messaging`: adds the history, DM and reaction scopes the inbox reads. - `analytics`, `comments`, `ads`: add nothing on Slack.  (optional) 

            try
            {
                // List Slack channels for the channel picker
                ListSlackChannels200Response result = apiInstance.ListSlackChannels(profileId, pendingDataToken, accountId, redirectUrl, scopes);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ListSlackChannels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListSlackChannelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Slack channels for the channel picker
    ApiResponse<ListSlackChannels200Response> response = apiInstance.ListSlackChannelsWithHttpInfo(profileId, pendingDataToken, accountId, redirectUrl, scopes);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ListSlackChannelsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** | Zernio profile the channel account will belong to. Must match the profile the OAuth flow was started on when &#x60;pendingDataToken&#x60; is used. |  |
| **pendingDataToken** | **string?** | Nonce from the OAuth redirect (first connect). | [optional]  |
| **accountId** | **string?** | Existing active Slack account (yours or a team member&#39;s) whose workspace token is reused. | [optional]  |
| **redirectUrl** | **string?** | Start-OAuth mode only: where to send the user after the connect completes. &#x60;redirectUrl&#x60; is accepted as an alias. | [optional]  |
| **scopes** | **string?** | Start-OAuth mode only. Comma-separated permission areas to request instead of the full Slack scope set, same semantics as &#x60;scopes&#x60; on &#x60;GET /v1/connect/{platform}&#x60;. Omit it to request everything.  - &#x60;posting&#x60;: installs the bot with the channel scopes it needs to post. - &#x60;messaging&#x60;: adds the history, DM and reaction scopes the inbox reads. - &#x60;analytics&#x60;, &#x60;comments&#x60;, &#x60;ads&#x60;: add nothing on Slack.  | [optional]  |

### Return type

[**ListSlackChannels200Response**](ListSlackChannels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Channel list (picker mode), or the OAuth URL when neither &#x60;pendingDataToken&#x60; nor &#x60;accountId&#x60; is sent |  -  |
| **400** | Invalid profileId or accountId format, or pendingDataToken invalid, expired or issued for another profile (code: invalid_field_value) |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | No access to the profile, or Slack connections are temporarily unavailable (code: feature_not_available) |  -  |
| **404** | Profile not found (start-OAuth mode), or no active Slack account with that accountId for this user or their team (code: account_not_found) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listsnapchatprofiles"></a>
# **ListSnapchatProfiles**
> ListSnapchatProfiles200Response ListSnapchatProfiles (string xConnectToken, string profileId, string tempToken)

List Snapchat profiles

For headless flows. Returns Snapchat Public Profiles the user can post to. Use X-Connect-Token from the redirect URL.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ListSnapchatProfilesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var xConnectToken = "xConnectToken_example";  // string | Short-lived connect token from the OAuth redirect
            var profileId = "profileId_example";  // string | Your Zernio profile ID
            var tempToken = "tempToken_example";  // string | Temporary Snapchat access token from the OAuth callback redirect

            try
            {
                // List Snapchat profiles
                ListSnapchatProfiles200Response result = apiInstance.ListSnapchatProfiles(xConnectToken, profileId, tempToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ListSnapchatProfiles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListSnapchatProfilesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Snapchat profiles
    ApiResponse<ListSnapchatProfiles200Response> response = apiInstance.ListSnapchatProfilesWithHttpInfo(xConnectToken, profileId, tempToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ListSnapchatProfilesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xConnectToken** | **string** | Short-lived connect token from the OAuth redirect |  |
| **profileId** | **string** | Your Zernio profile ID |  |
| **tempToken** | **string** | Temporary Snapchat access token from the OAuth callback redirect |  |

### Return type

[**ListSnapchatProfiles200Response**](ListSnapchatProfiles200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of Snapchat Public Profiles available for connection |  -  |
| **400** | Missing required parameters (profileId or tempToken) |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | No access to profile |  -  |
| **500** | Failed to fetch public profiles |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listwhatsappphonenumbers"></a>
# **ListWhatsAppPhoneNumbers**
> ListWhatsAppPhoneNumbers200Response ListWhatsAppPhoneNumbers (string profileId, string tempToken, string? xConnectToken = null)

List numbers for selection

Fetch the WhatsApp phone numbers available across the user's WhatsApp Business Accounts (WABAs) after a headless OAuth flow.  WhatsApp OAuth grants access at the WABA level. When a connected WABA has 2 or more phone numbers, you must call this endpoint to list them and then `POST /v1/connect/whatsapp/select-phone-number` to bind one to the Zernio profile. Single-phone WABAs auto-complete during the OAuth callback and never reach this endpoint.  Use the `profileId` and `tempToken` returned in the headless redirect (`step=select_phone_number`).  Alternative: if you already know `wabaId` and `phoneNumberId` (e.g. from Meta Business Suite), use `connectWhatsAppCredentials` instead, which skips this two-step flow. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ListWhatsAppPhoneNumbersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string | The Zernio profile ID from the headless redirect
            var tempToken = "tempToken_example";  // string | The temporary access token from the headless redirect
            var xConnectToken = "xConnectToken_example";  // string? | Alternative auth for API users' end customers (used when the bearer token is scoped to a different user) (optional) 

            try
            {
                // List numbers for selection
                ListWhatsAppPhoneNumbers200Response result = apiInstance.ListWhatsAppPhoneNumbers(profileId, tempToken, xConnectToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ListWhatsAppPhoneNumbers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWhatsAppPhoneNumbersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List numbers for selection
    ApiResponse<ListWhatsAppPhoneNumbers200Response> response = apiInstance.ListWhatsAppPhoneNumbersWithHttpInfo(profileId, tempToken, xConnectToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ListWhatsAppPhoneNumbersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** | The Zernio profile ID from the headless redirect |  |
| **tempToken** | **string** | The temporary access token from the headless redirect |  |
| **xConnectToken** | **string?** | Alternative auth for API users&#39; end customers (used when the bearer token is scoped to a different user) | [optional]  |

### Return type

[**ListWhatsAppPhoneNumbers200Response**](ListWhatsAppPhoneNumbers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Phone numbers fetched successfully |  -  |
| **400** | Missing profileId or tempToken |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **500** | Failed to fetch phone numbers (Meta API error, expired token, or insufficient permissions) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="resyncpagewebhooksubscription"></a>
# **ResyncPageWebhookSubscription**
> ResyncPageWebhookSubscription200Response ResyncPageWebhookSubscription (string accountId)

Re-subscribe a Facebook Page to Zernio's webhooks

Re-sends the full field set to Meta and returns the subscription read back afterwards. Meta only honours the field set sent at subscribe time, so a Page connected before a field existed stays without it until this runs. The response reflects what Meta actually granted, not what was requested. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class ResyncPageWebhookSubscriptionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 

            try
            {
                // Re-subscribe a Facebook Page to Zernio's webhooks
                ResyncPageWebhookSubscription200Response result = apiInstance.ResyncPageWebhookSubscription(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.ResyncPageWebhookSubscription: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResyncPageWebhookSubscriptionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Re-subscribe a Facebook Page to Zernio's webhooks
    ApiResponse<ResyncPageWebhookSubscription200Response> response = apiInstance.ResyncPageWebhookSubscriptionWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.ResyncPageWebhookSubscriptionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |

### Return type

[**ResyncPageWebhookSubscription200Response**](ResyncPageWebhookSubscription200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The subscription after re-subscribing |  -  |
| **400** | Invalid request |  -  |
| **404** | Resource not found |  -  |
| **409** | The connection has no selected Page |  -  |
| **502** | Meta rejected the subscription |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="selectfacebookpage"></a>
# **SelectFacebookPage**
> SelectFacebookPage200Response SelectFacebookPage (SelectFacebookPageRequest selectFacebookPageRequest)

Select Facebook page

Connects the Facebook Page the user picked after signing in, completing the Facebook or Meta Ads connection.  ### Two ways to call it  - Classic Facebook Page connection: send profileId, pageId, tempToken and userProfile. Use X-Connect-Token for headless connections. - Dashboard business-login picker: send only selectionToken and pageId to complete a Meta Ads connection.  ### Business selection  The server verifies the initiating user, profile access, current grants and connection eligibility. The profile, platform token, ad-account scope and return URL come only from the encrypted grant.  Business selection requires a session or bearer authentication for the initiating user; X-Connect-Token is not accepted.  It returns redirect_url with connected=metaads on success or an eligibility error redirect. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class SelectFacebookPageExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var selectFacebookPageRequest = new SelectFacebookPageRequest(); // SelectFacebookPageRequest | 

            try
            {
                // Select Facebook page
                SelectFacebookPage200Response result = apiInstance.SelectFacebookPage(selectFacebookPageRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.SelectFacebookPage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SelectFacebookPageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Select Facebook page
    ApiResponse<SelectFacebookPage200Response> response = apiInstance.SelectFacebookPageWithHttpInfo(selectFacebookPageRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.SelectFacebookPageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **selectFacebookPageRequest** | [**SelectFacebookPageRequest**](SelectFacebookPageRequest.md) |  |  |

### Return type

[**SelectFacebookPage200Response**](SelectFacebookPage200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Facebook Page connected or business-login redirect returned. |  -  |
| **400** | Invalid or expired selectionToken, invalid Page choice, forbidden grant overrides, or missing classic connection fields. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | User does not have access to the specified profile |  -  |
| **404** | Selected page not found in available pages |  -  |
| **409** | Reconnect identity mismatch. The OAuth was initiated as a &#x60;force&#x3D;true&#x60; token-recovery re-auth (&#x60;GET /v1/connect/{platform}/ads&#x60;), but the grant landed on a different Facebook user or page than the connected account. The existing account is left untouched.  Returned in the standard error envelope with &#x60;code: reconnect_account_mismatch&#x60; (the same value the OAuth redirect uses in &#x60;error&#x3D;&#x60;). Before 1.79.0 this body was &#x60;{error, code: RECONNECT_ACCOUNT_MISMATCH}&#x60; without &#x60;type&#x60;.  |  -  |
| **422** | pageIds only. None of the Pages could be connected; &#x60;details.failed&#x60; lists each one with its reason. |  -  |
| **429** | Meta is rate limiting Page reads for this Facebook account (code &#x60;rate_limited&#x60;). Retry after &#x60;Retry-After&#x60; seconds; the listing stops at the first throttle instead of retrying. |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |
| **500** | Failed to save Facebook connection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="selectgoogleanalyticsproperty"></a>
# **SelectGoogleAnalyticsProperty**
> SelectGoogleAnalyticsProperty200Response SelectGoogleAnalyticsProperty (SelectGoogleAnalyticsPropertyRequest selectGoogleAnalyticsPropertyRequest)

Connect the chosen Google Analytics property

For headless flows. Connects the property the user picked as a `googleanalytics` account and returns where to send the user next.  - On success: your `redirect_url` with `connected=googleanalytics`, `profileId`, `accountId` and `username`. - When the connect was refused (for example a billing block): an `error`.  Consumes the `pendingDataToken`; a refused or failed attempt leaves it usable for a retry.  Send your API key (or connect token) for the same profile with a headless token. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class SelectGoogleAnalyticsPropertyExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var selectGoogleAnalyticsPropertyRequest = new SelectGoogleAnalyticsPropertyRequest(); // SelectGoogleAnalyticsPropertyRequest | 

            try
            {
                // Connect the chosen Google Analytics property
                SelectGoogleAnalyticsProperty200Response result = apiInstance.SelectGoogleAnalyticsProperty(selectGoogleAnalyticsPropertyRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.SelectGoogleAnalyticsProperty: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SelectGoogleAnalyticsPropertyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Connect the chosen Google Analytics property
    ApiResponse<SelectGoogleAnalyticsProperty200Response> response = apiInstance.SelectGoogleAnalyticsPropertyWithHttpInfo(selectGoogleAnalyticsPropertyRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.SelectGoogleAnalyticsPropertyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **selectGoogleAnalyticsPropertyRequest** | [**SelectGoogleAnalyticsPropertyRequest**](SelectGoogleAnalyticsPropertyRequest.md) |  |  |

### Return type

[**SelectGoogleAnalyticsProperty200Response**](SelectGoogleAnalyticsProperty200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The property is connected, or the connect was refused with a reason in redirect_url |  -  |
| **400** | Invalid request |  -  |
| **404** | The pending sign-in expired or was already used. Start the connect again. |  -  |
| **500** | Google or Zernio failed while saving. The pendingDataToken stays usable; retry. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="selectgooglebusinesslocation"></a>
# **SelectGoogleBusinessLocation**
> SelectGoogleBusinessLocation200Response SelectGoogleBusinessLocation (SelectGoogleBusinessLocationRequest selectGoogleBusinessLocationRequest)

Select Google Business Profile location

Complete the headless Google Business Profile flow by saving the user's selected location. The pendingDataToken is returned in your redirect URL after OAuth completes (step=select_location). Tokens and profile data are stored server-side, so only the pendingDataToken is needed here. Use X-Connect-Token header if connecting via API key. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class SelectGoogleBusinessLocationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var selectGoogleBusinessLocationRequest = new SelectGoogleBusinessLocationRequest(); // SelectGoogleBusinessLocationRequest | 

            try
            {
                // Select Google Business Profile location
                SelectGoogleBusinessLocation200Response result = apiInstance.SelectGoogleBusinessLocation(selectGoogleBusinessLocationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.SelectGoogleBusinessLocation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SelectGoogleBusinessLocationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Select Google Business Profile location
    ApiResponse<SelectGoogleBusinessLocation200Response> response = apiInstance.SelectGoogleBusinessLocationWithHttpInfo(selectGoogleBusinessLocationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.SelectGoogleBusinessLocationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **selectGoogleBusinessLocationRequest** | [**SelectGoogleBusinessLocationRequest**](SelectGoogleBusinessLocationRequest.md) |  |  |

### Return type

[**SelectGoogleBusinessLocation200Response**](SelectGoogleBusinessLocation200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Google Business Profile location connected successfully |  -  |
| **400** | Missing required fields (profileId, locationId, or tempToken), or the provided accountId is not one of the accounts this connection manages |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | User does not have access to the specified profile |  -  |
| **404** | Selected location not found in available locations |  -  |
| **422** | locations only. None of the locations could be connected; &#x60;details.failed&#x60; lists each one with its reason. |  -  |
| **500** | Failed to save Google Business Profile connection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="selectinstagramaccount"></a>
# **SelectInstagramAccount**
> SelectInstagramAccount200Response SelectInstagramAccount (SelectInstagramAccountRequest selectInstagramAccountRequest)

Select the Page whose Instagram account to connect

Saves the selected Page as an Instagram account connected via Facebook Login. The Page access token becomes the account's access token, so every Instagram call for it runs against the Facebook Graph host.  A different Instagram account is added next to any already connected on the profile; picking one already connected refreshes it. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class SelectInstagramAccountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure API key authorization: connectToken
            config.AddApiKey("X-Connect-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-Connect-Token", "Bearer");
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var selectInstagramAccountRequest = new SelectInstagramAccountRequest(); // SelectInstagramAccountRequest | 

            try
            {
                // Select the Page whose Instagram account to connect
                SelectInstagramAccount200Response result = apiInstance.SelectInstagramAccount(selectInstagramAccountRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.SelectInstagramAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SelectInstagramAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Select the Page whose Instagram account to connect
    ApiResponse<SelectInstagramAccount200Response> response = apiInstance.SelectInstagramAccountWithHttpInfo(selectInstagramAccountRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.SelectInstagramAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **selectInstagramAccountRequest** | [**SelectInstagramAccountRequest**](SelectInstagramAccountRequest.md) |  |  |

### Return type

[**SelectInstagramAccount200Response**](SelectInstagramAccount200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Instagram account connected |  -  |
| **400** | Missing required fields, or the selected Page has no linked Instagram professional account |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | User does not have access to the specified profile |  -  |
| **404** | Selected page not found among the pages this token can manage |  -  |
| **409** | The connect was started with &#x60;expectedPlatformUserId&#x60; or &#x60;expectedUsername&#x60; (carried on redirect_url) and the selected Page&#39;s Instagram account is not that account. Nothing is written. Standard error envelope with &#x60;code: account_mismatch&#x60;; with pageIds the mismatching Pages are listed in &#x60;failed&#x60; instead. |  -  |
| **422** | pageIds only. None of the accounts could be connected; &#x60;details.failed&#x60; lists each Page with its reason. |  -  |
| **429** | Meta is rate limiting Page reads for this Facebook account (code &#x60;rate_limited&#x60;). Retry after &#x60;Retry-After&#x60; seconds; the listing stops at the first throttle instead of retrying. |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="selectlinkedinorganization"></a>
# **SelectLinkedInOrganization**
> SelectLinkedInOrganization200Response SelectLinkedInOrganization (SelectLinkedInOrganizationRequest selectLinkedInOrganizationRequest)

Select LinkedIn org

Complete the LinkedIn connection flow. Set accountType to \"personal\" or \"organization\" to connect as a company page. Use X-Connect-Token if connecting via API key.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class SelectLinkedInOrganizationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var selectLinkedInOrganizationRequest = new SelectLinkedInOrganizationRequest(); // SelectLinkedInOrganizationRequest | 

            try
            {
                // Select LinkedIn org
                SelectLinkedInOrganization200Response result = apiInstance.SelectLinkedInOrganization(selectLinkedInOrganizationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.SelectLinkedInOrganization: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SelectLinkedInOrganizationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Select LinkedIn org
    ApiResponse<SelectLinkedInOrganization200Response> response = apiInstance.SelectLinkedInOrganizationWithHttpInfo(selectLinkedInOrganizationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.SelectLinkedInOrganizationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **selectLinkedInOrganizationRequest** | [**SelectLinkedInOrganizationRequest**](SelectLinkedInOrganizationRequest.md) |  |  |

### Return type

[**SelectLinkedInOrganization200Response**](SelectLinkedInOrganization200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | LinkedIn account connected |  -  |
| **400** | Missing required fields |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The connect token was issued for a different profile or platform (INSUFFICIENT_PERMISSIONS). |  -  |
| **409** | The sign-in behind tempToken was already used by an earlier selection or has expired (code oauth_sign_in_consumed); start a new sign-in or send refreshToken |  -  |
| **422** | selections only. None of the accounts could be connected; &#x60;details.failed&#x60; lists each one with its reason. |  -  |
| **500** | Failed to connect LinkedIn account |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="selectpinterestboard"></a>
# **SelectPinterestBoard**
> SelectPinterestBoard200Response SelectPinterestBoard (SelectPinterestBoardRequest selectPinterestBoardRequest)

Select Pinterest board

Complete the Pinterest connection flow. After OAuth, use this endpoint to save the selected board and complete the account connection. Use the X-Connect-Token header if you initiated the connection via API key. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class SelectPinterestBoardExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var selectPinterestBoardRequest = new SelectPinterestBoardRequest(); // SelectPinterestBoardRequest | 

            try
            {
                // Select Pinterest board
                SelectPinterestBoard200Response result = apiInstance.SelectPinterestBoard(selectPinterestBoardRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.SelectPinterestBoard: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SelectPinterestBoardWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Select Pinterest board
    ApiResponse<SelectPinterestBoard200Response> response = apiInstance.SelectPinterestBoardWithHttpInfo(selectPinterestBoardRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.SelectPinterestBoardWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **selectPinterestBoardRequest** | [**SelectPinterestBoardRequest**](SelectPinterestBoardRequest.md) |  |  |

### Return type

[**SelectPinterestBoard200Response**](SelectPinterestBoard200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pinterest Board connected successfully |  -  |
| **400** | Missing required fields |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | No access to profile or profile limit exceeded |  -  |
| **500** | Failed to save Pinterest connection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="selectsnapchatprofile"></a>
# **SelectSnapchatProfile**
> SelectSnapchatProfile200Response SelectSnapchatProfile (SelectSnapchatProfileRequest selectSnapchatProfileRequest, string? xConnectToken = null)

Select Snapchat profile

Complete the Snapchat connection flow by saving the selected Public Profile. Snapchat requires a Public Profile to publish content. Use X-Connect-Token if connecting via API key.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class SelectSnapchatProfileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var selectSnapchatProfileRequest = new SelectSnapchatProfileRequest(); // SelectSnapchatProfileRequest | 
            var xConnectToken = "xConnectToken_example";  // string? | Short-lived connect token from the OAuth redirect (for API users) (optional) 

            try
            {
                // Select Snapchat profile
                SelectSnapchatProfile200Response result = apiInstance.SelectSnapchatProfile(selectSnapchatProfileRequest, xConnectToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.SelectSnapchatProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SelectSnapchatProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Select Snapchat profile
    ApiResponse<SelectSnapchatProfile200Response> response = apiInstance.SelectSnapchatProfileWithHttpInfo(selectSnapchatProfileRequest, xConnectToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.SelectSnapchatProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **selectSnapchatProfileRequest** | [**SelectSnapchatProfileRequest**](SelectSnapchatProfileRequest.md) |  |  |
| **xConnectToken** | **string?** | Short-lived connect token from the OAuth redirect (for API users) | [optional]  |

### Return type

[**SelectSnapchatProfile200Response**](SelectSnapchatProfile200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Snapchat Public Profile connected successfully |  -  |
| **400** | Missing required fields |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | No access to profile or profile limit exceeded |  -  |
| **500** | Failed to connect Snapchat account |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setredditpostflair"></a>
# **SetRedditPostFlair**
> UpdateYoutubeDefaultPlaylist200Response SetRedditPostFlair (string accountId, SetRedditPostFlairRequest setRedditPostFlairRequest)

Set Reddit post flair

Temporarily unavailable: Reddit has blocked third-party apps from its API, so this endpoint returns 503 `PLATFORM_DISABLED` until Reddit restores access. Reddit Ads is not affected.  Applies a flair to a post the connected account already published. Use the GET on this path to list the available `flairTemplateId` values for the subreddit.  Flair can also be set at submit time by passing `flairId` in `platformSpecificData` when creating the post. This endpoint is for changing it afterwards.  The subreddit must allow users to select their own post flair. Setting flair on another user's post requires moderator permissions, which Zernio does not request. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class SetRedditPostFlairExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The ID of the Reddit account that owns the post
            var setRedditPostFlairRequest = new SetRedditPostFlairRequest(); // SetRedditPostFlairRequest | 

            try
            {
                // Set Reddit post flair
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.SetRedditPostFlair(accountId, setRedditPostFlairRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.SetRedditPostFlair: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetRedditPostFlairWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set Reddit post flair
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.SetRedditPostFlairWithHttpInfo(accountId, setRedditPostFlairRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.SetRedditPostFlairWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The ID of the Reddit account that owns the post |  |
| **setRedditPostFlairRequest** | [**SetRedditPostFlairRequest**](SetRedditPostFlairRequest.md) |  |  |

### Return type

[**UpdateYoutubeDefaultPlaylist200Response**](UpdateYoutubeDefaultPlaylist200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Flair applied |  -  |
| **400** | Not a Reddit account, or missing subreddit/postId/flairTemplateId |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found |  -  |
| **502** | Reddit was unreachable or returned an unclassified error. Reddit 4xx statuses (e.g. subreddit does not allow user flair selection) are forwarded as-is. |  -  |
| **503** | Organic Reddit is temporarily unavailable while Reddit blocks third-party API access (&#x60;PLATFORM_DISABLED&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="startmicrosoftadminconsent"></a>
# **StartMicrosoftAdminConsent**
> StartMicrosoftAdminConsent200Response StartMicrosoftAdminConsent (string accountId, string? redirectUrl = null)

Admin-consent link for a Microsoft tenant

Returns the Microsoft Entra admin-consent link for the app, so a tenant administrator can grant mail or calendar access.  Some Microsoft 365 tenants let no user grant mail or calendar access themselves. The API then answers 412 `admin_consent_required` with `details.adminConsentUrl`, a ready admin-consent link.  This endpoint mints a fresh one (each is valid for one hour) and lets you choose `redirectUrl`.  ### Flow  1. A tenant administrator opens the link and approves. 2. They are sent to `redirectUrl` with `adminConsent=granted&tenant=…` (or `adminConsent=denied&error=…`). 3. The grant is recorded on the account, and later requests succeed without a reconnect. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class StartMicrosoftAdminConsentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var redirectUrl = "redirectUrl_example";  // string? | Where to send the administrator afterwards. (optional) 

            try
            {
                // Admin-consent link for a Microsoft tenant
                StartMicrosoftAdminConsent200Response result = apiInstance.StartMicrosoftAdminConsent(accountId, redirectUrl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.StartMicrosoftAdminConsent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the StartMicrosoftAdminConsentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Admin-consent link for a Microsoft tenant
    ApiResponse<StartMicrosoftAdminConsent200Response> response = apiInstance.StartMicrosoftAdminConsentWithHttpInfo(accountId, redirectUrl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.StartMicrosoftAdminConsentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **redirectUrl** | **string?** | Where to send the administrator afterwards. | [optional]  |

### Return type

[**StartMicrosoftAdminConsent200Response**](StartMicrosoftAdminConsent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The link to hand to a tenant administrator |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="testoauthapp"></a>
# **TestOAuthApp**
> CreateOAuthApp201Response TestOAuthApp (string appId)

Check an OAuth app's keys

Checks the saved keys with the platform again and records the outcome in `status` and `lastError`.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class TestOAuthAppExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var appId = "appId_example";  // string | 

            try
            {
                // Check an OAuth app's keys
                CreateOAuthApp201Response result = apiInstance.TestOAuthApp(appId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.TestOAuthApp: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TestOAuthAppWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check an OAuth app's keys
    ApiResponse<CreateOAuthApp201Response> response = apiInstance.TestOAuthAppWithHttpInfo(appId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.TestOAuthAppWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appId** | **string** |  |  |

### Return type

[**CreateOAuthApp201Response**](CreateOAuthApp201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The app with the new check result. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateconnectwelcomescreen"></a>
# **UpdateConnectWelcomeScreen**
> ConnectWelcomeScreen UpdateConnectWelcomeScreen (UpdateConnectWelcomeScreenRequest updateConnectWelcomeScreenRequest)

Save the welcome screen

Replaces the workspace's welcome screen settings: a field left out is cleared. Only the account owner or a full-access team member can save, and not with a profile-scoped API key. Parameters sent on a connect call still win over these values for that call.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class UpdateConnectWelcomeScreenExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var updateConnectWelcomeScreenRequest = new UpdateConnectWelcomeScreenRequest(); // UpdateConnectWelcomeScreenRequest | 

            try
            {
                // Save the welcome screen
                ConnectWelcomeScreen result = apiInstance.UpdateConnectWelcomeScreen(updateConnectWelcomeScreenRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.UpdateConnectWelcomeScreen: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateConnectWelcomeScreenWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Save the welcome screen
    ApiResponse<ConnectWelcomeScreen> response = apiInstance.UpdateConnectWelcomeScreenWithHttpInfo(updateConnectWelcomeScreenRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.UpdateConnectWelcomeScreenWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateConnectWelcomeScreenRequest** | [**UpdateConnectWelcomeScreenRequest**](UpdateConnectWelcomeScreenRequest.md) |  |  |

### Return type

[**ConnectWelcomeScreen**](ConnectWelcomeScreen.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The saved settings. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The caller cannot change workspace settings (code INSUFFICIENT_PERMISSIONS). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatefacebookpage"></a>
# **UpdateFacebookPage**
> UpdateFacebookPage200Response UpdateFacebookPage (string accountId, UpdateFacebookPageRequest updateFacebookPageRequest)

Update Facebook page

Switch which Facebook Page is active for a connected account.  - `facebook` account: changes the Page posts publish to. - Facebook Login for Business `metaads` connection: changes the default Page ads run as (and the Page whose leads are ingested). - Classic `metaads` connection: has no default Page and answers 400. Pass `pageId` per ad on POST /v1/ads/create instead.  The Page must be in the list returned by GET (use refresh=true to pick up newly granted Pages). 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class UpdateFacebookPageExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var updateFacebookPageRequest = new UpdateFacebookPageRequest(); // UpdateFacebookPageRequest | 

            try
            {
                // Update Facebook page
                UpdateFacebookPage200Response result = apiInstance.UpdateFacebookPage(accountId, updateFacebookPageRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.UpdateFacebookPage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateFacebookPageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Facebook page
    ApiResponse<UpdateFacebookPage200Response> response = apiInstance.UpdateFacebookPageWithHttpInfo(accountId, updateFacebookPageRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.UpdateFacebookPageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **updateFacebookPageRequest** | [**UpdateFacebookPageRequest**](UpdateFacebookPageRequest.md) |  |  |

### Return type

[**UpdateFacebookPage200Response**](UpdateFacebookPage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Page updated |  -  |
| **400** | Page not in available pages, missing selectedPageId, or a classic metaads connection (no default Page) |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found, or not a facebook or metaads account |  -  |
| **409** | Another account on this profile is already connected to that destination (profile_platform_conflict), or the Page has no stored access token (reconnect_required). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updategmblocation"></a>
# **UpdateGmbLocation**
> UpdateGmbLocation200Response UpdateGmbLocation (string accountId, UpdateGmbLocationRequest updateGmbLocationRequest)

Update Google Business Profile location

Switch which Google Business Profile location is active for a connected account.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class UpdateGmbLocationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var updateGmbLocationRequest = new UpdateGmbLocationRequest(); // UpdateGmbLocationRequest | 

            try
            {
                // Update Google Business Profile location
                UpdateGmbLocation200Response result = apiInstance.UpdateGmbLocation(accountId, updateGmbLocationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.UpdateGmbLocation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateGmbLocationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Google Business Profile location
    ApiResponse<UpdateGmbLocation200Response> response = apiInstance.UpdateGmbLocationWithHttpInfo(accountId, updateGmbLocationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.UpdateGmbLocationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **updateGmbLocationRequest** | [**UpdateGmbLocationRequest**](UpdateGmbLocationRequest.md) |  |  |

### Return type

[**UpdateGmbLocation200Response**](UpdateGmbLocation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Location updated |  -  |
| **400** | Location not in available locations, or the provided googleAccountId is not one of the accounts this connection manages |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found |  -  |
| **409** | Another account on this profile is already connected to that destination (profile_platform_conflict). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatelinkedinorganization"></a>
# **UpdateLinkedInOrganization**
> UpdateLinkedInOrganization200Response UpdateLinkedInOrganization (string accountId, UpdateLinkedInOrganizationRequest updateLinkedInOrganizationRequest)

Switch LinkedIn account type

Switch a LinkedIn account between personal profile and organization (company page) posting.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class UpdateLinkedInOrganizationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var updateLinkedInOrganizationRequest = new UpdateLinkedInOrganizationRequest(); // UpdateLinkedInOrganizationRequest | 

            try
            {
                // Switch LinkedIn account type
                UpdateLinkedInOrganization200Response result = apiInstance.UpdateLinkedInOrganization(accountId, updateLinkedInOrganizationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.UpdateLinkedInOrganization: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateLinkedInOrganizationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Switch LinkedIn account type
    ApiResponse<UpdateLinkedInOrganization200Response> response = apiInstance.UpdateLinkedInOrganizationWithHttpInfo(accountId, updateLinkedInOrganizationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.UpdateLinkedInOrganizationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **updateLinkedInOrganizationRequest** | [**UpdateLinkedInOrganizationRequest**](UpdateLinkedInOrganizationRequest.md) |  |  |

### Return type

[**UpdateLinkedInOrganization200Response**](UpdateLinkedInOrganization200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found |  -  |
| **409** | Another account on this profile is already connected to that destination (profile_platform_conflict). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateoauthapp"></a>
# **UpdateOAuthApp**
> CreateOAuthApp201Response UpdateOAuthApp (string appId, UpdateOAuthAppRequest updateOAuthAppRequest)

Update an OAuth app

Renames the app or rotates its secret.  A new secret is checked with the platform before it is saved, and takes effect for every account on the app at once; their tokens keep working.  The client ID cannot change: a different client ID is a different app, so add it and reconnect the accounts through it. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class UpdateOAuthAppExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var appId = "appId_example";  // string | 
            var updateOAuthAppRequest = new UpdateOAuthAppRequest(); // UpdateOAuthAppRequest | 

            try
            {
                // Update an OAuth app
                CreateOAuthApp201Response result = apiInstance.UpdateOAuthApp(appId, updateOAuthAppRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.UpdateOAuthApp: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateOAuthAppWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update an OAuth app
    ApiResponse<CreateOAuthApp201Response> response = apiInstance.UpdateOAuthAppWithHttpInfo(appId, updateOAuthAppRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.UpdateOAuthAppWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appId** | **string** |  |  |
| **updateOAuthAppRequest** | [**UpdateOAuthAppRequest**](UpdateOAuthAppRequest.md) |  |  |

### Return type

[**CreateOAuthApp201Response**](CreateOAuthApp201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated app. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The caller cannot change workspace settings (INSUFFICIENT_PERMISSIONS). |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatepinterestboards"></a>
# **UpdatePinterestBoards**
> ConnectBlueskyCredentials200Response UpdatePinterestBoards (string accountId, UpdatePinterestBoardsRequest updatePinterestBoardsRequest)

Set default Pinterest board

Sets the default board used when publishing pins for this account.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class UpdatePinterestBoardsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var updatePinterestBoardsRequest = new UpdatePinterestBoardsRequest(); // UpdatePinterestBoardsRequest | 

            try
            {
                // Set default Pinterest board
                ConnectBlueskyCredentials200Response result = apiInstance.UpdatePinterestBoards(accountId, updatePinterestBoardsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.UpdatePinterestBoards: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdatePinterestBoardsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set default Pinterest board
    ApiResponse<ConnectBlueskyCredentials200Response> response = apiInstance.UpdatePinterestBoardsWithHttpInfo(accountId, updatePinterestBoardsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.UpdatePinterestBoardsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **updatePinterestBoardsRequest** | [**UpdatePinterestBoardsRequest**](UpdatePinterestBoardsRequest.md) |  |  |

### Return type

[**ConnectBlueskyCredentials200Response**](ConnectBlueskyCredentials200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default board set |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateredditsubreddits"></a>
# **UpdateRedditSubreddits**
> UpdateYoutubeDefaultPlaylist200Response UpdateRedditSubreddits (string accountId, UpdateRedditSubredditsRequest updateRedditSubredditsRequest)

Set default subreddit

Temporarily unavailable: Reddit has blocked third-party apps from its API, so this endpoint returns 503 `PLATFORM_DISABLED` until Reddit restores access. Reddit Ads is not affected.  Sets the default subreddit used when publishing posts for this Reddit account. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class UpdateRedditSubredditsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var updateRedditSubredditsRequest = new UpdateRedditSubredditsRequest(); // UpdateRedditSubredditsRequest | 

            try
            {
                // Set default subreddit
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.UpdateRedditSubreddits(accountId, updateRedditSubredditsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.UpdateRedditSubreddits: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateRedditSubredditsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set default subreddit
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.UpdateRedditSubredditsWithHttpInfo(accountId, updateRedditSubredditsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.UpdateRedditSubredditsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **updateRedditSubredditsRequest** | [**UpdateRedditSubredditsRequest**](UpdateRedditSubredditsRequest.md) |  |  |

### Return type

[**UpdateYoutubeDefaultPlaylist200Response**](UpdateYoutubeDefaultPlaylist200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default subreddit set |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found |  -  |
| **503** | Organic Reddit is temporarily unavailable while Reddit blocks third-party API access (&#x60;PLATFORM_DISABLED&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateyoutubedefaultplaylist"></a>
# **UpdateYoutubeDefaultPlaylist**
> UpdateYoutubeDefaultPlaylist200Response UpdateYoutubeDefaultPlaylist (string accountId, UpdateYoutubeDefaultPlaylistRequest updateYoutubeDefaultPlaylistRequest)

Set default YouTube playlist

Sets the default playlist used when publishing videos for this account. When a post does not specify a playlistId, the default playlist is not automatically used (it is stored for client-side convenience).

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class UpdateYoutubeDefaultPlaylistExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var updateYoutubeDefaultPlaylistRequest = new UpdateYoutubeDefaultPlaylistRequest(); // UpdateYoutubeDefaultPlaylistRequest | 

            try
            {
                // Set default YouTube playlist
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.UpdateYoutubeDefaultPlaylist(accountId, updateYoutubeDefaultPlaylistRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.UpdateYoutubeDefaultPlaylist: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateYoutubeDefaultPlaylistWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set default YouTube playlist
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.UpdateYoutubeDefaultPlaylistWithHttpInfo(accountId, updateYoutubeDefaultPlaylistRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.UpdateYoutubeDefaultPlaylistWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **updateYoutubeDefaultPlaylistRequest** | [**UpdateYoutubeDefaultPlaylistRequest**](UpdateYoutubeDefaultPlaylistRequest.md) |  |  |

### Return type

[**UpdateYoutubeDefaultPlaylist200Response**](UpdateYoutubeDefaultPlaylist200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default playlist set |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="voteredditthing"></a>
# **VoteRedditThing**
> UpdateYoutubeDefaultPlaylist200Response VoteRedditThing (string accountId, VoteRedditThingRequest voteRedditThingRequest)

Vote on a Reddit post or comment

Temporarily unavailable: Reddit has blocked third-party apps from its API, so this endpoint returns 503 `PLATFORM_DISABLED` until Reddit restores access. Reddit Ads is not affected.  Cast, change, or clear the connected account's vote on a Reddit post or comment.  ### Reddit requires that votes be cast by humans  Reddit's API terms permit a client to proxy a human's action one-for-one, and prohibit a bot from deciding how to vote or from amplifying a human's vote.  Call this endpoint only in direct response to an explicit action by the account owner. Automated or agent-decided voting is vote manipulation and puts API access at risk. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class VoteRedditThingExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ConnectApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The ID of the Reddit account casting the vote
            var voteRedditThingRequest = new VoteRedditThingRequest(); // VoteRedditThingRequest | 

            try
            {
                // Vote on a Reddit post or comment
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.VoteRedditThing(accountId, voteRedditThingRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectApi.VoteRedditThing: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VoteRedditThingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Vote on a Reddit post or comment
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.VoteRedditThingWithHttpInfo(accountId, voteRedditThingRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectApi.VoteRedditThingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The ID of the Reddit account casting the vote |  |
| **voteRedditThingRequest** | [**VoteRedditThingRequest**](VoteRedditThingRequest.md) |  |  |

### Return type

[**UpdateYoutubeDefaultPlaylist200Response**](UpdateYoutubeDefaultPlaylist200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Vote registered |  -  |
| **400** | Not a Reddit account, or invalid thingId/direction |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Account not found |  -  |
| **502** | Reddit was unreachable or returned an unclassified error. Reddit 4xx statuses are forwarded as-is. |  -  |
| **503** | Organic Reddit is temporarily unavailable while Reddit blocks third-party API access (&#x60;PLATFORM_DISABLED&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

