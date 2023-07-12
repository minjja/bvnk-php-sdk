# # CryptoAddressDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | **string** | The crypto address to send funds to | [optional]
**tag** | **string** | This is a payment destination tag. This fields isn&#39;t null when the paidCurrency currency value is XRP. | [optional]
**protocol** | **string** | The protocol behind a currency, &#39;ERC20&#39; or &#39;TRC20&#39;. | [optional]
**uri** | **string** | The destination address URI for QR code | [optional]
**alternatives** | [**\OpenAPI\Client\Model\AlternativeAddressDto[]**](AlternativeAddressDto.md) | The list of non-default addresses for other tokens | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
