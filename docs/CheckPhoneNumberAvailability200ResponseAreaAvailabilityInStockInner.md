# Zernio.Model.CheckPhoneNumberAvailability200ResponseAreaAvailabilityInStockInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ndc** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Count** | **int** | Numbers we can sell there: the carrier count minus the numbers we hold back (WhatsApp refused them or another order holds them). | [optional] 
**Ndcs** | **List&lt;string&gt;** | Every area code of the city, deepest first (Madrid: 915, 911, 910, ...). &#x60;ndc&#x60; is the one an order is placed against. | [optional] 
**Aliases** | **List&lt;string&gt;** | Other names the area answers to, present only when it has some (Milano for Milan, Sevilla for Seville). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

