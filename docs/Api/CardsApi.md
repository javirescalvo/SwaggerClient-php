# Swagger\Client\CardsApi

All URIs are relative to *https://rest.paycomet.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addUser**](CardsApi.md#adduser) | **POST** /v1/cards | Tokenizes a card. Either card number and CVC2 or jetToken are required. For you to send directly the card data you should be PCI certified or the accepting the requirement to submit quarterly SAQ-AEP and get ASV scans. For most users is strongly recommended getting the jetToken with JETIFRAME or using GET integration to register the cards instead of REST.
[**editUser**](CardsApi.md#edituser) | **POST** /v1/cards/edit | Changes the expiry date, cvc2 or both
[**infoUser**](CardsApi.md#infouser) | **POST** /v1/cards/info | Get card info
[**physicalAddCard**](CardsApi.md#physicaladdcard) | **POST** /v1/cards/physical | Tokenize a card by physical encrypted data
[**physicalEditCard**](CardsApi.md#physicaleditcard) | **POST** /v1/cards/physical/edit | Edit a card entered by physical encrypted data
[**removeUser**](CardsApi.md#removeuser) | **POST** /v1/cards/delete | Removes a card

# **addUser**
> \Swagger\Client\Model\InlineResponse2001 addUser($body, $paycomet_api_token)

Tokenizes a card. Either card number and CVC2 or jetToken are required. For you to send directly the card data you should be PCI certified or the accepting the requirement to submit quarterly SAQ-AEP and get ASV scans. For most users is strongly recommended getting the jetToken with JETIFRAME or using GET integration to register the cards instead of REST.

This method supposes the registration of the card in PAYCOMET, it is not valid for subsequent charges with the exception of MIT. To register the card against the processor for subsequent recurring charges, it is necessary to charge for a secure environment, regardless of the amount.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\V1CardsBody(); // \Swagger\Client\Model\V1CardsBody | 
$paycomet_api_token = "paycomet_api_token_example"; // string | PAYCOMET API key (Token actions privilege required)

try {
    $result = $apiInstance->addUser($body, $paycomet_api_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CardsApi->addUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\V1CardsBody**](../Model/V1CardsBody.md)|  | [optional]
 **paycomet_api_token** | **string**| PAYCOMET API key (Token actions privilege required) | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **editUser**
> \Swagger\Client\Model\InlineResponse2001 editUser($body, $paycomet_api_token)

Changes the expiry date, cvc2 or both

edit_user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\CardsEditBody(); // \Swagger\Client\Model\CardsEditBody | 
$paycomet_api_token = "paycomet_api_token_example"; // string | PAYCOMET API key (Token actions privilege required)

try {
    $result = $apiInstance->editUser($body, $paycomet_api_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CardsApi->editUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CardsEditBody**](../Model/CardsEditBody.md)|  | [optional]
 **paycomet_api_token** | **string**| PAYCOMET API key (Token actions privilege required) | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **infoUser**
> \Swagger\Client\Model\InlineResponse2002 infoUser($body, $paycomet_api_token)

Get card info

Info about an user card.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\CardsInfoBody(); // \Swagger\Client\Model\CardsInfoBody | 
$paycomet_api_token = "paycomet_api_token_example"; // string | PAYCOMET API key (Query privilege required)

try {
    $result = $apiInstance->infoUser($body, $paycomet_api_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CardsApi->infoUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CardsInfoBody**](../Model/CardsInfoBody.md)|  | [optional]
 **paycomet_api_token** | **string**| PAYCOMET API key (Query privilege required) | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse2002**](../Model/InlineResponse2002.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **physicalAddCard**
> \Swagger\Client\Model\InlineResponse2004 physicalAddCard($body, $paycomet_api_token)

Tokenize a card by physical encrypted data

cards_physical

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\CardsPhysicalBody(); // \Swagger\Client\Model\CardsPhysicalBody | 
$paycomet_api_token = "paycomet_api_token_example"; // string | PAYCOMET API key (Token actions privilege required)

try {
    $result = $apiInstance->physicalAddCard($body, $paycomet_api_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CardsApi->physicalAddCard: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CardsPhysicalBody**](../Model/CardsPhysicalBody.md)|  | [optional]
 **paycomet_api_token** | **string**| PAYCOMET API key (Token actions privilege required) | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse2004**](../Model/InlineResponse2004.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **physicalEditCard**
> \Swagger\Client\Model\InlineResponse2005 physicalEditCard($body, $paycomet_api_token)

Edit a card entered by physical encrypted data

cards_physical_edit

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\PhysicalEditBody(); // \Swagger\Client\Model\PhysicalEditBody | 
$paycomet_api_token = "paycomet_api_token_example"; // string | PAYCOMET API key (Token actions privilege required)

try {
    $result = $apiInstance->physicalEditCard($body, $paycomet_api_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CardsApi->physicalEditCard: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\PhysicalEditBody**](../Model/PhysicalEditBody.md)|  | [optional]
 **paycomet_api_token** | **string**| PAYCOMET API key (Token actions privilege required) | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse2005**](../Model/InlineResponse2005.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **removeUser**
> \Swagger\Client\Model\InlineResponse2003 removeUser($body, $paycomet_api_token)

Removes a card

Deletes the user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\CardsDeleteBody(); // \Swagger\Client\Model\CardsDeleteBody | 
$paycomet_api_token = "paycomet_api_token_example"; // string | PAYCOMET API key (Token actions privilege required)

try {
    $result = $apiInstance->removeUser($body, $paycomet_api_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CardsApi->removeUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CardsDeleteBody**](../Model/CardsDeleteBody.md)|  | [optional]
 **paycomet_api_token** | **string**| PAYCOMET API key (Token actions privilege required) | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse2003**](../Model/InlineResponse2003.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

