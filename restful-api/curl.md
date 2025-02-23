# Task 1: Consume Data from an API Using Command Line Tools (`curl`)

## 📌 Step 1: Check `curl` Installation
To check if `curl` is installed:
```bash
curl --version
Output:
curl 7.81.0 (x86_64-pc-linux-gnu) libcurl/7.81.0 OpenSSL/3.0.2
...
```
``` bash
Output:
curl 7.81.0 (x86_64-pc-linux-gnu) libcurl/7.81.0 OpenSSL/3.0.2
...
```
---

🌎 **Step 2: Fetch a Simple Webpage (GET Request)**

Fetching data from example.com:

✅ Output Example:
``` bash
<!doctype html>
<html>
<head>
    <title>Example Domain</title>
</head>
<body>
    <h1>Example Domain</h1>
</body>
</html>
```
---
📡**Step 3: Retrieve JSON Data from an API (GET Request)**

Fetching data from the JSONPlaceholder API:
``` bash
curl https://jsonplaceholder.typicode.com/posts
```

✅ Output Example (First post only):
``` bash
[
  {
    "userId": 1,
    "id": 1,
    "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
    "body": "quia et suscipit suscipit recusandae ..."
  }
]
```
---
🔎 **Step 4: Fetch Only HTTP Headers**

Fetching only the headers from the API response:

curl -I https://jsonplaceholder.typicode.com/posts

✅ Output Example:
``` bash
HTTP/2 200 
content-type: application/json; charset=utf-8
cache-control: max-age=86400
...
```
---
📨 **Step 5: Send a POST Request (URL-Encoded Data)**

We will create a new post in the API using a URL-encoded format:
``` bash
curl -X POST -d "title=foo&body=bar&userId=1" \
  https://jsonplaceholder.typicode.com/posts
```

✅ Output Example:
``` bash
{
  "title": "foo",
  "body": "bar",
  "userId": 1,
  "id": 101
}
```
---
🎨 **Step 6: Formatting JSON Output for Readability (jq)**

By default, JSON responses appear in one long line. We can format them using jq:
``` bash
Install jq (if not installed):
Ubuntu/Linux
sudo apt install jq
```
Format API Response:
``` bash
curl -s https://jsonplaceholder.typicode.com/posts | jq
```

✅ Formatted JSON Output Example:
``` bash
[
  {
    "userId": 1,
    "id": 1,
    "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
    "body": "quia et suscipit suscipit recusandae ..."
  }
]
```

✅ **Why use jq?**
``` bash
Improves readability of JSON responses.
Easier data manipulation when debugging APIs.
```