# Day 7: Monitors

_Keep your APIs healthy—with automated monitoring in Postman._

---

## 🧭 Overview

Today you'll learn how to use **Monitors** in Postman to automatically run requests on a schedule and track performance, uptime, and correctness. Monitors are like automated testers that keep an eye on your APIs—even when you're not around.

For tech writers, monitors help validate that documented endpoints behave as expected. They also provide data to support reliability claims in your documentation.

---

## 🎯 What You'll Learn

- What Postman Monitors are and why they matter
- How to create a monitor for a collection
- How to schedule monitor runs
- How to view monitor results and logs
- How to use monitors for documentation validation

---

## 🛠️ Step-by-Step Guide

### 1. Open the Monitors Tab

- In the left sidebar, click the **Monitors** tab
- Click **+ New Monitor**
- Name it: `Echo Monitor`
- Choose your `Postman Tech Writer Challenge` collection
- Select the folder or requests you want to monitor

<img src="../assets/screenshots/day07-create-monitor.png" alt="Create a new monitor in Postman" width="600"/>

---

### 2. Set the Schedule

- Choose how often the monitor should run:
  - Every hour
  - Daily
  - Weekly
- Select your environment (e.g., `Day 5 Environment`)
- Click **Create Monitor**

Postman will now run your selected requests on the schedule you chose.

---

### 3. View Monitor Results

- Click on your monitor name
- Go to the **Run Results** tab
- You’ll see a history of each run, including:
  - Status codes
  - Response times
  - Test results
  - Console logs

<img src="../assets/screenshots/day07-monitor-results.png" alt="Monitor run results in Postman" width="600"/>

---

### 4. Debug Failures

- If a request fails, click into the run result
- Use the **Console** and **Test Results** tabs to investigate
- Common issues include:
  - Incorrect environment variables
  - Expired tokens
  - Network errors

---

## 🧠 What Just Happened?

You created a monitor to automatically run your API requests, scheduled it to run regularly, and reviewed the results. This is how Postman helps you ensure your APIs stay reliable and your documentation stays accurate.

---

## ✍️ Tech Writer’s Lens

Monitors are a powerful tool for validating your documentation. You can set up monitors to test example requests, check for expected responses, and alert you when something breaks—so your docs are always trustworthy.

---

## 📚 Glossary

- **Monitor**: A scheduled run of API requests that checks performance and correctness
- **Run Result**: The outcome of a monitor execution, including status codes and test logs
- **Schedule**: The frequency at which a monitor runs (hourly, daily, etc.)

---

## 🔗 Resources

- [Postman Monitors Overview](https://learning.postman.com/docs/monitoring/intro-monitors/)
- [Creating and Managing Monitors](https://learning.postman.com/docs/monitoring/setting-up-monitor/)

---

## ✅ Next Step

Head to [08-documentation](../08-documentation/) to learn how to write and publish beautiful, interactive API documentation in Postman.
