# OpenAPI\Client\PaymentsApi

All URIs are relative to https://api.sandbox.bvnk.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**paymentCreate()**](PaymentsApi.md#paymentCreate) | **POST** /api/v1/pay/summary | Create payment |
| [**paymentList()**](PaymentsApi.md#paymentList) | **GET** /api/v1/pay/summary | List Payments |
| [**paymentOutValidate()**](PaymentsApi.md#paymentOutValidate) | **PUT** /api/v1/pay/validate | Validate Address |
| [**paymentRead()**](PaymentsApi.md#paymentRead) | **GET** /api/v1/pay/{uuid}/summary | Get Payment |


## `paymentCreate()`

```php
paymentCreate($pay_request_dto): \OpenAPI\Client\Model\SummaryPaymentDto
```

Create payment

Creates a payment, either type IN or type OUT.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$pay_request_dto = new \OpenAPI\Client\Model\PayRequestDto(); // \OpenAPI\Client\Model\PayRequestDto

try {
    $result = $apiInstance->paymentCreate($pay_request_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->paymentCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pay_request_dto** | [**\OpenAPI\Client\Model\PayRequestDto**](../Model/PayRequestDto.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SummaryPaymentDto**](../Model/SummaryPaymentDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentList()`

```php
paymentList($merchant_id, $customer_reference, $payment_external_id, $from_date, $to_date, $offset, $max, $status, $order): \OpenAPI\Client\Model\SummaryPaymentDto[]
```

List Payments

Retrieves a list of payments on a specific Merchant ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$merchant_id = '5C8D8D78-366A-4AFB-B658-A64CE543C5DB'; // string | The merchant ID as a UUID.
$customer_reference = REF123; // string | The customer reference.
$payment_external_id = 5C8D8D78-366A-4AFB-B658-A64CE543C5DB; // string | The merchant payment uuid.
$from_date = 2023-03-30; // string | The start date.
$to_date = 2023-03-30; // string | The end date.
$offset = 0; // float | Where to start fetching records.
$max = 20; // float | Maximum number of items in response.
$status = new \OpenAPI\Client\Model\PaymentStatusDto(); // PaymentStatusDto
$order = asc; // string | Ordering direction.

try {
    $result = $apiInstance->paymentList($merchant_id, $customer_reference, $payment_external_id, $from_date, $to_date, $offset, $max, $status, $order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->paymentList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **merchant_id** | **string**| The merchant ID as a UUID. | [default to &#39;5C8D8D78-366A-4AFB-B658-A64CE543C5DB&#39;] |
| **customer_reference** | **string**| The customer reference. | [optional] |
| **payment_external_id** | **string**| The merchant payment uuid. | [optional] |
| **from_date** | **string**| The start date. | [optional] |
| **to_date** | **string**| The end date. | [optional] |
| **offset** | **float**| Where to start fetching records. | [optional] |
| **max** | **float**| Maximum number of items in response. | [optional] |
| **status** | [**PaymentStatusDto**](../Model/.md)|  | [optional] |
| **order** | **string**| Ordering direction. | [optional] |

### Return type

[**\OpenAPI\Client\Model\SummaryPaymentDto[]**](../Model/SummaryPaymentDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentOutValidate()`

```php
paymentOutValidate($pay_out_detail_dto)
```

Validate Address

Validates that a crypto address is correct.  Use this endpoint to validate that an address exists, is correctly formatted, and includes all the required data. This endpoint can help prevent your end users losing funds when submitting a payout.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$pay_out_detail_dto = new \OpenAPI\Client\Model\PayOutDetailDto(); // \OpenAPI\Client\Model\PayOutDetailDto

try {
    $apiInstance->paymentOutValidate($pay_out_detail_dto);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->paymentOutValidate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pay_out_detail_dto** | [**\OpenAPI\Client\Model\PayOutDetailDto**](../Model/PayOutDetailDto.md)|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentRead()`

```php
paymentRead($uuid): \OpenAPI\Client\Model\SummaryPaymentDto
```

Get Payment

Retrieves details of a specific payment using the UUID of the payment.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$uuid = '5C8D8D78-366A-4AFB-B658-A64CE543C5DB'; // string | The payment UUID.

try {
    $result = $apiInstance->paymentRead($uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->paymentRead: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **uuid** | **string**| The payment UUID. | [default to &#39;5C8D8D78-366A-4AFB-B658-A64CE543C5DB&#39;] |

### Return type

[**\OpenAPI\Client\Model\SummaryPaymentDto**](../Model/SummaryPaymentDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
