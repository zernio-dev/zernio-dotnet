# Zernio.Model.BrowseAdTargeting200ResponseNodesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NodeId** | **string** | Identifies the node within this response. Not a Meta id: never put it in a targeting spec. | 
**ParentNodeId** | **string** | nodeId of the parent organizational node, null for a root. | 
**Id** | **string** | Meta targeting id, null on organizational nodes. | 
**Name** | **string** |  | 
**Type** | **string** | Meta&#39;s targeting spec key (interests, behaviors, industries, life_events, education_statuses, relationship_statuses, family_statuses, income, ...). Null on most organizational nodes. | 
**Path** | **List&lt;string&gt;** | Labels of the ancestors, root first. Does not include the node itself. | 
**Selectable** | **bool** | True when the node can be targeted (it has a Meta id). | 
**Description** | **string** | Meta&#39;s description, when it has one. | [optional] 
**AudienceSizeLowerBound** | **int** | Meta&#39;s estimated audience size, lower bound, when reported. | [optional] 
**AudienceSizeUpperBound** | **int** | Meta&#39;s estimated audience size, upper bound, when reported. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

