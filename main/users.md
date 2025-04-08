# Users

## Query All Users

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

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "OK",
    "data": {
        "total": 50,
        "users": [
            {
                "user_id": "441d7520-0945-11f0-8461-7536c68372cb",
                "first_name": "foooo",
                "last_name": "barrrr",
                "email": "b@c.com",
                "wallet_address": null,
                "wallet_type": null,
                "password": "$2b$10$FcBi8Xk41p/V3u6FdMR5aej5Z5LzSev4mkhPPj9Dg6IfIhTUTAQR.",
                "phone_num": null,
                "nationality": "TWN",
                "number": 1073,
                "identity_number": "123456789",
                "invite_code": "leeo9nhz",
                "parent_code": "master",
                "path": "/1073",
                "last_login_ip": "223.166.75.57",
                "is_kyc_1": true,
                "is_kyc_2": false,
                "is_agent": false,
                "level": 1,
                "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
                "telegram_id": null,
                "status": "active",
                "created_at": "2025-03-25T06:49:14.000Z",
                "updated_at": "2025-03-25T07:04:20.000Z",
                "merchant": {
                    "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
                    "merchant_name": "Egg Pay"
                }
            }
        ],
        "current": 1,
        "pageSize": 1
    }
}
```
{% endcode %}



</details>

## Query One User

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/users/get/%7Bid%7D"><code>https://api.decenctype.com/users/get/</code></a><code>{user_id}</code></summary>

#### **Headers**

| Name         | Value              |
| ------------ | ------------------ |
| Content-Type | `application/json` |
| X-API-KEY    | `Your-API-Key`     |

#### Response

{% code title="200 OK" %}
```javascript
{
  "code": 0,
  "message": "OK",
  "data": {
    "user_id": "eaa20cf0-2c71-11ef-ad43-31099195148a",
    "first_name": "A",
    "last_name": "AB",
    "password": "$2b$10$/Lq3eiaOpWyq8vqx0lIWA.l9eBKCBQSK2I/c9.CB1tLMfQ8qt6V6W",
    "email": "ab@c.com",
    "wallet_address": null,
    "wallet_type": null,
    "phone_num": null,
    "nationality": null,
    "number": 72,
    "identity_number": null,
    "invite_code": "lqnsindk",
    "parent_code": "master",
    "path": "/72",
    "last_login_ip": "::ffff:127.0.0.1",
    "is_kyc_1": false,
    "is_kyc_2": false,
    "is_agent": false,
    "level": 0,
    "merchant_id": "9a8ac2c0-ff6c-11ee-b58f-f10b79b6147a",
    "telegram_id": null,
    "status": "active",
    "created_at": "2024-06-17T06:22:05.000Z",
    "updated_at": "2024-06-17T06:22:05.000Z",
    "merchant": {
      "merchant_id": "9a8ac2c0-ff6c-11ee-b58f-f10b79b6147a",
      "merchant_name": "Volcano Labs Limited"
    }
  }
}
```
{% endcode %}



</details>

## Search Users

<details>

<summary><mark style="color:green;"><code>GET</code></mark><a href="https://api.decenctype.com/users/search%7B?search_word}"><code>https://api.decenctype.com/users/search{?search_word}</code></a></summary>

#### **Headers**

| Name         | Value              |
| ------------ | ------------------ |
| Content-Type | `application/json` |
| X-API-KEY    | `Your-API-Key`     |

#### URI Parameters

| search\_word | First name, Last name, Email, ... |
| ------------ | --------------------------------- |

#### Response

{% code title="200 OK" %}
```javascript
{
    "code": 0,
    "message": "OK",
    "data": {
        "total": 1,
        "users": [
            {
                "user_id": "zviagin.vasil@gmail.com",
                "first_name": "Aleksandr",
                "last_name": "Cheban",
                "email": "zviagin.vasil@gmail.com",
                "wallet_address": null,
                "wallet_type": null,
                "password": "$2b$10$6gNsFyelBGr2WF3KxZe11uyS1f.TP2ZEHCOGzgzEMcpNO3NZsyCkC",
                "phone_num": "373-60835222",
                "nationality": "MD",
                "number": 143,
                "identity_number": "A0123456789",
                "invite_code": "0x8vnx55",
                "parent_code": "master",
                "path": "/143",
                "last_login_ip": "91.211.5.139",
                "is_kyc_1": true,
                "is_kyc_2": false,
                "is_agent": false,
                "level": 1,
                "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
                "telegram_id": null,
                "status": "active",
                "created_at": "2024-09-03T12:25:17.000Z",
                "updated_at": "2024-09-03T16:27:32.000Z",
                "merchant": {
                    "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
                    "merchant_name": "Egg Pay"
                }
            }
        ]
    }
}
```
{% endcode %}



</details>

## Update User

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/users/update"><code>https://api.decenctype.com/users/update</code></a></summary>

#### **Headers**

| Name         | Value              |
| ------------ | ------------------ |
| Content-Type | `application/json` |
| X-API-KEY    | `Your-API-Key`     |

#### Body

```javascript
{
    "user_id": "4fd8d8e0-7738-11ef-ae1c-7555bb3176ae",
    "first_name": "foo",
    "last_name": "bar",
    "phone_num": "852-12444959",
    "email": "aaaaa@gmail.com",
    "nationality": "HK",
    "identity_number": "H1231521"
}
```

#### Response

{% code title="200 OK" %}
```javascript
{
    "code": 0,
    "message": "User updated successfully",
    "data": {
        "user_id": "4fd8d8e0-7738-11ef-ae1c-7555bb3176ae",
        "first_name": "foo",
        "last_name": "bar",
        "email": "aaaaa@gmail.com",
        "wallet_address": null,
        "wallet_type": null,
        "phone_num": "852-12444959",
        "nationality": "HK",
        "number": 789,
        "identity_number": "H1231521",
        "invite_code": "ofdb3voq",
        "parent_code": "master",
        "path": "/NaN",
        "last_login_ip": "::ffff:127.0.0.1",
        "is_kyc_1": true,
        "is_kyc_2": false,
        "is_agent": false,
        "level": 1,
        "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
        "telegram_id": null,
        "status": "active",
        "created_at": "2024-09-20T10:08:41.000Z",
        "updated_at": "2025-03-25T06:46:28.000Z"
    }
}
```
{% endcode %}



</details>

## Create User

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark><a href="https://api.decenctype.com/merchants/create/user"><code>https://api.decenctype.com/merchants/create/user</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "first_name": "Foo",
  "last_name": "Bar",
  "email": "a@b.com",
  "password": "s0mep4ssw0rd"
}
```

#### Response

{% code title="200 OK" %}
```json
{
  "code": 0,
  "message": "Registration successful",
  "data": {
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyX2lkIjoiMzE5YmYxZjAtM2Y0ZC0xMWVmLWE1YTAtYzEzZTNjNDQzOWFlIiwiZmlyc3RfbmFtZSI6IlJveCIsImxhc3RfbmFtZSI6Inl6aiIsInR5cGUiOiJhcHAiLCJpYXQiOjE3MjA2Nzg2MjUsImV4cCI6MTcyMTk3NDYyNX0.XL83LpyNvChs8bDjEmx7cmPC-ckmR8DI-NT_ZwDHHtI",
    "user": {
      "user_id": "319bf1f0-3f4d-11ef-a5a0-c13e3c4439ae",
      "is_agent": false,
      "level": 0,
      "first_name": "Rox",
      "last_name": "yzj",
      "password": "$2b$10$TErYBp9jeoOZChWzdqgjPuOLBFI7bk8sRWYZKlaqzWyaOjC9VRDKu",
      "is_kyc_1": false,
      "is_kyc_2": false,
      "status": "active",
      "number": 77,
      "parent_code": "master",
      "path": "/77",
      "invite_code": "5gdynft2",
      "last_login_ip": "::1",
      "merchant_id": "d41ab5d0-02d3-11ef-8443-158c7c04347f",
      "email": "1927139831@qq.com",
      "updated_at": "2024-07-11T06:17:04.912Z",
      "created_at": "2024-07-11T06:17:04.912Z"
    }
  }
}
```
{% endcode %}



</details>

## User Login

<details>

<summary><mark style="color:yellow;"><code>POST</code></mark> <a href="https://api.decenctype.com/users/login"><code>https://api.decenctype.com/users/login</code></a></summary>

#### **Headers**

| Name         | Value               |
| ------------ | ------------------- |
| Content-Type | `application/json`  |
| X-API-KEY    | `Your-API-Key`      |

#### Body

```json
{
  "emailOrPhone": "a@b.com",
  "password": "s0mep4ssw0rd"
}
```

#### Response

{% code title="200 OK" %}
```json
{
    "code": 0,
    "message": "Login successful.",
    "data": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyX2lkIjoiNDQxZDc1MjAtMDk0NS0xMWYwLTg0NjEtNzUzNmM2ODM3MmNiIiwiZmlyc3RfbmFtZSI6ImZvb29vIiwibGFzdF9uYW1lIjoiYmFycnJyIiwiZW1haWwiOiJiQGMuY29tIiwicGhvbmVfbnVtIjpudWxsLCJpYXQiOjE3NDM0OTI0MDgsImV4cCI6MTc0NDc4ODQwOH0.NqMN4H0VX89gLxIk-0HPLRIBicx9IhaHoY9MlKw47ZM"
}
```
{% endcode %}



</details>
