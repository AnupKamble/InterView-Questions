

## 1. What is Javascript? 
 ### JavaScript is a high-level, dynamically typed, interpreted programming language. It was originally designed for creating dynamic and interactive web pages, but has since become one of the most popular programming languages and is now used for a wide range of applications, including server-side programming, desktop applications, and mobile app development. JavaScript is often used in conjunction with HTML and CSS to build modern, interactive web applications. It is an object-oriented language with a syntax that is similar to other programming languages such as C and Java. JavaScript is also known for its event-driven and asynchronous programming model, which makes it well suited for building real-time applications.


<br>


 ---
<br>


## 2 . What are the data types in JavaScript?
### Number: for numeric values, both integer and floating-point.
### String: for sequences of characters, e.g. "hello".
### Boolean: for logical values, either true or false.
### Undefined: a variable that has been declared but has not been assigned a value.
### Null: a special value representing the absence of any object value.
### Object: for complex data structures, including arrays, functions, and dates.
### Symbol: a new data type in ECMAScript 6 that is unique and immutable.


<br>


---
<br>


## 3. What are variables in JavaScript?
### Variables in JavaScript are containers that hold values which can be of various data types, such as strings, numbers, booleans, arrays, objects, etc. Variables are declared using the var, let, or const keywords, followed by a name and an optional assignment operator. The value can then be changed or reassigned as needed throughout the code. For example:

**javascript** 

`let name = "John Doe";`

`console.log(name);   // Output: "John Doe"`

`name = "Jane Doe";`

`console.log(name);   // Output: "Jane Doe" `



<br>


---
<br>


## 4. What is a function in JavaScript and how do you define it?
### A function in JavaScript is a block of code that can be executed repeatedly, and that can take inputs (arguments) and produce outputs (return values). Functions are defined using the function keyword, followed by a function name, a list of parameters enclosed in parentheses, and a block of code surrounded by curly braces. Functions can be invoked (called) by using the function name followed by its parameters in parentheses. For example:

**javascript**

`function greet(name) { `

`console.log("Hello, " + name + "!");`
`}`

`greet("John Doe");   // Output: "Hello, John Doe!"`


<br>


---

<br>


## 5. What is closure in JavaScript?
### A closure in JavaScript is an inner function that has access to the variables and functions defined in its outer scope, even after the outer function has returned. A closure allows a function to "remember" its state, even after it has completed its execution. The closure has access to the variables and functions in its outer scope, and retains access to these variables even after the outer function has completed its execution. This makes closures useful for creating private variables and methods, and for creating functions that can be passed around as first-class objects. Here's an example of closure in JavaScript:

**javascript**

`function outerFunction(x) {`
  `return function innerFunction(y) {`
    `return x + y;`
  `}`
`}`

`const add5 = outerFunction(5);`
`console.log(add5(3)); // Output: 8`


<br>


---

<br>


## 6.What is the difference between let , var and const in JavaScript?

### The main difference between var and let in JavaScript is the way they handle variable scoping and hoisting.var is function scoped, which means that a variable declared with var is accessible within the entire function it was declared in. It is also hoisted to the top of its scope, meaning that it can be used before it is declared.

### let, on the other hand, is block scoped, which means that a variable declared with let is only accessible within the block it was declared in. It is not hoisted to the top of its scope like var, which means that it cannot be used before it is declared.

### const,const is also block scoped, but it cannot be reassigned to a new value once it has been declared. This makes it useful for declaring constants or values that should not change throughout the program.

**Here's an example to illustrate the difference:**

`function example() {`
  `console.log(x); // Output: undefined`
  `var x = 1;`
  `console.log(x); // Output: 1`
`}`

`function example2() {`
  `console.log(y); // ReferenceError: y is not defined`
  `let y = 2;`
  `console.log(y); // Output: 2`
`}`

`function example() {`
  `var x = 1;`
  `let y = 2;`
  `const z = 3;`

  `x = 4;`
 ` y = 5;`
  `// z = 6; // TypeError: Assignment to constant variable.`

  `console.log(x); // Output: 4`
  `console.log(y); // Output: 5`
  `console.log(z); // Output: 3`
}


### In conclusion, const is best used for declaring constants, let for declaring variables that need to be reassigned, and var should generally be avoided in favor of let or const due to its function scoping and hoisting behavior.



<br>
---
<br>


## 7 What is the difference between null and undefined in JavaScript?
### In JavaScript, null and undefined are both values that indicate the absence of a value or object, but they have different meanings.

### undefined is the default value assigned to variables that have been declared but have not been assigned a value. It means that the variable has been declared but has no value assigned to it.

### null, on the other hand, is a value that is explicitly assigned to a variable to indicate that it has no value. It represents an intentional non-value, and is often used to indicate that an object reference has been intentionally cleared.

**Here's an example to illustrate the difference:**


`let x;`
`console.log(x); // Output: undefined`

`x = null;`
`console.log(x); // Output: null`

### In conclusion, undefined indicates that a variable has been declared but has no value assigned to it, while null represents an intentional non-value.


<br>

---


<br>

## 8. What is hoisting in JavaScript?

### Hoisting is a behavior in JavaScript where variables and function declarations are moved to the top of their respective scopes, regardless of where they are actually declared in the code.

### In other words, the JavaScript engine "hoists" the declarations to the top of the scope, making them available for use before the code execution reaches their actual declarations. This behavior is only applicable to the declarations and not to the assignments, which remain in their original positions in the code.

**Here's an example to illustrate hoisting:**


`console.log(x); // Output: undefined`
`var x = 1;`

`console.log(y); // ReferenceError: y is not defined`
`let y = 2;`

### In the first example, x is declared with var, so its declaration is hoisted to the top of the scope and it is accessible even before its assignment is executed. In the second example, y is declared with let, so it is not hoisted and is not accessible before its declaration.

### It is important to note that hoisting can lead to unexpected behavior in code, especially when using var. The use of let and const is generally preferred over var due to their block scoping behavior, which can make code easier to understand and prevent unintended behavior.


<br>

--- 


<br>

## 9. What is the difference between == and === in JavaScript?
### In JavaScript, == and === are two comparison operators used to compare values. They both perform equality checks, but there are some important differences between them.

### == performs type coercion before comparison, meaning that it will attempt to convert the operands to a common type before comparing them. For example, '5' == 5 is true because the string '5' is implicitly converted to the number 5 before comparison.

### ===, on the other hand, does not perform type coercion before comparison. It checks for both value and type equality, meaning that the operands must be of the same type and have the same value to be considered equal. For example, '5' === 5 is false because the string '5' is not equal to the number 5 both in value and type.

**Here's an example to illustrate the difference:**


`console.log(5 == '5'); // Output: true`
`console.log(5 === '5'); // Output: false`

<br>

### In conclusion, == is less strict and may lead to unexpected results due to type coercion, while === is more strict and checks for both value and type equality. The use of === is generally recommended over == for more accurate and predictable comparison results.


<br>

--- 

<br>


## 10.