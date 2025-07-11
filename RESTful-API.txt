# 📘 REST API Notes

Based on the video: [REST API Concepts and Examples](https://youtu.be/-MTSQjw5DrM?si=0s6A-YQcINbyUS0h)

---

## 🧠 What is a REST API?

- **REST** = Representational State Transfer
- Architectural style for building **web services**
- Enables communication between client and server using **HTTP**
- REST APIs allow access to resources via **URLs**

---

## 🌐 Client-Server Communication

- Client sends a request → Server responds with data
- Server handles logic; client handles UI
- Separation of concerns improves scalability and flexibility

---

## 🔁 Statelessness

- Each request is **independent**
- No session data stored on the server
- All required information (e.g., tokens) must be sent with each request

---

## 📦 Resources and URIs

- **Resource**: A data object (e.g., user, product)
- Identified using **URIs**

```http
GET https://example.com/api/users/5

✉️ HTTP Methods

| Method   | Description                 | Example               |
| -------- | --------------------------- | --------------------- |
| `GET`    | Retrieve data               | `GET /api/users`      |
| `POST`   | Create a new resource       | `POST /api/users`     |
| `PUT`    | Update (replace) a resource | `PUT /api/users/5`    |
| `PATCH`  | Update part of a resource   | `PATCH /api/users/5`  |
| `DELETE` | Delete a resource           | `DELETE /api/users/5` |

📄 JSON Format
Most REST APIs use JSON for request and response:

json
Copy
Edit
{
  "id": 1,
  "name": "Alice",
  "email": "alice@example.com"
}

📡 Request & Response Example:

Request:
http
GET /api/products/1

Response:
json
{
  "id": 1,
  "name": "iPhone",
  "price": 699
}

🚦 HTTP Status Codes:

  | Code | Meaning                  |
  | ---- | ------------------------ |
  | 200  | OK (Success)             |
  | 201  | Created (Resource added) |
  | 204  | No Content               |
  | 400  | Bad Request              |
  | 401  | Unauthorized             |
  | 403  | Forbidden                |
  | 404  | Not Found                |
  | 500  | Internal Server Error    |

✅ REST API Best Practices:
  1. Use nouns in endpoints, not verbs: /users not /getUsers
  2. Use HTTP methods for actions
  3. Return appropriate status codes
  4. Use versioning in URLs: /api/v1/users
  5. Keep APIs stateless
  6. Follow consistent naming conventions

📌 Summary:
  1. REST is a standard architecture for API design.
  2. Uses HTTP methods to perform operations on resources.
  3. Ensures scalability, simplicity, and modularity.
  4. Common in modern web & mobile apps.
