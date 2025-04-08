# Card Products

## Query All Card Products

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/product/query%7B?offset,limit}"><code>https://api.decenctype.com/cards/product/query{?offset,limit}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| offset | <p>Page</p><p><code>Example: 0</code></p>                     |
| ------ | ------------------------------------------------------------- |
| limit  | <p>Number of items per page</p><p><code>Example: 5</code></p> |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "Card products queried successfully.",
  "data": [
    {
      "card_product_id": "fd3e9eab-2deb-4ee8-938a-15168eca6e05",
      "issuer": "AIRWALLEX",
      "status": "ACTIVE",
      "product": "Leisure Physical",
      "price": 499,
      "currency": "usd",
      "type": "PHYSICAL_CARD",
      "card_design": "BLACK",
      "is_global": true,
      "merchants": [
        {
          "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
          "merchant_name": "Egg Pay",
          "public_key": "5fdb9ebf2f3d350c11ffbf5c95acfa493c56cce852ad8c275fed669942ea1239",
          "secret_key": "30d35a6cdb1bbe8696a0836c0524a008884853a076f79ad8ee97ba9fd5708ce6",
          "total_balance": "0.00",
          "available_balance": "0.00",
          "user_number": 0,
          "total_volume": "0.00",
          "monthly_volume": "0.00",
          "service_fee": "0.0000",
          "base_flag": false,
          "createdAt": "2024-04-25T07:17:09.000Z",
          "updatedAt": "2024-04-25T07:17:09.000Z",
          "MerchantCardProduct": {
            "createdAt": "2024-05-15T09:59:08.000Z",
            "updatedAt": "2024-05-15T09:59:08.000Z",
            "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
            "card_product_id": "fd3e9eab-2deb-4ee8-938a-15168eca6e05"
          }
        }
      ]
    }
  ]
}
```
{% endcode %}



</details>

## Query One Card Product

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/product/get/%7Bcard_product_id%7D"><code>https://api.decenctype.com/cards/product/get/{card_product_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| card\_product\_id | Card Product ID |
| ----------------- | --------------- |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "card_product_id": "fd3e9eab-2deb-4ee8-938a-15168eca6e05",
    "issuer": "AIRWALLEX",
    "status": "ACTIVE",
    "product": "Leisure Physical",
    "price": 499,
    "currency": "usd",
    "type": "PHYSICAL_CARD",
    "card_design": "BLACK",
    "is_global": true
  }
}
```
{% endcode %}

</details>

## Search Card Products

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/product/search%7B?search_word}"><code>https://api.decenctype.com/cards/product/search{?search_word}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| search\_word | <p><code>Product, issuer, design, ..</code></p><p><code>Example: REAP</code></p> |
| ------------ | -------------------------------------------------------------------------------- |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "total": 2,
    "products": [
      {
        "card_product_id": "4be3dbca-84d0-4c89-ab6f-3631ac891fe9",
        "issuer": "AIRWALLEX",
        "status": "ACTIVE",
        "product": "Leisure Virtual",
        "price": 19,
        "currency": "usd",
        "type": "VIRTUAL_CARD",
        "card_design": "Egg",
        "is_global": true
      },
      {
        "card_product_id": "fd3e9eab-2deb-4ee8-938a-15168eca6e05",
        "issuer": "AIRWALLEX",
        "status": "ACTIVE",
        "product": "Leisure Physical",
        "price": 499,
        "currency": "usd",
        "type": "PHYSICAL_CARD",
        "card_design": "BLACK",
        "is_global": true
      }
    ]
  }
}
```
{% endcode %}

</details>







