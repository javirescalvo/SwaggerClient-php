# Swagger\Client\TokenApi

All URIs are relative to *https://rest.paycomet.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addToken**](TokenApi.md#addtoken) | **POST** /v1/token | Tokenizes an APM.

# **addToken**
> \Swagger\Client\Model\InlineResponse20037 addToken($body, $paycomet_api_token)

Tokenizes an APM.

This method supposes the registration of the APM in PAYCOMET for subsequent charges.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\TokenApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\V1TokenBody(); // \Swagger\Client\Model\V1TokenBody | 
$paycomet_api_token = "paycomet_api_token_example"; // string | PAYCOMET API key (Token actions privilege required)

try {
    $result = $apiInstance->addToken($body, $paycomet_api_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenApi->addToken: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\V1TokenBody**](../Model/V1TokenBody.md)|  | [optional]
 **paycomet_api_token** | **string**| PAYCOMET API key (Token actions privilege required) | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse20037**](../Model/InlineResponse20037.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

