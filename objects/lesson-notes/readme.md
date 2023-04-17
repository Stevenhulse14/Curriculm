# Objects

## Learning Objectives

By the end of this lesson, you should be able to:

- Define what an object is and describe its properties
- Create an object with the object literal syntax.
- Access values in an object through bracket and dot notation.
- Update values in an object with bracket and dot notation.
- Add key-value pairs to an object with bracket and dot notation.
- Loop over an object.
- Differentiate between arrays and objects.

---

## Guiding Questions

- The following is an object. In as much detail as possible, describe the object. Consider describing specific syntax and terms.

```js
{
  firstName: "Grace",
  lastName: "Hopper"
}
```

- Objects have key-value pairs. Is it possible to have a key without a value or a value without a key in an object?

- What kinds of data types can be stored as values in objects?

- What kinds of data types can be used as keys in objects?

- Brackets can be used to access values in an object. The string you place inside the brackets after the object returns the value at the matching key. Keeping this in mind, what do you think will be logged to the console in the code below?

First, make a guess. Afterward, you can run the code and check your answer.

```js
const programmer = {
  firstName: "Grace",
  lastName: "Hopper",
};
const firstName = programmer["firstName"];
console.log(firstName);
```

- When you access a value in an array, you can perform additional operations on that piece of data. With that in mind, what do you think will be logged from the following code? Make your guess before running the code.

```js
const programmer = {
  firstName: "Grace",
  lastName: "Hopper",
};
const firstName = programmer["firstName"];
console.log(`Hello, ${firstName}!`);
```

- What do you think will be logged to the console in the code below? Mentally evaluate the code and guess by running the code to check your answer.

```js
const programmer = {
  firstName: "Grace",
  lastName: "Hopper",
};
const result = programmer["fullName"];
console.log(result);
```

- You can add key-value pairs to an object with bracket notation by assigning a value to a key that does not currently exist. The code below shows an example of this.

```js
const programmer = {
  firstName: "Grace",
  lastName: "Hopper",
};
programmer["middleName"] = "Brewster";
console.log(programmer);
```

How would you now access this new value?

- You can update existing key-value pairs in the same way. Knowing that, write code that would change the `middleName` key below from `Brewster` to `B.`.

```js
const programmer = {
  firstName: "Grace",
  middleName: "Brewster",
  lastName: "Hopper",
};
// Write your code.
console.log(programmer);
```

- Do objects have the `.length` property? Does the answer to the previous question seem reasonable?

- While bracket notation works for arrays, you can also use a syntax known as dot notation. If the key in an array contains no spaces and does not start with a number, you can access its value with a `.` like in the example below.

```js
const programmer = {
  firstName: "Grace",
  middleName: "Brewster",
  lastName: "Hopper",
};
console.log(programmer.firstName);
```

Take a moment to try out dot notation. Access each value in the object with dot notation and log it to the console.

- You can also assign new key-value pairs to an object with dot notation. Knowing what you know so far, write your code that adds the key `invention` and sets it equal to the value of `"FLOW-MATIC"`.

- You can also update key-value pairs using dot notation. Knowing what you know so far, write your code that updates the key `invention` to the value of `"COBOL"`.

- Write a loop that iterates over the object, and console logs the key and the value pairs.

- Now that you have seen both arrays and objects take a moment to consider the similarities and differences between the two. Consider their syntax, how the information is stored, and how it is organized.

Based on the above, think of an analogy that helps you distinguish between arrays and objects.
