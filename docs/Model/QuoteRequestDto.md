# # QuoteRequestDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**from** | **string** | The currency to convert from. | [default to 'EUR']
**to** | **string** | The currency to convert to. | [default to 'USDC']
**from_wallet** | **float** | The ID of the wallet converted from. | [default to 3598236]
**use_minimum** | **bool** | Is converting the minimum allowed amount. | [default to false]
**use_maximum** | **bool** | Is converting the max amount of the wallet. | [default to false]
**to_wallet** | **float** | The ID of the wallet converted to. | [default to 3598514]
**amount_in** | **float** | The amount being converted. | [default to 10]
**pay_in_method** | **string** | The type of method in. | [default to 'wallet']
**pay_out_method** | **string** | The type of method out. | [default to 'wallet']

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
