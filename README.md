# Frontend Backend Communication Guide

![GitHub stars](https://img.shields.io/github/stars/Chhatrapati-sahu-09/frontend-backend-communication?style=social)
![GitHub forks](https://img.shields.io/github/forks/Chhatrapati-sahu-09/frontend-backend-communication?style=social)
![GitHub issues](https://img.shields.io/github/issues/Chhatrapati-sahu-09/frontend-backend-communication)
![GitHub last commit](https://img.shields.io/github/last-commit/Chhatrapati-sahu-09/frontend-backend-communication)

## Overview

This repository demonstrates how a frontend application communicates with a backend server. It explains the fundamental concepts behind client-server architecture and shows practical examples of sending and receiving data between the frontend and backend.

Modern web applications rely heavily on APIs to exchange information between the user interface and the server. Understanding how this communication works is essential for full-stack development.

---

## How Frontend and Backend Communicate

The frontend sends an HTTP request to the backend server. The backend processes the request and returns a response, usually in JSON format.

Basic flow:

Frontend → HTTP Request → Backend API → Database → Response → Frontend

Example:

```
Browser → API Request → Server → Database
        ← JSON Response ←
```

---

## Technologies Used

Common technologies used for frontend–backend communication:

Frontend:
- HTML
- CSS
- JavaScript
- React

Backend:
- Node.js
- Express.js

Data Format:
- JSON

Communication Protocol:
- HTTP / HTTPS

---

## HTTP Methods

HTTP methods define the type of operation performed on the server.

| Method | Purpose |
|------|---------|
| GET | Retrieve data from server |
| POST | Send new data to server |
| PUT | Update existing data |
| PATCH | Partially update data |
| DELETE | Remove data |

Example request:

```
GET /api/users
```

---

## Fetch API Example

The Fetch API allows JavaScript to make HTTP requests.

Example:

```javascript
fetch("http://localhost:5000/api/users")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));
```

This sends a request to the backend and retrieves data.

---

## Axios Example

Axios is another popular library for making HTTP requests.

Example:

```javascript
import axios from "axios";

axios.get("http://localhost:5000/api/users")
  .then(response => {
    console.log(response.data);
  })
  .catch(error => {
    console.error(error);
  });
```

---

## Example Backend API (Express)

Example of a simple backend API using Express.

```javascript
const express = require("express");
const app = express();

app.get("/api/users", (req, res) => {
  res.json([
    { id: 1, name: "Alice" },
    { id: 2, name: "Bob" }
  ]);
});

app.listen(5000, () => {
  console.log("Server running on port 5000");
});
```

This API sends JSON data to the frontend.

---

## JSON Response Example

Backend responses are usually sent in JSON format.

Example:

```json
{
  "id": 1,
  "name": "Alice",
  "email": "alice@example.com"
}
```

The frontend reads this data and displays it in the user interface.

---

## Common Use Cases

Frontend–backend communication is used in many applications such as:

- Login and authentication systems
- Data dashboards
- E-commerce websites
- Social media platforms
- REST APIs

---

## Repository Structure

```
frontend-backend-communication
│
├── README.md
├── backend-example
│   └── express-server.js
│
├── fetch-example
│   └── fetch-api.js
│
└── axios-example
    └── axios-request.js
```

---

## Learning Goals

This repository helps developers understand:

- How APIs work
- How frontend applications request data
- How backend servers respond with data
- How to handle HTTP requests and responses

---

## Contributing

Contributions are welcome.

You can contribute by:

- Adding new examples
- Improving documentation
- Adding authentication examples
- Adding database integration examples

Steps to contribute:

1. Fork the repository  
2. Create a new branch  
3. Make your changes  
4. Submit a pull request  

---

## License

This repository is created for educational purposes and developer learning.
