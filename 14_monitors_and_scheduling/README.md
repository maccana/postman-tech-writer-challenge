# Day 14: Monitors and Scheduling

_Keep your API healthy—with automated, scheduled monitoring._

---

## 🧭 Overview

Today you'll learn how to schedule **Monitors** in Postman to run automatically at regular intervals. Monitors help you track uptime, performance, and correctness—without manual effort.

For tech writers, scheduled monitors validate that your documentation examples and sample requests continue to work over time. They’re your early warning system for broken endpoints.

---

## 🎯 What You'll Learn

- How to create and configure a monitor
- How to schedule monitor runs (hourly, daily, weekly)
- How to use environments with monitors
- How to view and interpret monitor results
- How to use monitors to validate documentation

---

## 🛠️ Step-by-Step Guide

### 1. Create a Monitor

- Go to the **Monitors** tab in the left sidebar
- Click **+ New Monitor**
- Name it: `Echo Monitor`
- Choose your `Postman Tech Writer Challenge` collection
- Select the folder or requests you want to monitor

<img src="../assets/screenshots/day14-create-monitor.png" alt="Create a new monitor in Postman" width="600"/>

---

### 2. Set the Schedule

- Choose how often the monitor should run:
  - Every hour
  - Daily
  - Weekly
- Select your environment (e.g., `Day 5 Environment`)
- Click **Create Monitor**

Postman will now run your selected requests automatically on the schedule you chose.

---

### 3. View Monitor Results

- Click on your monitor name
- Go to the **Run Results** tab
- You’ll see a history of each run, including:
  - Status codes
  - Response times
  - Test results
  - Console logs

<img src="../assets/screenshots/day14-monitor-results.png" alt="Monitor run results in Postman" width="600"/>

---

### 4. Debug Failures

- If a request fails, click into the run result
- Use the **Console** and **Test Results** tabs to investigate
- Common issues include:
  - Incorrect environment variables
  - Expired tokens
  - Network errors

---

### 5. Use Monitors to Validate Docs

- Monitors can run your documented requests regularly
- If a sample request fails, you’ll know before your readers do
- This helps keep your documentation trustworthy and up to date

---

## 🧠 What Just Happened?

You created a monitor, scheduled it to run automatically, and reviewed the results. This is how Postman helps you automate API health checks and ensure your documentation stays accurate.

---

## ✍️ Tech Writer’s Lens

Scheduled monitors are your safety net. They validate your examples, catch broken endpoints, and help you maintain reliable documentation—without manual testing.

---

## 📚 Glossary

- **Monitor**: A scheduled run of API requests that checks performance and correctness
- **Schedule**: The frequency at which a monitor runs (hourly, daily, etc.)
- **Run Result**: The outcome of a monitor execution, including status codes and test logs

---

## 🔗 Resources

- [Postman Monitors Overview](https://learning.postman.com/docs/monitoring/intro-monitors/)
- [Creating and Managing Monitors](https://learning.postman.com/docs/monitoring/setting-up-monitor/)
- [Using Environments with Monitors](https://learning.postman.com/docs/monitoring/using-environments-in-monitors/)

---

