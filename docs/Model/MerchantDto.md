# # MerchantDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | The ID of the Merchant ID. | [optional]
**merchant_id** | **string** | The Merchant ID as a UUID. | [optional]
**display_name** | **string** | The name of the merchant displayed on the payments page. | [optional]
**secret** | **string** | The secret key used to validate webhooks. | [optional]
**webhook_url** | **string** | The webhooks URL that webhoosk are sent to. | [optional]
**auto_convert_invalid_payments** | **bool** | Is set to auto convert invalid payments. | [optional] [default to true]
**default_expiry_minutes** | **int** | The default number of minutes before a payment expires for this Merchant ID. | [optional]
**webhook_version** | **int** | The version of webhooks sent. | [optional]
**wallet** | [**\OpenAPI\Client\Model\WalletDto**](WalletDto.md) |  | [optional]
**email_recipients** | **string** | The recipients of event emails. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
