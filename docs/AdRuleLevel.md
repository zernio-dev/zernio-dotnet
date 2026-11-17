# Zernio.Model.AdRuleLevel
Whether the rule checks campaigns, ad sets, single ads, Google keywords or Google search terms. Each one is evaluated on its own.  `keyword` and `search_term` read Google Search, on Google Ads accounts only. A keyword's id is `<adGroupId>~<criterionId>`, as `PATCH /v1/ads/keywords/{keywordId}` takes it. A search term is one per ad group, its id `<adGroupId>~<term>`.  - They read a daily history Zernio fetches from Google. A day keeps its 50,000 rows that spent most. - Every daily window works, `today` included: today is refreshed at most once an hour. - A new rule's first runs load its days a few at a time, and fail until all are in. - A keyword rule judges every serving keyword, one with no traffic at zero. Paused keywords are not judged. - Google lists only search terms that showed at least once, so a search term rule takes `impressions` with `>` or `>=`, never `<` or `<=`.  They take `spend`, `impressions`, `clicks`, `conversions`, `ctr`, `cpc`, `cpm`, `cpa` and `roas` over whole days, no `usual`, `of`, `top` or `bottom`, and `compareTo` only as `campaign`. A keyword rule can `notify` or `pause`; a search term rule only notifies. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

