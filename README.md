# Frontend Backend Communication Guide

![GitHub stars](https://img.shields.io/github/stars/Chhatrapati-sahu-09/frontend-backend-communication?style=social)
![GitHub forks](https://img.shields.io/github/forks/Chhatrapati-sahu-09/frontend-backend-communication?style=social)
![GitHub issues](https://img.shields.io/github/issues/Chhatrapati-sahu-09/frontend-backend-communication)
![GitHub last commit](https://img.shields.io/github/last-commit/Chhatrapati-sahu-09/frontend-backend-communication)

## Overview

Modern web applications follow a **client–server architecture**, where the frontend (client) interacts with a backend server through APIs. This repository demonstrates how frontend applications communicate with backend services using HTTP requests.

The goal of this project is to provide clear and practical examples that help developers understand how data flows between the frontend and backend.

---

## Table of Contents

- Architecture Overview  
- Communication Flow  
- Technologies Used  
- HTTP Methods  
- Fetch API Example  
- Axios Example  
- Backend API Example  
- JSON Data Format  
- Repository Structure  
- Learning Goals  
- Contributing  

---

## Architecture Overview

In a typical web application, the frontend and backend communicate using APIs. The frontend sends requests to the backend, and the backend processes those requests and returns responses.

Frontend examples:

- Web browsers
- React applications
- Mobile applications

Backend examples:

- Node.js servers
- Express APIs
- Database services

---

## Communication Flow

The communication between frontend and backend usually follows this process:

```
Frontend Application
        │
        │ HTTP Request
        ▼
Backend API Server
        │
        │ Query
        ▼
Database
        │
        │ Response (JSON)
        ▼
Frontend Application
```

Example simplified flow:

```
Browser → API Request → Server → Database
        ← JSON Response ←
```

---

## Technologies Used

### Frontend

- HTML
- CSS
- JavaScript
- React

### Backend

- Node.js
- Express.js

### Data Format

- JSON

### Communication Protocol

- HTTP
- HTTPS

---

## HTTP Methods

HTTP methods define the type of operation performed on the server.

| Method | Description |
|------|-------------|
| GET | Retrieve data from the server |
| POST | Send new data to the server |
| PUT | Update existing data |
| PATCH | Update part of a resource |
| DELETE | Remove a resource |

Example request:

```
GET /api/users
```

---

## Fetch API Example

The Fetch API allows JavaScript to send HTTP requests directly from the browser.

Example:

```javascript
fetch("http://localhost:5000/api/users")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));
```

Explanation:

- `fetch()` sends the HTTP request
- `response.json()` converts the response to JSON
- The data can then be used inside the frontend application

---

## Axios Example

Axios is a popular JavaScript library used for making HTTP requests.

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

Axios simplifies request handling and error management.

---

## Backend API Example (Express)

A simple backend API built with Express can respond to frontend requests.

Example:

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

This API sends JSON data that can be consumed by frontend applications.

---

## JSON Data Format

Most APIs communicate using JSON because it is lightweight and easy to parse.

Example response:

```json
{
  "id": 1,
  "name": "Alice",
  "email": "alice@example.com"
}
```

Frontend applications use this data to render information in the user interface.

---

## Common Use Cases

Frontend–backend communication is used in many real-world applications:

- User authentication systems
- Dashboard applications
- E-commerce platforms
- Social media services
- REST API integrations

---

## Repository Structure

```
frontend-backend-communication
│
├── README.md
│
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

- Client–server architecture
- How APIs work
- How frontend applications send requests
- How backend servers process requests
- How JSON data is exchanged between systems

---

## Contributing

Contributions are welcome. Developers can contribute by:

- Adding more API examples
- Improving documentation
- Adding authentication examples
- Adding database integration examples

Steps to contribute:

1. Fork the repository  
2. Create a new branch  
3. Make changes  
4. Submit a pull request  

---

## License

This repository is created for educational purposes and developer learning.
