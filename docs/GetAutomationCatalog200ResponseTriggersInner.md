# Zernio.Model.GetAutomationCatalog200ResponseTriggersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Kind** | **string** |  | 
**Type** | **string** | &#x60;schedule&#x60;, or the Zernio event name. | 
**Label** | **string** | Event triggers only. | [optional] 
**Subject** | **string** | What an event is about, such as &#x60;post&#x60; or &#x60;account&#x60;. | [optional] 
**Scope** | **Object** | Which of &#x60;profileId&#x60; and &#x60;accountIds&#x60; an event trigger needs. | [optional] 
**Facts** | [**List&lt;GetAutomationCatalog200ResponseTriggersInnerFactsInner&gt;**](GetAutomationCatalog200ResponseTriggersInnerFactsInner.md) | The facts a &#x60;filter&#x60; can compare, for an event trigger. | [optional] 
**Subjects** | **List&lt;Object&gt;** | Scheduled trigger only: what it can check (&#x60;post&#x60;), with the facts of each. | [optional] 
**Every** | **List&lt;string&gt;** |  | [optional] 
**Times** | **Object** | Ad rule trigger only: the weekly set times it takes. | [optional] 
**FilterOperators** | **List&lt;string&gt;** |  | [optional] 
**Steps** | **List&lt;string&gt;** |  | [optional] 
**Boost** | **Object** | Scheduled trigger only: the platforms, goals, most days and most boosts a day of &#x60;ads.boost_post&#x60;. | [optional] 
**Limits** | **List&lt;string&gt;** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

