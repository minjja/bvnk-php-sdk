# OpenAPI\Client\CurrenciesApi

All URIs are relative to https://api.sandbox.bvnk.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listCurrenciesCrypto()**](CurrenciesApi.md#listCurrenciesCrypto) | **GET** /api/currency/crypto | List Crypto Currencies |
| [**listCurrenciesDeposit()**](CurrenciesApi.md#listCurrenciesDeposit) | **GET** /api/currency/deposit | List Wallet Currencies |
| [**listCurrenciesFiat()**](CurrenciesApi.md#listCurrenciesFiat) | **GET** /api/currency/fiat | List Fiat Currencies |


## `listCurrenciesCrypto()`

```php
listCurrenciesCrypto($offset, $max, $allow_deposits): \OpenAPI\Client\Model\CurrencyDto[]
```

List Crypto Currencies

Retrieves a list of all cryptocurrencies available on the BVNK platform. This list represents cryptocurrencies that end users can select whilst making a payment.  For sandbox, only Ethereum (ETH) is fully functional.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CurrenciesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$offset = 0; // float | Where to start fetching records.
$max = 200; // float | Maximum number of items in response.
$allow_deposits = false; // bool | Only list currencies that allow deposits.

try {
    $result = $apiInstance->listCurrenciesCrypto($offset, $max, $allow_deposits);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CurrenciesApi->listCurrenciesCrypto: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **float**| Where to start fetching records. | [optional] [default to 0] |
| **max** | **float**| Maximum number of items in response. | [optional] [default to 200] |
| **allow_deposits** | **bool**| Only list currencies that allow deposits. | [optional] [default to false] |

### Return type

[**\OpenAPI\Client\Model\CurrencyDto[]**](../Model/CurrencyDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCurrenciesDeposit()`

```php
listCurrenciesDeposit($offset, $max): \OpenAPI\Client\Model\CurrencyDto[]
```

List Wallet Currencies

These are the currencies that can be used to create a new wallet.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CurrenciesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$offset = 0; // float | Where to start fetching records.
$max = 200; // float | Maximum number of items in response.

try {
    $result = $apiInstance->listCurrenciesDeposit($offset, $max);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CurrenciesApi->listCurrenciesDeposit: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **float**| Where to start fetching records. | [optional] [default to 0] |
| **max** | **float**| Maximum number of items in response. | [optional] [default to 200] |

### Return type

[**\OpenAPI\Client\Model\CurrencyDto[]**](../Model/CurrencyDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCurrenciesFiat()`

```php
listCurrenciesFiat($offset, $max): \OpenAPI\Client\Model\CurrencyFiatDto[]
```

List Fiat Currencies

Retrieves a list of all display fiat currencies available on BVNK's Crypto Payments API. This list refers to currencies merchants can display on a payment page to an end user. It does not represent the list of currencies that can be held on the platform in wallets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CurrenciesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$offset = 0; // float | Where to start fetching records.
$max = 200; // float | Maximum number of items in response.

try {
    $result = $apiInstance->listCurrenciesFiat($offset, $max);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CurrenciesApi->listCurrenciesFiat: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **float**| Where to start fetching records. | [optional] [default to 0] |
| **max** | **float**| Maximum number of items in response. | [optional] [default to 200] |

### Return type

[**\OpenAPI\Client\Model\CurrencyFiatDto[]**](../Model/CurrencyFiatDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
