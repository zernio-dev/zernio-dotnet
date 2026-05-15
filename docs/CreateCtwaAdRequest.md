# Zernio.Model.CreateCtwaAdRequest
In addition to the `required` list, the request must use EXACTLY ONE of the two shapes:  - Single-creative: `headline`, `body`, and one of   `imageUrl` / `video` (mutually exclusive). - Multi-creative: a non-empty `creatives[]` array. Top-level   `headline` / `body` / `imageUrl` / `video` must NOT be set   on this shape.  The route enforces this at the Zod boundary; OpenAPI's `required` cannot express the OR cleanly. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Facebook or Instagram SocialAccount ID. | 
**AdAccountId** | **string** | Meta ad account ID, e.g. &#x60;act_123456789&#x60;. | 
**Name** | **string** | Ad display name. Used to derive campaign / ad set names. On the multi-creative shape, each ad&#39;s Meta name gets a \&quot; #N\&quot; suffix (1-indexed) so Ads Manager shows them as a numbered batch.  | 
**Headline** | **string** | Single-creative shape only. Mutually exclusive with &#x60;creatives[]&#x60;.  | [optional] 
**Body** | **string** | Primary text shown above the image / video. Single-creative shape only. Mutually exclusive with &#x60;creatives[]&#x60;.  | [optional] 
**ImageUrl** | **string** | Image asset for single-creative shape. Mutually exclusive with &#x60;video&#x60; and with &#x60;creatives[]&#x60;. Required on the single-creative shape if &#x60;video&#x60; is not supplied.  | [optional] 
**Video** | [**CreateCtwaAdRequestVideo**](CreateCtwaAdRequestVideo.md) |  | [optional] 
**Creatives** | [**List&lt;CreateCtwaAdRequestCreativesInner&gt;**](CreateCtwaAdRequestCreativesInner.md) | Multi-creative shape: N CTWA ads under one campaign + one ad set, sharing budget and targeting. Mutually exclusive with the top-level single-creative fields (&#x60;headline&#x60; / &#x60;body&#x60; / &#x60;imageUrl&#x60; / &#x60;video&#x60;). Each entry must supply its own headline, body, and exactly one of &#x60;imageUrl&#x60; / &#x60;video&#x60;.  | [optional] 
**BudgetAmount** | **decimal** | Budget amount in the ad account&#39;s currency major units (e.g. dollars for USD, not cents). Must be &gt; 0.  | 
**BudgetType** | **string** |  | 
**Currency** | **string** | ISO 4217 currency code matching the ad account&#39;s currency (e.g. &#x60;USD&#x60;). Optional; Meta infers from the ad account when omitted.  | [optional] 
**EndDate** | **DateTime** | ISO 8601 datetime. Required when &#x60;budgetType&#x60; is &#x60;lifetime&#x60;.  | [optional] 
**Countries** | **List&lt;string&gt;** | ISO 3166-1 alpha-2 country codes. Defaults to &#x60;[\&quot;US\&quot;]&#x60;. | [optional] 
**AgeMin** | **int** |  | [optional] 
**AgeMax** | **int** |  | [optional] 
**Interests** | [**List&lt;CreateCtwaAdRequestInterestsInner&gt;**](CreateCtwaAdRequestInterestsInner.md) |  | [optional] 
**AudienceId** | **string** | Custom audience ID to target. | [optional] 
**AdvantageAudience** | **int** | Meta&#39;s Advantage+ audience expansion. &#x60;0&#x60; (default) keeps targeting strict; &#x60;1&#x60; lets Meta expand beyond the supplied targeting when its delivery system finds better matches. Always sent on CREATE (Meta requires it).  | [optional] 
**Objective** | **string** | Defaults to &#x60;OUTCOME_ENGAGEMENT&#x60; (the broadly-supported CTWA objective). &#x60;OUTCOME_SALES&#x60; and &#x60;OUTCOME_LEADS&#x60; require additional account configuration (Dataset linked to the WABA for sales) and may be rejected by Meta if missing.  | [optional] 
**BidStrategy** | **string** | Meta bid strategy applied to the shared ad set. Defaults to &#x60;LOWEST_COST_WITHOUT_CAP&#x60; (auto-bid) when omitted. &#x60;LOWEST_COST_WITH_BID_CAP&#x60; and &#x60;COST_CAP&#x60; require &#x60;bidAmount&#x60;. &#x60;LOWEST_COST_WITH_MIN_ROAS&#x60; requires &#x60;roasAverageFloor&#x60;. CTWA&#39;s &#x60;optimization_goal&#x60; is fixed to &#x60;CONVERSATIONS&#x60;, but the bid strategy is independent.  | [optional] 
**BidAmount** | **decimal** | Whole currency units (e.g. &#x60;5&#x60; &#x3D; $5.00 on a USD account). Required when &#x60;bidStrategy&#x60; is &#x60;LOWEST_COST_WITH_BID_CAP&#x60; or &#x60;COST_CAP&#x60;; rejected otherwise.  | [optional] 
**RoasAverageFloor** | **decimal** | Decimal ROAS multiplier (e.g. &#x60;2.0&#x60; &#x3D; 2.0× ROAS floor). Required when &#x60;bidStrategy&#x60; is &#x60;LOWEST_COST_WITH_MIN_ROAS&#x60;; rejected otherwise. Meta enforces its own upper bound server-side.  | [optional] 
**DsaBeneficiary** | **string** | Name of the legal entity benefiting from the ad. Required by Meta when targeting EU users (DSA Article 26). Not enforced at schema level; enforced server-side when targeting intersects EU member states.  | [optional] 
**DsaPayor** | **string** | Name of the legal entity paying for the ad. Required by Meta when targeting EU users (DSA Article 26). Note Meta API spelling: dsa_payor (not dsa_payer).  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

