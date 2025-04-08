# Volcano API Documentation

## Introduction

Welcome to the API Documentation for our merchant! Here, you will find comprehensive information and resources for integrating our services into your platform seamlessly. We offers a robust set of APIs designed to empower our merchants with advanced tools for managing their businesses effectively.&#x20;

## Key Features

* **Seamless Integration**: Easily integrate with your platform using our RESTful API.
* **Scalability**: Built to handle high volumes of requests with minimal latency.
* **Security**: Secure endpoints with API Key authentication and support for Bearer tokens.
* **Comprehensive Support**: Access detailed documentation, code examples, and a dedicated support team.

## API Basics

#### Environments

| Environment            | Base URL                  | Description                          |
| ---------------------- | ------------------------- | ------------------------------------ |
| Test Environment       | https://api.decentype.com | Use this for testing and development |
| Production Environment | https://api.volcano.app   | Use this for live applications       |

> Requests sent to the Test Environment will not affect live data. Ensure you switch to the Production Environment only after thorough testing.

#### Rate Limits

* **Limit**: 1000 requests per hour per API Key
* **Exceeded Response**: 429 Too Many Requests
* **How to Check**: The X-Rate-Limit-Remaining header in responses indicates remaining requests.

#### Response Format

All API responses are returned in JSON format with appropriate HTTP status codes.&#x20;

Example:

```json
{
  "status": "success",
  "data": {
    "id": 1,
    "name": "John"
  }
}
```

## Quick Start Example

Let’s make a simple <mark style="color:green;">`GET`</mark>request to query users.

#### Using <mark style="color:yellow;">`curl`</mark>

```javascript
curl -X GET "https://api.decentype.com/users/query" \
  -H "Content-Type: application/json" \
  -H "X-API-KEY: YOUR_API_KEY"
```

\<details> \<summary>Using JavaScript (Fetch)\</summary>

```javascript
fetch('https://api.decentype.com/users/query', {
  method: 'GET',
  headers: {
    'Content-Type': 'application/json',
    'X-API-KEY': 'YOUR_API_KEY'
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

\</details> \<details> \<summary>Using Python (Requests)\</summary>

```python
import requests

url = "https://api.decentype.com/users/query"
headers = {
    "Content-Type": "application/json",
    "X-API-KEY": "YOUR_API_KEY"
}

response = requests.get(url, headers=headers)
print(response.json())
```

\</details>&#x20;

Expected Response (200 OK) :

```json
{
  "status": "success",
  "data": [
    {
      "id": 1,
      "name": "John",
      "age": 30
    }
  ]
}
```

## Support

If you encounter any difficulties or have questions while integrating our endpoints, our [support team](https://t.me/thomas_yolo) is here to assist you. Feel free to reach out to us via email, telegram or our support portal, and we'll be glad to help resolve your queries promptly.

