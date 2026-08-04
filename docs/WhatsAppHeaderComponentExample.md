# Zernio.Model.WhatsAppHeaderComponentExample

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**HeaderText** | **List&lt;string&gt;** | Sample values for header text variables | [optional] 
**HeaderTextNamedParams** | [**List&lt;WhatsAppNamedParamExample&gt;**](WhatsAppNamedParamExample.md) | Sample values for NAMED header variables (templates using {{customer_name}}-style tokens with parameter_format: NAMED). | [optional] 
**HeaderHandle** | **List&lt;string&gt;** | When the header format is a media type (image, video, gif, document), provide a public URL here. Zernio will download and upload it to WhatsApp on your behalf, replacing it with the internal file handle before creating the template. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

