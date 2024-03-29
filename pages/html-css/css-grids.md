---
title: CSS Grids
keywords: sample
tags: HTML and CSS
sidebar: html-css
permalink: html-css/css-grids.html
folder: html-css
---

## Introduction

While Flexbox works one-dimensionally, either vertically or horizontally, CSS Grids can work two-dimensionally at the same time. This allows you to create more advanced layouts using the single system.

CSS Grids is so-named because it's based on the idea of a grid running horizontally and vertically across and down the screen. We can use CSS Grids to determine how many horizontal and vertical spaces in the grid each element should take up.

## Important Concepts

### Grid Container

- To get started using CSS Grids, you need to create what is called the Grid Container.
- To do this, set `display: grid` on a parent element.
- This will allow you to use CSS Grids to create rows and columns inside of that element.

### Grid Item

- A grid item is one of the direct child elements to the Grid Container.
- These are the items that will take up space in our grids.

### Grid Gap

- The Grid Gap refers to the space between columns and rows in the grid.

### Grid-template-columns and rows

- To control the size of rows or columns you use `grid-template-columns` and `grid-template-rows`.
- The CSS above creates a grid container with two columns. The first column is set to `auto` and takes up as much space as it requires on the page. The second column is set to `1fr` and takes up the remaining available space left over.
- The grid container also has two rows. The first is set to 1fr meaning it takes up whatever space is left, the second is set to auto so only takes up the space it needs. It’s important to see the min-height which allows us to see the row heights.

### Grid-template-areas

- One of the nicest aspects of CSS Grids is the ability to create grid areas. Especially useful is that the syntax (how the CSS is written) is how it will appear on the page.
- If you had a header, nav, main, footer in your HTML, you could set these areas as a grid-area.
- Note the property `grid-area` is used to create the area, and the value `myheader` etc. is decided by the developer.
- With the `grid-area`s defined, we can use `grid-template-area`s to arrange our content into rows and columns.

<hr>

## Activities

### Activity 1

**WATCH**

[This tutorial video on CSS grids.](https://scrimba.com/scrim/cWvWwNcP?pl=paaBbTa) (8m 38s)

### Activity 2

**READ**

[A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/) by CSS Tricks, use this as a reference guide. You might find it difficult to read it all in one go, so read a bit and then experiment and come back to it.

### Activity 3

**WATCH**

Video: Build a Classic Layout FAST in CSS Grid (8m 29s)

<iframe width="560" height="315" src="https://www.youtube.com/embed/KOvGeFUHAC0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<hr>

## Lesson Task

### Brief

There are practice questions in the master branch of [this repo](https://github.com/Noroff-Education/lesson-task-htmlcss-module3-lesson3).

Attempt the answers before checking them against the answers in the [answers branch](https://github.com/Noroff-Education/lesson-task-htmlcss-module3-lesson3/tree/answers) of the repo.
