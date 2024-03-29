---
title: Images and Icons
keywords: sample
tags: HTML and CSS
sidebar: html-css
permalink: html-css/images-icons.html
folder: html-css
---

## Introduction

There are two ways of adding images to the page:

- You can add an image into the HTML document using the `<img>` tag
- Or you can add the image as a background-image using CSS.

Choosing which option is right for the image you want to add is largely one of semantics, as well as the practicalities of the layout you have chosen.

In general, if the image you're looking to add is there to make the site look good, then adding it using CSS is best. If the image is there for content reasons and it would be useful for someone using assistive technologies or a search engine to know that this image is in the content of the page, then use the `<img>` tag.

The two most common formats you'll use for images are PNG, which is great for icons and logos as you can keep space in the image, and JPG, which offers very good compression for pictures.

## Images in HTML

We add images to HTML using the `<img>` tag like so:

- The first attribute you will see is the `src` attribute which tells the HTML where the file is located. If the image is located in your project, and not on a different server, then you should use a relative file path.
- The second is the `alt` attribute. This sets the alternative text for the image. This is what assistive technologies and search engines use to know what the image is about. If you are adding an image to the HTML, it needs to have alt text.

### Styling HTML images

You will also note that we're not setting widths or heights in the HTML. All styling of the image should be handled in CSS.

In the CSS above, we are setting a `max-width` rather than a fixed `width`. The reason for that is to avoid horizontal scrollbars. As long as the logo has 200px of space, it will take up all 200px. However, as soon as other elements 'bump' into it, the logo will reduce in size to allow space for the other element, rather than forcing a horizontal scrollbar to appear.

Another popular way of managing image sizes is using percentage. This is especially useful if the image is inside a containing element such as `<div>` or `<section>` and you are already controlling the size of this element.

### Border-radius

If you wanted to create rounded edges on your image, for example for a profile picture, you would use the `border-radius` property.

`border-radius` can also be used on other elements as well.

You can decide how rounded you want the corners, and which corners you want to be rounded.

The above code adds a 50% border-radius to each corner of the image making it a perfect circle. If you only define one value for the `border-radius` it will apply to all corners, but you can apply a unique radius to each corner by setting the value for all four, like so:

The values are applied clockwise, so the first value applies to the top left corner, then top right, then bottom right, then bottom left.

## Images in CSS

To add an image using CSS, we need to use the background-image property.

Above, we can see a `background-image` is applied to the header. We use the `url()` value to give a file path to the image we want to load. Again, it's important to use the correct file path and ensure the image is loading correctly. The url should be relative to the CSS file in which it is written.

### Background-size

We have also set the `background-size`. In this case we've set it to cover, which means that the image will scale as large as possible without stretching the image, and it will crop the image if there is no space either horizontally or vertically.

Other values for `background-size` include `contain` which, like `cover`, scales with the element to which it is applied, but it won't crop. You can also set a pixel length or a percentage.

### Background-repeat

By default, the browser will repeat your background-image if there is available space to do so. A repeated background might be fine for a texture or pattern, but generally it's not ideal and so setting `background-repeat: no-repeat` ensures the background appears only once. Other values for `background-repeat` include: `repeat`, `repeat-x`, `repeat-y,` `space`, and `round`.

### Background-color

While on the topic of backgrounds, it's worth mentioning the `background-color` property which allows you to set the color of an element. The text inside the element is set by the `color` property.

### Background

There is a shorthand for managing backgrounds. Instead of writing each property on its own line, we can write it in one line like so:

## Font Awesome

One of the most popular sets of icons for online is the Font Awesome library. Here you are able to add icons directly into your HTML using short code snippets provided to you by Font Awesome.

**Steps:**

- Go to the Font Awesome website.
- Register for an account. Creating an account will allow you to get access to their CDN (Content Delivery Network) where you will be able to load icons from their network.
- When you've signed up, you'll be given a script tag which you can add to the head of your HTML document.
- Once you've added the script tag to each HTML page on which you want icons, you can start adding the icons to the HTML.

There is a huge library of icons from which to choose. Once you've chosen your icons, you can add them like so:

<hr>

## Activities

**WATCH**

[This tutorial video on using and adding images to the page.](https://scrimba.com/scrim/c7PaPeAZ?pl=paaBbTa) (6m 10s)

<hr>

## Lesson Task

### Brief

There are practice questions in the master branch of [this repo](https://scrimba.com/scrim/c7PaPeAZ?pl=paaBbTa).

Attempt the answers before checking them against the answers in the [answers branch](https://github.com/Noroff-Education/lesson-task-htmlcss-module2-lesson1/tree/answers) of the repo.
