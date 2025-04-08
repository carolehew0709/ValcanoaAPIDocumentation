# Simulate

A test environment is made available to customers to facilitate seamless integration. Within this environment, transaction simulation endpoints are established specifically for testing purposes. These endpoints are designed to allow you to evaluate the functionality of the cards you have generated in the test environment and write test cases to ensure the stability of your integration.

It's important to note that unlike the production environment, the test environment does not establish communication with actual card networks. Consequently, any cards generated are incapable of conducting real-world transactions.

Volcano API's test environment provides a suite of endpoints that enable the simulation of diverse card network transactions, encompassing actions like authorizations, reversals, clearings, and refunds.

## Simulate Authorisation Transaction

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/simulate/authorisation"><code>https://api.decenctype.com/simulate/authorisation</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "cardID": "",
  "billAmount": 0
}
```

#### Response

{% code title="200 OK" %}
```json
```
{% endcode %}



</details>

## Simulate Authorisation Clearing Transaction

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/users/query%7B?current,pageSize}"><code>https://api.decenctype.com/users/query{?current,pageSize}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| current  | Page                     |
| -------- | ------------------------ |
| pageSize | Number of items per page |

#### Body

```
// Some code
```

#### Response

{% code title="200 OK" %}
```json

    }
}
```
{% endcode %}



</details>

## Simulate Authorisation Refund Transaction

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/users/query%7B?current,pageSize}"><code>https://api.decenctype.com/users/query{?current,pageSize}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| current  | Page                     |
| -------- | ------------------------ |
| pageSize | Number of items per page |

#### Body

```
// Some code
```

#### Response

{% code title="200 OK" %}
```json

    }
}
```
{% endcode %}



</details>

## Simulate authorisation reversal transaction

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/users/query%7B?current,pageSize}"><code>https://api.decenctype.com/users/query{?current,pageSize}</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### URI Parameters

| current  | Page                     |
| -------- | ------------------------ |
| pageSize | Number of items per page |

#### Body

```
// Some code
```

#### Response

{% code title="200 OK" %}
```json

    }
}
```
{% endcode %}



</details>





