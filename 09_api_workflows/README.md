# Day 9: API Workflows

_Connect your requests into powerful, automated flows._

---

## 🧭 Overview

Today you'll learn how to use **Flows** in Postman to build multi-step API workflows. Flows let you chain requests together, pass data between them, and visualize how your API behaves across different endpoints.

For tech writers, workflows help you understand and document how APIs interact. They’re also great for building tutorials, demos, and reproducible examples.

---

## 🎯 What You'll Learn

- What Postman Flows are and why they matter
- How to create a new flow
- How to add requests and logic blocks
- How to pass data between steps
- How to run and debug a flow

---

## 🛠️ Step-by-Step Guide

### 1. Open the Flows Tab

- In the left sidebar, click the **Flows** tab
- Click **+ New Flow**
- Name it: `Echo Workflow`
- Choose your workspace
- Click **Create Flow**

<img src="../assets/screenshots/day09-create-flow.png" alt="Create a new flow in Postman" width="600"/>

---

### 2. Add a Request Block

- Drag a **Send Request** block onto the canvas
- Click the block to configure it
- Choose your `GET Echo` request from the `Postman Tech Writer Challenge` collection

This sets up the first step in your workflow.

---

### 3. Add a Delay Block

- Drag a **Delay** block onto the canvas
- Set it to wait for `2 seconds`
- Connect the output of the request block to the input of the delay block

This simulates a pause between API calls.

---

### 4. Add a Second Request

- Drag another **Send Request** block onto the canvas
- Choose a second request (e.g., `POST Echo`)
- Connect the delay block to this second request

Now your flow sends a GET request, waits 2 seconds, then sends a POST.

---

### 5. Run the Flow

- Click the **Run** button in the top right
- Watch the flow execute step-by-step
- Inspect the output of each block to see status codes and response data

<img src="../assets/screenshots/day09-run-flow.png" alt="Run and inspect flow in Postman" width="600"/>

---

## 🧠 What Just Happened?

You built a simple API workflow using Postman Flows. You chained requests together, added a delay, and ran the flow to see how your API behaves across steps.

---

## ✍️ Tech Writer’s Lens

Flows are a great way to visualize how APIs work together. You can use them to test multi-step processes, simulate user journeys, and create interactive tutorials that mirror real-world usage.

---

## 📚 Glossary

- **Flow**: A visual sequence of API actions and logic blocks
- **Send Request Block**: Executes a saved API request
- **Delay Block**: Pauses the flow for a set time
- **Canvas**: The workspace where you build your flow

---

## 🔗 Resources

- [Postman Flows Overview](https://learning.postman.com/docs/flows/flows-overview/)
- [Building Flows in Postman](https://learning.postman.com/docs/flows/building-flows/)

---

