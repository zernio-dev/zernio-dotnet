# Zernio.Model.GetAutomationCatalog200ResponseTriggersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Kind** | **string** |  | 
**Group** | **string** | Where a trigger picker files it: the same groups as the template marketplace. | 
**ResourceGroup** | **string** | The API key resource group its kind needs to create one. | 
**Type** | **string** | &#x60;schedule&#x60;, &#x60;enrollment&#x60;, a comment door such as &#x60;comment.keyword&#x60; (comment to DM), a flow trigger such as &#x60;inbound_message&#x60;, or the Zernio event name. | 
**Label** | **string** | Its short name, such as &#x60;Ad rule schedule&#x60;. | 
**Description** | **string** | One line on when it starts and what the automation does then. | 
**Subject** | **string** | What an event is about, such as &#x60;post&#x60; or &#x60;account&#x60;. | [optional] 
**Scope** | **Object** | Which of &#x60;profileId&#x60;, &#x60;accountId&#x60;, &#x60;accountIds&#x60; and &#x60;platformPostId&#x60; the trigger needs. | [optional] 
**Platforms** | **List&lt;string&gt;** | The platforms a sequence, comment to DM or flow trigger runs on. | [optional] 
**Facts** | [**List&lt;GetAutomationCatalog200ResponseTriggersInnerFactsInner&gt;**](GetAutomationCatalog200ResponseTriggersInnerFactsInner.md) | The facts a &#x60;filter&#x60; can compare, for an event trigger. | [optional] 
**Subjects** | **List&lt;Object&gt;** | Scheduled trigger only: what it can check (&#x60;post&#x60;), with the facts of each. | [optional] 
**Every** | **List&lt;string&gt;** |  | [optional] 
**Times** | **Object** | Ad rule trigger only: the weekly set times it takes. | [optional] 
**FilterOperators** | **List&lt;string&gt;** |  | [optional] 
**Steps** | **List&lt;string&gt;** | The step types allowed after the trigger. For an event, only those its subject can reach. | 
**Boost** | **Object** | Scheduled trigger only: the platforms, goals, most days and most boosts a day of &#x60;ads.boost_post&#x60;. | [optional] 
**Limits** | **List&lt;string&gt;** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

