# # MerchantChannelPaymentDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_id** | **string** | The ID of the channel. | [optional]
**merchant_id** | **string** | The merchant ID linked to channel. | [optional]
**merchant_display_name** | **string** | The display name fo the merchant. | [optional]
**reference** | **string** | The unique reference of the channel. | [optional]
**date_created** | **int** | The date and time, encoded into UNIX epoch timestamps. | [optional] [default to 0]
**last_updated** | **int** | The date and time, encoded into UNIX epoch timestamps. | [optional] [default to 0]
**status** | **string** | The status of the channel payment. | [optional]
**uuid** | **string** | The uuid fo the channel payment. | [optional]
**hash** | **string** | The transaction hash of the channel payment. | [optional]
**address** | **string** | The address of the channel. | [optional]
**tag** | **string** | The tag of the channel. | [optional]
**paid_currency** | **string** | The currency of the payment. | [optional]
**display_currency** | **string** | The display currency of the channel. | [optional]
**wallet_currency** | **string** | The currency of the wallet linked to the channel. | [optional]
**fee_currency** | **string** | The currency of the fee taken. | [optional]
**paid_amount** | **float** | The amount paid to the channel. | [optional] [default to 0]
**display_amount** | **float** | The amount displayed of the channel payment. | [optional] [default to 0]
**wallet_amount** | **float** | The amount converted to the wallet linked to the channel. | [optional] [default to 0]
**fee_amount** | **float** | The amount of the fee taken. | [optional] [default to 0]
**exchange_rate** | [**\OpenAPI\Client\Model\ExchangeRateDto**](ExchangeRateDto.md) |  | [optional]
**display_rate** | [**\OpenAPI\Client\Model\ExchangeRateDto**](ExchangeRateDto.md) |  | [optional]
**risk** | [**\OpenAPI\Client\Model\ExchangeRateDto**](ExchangeRateDto.md) |  | [optional]
**sources** | **string[]** | The address source of the payment. | [optional]
**network_fee** | [**\OpenAPI\Client\Model\NetworkFeeDto**](NetworkFeeDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
