# Zernio.Model.ListConversionDestinations200ResponseDestinationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Destination identifier. Meta: pixel ID. Google: conversion action resource name. LinkedIn: numeric conversion rule ID. OpenAI Ads: pixel wire id.  | [optional] 
**Name** | **string** |  | [optional] 
**Type** | **string** | Present when the platform locks event type to the destination (Google conversion actions, LinkedIn conversion rules).  | [optional] 
**Status** | **string** |  | [optional] 
**AdAccountId** | **string** | Set by adapters whose destinations are scoped to a specific ad account (LinkedIn). Pass back on subsequent CRUD calls.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

