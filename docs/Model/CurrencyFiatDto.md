# # CurrencyFiatDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **string** | The currency code. | [optional]
**deposit_fee** | **float** | The % fee to deposit the currency. | [optional]
**fiat** | **bool** | Is a fiat currency. | [optional] [default to true]
**icon** | **string** | The icon of the currency. | [optional]
**id** | **int** | The ID of the currency. | [optional]
**name** | **string** | The currency name. | [optional]
**options** | **object** | The currency options. | [optional]
**price_precision** | **int** | The precision of decimal points for the currency. | [optional] [default to 2]
**protocols** | **mixed[]** | The alternative protocols array. | [optional]
**quantity_precision** | **int** | The precision of decimal points for the currency displayed. | [optional] [default to 2]
**supports_deposits** | **bool** | Is deposits for this currency supported. | [optional] [default to true]
**supports_withdrawals** | **bool** | Is withdrawals for this currency supported | [optional] [default to true]
**withdrawal_fee** | **float** | The % fee to withdraw this currency. | [optional]
**withdrawal_parameters** | **mixed[]** | The withdrawal parameter object. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
