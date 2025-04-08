# Accounts

## Query All Crypto Accounts

> When query list for `Crypto Accounts`, no matter what was the pageSize, the last one in the response list would be accounts for the current quering `Merchant`

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/accounts/crypto_accounts%7B?current,pageSize}"><code>https://api.decenctype.com/accounts/crypto_accounts{?current,pageSize}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| current  | <p>Page </p><p><code>Example: 1</code></p>                    |
| -------- | ------------------------------------------------------------- |
| pageSize | <p>Number of items per page</p><p><code>Example: 5</code></p> |

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "total": 179,
    "users": [
      {
        "user_id": "638d8270-32c1-11ef-9902-27d134165673",
        "first_name": "bbb",
        "last_name": "ccc",
        "number": 73,
        "nationality": null,
        "status": "active",
        "crypto_accounts": [
          {
            "account_id": "63df7300-32c1-11ef-9902-27d134165673",
            "account_token": "BTC",
            "account_balance": "0.0000000000",
            "account_type": "user"
          },
          {
            "account_id": "63df7301-32c1-11ef-9902-27d134165673",
            "account_token": "ETH",
            "account_balance": "0.0000000000",
            "account_type": "user"
          },
          {
            "account_id": "63df7302-32c1-11ef-9902-27d134165673",
            "account_token": "USDT",
            "account_balance": "0.0000000000",
            "account_type": "user"
          },
          {
            "account_id": "63df7303-32c1-11ef-9902-27d134165673",
            "account_token": "USDC",
            "account_balance": "0.0000000000",
            "account_type": "user"
          }
        ]
      },
      {
        "user_id": "638d8270-32c1-11ef-9902-27d134165673",
        "merchant_id": "bbb",
        "merchant_name": "ccc",
        "crypto_accounts": [
          {
            "account_id": "63df7300-32c1-11ef-9902-27d134165673",
            "account_token": "BTC",
            "account_balance": "0.0000000000",
            "account_type": "user"
          },
          {
            "account_id": "63df7301-32c1-11ef-9902-27d134165673",
            "account_token": "ETH",
            "account_balance": "0.0000000000",
            "account_type": "user"
          },
          {
            "account_id": "63df7302-32c1-11ef-9902-27d134165673",
            "account_token": "USDT",
            "account_balance": "0.0000000000",
            "account_type": "user"
          },
          {
            "account_id": "63df7303-32c1-11ef-9902-27d134165673",
            "account_token": "USDC",
            "account_balance": "0.0000000000",
            "account_type": "user"
          }
        ]
      },
    ],
    "current": 1,
    "pageSize": 10
  }
}
```
{% endcode %}



</details>

## Query One Crypto Account

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/accounts/crypto/%7Baccount_id%7D"><code>https://api.decenctype.com/accounts/crypto/{account_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| account\_id | Account ID |
| ----------- | ---------- |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "account_id": "63df7300-32c1-11ef-9902-27d134165673",
    "user_id": "638d8270-32c1-11ef-9902-27d134165673",
    "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
    "account_balance": "0.0000000000",
    "account_balance_unavailable": "0.0000000000",
    "account_token": "BTC",
    "account_type": "user",
    "created_at": "2024-06-25T07:06:05.000Z",
    "updated_at": "2024-06-25T07:06:05.000Z"
  }
}
```
{% endcode %}



</details>

## Query All Fiat Accounts

> When query list for `Fiat Accounts`, no matter what was the pageSize, the last one in the response list would be account for the current quering `Merchant`

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/accounts/fiat_accounts%7B?current,pageSize}"><code>https://api.decenctype.com/accounts/fiat_accounts{?current,pageSize}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| current  | <p>Page</p><p><code>Example: 1</code></p>                     |
| -------- | ------------------------------------------------------------- |
| pageSize | <p>Number of items per page</p><p><code>Example: 5</code></p> |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "total": 102,
    "users": [
      {
        "user_id": "638d8270-32c1-11ef-9902-27d134165673",
        "first_name": "bbb",
        "last_name": "ccc",
        "number": 73,
        "nationality": null,
        "status": "active",
        "fiat_accounts": [
          {
            "account_id": "63df7304-32c1-11ef-9902-27d134165673",
            "account_currency": "USD",
            "account_balance": "0.00",
            "account_deposit": "0.00"
          },
          {
            "account_id": "63df9a10-32c1-11ef-9902-27d134165673",
            "account_currency": "EUR",
            "account_balance": "0.00",
            "account_deposit": "0.00"
          }
        ]
      },
      {
        "user_id": "638d8270-32c1-11ef-9902-27d134165673",
        "merchant_id": "bbb",
        "merchant_name": "ccc",
        "fiat_accounts": [
                      {
            "account_id": "63df7304-32c1-11ef-9902-27d134165673",
            "account_currency": "USD",
            "account_balance": "0.00",
            "account_deposit": "0.00"
          },
          {
            "account_id": "63df9a10-32c1-11ef-9902-27d134165673",
            "account_currency": "EUR",
            "account_balance": "0.00",
            "account_deposit": "0.00"
          }
        ]
      },
    ],
    "current": 1,
    "pageSize": 10
  }
}
```
{% endcode %}



</details>

## Query One Fiat Accounts

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/accounts/fiat/%7Baccount_id%7D"><code>https://api.decenctype.com/accounts/fiat/{account_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| account\_id | Account ID |
| ----------- | ---------- |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "account_id": "63df7304-32c1-11ef-9902-27d134165673",
    "user_id": "638d8270-32c1-11ef-9902-27d134165673",
    "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
    "account_currency": "USD",
    "account_balance": "0.00",
    "account_balance_unavailable": "0.00",
    "balance_confirmed": "0.00",
    "account_deposit": "0.00",
    "account_type": "user",
    "created_at": "2024-06-25T07:06:05.000Z",
    "updated_at": "2024-06-25T07:06:05.000Z"
  }
}
```
{% endcode %}

</details>

## Query All Crypto Accounts by User

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/accounts/crypto/query/%7B?user_id}"><code>https://api.decenctype.com/accounts/crypto/query/{user_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| user\_id | User ID |
| -------- | ------- |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": [
    {
      "account_id": "99803ad0-11e7-11ef-8140-99c4f5b8d784",
      "user_id": "5d4ad700-0a69-482f-8786-2e321079f247",
      "merchant_id": null,
      "account_balance": "0.0000000000",
      "account_balance_unavailable": "0.0000000000",
      "account_token": "BTC",
      "account_type": "user",
      "created_at": "2024-05-14T11:46:28.000Z",
      "updated_at": "2024-05-14T11:46:28.000Z"
    },
    {
      "account_id": "99803ad1-11e7-11ef-8140-99c4f5b8d784",
      "user_id": "5d4ad700-0a69-482f-8786-2e321079f247",
      "merchant_id": null,
      "account_balance": "0.0000000000",
      "account_balance_unavailable": "0.0000000000",
      "account_token": "ETH",
      "account_type": "user",
      "created_at": "2024-05-14T11:46:28.000Z",
      "updated_at": "2024-05-14T11:46:28.000Z"
    },
    {
      "account_id": "99803ad2-11e7-11ef-8140-99c4f5b8d784",
      "user_id": "5d4ad700-0a69-482f-8786-2e321079f247",
      "merchant_id": null,
      "account_balance": "248.3139418260",
      "account_balance_unavailable": "0.0000000000",
      "account_token": "USDT",
      "account_type": "user",
      "created_at": "2024-05-14T11:46:28.000Z",
      "updated_at": "2024-06-18T09:03:33.000Z"
    },
    {
      "account_id": "998061e0-11e7-11ef-8140-99c4f5b8d784",
      "user_id": "5d4ad700-0a69-482f-8786-2e321079f247",
      "merchant_id": null,
      "account_balance": "0.0000000000",
      "account_balance_unavailable": "0.0000000000",
      "account_token": "USDC",
      "account_type": "user",
      "created_at": "2024-05-14T11:46:28.000Z",
      "updated_at": "2024-05-14T11:46:28.000Z"
    }
  ]
}
```
{% endcode %}

</details>

## Query All Fiat Accounts by User

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/accounts/fiat/query/%7B?user_id}"><code>https://api.decenctype.com/accounts/fiat/query/{?user_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| user\_id | User ID |
| -------- | ------- |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": [
    {
      "account_id": "998061e1-11e7-11ef-8140-99c4f5b8d784",
      "user_id": "5d4ad700-0a69-482f-8786-2e321079f247",
      "merchant_id": null,
      "account_currency": "USD",
      "account_balance": "87.00",
      "account_balance_unavailable": "0.00",
      "balance_confirmed": "0.00",
      "account_deposit": "0.00",
      "account_type": "user",
      "created_at": "2024-05-14T11:46:28.000Z",
      "updated_at": "2024-06-29T07:19:47.000Z"
    },
    {
      "account_id": "998061e2-11e7-11ef-8140-99c4f5b8d784",
      "user_id": "5d4ad700-0a69-482f-8786-2e321079f247",
      "merchant_id": null,
      "account_currency": "EUR",
      "account_balance": "0.00",
      "account_balance_unavailable": "0.00",
      "balance_confirmed": "0.00",
      "account_deposit": "0.00",
      "account_type": "user",
      "created_at": "2024-05-14T11:46:28.000Z",
      "updated_at": "2024-05-14T11:46:28.000Z"
    }
  ]
}
```
{% endcode %}



</details>

## Create Accounts

> We do not provide an endpoint to create wallet accounts individually, they are usually created automatically when the user is created by merchant.











