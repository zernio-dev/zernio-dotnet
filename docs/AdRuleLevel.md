# Zernio.Model.AdRuleLevel
Whether the rule checks campaigns, ad sets, single ads, Google keywords or Google search terms. Each one is evaluated on its own.  `keyword` and `search_term` read Google Search, on Google Ads accounts only. A keyword's id is `<adGroupId>~<criterionId>`, as `PATCH /v1/ads/keywords/{keywordId}` takes it. A search term is judged once per campaign, summed across the ad groups it showed in, its id `<campaignId>~<term>`.  - They read a daily history Zernio fetches from Google. A day keeps its 50,000 rows that spent most. - Every daily window works, `today` included: today is refreshed at most once an hour. - The history starts loading when the rule is saved, about 10 days a minute. A run or a preview before it is complete does not evaluate: the run fails and the preview returns 409 `history_loading`. - A keyword rule judges every serving keyword, one with no traffic at zero. Zernio syncs the keywords Google has not removed; paused keywords are not judged. - Google lists only search terms that showed at least once, so a search term rule takes `impressions` with `>` or `>=`, never `<` or `<=`.  They take `spend`, `impressions`, `clicks`, `conversions`, `ctr`, `cpc`, `cpm`, `cpa` and `roas` over whole days, no `usual`, `of`, `top` or `bottom`, and `compareTo` only as `campaign`. A keyword rule can `notify` or `pause`; a search term rule only notifies. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

