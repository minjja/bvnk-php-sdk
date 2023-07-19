# OpenAPI\Client\TradingAndConversionsApi

All URIs are relative to https://api.sandbox.bvnk.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**quoteAccept()**](TradingAndConversionsApi.md#quoteAccept) | **PUT** /api/v1/quote/accept/{uuid} | Accept Quote |
| [**quoteCreate()**](TradingAndConversionsApi.md#quoteCreate) | **POST** /api/v1/quote | Create Quote |
| [**quoteList()**](TradingAndConversionsApi.md#quoteList) | **GET** /api/v1/quote/{merchantId} | List Quotes |
| [**quoteRead()**](TradingAndConversionsApi.md#quoteRead) | **GET** /api/v1/quote/{uuid} | Get Quote |


## `quoteAccept()`

```php
quoteAccept($uuid): \OpenAPI\Client\Model\AcceptedQuoteDto
```

Accept Quote

Executes a quote.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TradingAndConversionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$uuid = '5dc4e061-31c6-4b96-8c4d-0ea984aece0b'; // string | The quote UUID you are accepting.

try {
    $result = $apiInstance->quoteAccept($uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TradingAndConversionsApi->quoteAccept: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **uuid** | **string**| The quote UUID you are accepting. | [default to &#39;5dc4e061-31c6-4b96-8c4d-0ea984aece0b&#39;] |

### Return type

[**\OpenAPI\Client\Model\AcceptedQuoteDto**](../Model/AcceptedQuoteDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `quoteCreate()`

```php
quoteCreate($estimate, $quote_request_dto): \OpenAPI\Client\Model\QuoteDto
```

Create Quote

Creates a quote to convert between wallets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TradingAndConversionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$estimate = false; // bool | Create estimate quote
$quote_request_dto = new \OpenAPI\Client\Model\QuoteRequestDto(); // \OpenAPI\Client\Model\QuoteRequestDto

try {
    $result = $apiInstance->quoteCreate($estimate, $quote_request_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TradingAndConversionsApi->quoteCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **estimate** | **bool**| Create estimate quote | [optional] [default to false] |
| **quote_request_dto** | [**\OpenAPI\Client\Model\QuoteRequestDto**](../Model/QuoteRequestDto.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\QuoteDto**](../Model/QuoteDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `quoteList()`

```php
quoteList($merchant_id): \OpenAPI\Client\Model\QuoteDto[]
```

List Quotes

Retrieves all quotes on a specific Merchant ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TradingAndConversionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$merchant_id = '0a12a214-1619-43fa-9be1-0029f6a440a0'; // string | Merchant ID you are retrieving quotes from.

try {
    $result = $apiInstance->quoteList($merchant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TradingAndConversionsApi->quoteList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **merchant_id** | **string**| Merchant ID you are retrieving quotes from. | [default to &#39;0a12a214-1619-43fa-9be1-0029f6a440a0&#39;] |

### Return type

[**\OpenAPI\Client\Model\QuoteDto[]**](../Model/QuoteDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `quoteRead()`

```php
quoteRead($uuid): \OpenAPI\Client\Model\QuoteDto
```

Get Quote

Retrieves a specific quote.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TradingAndConversionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$uuid = '0a12a214-1619-43fa-9be1-0029f6a440a0'; // string | UUID of the quote you are retrieving.

try {
    $result = $apiInstance->quoteRead($uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TradingAndConversionsApi->quoteRead: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **uuid** | **string**| UUID of the quote you are retrieving. | [default to &#39;0a12a214-1619-43fa-9be1-0029f6a440a0&#39;] |

### Return type

[**\OpenAPI\Client\Model\QuoteDto**](../Model/QuoteDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
