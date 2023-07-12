# # PayRequestDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**merchant_id** | **string** | Your Merchant ID. You can find it on the Merchant Details page in your account. | [default to '5C8D8D78-366A-4AFB-B658-A64CE543C5DB']
**amount** | **float** | The payment amount. | [default to 223.05]
**expiry_minutes** | **int** | The time period after which payment expires. | [optional] [default to 20]
**currency** | **string** | The currency acronym. | [default to 'EUR']
**return_url** | **string** | The URL that the customer will be redirected to if they click &#39;Back to Merchant&#39; button on the payment web page. | [optional] [default to 'https://my-shop.com/payment-complete?ref=xyz']
**reference** | **string** | The custom payment reference ID to tie the payment to your customer. | [default to 'myUniqueRef333']
**type** | [**\OpenAPI\Client\Model\DirectionDto**](DirectionDto.md) |  |
**pay_in_details** | [**\OpenAPI\Client\Model\PayInDetailDto**](PayInDetailDto.md) |  | [optional]
**pay_out_details** | [**\OpenAPI\Client\Model\PayOutDetailDto**](PayOutDetailDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
