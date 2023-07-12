# # WalletDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | **string** | The crypto wallet address | [optional]
**alternatives** | **mixed[]** | The array of alternative protocol addresses. | [optional]
**approx_available** | **string** | The approximate amount availible in the wallet. | [optional]
**approx_balance** | **string** | The balance amount availible of the wallet. | [optional]
**available** | **float** |  | [optional]
**balance** | **float** | The balance of the wallet. | [optional]
**converted_available** | **float** | The availible converted amount | [optional]
**currency** | [**\OpenAPI\Client\Model\CurrencyDto**](CurrencyDto.md) |  | [optional]
**custodian_wallet** | **bool** | Is a custodian wallet. | [optional]
**deposit_fee** | **float** | The fee to deposit funds in wallet. | [optional]
**description** | **string** | The description of the wallet. | [optional]
**id** | **int** | The wallet ID. | [optional]
**is_emoney** | **bool** | Is E Money Wallet | [optional] [default to false]
**lookup** | **string** | Is a lookup. | [optional]
**protocol** | **string** | The protocol of the wallet. | [optional]
**supports_deposits** | **bool** | Is able to support deposits. | [optional] [default to true]
**supports_third_party** | **bool** | Is a third party wallet. | [optional] [default to false]
**supports_withdrawals** | **bool** | Is able to support withdrawals. | [optional] [default to true]
**withdrawal_fee** | **float** | The fee to withdraw funds from wallet. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
