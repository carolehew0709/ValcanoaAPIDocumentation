# Wallets

## Query All Chain Types

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/wallet/chain_types/query%7B?token}"><code>https://api.decenctype.com/wallet/chain_types/query{?token}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| token | <p>Crypto token in [BTC, ETH, USDT, USDC]</p><p><code>Example: USDT</code></p> |
| ----- | ------------------------------------------------------------------------------ |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": [
    {
      "chain_id": 195,
      "chain_type": "TRC20"
    },
    {
      "chain_id": 2510,
      "chain_type": "BEP20"
    },
    {
      "chain_id": 62,
      "chain_type": "Polygon"
    },
    {
      "chain_id": 60,
      "chain_type": "ERC20"
    }
  ]
}
```
{% endcode %}



</details>

## Generate Chain Address

> Generate a new crypto address for KYC verified users. The `chain_id` and `chain_type` can refer to [Query Chain Type](wallets.md#query-all-chain-types).> &#x20;The available chains will be listed with the endpoint. If the user already has an address, the existing address will be returned.

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/wallet/address/generate"><code>https://api.decenctype.com/wallet/address/generate</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "chain_id": 60,
  "chain_type": "ERC20"
}
```

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "",
  "data": {

  }
}
```
{% endcode %}



</details>







