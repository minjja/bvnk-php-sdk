# # CurrencyDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **string** | The currency code. | [optional]
**deposit_fee** | **float** | The % fee to deposit the currency. | [optional]
**fiat** | **bool** | Is a fiat currency. | [optional] [default to false]
**icon** | **string** | The icon of the currency. | [optional]
**id** | **int** | The ID of the currency. | [optional]
**name** | **string** | The currency name. | [optional]
**options** | [**\OpenAPI\Client\Model\CurrencyOptions**](CurrencyOptions.md) |  | [optional]
**price_precision** | **int** | The precision of decimal points for the currency. | [optional] [default to 5]
**protocols** | [**\OpenAPI\Client\Model\CurrencyProtocol[]**](CurrencyProtocol.md) | The alternative protocols array. | [optional]
**quantity_precision** | **int** | The precision of decimal points for the currency displayed. | [optional] [default to 5]
**supports_deposits** | **bool** | Is deposits for this currency supported. | [optional] [default to false]
**supports_withdrawals** | **bool** | Is withdrawals for this currency supported | [optional] [default to false]
**withdrawal_fee** | **float** | The % fee to withdraw this currency. | [optional]
**withdrawal_parameters** | [**\OpenAPI\Client\Model\ExternalCurrencyWithdrawalParameter[]**](ExternalCurrencyWithdrawalParameter.md) | The withdrawal parameter object. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
