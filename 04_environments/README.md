# Day 4: Environments

_Make your API requests dynamic and reusable—with Postman Environments._

---

## 🧭 Overview

Today you'll learn how to use **Environments** in Postman to make your requests flexible and reusable. Environments let you define variables like `baseURL`, `token`, or `userId` that can change depending on where or how you're testing.

For tech writers, environments are a powerful way to document APIs across different stages—like development, staging, and production—without rewriting requests.

---

## 🎯 What You'll Learn

- What environments are and why they matter
- How to create and activate an environment
- How to define and use variables in requests
- How to switch between environments
- How to preview and debug variable values

---

## 🛠️ Step-by-Step Guide

### 1. Create a New Environment

- Click the **gear icon** in the top right corner of Postman
- Select **Manage Environments**
- Click **Add**
- Name it: `Day 4 Environment`
- Add a variable:
  - Key: `baseURL`
  - Initial Value: `https://postman-echo.com`
- Click **Save**

<img src="../assets/screenshots/day05-create-environment.png" alt="Create a new environment in Postman" width="600"/>

---

### 2. Set the Active Environment

- In the top-right dropdown next to the eye icon 👁️
- Select `Day 4 Environment` from the list

This tells Postman to use the variables from this environment in your requests.

---

### 3. Use a Variable in a Request

- Create a new request in your collection
- Set the method to `GET`
- Set the URL to:

```
{{baseURL}}/get
```

Postman will replace `{{baseURL}}` with `https://postman-echo.com` from your environment.

<img src="../assets/screenshots/day04-variable-url.png" alt="Using environment variable in URL" width="600"/>

---

### 4. Send the Request

- Click **Send**
- You should receive a `200 OK` response with echoed data

---

### 5. Preview and Debug Variables

- Click the **eye icon 👁️** next to the environment dropdown
- You’ll see all active variables and their current values
- This is helpful for debugging and verifying substitutions

<img src="../assets/screenshots/day04-preview-variables.png" alt="Preview environment variables" width="600"/>

---

## 🧠 What Just Happened?

You created an environment, defined a variable, used it in a request, and saw how Postman dynamically substituted it. This makes your requests portable and easier to maintain—especially when working across different API stages.

---

## ✍️ Tech Writer’s Lens

Environments are a tech writer’s best friend. They let you document APIs once and reuse them across multiple contexts. You can even define variables for authentication tokens, user IDs, or custom headers—making your documentation scalable and adaptable.

---

## 📚 Glossary

- **Environment**: A set of variables used to customize requests
- **Variable**: A placeholder that gets replaced with a value at runtime
- **Active Environment**: The currently selected environment Postman uses for variable substitution

---

## 🔗 Resources

- [Using Environments – Postman Docs](https://learning.postman.com/docs/sending-requests/variables/#using-environments)
- [Variables in Postman](https://learning.postman.com/docs/sending-requests/variables/)

---

## ✅ Next Step

Head to [05-variables](../05-variables/) to learn how to use variables to make your API requests dynamic and reusable.
