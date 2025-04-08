# Transaction

Enum types of <mark style="color:red;">`type`</mark> in the returned data:

* **DEPOSIT** : Funds deposited into an account.
* **WITHDRAWAL**: Funds withdrawn from an account.
* **CARD\_PAYMENT**: Payments made using a card.
* **REFUND**: Return of previously paid funds.
* **COMPLETED**: Transactions successfully finished.
* **APPROVED**: Transactions approved to proceed.
* **PENDING**: Transactions awaiting processing.
* **FAILED**: Transactions that did not succeed.
* **CLEARED**: Transactions that have been settled.
* **AUTHORIZATION**: Transactions requiring approval.
* **REVERSAL**: Transactions that have been undone.
* **ORIGINAL\_CREDIT**: Initial credit transactions, often refunds.



Enum types of <mark style="color:red;">`status`</mark> in the returned data:

* **PENDING**: Transactions that are in processing, would be updated later.
* **APPROVED**: Transactions approved to proceed with type <mark style="color:red;">`AUTHORIZATION`</mark>.
* **CLEARED**: Transactions that have been CLEARED by upstream.
* **FAILED**: Transactions did not succeed.
* **COMPLETED**: Transactions successfully finished.
* **CANCELED**: Transactions were CANCELLED.
* **AUTHORIZED**: Transactions that have been AUTHORIZED by upstream.
* **REJECTED**: Transactions that have been REJECTED by upstream.
* **DECLINED**: Transactions that have been DECLINED by upstream.



## Query All Transactions for All Cards

> The <mark style="color:red;">`mcc`</mark> field would show when there was merchant data from upstream. And the <mark style="color:red;">`failure_reason`</mark> field would show when the transaction was in a status of <mark style="color:red;">`FAILED`</mark> or <mark style="color:red;">`REJECTED`</mark> or <mark style="color:red;">`DECLINED`</mark>

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/merchants/transaction/list%7B?current,pageSize,showAll,start,end}"><code>https://api.decenctype.com/merchants/transaction/list{?current,pageSize,showAll,start,end}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| current  | <p>Page</p><p><code>Example: 1</code></p>                                                                                   |
| -------- | --------------------------------------------------------------------------------------------------------------------------- |
| pageSize | <p>Number of items per page</p><p><code>Example: 3</code></p>                                                               |
| showAll  | <p>Whether to ignore start and end dates and display all transactions, default is true</p><p><code>Example: true</code></p> |
| start    | <p>Starting date, format in [string, number, Date]</p><p><code>Example: 2024/1/1 08:00:00</code></p>                        |
| end      | <p>Ending date, format in [string, number, Date]</p><p><code>Example: 2024/12/31 08:00:00</code></p>                        |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "count": 716,
    "rows": [
      {
        "transaction_id": "8767e620-4f48-4d17-9e39-a75127a6e372",
        "network_transaction_id": "304207643310680",
        "type": "CLEARING",
        "card_id": "ed11121f-942d-4cd2-9515-78b6339236ec",
        "amount": "-1093.00",
        "currency": "DKK",
        "amount_cleared": "-160.77",
        "currency_cleared": "USD",
        "status": "APPROVED",
        "review": "PENDING",
        "timestamp": "2024-07-25T17:52:11.000Z",
        "timestamp_cleared": "2024-07-26T00:56:23.000Z",
        "mcc": {
            "merchant_name": "ALP*****",
            "merchant_country": "CHN"
          },
        "failure_reason": null,
      }
    ]
  }
}
```
{% endcode %}

</details>

## Query All Transactions for One Card

> The <mark style="color:red;">`mcc`</mark> field would show when there was merchant data from upstream. And the <mark style="color:red;">`failure_reason`</mark> field would show when the transaction was in a status of <mark style="color:red;">`FAILED`</mark> or <mark style="color:red;">`REJECTED`</mark> or <mark style="color:red;">`DECLINED`</mark>

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/merchants/transaction/list%7B?current,pageSize,showAll,start,end}"><code>https://api.decenctype.com/merchants/transaction/card{?current,pageSize,showAll,start,end}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| current  | <p>Page</p><p><code>Example: 1</code></p>                                                                                   |
| -------- | --------------------------------------------------------------------------------------------------------------------------- |
| pageSize | <p>Number of items per page</p><p><code>Example: 3</code></p>                                                               |
| showAll  | <p>Whether to ignore start and end dates and display all transactions, default is true</p><p><code>Example: true</code></p> |
| start    | <p>Starting date, format in [string, number, Date]</p><p><code>Example: 2024/1/1 08:00:00</code></p>                        |
| end      | <p>Ending date, format in [string, number, Date]</p><p><code>Example: 2024/12/31 08:00:00</code></p>                        |

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "OK",
    "data": {
        "total": 27,
        "transactions": [
            {
                "transaction_id": "CTX1602324069875744",
                "network_transaction_id": null,
                "type": "CARD_ONLINE_PAYMENTS",
                "card_id": "CA1598545220075552",
                "amount": "0.90",
                "currency": "CNY",
                "amount_cleared": "0.12",
                "currency_cleared": "EUR",
                "status": "AUTHORIZED",
                "review": "PENDING",
                "timestamp": "2024-03-18T03:27:35.000Z",
                "timestamp_cleared": "2024-03-18T03:27:35.000Z",
                "mcc": {
                    "merchant_name": "ALP*****",
                    "merchant_country": "CHN"
                  },
                "failure_reason": null,
            },
        ],
        "current": 2,
        "pageSize": 10
    }
}
```
{% endcode %}

</details>

## Query One Transaction

> The <mark style="color:red;">`mcc`</mark> field would show when there was merchant data from upstream. And the <mark style="color:red;">`failure_reason`</mark> field would show when the transaction was in a status of <mark style="color:red;">`FAILED`</mark> or <mark style="color:red;">`REJECTED`</mark> or <mark style="color:red;">`DECLINED`</mark>

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/transaction/card/%7Btransaction_id%7D"><code>https://api.decenctype.com/transaction/card/{transaction_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| transaction\_id | Transaction ID |
| --------------- | -------------- |

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "success": true,
    "data": {
      "transaction_id": "CTX1602342000525344",
      "network_transaction_id": null,
      "type": "CARD_ONLINE_PAYMENTS",
      "card_id": "CA1598545220075552",
      "amount": "5.50",
      "currency": "CNY",
      "amount_cleared": "0.72",
      "currency_cleared": "EUR",
      "status": "AUTHORIZED",
      "review": "PENDING",
      "timestamp": "2024-03-18T05:50:06.000Z",
      "timestamp_cleared": "2024-03-18T05:50:06.000Z",
      "mcc": {
        "merchant_name": "ALP*****",
        "merchant_country": "CHN"
      },
      "failure_reason": null,
    }
  }
}
```
{% endcode %}



</details>







