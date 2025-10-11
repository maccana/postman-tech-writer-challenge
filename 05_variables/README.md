# Day 5: Variables

_Write once, reuse everywhere—with Postman Variables._

---

## 🧭 Overview

Today you'll learn how to use **variables** in Postman to make your API requests dynamic, reusable, and easier to maintain. Variables let you store values like URLs, tokens, or user IDs and reference them throughout your requests, environments, and scripts.

For tech writers, variables are essential for creating scalable documentation that adapts to different environments, users, or workflows.

---

## 🎯 What You'll Learn

- What variables are and how they work
- How to define variables at different scopes
- How to reference variables in requests
- How to use variables in scripts
- How to debug variable values

---

## 🛠️ Step-by-Step Guide

### 1. Understand Variable Scopes

Postman supports multiple scopes for variables:

| Scope        | Description                              |
|--------------|------------------------------------------|
| Global       | Available across all workspaces          |
| Environment  | Tied to a specific environment           |
| Collection   | Available within a specific collection   |
| Local        | Temporary, used during request execution |
| Data         | Used in collection runners or external files |

---

### 2. Create a Collection Variable

- Click on your collection name
- Click the **three-dot menu (⋮)** > **Edit**
- Go to the **Variables** tab
- Add a variable:
  - Key: `userId`
  - Initial Value: `12345`
- Click **Save**

<img src="../assets/screenshots/day05-collection-variable.png" alt="Create collection variable in Postman" width="600"/>

---

### 3. Use the Variable in a Request

- Create a new request in your collection
- Set the method to `GET`
- Set the URL to:

```
https://postman-echo.com/get?userId={{userId}}
```

Postman will replace `{{userId}}` with `12345` from your collection variable.

<img src="../assets/screenshots/day05-variable-url.png" alt="Using variable in request URL" width="600"/>

---

### 4. Use Variables in Scripts

- Go to the **Tests** tab of your request
- Add this script:

```javascript
console.log("User ID is:", pm.variables.get("userId"));
```

- Click **Send**
- Open the **Postman Console** (bottom panel or View > Show Postman Console)
- You’ll see the logged value

<img src="../assets/screenshots/day05-console-log.png" alt="Logging variable in Postman Console" width="600"/>

---

### 5. Override with Environment Variable

- Create an environment variable also named `userId` with value `99999`
- Set the environment as active
- Send the request again

Postman will now use the environment variable instead of the collection one—because environment scope has higher priority.

---

## 🧠 What Just Happened?

You defined a variable, used it in a request, logged it in a script, and saw how scopes affect which value gets used. This is how Postman lets you write flexible, reusable requests that adapt to different contexts.

---

## ✍️ Tech Writer’s Lens

Variables are the backbone of scalable API documentation. They let you write once and reuse across environments, users, and workflows. You can even use them to generate dynamic examples or simulate real-world scenarios.

---

## 📚 Glossary

- **Variable**: A placeholder that gets replaced with a value at runtime
- **Scope**: The level at which a variable is defined (global, environment, collection, etc.)
- **pm.variables.get()**: A Postman script method to retrieve variable values

---

## 🔗 Resources

- [Postman Variables Overview](https://learning.postman.com/docs/sending-requests/variables/)
- [Variable Scopes Explained](https://learning.postman.com/docs/sending-requests/variables/#variable-scopes)

---

## ✅ Next Step

Head to [07-monitors](../07-monitors/) to learn how to monitor your API performance and uptime using Postman Monitors.

