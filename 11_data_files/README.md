# Day 11: Data Files

_Test your API with real-world data—using Postman data files._

---

## 🧭 Overview

Today you'll learn how to use **data files** in Postman to run requests with dynamic input. Data files let you simulate multiple users, test edge cases, and validate your API against real-world scenarios.

For tech writers, data files are a great way to test documentation examples, generate sample responses, and ensure your tutorials work with varied inputs.

---

## 🎯 What You'll Learn

- What data files are and how they work
- How to format CSV and JSON files for Postman
- How to use variables from a data file
- How to run a collection with a data file
- How to inspect results and debug failures

---

## 🛠️ Step-by-Step Guide

### 1. Create a Sample Data File

Create a simple CSV file named `users.csv` with the following content:

```
name,email
Alice,alice@example.com
Bob,bob@example.com
Charlie,charlie@example.com
```

Or a JSON file named `users.json`:

```json
[
  { "name": "Alice", "email": "alice@example.com" },
  { "name": "Bob", "email": "bob@example.com" },
  { "name": "Charlie", "email": "charlie@example.com" }
]
```

---

### 2. Use Variables in Your Request

- Create a new request in your collection
- Set the method to `POST`
- URL: `https://postman-echo.com/post`
- Body type: `raw` > `JSON`
- Paste this:

```json
{
  "name": "{{name}}",
  "email": "{{email}}"
}
```

Postman will replace `{{name}}` and `{{email}}` with values from your data file.

<img src="../assets/screenshots/day11-variable-body.png" alt="Use data file variables in request body" width="600"/>

---

### 3. Run the Collection with a Data File

- Click the **Runner** button in the top right
- Choose your collection
- Click **Select File** and upload `users.csv` or `users.json`
- Set iterations to match the number of rows (e.g., 3)
- Click **Run**

<img src="../assets/screenshots/day11-runner-datafile.png" alt="Run collection with data file in Postman" width="600"/>

---

### 4. Inspect the Results

- After the run, view the **Test Results** tab
- You’ll see each iteration with its input and response
- Use this to verify that your API handles different inputs correctly

---

## 🧠 What Just Happened?

You created a data file, used variables in your request, and ran a collection with multiple inputs. This is how Postman helps you simulate real-world scenarios and validate your API documentation.

---

## ✍️ Tech Writer’s Lens

Data files let you test your documentation at scale. You can simulate multiple users, validate examples, and ensure your tutorials work with varied inputs—all without writing extra code.

---

## 📚 Glossary

- **Data File**: A CSV or JSON file containing input values for requests
- **Collection Runner**: A tool that runs a collection multiple times with different data
- **Iteration**: One run of a request using a row from the data file

---

## 🔗 Resources

- [Using Data Files in Postman](https://learning.postman.com/docs/running-collections/working-with-data-files/)
- [Collection Runner Overview](https://learning.postman.com/docs/running-collections/intro-to-collection-runs/)

---

