# # QuoteDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | The ID of the quote. | [optional]
**from** | **string** | The currency to convert from. | [optional]
**to** | **string** | The currency to convert to. | [optional]
**amount_in** | **float** | The amount converted to. | [optional]
**amount_due** | **float** | The amount due to be converted. | [optional]
**amount_out** | **float** | The amount being converted out. | [optional]
**price** | **float** | The price quoted. | [optional]
**quote_status** | **string** | The status of the quote. | [optional]
**payment_status** | **string** | The payment status. | [optional]
**acceptance_expiry_date** | **int** | The date and time, encoded into UNIX epoch timestamps. | [optional]
**acceptance_date** | **int** | The date and time, encoded into UNIX epoch timestamps. | [optional]
**payment_expiry_date** | **int** | The date and time, encoded into UNIX epoch timestamps. | [optional]
**payment_receipt_date** | **int** | The date and time, encoded into UNIX epoch timestamps. | [optional]
**pay_in_legs** | [**\OpenAPI\Client\Model\PaymentLegDto[]**](PaymentLegDto.md) |  | [optional]
**pay_in_method** | [**\OpenAPI\Client\Model\PayInMethodDto**](PayInMethodDto.md) |  | [optional]
**pay_out_method** | [**\OpenAPI\Client\Model\PayOutMethodDto**](PayOutMethodDto.md) |  | [optional]
**uuid** | **string** | The UUID of the quote. | [optional]
**pay_out_instruction** | [**\OpenAPI\Client\Model\PayOutInstructionDto**](PayOutInstructionDto.md) |  | [optional]
**pay_in_instruction** | [**\OpenAPI\Client\Model\PayInInstructionDto**](PayInInstructionDto.md) |  | [optional]
**use_pay_in_method** | [**\OpenAPI\Client\Model\AccountMethodDto**](AccountMethodDto.md) |  | [optional]
**use_pay_out_method** | [**\OpenAPI\Client\Model\AccountMethodDto**](AccountMethodDto.md) |  | [optional]
**fee** | **float** | The fee for the quote. | [optional]
**processing_fee** | **float** | The processing fee. | [optional]
**type** | **string** | The type of quote. | [optional]
**net_price** | **float** | The net price fo the quote. | [optional]
**gross_price** | **float** | The gross price of the quote. | [optional]
**amount_in_gross** | **float** | The price of the quote in gross. | [optional]
**amount_in_net** | **float** | The price of the quote in net. | [optional]
**fees** | [**\OpenAPI\Client\Model\FeesDto**](FeesDto.md) |  | [optional]
**date_created** | **int** | The date and time, encoded into UNIX epoch timestamps. | [optional]
**last_updated** | **int** | The date and time, encoded into UNIX epoch timestamps. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
