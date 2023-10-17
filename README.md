# Js-objects-loops-and-conditions 
Object related methods


In JavaScript, objects are a fundamental data structure and can have various methods and properties. Here are some commonly used methods that you can perform on objects, along with examples:

1. **Object.keys(obj)**: Returns an array of an object's own property names.

   ```javascript
   const person = { name: 'John', age: 30, job: 'Engineer' };
   const keys = Object.keys(person);
   console.log(keys); // ["name", "age", "job"]
   ```

2. **Object.values(obj)**: Returns an array of an object's own property values.

   ```javascript
   const person = { name: 'John', age: 30, job: 'Engineer' };
   const values = Object.values(person);
   console.log(values); // ["John", 30, "Engineer"]
   ```

3. **Object.entries(obj)**: Returns an array of an object's own property key-value pairs as arrays.

   ```javascript
   const person = { name: 'John', age: 30, job: 'Engineer' };
   const entries = Object.entries(person);
   console.log(entries); // [["name", "John"], ["age", 30], ["job", "Engineer"]]
   ```

4. **Object.assign(target, source1, source2, ...)**: Copies the values of all enumerable properties from one or more source objects to a target object and returns the target object.

   ```javascript
   const target = { a: 1, b: 2 };
   const source = { b: 3, c: 4 };
   const result = Object.assign(target, source);
   console.log(result); // { a: 1, b: 3, c: 4 }
   ```

5. **Object.freeze(obj)**: Freezes an object, making it immutable (properties cannot be added, changed, or removed).

   ```javascript
   const person = Object.freeze({ name: 'John', age: 30 });
   person.name = 'Jane'; // This will not change the name property.
   ```

6. **Object.seal(obj)**: Seals an object, making its properties non-configurable, but still modifiable.

   ```javascript
   const person = Object.seal({ name: 'John', age: 30 });
   delete person.name; // This will not work (non-configurable), but you can still change the age.
   ```

7. **Object.keys(obj).length**: Get the number of own properties in an object.

   ```javascript
   const person = { name: 'John', age: 30, job: 'Engineer' };
   const numProperties = Object.keys(person).length;
   console.log(numProperties); // 3
   ```

8. **Object.hasOwnProperty(key)**: Checks if an object has a specific property.

   ```javascript
   const person = { name: 'John', age: 30, job: 'Engineer' };
   const hasName = person.hasOwnProperty('name');
   console.log(hasName); // true
   ```

These are some of the commonly used methods and properties for working with objects in JavaScript. Objects in JavaScript are highly versatile and can be manipulated in various ways to manage and retrieve data.

===================
# For loops

There are several types of loops available in most programming languages, including `for`, `while`, and `do...while` loops. Each type of loop has its own use cases and syntax. Here, I'll explain these loops and provide examples in JavaScript:

1. **`for` Loop:**

   The `for` loop is commonly used when you know the number of iterations in advance.

   ```javascript
   for (initialization; condition; update) {
       // code to be executed
   }
   ```

   Example:
   ```javascript
   for (let i = 0; i < 5; i++) {
       console.log(`Iteration ${i}`);
   }
   ```

2. **`while` Loop:**

   The `while` loop continues execution as long as a specified condition is true.

   ```javascript
   while (condition) {
       // code to be executed
   }
   ```

   Example:
   ```javascript
   let i = 0;
   while (i < 5) {
       console.log(`Iteration ${i}`);
       i++;
   }
   ```

3. **`do...while` Loop:**

   The `do...while` loop is similar to the `while` loop, but it always executes the code block at least once, and then checks the condition.

   ```javascript
   do {
       // code to be executed
   } while (condition);
   ```

   Example:
   ```javascript
   let i = 0;
   do {
       console.log(`Iteration ${i}`);
       i++;
   } while (i < 5);
   ```

4. **`for...in` Loop (for iterating over object properties):**

   The `for...in` loop is used to loop through the properties of an object.

   ```javascript
   for (let variable in object) {
       // code to be executed
   }
   ```

   Example:
   ```javascript
   const person = { name: 'Alice', age: 30 };
   for (let key in person) {
       console.log(`${key}: ${person[key]}`);
   }
   ```

5. **`for...of` Loop (for iterating over iterable objects like arrays):**

   The `for...of` loop is used for iterating over iterable objects.

   ```javascript
   for (let variable of iterable) {
       // code to be executed
   }
   ```

   Example:
   ```javascript
   const colors = ['red', 'green', 'blue'];
   for (let color of colors) {
       console.log(color);
   }
   ```

These are some of the common types of loops in JavaScript. The choice of loop depends on the specific requirements of your program and the data you are working with.


===============

# forEach & map

Certainly, here are examples of the `forEach` and `map` methods in JavaScript, which are commonly used for iterating over arrays:

**`forEach` Method:**

The `forEach` method is used for executing a provided function once for each element in an array, in order.

Example:

```javascript
const numbers = [1, 2, 3, 4, 5];

numbers.forEach(function(number) {
    console.log(number * 2);
});
```

In this example, the provided function is executed for each element in the `numbers` array, doubling each number and logging the result.

**`map` Method:**

The `map` method creates a new array by applying a function to each element of an existing array.

Example:

```javascript
const numbers = [1, 2, 3, 4, 5];

const doubledNumbers = numbers.map(function(number) {
    return number * 2;
});

console.log(doubledNumbers);
```

In this example, the `map` method creates a new array `doubledNumbers` by doubling each element from the `numbers` array.

Key differences:

- `forEach` is used for iterating over an array, but it doesn't create a new array. It is typically used for performing actions on the array elements without changing the array itself.

- `map` is used to create a new array by applying a function to each element of an existing array. It returns a modified version of the original array.

Both methods are powerful and widely used in JavaScript for array manipulation, but they serve different purposes. Use `forEach` when you need to iterate over elements and perform actions, and use `map` when you want to create a new array based on the original array.



========

# Order of execution

Certainly! Here are 10 coding questions that involve `setImmediate`, `setTimeout`, Promises, and `process.nextTick()`. I'll provide the order in which they execute in `stdout`.

**Question 1:**
```javascript
console.log("Start");
setImmediate(() => console.log("Set Immediate"));
console.log("End");
```
**Order of Execution 1:**
```
Start
End
Set Immediate
```

**Question 2:**
```javascript
console.log("Start");
setTimeout(() => console.log("Set Timeout"), 0);
console.log("End");
```
**Order of Execution 2:**
```
Start
End
Set Timeout
```

**Question 3:**
```javascript
console.log("Start");
setTimeout(() => console.log("Set Timeout 1"), 0);
setImmediate(() => console.log("Set Immediate"));
console.log("End");
```
**Order of Execution 3:**
```
Start
End
Set Timeout 1
Set Immediate
```

**Question 4:**
```javascript
console.log("Start");
setImmediate(() => console.log("Set Immediate 1"));
setTimeout(() => console.log("Set Timeout"), 0);
setImmediate(() => console.log("Set Immediate 2"));
console.log("End");
```
**Order of Execution 4:**
```
Start
End
Set Timeout
Set Immediate 1
Set Immediate 2
```

**Question 5:**
```javascript
console.log("Start");
setTimeout(() => console.log("Set Timeout 1"), 0);
process.nextTick(() => console.log("Next Tick"));
setImmediate(() => console.log("Set Immediate"));
console.log("End");
```
**Order of Execution 5:**
```
Start
End
Next Tick
Set Timeout 1
Set Immediate
```

**Question 6:**
```javascript
console.log("Start");
Promise.resolve().then(() => console.log("Promise 1"));
setTimeout(() => console.log("Set Timeout"), 0);
Promise.resolve().then(() => console.log("Promise 2"));
console.log("End");
```
**Order of Execution 6:**
```
Start
End
Promise 1
Promise 2
Set Timeout
```

**Question 7:**
```javascript
console.log("Start");
setTimeout(() => console.log("Set Timeout 1"), 0);
Promise.resolve().then(() => console.log("Promise"));
setTimeout(() => console.log("Set Timeout 2"), 0);
console.log("End");
```
**Order of Execution 7:**
```
Start
End
Promise
Set Timeout 1
Set Timeout 2
```

**Question 8:**
```javascript
console.log("Start");
setImmediate(() => console.log("Set Immediate"));
Promise.resolve().then(() => console.log("Promise"));
setImmediate(() => console.log("Set Immediate 2"));
console.log("End");
```
**Order of Execution 8:**
```
Start
End
Promise
Set Immediate
Set Immediate 2
```

**Question 9:**
```javascript
console.log("Start");
setImmediate(() => console.log("Set Immediate 1"));
process.nextTick(() => console.log("Next Tick"));
setImmediate(() => console.log("Set Immediate 2"));
console.log("End");
```
**Order of Execution 9:**
```
Start
End
Next Tick
Set Immediate 1
Set Immediate 2
```

**Question 10:**
```javascript
console.log("Start");
setTimeout(() => console.log("Set Timeout"), 0);
setImmediate(() => console.log("Set Immediate"));
process.nextTick(() => console.log("Next Tick"));
console.log("End");
```
**Order of Execution 10:**
```
Start
End
Next Tick
Set Timeout
Set Immediate
```

These questions and their execution orders help you understand the event loop and the order in which different asynchronous tasks are processed in JavaScript.



================
# ES6 Features 

Certainly! Here are some key ES6 (ECMAScript 2015) features explained with examples for an interview:

1. **Arrow Functions:**
   Arrow functions provide a more concise syntax for writing functions.

   ```javascript
   // ES5
   function add(a, b) {
       return a + b;
   }

   // ES6
   const add = (a, b) => a + b;
   ```

2. **Template Literals:**
   Template literals allow embedding expressions inside strings.

   ```javascript
   // ES5
   var name = "John";
   var greeting = "Hello, " + name + "!";

   // ES6
   let name = "John";
   let greeting = `Hello, ${name}!`;
   ```

3. **Destructuring Assignment:**
   Destructuring allows you to extract values from arrays and objects easily.

   ```javascript
   // ES6
   const [x, y] = [1, 2];
   const { firstName, lastName } = { firstName: "John", lastName: "Doe" };
   ```

4. **Spread and Rest Operators:**
   The spread operator spreads elements of an array or properties of an object, and the rest operator collects them.

   ```javascript
   // Spread operator
   const arr1 = [1, 2];
   const arr2 = [...arr1, 3, 4];

   // Rest operator
   function sum(...numbers) {
       return numbers.reduce((total, num) => total + num, 0);
   }
   ```

5. **Let and Const:**
   `let` and `const` provide block-scoped variable declarations.

   ```javascript
   // ES5
   var a = 5;

   // ES6
   let b = 5;
   const c = 10;
   ```

6. **Classes:**
   ES6 introduces class syntax for defining classes and constructor functions.

   ```javascript
   class Person {
       constructor(name) {
           this.name = name;
       }

       greet() {
           return `Hello, my name is ${this.name}.`;
       }
   }
   ```

7. **Promises:**
   Promises provide a better way to work with asynchronous operations.

   ```javascript
   function fetchData() {
       return new Promise((resolve, reject) => {
           // Asynchronous operation
           if (/* success */) {
               resolve(data);
           } else {
               reject(error);
           }
       });
   }
   ```

8. **Default Parameters:**
   You can set default values for function parameters.

   ```javascript
   function greet(name = "World") {
       return `Hello, ${name}!`;
   }
   ```

9. **Modules:**
   ES6 introduces a module system to encapsulate and organize code.

   ```javascript
   // Export
   export function add(a, b) {
       return a + b;
   }

   // Import
   import { add } from "./math";
   ```

10. **Map and Set:**
    Map and Set data structures provide efficient ways to store and manipulate data.

    ```javascript
    const myMap = new Map();
    myMap.set("key", "value");

    const mySet = new Set();
    mySet.add(1);
    mySet.add(2);
    ```

These are some of the key ES6 features, which have become standard in modern JavaScript development. Familiarity with these features can be a valuable asset during interviews.


====
# Deep Clone & Shallow Clone

In JavaScript, when you clone an object, you can perform either a deep clone or a shallow clone, depending on how you want to duplicate the object's structure and values. Here's a detailed explanation of both concepts:

**Shallow Clone:**
A shallow clone creates a new object that is a copy of the original object, but it does not create copies of nested objects or their properties. Instead, it copies references to nested objects. In other words, the top-level object is duplicated, but the nested objects are shared between the original and the clone.

For example:
```javascript
const originalObject = { a: 1, b: { c: 2 } };
const shallowClone = { ...originalObject };

shallowClone.b.c = 3;

console.log(originalObject.b.c); // 3 (changes the original)
```

In the above code, `shallowClone` is a new object, but both the `originalObject.b` and `shallowClone.b` reference the same nested object.

**Deep Clone:**
A deep clone, on the other hand, creates a completely new object with copies of all nested objects and their properties. It results in a completely independent copy of the original object, including all levels of nesting.

To perform a deep clone, you can use various techniques, such as recursion or specialized libraries like Lodash's `_.cloneDeep()` or the `JSON.parse(JSON.stringify(obj))` approach. Here's an example using the `JSON.parse(JSON.stringify(obj))` method:

```javascript
const originalObject = { a: 1, b: { c: 2 } };
const deepClone = JSON.parse(JSON.stringify(originalObject));

deepClone.b.c = 3;

console.log(originalObject.b.c); // 2 (original is not affected)
```

In this case, `deepClone` is a new object, and changes to the nested object do not affect the original.

Keep in mind that deep cloning can be computationally expensive, especially for complex objects with many levels of nesting or large data structures. Shallow cloning is more efficient but may not provide the isolation needed if you want to make independent modifications to objects and their nested structures. Your choice between deep and shallow cloning should depend on your specific use case and performance considerations.
