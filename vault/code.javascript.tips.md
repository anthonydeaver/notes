---
id: ddf85ae8-c8df-4120-8515-2062c30a96c3
title: Tips
desc: ''
updated: 1618946904329
created: 1618404325839
---

1. Ternary Operator
If you just want to assign a value to a variable based on a condition, this is a great alternative.
```javascript
const age = 15;

// Longhand
let message;
if (age > 18) {
  message = "The person is an adult";
} else {
  message = "The person is not an adult";
}

// Longhand
const message =
  age > 18 ? "The person is an adult" : "The person is not an adult";
```
You can also add an equivalent of an else if statement to this shorthand as shown.
```javascript
const age = 15;

// Longhand
if (age > 18) {
  message = "The person is an adult";
} else if (age > 12) {
  message = "The person is a teenager";
} else {
  message = "The person is not an adult";
}

// Shorthand
const age = 15;
const message =
  age > 18
    ? "The person is an adult"
    : age > 12275
    ? "The person is a teenager"
    : "The person is a child";
```
2. Assigning Default Values
If you want to assign a default value to a variable only if it is either `null` or `undefined`, you can use the nullish coalescing operator (`??`) to do this.
```javascript
const message;

// Longhand
if (message === null || message === undefined) {
  message = "Hello";
}
console.log(message + "there");

// Shorthand
console.log((message ?? "Hello") + "there");
```
3. Short-Circuit Evaluation with ??
The ?? operator executes the right-side expression only if the left-side expression returns anything other than null or undefined.

4. Checking if a Property Exists within an Object
Generally, when you access the properties within an object using the . operator, if any of them are not defined then an error is thrown. When you use the ?. operator, if any of the properties are either null or undefined, the operator returns undefined instead of throwing an error.

5. Default Values with ??=
This operator is similar to the ?? and will reduce a step further. Instead of the user assigning the value separately, the ??= checks assigns the default value at once if the given value is null or undefined.

6. Assigning Multiple Values

You can assign multiple values at the same time using destructuring.

> Note: In the case of object destructuring, please make sure that the variable names should be the same as the property name of that object. You can also change the variable name instead of the default property name using an alias, as shown below.

`const { name: firstName, age:myAge } = person;`

7. Assigning only Required Values to Variables from an Array and an Object
And you can also assign just the required values using destructuring as well. Since the elements/properties spread out if you are using destructuring, the values get assigned to left side variables based on positions while dealing with arrays and depending on the name of the keys for objects.

8. Merging Arrays and Adding Multiple Elements to an Array
You can merge two different arrays and also add new elements to an existing one using spread syntax.

9. Spread Syntax with Destructuring
You can also use spread syntax with destructuring for assigning the leftover elements or properties to a new variable altogether.

10. Short-Circuit Evaluation with &&
If you want to execute a function only if a condition evaluates to anything other than falsy values, then you can use short-circuit evaluation with && as shown.

Note: Please note that in JavaScript, the values of null, undefined, ‘’, false, and 0 are falsy, and all the other values are truthy.
11. Template Literals
If you wanted to concatenate variables with static string content, you would use the + operator. And while using the + operator, you would need to manage spaces yourself.
You can achieve the same thing in a much simpler way using template literals.

You can use the same for multiline strings as well.

12. Alternative for a Switch statement
You can use an object with function names associated with a key as an alternative for a switch statement.

13. Object Property Assignment
If an object key should be the same as the variable name, then defining object literals can be done in a much easier way, as shown below.

14. Arrow Functions
If you have a function nested within another function, it can become a bit confusing. So you can make use of arrow functions to write them in a much simpler and shorter way.

15. Implicit return
In an arrow function, if you have just a single statement that you need to return, you can skip the curly braces and the return keyword as well. And you can write it in a much simpler way, as shown below.

16. For Loops
Instead of using the traditional for-loop to iterate over array elements, you can use forEach().

If you want to access just the index values in an array or just the keys in a list of given objects, you can use a for…in loop.

17. Default Values for Function Parameters
Earlier, you used to check if the parameters passed to a function had all the values defined using an if statement and assign them a default value. You can do the same thing in the function declaration itself, as shown.

18. Declaring Variable
It is a good practice to declare and assign variables at the top of your scope. Rather than declaring each of them separately, you can do it in a shorter way to save both time and the number of lines in your code.

19. Adding Object Values into an Array

20. Finding an Element in an Array
Earlier, if you need to find an object in the array by a given condition, you would iterate over that array using a for loop. You can make use of the find() to return the object satisfying the condition.

21. String to Number Conversion
You can convert a string into a number in a much simpler way using the + operator like shown.

22. Multiple Condition Checks
If you need to check multiple conditions in an if statement using the || operator, then you can do that using includes(), as shown below.

23. Swap Variable Values
Instead of using a temporary variable for swapping the values, you can easily do the same using the array destructuring syntax.

24. Exponentiation Operator
When you want to raise the power of a given number, you use the Math.pow(). Instead, you can do the same using the ** in a much easier way.

25. Getting a Character at an Index for a String

26. Mandatory Parameters
If you want to check whether the mandatory parameters are provided or not, instead of using an if condition, you can use a shorter way like shown here.
What we are doing here is assigning the parameter with a default value of an error in case the user does not provide the required parameter

27. Decimal Base Exponents
If a number is long with multiple zeros at the end, then you can write that number in a decimal base exponent format, as shown.

28. Casting to a Boolean using the !!

29. Floor Value of a Number with ~~
You can use ~~ instead of Math.floor() to find the floor value of a number with a decimal point in a much quicker and easy way.
// Longhand
Math.floor(5.25) === 5 //true
//Shorthand
~~5.25 === 5 //true
30. Checking the Presence of an Item in Array
If you are checking if an element is present in an array, you usually use indexOf(). It returns -1 if the item is not there, and if the value returned is anything higher than -1, then the item is available.
A shorthand way of checking is by using the includes(), which returns true if the element is present or false if not found.

Conclusion
These were a list of 30 shorthand techniques that I have found to be very useful. I hope you also find them to be helpful when you use them in your coding.
Thanks for reading, and Happy learning!