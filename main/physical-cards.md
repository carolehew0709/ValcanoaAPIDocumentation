# Physical Cards

## Follow the steps to create a physical card&#x20;

1. [Create a card order](card.md#create-card-order) with a physical card product ID.
2. [Bulk ship the card](physical-cards.md#bulk-ship-physical-card) with the card ID you get in list or from the webhook, and before you could make the shipment, you should [create an delivery address](addresses.md#create-delivery-address) for the `addressId`.
3. Query the shipping order with the card ID or [Query the shipping order](physical-cards.md#get-physical-card-shipping-order-by-bulkship-id) with `bulkShipId`.
4. [Activate the card](physical-cards.md#activate-physical-card) with `pan`, `cvv` and `expiry_date` after receiving the card.
5. _(Optional)_ [Update the PIN](physical-cards.md#update-pin) for the card.

## Get Physical Card Shipping Order

> Use this to track the shipping order of a newly created card.

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/item/shipment?{card_id}"><code>https://api.decenctype.com/cards/item/shipment{?card_id}</code></a></summary>

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
    "message": "",
    "data": {}
}
```
{% endcode %}

</details>

## Get Physical Card Shipping Order by Bulkship ID

> Use this to retrieve the shipping information, tracking number and cardID of the given batch of shipped cards.

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/bulkship/orders?{bulkShipId}"><code>https://api.decenctype.com/cards/bulkship/orders{?bulkShipId}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| bulkShipId | Bulkship ID |
| ---------- | ----------- |

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

## Activate Physical Card

> You could pass `card_id` or `pan` and `cvv` and `expiry_date` to activate a physical card.

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/item/activate"><code>https://api.decenctype.com/cards/item/activate</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "card_id": "fasff3asge3sfsa",
  "pan": "123423543523",
  "cvv": "123",
  "code": "324as",
  "expiry_date": "11/27",
  "type": "reap"
}
```

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "Card activated successfully.",
  "data": {}
}
```
{% endcode %}

</details>

## Get Activation Code for Physical Card

> This endpoint is required to activate the physical card.

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/cards/activation-code/%7Bcard_id%7D"><code>https://api.decenctype.com/cards/activation-code/{card_id}</code></a></summary>

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
    "message": "Activation code retrieved successfully.",
    "data": {}
}
```
{% endcode %}

</details>

## Update PIN

> Pin number rules:
>
> * Only 4-12 digits long
> * Cannot have three or more in sequence (eg. 123674)
> * Cannot have three or more repeat in a row (111441)

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/pin/%7Bcard_id%7D"><code>https://api.decenctype.com/cards/pin/{card_id}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| card\_id | Card ID |
| -------- | ------- |

#### Body

```json
{
  "card_id": "",
  "pin": ""
}
```

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "PIN updated successfully.",
    "data": {}
}
```
{% endcode %}



</details>

## Bulk Ship Physical Card

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/cards/bulk-ship"><code>https://api.decenctype.com/cards/bulk-ship</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "bulkShipId": "fasff3asge3sfsa",
  "cardIds": "123423543523",
  "addressId": "123",
  "email": "324as",
  "cardDesignId": "d142fda"
}
```

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "Submit successfully.",
  "data": {}
}
```
{% endcode %}

</details>



















