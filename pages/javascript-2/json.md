---
title: JSON
keywords: sample
tags: JavaScript 2
sidebar: javascript-2
permalink: javascript-2/json.html
folder: javascript-2
---

# JSON

JSON stands for JavaScript Object Notation.

JSON is a way for us to easily convert our JavaScript data back and forth so

It is a way for us to store JavaScript data in a purely text format so that it can easily be shared, such as between applications or outside of a JavaScript environment.

The principle behind it is very simple:

1. We convert our JavaScript data to JSON

```js
const person = {
  name: 'Ola Nordmann',
  id: 9,
  isAdmin: true,
};
```

```json
{
  "name": "Ola Nordmann",
  "id": 9,
  "isAdmin": true
}
```

Two are two main parts to JSON.

1. Convert to JSON (`JSON.stringify`):

We convert our JavaScript data to JSON.

We Converting our JavaScript data to JSON:

We convert out JavaScript data to the JSON text format so i 2. Converting JSON back to JavaScript.

When we need to send our JavaScript

Convert to JSON (`parse`)

JSON Website: https://www.json.org/
