

## 1. What is Javascript? 
 ### JavaScript is a high-level, dynamically typed, interpreted programming language. It was originally designed for creating dynamic and interactive web pages, but has since become one of the most popular programming languages and is now used for a wide range of applications, including server-side programming, desktop applications, and mobile app development. JavaScript is often used in conjunction with HTML and CSS to build modern, interactive web applications. It is an object-oriented language with a syntax that is similar to other programming languages such as C and Java. JavaScript is also known for its event-driven and asynchronous programming model, which makes it well suited for building real-time applications.

 ---

## 2 . What are the data types in JavaScript?
### Number: for numeric values, both integer and floating-point.
### String: for sequences of characters, e.g. "hello".
### Boolean: for logical values, either true or false.
### Undefined: a variable that has been declared but has not been assigned a value.
### Null: a special value representing the absence of any object value.
### Object: for complex data structures, including arrays, functions, and dates.
### Symbol: a new data type in ECMAScript 6 that is unique and immutable.

---

## 3. What are variables in JavaScript?
### Variables in JavaScript are containers that hold values which can be of various data types, such as strings, numbers, booleans, arrays, objects, etc. Variables are declared using the var, let, or const keywords, followed by a name and an optional assignment operator. The value can then be changed or reassigned as needed throughout the code. For example:

**javascript** 

`let name = "John Doe";`

`console.log(name);   // Output: "John Doe"`

`name = "Jane Doe";`

`console.log(name);   // Output: "Jane Doe" `

---

## 4. What is a function in JavaScript and how do you define it?
### A function in JavaScript is a block of code that can be executed repeatedly, and that can take inputs (arguments) and produce outputs (return values). Functions are defined using the function keyword, followed by a function name, a list of parameters enclosed in parentheses, and a block of code surrounded by curly braces. Functions can be invoked (called) by using the function name followed by its parameters in parentheses. For example:

**javascript**

`function greet(name) { `

`console.log("Hello, " + name + "!");`
`}`

`greet("John Doe");   // Output: "Hello, John Doe!"`


---


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


---


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





