# Zernio.Api.BusinessAgentApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddBusinessAgentAllowlistEntry**](BusinessAgentApi.md#addbusinessagentallowlistentry) | **POST** /v1/accounts/{accountId}/business-agent/allowlist | Allowlist a consumer |
| [**AddBusinessAgentWebsite**](BusinessAgentApi.md#addbusinessagentwebsite) | **POST** /v1/accounts/{accountId}/business-agent/websites | Add a website to crawl |
| [**CreateBusinessAgentConnector**](BusinessAgentApi.md#createbusinessagentconnector) | **POST** /v1/accounts/{accountId}/business-agent/connectors | Create a connector |
| [**CreateBusinessAgentConnectorTool**](BusinessAgentApi.md#createbusinessagentconnectortool) | **POST** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/tools | Create a connector tool |
| [**CreateBusinessAgentFaq**](BusinessAgentApi.md#createbusinessagentfaq) | **POST** /v1/accounts/{accountId}/business-agent/faqs | Create a FAQ |
| [**CreateBusinessAgentSkill**](BusinessAgentApi.md#createbusinessagentskill) | **POST** /v1/accounts/{accountId}/business-agent/skills | Create a skill |
| [**CreateBusinessAgentUiSkill**](BusinessAgentApi.md#createbusinessagentuiskill) | **POST** /v1/accounts/{accountId}/business-agent/ui-skills | Create a UI skill |
| [**DeleteBusinessAgentConnector**](BusinessAgentApi.md#deletebusinessagentconnector) | **DELETE** /v1/accounts/{accountId}/business-agent/connectors/{connectorId} | Delete a connector |
| [**DeleteBusinessAgentConnectorTool**](BusinessAgentApi.md#deletebusinessagentconnectortool) | **DELETE** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/tools/{toolId} | Delete a connector tool |
| [**DeleteBusinessAgentFaq**](BusinessAgentApi.md#deletebusinessagentfaq) | **DELETE** /v1/accounts/{accountId}/business-agent/faqs/{faqId} | Delete a FAQ |
| [**DeleteBusinessAgentFile**](BusinessAgentApi.md#deletebusinessagentfile) | **DELETE** /v1/accounts/{accountId}/business-agent/files/{fileId} | Delete a knowledge file |
| [**DeleteBusinessAgentSkill**](BusinessAgentApi.md#deletebusinessagentskill) | **DELETE** /v1/accounts/{accountId}/business-agent/skills/{skillId} | Delete a skill |
| [**DeleteBusinessAgentUiSkill**](BusinessAgentApi.md#deletebusinessagentuiskill) | **DELETE** /v1/accounts/{accountId}/business-agent/ui-skills/{uiSkillId} | Delete a UI skill |
| [**DeleteBusinessAgentWebsite**](BusinessAgentApi.md#deletebusinessagentwebsite) | **DELETE** /v1/accounts/{accountId}/business-agent/websites/{websiteId} | Remove a crawled website |
| [**GetBusinessAgentBudget**](BusinessAgentApi.md#getbusinessagentbudget) | **GET** /v1/accounts/{accountId}/business-agent/budget | Get usage budgets |
| [**GetBusinessAgentBusinessInformation**](BusinessAgentApi.md#getbusinessagentbusinessinformation) | **GET** /v1/accounts/{accountId}/business-agent/business-information | Get business information |
| [**GetBusinessAgentConnector**](BusinessAgentApi.md#getbusinessagentconnector) | **GET** /v1/accounts/{accountId}/business-agent/connectors/{connectorId} | Get a connector |
| [**GetBusinessAgentConnectorLogs**](BusinessAgentApi.md#getbusinessagentconnectorlogs) | **GET** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/logs | Get connector failure logs |
| [**GetBusinessAgentConnectorTool**](BusinessAgentApi.md#getbusinessagentconnectortool) | **GET** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/tools/{toolId} | Get a connector tool |
| [**GetBusinessAgentEvent**](BusinessAgentApi.md#getbusinessagentevent) | **GET** /v1/accounts/{accountId}/business-agent/events/{eventId} | Get a business event status |
| [**GetBusinessAgentFaq**](BusinessAgentApi.md#getbusinessagentfaq) | **GET** /v1/accounts/{accountId}/business-agent/faqs/{faqId} | Get a FAQ |
| [**GetBusinessAgentFile**](BusinessAgentApi.md#getbusinessagentfile) | **GET** /v1/accounts/{accountId}/business-agent/files/{fileId} | Get a knowledge file |
| [**GetBusinessAgentSkill**](BusinessAgentApi.md#getbusinessagentskill) | **GET** /v1/accounts/{accountId}/business-agent/skills/{skillId} | Get a skill |
| [**GetBusinessAgentStatus**](BusinessAgentApi.md#getbusinessagentstatus) | **GET** /v1/accounts/{accountId}/business-agent | Get agent setup status |
| [**GetBusinessAgentUiSkill**](BusinessAgentApi.md#getbusinessagentuiskill) | **GET** /v1/accounts/{accountId}/business-agent/ui-skills/{uiSkillId} | Get a UI skill |
| [**GetBusinessAgentWebsite**](BusinessAgentApi.md#getbusinessagentwebsite) | **GET** /v1/accounts/{accountId}/business-agent/websites/{websiteId} | Get a crawled website |
| [**ListBusinessAgentAllowlist**](BusinessAgentApi.md#listbusinessagentallowlist) | **GET** /v1/accounts/{accountId}/business-agent/allowlist | List allowlisted consumers |
| [**ListBusinessAgentConnectorTools**](BusinessAgentApi.md#listbusinessagentconnectortools) | **GET** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/tools | List connector tools |
| [**ListBusinessAgentConnectors**](BusinessAgentApi.md#listbusinessagentconnectors) | **GET** /v1/accounts/{accountId}/business-agent/connectors | List connectors |
| [**ListBusinessAgentFaqs**](BusinessAgentApi.md#listbusinessagentfaqs) | **GET** /v1/accounts/{accountId}/business-agent/faqs | List FAQs |
| [**ListBusinessAgentFiles**](BusinessAgentApi.md#listbusinessagentfiles) | **GET** /v1/accounts/{accountId}/business-agent/files | List knowledge files |
| [**ListBusinessAgentSettings**](BusinessAgentApi.md#listbusinessagentsettings) | **GET** /v1/accounts/{accountId}/business-agent/settings | List agent settings |
| [**ListBusinessAgentSkills**](BusinessAgentApi.md#listbusinessagentskills) | **GET** /v1/accounts/{accountId}/business-agent/skills | List skills |
| [**ListBusinessAgentUiSkills**](BusinessAgentApi.md#listbusinessagentuiskills) | **GET** /v1/accounts/{accountId}/business-agent/ui-skills | List UI skills |
| [**ListBusinessAgentWebsites**](BusinessAgentApi.md#listbusinessagentwebsites) | **GET** /v1/accounts/{accountId}/business-agent/websites | List crawled websites |
| [**OnboardBusinessAgent**](BusinessAgentApi.md#onboardbusinessagent) | **POST** /v1/accounts/{accountId}/business-agent/onboard | Create the agent |
| [**ReadBusinessAgentEvals**](BusinessAgentApi.md#readbusinessagentevals) | **GET** /v1/accounts/{accountId}/business-agent/evals | Read evaluation data |
| [**RefreshBusinessAgentConnectorTools**](BusinessAgentApi.md#refreshbusinessagentconnectortools) | **POST** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/refresh-tools | Refresh MCP connector tools |
| [**RemoveBusinessAgentAllowlistEntry**](BusinessAgentApi.md#removebusinessagentallowlistentry) | **DELETE** /v1/accounts/{accountId}/business-agent/allowlist/{entryId} | Remove an allowlisted consumer |
| [**ReplaceBusinessAgentBudget**](BusinessAgentApi.md#replacebusinessagentbudget) | **PUT** /v1/accounts/{accountId}/business-agent/budget | Replace usage budgets |
| [**ReplaceBusinessAgentBusinessInformation**](BusinessAgentApi.md#replacebusinessagentbusinessinformation) | **PUT** /v1/accounts/{accountId}/business-agent/business-information | Replace business information |
| [**ResetBusinessAgentBusinessInformation**](BusinessAgentApi.md#resetbusinessagentbusinessinformation) | **DELETE** /v1/accounts/{accountId}/business-agent/business-information | Reset business information |
| [**RunBusinessAgentConnectorTool**](BusinessAgentApi.md#runbusinessagentconnectortool) | **POST** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/tools/{toolId}/run | Run a connector tool once |
| [**SendBusinessAgentEvent**](BusinessAgentApi.md#sendbusinessagentevent) | **POST** /v1/accounts/{accountId}/business-agent/events | Send a business event |
| [**SendBusinessAgentTestMessage**](BusinessAgentApi.md#sendbusinessagenttestmessage) | **POST** /v1/accounts/{accountId}/business-agent/test-messages | Send a test message |
| [**SetBusinessAgentConnectorCredentials**](BusinessAgentApi.md#setbusinessagentconnectorcredentials) | **POST** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/credentials | Set connector credentials |
| [**StartBusinessAgentEvalRun**](BusinessAgentApi.md#startbusinessagentevalrun) | **POST** /v1/accounts/{accountId}/business-agent/evals | Start an evaluation run |
| [**UpdateBusinessAgentConnector**](BusinessAgentApi.md#updatebusinessagentconnector) | **PUT** /v1/accounts/{accountId}/business-agent/connectors/{connectorId} | Update a connector |
| [**UpdateBusinessAgentConnectorTool**](BusinessAgentApi.md#updatebusinessagentconnectortool) | **PUT** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/tools/{toolId} | Update a connector tool |
| [**UpdateBusinessAgentFaq**](BusinessAgentApi.md#updatebusinessagentfaq) | **PUT** /v1/accounts/{accountId}/business-agent/faqs/{faqId} | Update a FAQ |
| [**UpdateBusinessAgentSettings**](BusinessAgentApi.md#updatebusinessagentsettings) | **PATCH** /v1/accounts/{accountId}/business-agent/settings | Update agent settings |
| [**UpdateBusinessAgentSkill**](BusinessAgentApi.md#updatebusinessagentskill) | **PUT** /v1/accounts/{accountId}/business-agent/skills/{skillId} | Update a skill |
| [**UpdateBusinessAgentUiSkill**](BusinessAgentApi.md#updatebusinessagentuiskill) | **PUT** /v1/accounts/{accountId}/business-agent/ui-skills/{uiSkillId} | Update a UI skill |
| [**UpdateBusinessAgentWebsite**](BusinessAgentApi.md#updatebusinessagentwebsite) | **PUT** /v1/accounts/{accountId}/business-agent/websites/{websiteId} | Update a crawled website |
| [**UploadBusinessAgentFile**](BusinessAgentApi.md#uploadbusinessagentfile) | **POST** /v1/accounts/{accountId}/business-agent/files | Upload a knowledge file |

<a id="addbusinessagentallowlistentry"></a>
# **AddBusinessAgentAllowlistEntry**
> BusinessAgentAllowlistEntry AddBusinessAgentAllowlistEntry (string accountId, AddBusinessAgentAllowlistEntryRequest addBusinessAgentAllowlistEntryRequest)

Allowlist a consumer

One E.164 number per call. Not idempotent.

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
    public class AddBusinessAgentAllowlistEntryExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var addBusinessAgentAllowlistEntryRequest = new AddBusinessAgentAllowlistEntryRequest(); // AddBusinessAgentAllowlistEntryRequest | 

            try
            {
                // Allowlist a consumer
                BusinessAgentAllowlistEntry result = apiInstance.AddBusinessAgentAllowlistEntry(accountId, addBusinessAgentAllowlistEntryRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.AddBusinessAgentAllowlistEntry: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddBusinessAgentAllowlistEntryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Allowlist a consumer
    ApiResponse<BusinessAgentAllowlistEntry> response = apiInstance.AddBusinessAgentAllowlistEntryWithHttpInfo(accountId, addBusinessAgentAllowlistEntryRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.AddBusinessAgentAllowlistEntryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **addBusinessAgentAllowlistEntryRequest** | [**AddBusinessAgentAllowlistEntryRequest**](AddBusinessAgentAllowlistEntryRequest.md) |  |  |

### Return type

[**BusinessAgentAllowlistEntry**](BusinessAgentAllowlistEntry.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Entry added |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="addbusinessagentwebsite"></a>
# **AddBusinessAgentWebsite**
> BusinessAgentWebsite AddBusinessAgentWebsite (string accountId, BusinessAgentWebsiteInput businessAgentWebsiteInput)

Add a website to crawl

Meta crawls the site into the agent knowledge and recrawls it periodically; check `crawl_status` and `crawl_error` on read. Not idempotent.

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
    public class AddBusinessAgentWebsiteExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var businessAgentWebsiteInput = new BusinessAgentWebsiteInput(); // BusinessAgentWebsiteInput | 

            try
            {
                // Add a website to crawl
                BusinessAgentWebsite result = apiInstance.AddBusinessAgentWebsite(accountId, businessAgentWebsiteInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.AddBusinessAgentWebsite: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddBusinessAgentWebsiteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add a website to crawl
    ApiResponse<BusinessAgentWebsite> response = apiInstance.AddBusinessAgentWebsiteWithHttpInfo(accountId, businessAgentWebsiteInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.AddBusinessAgentWebsiteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **businessAgentWebsiteInput** | [**BusinessAgentWebsiteInput**](BusinessAgentWebsiteInput.md) |  |  |

### Return type

[**BusinessAgentWebsite**](BusinessAgentWebsite.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Website added |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createbusinessagentconnector"></a>
# **CreateBusinessAgentConnector**
> BusinessAgentConnector CreateBusinessAgentConnector (string accountId, BusinessAgentConnectorInput businessAgentConnectorInput)

Create a connector

Base URL plus how to authenticate (OAuth client credentials, API key or none). Names are unique per number. Not idempotent.

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
    public class CreateBusinessAgentConnectorExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var businessAgentConnectorInput = new BusinessAgentConnectorInput(); // BusinessAgentConnectorInput | 

            try
            {
                // Create a connector
                BusinessAgentConnector result = apiInstance.CreateBusinessAgentConnector(accountId, businessAgentConnectorInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.CreateBusinessAgentConnector: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBusinessAgentConnectorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a connector
    ApiResponse<BusinessAgentConnector> response = apiInstance.CreateBusinessAgentConnectorWithHttpInfo(accountId, businessAgentConnectorInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.CreateBusinessAgentConnectorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **businessAgentConnectorInput** | [**BusinessAgentConnectorInput**](BusinessAgentConnectorInput.md) |  |  |

### Return type

[**BusinessAgentConnector**](BusinessAgentConnector.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Connector created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |
| **409** | A connector with that name already exists (code business_agent_conflict). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createbusinessagentconnectortool"></a>
# **CreateBusinessAgentConnectorTool**
> BusinessAgentConnectorTool CreateBusinessAgentConnectorTool (string accountId, string connectorId, BusinessAgentConnectorToolInput businessAgentConnectorToolInput)

Create a connector tool

One operation on the connector, with the request definition Meta uses to build the outbound call from the conversation. Type the body params explicitly. Not idempotent.

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
    public class CreateBusinessAgentConnectorToolExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var connectorId = "connectorId_example";  // string | 
            var businessAgentConnectorToolInput = new BusinessAgentConnectorToolInput(); // BusinessAgentConnectorToolInput | 

            try
            {
                // Create a connector tool
                BusinessAgentConnectorTool result = apiInstance.CreateBusinessAgentConnectorTool(accountId, connectorId, businessAgentConnectorToolInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.CreateBusinessAgentConnectorTool: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBusinessAgentConnectorToolWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a connector tool
    ApiResponse<BusinessAgentConnectorTool> response = apiInstance.CreateBusinessAgentConnectorToolWithHttpInfo(accountId, connectorId, businessAgentConnectorToolInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.CreateBusinessAgentConnectorToolWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **connectorId** | **string** |  |  |
| **businessAgentConnectorToolInput** | [**BusinessAgentConnectorToolInput**](BusinessAgentConnectorToolInput.md) |  |  |

### Return type

[**BusinessAgentConnectorTool**](BusinessAgentConnectorTool.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Tool created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createbusinessagentfaq"></a>
# **CreateBusinessAgentFaq**
> BusinessAgentFaq CreateBusinessAgentFaq (string accountId, BusinessAgentFaqInput businessAgentFaqInput)

Create a FAQ

One specific question per entry; beyond a few hundred entries retrieval quality drops. Not idempotent.

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
    public class CreateBusinessAgentFaqExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var businessAgentFaqInput = new BusinessAgentFaqInput(); // BusinessAgentFaqInput | 

            try
            {
                // Create a FAQ
                BusinessAgentFaq result = apiInstance.CreateBusinessAgentFaq(accountId, businessAgentFaqInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.CreateBusinessAgentFaq: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBusinessAgentFaqWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a FAQ
    ApiResponse<BusinessAgentFaq> response = apiInstance.CreateBusinessAgentFaqWithHttpInfo(accountId, businessAgentFaqInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.CreateBusinessAgentFaqWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **businessAgentFaqInput** | [**BusinessAgentFaqInput**](BusinessAgentFaqInput.md) |  |  |

### Return type

[**BusinessAgentFaq**](BusinessAgentFaq.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | FAQ created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |
| **409** | Meta rejected the entry (code business_agent_conflict). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createbusinessagentskill"></a>
# **CreateBusinessAgentSkill**
> BusinessAgentSkill CreateBusinessAgentSkill (string accountId, BusinessAgentSkillInput businessAgentSkillInput)

Create a skill

Behavioral instructions in the brand voice. Reads back `pending_review` until Meta content review passes it. Not idempotent.

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
    public class CreateBusinessAgentSkillExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var businessAgentSkillInput = new BusinessAgentSkillInput(); // BusinessAgentSkillInput | 

            try
            {
                // Create a skill
                BusinessAgentSkill result = apiInstance.CreateBusinessAgentSkill(accountId, businessAgentSkillInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.CreateBusinessAgentSkill: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBusinessAgentSkillWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a skill
    ApiResponse<BusinessAgentSkill> response = apiInstance.CreateBusinessAgentSkillWithHttpInfo(accountId, businessAgentSkillInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.CreateBusinessAgentSkillWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **businessAgentSkillInput** | [**BusinessAgentSkillInput**](BusinessAgentSkillInput.md) |  |  |

### Return type

[**BusinessAgentSkill**](BusinessAgentSkill.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Skill created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createbusinessagentuiskill"></a>
# **CreateBusinessAgentUiSkill**
> BusinessAgentUiSkill CreateBusinessAgentUiSkill (string accountId, BusinessAgentUiSkillInput businessAgentUiSkillInput)

Create a UI skill

Tells the agent when to send a rich component (CTA URL button, image, carousel, list, reply buttons, location, Flow) and what to put in it. Not idempotent.

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
    public class CreateBusinessAgentUiSkillExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var businessAgentUiSkillInput = new BusinessAgentUiSkillInput(); // BusinessAgentUiSkillInput | 

            try
            {
                // Create a UI skill
                BusinessAgentUiSkill result = apiInstance.CreateBusinessAgentUiSkill(accountId, businessAgentUiSkillInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.CreateBusinessAgentUiSkill: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBusinessAgentUiSkillWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a UI skill
    ApiResponse<BusinessAgentUiSkill> response = apiInstance.CreateBusinessAgentUiSkillWithHttpInfo(accountId, businessAgentUiSkillInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.CreateBusinessAgentUiSkillWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **businessAgentUiSkillInput** | [**BusinessAgentUiSkillInput**](BusinessAgentUiSkillInput.md) |  |  |

### Return type

[**BusinessAgentUiSkill**](BusinessAgentUiSkill.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | UI skill created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletebusinessagentconnector"></a>
# **DeleteBusinessAgentConnector**
> InlineObject DeleteBusinessAgentConnector (string accountId, string connectorId)

Delete a connector

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
    public class DeleteBusinessAgentConnectorExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var connectorId = "connectorId_example";  // string | 

            try
            {
                // Delete a connector
                InlineObject result = apiInstance.DeleteBusinessAgentConnector(accountId, connectorId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentConnector: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBusinessAgentConnectorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a connector
    ApiResponse<InlineObject> response = apiInstance.DeleteBusinessAgentConnectorWithHttpInfo(accountId, connectorId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentConnectorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **connectorId** | **string** |  |  |

### Return type

[**InlineObject**](InlineObject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletebusinessagentconnectortool"></a>
# **DeleteBusinessAgentConnectorTool**
> InlineObject DeleteBusinessAgentConnectorTool (string accountId, string connectorId, string toolId)

Delete a connector tool

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
    public class DeleteBusinessAgentConnectorToolExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var connectorId = "connectorId_example";  // string | 
            var toolId = "toolId_example";  // string | 

            try
            {
                // Delete a connector tool
                InlineObject result = apiInstance.DeleteBusinessAgentConnectorTool(accountId, connectorId, toolId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentConnectorTool: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBusinessAgentConnectorToolWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a connector tool
    ApiResponse<InlineObject> response = apiInstance.DeleteBusinessAgentConnectorToolWithHttpInfo(accountId, connectorId, toolId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentConnectorToolWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **connectorId** | **string** |  |  |
| **toolId** | **string** |  |  |

### Return type

[**InlineObject**](InlineObject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletebusinessagentfaq"></a>
# **DeleteBusinessAgentFaq**
> InlineObject DeleteBusinessAgentFaq (string accountId, string faqId)

Delete a FAQ

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
    public class DeleteBusinessAgentFaqExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var faqId = "faqId_example";  // string | 

            try
            {
                // Delete a FAQ
                InlineObject result = apiInstance.DeleteBusinessAgentFaq(accountId, faqId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentFaq: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBusinessAgentFaqWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a FAQ
    ApiResponse<InlineObject> response = apiInstance.DeleteBusinessAgentFaqWithHttpInfo(accountId, faqId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentFaqWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **faqId** | **string** |  |  |

### Return type

[**InlineObject**](InlineObject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletebusinessagentfile"></a>
# **DeleteBusinessAgentFile**
> InlineObject DeleteBusinessAgentFile (string accountId, string fileId)

Delete a knowledge file

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
    public class DeleteBusinessAgentFileExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var fileId = "fileId_example";  // string | 

            try
            {
                // Delete a knowledge file
                InlineObject result = apiInstance.DeleteBusinessAgentFile(accountId, fileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBusinessAgentFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a knowledge file
    ApiResponse<InlineObject> response = apiInstance.DeleteBusinessAgentFileWithHttpInfo(accountId, fileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **fileId** | **string** |  |  |

### Return type

[**InlineObject**](InlineObject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletebusinessagentskill"></a>
# **DeleteBusinessAgentSkill**
> InlineObject DeleteBusinessAgentSkill (string accountId, string skillId)

Delete a skill

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
    public class DeleteBusinessAgentSkillExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var skillId = "skillId_example";  // string | 

            try
            {
                // Delete a skill
                InlineObject result = apiInstance.DeleteBusinessAgentSkill(accountId, skillId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentSkill: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBusinessAgentSkillWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a skill
    ApiResponse<InlineObject> response = apiInstance.DeleteBusinessAgentSkillWithHttpInfo(accountId, skillId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentSkillWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **skillId** | **string** |  |  |

### Return type

[**InlineObject**](InlineObject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletebusinessagentuiskill"></a>
# **DeleteBusinessAgentUiSkill**
> InlineObject DeleteBusinessAgentUiSkill (string accountId, string uiSkillId)

Delete a UI skill

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
    public class DeleteBusinessAgentUiSkillExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var uiSkillId = "uiSkillId_example";  // string | 

            try
            {
                // Delete a UI skill
                InlineObject result = apiInstance.DeleteBusinessAgentUiSkill(accountId, uiSkillId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentUiSkill: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBusinessAgentUiSkillWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a UI skill
    ApiResponse<InlineObject> response = apiInstance.DeleteBusinessAgentUiSkillWithHttpInfo(accountId, uiSkillId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentUiSkillWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **uiSkillId** | **string** |  |  |

### Return type

[**InlineObject**](InlineObject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletebusinessagentwebsite"></a>
# **DeleteBusinessAgentWebsite**
> InlineObject DeleteBusinessAgentWebsite (string accountId, string websiteId)

Remove a crawled website

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
    public class DeleteBusinessAgentWebsiteExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var websiteId = "websiteId_example";  // string | 

            try
            {
                // Remove a crawled website
                InlineObject result = apiInstance.DeleteBusinessAgentWebsite(accountId, websiteId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentWebsite: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBusinessAgentWebsiteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove a crawled website
    ApiResponse<InlineObject> response = apiInstance.DeleteBusinessAgentWebsiteWithHttpInfo(accountId, websiteId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.DeleteBusinessAgentWebsiteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **websiteId** | **string** |  |  |

### Return type

[**InlineObject**](InlineObject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbusinessagentbudget"></a>
# **GetBusinessAgentBudget**
> GetBusinessAgentBudget200Response GetBusinessAgentBudget (string accountId)

Get usage budgets

Caps over rolling windows for the Business Manager that owns the number. An empty list means unlimited.

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
    public class GetBusinessAgentBudgetExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).

            try
            {
                // Get usage budgets
                GetBusinessAgentBudget200Response result = apiInstance.GetBusinessAgentBudget(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentBudget: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessAgentBudgetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get usage budgets
    ApiResponse<GetBusinessAgentBudget200Response> response = apiInstance.GetBusinessAgentBudgetWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentBudgetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |

### Return type

[**GetBusinessAgentBudget200Response**](GetBusinessAgentBudget200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Budgets |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbusinessagentbusinessinformation"></a>
# **GetBusinessAgentBusinessInformation**
> BusinessAgentBusinessInformation GetBusinessAgentBusinessInformation (string accountId)

Get business information

Payment methods, return policy, how to buy, shipping, description and contact details the agent answers from. Empty values until configured.

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
    public class GetBusinessAgentBusinessInformationExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).

            try
            {
                // Get business information
                BusinessAgentBusinessInformation result = apiInstance.GetBusinessAgentBusinessInformation(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentBusinessInformation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessAgentBusinessInformationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get business information
    ApiResponse<BusinessAgentBusinessInformation> response = apiInstance.GetBusinessAgentBusinessInformationWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentBusinessInformationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |

### Return type

[**BusinessAgentBusinessInformation**](BusinessAgentBusinessInformation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Business information |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbusinessagentconnector"></a>
# **GetBusinessAgentConnector**
> BusinessAgentConnector GetBusinessAgentConnector (string accountId, string connectorId)

Get a connector

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
    public class GetBusinessAgentConnectorExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var connectorId = "connectorId_example";  // string | 

            try
            {
                // Get a connector
                BusinessAgentConnector result = apiInstance.GetBusinessAgentConnector(accountId, connectorId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentConnector: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessAgentConnectorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a connector
    ApiResponse<BusinessAgentConnector> response = apiInstance.GetBusinessAgentConnectorWithHttpInfo(accountId, connectorId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentConnectorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **connectorId** | **string** |  |  |

### Return type

[**BusinessAgentConnector**](BusinessAgentConnector.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connector |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbusinessagentconnectorlogs"></a>
# **GetBusinessAgentConnectorLogs**
> GetBusinessAgentConnectorLogs200Response GetBusinessAgentConnectorLogs (string accountId, string connectorId, int? startTime = null, int? endTime = null, int? limit = null, string? toolId = null, bool? includeStats = null, bool? summaryOnly = null, int? topN = null)

Get connector failure logs

Third-party failures over the last 7 days (window at most 7 days, default the last 24 hours). Each entry carries `failure_code_name` and `error_message`.

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
    public class GetBusinessAgentConnectorLogsExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var connectorId = "connectorId_example";  // string | 
            var startTime = 56;  // int? | Unix seconds. (optional) 
            var endTime = 56;  // int? | Unix seconds. (optional) 
            var limit = 56;  // int? |  (optional) 
            var toolId = "toolId_example";  // string? |  (optional) 
            var includeStats = true;  // bool? | Add success rate and latency percentiles. (optional) 
            var summaryOnly = true;  // bool? | Aggregate failure patterns instead of entries. (optional) 
            var topN = 56;  // int? |  (optional) 

            try
            {
                // Get connector failure logs
                GetBusinessAgentConnectorLogs200Response result = apiInstance.GetBusinessAgentConnectorLogs(accountId, connectorId, startTime, endTime, limit, toolId, includeStats, summaryOnly, topN);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentConnectorLogs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessAgentConnectorLogsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get connector failure logs
    ApiResponse<GetBusinessAgentConnectorLogs200Response> response = apiInstance.GetBusinessAgentConnectorLogsWithHttpInfo(accountId, connectorId, startTime, endTime, limit, toolId, includeStats, summaryOnly, topN);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentConnectorLogsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **connectorId** | **string** |  |  |
| **startTime** | **int?** | Unix seconds. | [optional]  |
| **endTime** | **int?** | Unix seconds. | [optional]  |
| **limit** | **int?** |  | [optional]  |
| **toolId** | **string?** |  | [optional]  |
| **includeStats** | **bool?** | Add success rate and latency percentiles. | [optional]  |
| **summaryOnly** | **bool?** | Aggregate failure patterns instead of entries. | [optional]  |
| **topN** | **int?** |  | [optional]  |

### Return type

[**GetBusinessAgentConnectorLogs200Response**](GetBusinessAgentConnectorLogs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Logs |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbusinessagentconnectortool"></a>
# **GetBusinessAgentConnectorTool**
> BusinessAgentConnectorTool GetBusinessAgentConnectorTool (string accountId, string connectorId, string toolId)

Get a connector tool

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
    public class GetBusinessAgentConnectorToolExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var connectorId = "connectorId_example";  // string | 
            var toolId = "toolId_example";  // string | 

            try
            {
                // Get a connector tool
                BusinessAgentConnectorTool result = apiInstance.GetBusinessAgentConnectorTool(accountId, connectorId, toolId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentConnectorTool: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessAgentConnectorToolWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a connector tool
    ApiResponse<BusinessAgentConnectorTool> response = apiInstance.GetBusinessAgentConnectorToolWithHttpInfo(accountId, connectorId, toolId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentConnectorToolWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **connectorId** | **string** |  |  |
| **toolId** | **string** |  |  |

### Return type

[**BusinessAgentConnectorTool**](BusinessAgentConnectorTool.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tool |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbusinessagentevent"></a>
# **GetBusinessAgentEvent**
> BusinessAgentEventStatus GetBusinessAgentEvent (string accountId, string eventId)

Get a business event status

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
    public class GetBusinessAgentEventExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var eventId = "eventId_example";  // string | 

            try
            {
                // Get a business event status
                BusinessAgentEventStatus result = apiInstance.GetBusinessAgentEvent(accountId, eventId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessAgentEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a business event status
    ApiResponse<BusinessAgentEventStatus> response = apiInstance.GetBusinessAgentEventWithHttpInfo(accountId, eventId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **eventId** | **string** |  |  |

### Return type

[**BusinessAgentEventStatus**](BusinessAgentEventStatus.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Event status |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbusinessagentfaq"></a>
# **GetBusinessAgentFaq**
> BusinessAgentFaq GetBusinessAgentFaq (string accountId, string faqId)

Get a FAQ

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
    public class GetBusinessAgentFaqExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var faqId = "faqId_example";  // string | 

            try
            {
                // Get a FAQ
                BusinessAgentFaq result = apiInstance.GetBusinessAgentFaq(accountId, faqId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentFaq: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessAgentFaqWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a FAQ
    ApiResponse<BusinessAgentFaq> response = apiInstance.GetBusinessAgentFaqWithHttpInfo(accountId, faqId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentFaqWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **faqId** | **string** |  |  |

### Return type

[**BusinessAgentFaq**](BusinessAgentFaq.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | FAQ |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbusinessagentfile"></a>
# **GetBusinessAgentFile**
> BusinessAgentKnowledgeFile GetBusinessAgentFile (string accountId, string fileId)

Get a knowledge file

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
    public class GetBusinessAgentFileExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var fileId = "fileId_example";  // string | 

            try
            {
                // Get a knowledge file
                BusinessAgentKnowledgeFile result = apiInstance.GetBusinessAgentFile(accountId, fileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessAgentFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a knowledge file
    ApiResponse<BusinessAgentKnowledgeFile> response = apiInstance.GetBusinessAgentFileWithHttpInfo(accountId, fileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **fileId** | **string** |  |  |

### Return type

[**BusinessAgentKnowledgeFile**](BusinessAgentKnowledgeFile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | File |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbusinessagentskill"></a>
# **GetBusinessAgentSkill**
> BusinessAgentSkill GetBusinessAgentSkill (string accountId, string skillId)

Get a skill

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
    public class GetBusinessAgentSkillExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var skillId = "skillId_example";  // string | 

            try
            {
                // Get a skill
                BusinessAgentSkill result = apiInstance.GetBusinessAgentSkill(accountId, skillId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentSkill: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessAgentSkillWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a skill
    ApiResponse<BusinessAgentSkill> response = apiInstance.GetBusinessAgentSkillWithHttpInfo(accountId, skillId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentSkillWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **skillId** | **string** |  |  |

### Return type

[**BusinessAgentSkill**](BusinessAgentSkill.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Skill |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbusinessagentstatus"></a>
# **GetBusinessAgentStatus**
> BusinessAgentStatus GetBusinessAgentStatus (string accountId)

Get agent setup status

One read that says where the merchant is: whether the number is eligible, whether the Meta Business Agent terms are accepted, whether an agent exists, whether it is on, and its settings. `manualSteps` lists what Zernio can verify is still pending (accepting the terms in WhatsApp Manager); `unverifiedSteps` lists what Meta exposes no state for (the payment method in Billing Hub). Never fails for those pre-setup states; it reports them as flags. 

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
    public class GetBusinessAgentStatusExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).

            try
            {
                // Get agent setup status
                BusinessAgentStatus result = apiInstance.GetBusinessAgentStatus(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessAgentStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get agent setup status
    ApiResponse<BusinessAgentStatus> response = apiInstance.GetBusinessAgentStatusWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |

### Return type

[**BusinessAgentStatus**](BusinessAgentStatus.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Setup status |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbusinessagentuiskill"></a>
# **GetBusinessAgentUiSkill**
> BusinessAgentUiSkill GetBusinessAgentUiSkill (string accountId, string uiSkillId)

Get a UI skill

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
    public class GetBusinessAgentUiSkillExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var uiSkillId = "uiSkillId_example";  // string | 

            try
            {
                // Get a UI skill
                BusinessAgentUiSkill result = apiInstance.GetBusinessAgentUiSkill(accountId, uiSkillId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentUiSkill: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessAgentUiSkillWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a UI skill
    ApiResponse<BusinessAgentUiSkill> response = apiInstance.GetBusinessAgentUiSkillWithHttpInfo(accountId, uiSkillId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentUiSkillWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **uiSkillId** | **string** |  |  |

### Return type

[**BusinessAgentUiSkill**](BusinessAgentUiSkill.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | UI skill |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbusinessagentwebsite"></a>
# **GetBusinessAgentWebsite**
> BusinessAgentWebsite GetBusinessAgentWebsite (string accountId, string websiteId)

Get a crawled website

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
    public class GetBusinessAgentWebsiteExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var websiteId = "websiteId_example";  // string | 

            try
            {
                // Get a crawled website
                BusinessAgentWebsite result = apiInstance.GetBusinessAgentWebsite(accountId, websiteId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentWebsite: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessAgentWebsiteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a crawled website
    ApiResponse<BusinessAgentWebsite> response = apiInstance.GetBusinessAgentWebsiteWithHttpInfo(accountId, websiteId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.GetBusinessAgentWebsiteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **websiteId** | **string** |  |  |

### Return type

[**BusinessAgentWebsite**](BusinessAgentWebsite.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Website |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbusinessagentallowlist"></a>
# **ListBusinessAgentAllowlist**
> ListBusinessAgentAllowlist200Response ListBusinessAgentAllowlist (string accountId)

List allowlisted consumers

Consumers the agent answers while `ai_audience` is ALLOWLISTED_ONLY.

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
    public class ListBusinessAgentAllowlistExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).

            try
            {
                // List allowlisted consumers
                ListBusinessAgentAllowlist200Response result = apiInstance.ListBusinessAgentAllowlist(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentAllowlist: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBusinessAgentAllowlistWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List allowlisted consumers
    ApiResponse<ListBusinessAgentAllowlist200Response> response = apiInstance.ListBusinessAgentAllowlistWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentAllowlistWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |

### Return type

[**ListBusinessAgentAllowlist200Response**](ListBusinessAgentAllowlist200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Allowlist |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbusinessagentconnectortools"></a>
# **ListBusinessAgentConnectorTools**
> ListBusinessAgentConnectorTools200Response ListBusinessAgentConnectorTools (string accountId, string connectorId)

List connector tools

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
    public class ListBusinessAgentConnectorToolsExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var connectorId = "connectorId_example";  // string | 

            try
            {
                // List connector tools
                ListBusinessAgentConnectorTools200Response result = apiInstance.ListBusinessAgentConnectorTools(accountId, connectorId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentConnectorTools: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBusinessAgentConnectorToolsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List connector tools
    ApiResponse<ListBusinessAgentConnectorTools200Response> response = apiInstance.ListBusinessAgentConnectorToolsWithHttpInfo(accountId, connectorId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentConnectorToolsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **connectorId** | **string** |  |  |

### Return type

[**ListBusinessAgentConnectorTools200Response**](ListBusinessAgentConnectorTools200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tools |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbusinessagentconnectors"></a>
# **ListBusinessAgentConnectors**
> ListBusinessAgentConnectors200Response ListBusinessAgentConnectors (string accountId)

List connectors

External APIs the agent may call. `connection_status` says whether Meta can currently reach each one.

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
    public class ListBusinessAgentConnectorsExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).

            try
            {
                // List connectors
                ListBusinessAgentConnectors200Response result = apiInstance.ListBusinessAgentConnectors(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentConnectors: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBusinessAgentConnectorsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List connectors
    ApiResponse<ListBusinessAgentConnectors200Response> response = apiInstance.ListBusinessAgentConnectorsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentConnectorsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |

### Return type

[**ListBusinessAgentConnectors200Response**](ListBusinessAgentConnectors200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connectors |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbusinessagentfaqs"></a>
# **ListBusinessAgentFaqs**
> ListBusinessAgentFaqs200Response ListBusinessAgentFaqs (string accountId)

List FAQs

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
    public class ListBusinessAgentFaqsExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).

            try
            {
                // List FAQs
                ListBusinessAgentFaqs200Response result = apiInstance.ListBusinessAgentFaqs(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentFaqs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBusinessAgentFaqsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List FAQs
    ApiResponse<ListBusinessAgentFaqs200Response> response = apiInstance.ListBusinessAgentFaqsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentFaqsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |

### Return type

[**ListBusinessAgentFaqs200Response**](ListBusinessAgentFaqs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | FAQs |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbusinessagentfiles"></a>
# **ListBusinessAgentFiles**
> ListBusinessAgentFiles200Response ListBusinessAgentFiles (string accountId)

List knowledge files

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
    public class ListBusinessAgentFilesExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).

            try
            {
                // List knowledge files
                ListBusinessAgentFiles200Response result = apiInstance.ListBusinessAgentFiles(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentFiles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBusinessAgentFilesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List knowledge files
    ApiResponse<ListBusinessAgentFiles200Response> response = apiInstance.ListBusinessAgentFilesWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentFilesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |

### Return type

[**ListBusinessAgentFiles200Response**](ListBusinessAgentFiles200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Files |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbusinessagentsettings"></a>
# **ListBusinessAgentSettings**
> ListBusinessAgentSettings200Response ListBusinessAgentSettings (string accountId, string? agentId = null)

List agent settings

Settings of every agent configured on the number (normally one). Pass `agentId` to read one.

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
    public class ListBusinessAgentSettingsExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var agentId = "agentId_example";  // string? |  (optional) 

            try
            {
                // List agent settings
                ListBusinessAgentSettings200Response result = apiInstance.ListBusinessAgentSettings(accountId, agentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentSettings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBusinessAgentSettingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List agent settings
    ApiResponse<ListBusinessAgentSettings200Response> response = apiInstance.ListBusinessAgentSettingsWithHttpInfo(accountId, agentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentSettingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **agentId** | **string?** |  | [optional]  |

### Return type

[**ListBusinessAgentSettings200Response**](ListBusinessAgentSettings200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Settings |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbusinessagentskills"></a>
# **ListBusinessAgentSkills**
> ListBusinessAgentSkills200Response ListBusinessAgentSkills (string accountId)

List skills

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
    public class ListBusinessAgentSkillsExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).

            try
            {
                // List skills
                ListBusinessAgentSkills200Response result = apiInstance.ListBusinessAgentSkills(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentSkills: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBusinessAgentSkillsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List skills
    ApiResponse<ListBusinessAgentSkills200Response> response = apiInstance.ListBusinessAgentSkillsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentSkillsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |

### Return type

[**ListBusinessAgentSkills200Response**](ListBusinessAgentSkills200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Skills |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbusinessagentuiskills"></a>
# **ListBusinessAgentUiSkills**
> ListBusinessAgentUiSkills200Response ListBusinessAgentUiSkills (string accountId, string? before = null, string? after = null, int? limit = null)

List UI skills

Cursor paged; follow `paging.cursors.after` until `paging.next` is absent.

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
    public class ListBusinessAgentUiSkillsExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var before = "before_example";  // string? |  (optional) 
            var after = "after_example";  // string? |  (optional) 
            var limit = 56;  // int? |  (optional) 

            try
            {
                // List UI skills
                ListBusinessAgentUiSkills200Response result = apiInstance.ListBusinessAgentUiSkills(accountId, before, after, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentUiSkills: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBusinessAgentUiSkillsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List UI skills
    ApiResponse<ListBusinessAgentUiSkills200Response> response = apiInstance.ListBusinessAgentUiSkillsWithHttpInfo(accountId, before, after, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentUiSkillsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **before** | **string?** |  | [optional]  |
| **after** | **string?** |  | [optional]  |
| **limit** | **int?** |  | [optional]  |

### Return type

[**ListBusinessAgentUiSkills200Response**](ListBusinessAgentUiSkills200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | UI skills |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbusinessagentwebsites"></a>
# **ListBusinessAgentWebsites**
> ListBusinessAgentWebsites200Response ListBusinessAgentWebsites (string accountId)

List crawled websites

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
    public class ListBusinessAgentWebsitesExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).

            try
            {
                // List crawled websites
                ListBusinessAgentWebsites200Response result = apiInstance.ListBusinessAgentWebsites(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentWebsites: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBusinessAgentWebsitesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List crawled websites
    ApiResponse<ListBusinessAgentWebsites200Response> response = apiInstance.ListBusinessAgentWebsitesWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.ListBusinessAgentWebsitesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |

### Return type

[**ListBusinessAgentWebsites200Response**](ListBusinessAgentWebsites200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Websites |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="onboardbusinessagent"></a>
# **OnboardBusinessAgent**
> OnboardBusinessAgent201Response OnboardBusinessAgent (string accountId)

Create the agent

Creates the Meta Business Agent on the number and schedules Meta's data preparation. Requires the terms to be accepted; eligibility is checked first and an ineligible number answers 403 `business_agent_not_eligible`. Not idempotent: call it once, then configure knowledge and skills, then enable it through the settings. Configuration calls made in the first minute can still answer `business_agent_not_found` while Meta prepares the workspace. 

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
    public class OnboardBusinessAgentExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).

            try
            {
                // Create the agent
                OnboardBusinessAgent201Response result = apiInstance.OnboardBusinessAgent(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.OnboardBusinessAgent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OnboardBusinessAgentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create the agent
    ApiResponse<OnboardBusinessAgent201Response> response = apiInstance.OnboardBusinessAgentWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.OnboardBusinessAgentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |

### Return type

[**OnboardBusinessAgent201Response**](OnboardBusinessAgent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Agent created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |
| **409** | Meta rejected the state change (code business_agent_conflict). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="readbusinessagentevals"></a>
# **ReadBusinessAgentEvals**
> Dictionary&lt;string, Object&gt; ReadBusinessAgentEvals (string accountId, string? jobId = null, string? summaryIds = null, string? evalIds = null)

Read evaluation data

Without query parameters, lists the evaluation scenarios (`eval_cases`). With `jobId`, polls a run started with POST. With `summaryIds`, returns the aggregated insight reports. With `evalIds`, returns per-conversation evaluation details. One of the three at a time. 

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
    public class ReadBusinessAgentEvalsExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var jobId = "jobId_example";  // string? |  (optional) 
            var summaryIds = "summaryIds_example";  // string? | Comma-separated summary ids. (optional) 
            var evalIds = "evalIds_example";  // string? | Comma-separated evaluation ids. (optional) 

            try
            {
                // Read evaluation data
                Dictionary<string, Object> result = apiInstance.ReadBusinessAgentEvals(accountId, jobId, summaryIds, evalIds);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.ReadBusinessAgentEvals: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReadBusinessAgentEvalsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read evaluation data
    ApiResponse<Dictionary<string, Object>> response = apiInstance.ReadBusinessAgentEvalsWithHttpInfo(accountId, jobId, summaryIds, evalIds);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.ReadBusinessAgentEvalsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **jobId** | **string?** |  | [optional]  |
| **summaryIds** | **string?** | Comma-separated summary ids. | [optional]  |
| **evalIds** | **string?** | Comma-separated evaluation ids. | [optional]  |

### Return type

**Dictionary<string, Object>**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Evaluation data as Meta returns it for the selected read |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="refreshbusinessagentconnectortools"></a>
# **RefreshBusinessAgentConnectorTools**
> BusinessAgentConnector RefreshBusinessAgentConnectorTools (string accountId, string connectorId)

Refresh MCP connector tools

Re-discovers the tools of an MCP connector. A failed discovery keeps the previous tool set and reports an ERROR sync status inside a 200.

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
    public class RefreshBusinessAgentConnectorToolsExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var connectorId = "connectorId_example";  // string | 

            try
            {
                // Refresh MCP connector tools
                BusinessAgentConnector result = apiInstance.RefreshBusinessAgentConnectorTools(accountId, connectorId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.RefreshBusinessAgentConnectorTools: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefreshBusinessAgentConnectorToolsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Refresh MCP connector tools
    ApiResponse<BusinessAgentConnector> response = apiInstance.RefreshBusinessAgentConnectorToolsWithHttpInfo(accountId, connectorId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.RefreshBusinessAgentConnectorToolsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **connectorId** | **string** |  |  |

### Return type

[**BusinessAgentConnector**](BusinessAgentConnector.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connector with updated tool sync metadata |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removebusinessagentallowlistentry"></a>
# **RemoveBusinessAgentAllowlistEntry**
> InlineObject RemoveBusinessAgentAllowlistEntry (string accountId, string entryId)

Remove an allowlisted consumer

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
    public class RemoveBusinessAgentAllowlistEntryExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var entryId = "entryId_example";  // string | 

            try
            {
                // Remove an allowlisted consumer
                InlineObject result = apiInstance.RemoveBusinessAgentAllowlistEntry(accountId, entryId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.RemoveBusinessAgentAllowlistEntry: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveBusinessAgentAllowlistEntryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove an allowlisted consumer
    ApiResponse<InlineObject> response = apiInstance.RemoveBusinessAgentAllowlistEntryWithHttpInfo(accountId, entryId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.RemoveBusinessAgentAllowlistEntryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **entryId** | **string** |  |  |

### Return type

[**InlineObject**](InlineObject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="replacebusinessagentbudget"></a>
# **ReplaceBusinessAgentBudget**
> GetBusinessAgentBudget200Response ReplaceBusinessAgentBudget (string accountId, GetBusinessAgentBudget200Response getBusinessAgentBudget200Response)

Replace usage budgets

The full desired set: budgets left out are removed, an empty list returns to unlimited. Pass `budget_id` to edit one in place. When a cap is hit the agent finishes its turn, stops answering and hands the thread to a human until the window rolls over.

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
    public class ReplaceBusinessAgentBudgetExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var getBusinessAgentBudget200Response = new GetBusinessAgentBudget200Response(); // GetBusinessAgentBudget200Response | 

            try
            {
                // Replace usage budgets
                GetBusinessAgentBudget200Response result = apiInstance.ReplaceBusinessAgentBudget(accountId, getBusinessAgentBudget200Response);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.ReplaceBusinessAgentBudget: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReplaceBusinessAgentBudgetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Replace usage budgets
    ApiResponse<GetBusinessAgentBudget200Response> response = apiInstance.ReplaceBusinessAgentBudgetWithHttpInfo(accountId, getBusinessAgentBudget200Response);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.ReplaceBusinessAgentBudgetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **getBusinessAgentBudget200Response** | [**GetBusinessAgentBudget200Response**](GetBusinessAgentBudget200Response.md) |  |  |

### Return type

[**GetBusinessAgentBudget200Response**](GetBusinessAgentBudget200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Budgets after the update |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="replacebusinessagentbusinessinformation"></a>
# **ReplaceBusinessAgentBusinessInformation**
> BusinessAgentBusinessInformation ReplaceBusinessAgentBusinessInformation (string accountId, BusinessAgentBusinessInformation businessAgentBusinessInformation)

Replace business information

Full replacement: every field you send overwrites the stored value; fields you omit are cleared.

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
    public class ReplaceBusinessAgentBusinessInformationExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var businessAgentBusinessInformation = new BusinessAgentBusinessInformation(); // BusinessAgentBusinessInformation | 

            try
            {
                // Replace business information
                BusinessAgentBusinessInformation result = apiInstance.ReplaceBusinessAgentBusinessInformation(accountId, businessAgentBusinessInformation);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.ReplaceBusinessAgentBusinessInformation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReplaceBusinessAgentBusinessInformationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Replace business information
    ApiResponse<BusinessAgentBusinessInformation> response = apiInstance.ReplaceBusinessAgentBusinessInformationWithHttpInfo(accountId, businessAgentBusinessInformation);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.ReplaceBusinessAgentBusinessInformationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **businessAgentBusinessInformation** | [**BusinessAgentBusinessInformation**](BusinessAgentBusinessInformation.md) |  |  |

### Return type

[**BusinessAgentBusinessInformation**](BusinessAgentBusinessInformation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Stored business information |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="resetbusinessagentbusinessinformation"></a>
# **ResetBusinessAgentBusinessInformation**
> InlineObject ResetBusinessAgentBusinessInformation (string accountId)

Reset business information

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
    public class ResetBusinessAgentBusinessInformationExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).

            try
            {
                // Reset business information
                InlineObject result = apiInstance.ResetBusinessAgentBusinessInformation(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.ResetBusinessAgentBusinessInformation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResetBusinessAgentBusinessInformationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reset business information
    ApiResponse<InlineObject> response = apiInstance.ResetBusinessAgentBusinessInformationWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.ResetBusinessAgentBusinessInformationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |

### Return type

[**InlineObject**](InlineObject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="runbusinessagentconnectortool"></a>
# **RunBusinessAgentConnectorTool**
> RunBusinessAgentConnectorTool200Response RunBusinessAgentConnectorTool (string accountId, string connectorId, string toolId, RunBusinessAgentConnectorToolRequest runBusinessAgentConnectorToolRequest)

Run a connector tool once

Executes the tool against the merchant API and returns the raw upstream result, to check a connector before the agent relies on it.

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
    public class RunBusinessAgentConnectorToolExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var connectorId = "connectorId_example";  // string | 
            var toolId = "toolId_example";  // string | 
            var runBusinessAgentConnectorToolRequest = new RunBusinessAgentConnectorToolRequest(); // RunBusinessAgentConnectorToolRequest | 

            try
            {
                // Run a connector tool once
                RunBusinessAgentConnectorTool200Response result = apiInstance.RunBusinessAgentConnectorTool(accountId, connectorId, toolId, runBusinessAgentConnectorToolRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.RunBusinessAgentConnectorTool: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RunBusinessAgentConnectorToolWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Run a connector tool once
    ApiResponse<RunBusinessAgentConnectorTool200Response> response = apiInstance.RunBusinessAgentConnectorToolWithHttpInfo(accountId, connectorId, toolId, runBusinessAgentConnectorToolRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.RunBusinessAgentConnectorToolWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **connectorId** | **string** |  |  |
| **toolId** | **string** |  |  |
| **runBusinessAgentConnectorToolRequest** | [**RunBusinessAgentConnectorToolRequest**](RunBusinessAgentConnectorToolRequest.md) |  |  |

### Return type

[**RunBusinessAgentConnectorTool200Response**](RunBusinessAgentConnectorTool200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tool result |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sendbusinessagentevent"></a>
# **SendBusinessAgentEvent**
> SendBusinessAgentEvent202Response SendBusinessAgentEvent (string accountId, SendBusinessAgentEventRequest sendBusinessAgentEventRequest)

Send a business event

Tell the agent something happened in your systems (order shipped, document verified) so it messages the consumer about it. The consumer must already have a conversation with the number. Answers 202 with the event id; poll it for the outcome.

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
    public class SendBusinessAgentEventExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var sendBusinessAgentEventRequest = new SendBusinessAgentEventRequest(); // SendBusinessAgentEventRequest | 

            try
            {
                // Send a business event
                SendBusinessAgentEvent202Response result = apiInstance.SendBusinessAgentEvent(accountId, sendBusinessAgentEventRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.SendBusinessAgentEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendBusinessAgentEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send a business event
    ApiResponse<SendBusinessAgentEvent202Response> response = apiInstance.SendBusinessAgentEventWithHttpInfo(accountId, sendBusinessAgentEventRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.SendBusinessAgentEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **sendBusinessAgentEventRequest** | [**SendBusinessAgentEventRequest**](SendBusinessAgentEventRequest.md) |  |  |

### Return type

[**SendBusinessAgentEvent202Response**](SendBusinessAgentEvent202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Event accepted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sendbusinessagenttestmessage"></a>
# **SendBusinessAgentTestMessage**
> BusinessAgentTestMessageResponse SendBusinessAgentTestMessage (string accountId, SendBusinessAgentTestMessageRequest sendBusinessAgentTestMessageRequest)

Send a test message

Runs the message through the full agent pipeline in Meta sandbox with no WhatsApp user and no token billing. Pass back `conversationId` to continue a thread. Meta rate-limits it per number per hour.

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
    public class SendBusinessAgentTestMessageExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var sendBusinessAgentTestMessageRequest = new SendBusinessAgentTestMessageRequest(); // SendBusinessAgentTestMessageRequest | 

            try
            {
                // Send a test message
                BusinessAgentTestMessageResponse result = apiInstance.SendBusinessAgentTestMessage(accountId, sendBusinessAgentTestMessageRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.SendBusinessAgentTestMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendBusinessAgentTestMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send a test message
    ApiResponse<BusinessAgentTestMessageResponse> response = apiInstance.SendBusinessAgentTestMessageWithHttpInfo(accountId, sendBusinessAgentTestMessageRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.SendBusinessAgentTestMessageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **sendBusinessAgentTestMessageRequest** | [**SendBusinessAgentTestMessageRequest**](SendBusinessAgentTestMessageRequest.md) |  |  |

### Return type

[**BusinessAgentTestMessageResponse**](BusinessAgentTestMessageResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Agent reply |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |
| **429** | Meta hourly test-message limit reached (code rate_limited, Retry-After when known). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setbusinessagentconnectorcredentials"></a>
# **SetBusinessAgentConnectorCredentials**
> BusinessAgentConnector SetBusinessAgentConnectorCredentials (string accountId, string connectorId, SetBusinessAgentConnectorCredentialsRequest setBusinessAgentConnectorCredentialsRequest)

Set connector credentials

Set or rotate the connector's credentials in place: `kind: api_key`, `kind: oauth` (client credentials) or `kind: certificate` (mTLS client certificate). Meta has no call that removes a credential layer; change the connector's `auth_type` or delete it instead. 

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
    public class SetBusinessAgentConnectorCredentialsExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var connectorId = "connectorId_example";  // string | 
            var setBusinessAgentConnectorCredentialsRequest = new SetBusinessAgentConnectorCredentialsRequest(); // SetBusinessAgentConnectorCredentialsRequest | 

            try
            {
                // Set connector credentials
                BusinessAgentConnector result = apiInstance.SetBusinessAgentConnectorCredentials(accountId, connectorId, setBusinessAgentConnectorCredentialsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.SetBusinessAgentConnectorCredentials: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetBusinessAgentConnectorCredentialsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set connector credentials
    ApiResponse<BusinessAgentConnector> response = apiInstance.SetBusinessAgentConnectorCredentialsWithHttpInfo(accountId, connectorId, setBusinessAgentConnectorCredentialsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.SetBusinessAgentConnectorCredentialsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **connectorId** | **string** |  |  |
| **setBusinessAgentConnectorCredentialsRequest** | [**SetBusinessAgentConnectorCredentialsRequest**](SetBusinessAgentConnectorCredentialsRequest.md) |  |  |

### Return type

[**BusinessAgentConnector**](BusinessAgentConnector.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connector with the new credential metadata |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="startbusinessagentevalrun"></a>
# **StartBusinessAgentEvalRun**
> StartBusinessAgentEvalRun202Response StartBusinessAgentEvalRun (string accountId, StartBusinessAgentEvalRunRequest startBusinessAgentEvalRunRequest)

Start an evaluation run

Simulates the given scenarios against the agent and scores them. Answers 202 with a `job_id` to poll with GET.

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
    public class StartBusinessAgentEvalRunExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var startBusinessAgentEvalRunRequest = new StartBusinessAgentEvalRunRequest(); // StartBusinessAgentEvalRunRequest | 

            try
            {
                // Start an evaluation run
                StartBusinessAgentEvalRun202Response result = apiInstance.StartBusinessAgentEvalRun(accountId, startBusinessAgentEvalRunRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.StartBusinessAgentEvalRun: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the StartBusinessAgentEvalRunWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Start an evaluation run
    ApiResponse<StartBusinessAgentEvalRun202Response> response = apiInstance.StartBusinessAgentEvalRunWithHttpInfo(accountId, startBusinessAgentEvalRunRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.StartBusinessAgentEvalRunWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **startBusinessAgentEvalRunRequest** | [**StartBusinessAgentEvalRunRequest**](StartBusinessAgentEvalRunRequest.md) |  |  |

### Return type

[**StartBusinessAgentEvalRun202Response**](StartBusinessAgentEvalRun202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Run started |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatebusinessagentconnector"></a>
# **UpdateBusinessAgentConnector**
> BusinessAgentConnector UpdateBusinessAgentConnector (string accountId, string connectorId, BusinessAgentConnectorInput businessAgentConnectorInput)

Update a connector

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
    public class UpdateBusinessAgentConnectorExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var connectorId = "connectorId_example";  // string | 
            var businessAgentConnectorInput = new BusinessAgentConnectorInput(); // BusinessAgentConnectorInput | 

            try
            {
                // Update a connector
                BusinessAgentConnector result = apiInstance.UpdateBusinessAgentConnector(accountId, connectorId, businessAgentConnectorInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentConnector: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBusinessAgentConnectorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a connector
    ApiResponse<BusinessAgentConnector> response = apiInstance.UpdateBusinessAgentConnectorWithHttpInfo(accountId, connectorId, businessAgentConnectorInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentConnectorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **connectorId** | **string** |  |  |
| **businessAgentConnectorInput** | [**BusinessAgentConnectorInput**](BusinessAgentConnectorInput.md) |  |  |

### Return type

[**BusinessAgentConnector**](BusinessAgentConnector.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connector updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatebusinessagentconnectortool"></a>
# **UpdateBusinessAgentConnectorTool**
> BusinessAgentConnectorTool UpdateBusinessAgentConnectorTool (string accountId, string connectorId, string toolId, BusinessAgentConnectorToolInput businessAgentConnectorToolInput)

Update a connector tool

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
    public class UpdateBusinessAgentConnectorToolExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var connectorId = "connectorId_example";  // string | 
            var toolId = "toolId_example";  // string | 
            var businessAgentConnectorToolInput = new BusinessAgentConnectorToolInput(); // BusinessAgentConnectorToolInput | 

            try
            {
                // Update a connector tool
                BusinessAgentConnectorTool result = apiInstance.UpdateBusinessAgentConnectorTool(accountId, connectorId, toolId, businessAgentConnectorToolInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentConnectorTool: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBusinessAgentConnectorToolWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a connector tool
    ApiResponse<BusinessAgentConnectorTool> response = apiInstance.UpdateBusinessAgentConnectorToolWithHttpInfo(accountId, connectorId, toolId, businessAgentConnectorToolInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentConnectorToolWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **connectorId** | **string** |  |  |
| **toolId** | **string** |  |  |
| **businessAgentConnectorToolInput** | [**BusinessAgentConnectorToolInput**](BusinessAgentConnectorToolInput.md) |  |  |

### Return type

[**BusinessAgentConnectorTool**](BusinessAgentConnectorTool.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tool updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatebusinessagentfaq"></a>
# **UpdateBusinessAgentFaq**
> BusinessAgentFaq UpdateBusinessAgentFaq (string accountId, string faqId, BusinessAgentFaqInput businessAgentFaqInput)

Update a FAQ

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
    public class UpdateBusinessAgentFaqExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var faqId = "faqId_example";  // string | 
            var businessAgentFaqInput = new BusinessAgentFaqInput(); // BusinessAgentFaqInput | 

            try
            {
                // Update a FAQ
                BusinessAgentFaq result = apiInstance.UpdateBusinessAgentFaq(accountId, faqId, businessAgentFaqInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentFaq: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBusinessAgentFaqWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a FAQ
    ApiResponse<BusinessAgentFaq> response = apiInstance.UpdateBusinessAgentFaqWithHttpInfo(accountId, faqId, businessAgentFaqInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentFaqWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **faqId** | **string** |  |  |
| **businessAgentFaqInput** | [**BusinessAgentFaqInput**](BusinessAgentFaqInput.md) |  |  |

### Return type

[**BusinessAgentFaq**](BusinessAgentFaq.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | FAQ updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatebusinessagentsettings"></a>
# **UpdateBusinessAgentSettings**
> BusinessAgentSettings UpdateBusinessAgentSettings (string accountId, UpdateBusinessAgentSettingsRequest updateBusinessAgentSettingsRequest, string? agentId = null)

Update agent settings

Partial update: fields you omit keep their value. `rollout.enabled: true` turns the agent on for new conversations; `false` stops it on every thread. Turning it on for `EVERYONE` needs a payment method on the Business Agent billable account (Meta accepts the call but delivers nothing without one); `ALLOWLISTED_ONLY` does not, which is how you test with a few numbers before billing. `never_say_phrases` replaces the whole list. 

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
    public class UpdateBusinessAgentSettingsExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var updateBusinessAgentSettingsRequest = new UpdateBusinessAgentSettingsRequest(); // UpdateBusinessAgentSettingsRequest | 
            var agentId = "agentId_example";  // string? |  (optional) 

            try
            {
                // Update agent settings
                BusinessAgentSettings result = apiInstance.UpdateBusinessAgentSettings(accountId, updateBusinessAgentSettingsRequest, agentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentSettings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBusinessAgentSettingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update agent settings
    ApiResponse<BusinessAgentSettings> response = apiInstance.UpdateBusinessAgentSettingsWithHttpInfo(accountId, updateBusinessAgentSettingsRequest, agentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentSettingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **updateBusinessAgentSettingsRequest** | [**UpdateBusinessAgentSettingsRequest**](UpdateBusinessAgentSettingsRequest.md) |  |  |
| **agentId** | **string?** |  | [optional]  |

### Return type

[**BusinessAgentSettings**](BusinessAgentSettings.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated settings |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatebusinessagentskill"></a>
# **UpdateBusinessAgentSkill**
> BusinessAgentSkill UpdateBusinessAgentSkill (string accountId, string skillId, BusinessAgentSkillInput businessAgentSkillInput)

Update a skill

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
    public class UpdateBusinessAgentSkillExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var skillId = "skillId_example";  // string | 
            var businessAgentSkillInput = new BusinessAgentSkillInput(); // BusinessAgentSkillInput | 

            try
            {
                // Update a skill
                BusinessAgentSkill result = apiInstance.UpdateBusinessAgentSkill(accountId, skillId, businessAgentSkillInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentSkill: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBusinessAgentSkillWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a skill
    ApiResponse<BusinessAgentSkill> response = apiInstance.UpdateBusinessAgentSkillWithHttpInfo(accountId, skillId, businessAgentSkillInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentSkillWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **skillId** | **string** |  |  |
| **businessAgentSkillInput** | [**BusinessAgentSkillInput**](BusinessAgentSkillInput.md) |  |  |

### Return type

[**BusinessAgentSkill**](BusinessAgentSkill.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Skill updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatebusinessagentuiskill"></a>
# **UpdateBusinessAgentUiSkill**
> BusinessAgentUiSkill UpdateBusinessAgentUiSkill (string accountId, string uiSkillId, BusinessAgentUiSkillInput businessAgentUiSkillInput)

Update a UI skill

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
    public class UpdateBusinessAgentUiSkillExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var uiSkillId = "uiSkillId_example";  // string | 
            var businessAgentUiSkillInput = new BusinessAgentUiSkillInput(); // BusinessAgentUiSkillInput | 

            try
            {
                // Update a UI skill
                BusinessAgentUiSkill result = apiInstance.UpdateBusinessAgentUiSkill(accountId, uiSkillId, businessAgentUiSkillInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentUiSkill: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBusinessAgentUiSkillWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a UI skill
    ApiResponse<BusinessAgentUiSkill> response = apiInstance.UpdateBusinessAgentUiSkillWithHttpInfo(accountId, uiSkillId, businessAgentUiSkillInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentUiSkillWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **uiSkillId** | **string** |  |  |
| **businessAgentUiSkillInput** | [**BusinessAgentUiSkillInput**](BusinessAgentUiSkillInput.md) |  |  |

### Return type

[**BusinessAgentUiSkill**](BusinessAgentUiSkill.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | UI skill updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatebusinessagentwebsite"></a>
# **UpdateBusinessAgentWebsite**
> BusinessAgentWebsite UpdateBusinessAgentWebsite (string accountId, string websiteId, BusinessAgentWebsiteInput businessAgentWebsiteInput)

Update a crawled website

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
    public class UpdateBusinessAgentWebsiteExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var websiteId = "websiteId_example";  // string | 
            var businessAgentWebsiteInput = new BusinessAgentWebsiteInput(); // BusinessAgentWebsiteInput | 

            try
            {
                // Update a crawled website
                BusinessAgentWebsite result = apiInstance.UpdateBusinessAgentWebsite(accountId, websiteId, businessAgentWebsiteInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentWebsite: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBusinessAgentWebsiteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a crawled website
    ApiResponse<BusinessAgentWebsite> response = apiInstance.UpdateBusinessAgentWebsiteWithHttpInfo(accountId, websiteId, businessAgentWebsiteInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.UpdateBusinessAgentWebsiteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **websiteId** | **string** |  |  |
| **businessAgentWebsiteInput** | [**BusinessAgentWebsiteInput**](BusinessAgentWebsiteInput.md) |  |  |

### Return type

[**BusinessAgentWebsite**](BusinessAgentWebsite.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Website updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="uploadbusinessagentfile"></a>
# **UploadBusinessAgentFile**
> BusinessAgentKnowledgeFile UploadBusinessAgentFile (string accountId, UploadBusinessAgentFileRequest uploadBusinessAgentFileRequest)

Upload a knowledge file

Accepted types: pdf, doc, docx, png, jpg, jpeg, plus csv and xlsx when Meta enabled extraction on the asset. Meta's limit is 100 MB. Two ways to send the file: - JSON `{ url, fileName }`: Zernio downloads the file (public https URL, no redirects,   capped at 100 MB) and forwards it. Use this for anything above a few megabytes. - multipart form-data with a `file` part (and an optional `fileName`): bounded by the   request body limit of about 4.5 MB; larger uploads must use the `url` form. Not idempotent. 

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
    public class UploadBusinessAgentFileExample
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
            var apiInstance = new BusinessAgentApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account id (the number must be managed through the Cloud API).
            var uploadBusinessAgentFileRequest = new UploadBusinessAgentFileRequest(); // UploadBusinessAgentFileRequest | 

            try
            {
                // Upload a knowledge file
                BusinessAgentKnowledgeFile result = apiInstance.UploadBusinessAgentFile(accountId, uploadBusinessAgentFileRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessAgentApi.UploadBusinessAgentFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadBusinessAgentFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload a knowledge file
    ApiResponse<BusinessAgentKnowledgeFile> response = apiInstance.UploadBusinessAgentFileWithHttpInfo(accountId, uploadBusinessAgentFileRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessAgentApi.UploadBusinessAgentFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account id (the number must be managed through the Cloud API). |  |
| **uploadBusinessAgentFileRequest** | [**UploadBusinessAgentFileRequest**](UploadBusinessAgentFileRequest.md) |  |  |

### Return type

[**BusinessAgentKnowledgeFile**](BusinessAgentKnowledgeFile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json, multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | File uploaded |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox add-on required, the WhatsApp token lacks the Business Agent permissions (code reconnect_required), or the merchant has not accepted the Meta Business Agent terms in WhatsApp Manager (code business_agent_terms_not_accepted). |  -  |
| **404** | Account not found, or no agent exists on the number yet or the referenced item does not exist (code business_agent_not_found). |  -  |
| **413** | File larger than 100 MB (code payload_too_large). A multipart body above the request limit is rejected by the host before the route runs. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

