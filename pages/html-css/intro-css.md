---
title: Introduction to CSS
keywords: sample
tags: HTML and CSS
sidebar: html-css
permalink: html-css/intro-css.html
folder: html-css
---
## Introduction
While HTML is used for creating the content of web pages, CSS is used to style web pages. One of the most compelling demonstrations of this is a website called [CSS Zen Garden](http://www.csszengarden.com/). On this site you may apply different CSS styles to fixed HTML content. It is impressive how the entire layout and look of the page can transformed by changing the CSS applied to HTML content (the HTML stays exactly the same). 

## Create stylesheet and link to HTML

To begin adding styles to our HTML pages, we need to create a .css file and link it to our HTML files. To connect a .css file to a .html file we use the `<link>` tag in our HTML file. The tag we'd use looks like this:  
`<link href="css/styles.css" rel="stylesheet">`

The `href` is used to tell the browser where to look for the stylesheet. In this case, look inside the 'css' folder for a file called 'styles.css'. 

We've created a simple example of linking a CSS file to an HTML file in [this repo on GitHub](https://github.com/NoroffFEU/html-css-module1-lesson3).

If you clone the repo to your computer, you will see an index.html file in the root folder, and a styles.css file inside the 'css' folder. If you open the index.html file in your browser, you will see the background has been turned orange by a style set in the CSS.

## The Basic Syntax

To style elements you need to use a specific syntax.

Here is an example:

- First, we state which element(s) we want to style using a selector. In this case the `h1`.
- Then we use curly braces to group styles together that we're applying to that selector. In this case we're setting the font size to be 20px and the color to be green. 
- After we've written each style rule, we close the line with a semi-colon so the browser knows we've finished that rule.

## Selectors

Selectors are used to identify which element on the page we're wanting to style.

### Tag

The tag selector, also called the element selector, is simply a way to select the HTML element using its HTML tag. It's generally best to use a tag selector if there's something specific about that HTML element you want to change. By default, the browser applies certain styles to your HTML, which might be useful or not depending on your design. For example, by default, an anchor tag (`<a>`) is styled blue and underlined. To change this, we could select all anchor tags using the following selector.

The following styling changes the text color and removes the underline.

### Class

Generally, the best way to style elements is using a class. Classes can be applied to multiple elements across the page which helps you reduce the amount of CSS you need to write. You can add classes to HTML elements using the `class` attribute like so:

We can then style the classes we've added to the HTML by referencing them in our CSS file by using a dot followed by the class name:

In the example above, we applied the `content` class to two sections, and added a unique class called `highlighted` to the second section. This illustrates how you can combine classes on your elements. 

Naming classes clearly is very important. Giving an introductory paragraph in a header the class of `intro` is much more meaningful than `p1`. Remember that other developers will usually need to read and understand your code, so make it as clear as possible.

### ID

IDs can be used only on one element on each HTML page, and it overrides styling applied by classes or tag selectors. Generally, IDs are best used with JavaScript where we want to be able to override styles applied by CSS easily.

Here is how you would apply an ID to an element in HTML, and then to style it in CSS you you'd use # followed by the ID name.

## Combining Selectors

You can combine selectors together.

Take a look at the following HTML:

To set the font-family of the headings, we could possibly select them individually like so:

However, this is repetitive.

In CSS we try to follow what is called the DRY Principle (Don't Repeat Yourself). This is key to writing good CSS, and helps us to write CSS that is as succinct as possible. Therefore, instead of writing them twice, we can use a comma to combine the styles together:

Let's say we wanted to style all `<li>` elements in the navigation to be in a row. We couldn't use `li {display: inline-block;}` because this would also affect the list items in the `<main>`. What we could do is use what is called a descendant combinator, like so: `nav li {}`

This targets every list item that is a child of a nav element.

Let's also remove the padding to the `<ul>` that the browser automatically applies, and set the anchor tags in the navigation to be black with no underline. We can do this all using the descendant combinator as we did above.

Now let's say we wanted to style all elements with the class of sale to be red, we could simply target the class: `.sale {}`

This would be applied to the link in the navigation as well as the span in the main, but what if I wanted the link in the main to have an underline. I've already removed all underlined links in the nav using `nav a`. To specifically target the link in the nav with class of 'sale', we can do the following: `a.sale {}`

This targets each anchor tag that has the class 'sale'. It's important to note that there is no space between `a` and `.sale`. If there were a space, it would select every anchor tag that had a child element with the class `.sale` which in this case wouldn't apply to any elements. 

Another combinator we can use is called the adjacent sibling combinator which selects elements which are next to each other in the HTML. To increase the font size of each paragraph that follows an h2, we could use the following: `h2 + p {}`

This styling would only be applied to paragraphs that are siblings (ie. they share the same parent element).

### Pseudo-classes

We can also apply styling by using what is called pseudo-classes, which allow us to use keywords to target elements based on their state. A good example is when a user hovers over an element. Let's say we wanted the navigation links to change when a user hovers over it. We could use the following code (notice the colon between `a` and the keyword `hover): nav a:hover {}`

Other pseudo-classes include `:active` for when a user is busy interacting with the element, for example clicking a button. Another is `:first-child` which targets the first child element inside the chosen parent. 

**READ**

Article: [Psuedo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

### Pseudo-elements

A pseudo-element allows you to style a specific part of the element you've selected. Let's say you wanted to style the first letter of a paragraph. You could use the `::first-letter` pseudo-element.

Other pseudo-elements that are useful to know are `::before` and `::after` which let you style the section before or after a specific element. With CSS you can use the content property to add `content` to the HTML. In this example we are adding a calendar icon in front of the date.

We could add the icon in the HTML in front of the date, but the question we should ask is whether the icon is important content that should be in the HTML for someone using an assistive technology, or if it is purely styling. If it's just for styling then it's best managed using CSS. Plus, we'd be able to quickly change all calendar icons in one place if we wanted a different icon at a later date.

## Cheat sheet of Selectors and Combinators

Example	What is selected
`section {}`	`section` elements
`.highlighted {}`	Elements with a class of `highlighted`
`#logo {}`	Elements with an ID of `logo`
`section.highlighted {}`	`section` elements with a class of `highlighted`
`section .highlighted {}`	Elements with a class of `highlighted` inside of `section` elements
`section > .highlighted {}`	Elements with a class of `highlighted` that are direct descendants of a `section`
`section + .highlighted {}`	The first element with a class of `highlighted` after each `section`
`section, .highlighted {}`	All `section` elements, and all elements with a class of `highlighted`
`section ~ .highlighted {}`	All elements with a class of `highlighted` that are siblings of a `section`
`input[type="text"] {}`	`input` elements that have a type of `text`

## Cascading, Specificity and Inheritance

- CSS stands for Cascading Style Sheets. 
- Cascading is the order in which we write CSS, going from top to bottom.

In the following example, two conflicting rules are applied, but which styling should the browser apply? Since CSS runs from top to bottom, it cascades. Thus, the browser will choose the styling applied last and make the background blue. 

### Specificity

In the above example we have two selectors that have the same level of specificity. They're both targeting the `<body>`. But what if we want the `<main>` to be styled a different colour to the rest of the body? In this example, the `<body>` will be orange and the `<main>` will be blue as the main is more specific than its parent element, the body.

In the order of specificity:

- A tag selector is the least specific.
- Then a class as it can be applied to multiple elements. 
- Then an ID as it can only be applied to one element. 

The more specific selector will be the one that gets chosen. Inline styling in the HTML is the most specific you can get, but this shouldn't be added into the HTML and should only be added using JavaScript, which we will get to in the JavaScript course.

We can actually calculate the specificity of a CSS selector numerically. The values of each CSS selector are as follows:

```
Inline style: 1000
ID: 100 Class, attribute, pseudo-class: 10
Type Selector: 1
```

## Activities

**WATCH**

[This tutorial video on CSS.](https://scrimba.com/scrim/cPJpJWCq?pl=paaBbTa) (12m 20s)

## Lesson Task

### Brief

There are practice questions in the master branch of [this repo](https://github.com/Noroff-Education/lesson-task-htmlcss-module1-lesson3).

Attempt the answers before checking them against the answers in the [answers branch](https://github.com/Noroff-Education/lesson-task-htmlcss-module1-lesson3/tree/answers) of the repo.
