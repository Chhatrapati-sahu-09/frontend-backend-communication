# Sending Form Data to APIs

Frontend applications often collect data from forms and send it to backend APIs.

---

## Example HTML Form

```html
<form id="userForm">
  <input type="text" name="name" />
  <input type="email" name="email" />
  <button type="submit">Submit</button>
</form>
```

---

## Sending Data to API

```javascript
document.getElementById("userForm").addEventListener("submit", async (e) => {

  e.preventDefault();

  const data = {
    name: "John",
    email: "john@email.com"
  };

  await fetch("http://localhost:5000/api/users", {
    method: "POST",
    headers: {
      "Content-Type": "application/json"
    },
    body: JSON.stringify(data)
  });

});
```

This sends the form data to the backend server.
