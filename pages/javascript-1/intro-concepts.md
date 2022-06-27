---
title: Introductory Concepts
keywords: sample
tags: JavaScript 1
sidebar: javascript-1
permalink: javascript-1/intro-concepts.html
folder: javascript-1
---

## Introduction

In this lesson we look at some concepts we will use throughout our JavaScript studies.

The topics we will cover are:

- Using the browser console
- ES6
- Declaring variables with the const and let keywords
- Creating strings with backticks
- Accessing object properties using brackets
- Functions as properties of objects.

## The browser console

The browser console is one of your most essential tools when writing JavaScript.

It is a good idea to keep it always open to view variables that you log and any errors that you may encounter.

We suggest using either Firefox or Chrome when developing with JavaScript.

In the video below, we'll look at logging variable values using the console.

 <div style="padding:42.19% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/443132927?h=bb68f831f5&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Console Commands"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

[Vimeo link](https://vimeo.com/443132927/bb68f831f5) for the above video.

## ES6

ECMAScript (ES) is the official specification for JavaScript. It decides what features should be in the language.

ES6, or ES2015, was released in 2015 and introduced many improvements to the language after a long gap in updates to the specification. New features are now continuously being added.

ES6 is often, somewhat confusingly, used to refer to the modern versions of JavaScript.

You can check the browser support for a feature (JavaScript and CSS) by using caniuse.com

### const and let

ES6 introduced the const and let keywords for declaring variables.

A key difference between const and let is that let can have its value reassigned, whereas const cannot.

If we declare a variable using const and assign it a value:

```js
const count = 1;
```

We cannot give it a different value. We cannot now do this, for example:

```js
count = 2;
```

There are more details on const and let in the Scrimba below.

The cast begins with a brief look at the undefined value.

LINK

Scrimba for the above video.

Strings using backticks

Previously, we've seen that we can create strings using double or single quotes, and that you should pick one and use it consistently (for any Noroff code use double quotes).

There is another way to create strings - with backticks, which is this character: `.

Using backticks:

    Provides an easy way to split strings across lines.

    Provides a cleaner way to embed variables in strings.

On many keyboards the key is situated top left.

LINKS

Vimeo for the above video.  
Code from the video.

Accessing object properties using brackets

Previously we have accessed object properties using dot notation – using a full stop.

We can also access object properties using square brackets [], with the key of the property as the value inside the brackets:

```js
const pet = { type: "dog" };
console.log(pet["type"]);
```

The Scrimba below explores this further.

LINK

Scrimba for the above video.

Functions inside objects

We've previously seen objects with properties having string, number, or Boolean values.

Objects can also have functions as properties. These are often called methods.

LINK

Scrimba for the above video.

Imports/exports

We can split our code up into files using modules.

To import code from another file, we need to export it first.

There are two kinds of exports:

    Named exports

    Default exports.

Named exports

Named exports are exported with the export keyword and imported using their name between braces.

One file can contain many named exports.

You can alias a named export using the as keyword.

Default exports

Default exports are exported with the export default keywords and imported without braces.

When you import a default export, you can import it using any name, the name you use in the import is just an alias.

Navigating directories

    Go up a folder
    ../ - go back (or up) one directory (folder) from the current directory.
    You can use several of these, the below will go back three folders:
    ../../../

    Look in the current folder
    ./ - look in the current folder for the path

Using imports and exports

The following video looks at using imports and exports.

LINK

Vimeo for the above video.

Import/export example

The following video converts a small existing project to use modules, splitting the code up using imports and exports.

LINKS

Vimeo for the above video.  
Code from the video.

Activity

WATCH

Video: ECMAScript, TC39, and the History of JavaScript (11m 32s)

Lesson Task - Introductory concepts

Lesson Task

Brief

There are practise questions in the master branch of this repo.

Attempt to answer the questions before checking them against the answers in the script.js file in the answer branch of the repo.
