# Card

## Query All Cards

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/item/list/query%7B?current,pageSize}"><code>https://api.decenctype.com/cards/item/list/query{?current,pageSize}</code></a></summary>

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
    "total": 90,
    "users": [
      {
        "user_id": "c94ae5dc-a021-7017-9fa3-b8f3350fd2de",
        "first_name": "First",
        "last_name": "Last",
        "number": 70,
        "nationality": "ua",
        "status": "active",
        "is_kyc_1": true,
        "is_kyc_2": false,
        "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
        "cards": [
          {
            "card_id": "4efc150b-68b9-4289-b27b-32c4ad4d1c0a",
            "account_balance": "****",
            "currency": "USD",
            "status": "ACTIVE",
            "card_product_id": "582ae1e1-c231-4534-8f32-22866cd5bdbf",
            "pan": "****",
            "nameOnCard": "****"
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

## Query All Cards 2

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/item/list/query2%7B?current,pageSize,user_id,card_id}"><code>https://api.decenctype.com/cards/item/list/query2{?current,pageSize,user_id,card_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| current  | <p>Page</p><p>Example: 1</p>                                                      |
| -------- | --------------------------------------------------------------------------------- |
| pageSize | <p>Number of items per page</p><p>Example: 5</p>                                  |
| user\_id | <p>a021-7017-9fa3-b8f3350fd2de - User Id</p><p><code>Example: c94ae5dc</code></p> |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "total": 90,
    "cards": [
      {
        "card_id": "4efc150b-68b9-4289-b27b-32c4ad4d1c0a",
        "account_balance": "****",
        "currency": "USD",
        "status": "ACTIVE",
        "card_product_id": "582ae1e1-c231-4534-8f32-22866cd5bdbf",
        "pan": "****",
        "nameOnCard": "****"
      }
    ],
    "current": 1,
    "pageSize": 10
  }
}
```
{% endcode %}

</details>

## Query One Card

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/item/info/%7Bcard_id%7D"><code>https://api.decenctype.com/cards/item/info/{card_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| card\_id | Card ID |
| -------- | ------- |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "card_id": "CA1598545220075552",
    "pan": "5246042608430844",
    "nameOnCard": "Zhijie Yang",
    "account_balance": "869.52",
    "amount_top_up": "0.00",
    "amount_spent": "12.10",
    "currency": "EUR",
    "type": "VIRTUAL_CARD",
    "activate_code": "908930558379",
    "status": "ACTIVE",
    "card_product_id": "2483fbc5-db82-4e8c-8761-1bfd79fb3afc",
    "user_id": "924ec136-d2be-403e-8303-b1f8e1882870",
    "tag_id": "41e85407-56f3-471e-9958-dbc39f3f30d2",
    "createdAt": "2024-02-26T06:56:00.000Z",
    "updatedAt": "2024-06-12T05:52:24.000Z",
    "card_product": {
      "card_product_id": "2483fbc5-db82-4e8c-8761-1bfd79fb3afc",
      "issuer": "OUITRUST",
      "status": "INACTIVE",
      "product": "Virtual-Master-EUR",
      "price": 19,
      "currency": "USD",
      "type": "VIRTUAL_CARD",
      "card_design": "BLACK",
      "is_global": true
    },
    "tag": {
      "tag_id": "41e85407-56f3-471e-9958-dbc39f3f30d2",
      "title": "Leisure",
      "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
      "created_at": "2024-05-01T12:46:35.000Z",
      "updated_at": "2024-05-28T15:04:24.000Z"
    }
  }
}
```
{% endcode %}

</details>

## Create Card Order

> Create card order for your user, pay them automatically using the USDT balance of the master account.

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/order/create"><code>https://api.decenctype.com/cards/order/create</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "user_id": "",
  "deliveryAddressId": "",
  "billingAddressId": "",
  "cardProductId": ""
}
```

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": "Your card paid successfully, and it's being processed."
}
```
{% endcode %}

</details>



## Pay Card Order

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/order/pay"><code>https://api.decenctype.com/cards/order/pay</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "orderCardId": "sre2r",
  "payAccountId": "dasdsadsa",
  "accountType": "crypto"
}
```

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": "Your card paid successfully, and it's being processed."
}
```
{% endcode %}

</details>

## Activate Card

> The activation endpoint for physical cards can be found [here](physical-cards.md#activate-physical-card).
>
> The virtual card is activated by us in advance, you can just update the cvv and other security information for the card [here.](card.md#update-card)

## Delete Card

> We do not provide an endpoint to delete card, please use [lock card](card.md#lock-card) instead.

## Update Card

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/item/update"><code>https://api.decenctype.com/cards/item/update</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "card_id": "",
  "pan": "41448888888889999",
  "expire_date": "07/27",
  "cvv": "123",
  "pin": "321"
}
```

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "Card updated successfully.",
  "data": {
    "card_id": "CA1598545220075552",
    "pan": "5246042608430844",
    "nameOnCard": "Zhijie Yang",
    "account_balance": "869.52",
    "amount_top_up": "0.00",
    "amount_spent": "12.10",
    "currency": "EUR",
    "type": "VIRTUAL_CARD",
    "activate_code": "908930558379",
    "status": "ACTIVE",
    "card_product_id": "2483fbc5-db82-4e8c-8761-1bfd79fb3afc",
    "user_id": "924ec136-d2be-403e-8303-b1f8e1882870",
    "tag_id": "41e85407-56f3-471e-9958-dbc39f3f30d2",
    "createdAt": "2024-02-26T06:56:00.000Z",
    "updatedAt": "2024-06-12T05:52:24.000Z",
    "card_product": {
      "card_product_id": "2483fbc5-db82-4e8c-8761-1bfd79fb3afc",
      "issuer": "OUITRUST",
      "status": "INACTIVE",
      "product": "Virtual-Master-EUR",
      "price": 19,
      "currency": "USD",
      "type": "VIRTUAL_CARD",
      "card_design": "BLACK",
      "is_global": true
    }
}
```
{% endcode %}

</details>

## Update Card Nickname

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/update/alias"><code>https://api.decenctype.com/cards/update/alias</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "card_id": "",
  "alias": "foo bar"
}
```

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "Card updated successfully.",
  "data": {
    "card_id": "CA1598545220075552",
    "pan": "5246042608430844",
    "nameOnCard": "Zhijie Yang",
    "account_balance": "869.52",
    "amount_top_up": "0.00",
    "amount_spent": "12.10",
    "currency": "EUR",
    "type": "VIRTUAL_CARD",
    "activate_code": "908930558379",
    "status": "ACTIVE",
    "card_product_id": "2483fbc5-db82-4e8c-8761-1bfd79fb3afc",
    "user_id": "924ec136-d2be-403e-8303-b1f8e1882870",
    "tag_id": "41e85407-56f3-471e-9958-dbc39f3f30d2",
    "createdAt": "2024-02-26T06:56:00.000Z",
    "updatedAt": "2024-06-12T05:52:24.000Z",
    "card_product": {
      "card_product_id": "2483fbc5-db82-4e8c-8761-1bfd79fb3afc",
      "issuer": "OUITRUST",
      "status": "INACTIVE",
      "product": "Virtual-Master-EUR",
      "price": 19,
      "currency": "USD",
      "type": "VIRTUAL_CARD",
      "card_design": "BLACK",
      "is_global": true
    }
}
```
{% endcode %}

</details>

## Query Card Security Info

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/item/security%7B?card_id}"><code>https://api.decenctype.com/cards/item/security{?card_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| card\_id | Card ID |
| -------- | ------- |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "card_id": "CA1598545220075552",
    "pin": "****",
    "cvv": "***",
    "expiry_date": "**/**",
    "pan": "**********"
  }
}
```
{% endcode %}

</details>

## Reissue Card

> This endpoint allows you to generate a new PAN, CVV and expiry date for a given card.

<details>

<summary><mark style="color:orange;"><code>PUT</code></mark><a href="https://api.decenctype.com/cards/replace/%7Bcard_id%7D"><code>https://api.decenctype.com/cards/replace/{card_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "card_id": ""
}
```

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "Successfully reissued card.",
    "data": {}
}
```
{% endcode %}

</details>

## Query Card Top Up History

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/balance%7B?card_id,current,pageSize}"><code>https://api.decenctype.com/cards/balance{?card_id,current,pageSize}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| card\_id | Card ID                                                       |
| -------- | ------------------------------------------------------------- |
| current  | <p>Page</p><p><code>Example: 1</code></p>                     |
| pageSize | <p>Number of items per page</p><p><code>Example: 5</code></p> |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "",
  "data": {}
}
```
{% endcode %}

</details>

## Top Up Card

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/increase-balance"><code>https://api.decenctype.com/cards/increase-balance</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "card_id": "",
  "amount": 5,
  "remark": "Test",
  "account_id": "",
  "account_type": "crypto"
}
```

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "OK",
    "data": 871.2
}
```
{% endcode %}

</details>

## Lock Card

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/item/lock/%7Bcard_id%7D"><code>https://api.decenctype.com/cards/item/lock/{card_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "card_id": ""
}
```

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "Card locked successfully.",
    "data": {
        "cardId": "CA1598545220075552",
        "cardStatus": "LOCKED"
    }
}
```
{% endcode %}

</details>

## Unlock Card

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/item/unlock/%7Bcard_id%7D"><code>https://api.decenctype.com/cards/item/unlock/{card_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "card_id": ""
}
```

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "Card unlocked successfully.",
    "data": {
        "cardId": "CA1598545220075552",
        "cardStatus": "ACTIVE"
    }
}
```
{% endcode %}

</details>

## Update Card Email

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/email/%7Bcard_id%7D"><code>https://api.decenctype.com/cards/email/{card_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "card_id": "",
  "email": "a@b.com"
}
```

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "Card email updated successfully.",
    "data": {}
}
```
{% endcode %}

</details>

## Update Card Phone Number

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/phone/%7Bcard_id%7D"><code>https://api.decenctype.com/cards/phone/{card_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "card_id": "",
  "dialCode": "886",
  "phoneNumber": "098765432"
}
```

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "Card phone updated successfully.",
    "data": {}
}
```
{% endcode %}

</details>

## Withdraw from Card

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/item/withdraw"><code>https://api.decenctype.com/cards/item/withdraw</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "card_id": "123",
  "amount": 123
}
```

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "Card withdraw successfully.",
  "data": {}
}
```
{% endcode %}

</details>

## Query Card Id by Pan

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/item/cardId%7B?pan,cvv}"><code>https://api.decenctype.com/cards/item/cardId{?pan,cvv}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "pan": "123124124214214",
  "cvv": "124",
  "expiry_date": "11/27"
}
```

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "CardId retrieved successfully.",
  "data": [
    {
        "card_id": "4efc150b-68b9-4289-b27b-32c4ad4d1c0a",
        "account_balance": "****",
        "currency": "USD",
        "status": "ACTIVE",
        "card_product_id": "582ae1e1-c231-4534-8f32-22866cd5bdbf",
        "pan": "****",
        "nameOnCard": "****"
    }
  ]
}
```
{% endcode %}

</details>

## Get 3DS status of a card

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/item/3ds/%7B?card_id}"><code>https://api.decenctype.com/cards/item/3ds/{?card_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| card\_id | <p>ID of the card</p><p><code>Example: asdad33-asasfsaf-dasdas</code></p> |
| -------- | ------------------------------------------------------------------------- |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "Ok.",
  "data": {}
}
```
{% endcode %}

</details>

## Update 3DS method of a card

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/item/3ds/%7Bcard_id%7D"><code>https://api.decenctype.com/cards/item/3ds/{card_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| card\_id | <p>ID of the card</p><p><code>Example: asdad33-asasfsaf-dasdas</code></p> |
| -------- | ------------------------------------------------------------------------- |

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "Ok.",
    "data": {}
}
```
{% endcode %}

</details>

## Get 3DS Verification List

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/item/auth/list%7B?card_id,current,pageSize}"><code>https://api.decenctype.com/cards/item/auth/list{?card_id,current,pageSize}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| current  | <p>Page</p><p><code>Example: 1</code></p>                                |
| -------- | ------------------------------------------------------------------------ |
| pageSize | <p>Number of items per page</p><p><code>Example: 10</code></p>           |
| card\_id | <p>ID of the card</p><p><code>Example: asdad33-asasfsaf-dasda</code></p> |

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "Ok.",
    "data": [
        {
            "card_id": "dadafae-3dfdasfe-fsffwf",
            "initiate_action_id": "asd2wd-2wdadewf-232cdss",
            "status": "PENDING",
            "details": {
              "cardId": "dadafae-3dfdasfe-fsffwf",
              "status": "PENDING",
              "merchantName": "dasdadas",
              "initiateActionId": "asd2wd-2wdadewf-232cdss",
              "transactionAmount": 200,
              "merchantCountryCode": "CHN",
              "transactionCurrency": "CNY",
              "transactionTimestamp": "2024-11-19 08:00:00",
            },
            "merchant_id": "112ewdqwdw0-sadada-dad3d",
            "created_at": "2024-11-19 08:00:00",
            "updated_at: "2024-11-19 08:00:00",
        }
    ]
}
```
{% endcode %}

</details>

## Respond 3DS Verification

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/item/3ds/verify/%7Bcard_id%7D"><code>https://api.decenctype.com/cards/item/3ds/verify/{card_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| card\_id | <p>ID of the card</p><p><code>Example: asdad33-asasfsaf-dasda</code></p> |
| -------- | ------------------------------------------------------------------------ |

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "Ok.",
    "data": {}
}
```
{% endcode %}

</details>

## Bind card with last4

> This endpoint only support cards were not published from the system (especially **bulk created manually**) .

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/item/bind"><code>https://api.decenctype.com/cards/item/bind</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "Ok.",
    "data": {}
}
```
{% endcode %}

</details>









































