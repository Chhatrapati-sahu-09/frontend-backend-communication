# Handling API Responses

When a frontend application sends a request to the backend, the server responds with data.

Frontend code must process this response properly.

---

## Reading JSON Response

Example:

```javascript
fetch("http://localhost:5000/api/users")
  .then(response => response.json())
  .then(data => {
    console.log(data);
  });
```

---

## Checking Response Status

```javascript
if (response.ok) {
  console.log("Request successful");
}
```

---

## Example Response

```json
{
  "id": 1,
  "name": "Alice",
  "email": "alice@example.com"
}
```

The frontend can display this data in the UI.
