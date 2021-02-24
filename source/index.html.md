---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - python
  - java

toc_footers:
  - <a href='https://bitmax.io'>Sign Up for BitMax.io</a>

includes:
  - rest
  - rest_pub_general
  - rest_pub_general_futures_products
  - rest_pub_mkt
  - rest_pub_mkt_futures_pricing_data
  - rest_prv_auth
  - rest_prv_account
  - rest_prv_account_info
  - rest_prv_account_position
  - rest_prv_free_margin
  - rest_prv_account_change_margin
  - rest_prv_account_change_margin_type
  - rest_prv_account_change_leverage
  - rest_prv_account_transfer
  - rest_prv_order
  - rest_prv_order_generate_id
  - rest_prv_order_new
  - rest_prv_order_new_batch
  - rest_prv_order_cancel
  - rest_prv_order_cancel_batch
  - rest_prv_order_cancel_all
  - rest_prv_order_open
  - rest_prv_order_hist_curr
  - rest_prv_order_query_by_id
  - wss
  - wss_general
  - wss_auth
  - wss_keep_alive
  - wss_pub
  - wss_pub_futures_pricing_data
  - wss_sub_level1
  - wss_sub_level2
  - wss_sub_trades
  - wss_sub_bar
  - wss_prv <!--- - wss_prv_auth -->
  - wss_prv_order
  - wss_prv_account_update
  - wss_prv_req
  - wss_prv_req_account_snapshot
  - wss_prv_req_order_place
  - wss_prv_req_order_cancel
  - wss_prv_req_order_cancel_all
  - appendix
  - appendix_enum

search: true

code_clipboard: true
---

# Introducing Futures Pro (v2) APIs (Testnet Only)

## Change Log

**2021-02-23**

* Removed collapseDecimals field from [*Futures Contracts Info*](#futures-contracts-info) response.

**2021-02-22**

* Added RESTful [*Current Order History*](#list-current-history-orders) API.

**2021-02-21**

* Added [*Order Id Generate Algorithm*](#generate-order-id).
* Added RESTful [*Place Batch Orders*](#place-batch-orders) API.
* Added RESTful [*Cancel Batch Orders*](#cancel-batch-orders) API.
* Added RESTful [*Query Order By ID*](#query-order-by-id) API.

**2021-02-19**

* Added [*WebSocket Account Snapshot*](#ws-account-snapshot) API.
* Added [*WebSocket Place Order*](#ws-place-order) API.
* Added [*WebSocket Cancel Order*](#ws-cancel-order) API.
* Added [*WebSocket Cancel All Orders*](#ws-cancel-all-orders) API.

**2021-02-18**

* Replaced `baseAsset` and `quoteAsset` with `settlementAsset` in [*Futures Contract Info*](#futures-contracts-info) response.
* Updated [*Account Info*](#account-info) API path.

## Testnet 

Testnet URL: [*https://api-test.bitmax-sandbox.io*](https://api-test.bitmax-sandbox.io/)

You are free to register one or more accounts in the testnet. You can use the magic code **888888** to bypass all verification code checks 
(email verification, phone number verification, two-step authentication, etc.).

You accounts will automatically receive initial funding. 

Please expect the testnet to be reset every a few days. 

## Obtain API Keys

Prior to use API, you need to login the website to create API Key with proper permissions. The API key is shared for all instruments in BitMax including cash, margin and futures.

You can create and manage your API Keys [here](https://bitmax.io/en/account/api-key).

Every user can create up to 10 API Keys, each can be applied with either permission below:

- **View permission**: It is used to query the data, such as order query, trade query.
- **Trade permission**: It is used to place order, cancel order and transfer, etc.
- **Transfer permission**: It is used to create/cancel asset transfer order, etc.

Please remember below information after creation:

- **Access Key** is used in API request
- **Secret Key** is used to generate the signature (only visible once after creation)
- The API Key can bind maximum 20 IP addresses (either host IP or network IP), we strongly suggest you bind IP address for security purpose. The API Key without IP binding will be expired after 90 days.

## Demo Code

Python Demo: [*https://github.com/bitmax-exchange/bitmax-futures-api-demo-v2*](https://github.com/bitmax-exchange/bitmax-futures-api-demo-v2)

