# Zernio.Model.ListConversionDestinations200ResponseDestinationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Destination identifier. Meta: pixel ID. Google: conversion action resource name. LinkedIn: numeric conversion rule ID. OpenAI Ads: pixel wire id.  | [optional] 
**Name** | **string** |  | [optional] 
**Type** | **string** | Present when the platform locks event type to the destination (Google conversion actions, LinkedIn conversion rules).  | [optional] 
**Status** | **string** |  | [optional] 
**AdAccountId** | **string** | Set by adapters whose destinations are scoped to a specific ad account (LinkedIn). Pass back on subsequent CRUD calls.  | [optional] 
**ConversionEvents** | [**List&lt;ListConversionDestinations200ResponseDestinationsInnerConversionEventsInner&gt;**](ListConversionDestinations200ResponseDestinationsInnerConversionEventsInner.md) | OpenAI Ads only: the conversion event settings wired to this pixel. A &#x60;goal: conversions&#x60; create on POST /v1/ads/create optimizes for the first &#x60;optimizable&#x60; one; when none is, it returns 400.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

