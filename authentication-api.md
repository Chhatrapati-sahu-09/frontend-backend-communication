# API Authentication

Authentication ensures that only authorized users can access certain resources on the server.

Many APIs use token-based authentication such as JWT.

---

## Login Request Example

```javascript
fetch("http://localhost:5000/api/login", {
  method: "POST",
  headers: {
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    email: "user@email.com",
    password: "123456"
  })
});
```

If authentication is successful, the server usually returns a token.

---

## Using Authorization Token

Protected routes require a token in the request header.

Example:

```javascript
fetch("http://localhost:5000/api/profile", {
  headers: {
    Authorization: "Bearer TOKEN"
  }
});
```

The server verifies the token before allowing access.

---

## Why Authentication is Important

Authentication helps:

- protect user data
- prevent unauthorized access
- secure backend APIs
