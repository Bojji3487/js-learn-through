# 1.Destructuring
 **Destructuring** is a JavaScript syntax that allows you to extract values from arrays or properties from objects into distinct variables in a concise and readable way. It simplifies working with complex data structures by "unpacking" values into variables.

## 1. Object Destructuring
Extract values from objects into variables with matching property names.

Eg.
<pre>const user = { 
  name: "John", 
  age: 30, 
  city: "New York" 
};

// Destructure into variables
const { name, age, city } = user;

console.log(name); // "John"
console.log(age);  // 30

</pre>

Renaming Variables:

<pre>
const { name: userName, age: userAge } = user;
console.log(userName); // "John"

</pre>
Default Values:
Useful if a property might be missing:

<pre>
const { name, age, country = "USA" } = user;
console.log(country);
</pre>