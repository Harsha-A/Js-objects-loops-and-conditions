# Object.methods
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
