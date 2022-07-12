---
title: Classes
keywords: sample
tags: JavaScript 2
sidebar: javascript-2
permalink: javascript-2/classes.html
folder: javascript-2
---

# Classes

## Intro:

A class is a template for us to create objects, like a blueprint for the shape of the data.

In programming, a class contains properties and methods. Properties are variables inside of a class, and methods are functions inside of a class.

## Basics:

Consider the following class which contains a constructor, a method called `myMethod` and a property called `myInitialValue`:

```js
class MyClass {
  // This is a property in our class
  basicProperty = 'My basic property';
  // This is another property however it isn't initialized to a value
  emptyProperty;
  // The constructor lets us set values when we create an instance of a class
  constructor(myInitialValue) {
    // A property 'myInitialValue' being initialized to an argument
    this.myInitialValue = myInitialValue;
  }

  // A method in the class
  myMethod() {
    console.log(this.myInitialValue);
  }
}

const myClassInstance = new MyClass('Hello world');
myClassInstance.myMethod();
// Logs:
// Hello world
```

### 'new' keyword:

As mentioned, a class is a template of an object. We create a copy of a class, called an "instance", which then has all of the properties and methods from the original class.

We create a new instance of a class by using the `new` keyword.

```js
const myClassInstance = new MyClass('Hello world');
```

We can now call the `myMethod` method from this class:

```js
// Logs "Hello world"
myClassInstance.myMethod();
```

### Constructor:

The constructor in a class allows us to set any initial values that we'd like to set, such as a user's name. These values can be passed in or be static.

In this example we set a value `myInitialValue` that's being passed into the class:

```js
constructor(myInitialValue) {
  this.myInitialValue = myInitialValue;
}
```

**Note:** You do not need to make use of a constructor if you have nothing to initialize.

### Methods:

Methods are functions inside of a class. They are copied when we create a new instance of a class.

We don't use the `function` keyword when creating a method in a class, we simply write the method name:

```js
class MyClass {
  // ... constructor

  // Method called 'myMethod'
  myMethod() {
    console.log(this.myInitialValue);
  }
}

// Create an instance of the class
const myClassInstance = new MyClass();
// Calling the 'myMethod' method
myClassInstance.myMethod();
```

### 'this' keyword:

To access our variables inside of the class, we need to make use of the `this` keyword.

```js
myMethod() {
  console.log(this.myInitialValue);
}
```

### Strict mode:

The code in the body of a class is in "strict mode".

## Practical Example 1: Person object:

Now that we've covered the basics, let's start looking at a more practical example:

The following is a basic example of a class called `User`. It takes in `firstName` and `lastName` parameters, and has a method `greetUser()` which logs a greeting message.

```js
class User {
  language = 'Norwegian';
  constructor(firstName, lastName) {
    // Set 'firstName' to the 'firstName' parameter
    this.firstName = firstName;
    // Set 'lastName' to the 'lastName' parameter
    this.lastName = lastName;
  }

  // 'greetUser' method that logs a greeting message
  greetUser() {
    console.log(
      `Hello ${this.firstName} ${this.lastName}! Language: ${this.language}`,
    );
  }
}

const newUser = new User('Old', 'Nordmann');
// Logs "Hello Ola Nordmann! Language: Norwegian"
newUser.greetUser();
```

## Practical Example 2: Shopping Cart

We are going to have a look at a more complex implementation of a class.

In this example, we are going to create a Shopping Cart.

This class has: [INCOMPLETE]

```js
class ShoppingCart {
  cart = [];

  constructor(shopName, currency) {
    this.shopName = shopName;
    this.currency = currency;
  }

  /** Adds the item to the cart **/
  addToCart(item) {
    this.cart.push(item);
  }

  /** Removes the item from the cart **/
  removeFromCart(item) {
    const idToFind = item.id;
    // Find the index to remove
    const indexToRemove = this.cart.findIndex(
      (currentItem) => currentItem.id === idToFind,
    );
    // If the index is -1 then it means no item was found, so
    //    we return null to break out of the function
    if (indexToRemove === -1) {
      return null;
    }
    // Filter the items and remove the item that matches our index
    const newCart = this.cart.filter((item, index) => index !== indexToRemove);
    // Set the cart to cart without the item by spreading out the array
    this.cart = [...newCart];
  }

  /** Calculates the total cost of items in the cart **/
  calculateTotalCost() {
    const totalCost = this.cart.reduce((total, item) => {
      total += item.price;
      return total;
    }, 0);
    return totalCost;
  }

  /** Displays the items in the cart **/
  displayCart() {
    console.log('Your cart:');
    console.log('-------------------');
    this.cart.forEach((item) => {
      console.log(item.title);
    });
    console.log('===================');
  }

  /** Displays the total cost of the items in the cart **/
  displayTotalCost() {
    console.log('Total items: ', this.cart.length);
    console.log('The total of the cart is:', this.calculateTotalCost());
  }
}

const myCart = new ShoppingCart('Norway Bakery', 'USD');

const cookies = { id: 23, title: 'Chocolate Chip Cookies', price: 20.0 };
const cake = { id: 45, title: 'Vanilla Cake', price: 30.0 };

myCart.addToCart(cookies); // Add an item
myCart.addToCart(cookies); // Add an item
myCart.addToCart(cake); // Add an item
myCart.displayCart(); // Display the cart
myCart.removeFromCart(cookies); // Remove an item
myCart.displayCart(); // Display the cart
myCart.displayTotalCost(); // Display total cost of the cart
```

## Video:

In this video we look at classes and how they work:

[Vimeo video: Classes - Basics: https://vimeo.com/672258591/4182086e2c]

# Classes (cont.):

## Static Methods and properties:

Static methods and properties allow us to create methods and properties that are attached to the main class itself instead of the instance of a class. Therefore these static methods and properties cannot be accessed by the instance of a class.

```js
class User {
  constructor(name) {
    this.name = name;
  }

  // This method is available to all instances of a class
  greetUser() {
    console.log(`Hello ${this.name}!`);
  }

  static company = 'Acme';

  // This method is available only on the User class itself
  static displayTime() {
    console.log('12:00');
  }
}

const newUser = new User('Ola Nordmann');

// This is called on the new instance of the class
newUser.greetUser();
// Logs:
// Hello Ola Nordmann

// The static property 'company' is only available on the class itself
console.log(User.company);
// Logs:
// Acme

// The static method 'displayTime()' is only available on the class itself
User.displayTime();
// Logs:
// 12:00
```

## Extending a class:

We can create that inherits from another class so that it acts as a child class.

```js
class Animal {
  constructor(name) {
    this.name = name;
  }
  speak() {
    console.log(`${this.name} makes a sound`);
  }
}

class Cat extends Animal {
  //
  constructor(name) {
    super(name);
  }

  speak() {
    console.log(`${this.name} goes meow`);
  }
}

const sheep = new Animal('Lambert');
sheep.speak();
// Logs:
// Lambert makes a sound

const cat = new Cat('Pookie');
cat.speak();
// Logs:
// Pookie goes meow
```

## Getters and Setters:

We can use getters and setters to make our code a bit more intuitive to work with.

If we had a `name` property that we wanted to change in our class, we would have to have a function like `setName`. We would also have to do the same for getting a name, e.g. `getName`.

We can instead use getters and setters to get and set a value.

Note: We have to use a different variable name in the setter (`set name`), otherwise we will end up with a recursive call.

```js
class Person {
  constructor(name) {
    this.name = name;
  }

  get name() {
    return this._name;
  }

  set name(newName) {
    this._name = newName;
  }
}

const newPerson = new Person('Ola Nordmann');

console.log(newPerson.name);
```

## Classes video:

In this video we look at static methods/properties, extending a class and getters/setters.

[Vimeo link: Classes - Continued: https://vimeo.com/672260345/5ee4300446]

---

Resources:

[MDN: Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

[Javascript.info: Class](https://javascript.info/class)
