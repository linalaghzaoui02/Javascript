JavaScript and Functions

Welcome to my guide on JavaScript functions. Below are code samples and explanations to help you understand functions in JavaScript.

Write code for given requirements:

javascript
Copy code
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
Addressing the questions:

Syntax for declaring a function:
In JavaScript, functions can be declared using the function keyword, followed by a name, and then parameters inside parentheses.

javascript
Copy code
function functionName(parameters) {
    // body of the function
}
Placement of function:
JavaScript uses function hoisting, which allows you to call a function before it is defined. However, it's recommended to define functions before calling them to make the code clear.

Support for recursive functions:
Yes, JavaScript supports recursive functions. A function can call itself either directly or indirectly.

Accepting multiple parameters of different data types:
Yes, JavaScript functions can accept multiple parameters, and they can be of any data type, including numbers, strings, objects, arrays, or other functions.

Returning multiple values:
Functions in JavaScript can return only one value using the return statement. However, to return multiple values, you can use an array or an object. The destructuring assignment can then be used to extract these values, as seen in the splitString function above.
