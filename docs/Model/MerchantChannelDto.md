# # MerchantChannelDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | The UUID of the channel. | [optional] [default to 0]
**date_created** | **int** | The date and time, encoded into UNIX epoch timestamps. | [optional] [default to 0]
**last_updated** | **int** | The date and time, encoded into UNIX epoch timestamps. | [optional] [default to 0]
**merchant_id** | **string** | The merchant ID linked to the channel. | [optional]
**wallet_currency** | **string** | The wallet currency of the channel. | [optional]
**display_currency** | **string** | The display currency of the channel. | [optional]
**pay_currency** | **string** | The payed currency of the channel. | [optional]
**address** | **string** | The address of the channel | [optional]
**tag** | **string** | The tag for payments | [optional]
**protocol** | **string** | The protocol of the channel. | [optional]
**reference** | **string** | The custom reference for the channel payment. | [optional]
**status** | **string** | The status of the channel. | [optional]
**uuid** | **string** | The UUID of the channel. | [optional]
**redirect_url** | **string** | The redirect URL to the channel payment page. | [optional]
**uri** | **string** | The URI of the address for QR code | [optional]
**alternatives** | [**\OpenAPI\Client\Model\AlternativeAddressDto[]**](AlternativeAddressDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
