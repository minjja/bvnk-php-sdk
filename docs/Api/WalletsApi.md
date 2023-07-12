# OpenAPI\Client\WalletsApi

All URIs are relative to https://api.sandbox.bvnk.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**walletBalanceList()**](WalletsApi.md#walletBalanceList) | **GET** /api/wallet/balances | List Wallet Balances |
| [**walletCreate()**](WalletsApi.md#walletCreate) | **POST** /api/wallet | Create Wallet |
| [**walletList()**](WalletsApi.md#walletList) | **GET** /api/wallet | List Wallets |
| [**walletRead()**](WalletsApi.md#walletRead) | **GET** /api/wallet/{id} | Get Wallet |
| [**walletTransactionReport()**](WalletsApi.md#walletTransactionReport) | **GET** /api/transaction/report | Transactions Report |


## `walletBalanceList()`

```php
walletBalanceList($date): \OpenAPI\Client\Model\BalanceDto[]
```

List Wallet Balances

Retrieves the balances of your wallets on platform.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\WalletsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$date = 2020-03-17; // string | Date at to retrieve balances.

try {
    $result = $apiInstance->walletBalanceList($date);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalletsApi->walletBalanceList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **date** | **string**| Date at to retrieve balances. | [optional] |

### Return type

[**\OpenAPI\Client\Model\BalanceDto[]**](../Model/BalanceDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `walletCreate()`

```php
walletCreate($wallet_request_dto): \OpenAPI\Client\Model\WalletDto
```

Create Wallet

Creates a wallet on the BVNK platform.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\WalletsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$wallet_request_dto = new \OpenAPI\Client\Model\WalletRequestDto(); // \OpenAPI\Client\Model\WalletRequestDto

try {
    $result = $apiInstance->walletCreate($wallet_request_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalletsApi->walletCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **wallet_request_dto** | [**\OpenAPI\Client\Model\WalletRequestDto**](../Model/WalletRequestDto.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\WalletDto**](../Model/WalletDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `walletList()`

```php
walletList($offset, $max): \OpenAPI\Client\Model\WalletDto[]
```

List Wallets

Retrieves a list of wallets on your account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\WalletsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$offset = 56; // int | Where to start fetching records.
$max = 10; // int | Maximum number of items in response.

try {
    $result = $apiInstance->walletList($offset, $max);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalletsApi->walletList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **int**| Where to start fetching records. | [optional] |
| **max** | **int**| Maximum number of items in response. | [optional] [default to 10] |

### Return type

[**\OpenAPI\Client\Model\WalletDto[]**](../Model/WalletDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `walletRead()`

```php
walletRead($id): \OpenAPI\Client\Model\WalletDto
```

Get Wallet

Retrieves a specific wallet.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\WalletsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 255861; // int | The ID of the wallet that you want to retrieve.

try {
    $result = $apiInstance->walletRead($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalletsApi->walletRead: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The ID of the wallet that you want to retrieve. | [default to 255861] |

### Return type

[**\OpenAPI\Client\Model\WalletDto**](../Model/WalletDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `walletTransactionReport()`

```php
walletTransactionReport($wallet_id, $from_date, $to_date, $format, $transaction_type): \OpenAPI\Client\Model\TransactionReportDto[]
```

Transactions Report

Report all transactions from wallet in specified format. Report will be generated and sent to main account email in the specified format.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\WalletsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$wallet_id = 255861; // int | Date at to retrieve balances.
$from_date = '2022-09-17'; // string | Export range from date in format 'YYYY-MM-dd'.
$to_date = '2023-03-17'; // string | Export range to date in format 'YYYY-MM-dd'.
$format = 'csv'; // string | 'json' - json format, 'csv' - csv format
$transaction_type = 'transaction_type_example'; // string | Transaction type code

try {
    $result = $apiInstance->walletTransactionReport($wallet_id, $from_date, $to_date, $format, $transaction_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalletsApi->walletTransactionReport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **wallet_id** | **int**| Date at to retrieve balances. | [optional] [default to 255861] |
| **from_date** | **string**| Export range from date in format &#39;YYYY-MM-dd&#39;. | [optional] [default to &#39;2022-09-17&#39;] |
| **to_date** | **string**| Export range to date in format &#39;YYYY-MM-dd&#39;. | [optional] [default to &#39;2023-03-17&#39;] |
| **format** | **string**| &#39;json&#39; - json format, &#39;csv&#39; - csv format | [optional] [default to &#39;csv&#39;] |
| **transaction_type** | **string**| Transaction type code | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransactionReportDto[]**](../Model/TransactionReportDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
