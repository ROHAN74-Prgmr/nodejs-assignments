# nodejs-assignments
  
## Module – 1: Node - JavaScript Fundamental

 ### Q1: What is the difference between Java & JavaScript?
- Java Type is a Compiled language, meaning code is converted into machine-readable format before running. 
	js Type is an Interpreted language, meaning code is executed directly without compilation.

-	Java Use Cases: Android apps, enterprise software, big data applications. Javascript use Cases: Front-end web development, game development, server-side development (Node.js).

- Java is statically typed (data types are defined beforehand). JavaScript is dynamically typed (data types are determined at runtime).

-	Java supports multithreading, allowing multiple small programs (threads) to run concurrently inside a process. This enables efficient parallel execution of tasks within the same program. While  Javascript is Single-threaded, meaning it runs one piece of code at a time. However, it uses asynchronous programming to handle concurrent operations, allowing the main thread to continue running while waiting for tasks like network requests or timers to complete.

### Q2. What is JavaScript?

-	JavaScript is a programming language primarily used in web development and it was created by Brendan Eich in 1995.
-	It runs in web browsers and is used to create interactive and dynamic web pages.
-	JavaScript is interpreted, meaning it is executed line-by-line by the browser or the JavaScript engine.
-	Dynamically Typed: Variable types are determined at runtime, allowing for more flexible and less rigid code. and also supports asynchronous programming.
-	It is a cross-platform language that works consistently across different devices and operating systems.
-	Client-side and server-side programming is possible using numerous libraries and frameworks like React, Angular, Vue.js for front-end development, and Express.js for back-end development.

  ###	 Q3. What are the data types supported by JavaScript?

-	It supports several data types which are Number, String, Boolean,undefined, null, object, BigInt

1 - Number 
-	 Represents both integer and floating-point numbers.
Example:
 ```
let age = 25;
 let price = 19.99;
```

 2- String
-  Represents sequences of characters.
 Example:
```
 let name = "John Doe";
 let greeting = 'Hello, world!';
```

 3 - Boolean 
- Represents logical values: true or false.
Example: 
```
let isActive = true;
 let isMember = false;
```
 4 - undefined
- A variable that has been declared but not assigned a value.
Example:
` let x; // x is undefined

5 - Null
- Represents the intentional absence of any object value.
Example:
` let y = null;

 6 – Object

- A collection of key-value pairs, where keys are strings (or Symbols) and values can be any type.

 Example
```
let person = {
    name: "Alice",
    age: 30,
    isMember: true
};
```
 7 – BigInt 
- Represents very large whole numbers.
 Example:

```
let bigIntValue = 1234567890123456789012345678901234567890n;
```

 ### Q4. What are the scopes of a variable in JavaScript?

1. Global Scope
- Definition: Variables declared outside of any function or block have global scope. They can be accessed from anywhere in the code.
```
let globalVar = "I'm a global variable";
function exampleFunction()    {
console.log(globalVar); // Accessible here }
exampleFunction();
console.log(globalVar); // Accessible here too
```

2. Function Scope
-	Definition: Variables declared within a function are local to that function and cannot be accessed outside of it. Function scope is created with the function keyword.
```
function exampleFunction() {
    let localVar = "I'm a local variable";
    console.log(localVar); // Accessible here
}
exampleFunction();
console.log(localVar); // Error: localVar is not defined
```

3. Block Scope
-	Definition: Variables declared with let or const within a block (denoted by {}) are local to that block. This includes blocks defined by loops, conditionals, or simply {} braces.
```
if (true) {
    let blockVar = "I'm a block-scoped variable";
    console.log(blockVar); // Accessible here
}
console.log(blockVar); // Error: blockVar is not defined
```


### Q5. What is Callback?
-	A callback is a function passed as an argument to another function, which is then invoked inside the outer function to complete some kind of action or routine.
-	Callbacks are commonly used in asynchronous programming.
```
function fetchData(callback) {
    setTimeout(() => {
        let data = "Data retrieved from server";
        callback(data); 
    }, 2000);
}
function processData(data) {
    console.log("Processing data: " + data);
}
fetchData(processData);
```
### Q6. What is Closure? Give an example.

- A closure is a feature in JavaScript where an inner function has access to the variables of an outer function, even after the outer function has finished running. This means the inner function "remembers" the environment i.e inner function retains access to the variables and parameters of the outer function.
  
Example
```
function outerFunction() {
    let outerVariable = "Hello, I'm an outer variable";
    function innerFunction() {
        console.log(outerVariable); // Inner function can access outerVariable
    }
    return innerFunction; // Return the inner function
}
const closureFunction = outerFunction();  // outerFunction runs and returns innerFunction
closureFunction(); // This calls innerFunction and logs: "Hello, I'm an outer variable"
```

### Q7. What is the difference between the operators ‘==‘ & ‘===‘?
-	` == ` (Equality Operator) – This operator compares two values for equality after converting them to a common type. This is known as type coercion.
Example
```
console.log(5 == '5'); // true, because '5' is coerced to 5
console.log(0 == false); // true, because false is coerced to 0
```

- `===` (Strict Equality Operator) -  This operator compares two values for equality without performing type conversion. Both values must be of the same type and have the same value to be considered equal.

Example
```
console.log(5 === '5'); // false, because 5 is a number and '5' is a string
console.log(0 === false); // false, because 0 is a number and false is a Boolean
```

 ### Q8. What is the difference between null & undefined?
 
-	undefined - When a variable is declared but not assigned a value, its default value is undefined.

```
let myVariable; // Declared but not initialized
console.log(myVariable); // Logs: undefined
```

-	null -  It is an explicit value that represents empty value which is assigned by the programmer.
```
let user = null; 
console.log(user); 
```

 ### Q9. What would be the result of 2+5+”3″?

-	JavaScript performs the addition operation from left to right.So  because both operands are numbers, so the addition is performed and then  as 7 is a number and "3" is a string JavaScript converts the number to a string and then concatenates the two strings.

 ### Q10. What is the difference between Call & Apply?
-	call method calls a function with a given this value and arguments provided individually 
-	Syntax : func.call(thisArg, arg1, arg2, ...)

-	apply method calls a function with a given this value, and arguments provided as an array
-	Syntax : func.apply(thisArg, [argsArray])







  
