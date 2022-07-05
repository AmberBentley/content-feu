---
title: Forms
keywords: sample
tags: HTML and CSS
sidebar: html-css
permalink: html-css/forms.html
folder: html-css
---
## Introduction

In this lesson, we'll be looking at how you can set up forms correctly.

## The Form Element

The form element provides you with a method of collecting a user’s input. We could collect the user's name, email address, or a message. We can also use checkboxes and radio buttons to allow users to choose specific items in the form.

The `<form>` element is used to create a form that can submit data to a server where it can be handled.
The form's action property sets where the data gets sent. In the above example, the data will be sent to a file called submit.php where PHP will be used to handle the data. 

_Note: we won't be working with data handling. It is outside the scope of this course._

The method property sets how the data will be sent. POST is the most secure way of sending data. The other option is GET which sends the data in the browser's address bar. This is good for testing that the data is being sent correctly, but for ensuring your user's data gets handled carefully, you should mostly use POST for the finished form.

## Inputs

One of the most common ways of collecting data from a user is using the `<input>` element. There are many different types of input. How they display in the browser depends on their type. By default, an input has a type of text.

The types of input include the following (although there are more):
- Button 
- Checkbox 
- Date 
- Email 
- Number 
- Password 
- Radio 
- Submit 
- Tel (for telephone numbers, note that you should not use the 'number' type for a telephone number).

### Name attribute

When the form data gets sent to the server, the name of the input element will be sent with its content. Since a form may have any number of input fields, these name attributes are important! What these names are is up to you: you don't have to call the input for the first name "firstname" – you can call it "forename", "first_name", "f_name" or pretty much whatever you want. Just be sure not to use spaces or illegal characters. For your own sake, it is best to use names that will be easy to remember. While it is possible to name your first name input "wingnut", it may not be so helpful when you revisit the project six months later!

### Radio Buttons

Grouped radio buttons allow you to choose only one of the supplied options. On an HTML page, only one radio button may be chosen. If one button is chosen, the other radio buttons will deselect. For this reason, grouped radio buttons must share the same name. Here is an example:

### Labels

In the code above you will see that a label has been joined to an input. Semantically this is good, but it also has the added bonus of being good for UX as a user can click the label and still select the radio button. To link a label to an input, use the `id` attribute of the input for the `for` property. 

If you want the input and labels to each be on their own lines, please do not use `<br>` tags. What you can do, is add content after the label and set it to `display: block:`

Another option is to group inputs and labels in a div or section element.

### Value attribute

You will see a new attribute on these inputs: the `value` attribute. What is the difference between the name and value attributes? The `name` simply identifies the input element. The `value` attribute sends the associated value of the input. In the case of a text input field, it would be the user's typed input. But as radio buttons do not have an associated default value, we must supply it. This is especially important for any kind of input types that do not allow text input – the value must be set in advance.

### Checkboxes

Checkboxes allow users to pick multiple (or no) options on the form. You will see that the name property for each of the checkboxes is unique unlike on radio buttons where it was the same.

### Submit

The submit input sends the form data off to whatever file is set up as the action using whatever method is set on the form. You can control the text of the input button using the `value` attribute.

### Select

If you want to create a menu of options list, you can use the `select` element. Each option inside the select should have a value set.

### Datalist

The `datalist` element is similar to a `select` in that it uses options for the user. The difference between the two is that with a `select` the user must choose one of the available options, but with the `datalist` element it simply offers suggestions.

### Textarea

To allow users to input multiple lines of text, as you would in a message, you can use the textarea element.

The `row` and `col` attributes set how large the textarea is, although this can cause issues in responsive design, and so in general it's best to control the sizing of `textarea`s using CSS.

### Fieldsets

Fieldsets are a good way of organizing form data. The `<fieldset>` element may be wrapped around any number of input elements.

The `<legend>` tag supplies a caption for the fieldset, allowing the user to know what this group of inputs is about. More than one fieldset may be included in a form.

### CSS Attribute Selectors

We will also be looking at another way of styling CSS – CSS attribute selectors. Attribute selectors allow us to define CSS rules by shared attributes. We will be using attribute selectors to style a form. This will illustrate how these may be used, and how this will again make for more efficient CSS and less work spent on formatting elements that share attributes. The syntax for CSS attribute selectors is square braces containing the attribute, as follows:

This selector will affect any form input element that has the type of text. As with other CSS selectors, careful planning will allow us to style multiple elements simultaneously.

## Activities

**WATCH**

[This tutorial video on using forms.](https://scrimba.com/scrim/cpDVJVHz?pl=paaBbTa) (10m 21s)

## Lesson Task

### Brief

There are practice questions in the master branch of [this repo](https://github.com/Noroff-Education/lesson-task-htmlcss-module2-lesson2).

Attempt the answers before checking them against the answers in the [answers branch](https://github.com/Noroff-Education/lesson-task-htmlcss-module2-lesson2/tree/answers) of the repo.
