---
title: Introduction to HTML
keywords: sample
tags: HTML and CSS
sidebar: html-css
permalink: html-css/intro-html.html
folder: html-css
---

## Introduction

Throughout this course, we will look at HTML in more detail and learn exactly how to use it when creating a website.

A few notes about HTML:

- HTML stands for HyperText Markup Language.
- Any website you visit has been created with the use of HTML.
- Every webpage is an HTML file.
- It is the backbone of website creation and therefore a relatively easy concept to learn.
- HTML is made up of short codes typed into a text-file by the creator of a site. These codes are known as tags.
- When the text is saved as an HTML file and opened by a browser, such as Google Chrome, the browser translates the text into the webpage that was intended to be created.

## Code Editors

Because HTML is written as text, a program as simple as Notepad (PC) or TextEdit (Mac) can be used. Yet, these have very limited functionality. They don’t offer things such as syntax highlighting and error spotting in your code.

We recommend using VS Code as your code editor. It is a popular choice for front-end developers. We also suggest plugins such as Prettier, which automatically formats your code for you and Live Server which allows you to code on one screen and have the browser automatically update on another screen as you work.

Other code editors include Atom, Brackets and Sublime.

If you already have a code editor you prefer, you’re welcome to use that.

_Tip: Try using a dark theme with less contrast. This can be less tiring on your eyes than a white theme. This is personal preference though, so try different options to see what works best for you._

## A Basic HTML page

Here is a basic HTML page. We will be going through the page looking at each element separately. Click through the tabs below to view descriptions of each element.

### Doctype Declaration

`<!doctype html>` is known as a doctype declaration and is necessary at the top of each HTML page. The declaration lets the browser know to interpret the page as HTML.

### Head

The head of the document is used to contain metadata about the page, but is not displayed on the page like the data inside the body. The metadata defined in the head might include: the page title, descriptions of the page, styles, scripts, viewports, links, and more.

### Title

The title tag sets the title of the document. You can see the title displayed on the browser tab. It is also the title that is displayed on search engines, and so it is important to pick clear, unique titles for each page. On most websites, the title will contain the site name as well as the page name. For example, "Business Name | Contact Us"

### Meta Tags

Meta tags are used to add extra information about the page.

Here are two important meta tags:

- **Meta Description**

The meta description of the page is vital for search engines as this text is displayed on a results page under the page's title. It should be enticing and be unique for each page on the website.

- **Meta Viewport**

The visible area of a page (or viewport) varies a lot across devices, and so the meta viewport tag `<meta name="viewport" content="width=device-width, initial-scale=1">` provides a way to tell the browser how to control the page's dimensions. Adding the meta viewport tag to your HTML document is very important for creating websites that look good across devices.

### Body

Everything visible on the page should go inside the body tag. The head is for all the extra information and styling for the page. HTML content that will be displayed on the page must be inside the body. It is important to notice how elements are nested inside other tags in HTML. This is a fundamental concept of HTML. For example, a div tag is nested inside the body tag which is nested inside an HTML tag.

Note below how nested elements are indented. This makes the code easier to read.

### Header

The header of a page contains an introduction to the page. It might typically contain the logo, a heading and/or introduction to the page, the main navigation for the site, as well as a header image. It's important to point out the difference between `<head>` and `<header>`.

- The `<head>` is used for extra information about the document.
- The `<header>` is the introduction to the page.

### Nav

The nav element should contain your main navigation for the website. On most websites you'll likely have one nav element, while links in the footer do not need to be in a nav element. If you have navigation to allow moving between pages, as well as moving around on that page, you might want to use the aria-labelledby attribute, which is your primary navigation as you can see in [this example on MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements).

### UL and LI

In the code above there is a `<ul>` element inside the nav element – this is an abbreviation of unordered list. We use it in this context because there is a list of links inside the navigation element. Each item inside the `<ul>` is a list item or `<li>`. By default, a `<ul>` displays as a bullet point list, but with CSS this can be adjusted.

Another type of list you might see is an `<ol>` or Ordered List. This is a list where the order matters and by default it is numbered.

### Main

The `<main>` element is used to group the primary content that this page is about. While the header introduces what the page is about, the main element is used for the actual content. This content should be unique to that page, so elements which are repeated across different pages, such as nav links etc. should be kept outside of this element.

### Section and Div

The `<section>` element is used to identify specific sections of content, and should be used if a more appropriate element can't be found. It will often have a heading in the section.

If you need a generic container and there is no meaningful reason for adding the element other than it gives you something to style, then the best element for that is the `<div>`. In general, try find a semantic element. If there isn't one, you can use a `<div>`. Before HTML5, developers used `<div>` a lot, but now we have more meaningful tags and they should be used where appropriate.

### Headings

Headings are essentially titles for pages or sections on the page. Headings run from `<h1>` to `<h6>` and should be used in order of importance. Thus, `<h1>` is the most important heading on the page, then `<h2>` the second most important heading or headings, then `<h3>` the third most important and so on.

There should just be one h1 per page and it should be unique for that page. You should also not skip headings (i.e. jump from h1 to h3 with no h2 on the page).

### Paragraphs

Paragraphs, indicated with `<p>` tags, are blocks of text, usually a group of sentences with no line break. If you want to break up a paragraph, do not use `<br>` tags. Rather, close the paragraph and open another paragraph.

### Footer

You can use the `<footer>` element to include additional information about the page. Typically, it will include copyright information and additional links which users might find useful. It's generally not very important information, and is therefore typically displayed right at the bottom of the page.

## Semantics

In HTML, semantics refers to the meaning of a piece of code. Does the HTML code have meaning? The reason we'd like our HTML to be meaningful is that it makes the code easier to read, which is important for yourself as well as other developers.

Meaningful code also makes it more accessible. With good semantics, an assistive technology can more easily make sense of the different elements on the page and their usage. The same logic applies for search engines. If every element on the page is a `<div>` then all elements are seen as equal. It's much better to use meaningful tags to identify what each section is about.

## Good Formatting

Correctly formatting your code makes it much easier to read, and it thus becomes quicker to identify which elements are nested inside of other elements.

To practice good formatting of your HTML here are key points:

- Elements placed inside other elements should be indented to the right of the parent. For example, the body element is inside the html element and so should be indented to the right of its parent.
- The opening tag and closing tag should be indented the same amount.
- Elements such as headings, paragraphs and images can be placed on one line. The example above is much more difficult to read than the example below, where indenting is used, making it quicker to scan through the code. You can use tab to indent, and most text editors will help you indent correctly. You can use plugins such as [Prettier](https://prettier.io/) to format your code for you.

<hr>

## Activities

**WATCH**

[This tutorial video on laying out a basic HTML page.](https://scrimba.com/scrim/cBL7gDUv?pl=paaBbTa) (15m 39s)

<hr>

## Lesson Task

### Brief

There are practice questions in the master branch of [this repo](https://github.com/Noroff-Education/lesson-task-htmlcss-module1-lesson1).

Attempt the answers before checking them against the answers in the [answers branch](https://github.com/Noroff-Education/lesson-task-htmlcss-module1-lesson1/tree/answers) of the repo.
