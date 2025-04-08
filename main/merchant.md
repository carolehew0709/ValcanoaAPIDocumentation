# Merchant

## Get Merchant Info

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/merchants/get"><code>https://api.decenctype.com/merchants/get</code></a></summary>

#### **Headers**

| Name         | Value              |
| ------------ | ------------------ |
| Content-Type | `application/json` |
| X-API-KEY    | `Your-API-Key`     |

#### Response

{% code title="200 OK" %}
```javascript
{
    "code": 0,
    "message": "OK",
    "data": {
        "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
        "merchant_name": "Egg Pay",
        "public_key": "5fdb9ebf2f3d350c11ffbf5c95acfa493c56cce852ad8c275fed669942ea1239",
        "secret_key": "30d35a6cdb1bbe8696a0836c0524a008884853a076f79ad8ee97ba9fd5708ce6",
        "total_balance": "0.00",
        "available_balance": "0.00",
        "user_number": 0,
        "total_volume": "0.00",
        "monthly_volume": "0.00",
        "service_fee": "0.0140",
        "base_flag": false,
        "status": "active",
        "settings": {
            "account": {
                "cryptoDepositFeeMode": "fixed",
                "cryptoDepositFeeRate": "0.04"
            },
            "basicInfo": {
                "supportTeamName": "Egg Pay",
                "supportTeamEmail": "help@eggpay.app"
            },
            "transaction": {
                "minimumBalance": 100,
                "transactionMode": "Card",
                "automaticallyTopUp": "false",
                "minimumTopUpAmount": 100,
                "minimumTopupAmount": 10,
                "automaticallyTopUpAmount": 50,
                "automaticallyTopUpAccountCurrency": "USDT"
            }
        },
        "createdAt": "2024-04-25T07:17:09.000Z",
        "updatedAt": "2024-11-05T15:21:27.000Z",
        "cardProducts": [
            {
                "card_product_id": "16e63441-5e08-4f33-92e4-4e06f6bb3b32",
                "issuer": "AIRWALLEX",
                "channel": "ads",
                "status": "ACTIVE",
                "product": "Ads-Visa",
                "price": 19,
                "currency": "USD",
                "type": "VIRTUAL_CARD",
                "card_design": "GRAY",
                "design_id": null,
                "country": "中国香港",
                "bin": "493767",
                "description": "fb扣费验证码，在总交易记录中查看",
                "is_global": true,
                "createdAt": "2025-01-10T02:08:26.000Z",
                "updatedAt": "2025-01-10T02:08:27.000Z",
                "MerchantCardProduct": {
                    "createdAt": "2024-05-15T09:59:08.000Z",
                    "updatedAt": "2024-05-15T09:59:08.000Z",
                    "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
                    "card_product_id": "16e63441-5e08-4f33-92e4-4e06f6bb3b32"
                }
            },
            {
                "card_product_id": "3a84b64d-8dd3-40a7-b6c4-9585597c2865",
                "issuer": "REAP",
                "channel": "common",
                "status": "ACTIVE",
                "product": "Business Virtual",
                "price": 19,
                "currency": "usd",
                "type": "VIRTUAL_CARD",
                "card_design": "RED",
                "design_id": null,
                "country": "中国香港",
                "bin": "493728",
                "description": "fb扣费验证码，在总交易记录中查看",
                "is_global": true,
                "createdAt": "2025-01-10T02:08:26.000Z",
                "updatedAt": "2025-01-10T02:08:27.000Z",
                "MerchantCardProduct": {
                    "createdAt": "2024-05-15T09:59:08.000Z",
                    "updatedAt": "2024-05-15T09:59:08.000Z",
                    "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
                    "card_product_id": "3a84b64d-8dd3-40a7-b6c4-9585597c2865"
                }
            },
            {
                "card_product_id": "4be3dbca-84d0-4c89-ab6f-3631ac891fe9",
                "issuer": "AIRWALLEX",
                "channel": "common",
                "status": "ACTIVE",
                "product": "Leisure Virtual",
                "price": 19,
                "currency": "usd",
                "type": "VIRTUAL_CARD",
                "card_design": "Egg",
                "design_id": null,
                "country": "中国香港",
                "bin": "493767",
                "description": "fb扣费验证码，在总交易记录中查看",
                "is_global": true,
                "createdAt": "2025-01-10T02:08:26.000Z",
                "updatedAt": "2025-01-10T02:08:27.000Z",
                "MerchantCardProduct": {
                    "createdAt": "2024-05-15T09:59:08.000Z",
                    "updatedAt": "2024-05-15T09:59:08.000Z",
                    "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
                    "card_product_id": "4be3dbca-84d0-4c89-ab6f-3631ac891fe9"
                }
            },
            {
                "card_product_id": "fd3e9eab-2deb-4ee8-938a-15168eca6e05",
                "issuer": "AIRWALLEX",
                "channel": "common",
                "status": "ACTIVE",
                "product": "Leisure Physical",
                "price": 499,
                "currency": "usd",
                "type": "PHYSICAL_CARD",
                "card_design": "BLACK",
                "design_id": null,
                "country": "中国香港",
                "bin": "493767",
                "description": "fb扣费验证码，在总交易记录中查看",
                "is_global": true,
                "createdAt": "2025-01-10T02:08:26.000Z",
                "updatedAt": "2025-01-10T02:08:27.000Z",
                "MerchantCardProduct": {
                    "createdAt": "2024-05-15T09:59:08.000Z",
                    "updatedAt": "2024-05-15T09:59:08.000Z",
                    "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
                    "card_product_id": "fd3e9eab-2deb-4ee8-938a-15168eca6e05"
                }
            }
        ]
    }
}
```
{% endcode %}



</details>

## Query Master Accounts

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/merchants/account/list"><code>https://api.decenctype.com/merchants/account/list</code></a></summary>

#### **Headers**

| Name         | Value              |
| ------------ | ------------------ |
| Content-Type | `application/json` |
| X-API-KEY    | `Your-API-Key`     |

#### Response

{% code title="200 OK" %}
```javascript
{
    "code": 0,
    "message": "OK",
    "data": {
        "crypto": [
            {
                "account_id": "0736f5d0-ff6b-11ee-bc93-6382caed923a",
                "account_balance": "0.00000000",
                "account_token": "BTC",
                "account_balance_unavailable": "0.00000000"
            },
            {
                "account_id": "07371ce0-ff6b-11ee-bc93-6382caed923a",
                "account_balance": "0.00000000",
                "account_token": "ETH",
                "account_balance_unavailable": "0.00000000"
            },
            {
                "account_id": "07371ce1-ff6b-11ee-bc93-6382caed923a",
                "account_balance": "997912.56691149",
                "account_token": "USDT",
                "account_balance_unavailable": "0.00000000"
            },
            {
                "account_id": "07371ce2-ff6b-11ee-bc93-6382caed923a",
                "account_balance": "0.00000000",
                "account_token": "USDC",
                "account_balance_unavailable": "0.00000000"
            }
        ],
        "fiat": [
            {
                "account_id": "c92ff390-47f4-11ef-a789-4da2026c2502",
                "account_currency": "USD",
                "account_balance": "9998.00000000",
                "account_balance_unavailable": "0.00000000"
            },
            {
                "account_id": "c9301aa0-47f4-11ef-a789-4da2026c2502",
                "account_currency": "EUR",
                "account_balance": "0.00000000",
                "account_balance_unavailable": "0.00000000"
            }
        ]
    }
}
```
{% endcode %}



</details>

## Query All Commissions

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/merchants/commission/list"><code>https://api.decenctype.com/merchants/commission/list</code></a></summary>

#### **Headers**

| Name         | Value              |
| ------------ | ------------------ |
| Content-Type | `application/json` |
| X-API-KEY    | `Your-API-Key`     |

#### Response

{% code title="200 OK" %}
```javascript
{
    "code": 0,
    "message": "OK",
    "data": {
        "total": 1,
        "list": [
            {
                "c_id": "f0455397-b514-4234-aa4b-2fffeaa89793",
                "agent_id": "905fb9e0-f4b3-11ee-bcfe-71e1c295ffd2",
                "amount": "7.2747",
                "currency": "USD",
                "type": "merchant",
                "status": "pending",
                "createdAt": "2024-09-06T14:16:57.000Z",
                "updatedAt": "2024-09-06T14:16:57.000Z",
                "merchant": {
                    "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
                    "merchant_name": "Egg Pay"
                },
                "agent": {
                    "agent_id": "905fb9e0-f4b3-11ee-bcfe-71e1c295ffd2",
                    "user": {
                        "user_id": "df10fac1-dd25-40c6-9c72-3223872825d7",
                        "first_name": "Anton",
                        "last_name": "Marchenko"
                    }
                },
                "transaction_fee": {
                    "transaction_id": "20240227133822731580",
                    "amount_total": "454.6713",
                    "currency": "EUR",
                    "timestamp": "2024-02-27T13:38:22.000Z",
                    "transaction_card": {
                        "transaction_id": "20240227133824921884",
                        "network_transaction_id": "20240227133824757552",
                        "type": "CHARGE_CARD",
                        "card_id": "CA1598720640548896",
                        "amount": "447.67",
                        "currency": "EUR",
                        "amount_cleared": "447.67",
                        "currency_cleared": "EUR",
                        "consumption_tax": "0.00",
                        "status": "COMPLETED",
                        "review": "PENDING",
                        "timestamp": "2024-02-27T13:38:24.000Z",
                        "timestamp_cleared": "2024-02-27T13:38:24.000Z",
                        "details": {
                            "id": "20240227133824921884",
                            "type": "CHARGE CARD",
                            "cardId": "CA1598720640548896",
                            "status": "COMPLETED",
                            "txnAmount": 447.671345,
                            "txnInstant": 1709041104162,
                            "txnCurrency": "EUR",
                            "amountCleared": 447.671345
                        },
                        "crypto_amount": null,
                        "crypto_currency": null,
                        "crypto_exchange_rate": null
                    }
                }
            }
}
```
{% endcode %}



</details>

## Settle Commissions

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/merchants/trigger/settlement"><code>https://api.decenctype.com/merchants/trigger/settlement</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Request (Object)

| <p>start </p><p>(string)</p> | <p>Date</p><p><code>2024/1/1</code></p>   |
| ---------------------------- | ----------------------------------------- |
| <p>end</p><p>(string)</p>    | <p>Date</p><p><code>2024/12/31</code></p> |

#### Body

```json
{
    "start":" ",
    "end":" "
}
```

#### Response

{% code title="200 OK" %}
```javascript
{
    "code": 0,
    "message": "OK",
    "data": "No transactions found for the given"
}
```
{% endcode %}



</details>

## Create Transfer Order

> Transfer crypto or fiat from master account to user, do not require approval from a higher-level administrator.

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/merchants/order/transfer"><code>https://api.decenctype.com/merchants/order/transfer</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Request (Object)

| <p>transfer_account</p><p>(string)</p> | <p><a href="users.md#query-all-users">User ID</a></p><p><code>sdasdfaf=sadasd</code></p>              |
| -------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| <p>transfer_type</p><p>(string)</p>    | <p>Email</p><p><code>aaabbb@gmail.com</code></p>                                                      |
| pay\_account\_id                       | <p><a href="merchant.md#query-master-accounts">Master Account ID</a></p><p><code>dssdsdsds</code></p> |
| <p>amount</p><p>(number)</p>           | <p>Number of transfer</p><p><code>100</code></p>                                                      |
| account\_type                          | <p>value in [crypto, fiat]</p><p><code>crypto</code></p>                                              |

#### Body

```json
{
  "transfer_account": "sdasdfaf=sadasd",
  "transfer_type: email (string) - value in [email, phone, merchant, invite_code]": "",
  "pay_account_id": "dssdsdsds",
  "amount": 100,
  "account_type": "crypto"
}
```

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "OK",
    "data": {
        "order_id": "d70bf7b0-0ec4-11f0-a14e-919657f6ce07",
        "transfer_type": "ADMIN OPERATION",
        "transfer_account": "5d4ad700-0a69-482f-8786-2e321079f247",
        "user_id": "5d4ad700-0a69-482f-8786-2e321079f247",
        "pay_account_id": "07371ce1-ff6b-11ee-bc93-6382caed923a",
        "receive_account_id": "99803ad2-11e7-11ef-8140-99c4f5b8d784",
        "amount": 100,
        "currency": "USDT",
        "admin_id": 6,
        "order_status": "approved",
        "updated_at": "2025-04-01T06:45:03.297Z",
        "created_at": "2025-04-01T06:45:03.276Z"
    }
}
```
{% endcode %}



</details>

## Create Withdraw Order

> Withdraw crypto from master account to wallet address, this request requires administrator approval.

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/merchants/order/withdraw"><code>https://api.decenctype.com/merchants/order/withdraw</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Request (Object)

| <p>account_id</p><p>(string)</p>    | <p><a href="merchant.md#query-master-accounts">Master Account ID</a></p><p><code>ssdsdsds</code></p> |
| ----------------------------------- | ---------------------------------------------------------------------------------------------------- |
| <p>chain_address</p><p>(string)</p> | Chain address                                                                                        |
| <p>amount</p><p>(number)</p>        | <p>Number of withdraw</p><p><code>100</code></p>                                                     |

#### Body

```json
{
  "account_id": "",
  "chain_address": "",
  "amount": 100
}
```

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "order_id": "b6a911d0-48a2-11ef-b11e-453f862f620d",
    "user_id": "",
    "type": "crypto",
    "fee": "0.010000",
    "currency": "USDT",
    "amount": 100,
    "bank_account_id": "4936e4e0-1b2c-11ef-b082-ffdab13c006e",
    "wallet_account_id": "07371ce1-ff6b-11ee-bc93-6382caed923a",
    "order_status": "pending",
    "admin_id": "1",
    "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
    "updated_at": "2024-07-23T03:21:55.821Z",
    "created_at": "2024-07-23T03:21:55.821Z"
  }
}
```
{% endcode %}



</details>

## Create Exchange Order

> Exchange crypto to the appropriate fiat, this request requires administrator approval.

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/merchants/order/exchange"><code>https://api.decenctype.com/merchants/order/exchange</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "account_crypto_id": "",
  "account_fiat_id": "",
  "amount": 100
}
```

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "OK",
    "data": {
        "order_id": "854fc8b0-0ec5-11f0-a14e-919657f6ce07",
        "order_status": "pending",
        "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
        "account_crypto_id": "07371ce1-ff6b-11ee-bc93-6382caed923a",
        "account_fiat_id": "c92ff390-47f4-11ef-a789-4da2026c2502",
        "rate_id": 1,
        "rate_exchange": 0.9995,
        "amount_crypto": 100,
        "amount_fiat": 99.95,
        "fee": 0,
        "amount_total": 99.95,
        "admin_id": null,
        "updated_at": "2025-04-01T06:49:55.644Z",
        "created_at": "2025-04-01T06:49:55.644Z"
    }
}
```
{% endcode %}



</details>
