# API Request Examples

This guide explains how frontend applications send HTTP requests to backend APIs using JavaScript.

APIs allow the frontend to send and receive data from a server.

---

## GET Request

A GET request retrieves data from the server.

Example:

```javascript
fetch("http://localhost:5000/api/users")
  .then(response => response.json())
  .then(data => console.log(data));
```

This request asks the server for a list of users.

---

## POST Request

A POST request sends data to the server.

Example:

```javascript
fetch("http://localhost:5000/api/users", {
  method: "POST",
  headers: {
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    name: "John",
    email: "john@email.com"
  })
});
```

This sends user data to the backend.

---

## PUT Request

A PUT request updates existing data.

Example:

```javascript
fetch("http://localhost:5000/api/users/1", {
  method: "PUT",
  headers: {
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    name: "Updated Name"
  })
});
```

---

## DELETE Request

A DELETE request removes data from the server.

Example:

```javascript
fetch("http://localhost:5000/api/users/1", {
  method: "DELETE"
});
```
