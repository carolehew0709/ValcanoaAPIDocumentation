# KYC

## Query All KYC Orders

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/orders/kyc/query%7B?current,pageSize}"><code>https://api.decenctype.com/orders/kyc/query{?current,pageSize}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| current  | Page                     |
| -------- | ------------------------ |
| pageSize | Number of items per page |

#### Response

{% code title="200 OK" %}
```json
{
    "success": true,
    "total": 26,
    "data": [
        {
            "order_id": "52ebabb0-0947-11f0-8461-7536c68372cb",
            "user_id": "441d7520-0945-11f0-8461-7536c68372cb",
            "first_name": "foooo",
            "last_name": "barrrr",
            "nationality": "TWN",
            "city": "Taipei",
            "line1": "Somestreet",
            "line2": "Somedistrict",
            "postalCode": "100",
            "dob": "",
            "documentType": "passport",
            "documentNumber": "123456789",
            "documentImage": null,
            "order_status": "approved",
            "reason": null,
            "admin_id": "6",
            "created_at": "2025-03-25T07:03:58.000Z",
            "updated_at": "2025-03-25T07:04:19.000Z",
            "user": {
                "user_id": "441d7520-0945-11f0-8461-7536c68372cb",
                "email": "b@c.com",
                "phone_num": null,
                "number": 1073,
                "is_kyc_1": true,
                "is_kyc_2": false
            }
        }
    ],
    "current": 1,
    "pageSize": 1
}
```
{% endcode %}



</details>

## Check KYC Order

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/orders/kyc/check%7B?user_id}"><code>https://api.decenctype.com/orders/kyc/check{?user_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| user\_id | [User ID](https://volcanopay.docs.apiary.io/#/reference/users/query-all-users) of the KYC order you want to check |
| -------- | ----------------------------------------------------------------------------------------------------------------- |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "order_id": "18a0b2b0-0dae-11ef-8140-99c4f5b8d784",
    "user_id": "5d4ad700-0a69-482f-8786-2e321079f247",
    "first_name": "Zhijie",
    "last_name": "Yang",
    "nationality": "hk",
    "city": "",
    "line1": "",
    "line2": null,
    "postalCode": "",
    "dob": "",
    "documentType": "national_id",
    "documentNumber": "123321234567890987",
    "documentImage": "",
    "order_status": "approved",
    "admin_id": "3",
    "created_at": "2024-05-09T02:44:46.000Z",
    "updated_at": "2024-05-14T03:27:48.000Z"
  }
}
```
{% endcode %}



</details>

## Create KYC Order

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/orders/kyc/create"><code>https://api.decenctype.com/orders/kyc/create</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

Body

```javascript
{
  "user_id": "",
  "first_name": "Foo",
  "last_name": "Bar",
  "dob": "",
  "nationality": "TWN",
  "city": "Taipei",
  "line1": "Somestreet",
  "line2": "Somedistrict",
  "postal_code": "100",
  "document_type": "passport",
  "document_number": "123456789"
}
```

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "KYC order created successfully",
  "data": {
    "order_id": "18a0b2b0-0dae-11ef-8140-99c4f5b8d784",
    "user_id": "5d4ad700-0a69-482f-8786-2e321079f247",
    "first_name": "Zhijie",
    "last_name": "Yang",
    "nationality": "hk",
    "city": "",
    "line1": "",
    "line2": null,
    "postalCode": "",
    "dob": "",
    "documentType": "national_id",
    "documentNumber": "123321234567890987",
    "documentImage": "",
    "order_status": "pending",
    "admin_id": "",
    "created_at": "2024-05-09T02:44:46.000Z",
    "updated_at": "2024-05-14T03:27:48.000Z"
  }
}
```
{% endcode %}



</details>

## Approve KYC

> **Just for CRM usage for now**

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/admin/approveKYC"><code>https://api.decenctype.com/admin/approveKYC</code></a></summary>

#### **Headers**

| Name         | Value              |
| ------------ | ------------------ |
| Content-Type | `application/json` |
| X-API-KEY    | `Your-API-Key`     |

Body

```javascript
{
  "order_id": "",
  "status": ""
}
```

#### Response

{% code title="200 OK" %}
```javascript
{
  "message": "KYC approved and accounts created successfully for user ID: 319bf1f0-3f4d-11ef-a5a0-c13e3c4439ae."
}
```
{% endcode %}



</details>
