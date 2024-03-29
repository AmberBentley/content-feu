---
title: Navigation
keywords: sample
tags: HTML and CSS
sidebar: html-css
permalink: html-css/navigation.html
folder: html-css
---

## Introduction

It is crucial to grasp website navigation by a user.

Here are a few suggestions in terms of setting up your navigation:

- Don't re-invent the wheel. Users generally expect the navigation to be at the top of the screen on desktop, and a hamburger menu on mobile. The only real exception is a dashboard, where the navigation is usually on the left side.
- Add a class to the menu item of the page the user is on. So, if they're on the About page, highlight 'About' in the navigation in some way so that they know on which page they are. On each page, you'll need to change which item to which the class is applied.
- The navigation should be consistent across pages, so always have the navigation there for users to move between pages.

## Nav Element

You should hopefully be familiar with the idea of semantics and wanting to choose the most semantic option you can. The main way to navigate the website should be in a nav element so that it's easy for assistive technology to know which is the primary way of moving about the website.

It is debatable, but the most common way of creating navigation is using an unordered list (`<ul>`).

We have also added common styling in the CSS:

- By default, the browser indents the `<ul>` so we remove that by setting the padding to 0px.
- Next, to display the list items in a horizontal line, we use `display: inline`.
- If we want to add padding to each of the navigation items, it's best to do this on the anchor tag. The reason is that you don't end up with a situation where the user thinks they should be able to click a link, but the link is applied only on the text.
- Lastly, we style the current class to bold so that it's easy to spot.

## CSS-only Hamburger Menu

Usually you need JavaScript to create a hamburger menu. But it is possible to make a hamburger menu using just CSS. You need to use what is commonly called the 'checkbox hack'.

The basis of the method is to have a checkbox which can get checked and unchecked. We can add CSS which applies if the element gets checked and unchecked.

Below is a video explaining how to create a hamburger menu using only CSS.

<hr>

## Activities

**WATCH**

This tutorial video on building a responsive navigation. (11m 42s)

<iframe src="https://player.vimeo.com/video/662883528?h=a4cae2c618&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="1914" height="1036" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen title="Responsive Navigation"></iframe>

<hr>

## Lesson Task

### Brief

There are practice questions in the master branch of [this repo](https://github.com/Noroff-Education/lesson-task-htmlcss-module2-lesson3).

Attempt the answers before checking them against the answers in the [answers branch](https://github.com/Noroff-Education/lesson-task-htmlcss-module2-lesson3/tree/answers) of the repo.
