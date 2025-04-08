# Webhooks

Volcano API provides webhooks to allow you to receive real-time notifications of events. You can subscribe to all available webhooks by using the subscribe endpoint below.

## Subscribe To Webhooks

> Receive transaction events and notifications to facilitate your required actions and response.

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/merchants/webhook/register"><code>https://api.decenctype.com/merchants/webhook/register</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "webhook_url": "",
  "merchant_id": ""
}
```

#### Response

{% code title="200 OK" %}
```json
{
  "code": 200,
  "message": "Successfully subscribed to webhooks!",
  "data": null
}
```
{% endcode %}

</details>

## Webhook Events

> Currently, there are 4 event types, which are card, transaction, authorization, and shipping.

### User

### KYC Status

> The `KYC status` webhook is triggered when the status of a KYC order changes.

```json
{
  "eventType": "user",
  "eventName": "kyc_status",
  "data": {
    "order_id": "00d126f0-1bf1-11ef-841f-6d72f33e3ee9",
    "status": "approved"
  }
}
```

| Status   | Description               |
| -------- | ------------------------- |
| approved | The kyc order is approved |
| rejected | The kyc order is rejected |

### Card Status

> The `card status` webhook is triggered when the status of a card changes.

```json
{
  "eventType": "card",
  "eventName": "card_status",
  "data": {
    "card_id": "e3b45865-8bc1-4ac7-9eb2-6c520bc9a545",
    "order_id": "00d126f0-1bf1-11ef-841f-6d72f33e3ee9",
    "status": "CREATED"
  }
}
```

The status can be one of the following :&#x20;

| Status   | Description                                       |
| -------- | ------------------------------------------------- |
| CREATED  | The card is created and reaches available status  |
| ACTIVE   | 3 attempts for incorrect transaction PIN are made |
| INACTIVE | 3 attempts for incorrect transaction PIN are made |

### Card Activation

> The `card activation` webhook is triggered when the status of a card changes.

```json
{
  "eventType": "card",
  "eventName": "card_activation",
  "data": {
    "card_id": "e3b45865-8bc1-4ac7-9eb2-6c520bc9a545",
    "order_id": "00d126f0-1bf1-11ef-841f-6d72f33e3ee9",
    "status": "CREATED",
    "merchant_id": "122142352-12425345-65464564747"
  }
}
```

The status can be one of the following:

| Status | Description                                      |
| ------ | ------------------------------------------------ |
| ACTIVE | The card is created and reaches available status |

### Bulk Shipment

> The `bulk shipment` webhook is triggered when bulk shipment order for cards was created

```json
{
  "eventType": "card",
  "eventName": "bulk_shipment",
  "data": {
    "bulk_ship_id": "e3b45865-8bc1-4ac7-9eb2-6c520bc9a545",
    "card_ids": ["00d126f0-1bf1-11ef-841f-6d72f33e3ee9"],
    "address_id": "12edasdsf-fasfe-fdasfasfa-12e1",
    "email": "test@example.com",
    "success_count": 1,
    "remain_slots": 99,
    "cuf_off_date": "deadline for the order",
    "merchant_id": "122142352-12425345-65464564747"
  }
}
```

### Order Card Status

> The `Order card status` webhook is triggered when the status of a card order changes.

```json
{
  "eventType": "order",
  "eventName": "order_card_status",
  "data": {
    "order_id": "00d126f0-1bf1-11ef-841f-6d72f33e3ee9",
    "status": "refunded"
  }
}
```

| Status    | Description                      |
| --------- | -------------------------------- |
| unpaid    | The order is pending for payment |
| cancelled | The order is cancelled           |
| paid      | The kyc order is paid            |
| refunded  | The order is refunded            |

### Order Deposit

> The `Order deposit` webhook is triggered when the crypto deposit happens

```json
{
  "eventType": "order",
  "eventName": "deposit",
  "data": {
    "type": "merchant",
    "user_id": null,
    "order_id": "b46da970-ed35-11ef-abb7-b9b0636b7055",
    "created_at": "2025-02-17T13:47:18.792Z",
    "updated_at": "2025-02-17T13:47:18.792Z",
    "crypto_chain": "195",
    "hash_deposit": "e173171f37c92d4055a908c36dabea2fcffb8e3af35113fd53e992e303dac3eb",
    "order_status": "pending",
    "account_token": "USDT-TRC20",
    "account_crypto_id": "caa26d32-7584-11ef-b20f-cb555f132c88",
    "account_address_in": "TBSrKTGB7kBtEM51LzowykKEGH3LvUX4Wq",
    "amount_deposit_crypto": "0.010001"
  }
}
```

### Transaction

> The `transaction` webhook is triggered when a transaction event is performed.

```json
{
  "eventType": "transaction",
  "eventName": "authorization",
  "data": {
      "transaction_id": "tid_saewaftax",
      "network_transaction_id": null,
      "type": "authorization",
      "card_id": "sd324-324fs-fgs32ds-5452f",
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
```

The type can be one of the following:

| Type             | Description                                |
| ---------------- | ------------------------------------------ |
| DEPOSIT          | Funds deposited into an account            |
| WITHDRAWAL       | Funds withdrawn from an account            |
| CARD\_PAYMENT    | Payments made using a card                 |
| REFUND           | Return of previously paid funds            |
| COMPLETED        | Transactions successfully finished         |
| APPROVED         | Transactions approved to proceed           |
| PENDING          | Transactions awaiting processing           |
| FAILED           | Transactions that did not succeed          |
| CLEARED          | Transactions that have been settled        |
| AUTHORIZATION    | Transactions requiring approval            |
| REVERSAL         | Transactions that have been undone         |
| ORIGINAL\_CREDIT | Initial credit transactions, often refunds |

The status can be one of the following:

| Status   | Description                                                |
| -------- | ---------------------------------------------------------- |
| PENDING  | The transaction is awaiting further action or confirmation |
| CLEARED  | The transaction has been authorized and approved           |
| DECLINED | The transaction has been declined or rejected              |
| VOID     | The transaction has fully reversed or refunded             |

### 3ds Verification

> The `3ds` webhook is triggered when 3ds security event is performed.

```json
{
  "eventType": "transaction",
  "eventName": "3ds",
  "data": {
      "status": "PENDING",
      "card_id": "01292d5b-5ee4-4502-bb84-9b69623baad4",
      "createdAt": "2025-02-21T11:10:17.616Z",
      "updatedAt": "2025-02-21T11:10:17.616Z",
      "merchant_name": "UOBT - IDP EDUCATION",
      "initiate_action_id": "8c2b6635-2b42-4600-8d78-8bd0a610fbf1",
      "transaction_amount": "7650.0000",
      "transaction_currency": "THB",
      "merchant_country_code": "THA",
      "transaction_timestamp": "2025-02-21T11:10:03.904Z"
  }
}
```



















