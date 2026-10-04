# Day 01 — JavaScript Basics Revision Notes

## 🎯 What We Learned

Day 01 introduced the JavaScript fundamentals needed before starting Playwright automation.

We learned:
1. `console.log()`
2. Variables
3. `const` and `let`
4. Basic JavaScript data types
5. QA-oriented test data
6. Running JavaScript with Node.js

---

## 1. `console.log()`

`console.log()` is used to print information in the terminal.

### Example

```javascript
console.log("Hello Raj");
console.log("Playwright Automation");
```

### QA Example

```javascript
const testCaseId = "TC001";

console.log("Test Case ID:", testCaseId);
```

Output:

```text
Test Case ID: TC001
```

**Remember:**  
`console.log()` = show the value in the terminal.

---

## 2. What Is a Variable?

A variable is a named place where we store a value.

### Example

```javascript
const browserName = "Chrome";
```

Here:
- `browserName` = variable name
- `"Chrome"` = value

### QA Examples

```javascript
const username = "raj@test.com";
const testCaseId = "TC001";
const browserName = "Chrome";
const browserVersion = 154;
```

Variables allow us to store test data and use it later in our automation.

---

## 3. `const` vs `let`

### `const`

Use `const` when the variable should not be reassigned.

```javascript
const testCaseId = "TC001";
const browserName = "Chrome";
```

You should not later do:

```javascript
testCaseId = "TC002";
```

That causes an error because a `const` variable cannot be reassigned.

### `let`

Use `let` when the value may change.

```javascript
let testPassed = true;

testPassed = false;
```

This is useful for values whose state can change during a test.

### Easy Rule

**const = value should stay assigned to the same variable**

**let = value may be reassigned**

---

## 4. Basic JavaScript Data Types

We practiced five important values/types.

### A. String

Text is a **String**.

Strings are normally written inside quotes.

```javascript
const browserName = "Chrome";
const testName = "Login Test";
const username = "raj@test.com";
```

Examples:

```text
"Chrome"
"Login Test"
"Raj"
"123"
```

**Important:** `"123"` is a String, not a Number, because it is inside quotes.

---

### B. Number

Numbers are written without quotes.

```javascript
const browserVersion = 154;
const retryCount = 3;
const timeout = 5000;
```

Examples:

```text
154
3
5000
10.5
```

**Remember:**

```javascript
123      // Number
"123"    // String
```

---

### C. Boolean

A Boolean has only two possible values:

```javascript
true
false
```

Example:

```javascript
const isLoggedIn = true;
const testPassed = false;
const isVisible = true;
```

### QA Meaning

```javascript
const testPassed = true;
```

means the test passed.

```javascript
const testPassed = false;
```

means the test did not pass.

**Important:**  
`true` and `false` are Booleans.

`"true"` and `"false"` are Strings because they are inside quotes.

---

### D. Undefined

A variable is **undefined** when it has been declared but no value has been assigned.

Example:

```javascript
let errorMessage;
```

Because no value was assigned, JavaScript gives it:

```text
undefined
```

Example:

```javascript
let actualResult;

console.log(actualResult);
```

Output:

```text
undefined
```

### QA Meaning

You might use this while waiting for a value to be populated, such as an actual result or error message.

---

### E. Null

`null` means we intentionally say there is **no value**.

Example:

```javascript
const testData = null;
```

This is different from `undefined`.

### Easy Difference

**undefined** → no value has been assigned yet.

**null** → we intentionally assigned “no value”.

---

## 5. Quick Data Type Table

| Example | Type | Meaning |
|---|---|---|
| `"Chrome"` | String | Text |
| `154` | Number | Numeric value |
| `true` | Boolean | True/false value |
| `let errorMessage;` | Undefined | No value assigned |
| `null` | Null | Intentionally no value |

### Memory Trick

```text
"Hello"           → String
123               → Number
true / false      → Boolean
nothing assigned  → Undefined
intentionally empty → Null
```

---

## 6. QA Test Data Practice

We created a small login test case:

```javascript
const testCaseId = "TC001";
const testCaseName = "Verify valid login";
const username = "raj@test.com";
const password = "Dummy@123";
let testPassed = true;
```

Then we printed the values:

```javascript
console.log("Test Case ID:", testCaseId);
console.log("Test Case Name:", testCaseName);
console.log("Username:", username);
console.log("Password:", password);
console.log("Test Passed:", testPassed);
```

### Why This Matters

In real automation, we constantly work with:
- Test case names
- Usernames
- Test data
- Browser names
- Version numbers
- Expected results
- Actual results
- Pass/fail states

These JavaScript basics are the foundation for handling that information.

---

## 7. Running JavaScript with Node.js

Our file:

```text
day01.js
```

Because the terminal was already inside the `day-01` folder, we ran:

```bash
node day01.js
```

### Important Terminal Lesson

If the terminal is already here:

```text
playwright-automation-masterclass\javascript-fundamentals\day-01
```

run:

```bash
node day01.js
```

Do not repeat the full folder path from inside that folder.

---

## 8. Common Beginner Mistake We Solved

We first ran:

```bash
node javascript-fundamentals/day-01/day01.js
```

while already inside the `day-01` folder.

Node then looked for a path that did not exist and returned:

```text
MODULE_NOT_FOUND
```

### Lesson

Always check your current terminal folder before running a file.

---

## 9. Security Reminder

Our repository is public, so we used:

```javascript
const password = "Dummy@123";
```

This is dummy test data.

**Never commit real passwords, API keys, tokens, secrets, or private credentials to a public GitHub repository.**

---

## 10. Day 01 Cheat Sheet

```javascript
// String
const browser = "Chrome";

// Number
const version = 154;

// Boolean
const isLoggedIn = true;

// Undefined
let errorMessage;

// Null
const response = null;

// Output
console.log(browser);
```

### Variable Rules

```javascript
const value = "fixed";
let changingValue = 1;
```

### Most Important Difference

```text
"true"   → String
true     → Boolean

"123"    → String
123      → Number

undefined → no value assigned
null      → intentionally no value
```

---

## 🧠 Self-Check Before Day 02

You should be able to answer:

**1. What does `console.log()` do?**

Prints a value to the terminal.

**2. When should we use `const`?**

When a variable should not be reassigned.

**3. When should we use `let`?**

When a variable may be reassigned.

**4. What is the type of `"Chrome"`?**

String.

**5. What is the type of `154`?**

Number.

**6. What is the type of `true`?**

Boolean.

**7. What is `undefined`?**

A variable exists but no value has been assigned.

**8. What is `null`?**

An intentionally assigned “no value”.

---

## ✅ Day 01 Completion

**Checkpoint Score:** 5/5

**Hands-on:** Completed

**Node.js execution:** Successful

**Status:** ✅ Completed

---

## Next Lesson

**Day 02 — Operators and Expressions**
