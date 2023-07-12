# # SummaryPaymentDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | The unique identifier for the merchant payment. | [optional]
**merchant_display_name** | **string** | The display name for the merchant payment. | [optional]
**merchant_id** | **string** | The Merchant ID. You can find it on the Merchant Details page in your account. | [optional]
**date_created** | **int** | The date and time, encoded into UNIX epoch timestamps. | [optional]
**expiry_date** | **int** | The date and time, encoded into UNIX epoch timestamps | [optional]
**quote_expiry_date** | **int** | The date and time, encoded into UNIX epoch timestamps | [optional]
**acceptance_expiry_date** | **int** | The date and time, encoded into UNIX epoch timestamps | [optional]
**quote_status** | **string** |  | [optional]
**reference** | **string** | The custom payment reference ID to tie the payment to your customer. | [optional]
**type** | [**\OpenAPI\Client\Model\DirectionDto**](DirectionDto.md) |  | [optional]
**sub_type** | **string** | The payment sub type | [optional] [default to 'merchantPayIn']
**status** | [**\OpenAPI\Client\Model\PaymentStatusDto**](PaymentStatusDto.md) |  | [optional]
**display_currency** | [**\OpenAPI\Client\Model\PayAmountsDto**](PayAmountsDto.md) |  | [optional]
**wallet_currency** | [**\OpenAPI\Client\Model\PayAmountsDto**](PayAmountsDto.md) |  | [optional]
**paid_currency** | [**\OpenAPI\Client\Model\PayAmountsDto**](PayAmountsDto.md) |  | [optional]
**fee_currency** | [**\OpenAPI\Client\Model\PayAmountsDto**](PayAmountsDto.md) |  | [optional]
**display_rate** | [**\OpenAPI\Client\Model\ExchangeRateDto**](ExchangeRateDto.md) |  | [optional]
**exchange_rate** | [**\OpenAPI\Client\Model\ExchangeRateDto**](ExchangeRateDto.md) |  | [optional]
**address** | [**\OpenAPI\Client\Model\CryptoAddressDto**](CryptoAddressDto.md) |  | [optional]
**return_url** | **string** | The URL that the customer will be redirected to if they click &#39;Back to Merchant&#39; button on the payment web page. | [optional]
**redirect_url** | **string** | The URL to the payment page that you redirect your customers to. | [optional]
**transactions** | [**\OpenAPI\Client\Model\GatewayTransactionDto[]**](GatewayTransactionDto.md) |  | [optional]
**refund** | **object** | The payment this object is a refund of. This should reference the pay in that this refund was created for. | [optional]
**refunds** | **object[]** | Refunds that have been requested for this payment. This should reference the refund payout for this pay in. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
