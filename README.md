# OpenAPIClient-php

The BVNK API is designed to facilitate seamless and secure transactions including payments, channels, and digital wallet transactions.


## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure API key authorization: Hawk
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$merchant_channel_request_dto = new \OpenAPI\Client\Model\MerchantChannelRequestDto(); // \OpenAPI\Client\Model\MerchantChannelRequestDto

try {
    $result = $apiInstance->channelCreate($merchant_channel_request_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->channelCreate: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api.sandbox.bvnk.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ChannelsApi* | [**channelCreate**](docs/Api/ChannelsApi.md#channelcreate) | **POST** /api/v2/channel | Create Channel
*ChannelsApi* | [**channelList**](docs/Api/ChannelsApi.md#channellist) | **GET** /api/v2/channel | List Channels
*ChannelsApi* | [**channelPaymentList**](docs/Api/ChannelsApi.md#channelpaymentlist) | **GET** /api/v2/channel/payment | List Channel Payments
*ChannelsApi* | [**channelPaymentRead**](docs/Api/ChannelsApi.md#channelpaymentread) | **GET** /api/v2/channel/payment/{uuid} | Get Channel Payment
*ChannelsApi* | [**channelRead**](docs/Api/ChannelsApi.md#channelread) | **GET** /api/v2/channel/{uuid} | Get Channel
*CurrenciesApi* | [**listCurrenciesCrypto**](docs/Api/CurrenciesApi.md#listcurrenciescrypto) | **GET** /api/currency/crypto | List Crypto Currencies
*CurrenciesApi* | [**listCurrenciesDeposit**](docs/Api/CurrenciesApi.md#listcurrenciesdeposit) | **GET** /api/currency/deposit | List Wallet Currencies
*CurrenciesApi* | [**listCurrenciesFiat**](docs/Api/CurrenciesApi.md#listcurrenciesfiat) | **GET** /api/currency/fiat | List Fiat Currencies
*MerchantIDsApi* | [**merchantIdCreate**](docs/Api/MerchantIDsApi.md#merchantidcreate) | **POST** /api/v1/merchant | Create Merchant ID
*MerchantIDsApi* | [**merchantIdList**](docs/Api/MerchantIDsApi.md#merchantidlist) | **GET** /api/v1/merchant | List Merchant IDs
*PaymentsApi* | [**paymentCreate**](docs/Api/PaymentsApi.md#paymentcreate) | **POST** /api/v1/pay/summary | Create payment
*PaymentsApi* | [**paymentList**](docs/Api/PaymentsApi.md#paymentlist) | **GET** /api/v1/pay/summary | List Payments
*PaymentsApi* | [**paymentOutValidate**](docs/Api/PaymentsApi.md#paymentoutvalidate) | **PUT** /api/v1/pay/validate | Validate Address
*PaymentsApi* | [**paymentRead**](docs/Api/PaymentsApi.md#paymentread) | **GET** /api/v1/pay/{uuid}/summary | Get Payment
*TradingAndConversionsApi* | [**quoteAccept**](docs/Api/TradingAndConversionsApi.md#quoteaccept) | **PUT** /api/v1/quote/accept/{uuid} | Accept Quote
*TradingAndConversionsApi* | [**quoteCreate**](docs/Api/TradingAndConversionsApi.md#quotecreate) | **POST** /api/v1/quote | Create Quote
*TradingAndConversionsApi* | [**quoteList**](docs/Api/TradingAndConversionsApi.md#quotelist) | **GET** /api/v1/quote/{merchantId} | List Quotes
*TradingAndConversionsApi* | [**quoteRead**](docs/Api/TradingAndConversionsApi.md#quoteread) | **GET** /api/v1/quote/{uuid} | Get Quote
*WalletsApi* | [**walletBalanceList**](docs/Api/WalletsApi.md#walletbalancelist) | **GET** /api/wallet/balances | List Wallet Balances
*WalletsApi* | [**walletCreate**](docs/Api/WalletsApi.md#walletcreate) | **POST** /api/wallet | Create Wallet
*WalletsApi* | [**walletList**](docs/Api/WalletsApi.md#walletlist) | **GET** /api/wallet | List Wallets
*WalletsApi* | [**walletRead**](docs/Api/WalletsApi.md#walletread) | **GET** /api/wallet/{id} | Get Wallet
*WalletsApi* | [**walletTransactionReport**](docs/Api/WalletsApi.md#wallettransactionreport) | **GET** /api/transaction/report | Transactions Report

## Models

- [AcceptedQuoteDto](docs/Model/AcceptedQuoteDto.md)
- [AccountMethodDto](docs/Model/AccountMethodDto.md)
- [AlternativeAddressDto](docs/Model/AlternativeAddressDto.md)
- [BalanceDto](docs/Model/BalanceDto.md)
- [ClientValidationErrorDto](docs/Model/ClientValidationErrorDto.md)
- [CryptoAddressDto](docs/Model/CryptoAddressDto.md)
- [CurrencyDto](docs/Model/CurrencyDto.md)
- [CurrencyFiatDto](docs/Model/CurrencyFiatDto.md)
- [CurrencyOptions](docs/Model/CurrencyOptions.md)
- [CurrencyProtocol](docs/Model/CurrencyProtocol.md)
- [DirectionDto](docs/Model/DirectionDto.md)
- [ExchangeRateDto](docs/Model/ExchangeRateDto.md)
- [ExternalCurrencyWithdrawalParameter](docs/Model/ExternalCurrencyWithdrawalParameter.md)
- [FeeDto](docs/Model/FeeDto.md)
- [FeesDto](docs/Model/FeesDto.md)
- [FormDto](docs/Model/FormDto.md)
- [GatewayTransactionDto](docs/Model/GatewayTransactionDto.md)
- [MerchantChannelDto](docs/Model/MerchantChannelDto.md)
- [MerchantChannelPaymentDto](docs/Model/MerchantChannelPaymentDto.md)
- [MerchantChannelRequestDto](docs/Model/MerchantChannelRequestDto.md)
- [MerchantDto](docs/Model/MerchantDto.md)
- [MerchantIdCreateRequest](docs/Model/MerchantIdCreateRequest.md)
- [MerchantIdCreateRequestWallet](docs/Model/MerchantIdCreateRequestWallet.md)
- [NetworkFeeDto](docs/Model/NetworkFeeDto.md)
- [PayAmountsDto](docs/Model/PayAmountsDto.md)
- [PayInDetailDto](docs/Model/PayInDetailDto.md)
- [PayInInstructionDto](docs/Model/PayInInstructionDto.md)
- [PayInMethodDto](docs/Model/PayInMethodDto.md)
- [PayOutDetailDto](docs/Model/PayOutDetailDto.md)
- [PayOutInstructionDto](docs/Model/PayOutInstructionDto.md)
- [PayOutMethodDto](docs/Model/PayOutMethodDto.md)
- [PayRequestDto](docs/Model/PayRequestDto.md)
- [PaymentLegDto](docs/Model/PaymentLegDto.md)
- [PaymentStatusDto](docs/Model/PaymentStatusDto.md)
- [QuoteDto](docs/Model/QuoteDto.md)
- [QuoteRequestDto](docs/Model/QuoteRequestDto.md)
- [ServerErrorDto](docs/Model/ServerErrorDto.md)
- [SummaryPaymentDto](docs/Model/SummaryPaymentDto.md)
- [TransactionReportDto](docs/Model/TransactionReportDto.md)
- [TransactionReportRequestDataDto](docs/Model/TransactionReportRequestDataDto.md)
- [ValidationErrorDto](docs/Model/ValidationErrorDto.md)
- [WalletDto](docs/Model/WalletDto.md)
- [WalletRequestDto](docs/Model/WalletRequestDto.md)

## Authorization

Authentication schemes defined for the API:
### Hawk

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.1`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
