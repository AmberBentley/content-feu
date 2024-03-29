---
title: Fonts
keywords: sample
tags: HTML and CSS
sidebar: html-css
permalink: html-css/fonts.html
folder: html-css
---

## Introduction

Most websites rely on text to communicate with their users. It is therefore important to use strong fonts that you’re confident will load correctly.

By default, browsers apply <i>Times New Roman</i> to text on the web. You should avoid using Times New Roman. It has been overused and makes it seem like your font hasn't loaded correctly. It is always advisable to set a base font on the body or html element, so that all text across the site will be styled.

## Font-family

To set a font, we need to use the property `font-family` like so:

The CSS written above is applying the font, Verdana, to all paragraphs on the page, but if the browser doesn't have the first-choice of Verdana (maybe the user deleted the font file from their computer) the browser will display whatever the default sans-serif font is. You should always include a generic family name (serif, sans-serif, monospace, cursive).

You can have multiple fallbacks when applying a font like so:

In this case, we are asking the browser to load "Open Sans" (note the quotation marks because it's two words), but if you don't have "Open Sans" try Tahoma. If you don't have Tahoma you can try Verdana, and finally just load the generic sans-serif for the browser.

### Web Safe Fonts

Verdana is considered a web safe font. A web safe font is a font that is installed on (almost) every device, and using it will mean that you can be very sure that a user will have that font.

Web safe fonts include: Arial, Verdana, Tahoma, Georgia, and Times New Roman. You can use [CSS Font Stack](https://www.cssfontstack.com/) to see how widely available a specific font is.

## Loading Fonts to the Browser

You will probably have recognised most of the fonts mentioned under Web Safe Fonts, because they are popular on the web and therefore well-used. In most cases it's better for your design if you don't have overused fonts on your website, and are able to use a font better-suited to the specific brand for which you are developing.

To make sure our font works on a user's computer, we need to load the font to the browser. Click on the two tabs below for more information.

### @font-face

We use the @font-face rule to load a font to the browser. The font file can be local to the stylesheet from which it is being called, or it can be on another server.

The important things to get right are:

- following the syntax
- ensuring the file path is correct
- setting the font before you use it

Thus, it is always a good idea to have the @font-face rule at the top of your stylesheet.

We use the `font-family` property to set the font's name (note that this isn't applying the font to any elements, it's simply setting the name of the font which we can use). Secondly, we set the `src` to link to the font file and say what format the font file is.

### Google fonts and external stylesheets

We can also load fonts to the browser using stylesheets which have pre-written @font-face rules for us to use. Google Fonts is a popular resource for fonts and they give us the stylesheet we can link to from our HTML files in order to load the font to the browser.

![Google Fonts](../../images/htmlcss/1-4-1.jpg)

It is very important when adding these external stylesheets in your HTML, that you place them above your own stylesheet. Otherwise you will reference a font in your stylesheet before the browser has loaded the font.

## Font-sizes

Font sizes are managed using the `font-size` property. By default, your browser sets font-sizes on headings to run in order; h1 has the largest font-size, h2 the second largest and so on.

### Px

- `px` sets an absolute font-size and this size will stay exactly that pixel size regardless of screen size or other changes.
- It was a popular way of setting font-sizes, but it isn't very inclusive because user's with bad eyesight couldn't easily adjust the font-size using their assistive technology.

### Em

- `em` is a dynamic way of setting font-sizes and it adjusts based on the pixel size of the element it's used on.
- By default, your browser uses 16px for a font-size, and so 1em = 16px.
- The code above sets the h2 to be 2em, which by default would be 32px. You can also have integers, so 0.5em would be 8px.
- What is especially useful about `em`s is that if a user needed the text to be larger, they could change the default size of their browser's text and all font-sizes would adjust.

### Compounding

- One issue with `em`s is that they are relative to their parent element, but if you have the same parent element used twice then it can double up.
- As you can see above, a span is nested inside another span. If we set the span to be 1.5em (and the browser default for the font was 16px), then the outer span would be 24px (16px x 1.5em). The inner span would then be calculated based on the parent element being 24px, and so the inner span would be 36px (24px x 1.5em).

### Rem

- To get around the issue of compounding, `rem` sizes were invented.
- `rem` is calculated based on the `<html>` element and not the parent element.
- Using this above code would mean both the outer and nested span element would be set to be 24px.

<hr>

## Activities

**WATCH**

[This tutorial video on the @font-face rule.](https://scrimba.com/scrim/cNq6q8hq?pl=paaBbTa) (4m)

<hr>

## Lesson Task

### Brief

There are practice questions in the master branch of [this repo](https://github.com/Noroff-Education/lesson-task-htmlcss-module1-lesson4).

Attempt the answers before checking them against the answers in the [answers branch](https://github.com/Noroff-Education/lesson-task-htmlcss-module1-lesson4/tree/answers) of the repo.
