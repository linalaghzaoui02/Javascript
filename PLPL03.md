 # JavaScript and Functions


```javascript
// Multiply two numbers
function multiply(a, b) {
    return a * b;
}

// Recursive function to calculate factorial
function factorial(n) {
    if (n <= 1) {
        return 1;
    }
    return n * factorial(n - 1);
}

// Split a string into two strings
function splitString(str) {
    const middleIndex = Math.floor(str.length / 2);
    return [str.slice(0, middleIndex), str.slice(middleIndex)];
}

// Call the functions and save the results
let result1 = multiply(5, 3);    // 15
let result2 = factorial(5);      // 120
let [string1, string2] = splitString("HelloWorld"); // ["Hello", "World"]

// Test pass-by-reference vs pass-by-value
function testPassBy(arr) {
    arr[0] = 100;
    return arr;
}
let originalArray = [1, 2, 3];
let modifiedArray = testPassBy([...originalArray]);
```


 ## Syntax for declaring a function:
In JavaScript, functions can be declared using the function keyword, followed by a name, and then parameters inside parentheses.

```javascript
function functionName(parameters) {
    // body of the function
}
```

 ## Placement of function:
JavaScript uses function hoisting which allows you to call a function before it is defined. However, it's recommended to define functions before calling them to make the code clear.

 ## Support for recursive functions:
Yes, JavaScript supports recursive functions. A function can call itself either directly or indirectly.

 ## Accepting multiple parameters of different data types:
Yes, JavaScript functions can accept multiple parameters, and they can be of any data type, including numbers, strings, objects, arrays, or other functions.

 ## Returning multiple values:
Functions in JavaScript can return only one value using the return statement. However, to return multiple values, you can return an array or an object. The destructuring assignment can then be used to extract these values, as seen in the splitString function above.

 ## Pass-by-reference or value:
JavaScript is primarily pass-by-value for primitive types (like numbers and strings). For objects (which include arrays and functions), it passes a reference to the object. In the testPassBy function above, we pass an array (object) and modify it, showing that the reference is passed.

 ## Storage of arguments, parameters, and local variables:
In JavaScript, arguments, parameters, and local variables are stored on the call stack. However, if the function creates an object, the object is stored on the heap, and its reference is put on the stack.

 ## Scoping rules:
JavaScript uses lexical (or static) scoping. Variables declared inside a function are local to that function and can't be accessed outside. With the introduction of ES6, we now have block-level scoping for variables declared with let and const.

 ## Side-effects:
Yes, side-effects are possible in JavaScript. A function can modify a global variable, change an object property, or alter an array. However, functional programming paradigms discourage side-effects for predictability and maintainability.

 ## Storage of local variable values:
Local variables are stored on the call stack. Objects and arrays (non-primitives) are stored on the heap, but their references are stored on the stack.

 ### Other important aspects:
JavaScript supports both function declarations and function expressions. The latter can be anonymous.
Arrow functions, introduced in ES6, provide a concise way to write functions and have a different this binding behavior.
JavaScript supports closures, which allow inner functions to access the outer function's variables.
