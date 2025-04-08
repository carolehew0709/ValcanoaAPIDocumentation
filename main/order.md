# Order

## Create Transfer Order by User

> Transfer crypto or fiat from master account to user, do not require approval from a higher-level administrator.

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark> <a href="https://api.decenctype.com/orders/transfer/create"><code>https://api.decenctype.com/orders/transfer/create</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

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
    "order_id": "2109a430-48c2-11ef-9f61-974f59dba5d2",
    "transfer_account": "5d4ad700-0a69-482f-8786-2e321079f247",
    "pay_account_id": "07371ce1-ff6b-11ee-bc93-6382caed923a",
    "receive_account_id": "99803ad2-11e7-11ef-8140-99c4f5b8d784",
    "amount": 100,
    "currency": "USDT",
    "user_id": "5d4ad700-0a69-482f-8786-2e321079f247",
    "admin_id": "1",
    "order_status": "approved",
    "updated_at": "2024-07-23T07:06:49.583Z",
    "created_at": "2024-07-23T07:06:48.692Z"
  }
}
```
{% endcode %}



</details>

