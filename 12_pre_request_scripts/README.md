# Day 12: Pre-request Scripts

_Prepare your requests with dynamic data—before they’re sent._

---

## 🧭 Overview

Today you'll learn how to use **Pre-request Scripts** in Postman to run JavaScript before a request is sent. These scripts let you set variables, generate dynamic values, and customize your requests on the fly.

For tech writers, pre-request scripts help simulate real-world scenarios, automate examples, and validate documentation with dynamic inputs.

---

## 🎯 What You'll Learn

- What pre-request scripts are and how they work
- How to write a basic script in Postman
- How to set variables dynamically
- How to generate timestamps, tokens, and random data
- How to debug script output using the Postman Console

---

## 🛠️ Step-by-Step Guide

### 1. Open the Pre-request Script Tab

- Click on a request in your collection (e.g., `POST Echo`)
- Go to the **Pre-request Script** tab
- This is where you’ll write JavaScript that runs before the request is sent

<img src="../assets/screenshots/day12-pre-request-tab.png" alt="Pre-request script tab in Postman" width="600"/>

---

### 2. Set a Dynamic Variable

Paste this script into the tab:

```javascript
let timestamp = new Date().toISOString();
pm.environment.set("currentTime", timestamp);
```

This sets a variable called `currentTime` with the current ISO timestamp.

---

### 3. Use the Variable in Your Request

- In the request body, use:

```json
{
  "sentAt": "{{currentTime}}"
}
```

- Postman will replace `{{currentTime}}` with the value set by your script

<img src="../assets/screenshots/day12-variable-body.png" alt="Use dynamic variable in request body" width="600"/>

---

### 4. Generate Random Data

Try this script to simulate a random user ID:

```javascript
let userId = Math.floor(Math.random() * 10000);
pm.variables.set("userId", userId);
```

Use `{{userId}}` in your request to insert the random value.

---

### 5. Debug with the Console

- Open the **Postman Console** (bottom panel or View > Show Postman Console)
- Add a log to your script:

```javascript
console.log("Sending request at:", pm.environment.get("currentTime"));
```

- Click **Send**
- Check the console output to verify your script ran correctly

<img src="../assets/screenshots/day12-console-log.png" alt="View pre-request script output in Postman Console" width="600"/>

---

## 🧠 What Just Happened?

You wrote a pre-request script to set dynamic variables, used those variables in your request, and verified the output using the console. This is how Postman lets you automate and customize your API workflows.

---

## ✍️ Tech Writer’s Lens

Pre-request scripts help you simulate real-world API behavior. You can generate dynamic examples, automate timestamps, and validate your documentation with realistic data—all without manual edits.

---

## 📚 Glossary

- **Pre-request Script**: JavaScript that runs before a request is sent
- **pm.environment.set()**: Sets a variable in the active environment
- **Postman Console**: A debugging tool that shows logs and request details

---

## 🔗 Resources

- [Pre-request Scripts Overview](https://learning.postman.com/docs/writing-scripts/script-references/pre-request-scripts/)
- [Postman JavaScript API](https://learning.postman.com/docs/writing-scripts/script-references/postman-sandbox-api/)

---
