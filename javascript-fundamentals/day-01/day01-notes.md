# Day 01 — JavaScript Basics: Detailed Revision Notes

> **Purpose:** These notes are written for a complete beginner. You should be able to return to this file later and understand Day 01 without needing to remember the lesson from chat.

---

# 1. First Understand the Big Picture

Before learning Playwright, we need to learn JavaScript because Playwright automation can be written using JavaScript.

Think of the learning path like this:

~~~text
JavaScript
    ↓
JavaScript fundamentals
    ↓
Playwright
    ↓
Automation tests
    ↓
Automation framework
    ↓
Real-world QA automation
~~~

Since you currently have **zero JavaScript knowledge**, we are starting from the beginning instead of jumping directly into Playwright.

Day 01 is about understanding the basic building blocks of JavaScript.

---

# 2. What Is JavaScript?

**JavaScript is a programming language.**

A programming language lets us give instructions to a computer.

For example:

~~~javascript
console.log("Hello Raj");
~~~

This tells JavaScript:

> Display the text "Hello Raj".

JavaScript is widely used for web development and can also be used for test automation.

For our learning journey, JavaScript will eventually be used to tell Playwright things such as:

- Open a browser
- Open a website
- Find an element
- Enter a username
- Enter a password
- Click Login
- Verify that the user is logged in

We are **not doing those Playwright actions yet**. First we are learning the JavaScript language that will control those actions.

---

# 3. What Is Node.js?

You installed **Node.js** on your computer.

Node.js allows JavaScript code to run outside a web browser.

For our beginner exercises, this means we can create a JavaScript file and run it directly from the VS Code terminal.

For example:

~~~text
day01.js
~~~

can be executed with:

~~~bash
node day01.js
~~~

Think of it simply as:

~~~text
day01.js
   ↓
Node.js reads/runs the JavaScript
   ↓
Result appears in the terminal
~~~

### Important

- **VS Code** = the editor where we write code
- **JavaScript** = the programming language
- **Node.js** = the runtime that executes our JavaScript
- **Terminal** = where we run commands and see output
- **GitHub** = where we store and track the learning project

---

# 4. What Is a .js File?

A file ending with:

~~~text
.js
~~~

is normally a JavaScript source file.

Our Day 01 file is:

~~~text
day01.js
~~~

The .js tells us:

> This file contains JavaScript code.

---

# 5. What Is Code?

**Code is a set of instructions written in a programming language.**

Example:

~~~javascript
console.log("Playwright Automation Masterclass");
~~~

This is one instruction.

Another example:

~~~javascript
const learner = "Raj";
~~~

This tells JavaScript to create a variable called learner and give it the value "Raj".

We will learn many more instructions as the course progresses.

---

# 6. What Is console.log()?

**console.log()** is one of the first JavaScript commands beginners learn.

It is used to display information.

Example:

~~~javascript
console.log("Hello Raj");
~~~

Output:

~~~text
Hello Raj
~~~

Another example:

~~~javascript
console.log("Playwright Automation Masterclass");
~~~

Output:

~~~text
Playwright Automation Masterclass
~~~

## Why Are We Learning This?

Because while learning JavaScript and later while debugging automation tests, we often want to see the value of something.

For example:

~~~javascript
const username = "raj@test.com";

console.log(username);
~~~

Output:

~~~text
raj@test.com
~~~

We can therefore think of:

~~~text
console.log() = "Show me this value"
~~~

---

# 7. Understanding the Parts of console.log()

Look at:

~~~javascript
console.log("Hello Raj");
~~~

There are several parts here.

### console

This provides access to console-related functionality.

You do not need to deeply understand objects yet. For Day 01, just recognize the word **console**.

### Dot (.)

The dot is used to access something provided by console.

### log

log is the function we are calling.

### Parentheses ()

Parentheses are used when calling a function.

We will properly learn functions later.

### "Hello Raj"

This is the value we are asking JavaScript to print.

### Semicolon ;

The semicolon marks the end of a statement in this style of JavaScript.

JavaScript can often work without semicolons, but using them consistently is a good beginner habit.

---

# 8. What Is a Statement?

A **statement** is an instruction written in code.

Example:

~~~javascript
console.log("Hello");
~~~

This is a statement.

Another example:

~~~javascript
const learner = "Raj";
~~~

This is also a statement.

You can think of a statement as:

> One instruction for JavaScript.

---

# 9. What Is a Variable?

A **variable** is a named place/reference used to store a value.

Imagine a box with a label:

~~~text
+-------------------+
| learner           |
|      "Raj"        |
+-------------------+
~~~

The label is **learner**.

The value stored there is **"Raj"**.

In JavaScript:

~~~javascript
const learner = "Raj";
~~~

We can break this into:

- **const** = how we declare the variable
- **learner** = variable name
- **=** = assign a value
- **"Raj"** = value

For now, think of = as:

~~~text
"Put this value into this variable"
~~~

We will study operators, including =, much more in Day 02.

---

# 10. Why Do We Need Variables?

Without variables, we would have to repeatedly write values everywhere.

For example:

~~~javascript
console.log("Raj");
console.log("Raj");
console.log("Raj");
~~~

Instead, we can store the value:

~~~javascript
const learner = "Raj";

console.log(learner);
console.log(learner);
console.log(learner);
~~~

This becomes much more useful in automation.

For example:

~~~javascript
const username = "raj@test.com";

console.log(username);
~~~

Later, Playwright can use that variable as test data.

---

# 11. Variable Names

A variable needs a name.

Examples:

~~~javascript
const username = "raj@test.com";
const browserName = "Chrome";
const browserVersion = 154;
const testCaseId = "TC001";
~~~

Good variable names should describe what the value represents.

Compare:

~~~javascript
const x = "Chrome";
~~~

with:

~~~javascript
const browserName = "Chrome";
~~~

Both can work, but browserName is much easier to understand.

### QA Principle

Good names make automation code easier to read and maintain.

---

# 12. JavaScript Is Case-Sensitive

JavaScript treats uppercase and lowercase letters as different.

These are different names:

~~~text
username
Username
USERName
USERNAME
~~~

For example:

~~~javascript
const username = "raj@test.com";

console.log(username);
~~~

works.

But:

~~~javascript
console.log(Username);
~~~

does not refer to the same variable.

### Important Rule

Be consistent with spelling and capitalization.

---

# 13. const

**const** is used to declare a variable that should not be **reassigned** later.

Example:

~~~javascript
const testCaseId = "TC001";
~~~

We can use:

~~~javascript
console.log(testCaseId);
~~~

But this is not allowed:

~~~javascript
testCaseId = "TC002";
~~~

because we are trying to assign a different value to a const variable.

### Why Is const Useful?

Many test-data values do not need to change during the current piece of code.

Examples:

~~~javascript
const testCaseId = "TC001";
const username = "raj@test.com";
const browserName = "Chrome";
~~~

For these kinds of values, const is a good choice.

### Important Wording

const does **not** mean:

> "This value can never exist differently anywhere in the whole program."

It means:

> "This variable cannot be reassigned to another value."

For Day 01, remember:

~~~text
const = do not reassign this variable
~~~

---

# 14. let

**let** is used when a variable may need to be reassigned.

Example:

~~~javascript
let testPassed = true;

testPassed = false;
~~~

This is allowed.

The value changed from:

~~~text
true
~~~

to:

~~~text
false
~~~

### QA Example

Imagine we start a process:

~~~javascript
let testPassed = false;
~~~

After validation succeeds:

~~~javascript
testPassed = true;
~~~

The variable can change because we used let.

---

# 15. const vs let

This is one of the most important Day 01 concepts.

| Keyword | Can variable be reassigned? | Example |
|---|---|---|
| const | No | const browser = "Chrome"; |
| let | Yes | let status = false; |

### Memory Trick

~~~text
const → fixed assignment
let   → can change assignment
~~~

### Practical Beginner Rule

When you create a variable, ask:

> "Will I need to assign a different value to this variable later?"

If the answer is **No**, use const.

If the answer is **Yes**, use let.

---

# 16. What Is a Data Type?

A **data type** describes the kind of value stored in a variable.

For example:

~~~javascript
const browserName = "Chrome";
~~~

The value is text, so it is a **String**.

Another:

~~~javascript
const browserVersion = 154;
~~~

The value is numeric, so it is a **Number**.

Why is this important?

Because JavaScript needs to know how values should behave.

For Day 01, we learned these five important types/values:

~~~text
String
Number
Boolean
undefined
null
~~~

---

# 17. String

A **String** represents text.

Example:

~~~javascript
const browserName = "Chrome";
const testName = "Verify valid login";
const username = "raj@test.com";
~~~

Strings are commonly written inside quotes.

Examples:

~~~text
"Chrome"
"Verify valid login"
"raj@test.com"
~~~

## Very Important: Quotes Matter

Compare:

~~~javascript
const value1 = 123;
const value2 = "123";
~~~

These are not the same data type.

~~~text
123    → Number
"123"  → String
~~~

The second one is text because it is inside quotes.

### QA Examples

A username is normally text:

~~~javascript
const username = "raj@test.com";
~~~

The browser name is text:

~~~javascript
const browserName = "Chrome";
~~~

The test case name is text:

~~~javascript
const testCaseName = "Verify valid login";
~~~

---

# 18. Number

A **Number** represents numeric data.

Examples:

~~~javascript
const browserVersion = 154;
const retryCount = 3;
const timeout = 5000;
~~~

These are numbers because they are written without quotes.

### Compare

~~~javascript
const a = 5000;
const b = "5000";
~~~

Here:

~~~text
a → Number
b → String
~~~

### QA Examples

A timeout might be stored as a number:

~~~javascript
const timeout = 5000;
~~~

A retry count might be a number:

~~~javascript
const retryCount = 3;
~~~

A browser version number can be represented as a number:

~~~javascript
const browserVersion = 154;
~~~

---

# 19. Boolean

A **Boolean** represents a true/false state.

There are only two Boolean values:

~~~javascript
true
false
~~~

Examples:

~~~javascript
const isLoggedIn = true;
const testPassed = false;
const isVisible = true;
~~~

### QA Examples

~~~javascript
const testPassed = true;
~~~

means:

> The test passed.

~~~javascript
const testPassed = false;
~~~

means:

> The test did not pass.

~~~javascript
const isVisible = true;
~~~

means:

> We are representing that the element is visible.

### Important Difference

Do not confuse:

~~~javascript
true
~~~

with:

~~~javascript
"true"
~~~

The first is Boolean.

The second is String.

The quotes change the type.

---

# 20. Undefined

**undefined** means a variable exists, but no value has been assigned to it.

Example:

~~~javascript
let errorMessage;
~~~

We created the variable errorMessage, but we did not give it a value.

Therefore JavaScript gives it the value:

~~~text
undefined
~~~

Example:

~~~javascript
let actualResult;

console.log(actualResult);
~~~

Output:

~~~text
undefined
~~~

### Simple Mental Model

~~~text
Variable exists
       ↓
No value assigned yet
       ↓
undefined
~~~

### QA Example

You might have a variable ready to receive an actual result:

~~~javascript
let actualResult;
~~~

Later, you may assign a real value to it.

---

# 21. Null

**null** is used when we intentionally represent **no value**.

Example:

~~~javascript
const testData = null;
~~~

This means:

> We intentionally set this variable to "no value".

### Compare undefined and null

#### Undefined

~~~javascript
let actualResult;
~~~

No value was assigned.

Result:

~~~text
undefined
~~~

#### Null

~~~javascript
const actualResult = null;
~~~

We intentionally assigned:

~~~text
null
~~~

### Easy Memory Trick

~~~text
undefined → no value assigned
null      → intentionally no value
~~~

---

# 22. The Five Values We Must Recognize

| Example | Type/value | Beginner meaning |
|---|---|---|
| "Chrome" | String | Text |
| 154 | Number | Numeric value |
| true | Boolean | True |
| false | Boolean | False |
| let errorMessage; | undefined | No value assigned |
| null | null | Intentionally no value |

The five key categories we practiced are:

~~~text
String
Number
Boolean
undefined
null
~~~

---

# 23. Very Important Quotes Rule

One of the easiest ways to recognize a String is to look for quotes.

### String

~~~javascript
"123"
"true"
"Chrome"
"Raj"
~~~

### Not String

~~~javascript
123
true
~~~

So:

~~~text
"true" → String
true   → Boolean

"123"  → String
123    → Number
~~~

This is a very important concept for automation test data.

---

# 24. Our Day 01 QA Example

We created a small login test data example:

~~~javascript
const testCaseId = "TC001";
const testCaseName = "Verify valid login";
const username = "raj@test.com";
const password = "Dummy@123";
let testPassed = true;
~~~

Let's understand each line.

### Line 1

~~~javascript
const testCaseId = "TC001";
~~~

- Variable name = testCaseId
- Value = "TC001"
- Type = String
- const = we do not plan to reassign the variable

### Line 2

~~~javascript
const testCaseName = "Verify valid login";
~~~

- Variable name = testCaseName
- Value = "Verify valid login"
- Type = String

### Line 3

~~~javascript
const username = "raj@test.com";
~~~

- Variable name = username
- Value = "raj@test.com"
- Type = String

### Line 4

~~~javascript
const password = "Dummy@123";
~~~

- Variable name = password
- Value = "Dummy@123"
- Type = String

### Line 5

~~~javascript
let testPassed = true;
~~~

- Variable name = testPassed
- Value = true
- Type = Boolean
- let = value may be reassigned later

---

# 25. Printing Our QA Data

We then used:

~~~javascript
console.log("Test Case ID:", testCaseId);
console.log("Test Case Name:", testCaseName);
console.log("Username:", username);
console.log("Password:", password);
console.log("Test Passed:", testPassed);
~~~

Notice that console.log() can receive more than one thing.

For example:

~~~javascript
console.log("Username:", username);
~~~

The first part:

~~~text
"Username:"
~~~

is a label.

The second part:

~~~text
username
~~~

is the variable whose value we want to print.

Output:

~~~text
Username: raj@test.com
~~~

This is useful for debugging because the label tells us what the value represents.

---

# 26. Browser/Test Data Example

We also practiced:

~~~javascript
const browserName = "Chrome";
const browserVersion = 154;
const isLoggedIn = true;
let errorMessage;
const testData = null;
~~~

Let's identify them.

| Variable | Value | Type |
|---|---|---|
| browserName | "Chrome" | String |
| browserVersion | 154 | Number |
| isLoggedIn | true | Boolean |
| errorMessage | no assigned value | undefined |
| testData | null | null |

This small example gave us practice with all the main concepts from Day 01.

---

# 27. How We Ran the Code

Our file is:

~~~text
day01.js
~~~

The terminal was already inside:

~~~text
playwright-automation-masterclass\javascript-fundamentals\day-01
~~~

Therefore we ran:

~~~bash
node day01.js
~~~

Node.js executed the file and printed the result.

The basic process is:

~~~text
Write code
   ↓
Save file
   ↓
Open terminal
   ↓
Run: node day01.js
   ↓
JavaScript executes
   ↓
See output
~~~

---

# 28. The MODULE_NOT_FOUND Error We Experienced

At first, we ran:

~~~bash
node javascript-fundamentals/day-01/day01.js
~~~

But the terminal was already inside:

~~~text
...\javascript-fundamentals\day-01
~~~

So the command used a path relative to our current folder that did not exist.

Node therefore reported:

~~~text
MODULE_NOT_FOUND
~~~

### The lesson

Before running a file, look at the current terminal path.

If you are already inside the folder containing the file:

~~~bash
node day01.js
~~~

is enough.

### General rule

A command containing a path is interpreted relative to your current working directory unless you provide an absolute path.

You do not need to memorize the technical wording yet. Just remember:

> **Check where the terminal is before giving Node the file path.**

---

# 29. Comments in JavaScript

Our file contains lines like:

~~~javascript
// Day 01 — JavaScript Basics
~~~

The **//** means:

> The rest of this line is a comment.

Comments are written for humans. JavaScript does not execute the comment as a program instruction.

Example:

~~~javascript
// This is a comment
console.log("Hello");
~~~

Output:

~~~text
Hello
~~~

The comment does not appear in the output.

### Why Are Comments Useful?

Comments can explain:

- What a section of code does
- Why something exists
- Which exercise the code belongs to
- Important QA information

Good comments can make a test automation project easier to understand.

---

# 30. Basic JavaScript Syntax We Saw

Here is the general shape we used:

~~~javascript
const variableName = value;
~~~

Example:

~~~javascript
const browserName = "Chrome";
~~~

And:

~~~javascript
let variableName = value;
~~~

Example:

~~~javascript
let testPassed = true;
~~~

For output:

~~~javascript
console.log(value);
~~~

Example:

~~~javascript
console.log(browserName);
~~~

Do not worry about memorizing every symbol immediately. Repetition will make the syntax familiar.

---

# 31. What Does the = Sign Mean Here?

You will see:

~~~javascript
const browserName = "Chrome";
~~~

For Day 01, understand the **=** sign as **assignment**.

It means:

> Put the value "Chrome" into the variable browserName.

It does **not** mean "these two things are equal" in the way mathematical equality is written.

We will study comparison operators and equality operators properly in **Day 02**.

For now:

~~~text
= → assignment
~~~

---

# 32. Why Variable Types Matter in QA

In manual testing, you already work with different kinds of information.

For example:

~~~text
Test Case ID       → TC001
Test Case Name     → Verify valid login
Browser Version    → 154
Test Passed        → true
Error Message      → no value yet
Response Data      → no value
~~~

JavaScript lets us represent those values in code.

This is why JavaScript basics are directly useful for a QA engineer.

Later, these same ideas appear in:

- Playwright test data
- Assertions
- API responses
- Configuration
- Test results
- Environment variables
- Page Object Models
- Utility functions

---

# 33. Security Rule for GitHub

Our GitHub repository is public.

We used:

~~~javascript
const password = "Dummy@123";
~~~

This is fake/dummy test data.

### Never commit real secrets to a public repository.

Do not put real:

- Passwords
- API keys
- Authentication tokens
- Access tokens
- Private credentials
- Database passwords
- Secret keys

inside publicly visible source code.

This is an important professional habit for an Automation QA Engineer.

---

# 34. Common Day 01 Beginner Mistakes

## Mistake 1: Putting quotes around a Number

Incorrect if you want a Number:

~~~javascript
const retryCount = "3";
~~~

This is a String.

Number:

~~~javascript
const retryCount = 3;
~~~

---

## Mistake 2: Putting quotes around a Boolean

Incorrect if you want Boolean:

~~~javascript
const testPassed = "true";
~~~

This is a String.

Boolean:

~~~javascript
const testPassed = true;
~~~

---

## Mistake 3: Capitalizing Boolean values

Use:

~~~javascript
true
false
~~~

not:

~~~javascript
True
False
~~~

JavaScript is case-sensitive.

---

## Mistake 4: Expecting let errorMessage; to contain null

It contains:

~~~text
undefined
~~~

because no value was assigned.

---

## Mistake 5: Confusing undefined and null

Remember:

~~~text
undefined → no value assigned
null      → intentionally no value
~~~

---

## Mistake 6: Using the wrong file path

Always check the terminal's current folder before running:

~~~bash
node day01.js
~~~

or another path.

---

# 35. Day 01 Cheat Sheet

## Print something

~~~javascript
console.log("Hello");
~~~

## Create a constant

~~~javascript
const browser = "Chrome";
~~~

## Create a changeable variable

~~~javascript
let testPassed = false;
~~~

## String

~~~javascript
const name = "Raj";
~~~

## Number

~~~javascript
const retryCount = 3;
~~~

## Boolean

~~~javascript
const isLoggedIn = true;
~~~

## Undefined

~~~javascript
let errorMessage;
~~~

## Null

~~~javascript
const response = null;
~~~

## Run a JavaScript file

~~~bash
node day01.js
~~~

---

# 36. One-Page Memory Table

| Concept | Meaning | Example |
|---|---|---|
| JavaScript | Programming language | Our automation language |
| Node.js | Runs JavaScript outside a browser | node day01.js |
| .js | JavaScript file extension | day01.js |
| Variable | Named place/reference for a value | username |
| const | Variable cannot be reassigned | const id = "TC001"; |
| let | Variable can be reassigned | let passed = false; |
| String | Text | "Chrome" |
| Number | Numeric value | 154 |
| Boolean | True/false | true |
| undefined | No value assigned | let error; |
| null | Intentionally no value | const data = null; |
| console.log() | Prints information | console.log(username) |
| // | Comment | // explanation |

---

# 37. Mental Model for Day 01

When you see:

~~~javascript
const browserName = "Chrome";
~~~

read it in your head as:

> Create a constant variable called browserName and store the text "Chrome" in it.

When you see:

~~~javascript
let testPassed = false;
~~~

read it as:

> Create a changeable variable called testPassed and store the Boolean value false in it.

When you see:

~~~javascript
console.log(testPassed);
~~~

read it as:

> Print the current value of testPassed.

When you see:

~~~javascript
let errorMessage;
~~~

read it as:

> Create the variable errorMessage, but I have not assigned a value yet.

When you see:

~~~javascript
const testData = null;
~~~

read it as:

> Create the variable testData and intentionally give it no value.

This way of reading code is more useful than memorizing definitions.

---

# 38. Day 01 Practice Code — Final Version

Your Day 01 file contains this practice:

~~~javascript
// Day 01 — JavaScript Basics
// Hands-on practice for the first JavaScript lesson.

console.log("Playwright Automation Masterclass");

const learner = "Raj";
let completedLessons = 0;

console.log("Learner:", learner);
console.log("Completed lessons:", completedLessons);

// QA Test Data Practice

const testCaseId = "TC001";
const testCaseName = "Verify valid login";
const username = "raj@test.com";
const password = "Dummy@123";
let testPassed = true;

console.log("Test Case ID:", testCaseId);
console.log("Test Case Name:", testCaseName);
console.log("Username:", username);
console.log("Password:", password);
console.log("Test Passed:", testPassed);

// JavaScript Data Types Practice

const browserName = "Chrome";
const browserVersion = 154;
const isLoggedIn = true;
let errorMessage;
const testData = null;

console.log("Browser:", browserName);
console.log("Browser Version:", browserVersion);
console.log("Logged In:", isLoggedIn);
console.log("Error Message:", errorMessage);
console.log("Test Data:", testData);
~~~

---

# 39. What You Should Be Able to Explain Without Notes

Before moving forward from Day 01, you should be able to explain these in your own words:

### JavaScript
What is JavaScript and why are we learning it?

### Node.js
What is Node.js and why did we install it?

### Variable
What is a variable?

### const
Why did we use const for testCaseId?

### let
Why did we use let for testPassed?

### String
Why is "Chrome" a String?

### Number
Why is 154 a Number?

### Boolean
Why is true a Boolean?

### Undefined
Why does this:

~~~javascript
let errorMessage;
~~~

produce undefined?

### Null
Why is this:

~~~javascript
const testData = null;
~~~

different from undefined?

### Console
What does console.log() do?

### Terminal
Why did node day01.js work when we were already inside the Day 01 folder?

If you can explain these concepts, your Day 01 foundation is strong.

---

# 40. Self-Check Questions

Try answering these without looking at the answers.

## Q1

What is the type of:

~~~javascript
const browser = "Chrome";
~~~

## Q2

What is the type of:

~~~javascript
const retryCount = 3;
~~~

## Q3

What is the type of:

~~~javascript
const testPassed = false;
~~~

## Q4

What value does this variable contain initially?

~~~javascript
let actualResult;
~~~

## Q5

What does this mean?

~~~javascript
const expectedResult = null;
~~~

## Q6

Which keyword should normally be used when a variable must be reassigned later?

## Q7

What is wrong with this if we want a Boolean?

~~~javascript
const isVisible = "true";
~~~

## Q8

What command runs day01.js when the terminal is already inside the Day 01 folder?

---

# 41. Answers to Self-Check

### A1
String.

### A2
Number.

### A3
Boolean.

### A4
Undefined.

### A5
The variable was intentionally assigned no value.

### A6
let.

### A7
"true" is a String, not a Boolean.

Correct Boolean:

~~~javascript
const isVisible = true;
~~~

### A8

~~~bash
node day01.js
~~~

---

# 42. Day 01 Completion Record

**Hands-on:** ✅ Completed

**Node.js execution:** ✅ Successful

**Data type practice:** ✅ Completed

**Checkpoint:** ✅ 5/5

**Revision notes:** ✅ Completed

**Status:** ✅ Day 01 Complete

---

# 43. What Comes Next

The next lesson is:

**Day 02 — Operators and Expressions**

We will learn how JavaScript performs operations and comparisons, including:

~~~text
+
-
*
/
%
>
<
>=
<=
===
!==
&&
||
!
~~~

These concepts will later become important for:

- Test conditions
- Validation
- Assertions
- Pass/fail logic
- Playwright test behavior

**Do not study the Day 02 operators from this file yet.** Day 01 is intentionally focused on building the foundation first.
