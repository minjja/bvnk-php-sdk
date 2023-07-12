# OpenAPI\Client\MerchantIDsApi

All URIs are relative to https://api.sandbox.bvnk.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**merchantIdCreate()**](MerchantIDsApi.md#merchantIdCreate) | **POST** /api/v1/merchant | Create Merchant ID |
| [**merchantIdList()**](MerchantIDsApi.md#merchantIdList) | **GET** /api/v1/merchant | List Merchant IDs |


## `merchantIdCreate()`

```php
merchantIdCreate($merchant_id_create_request): \OpenAPI\Client\Model\MerchantDto
```

Create Merchant ID

Generate a Merchant ID for your account to process pay-ins and pay-outs through our API.  A Merchant ID is essential as it designates the account wallet where incoming pay-ins will be settled. For instance, if a Merchant ID is associated with a EUR wallet ID, any incoming USDT payment will be automatically converted to EUR and deposited in the designated EUR wallet.  Vice versa, any outgoing USDT payment will be automatically converted and withdrawn from the designated EUR wallet.  For further information, please visit https://docs.bvnk.com/docs/creating-your-first-merchant to learn more about creating your first Merchant ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MerchantIDsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$merchant_id_create_request = new \OpenAPI\Client\Model\MerchantIdCreateRequest(); // \OpenAPI\Client\Model\MerchantIdCreateRequest

try {
    $result = $apiInstance->merchantIdCreate($merchant_id_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MerchantIDsApi->merchantIdCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **merchant_id_create_request** | [**\OpenAPI\Client\Model\MerchantIdCreateRequest**](../Model/MerchantIdCreateRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\MerchantDto**](../Model/MerchantDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `merchantIdList()`

```php
merchantIdList(): \OpenAPI\Client\Model\MerchantDto[]
```

List Merchant IDs

Retrieves merchant IDs setup on your account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MerchantIDsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->merchantIdList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MerchantIDsApi->merchantIdList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\MerchantDto[]**](../Model/MerchantDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
