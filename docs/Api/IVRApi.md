# Swagger\Client\IVRApi

All URIs are relative to *https://rest.paycomet.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**checkSession**](IVRApi.md#checksession) | **POST** /v1/ivr/session-state | Checks an IVR session
[**getSession**](IVRApi.md#getsession) | **POST** /v1/ivr/get-session | Creates an IVR session
[**sessionCancel**](IVRApi.md#sessioncancel) | **POST** /v1/ivr/session-cancel | Cancel an IVR session

# **checkSession**
> \Swagger\Client\Model\InlineResponse20035 checkSession($paycomet_api_token, $body)

Checks an IVR session

check_session

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\IVRApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$paycomet_api_token = "paycomet_api_token_example"; // string | PAYCOMET API key (Authorization privilege required)
$body = new \Swagger\Client\Model\IvrSessionstateBody(); // \Swagger\Client\Model\IvrSessionstateBody | 

try {
    $result = $apiInstance->checkSession($paycomet_api_token, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IVRApi->checkSession: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **paycomet_api_token** | **string**| PAYCOMET API key (Authorization privilege required) |
 **body** | [**\Swagger\Client\Model\IvrSessionstateBody**](../Model/IvrSessionstateBody.md)|  | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse20035**](../Model/InlineResponse20035.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSession**
> \Swagger\Client\Model\InlineResponse20034 getSession($paycomet_api_token, $body)

Creates an IVR session

get_session

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\IVRApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$paycomet_api_token = "paycomet_api_token_example"; // string | PAYCOMET API key (Authorization privilege required)
$body = new \Swagger\Client\Model\IvrGetsessionBody(); // \Swagger\Client\Model\IvrGetsessionBody | 

try {
    $result = $apiInstance->getSession($paycomet_api_token, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IVRApi->getSession: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **paycomet_api_token** | **string**| PAYCOMET API key (Authorization privilege required) |
 **body** | [**\Swagger\Client\Model\IvrGetsessionBody**](../Model/IvrGetsessionBody.md)|  | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse20034**](../Model/InlineResponse20034.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **sessionCancel**
> \Swagger\Client\Model\InlineResponse20036 sessionCancel($paycomet_api_token, $body)

Cancel an IVR session

session_cancell

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\IVRApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$paycomet_api_token = "paycomet_api_token_example"; // string | PAYCOMET API key (Authorization privilege required)
$body = new \Swagger\Client\Model\IvrSessioncancelBody(); // \Swagger\Client\Model\IvrSessioncancelBody | 

try {
    $result = $apiInstance->sessionCancel($paycomet_api_token, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IVRApi->sessionCancel: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **paycomet_api_token** | **string**| PAYCOMET API key (Authorization privilege required) |
 **body** | [**\Swagger\Client\Model\IvrSessioncancelBody**](../Model/IvrSessioncancelBody.md)|  | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse20036**](../Model/InlineResponse20036.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

