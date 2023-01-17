# V1CardsBody

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**terminal** | **int** | Product or terminal Id. | 
**cvc2** | **string** | cvc2. Mandatory if no JetToken provided | [optional] 
**jet_token** | **string** | Temporary token provided from PAYCOMET. Mandatory if no card provided. | [optional] 
**expiry_year** | **string** | Expiry year.  Mandatory if no JetToken provided | [optional] 
**expiry_month** | **string** | Expiry month.  Mandatory if no JetToken provided. | [optional] 
**pan** | **string** | Card number. Mandatory if no JetToken provided | [optional] 
**order** | **string** | Reference, will be included in callback. | [optional] 
**product_description** | **string** | Concept, will be included in callback. | [optional] 
**language** | **string** | Language for callback translation. | [optional] [default to 'es']
**notify** | **int** | Configure POST notification of the card tokenization result (possible values: 1 - force notify, 2 - not notify). Default product value will be used if notify is not informed | [optional] 
**card_holder_name** | **string** | Card holder name | [optional] 
**secure_authentication** | [**\Swagger\Client\Model\V1cardsSecureAuthentication**](V1cardsSecureAuthentication.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

