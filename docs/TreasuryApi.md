# Zernio.Api.TreasuryApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CancelPayoutBatch**](TreasuryApi.md#cancelpayoutbatch) | **POST** /v1/payout-batches/{batchId}/cancel | Cancel an unpaid payout batch |
| [**CancelTopup**](TreasuryApi.md#canceltopup) | **POST** /v1/balance/top-ups/{topupId}/cancel | Cancel a top-up |
| [**ConfirmPayoutBatch**](TreasuryApi.md#confirmpayoutbatch) | **POST** /v1/payout-batches/{batchId}/confirm | Confirm a payout batch payment |
| [**ConfirmTopup**](TreasuryApi.md#confirmtopup) | **POST** /v1/balance/top-ups/{topupId}/confirm | Confirm a top-up |
| [**CreatePayeeOnboardingLink**](TreasuryApi.md#createpayeeonboardinglink) | **POST** /v1/payees/{payeeId}/onboarding-link | Create a payee onboarding link |
| [**CreateTopup**](TreasuryApi.md#createtopup) | **POST** /v1/balance/top-ups | Create a top-up |
| [**CreateTransfer**](TreasuryApi.md#createtransfer) | **POST** /v1/transfers | Create a transfer |
| [**GetBalance**](TreasuryApi.md#getbalance) | **GET** /v1/balance | Get balance |
| [**GetPayoutBatch**](TreasuryApi.md#getpayoutbatch) | **GET** /v1/payout-batches/{batchId} | Get a payout batch |
| [**GetTopupReceipt**](TreasuryApi.md#gettopupreceipt) | **GET** /v1/balance/top-ups/{topupId}/receipt | Get a top-up receipt |
| [**GetTransfer**](TreasuryApi.md#gettransfer) | **GET** /v1/transfers/{transferId} | Get a transfer |
| [**ListPayees**](TreasuryApi.md#listpayees) | **GET** /v1/payees | List payees |
| [**ListTopups**](TreasuryApi.md#listtopups) | **GET** /v1/balance/top-ups | List top-ups |
| [**ListTransfers**](TreasuryApi.md#listtransfers) | **GET** /v1/transfers | List transfers |

<a id="cancelpayoutbatch"></a>
# **CancelPayoutBatch**
> GetPayoutBatch200Response CancelPayoutBatch (string batchId)

Cancel an unpaid payout batch

Ends the payment of a batch that is still `awaiting_payment` (3D Secure left unfinished) and makes every amount payable again right away.  - When Stripe reports the charge already made, the batch is paid out instead. - A batch that was already paid is returned unchanged.  Needs an owner, admin or billing admin, signed in or through a full-access key they created. 

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
    public class CancelPayoutBatchExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);
            var batchId = "batchId_example";  // string | Payout batch ID.

            try
            {
                // Cancel an unpaid payout batch
                GetPayoutBatch200Response result = apiInstance.CancelPayoutBatch(batchId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.CancelPayoutBatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CancelPayoutBatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cancel an unpaid payout batch
    ApiResponse<GetPayoutBatch200Response> response = apiInstance.CancelPayoutBatchWithHttpInfo(batchId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.CancelPayoutBatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **batchId** | **string** | Payout batch ID. |  |

### Return type

[**GetPayoutBatch200Response**](GetPayoutBatch200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The payout batch after the cancel. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused (&#x60;insufficient_permissions&#x60;). One of:  - A restricted API key without the &#x60;money&#x60; resource group. - A profile-scoped API key. Money leaves the whole team&#39;s balance, so moving it needs a full-access key or a signed-in session (\&quot;Moving money needs a full-access key or a signed-in session.\&quot;). - A member or viewer, signed in or through a key they created. Only an owner, admin or billing admin moves money.  |  -  |
| **404** | No payout batch with this id in a campaign you can see. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="canceltopup"></a>
# **CancelTopup**
> TreasuryTopup CancelTopup (string topupId)

Cancel a top-up

Ends the payment of a pending top-up (3D Secure left unfinished), so it stops counting toward `pendingTopupCents`, and returns it as `expired`.  - When Stripe reports it already paid, the top-up is credited and comes back `succeeded`. - A top-up that is no longer pending comes back unchanged. - A creator payout payment (`purpose: payout_batch`) answers 409; cancel it from its campaign.  Needs an owner, admin or billing admin, signed in or through a full-access key they created. 

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
    public class CancelTopupExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);
            var topupId = "topupId_example";  // string | 

            try
            {
                // Cancel a top-up
                TreasuryTopup result = apiInstance.CancelTopup(topupId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.CancelTopup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CancelTopupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cancel a top-up
    ApiResponse<TreasuryTopup> response = apiInstance.CancelTopupWithHttpInfo(topupId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.CancelTopupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **topupId** | **string** |  |  |

### Return type

[**TreasuryTopup**](TreasuryTopup.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The top-up after cancelling |  -  |
| **400** | Invalid request |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | Refused (&#x60;insufficient_permissions&#x60;). One of:  - A restricted API key without the &#x60;money&#x60; resource group. - A profile-scoped API key. Money leaves the whole team&#39;s balance, so moving it needs a full-access key or a signed-in session (\&quot;Moving money needs a full-access key or a signed-in session.\&quot;). - A member or viewer, signed in or through a key they created. Only an owner, admin or billing admin moves money.  |  -  |
| **404** | Resource not found |  -  |
| **409** | The top-up is a creator payout payment (code &#x60;invalid_resource_state&#x60;); cancel it from its campaign. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="confirmpayoutbatch"></a>
# **ConfirmPayoutBatch**
> GetPayoutBatch200Response ConfirmPayoutBatch (string batchId)

Confirm a payout batch payment

Call after 3D Secure. Reads the batch's payment from Stripe, then:  - charge succeeded: pays the creators (`paying`, then `paid`). - bank refused: ends the batch (`failed`) and makes every amount payable again. - still settling: leaves it `awaiting_payment`.  Safe to repeat. Needs an owner, admin or billing admin, signed in or through a full-access key they created. 

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
    public class ConfirmPayoutBatchExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);
            var batchId = "batchId_example";  // string | Payout batch ID.

            try
            {
                // Confirm a payout batch payment
                GetPayoutBatch200Response result = apiInstance.ConfirmPayoutBatch(batchId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.ConfirmPayoutBatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConfirmPayoutBatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Confirm a payout batch payment
    ApiResponse<GetPayoutBatch200Response> response = apiInstance.ConfirmPayoutBatchWithHttpInfo(batchId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.ConfirmPayoutBatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **batchId** | **string** | Payout batch ID. |  |

### Return type

[**GetPayoutBatch200Response**](GetPayoutBatch200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The payout batch after confirming. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Refused (&#x60;insufficient_permissions&#x60;). One of:  - A restricted API key without the &#x60;money&#x60; resource group. - A profile-scoped API key. Money leaves the whole team&#39;s balance, so moving it needs a full-access key or a signed-in session (\&quot;Moving money needs a full-access key or a signed-in session.\&quot;). - A member or viewer, signed in or through a key they created. Only an owner, admin or billing admin moves money.  |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="confirmtopup"></a>
# **ConfirmTopup**
> TreasuryTopup ConfirmTopup (string topupId)

Confirm a top-up

Call after 3D Secure. Reads the payment from Stripe, then:  - `succeeded`: paid, the top-up is credited. - `failed`: the bank refused it. - `pending`: Stripe is still settling the charge.  Safe to repeat. Needs an owner, admin or billing admin, signed in or through a full-access key they created. 

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
    public class ConfirmTopupExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);
            var topupId = "topupId_example";  // string | 

            try
            {
                // Confirm a top-up
                TreasuryTopup result = apiInstance.ConfirmTopup(topupId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.ConfirmTopup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConfirmTopupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Confirm a top-up
    ApiResponse<TreasuryTopup> response = apiInstance.ConfirmTopupWithHttpInfo(topupId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.ConfirmTopupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **topupId** | **string** |  |  |

### Return type

[**TreasuryTopup**](TreasuryTopup.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The top-up after confirming |  -  |
| **400** | Invalid request |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | Refused (&#x60;insufficient_permissions&#x60;). One of:  - A restricted API key without the &#x60;money&#x60; resource group. - A profile-scoped API key. Money leaves the whole team&#39;s balance, so moving it needs a full-access key or a signed-in session (\&quot;Moving money needs a full-access key or a signed-in session.\&quot;). - A member or viewer, signed in or through a key they created. Only an owner, admin or billing admin moves money.  |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createpayeeonboardinglink"></a>
# **CreatePayeeOnboardingLink**
> CreatePayeeOnboardingLink200Response CreatePayeeOnboardingLink (string payeeId)

Create a payee onboarding link

Returns a Stripe-hosted link where the payee completes identity and bank details so they can receive payouts.

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
    public class CreatePayeeOnboardingLinkExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);
            var payeeId = "payeeId_example";  // string | 

            try
            {
                // Create a payee onboarding link
                CreatePayeeOnboardingLink200Response result = apiInstance.CreatePayeeOnboardingLink(payeeId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.CreatePayeeOnboardingLink: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreatePayeeOnboardingLinkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a payee onboarding link
    ApiResponse<CreatePayeeOnboardingLink200Response> response = apiInstance.CreatePayeeOnboardingLinkWithHttpInfo(payeeId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.CreatePayeeOnboardingLinkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **payeeId** | **string** |  |  |

### Return type

[**CreatePayeeOnboardingLink200Response**](CreatePayeeOnboardingLink200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Onboarding link |  -  |
| **400** | Invalid request |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createtopup"></a>
# **CreateTopup**
> CreateTopup201Response CreateTopup (CreateTopupRequest createTopupRequest, string? idempotencyKey = null)

Create a top-up

Charges the billing owner's saved card (the default one, or `paymentMethodId`) for `amountCents` while the payer is present.  - `status: succeeded`: the card was charged. The top-up is credited to `availableCents` within seconds, net of Stripe's processing fee. Transfers to payees can use it from 7 days after the charge. - `status: requires_action`: the bank asked for 3D Secure. Complete it with Stripe.js `handleNextAction({ clientSecret })`, then call `POST /v1/balance/top-ups/{topupId}/confirm`. One left unconfirmed is cancelled after 30 minutes.  ### Errors  - 402 `payment_required`: no saved card. - 402 `card_declined`: the bank's reason. - 400: `method: bank_transfer` (bank transfers are not available yet).  Needs an owner, admin or billing admin, signed in or through a full-access key they created. 

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
    public class CreateTopupExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);
            var createTopupRequest = new CreateTopupRequest(); // CreateTopupRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  (optional) 

            try
            {
                // Create a top-up
                CreateTopup201Response result = apiInstance.CreateTopup(createTopupRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.CreateTopup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTopupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a top-up
    ApiResponse<CreateTopup201Response> response = apiInstance.CreateTopupWithHttpInfo(createTopupRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.CreateTopupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createTopupRequest** | [**CreateTopupRequest**](CreateTopupRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  | [optional]  |

### Return type

[**CreateTopup201Response**](CreateTopup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The card was charged, or the bank asked for 3D Secure |  -  |
| **400** | Invalid request |  -  |
| **402** | No saved card (code &#x60;payment_required&#x60;), or the bank declined the charge (code &#x60;card_declined&#x60;, the message is the reason), or a billing gate. |  -  |
| **403** | Refused (&#x60;insufficient_permissions&#x60;). One of:  - A restricted API key without the &#x60;money&#x60; resource group. - A profile-scoped API key. Money leaves the whole team&#39;s balance, so moving it needs a full-access key or a signed-in session (\&quot;Moving money needs a full-access key or a signed-in session.\&quot;). - A member or viewer, signed in or through a key they created. Only an owner, admin or billing admin moves money.  |  -  |
| **404** | Resource not found |  -  |
| **409** | Same Idempotency-Key still processing; retry after a short backoff |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createtransfer"></a>
# **CreateTransfer**
> TreasuryTransfer CreateTransfer (CreateTransferRequest createTransferRequest, string? idempotencyKey = null)

Create a transfer

Moves money from your balance to a payee.  ### Fee  The payee receives the full `amountCents`. Zernio's fee (4%, 50 cent minimum) is added on top, so your balance is debited `totalCents` = `amountCents` + `feeCents`.  ### Who can call it  Needs an owner, admin or billing admin, signed in or through a full-access key they created. A profile-scoped key answers 403.  ### Errors  - 402: the balance does not cover the amount plus the fee. - 402: the balance is negative after a dispute or refund of a card top-up (\"Your balance is negative after a dispute or refund of a card top-up. Add funds to cover it before sending transfers.\"). - 409: the payee has not finished onboarding, or the Idempotency-Key is still processing. - 409 `payout_funds_locked`: money from a card top-up can be transferred from 7 days after the charge. The message names the amount and the day (\"$100.00 from your card top-up on Oct 29 can be paid out from Nov 5.\").  ### Retries  A same-key retry never makes the transfer twice within Stripe's 24-hour idempotency window. It answers 409 while another request is still waiting on Stripe for it.  A transfer Stripe has not confirmed after 24 hours answers 409 until the daily reconciliation marks it paid (Stripe made it) or failed (it did not). 

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
    public class CreateTransferExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);
            var createTransferRequest = new CreateTransferRequest(); // CreateTransferRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  (optional) 

            try
            {
                // Create a transfer
                TreasuryTransfer result = apiInstance.CreateTransfer(createTransferRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.CreateTransfer: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTransferWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a transfer
    ApiResponse<TreasuryTransfer> response = apiInstance.CreateTransferWithHttpInfo(createTransferRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.CreateTransferWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createTransferRequest** | [**CreateTransferRequest**](CreateTransferRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  | [optional]  |

### Return type

[**TreasuryTransfer**](TreasuryTransfer.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Transfer created |  -  |
| **400** | Invalid request |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | Refused (&#x60;insufficient_permissions&#x60;). One of:  - A restricted API key without the &#x60;money&#x60; resource group. - A profile-scoped API key. Money leaves the whole team&#39;s balance, so moving it needs a full-access key or a signed-in session (\&quot;Moving money needs a full-access key or a signed-in session.\&quot;). - A member or viewer, signed in or through a key they created. Only an owner, admin or billing admin moves money.  |  -  |
| **404** | Resource not found |  -  |
| **409** | Payee has not finished payout onboarding, the Idempotency-Key is still processing, another request is waiting on Stripe for this transfer, or Stripe has not confirmed it within 24 hours |  -  |
| **422** | Idempotency-Key reused with a different request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbalance"></a>
# **GetBalance**
> GetBalance200Response GetBalance ()

Get balance

Returns your team's balance:  - the balance you can transfer - the part of it that cannot be paid out to creators yet (`payoutLockedCents`, `payoutLocks`) - top-ups still waiting for payment - your latest top-ups  A card top-up is in `availableCents` as soon as it is paid. Transfers to payees can use it from 7 days after the charge, so a stolen card cannot be turned straight into payouts.  A transfer debits its amount plus the fee added on top; the payee receives the full amount.  A card dispute or refund on a top-up is debited from the available balance and can make it negative. Transfers are refused until it is positive again.  A profile-scoped key answers 403, since the balance belongs to the whole team. 

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
    public class GetBalanceExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);

            try
            {
                // Get balance
                GetBalance200Response result = apiInstance.GetBalance();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.GetBalance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBalanceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get balance
    ApiResponse<GetBalance200Response> response = apiInstance.GetBalanceWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.GetBalanceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**GetBalance200Response**](GetBalance200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Balance in cents |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getpayoutbatch"></a>
# **GetPayoutBatch**
> GetPayoutBatch200Response GetPayoutBatch (string batchId)

Get a payout batch

One payout batch with its status and each creator's item. Poll it after the card payment to see when every creator is paid.

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
    public class GetPayoutBatchExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);
            var batchId = "batchId_example";  // string | Payout batch ID.

            try
            {
                // Get a payout batch
                GetPayoutBatch200Response result = apiInstance.GetPayoutBatch(batchId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.GetPayoutBatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPayoutBatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a payout batch
    ApiResponse<GetPayoutBatch200Response> response = apiInstance.GetPayoutBatchWithHttpInfo(batchId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.GetPayoutBatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **batchId** | **string** | Payout batch ID. |  |

### Return type

[**GetPayoutBatch200Response**](GetPayoutBatch200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The payout batch. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | No payout batch with this id in a campaign you can see. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettopupreceipt"></a>
# **GetTopupReceipt**
> GetTopupReceipt200Response GetTopupReceipt (string topupId)

Get a top-up receipt

The receipt for a paid top-up or creator payout payment (`purpose: payout_batch`). `format: pdf` is the Stripe invoice PDF; `format: page` is Stripe's receipt page, for payments that have no invoice. The link is short-lived, so fetch it when you need it. A profile-scoped key answers 403.

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
    public class GetTopupReceiptExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);
            var topupId = "topupId_example";  // string | 

            try
            {
                // Get a top-up receipt
                GetTopupReceipt200Response result = apiInstance.GetTopupReceipt(topupId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.GetTopupReceipt: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTopupReceiptWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a top-up receipt
    ApiResponse<GetTopupReceipt200Response> response = apiInstance.GetTopupReceiptWithHttpInfo(topupId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.GetTopupReceiptWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **topupId** | **string** |  |  |

### Return type

[**GetTopupReceipt200Response**](GetTopupReceipt200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Receipt link |  -  |
| **400** | Invalid request |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettransfer"></a>
# **GetTransfer**
> TreasuryTransfer GetTransfer (string transferId)

Get a transfer

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
    public class GetTransferExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);
            var transferId = "transferId_example";  // string | 

            try
            {
                // Get a transfer
                TreasuryTransfer result = apiInstance.GetTransfer(transferId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.GetTransfer: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTransferWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a transfer
    ApiResponse<TreasuryTransfer> response = apiInstance.GetTransferWithHttpInfo(transferId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.GetTransferWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **transferId** | **string** |  |  |

### Return type

[**TreasuryTransfer**](TreasuryTransfer.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Transfer |  -  |
| **400** | Invalid request |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listpayees"></a>
# **ListPayees**
> ListPayees200Response ListPayees ()

List payees

Payees you can transfer to. A payee can receive transfers once `payoutsEnabled` is true. A profile-scoped key answers 403.

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
    public class ListPayeesExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);

            try
            {
                // List payees
                ListPayees200Response result = apiInstance.ListPayees();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.ListPayees: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListPayeesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List payees
    ApiResponse<ListPayees200Response> response = apiInstance.ListPayeesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.ListPayeesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListPayees200Response**](ListPayees200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payees |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtopups"></a>
# **ListTopups**
> ListTopups200Response ListTopups (int? limit = null, int? skip = null)

List top-ups

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
    public class ListTopupsExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List top-ups
                ListTopups200Response result = apiInstance.ListTopups(limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.ListTopups: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTopupsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List top-ups
    ApiResponse<ListTopups200Response> response = apiInstance.ListTopupsWithHttpInfo(limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.ListTopupsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int?** |  | [optional] [default to 50] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**ListTopups200Response**](ListTopups200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Top-ups, newest first |  -  |
| **400** | Invalid request |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtransfers"></a>
# **ListTransfers**
> ListTransfers200Response ListTransfers (int? limit = null, int? skip = null)

List transfers

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
    public class ListTransfersExample
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
            var apiInstance = new TreasuryApi(httpClient, config, httpClientHandler);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var skip = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // List transfers
                ListTransfers200Response result = apiInstance.ListTransfers(limit, skip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TreasuryApi.ListTransfers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTransfersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List transfers
    ApiResponse<ListTransfers200Response> response = apiInstance.ListTransfersWithHttpInfo(limit, skip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TreasuryApi.ListTransfersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int?** |  | [optional] [default to 50] |
| **skip** | **int?** |  | [optional] [default to 0] |

### Return type

[**ListTransfers200Response**](ListTransfers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Transfers, newest first |  -  |
| **400** | Invalid request |  -  |
| **402** | Payment method or enterprise contract required: the authenticated account hit a billing gate before the connection could proceed. Switch on &#x60;reason&#x60; to render the right prompt:  - &#x60;free_tier_exceeded&#x60;: the team has connected more accounts than the free tier allows. Add a payment method to continue (billed per additional connected account). - &#x60;twitter_passthrough&#x60;: connecting an X account requires a card on file from day one, because X API calls incur real per-call pass-through costs. Applies to the 1st X account, not only the 3rd+. - &#x60;enterprise_required&#x60;: the team&#39;s enterprise contract sets a connected-account cap and it has been reached. Self-service teams have NO cap (the $1/account rate continues at any scale). The user already has a card on file; this gate is about contract terms. - &#x60;card_verification_required&#x60;: the card on file was flagged at add time (prepaid, or issued in a different country than the billing address). A one-time verification charge of &#x60;details.verification_amount_cents&#x60; (USD) is pending; it is credited to the team&#39;s usage balance, not a fee.  **What to do:** redirect the end-user to &#x60;dashboard_url&#x60;.  - &#x60;free_tier_exceeded&#x60;, &#x60;twitter_passthrough&#x60;, &#x60;card_verification_required&#x60;: it opens the Zernio billing page (the add-payment-method drawer, or the verification step). The request succeeds once the card is on file (or verified, or paid). - &#x60;enterprise_required&#x60;: it opens the enterprise contact form (not the billing tab), to adjust the contract&#39;s limit.  |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

