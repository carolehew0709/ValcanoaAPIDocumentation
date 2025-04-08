# Addresses

## Query All Address

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/address/query%7B?current,pageSize}"><code>https://api.decenctype.com/cards/address/query{?current,pageSize}</code></a></summary>

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
    "total": 3,
    "address": [
      {
        "delivery_address_id": "44578890-32c8-11ef-9902-27d134165673",
        "user_id": "5d4ad700-0a69-482f-8786-2e321079f247",
        "recipient_title": "Mr",
        "recipient_first_name": "Yang",
        "recipient_last_name": "Zhijie",
        "phone_area_code": "86",
        "phone_number": "1234567",
        "address_country": "China",
        "address_state": "",
        "address_city": "Shanghai",
        "address_line": "Pudong",
        "address_postcode": "200125",
        "createdAt": "2024-06-25T07:55:19.000Z",
        "updatedAt": "2024-06-25T07:55:19.000Z"
      },
    ],
    "current": 1,
    "pageSize": 10
  }
}
```
{% endcode %}



</details>

## Query One Address

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/address/get/%7Bdelivery_address_id%7D"><code>https://api.decenctype.com/cards/address/get/{delivery_address_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| delivery\_address\_id | Delivery address ID |
| --------------------- | ------------------- |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "delivery_address_id": "b1c23150-2c7e-11ef-ad43-31099195148a",
    "user_id": "5d4ad700-0a69-482f-8786-2e321079f247",
    "recipient_title": "Mr",
    "recipient_first_name": "Zhijie",
    "recipient_last_name": "Yang",
    "phone_area_code": "886",
    "phone_number": "123456789",
    "address_country": "TW",
    "address_state": "TPE",
    "address_city": "Taipei City",
    "address_line": "AAAA",
    "address_postcode": "1234",
    "createdAt": "2024-06-17T07:53:33.000Z",
    "updatedAt": "2024-06-17T07:53:33.000Z"
  }
}
```
{% endcode %}

</details>

## Create Delivery Address

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/address/create"><code>https://api.decenctype.com/cards/address/create</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

<pre class="language-json"><code class="lang-json">{
<strong>  "user_id": "",
</strong>  "recipient_title": "Mr",
  "recipient_first_name": "Foo",
  "recipient_last_name": "Bar",
  "phone_area_code": "886",
  "phone_number": "098765432",
  "address_country": "TWN",
  "address_city": "Taipei",
  "address_line": "Line1",
  "address_postcode": "100"
}
</code></pre>

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "DeliveryAddress created successfully.",
  "data": {
    "delivery_address_id": "44578890-32c8-11ef-9902-27d134165673",
    "user_id": "5d4ad700-0a69-482f-8786-2e321079f247",
    "recipient_title": "Mr",
    "recipient_first_name": "Yang",
    "recipient_last_name": "Zhijie",
    "phone_area_code": "86",
    "phone_number": "1234567",
    "address_country": "China",
    "address_state": "",
    "address_city": "Shanghai",
    "address_line": "Pudong",
    "address_postcode": "200125",
    "updatedAt": "2024-06-25T07:55:19.321Z",
    "createdAt": "2024-06-25T07:55:19.321Z"
  }
}
```
{% endcode %}



</details>







