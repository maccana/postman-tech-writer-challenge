# Day 13: Tests

_Validate your API responses—with automated tests in Postman._

---

## 🧭 Overview

Today you'll learn how to write **tests** in Postman to automatically check the behavior of your API. Tests help you confirm that responses are correct, data is present, and endpoints behave as expected.

For tech writers, tests are a powerful way to validate documentation examples and ensure that your tutorials and sample requests always return what they promise.

---

## 🎯 What You'll Learn

- What Postman tests are and how they work
- How to write basic JavaScript tests
- How to check status codes and response bodies
- How to use the Test Results tab
- How to debug failed tests

---

## 🛠️ Step-by-Step Guide

### 1. Open the Tests Tab

- Click on a request in your collection (e.g., `GET Echo`)
- Go to the **Tests** tab
- This is where you’ll write JavaScript that runs after the response is received

<img src="../assets/screenshots/day13-tests-tab.png" alt="Tests tab in Postman" width="600"/>

---

### 2. Write a Basic Status Code Test

Paste this into the Tests tab:

```javascript
pm.test("Status code is 200", function () {
  pm.response.to.have.status(200);
});
```

This checks that the response returned a `200 OK`.

---

### 3. Check for a Specific Field

Add another test:

```javascript
pm.test("Response has 'args' object", function () {
  pm.response.to.have.property("json");
  pm.expect(pm.response.json().args).to.be.an("object");
});
```

This confirms that the response includes an `args` object in the body.

---

### 4. Send the Request and View Results

- Click **Send**
- Go to the **Test Results** tab below the response
- You’ll see pass/fail indicators for each test

<img src="../assets/screenshots/day13-test-results.png" alt="View test results in Postman" width="600"/>

---

### 5. Debug Failed Tests

- If a test fails, check the **Console** for logs
- Use `console.log()` in your test scripts to inspect values:

```javascript
console.log("Response body:", pm.response.json());
```

This helps you understand why a test failed and how to fix it.

---

## 🧠 What Just Happened?

You wrote automated tests to validate your API responses, ran them, and inspected the results. This is how Postman helps you ensure your API behaves as expected—and your documentation stays accurate.

---

## ✍️ Tech Writer’s Lens

Tests help you verify that your documentation examples are correct. You can use them to validate sample requests, check for required fields, and ensure consistency across environments—all without manual effort.

---

## 📚 Glossary

- **Test**: A script that checks the response of an API request
- **pm.test()**: A Postman function to define a test
- **Test Results Tab**: Where you see pass/fail indicators for each test

---

## 🔗 Resources

- [Writing Tests in Postman](https://learning.postman.com/docs/writing-scripts/test-scripts/)
- [Postman JavaScript API](https://learning.postman.com/docs/writing-scripts/script-references/postman-sandbox-api/)

---

