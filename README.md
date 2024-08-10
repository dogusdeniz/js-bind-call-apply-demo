# JS Bind, Call, Apply Demo

This project is an interactive demonstration of the differences between JavaScript's `bind`, `call`, and `apply` methods. Each section includes examples of how these methods work and where they might fail, complete with buttons to run the code and see the results in real-time.

## Table of Contents

- [Overview](#overview)
- [Getting Started](#getting-started)
- [Examples](#examples)
  - [bind](#bind)
  - [call](#call)
  - [apply](#apply)
- [Contributing](#contributing)
- [License](#license)

## Overview

JavaScript provides three powerful methods for function manipulation: `bind`, `call`, and `apply`. This project is designed to help developers understand the differences between these methods through clear examples and real-time execution.

## Demo
[View Live Demo](https://dogusdeniz.github.io/js-bind-call-apply-demo/)

## Getting Started

To run this project locally, follow these steps:

1. Clone the repository:

    ```bash
    git clone https://github.com/dogusdeniz/js-bind-call-apply-demo.git
    ```

2. Open the `index.html` file in your preferred browser.

3. Click the buttons next to each example to see how the code behaves.

## Examples

### Bind

`bind` creates a new function that, when called, has its `this` keyword set to the provided value.

#### Example

```javascript
// bind example code will go here
function greet(greeting) {
    return greeting + ", " + "John" + " " + this.surname;
}

const greet1 = greet.bind({surname: "Doe"}, "Hello");
console.log(greet1());  // "Hello, John Doe"
```


### Call

The `call` example is used to invoke a function on a specific object.

#### Example

```javascript
// call example code will go here
function greet(greeting) {
    return greeting + ", " + "John" + " " + this.surname;
}

const user = { surname: "Jane" };
console.log(greet.call(user, "Hello"));  // "Hello, John Doe"
```


### Apply

The `apply` example is used to invoke a function on a specific object and takes arguments as an array.

#### Example

```javascript
// apply example code will go here
function greet(greeting, ending) {
    return greeting + ", " + "John" + " " + this.surname + " " + ending;
}

console.log(greet.apply({ surname: "Doe" }, ["Hello", "goodbye"]));  // "Hello, John Doe goodbye"
```
