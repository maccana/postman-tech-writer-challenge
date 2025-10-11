# Day 6: APIs

_Define, explore, and document your APIs—all in one place._

---

## 🧭 Overview

Today you'll explore the **APIs tab** in Postman, where you can define and manage your API specifications. This is where Postman becomes more than just a request tool—it becomes a full API lifecycle platform.

For tech writers, the APIs tab is where documentation begins. You can import or create OpenAPI specs, explore endpoints, and generate reference docs—all without writing code.

---

## 🎯 What You'll Learn

- What the APIs tab is and why it matters
- How to create a new API in Postman
- How to define an API using OpenAPI
- How to link collections to an API
- How to preview and publish API documentation

---

## 🛠️ Step-by-Step Guide

### 1. Open the APIs Tab

- In the left sidebar, click the **APIs** tab
- Click **+ New API**
- Name it: `Echo API`
- Version: `1.0.0`
- Schema type: `OpenAPI 3.0`
- Click **Create API**

<img src="../assets/screenshots/day06-create-api.png" alt="Create a new API in Postman" width="600"/>

---

### 2. Add an API Schema

- In the API workspace, go to the **Definition** tab
- Click **Edit**
- Paste this sample OpenAPI schema:

```
openapi: 3.0.0
info:
  title: Echo API
  version: 1.0.0
paths:
  /get:
    get:
      summary: Returns request data
      responses:
        '200':
          description: Successful response
```

- Click **Save**

<img src="../assets/screenshots/day06-api-schema.png" alt="Add OpenAPI schema to API" width="600"/>

---

### 3. Link a Collection to the API

- Go to the **Collections** tab inside your API
- Click **Add Collection**
- Choose your `Postman Tech Writer Challenge` collection
- Select the folder or requests that match the `/get` endpoint

This links your live requests to the API definition.

---

### 4. Preview the API Documentation

- Go to the **Docs** tab in your API
- You’ll see a structured reference view of your endpoints
- Click **View in web** to preview how it looks when shared

<img src="../assets/screenshots/day06-api-docs.png" alt="Preview API documentation in Postman" width="600"/>

---

## 🧠 What Just Happened?

You created an API in Postman, defined it using OpenAPI, linked it to your collection, and previewed the documentation. This is how Postman helps you manage the full API lifecycle—from definition to testing to publishing.

---

## ✍️ Tech Writer’s Lens

The APIs tab is where documentation begins. By defining your API with OpenAPI, you create a single source of truth that developers and writers can build on. Postman lets you turn that spec into live, testable, and shareable documentation.

---

## 📚 Glossary

- **API**: A set of rules that lets software talk to other software
- **OpenAPI**: A standard format for describing REST APIs
- **Schema**: A structured definition of your API’s endpoints and responses
- **Docs Tab**: A preview of your API reference documentation

---

## 🔗 Resources

- [Defining APIs in Postman](https://learning.postman.com/docs/designing-and-developing-your-api/the-api-workflow/)
- [OpenAPI Specification](https://swagger.io/specification/)
- [Linking Collections to APIs](https://learning.postman.com/docs/designing-and-developing-your-api/linking-collections/)

---

## ✅ Next Step

Head to [07-tests-and-scripts](../07-tests-and-scripts/) to learn how to write automated tests and scripts for your API requests.
