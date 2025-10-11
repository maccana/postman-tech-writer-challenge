# Day 8: Mock Servers

_Simulate your API—even before it exists._

---

## 🧭 Overview

Today you'll learn how to use **Mock Servers** in Postman to simulate API responses. Mock servers let you test and share your API—even if the backend isn’t ready yet.

For tech writers, mock servers are a game-changer. They allow you to write and test documentation, examples, and tutorials before the real API is live.

---

## 🎯 What You'll Learn

- What a mock server is and why it matters
- How to create a mock server from a collection
- How to define example responses
- How to send requests to a mock endpoint
- How to use mock servers in documentation

---

## 🛠️ Step-by-Step Guide

### 1. Create a Mock Server

- Go to your `Postman Tech Writer Challenge` collection
- Click the **three-dot menu (⋮)** > **Mock Collection**
- Name it: `Echo Mock Server`
- Select **Save the mock server URL as an environment variable**
- Click **Create Mock Server**

Postman will generate a public URL like:

```
https://<mock-id>.mock.pstmn.io
```

<img src="../assets/screenshots/day08-create-mock.png" alt="Create a mock server in Postman" width="600"/>

---

### 2. Add an Example Response

- In your collection, open a request (e.g., `GET Echo`)
- Click the **Save Response** button (next to the response panel)
- Name the example: `200 OK – Sample Response`
- Edit the response body if needed
- Click **Save Example**

<img src="../assets/screenshots/day08-save-example.png" alt="Save example response in Postman" width="600"/>

---

### 3. Update the Request URL

- Change the request URL to use the mock server variable:

```
{{mockServerUrl}}/get
```

- Make sure your environment has the `mockServerUrl` variable set (Postman does this automatically when creating the mock)

---

### 4. Send the Request

- Click **Send**
- You should receive the example response you saved earlier
- This confirms your mock server is working

---

### 5. Use Mocks in Documentation

- Go to your collection > **View complete documentation**
- You’ll see the mock server URL used in examples
- This lets others try the API—even if the real backend isn’t ready

---

## 🧠 What Just Happened?

You created a mock server, saved an example response, and sent a request to a simulated endpoint. This is how Postman helps you test and document APIs before they’re built.

---

## ✍️ Tech Writer’s Lens

Mock servers let you write and test documentation early. You can simulate real responses, build tutorials, and share working examples with stakeholders—without waiting on developers.

---

## 📚 Glossary

- **Mock Server**: A simulated API that returns predefined responses
- **Example Response**: A saved sample of what an API might return
- **mockServerUrl**: A variable pointing to your mock server’s base URL

---

## 🔗 Resources

- [Mock Servers Overview – Postman Docs](https://learning.postman.com/docs/designing-and-developing-your-api/mocking-data/setting-up-mock/)
- [Using Examples with Mocks](https://learning.postman.com/docs/sending-requests/examples/)

---

