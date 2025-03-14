# Javascript Code Consistency

## Naming Conventions

Ensure consistency and readability in variable, function, and class names.

- Use **camelCase** for variables and functions.
- Use **PascalCase** for classes.
- Use **UPPER_CASE** for constants.

```js
// Good Practice
const MAX_USERS = 100; // Constant
let userCount = 10; // Variable
function fetchUserData() { ... } // Function
class UserProfile { ... } // Class

// Bad Practice
const MaxUsers = 100;
let User_Count = 10;
function Fetch_User_Data() { ... }
```

## Variable Declarations

Improve code safety and avoid hoisting issues. Avoid using `var` and use `const` & `let` 

```js
// Good Practice
const API_URL = "https://api.example.com";
let count = 0;

// Bad Practice
var user = "John";
```

## Function Standards

Keep functions short and focused (single responsibility). 

- Give functions names that tell you what they do.
- Choose meaningful names for your variables, not just a, b, c.
- Use arrow function for simple logic.

```js
// Good Practice
const add = (a, b) => a + b;
function getUserProfile(userId) { return fetch(`/api/users/${userId}`); }

// Bad Practice
function processDataAndSendEmail() { ... } // Too many responsibilities
```

**Default parameters:**

Default function parameters allow named parameters to be initialized with default values if no value or undefined is passed.

```js
// Single Parameter
function greet(name = 'Guest') {
  console.log(`Hello, ${name}!`);
}
greet();         // output: Hello, Guest!
greet('John');  // output: Hello, John!

// Multiple Parameters
function multiply(a, b = 1) {
  return a * b;
}
multiply(5);    // output: 5
multiply(5, 2);  // output: 10
```

## String Handling

Improve readability and reduce errors. Use template literals instead of concatenation.

```js
// Good Practice
const user = "Alice";
console.log(`Hello, ${user}!`);

// Bad Practice
console.log("Hello, " + user + "!");
```

**Be careful with Automatic type conversion**

Beware of numbers, can be converted to `string` or `NaN` by accident. Therefore, consider implementing type testing before sensitive operations or consider using TypeScript for safe typing.

```js
let sum = "5" + 1; // "51" (string concatenation)
// In the code above, typeof sum is a string

let sub = "5" - 1; // 4 (string converted to number)
// In the code obove, typeof sub in a number

let lang = "JavaScript"; // typeof name is string
lang = 15; // changes typeof x to a number
```

## Object and Array Handling

Use modern ES6+ features. Use Object / Array destructuring, it allows you to extract multiple properties from an object or elements from an array in a single statement, reducing the amount of code you need to write.

```js
// Good Practice
const user = { name: "Alice", age: 25 };
const { name, age } = user;

const numbers = [1, 2, 3];
const [first, second] = numbers;

const { height = 180 } = person; // uses default value if height is undefined

// Bad Practice
const name = user.name;
const age = user.age;
```

Use `map`, `filter`, `reduce` array methods instead of `for` loops for cleaner code.

```js
// Good Practice
const numbers = [1, 2, 3, 4, 5];
const squared = numbers.map(num => num * num);

// Bad Practice
const squared = [];
for (let i = 0; i < numbers.length; i++) {
  squared.push(numbers[i] * numbers[i]);
}
```

## Code Readability and Maintainability

- Use consistent formatting.
- Indenting and spaces: 2 spaces (To be configured in text editor of choice)
- Linting:
    - Eslint: code recommendation with formatting off
    - prettier: for code formatting
- Comments:
    - Comments should be available for things that are complicated.
    - Add comments only where necessary.

## Error Handling

Prevent app crashes due to unhandled errors. Use `try/catch` to catch errors in risky spots.

```js
try {
  riskyCode(); 
} catch (error) {
  console.log(error, contextDetails);
  showFallback(); 
}
```

## Control Flow and Logical Operators

Use `===` instead of `==` to avoid type coercion.

```js
// Good Practice
console.log(5 === "5"); // false

// Bad Practice
console.log(5 == "5"); // true (unexpected behavior)
```

Use Optional Chaining (`?.`) to avoid errors.

```js
// Good Practice
console.log(user.profile?.name); // Avoids TypeError

// Bad Practice
console.log(user.profile.name); // Error if profile is undefined
```

## Asynchronous Code

Asynchronous JavaScript is essential for handling tasks like API calls, file operations, or database queries efficiently. Below are the best practices for writing clean and maintainable asynchronous code.

**Use `async/await` Instead of Callbacks:**

```js
async function fetchUserData(userId) {
  try {
    const response = await fetch(`https://api.example.com/users/${userId}`);
    const data = await response.json();
    return data;
  } catch (error) {
    console.error("Error fetching user data:", error);
  }
}
```

**Handle Errors with Try-Catch:**

Use `try...catch` inside async functions

```js
async function getData() {
  try {
    const response = await fetch("https://api.example.com/data");
    if (!response.ok) throw new Error("Failed to fetch data");
    return await response.json();
  } catch (error) {
    console.error("Error:", error);
  }
}
```

**Parallel Execution:**

Use `Promise.all` for running multiple independent async tasks concurrently.

```js
async function fetchMultipleUsers(userIds) {
  const userPromises = userIds.map(id => fetch(`https://api.example.com/users/${id}`).then(res => res.json()));
  return await Promise.all(userPromises);
}
```

**Execute Cleanup Code:**

Use `finally` to execute cleanup code always.

```js
async function processData() {
  try {
    console.log("Fetching data...");
    const data = await fetch("https://api.example.com/data").then(res => res.json());
    console.log("Data received:", data);
  } catch (error) {
      console.error("Error fetching data:", error);
  } finally {
    console.log("Cleanup: Closing connections...");
  }
}
```

**Avoid Mixing `async/await` and `.then/.catch`**

Stick to only one approach.

```js
// Good Practice
async function getData() {
  try {
    const response = await fetch("https://api.example.com/data");
    return await response.json();
  } catch (error) {
    console.error("Error fetching data:", error);
  }
}

// Bad Practice
async function getData() {
  return fetch("https://api.example.com/data")
    .then(response => response.json())
    .catch(error => console.error("Error fetching data:", error));
}
```