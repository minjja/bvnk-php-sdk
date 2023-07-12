# OpenAPI\Client\ChannelsApi

All URIs are relative to https://api.sandbox.bvnk.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**channelCreate()**](ChannelsApi.md#channelCreate) | **POST** /api/v2/channel | Create Channel |
| [**channelList()**](ChannelsApi.md#channelList) | **GET** /api/v2/channel | List Channels |
| [**channelPaymentList()**](ChannelsApi.md#channelPaymentList) | **GET** /api/v2/channel/payment | List Channel Payments |
| [**channelPaymentRead()**](ChannelsApi.md#channelPaymentRead) | **GET** /api/v2/channel/payment/{uuid} | Get Channel Payment |
| [**channelRead()**](ChannelsApi.md#channelRead) | **GET** /api/v2/channel/{uuid} | Get Channel |


## `channelCreate()`

```php
channelCreate($merchant_channel_request_dto): \OpenAPI\Client\Model\MerchantChannelDto
```

Create Channel

Creates a channel that your end users can openly send payments to.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$merchant_channel_request_dto = new \OpenAPI\Client\Model\MerchantChannelRequestDto(); // \OpenAPI\Client\Model\MerchantChannelRequestDto

try {
    $result = $apiInstance->channelCreate($merchant_channel_request_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->channelCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **merchant_channel_request_dto** | [**\OpenAPI\Client\Model\MerchantChannelRequestDto**](../Model/MerchantChannelRequestDto.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\MerchantChannelDto**](../Model/MerchantChannelDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `channelList()`

```php
channelList($merchant_id, $offset, $max, $sort, $order): \OpenAPI\Client\Model\MerchantChannelDto[]
```

List Channels

Retrieves all channels related to a Merchant ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$merchant_id = 'c02153ae-8ac8-4222-80e8-b2b2af85bd78'; // string | The merchant ID that the channels belong to
$offset = 0; // string | Where to start fetching records.
$max = 10; // string | Maximum number of items in response.
$sort = new \OpenAPI\Client\Model\PaymentStatusDto(); // PaymentStatusDto | The attribute used to sort the data
$order = 'order_example'; // string | Ordering direction

try {
    $result = $apiInstance->channelList($merchant_id, $offset, $max, $sort, $order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->channelList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **merchant_id** | **string**| The merchant ID that the channels belong to | [default to &#39;c02153ae-8ac8-4222-80e8-b2b2af85bd78&#39;] |
| **offset** | **string**| Where to start fetching records. | [optional] |
| **max** | **string**| Maximum number of items in response. | [optional] |
| **sort** | [**PaymentStatusDto**](../Model/.md)| The attribute used to sort the data | [optional] |
| **order** | **string**| Ordering direction | [optional] |

### Return type

[**\OpenAPI\Client\Model\MerchantChannelDto[]**](../Model/MerchantChannelDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `channelPaymentList()`

```php
channelPaymentList($merchant_id, $status, $from_date, $to_date, $offset, $max, $order, $q): \OpenAPI\Client\Model\MerchantChannelPaymentDto[]
```

List Channel Payments

Retrieves a list of payments to a channel on a specific Merchant ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$merchant_id = 'c02153ae-8ac8-4222-80e8-b2b2af85bd78'; // string | The Merchant ID
$status = COMPLETE; // string
$from_date = 2023-03-05; // string | From which date to start searching.
$to_date = 2023-05-03; // string | At which date to stop searching.
$offset = 0; // string | Where to start fetching records.
$max = 10; // string | Maximum number of items in response.
$order = asc; // string | Ordering direction
$q = 'q_example'; // string | Can be UUID of the payment, reference, channel UUID, transaction hash, or wallet code.

try {
    $result = $apiInstance->channelPaymentList($merchant_id, $status, $from_date, $to_date, $offset, $max, $order, $q);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->channelPaymentList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **merchant_id** | **string**| The Merchant ID | [default to &#39;c02153ae-8ac8-4222-80e8-b2b2af85bd78&#39;] |
| **status** | **string**|  | [optional] |
| **from_date** | **string**| From which date to start searching. | [optional] |
| **to_date** | **string**| At which date to stop searching. | [optional] |
| **offset** | **string**| Where to start fetching records. | [optional] |
| **max** | **string**| Maximum number of items in response. | [optional] |
| **order** | **string**| Ordering direction | [optional] |
| **q** | **string**| Can be UUID of the payment, reference, channel UUID, transaction hash, or wallet code. | [optional] |

### Return type

[**\OpenAPI\Client\Model\MerchantChannelPaymentDto[]**](../Model/MerchantChannelPaymentDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `channelPaymentRead()`

```php
channelPaymentRead($uuid): \OpenAPI\Client\Model\MerchantChannelPaymentDto
```

Get Channel Payment

Retrieves a specific payment made into a channel.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$uuid = 'c0dc9c14-0312-4a6b-a1a3-a6dcebdcc8a4'; // string | The UUID of the payment you are querying.

try {
    $result = $apiInstance->channelPaymentRead($uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->channelPaymentRead: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **uuid** | **string**| The UUID of the payment you are querying. | [default to &#39;c0dc9c14-0312-4a6b-a1a3-a6dcebdcc8a4&#39;] |

### Return type

[**\OpenAPI\Client\Model\MerchantChannelPaymentDto**](../Model/MerchantChannelPaymentDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `channelRead()`

```php
channelRead($uuid): \OpenAPI\Client\Model\MerchantChannelDto
```

Get Channel

Retrieves a specific channel by UUID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$uuid = '9d1f67f2-a647-404b-9b02-247c77be81d0'; // string | The UUID of the channel you are querying

try {
    $result = $apiInstance->channelRead($uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->channelRead: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **uuid** | **string**| The UUID of the channel you are querying | [default to &#39;9d1f67f2-a647-404b-9b02-247c77be81d0&#39;] |

### Return type

[**\OpenAPI\Client\Model\MerchantChannelDto**](../Model/MerchantChannelDto.md)

### Authorization

[Hawk](../../README.md#Hawk)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
