# # GatewayTransactionDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date_created** | **int** | The date and time, encoded into UNIX epoch timestamps. | [optional]
**date_confirmed** | **int** | The date and time, encoded into UNIX epoch timestamps. | [optional]
**hash** | **string** | Transaction hash. | [optional]
**amount** | **float** | The payment amount. | [optional]
**risk** | **object** |  | [optional]
**network_fee_currency** | **string** | The currency acronym. | [optional]
**network_fee_amount** | **float** | The network fee amount. | [optional]
**sources** | **string[]** | The list of source addresses, only applicable if payment in. | [optional]
**display_rate** | [**\OpenAPI\Client\Model\ExchangeRateDto**](ExchangeRateDto.md) |  | [optional]
**exchange_rate** | [**\OpenAPI\Client\Model\ExchangeRateDto**](ExchangeRateDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
