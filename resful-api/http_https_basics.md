# 0. Basics of HTTP/HTTPS

## Introduction

The **Hypertext Transfer Protocol (HTTP)** is the foundation of communication on the web. It defines how requests and responses are structured between clients (e.g., browsers, API consumers) and servers. 

HTTP has evolved to include **HTTPS (HTTP Secure)**, which encrypts communications to prevent data interception and tampering. Understanding these protocols is crucial for building and consuming web services securely.

---

## Differences Between HTTP and HTTPS

| Feature         | HTTP                                      | HTTPS                                         |
|----------------|------------------------------------------|-----------------------------------------------|
| **Security**    | No encryption, data sent in plain text. | Encrypted using SSL/TLS, securing data.      |
| **Port**        | 80 (default)                            | 443 (default)                                |
| **Data Integrity** | Data can be intercepted or altered. | Data is protected from eavesdropping.        |
| **Certificates** | No certificate required.               | Requires an SSL/TLS certificate.             |
| **SEO Ranking** | Not prioritized by search engines.      | Preferred by search engines (Google, etc.). |

### **Key Takeaways:**
- HTTPS encrypts communication, making it essential for security.
- Websites that handle sensitive data (e.g., banking, e-commerce) must use HTTPS.
- Modern browsers warn users about **insecure HTTP connections**.

---

## HTTP Request/Response Structure

### **Structure of an HTTP Request**


### **Request Components:**
1. **HTTP Method** – Defines the action to be performed (e.g., GET, POST).
2. **Path** – The resource being requested (`/resource/path`).
3. **Headers** – Metadata about the request (e.g., `User-Agent`, `Accept`).
4. **Body** *(optional)* – Data sent with requests (for POST, PUT).

---

### **Structure of an HTTP Response**
``` bash
HTTP/1.1 200 OK Date: Wed, 21 Feb 2025 10:00:00 GMT Server: Apache/2.4.41 (Ubuntu) Content-Type: application/json; charset=UTF-8 Content-Length: 1234

{ "message": "Hello, world!", "status": "success" }
```

### **Response Components:**
1. **Status Line** – Indicates request success or failure (`HTTP/1.1 200 OK`).
2. **Headers** – Provide metadata (e.g., `Content-Type`, `Server`).
3. **Body** – The response data (JSON, HTML, XML, etc.).

---

## Common HTTP Methods

| Method  | Description                                    | Example Use Case |
|---------|----------------------------------------------|------------------|
| **GET** | Retrieves a resource.                      | Fetch a webpage or API data. |
| **POST** | Creates a new resource.                   | Submit a form, create a new user. |
| **PUT** | Updates an existing resource.              | Modify user details. |
| **DELETE** | Removes a resource.                    | Delete a user account. |

*(Additional methods: **PATCH** (partial update), **HEAD**, **OPTIONS**.)*

---

## Common HTTP Status Codes

| Status Code | Meaning | Example Scenario |
|-------------|---------|------------------|
| **200 OK** | Request successful. | Fetching a webpage. |
| **201 Created** | Resource successfully created. | User account creation. |
| **400 Bad Request** | The request is malformed. | Sending invalid JSON data. |
| **404 Not Found** | Requested resource does not exist. | Accessing a non-existent URL. |
| **500 Internal Server Error** | General server error. | Server misconfiguration. |

- **1xx (Informational)** – Request received, processing.
- **2xx (Success)** – Request was successful.
- **3xx (Redirection)** – Further action needed (e.g., redirect).
- **4xx (Client Errors)** – Request issues (e.g., invalid input, missing resource).
- **5xx (Server Errors)** – The server encountered an issue.

---

## Inspecting HTTP Requests with Developer Tools

To see real HTTP requests and responses in action:

1. **Using Browser Developer Tools:**
   - Open a web browser (Chrome, Firefox).
   - Right-click and select **Inspect** → Go to the **Network** tab.
   - Reload the page and click on any request to see its details.

2. **Using `curl` from the Command Line:**
   ```bash
   curl -I http://example.com

Output:

``` bash 
HTTP/1.1 200 OK
Content-Type: text/html; charset=UTF-8
Server: nginx/1.18.0



