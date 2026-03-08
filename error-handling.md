# API Error Handling

When communicating with APIs, requests may fail due to network errors, server issues, or incorrect requests. Proper error handling helps developers manage these situations.

---

## Handling Errors with Fetch

Example:

```javascript
fetch("http://localhost:5000/api/users")
  .then(response => {
    if (!response.ok) {
      throw new Error("Request failed");
    }
    return response.json();
  })
  .then(data => console.log(data))
  .catch(error => console.error(error));
```

This checks if the request was successful before processing the response.

---

## Using Try Catch with Async/Await

Example:

```javascript
async function getUsers() {
  try {
    const response = await fetch("http://localhost:5000/api/users");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Error fetching data");
  }
}

getUsers();
```

---

## Common API Errors

| Status Code | Meaning |
|-------------|---------|
| 400 | Bad request |
| 401 | Unauthorized |
| 404 | Resource not found |
| 500 | Server error |
