---
title: Customising Bootstrap using Sass
keywords: sample
tags: CSS Frameworks
sidebar: css-frameworks
permalink: css-frameworks/bootstrap-with-sass.html
folder: css-frameworks
---

## Introduction

Bootstrap offers a great basis for building a web application, however the colour and theme design choices made by the Bootstrap team may not match your requirements. Luckily, Bootstrap has been designed with customisation in mind and there are two methods to achieve this.

## Bootstrap Variables

If you explore either the Bootstrap SASS or CSS files you will notice that many values are controlled by variables. For example, the styles for the `.card` component:

```scss
.card {
  position: relative;
  display: flex;
  flex-direction: column;
  min-width: 0;
  height: $card-height;
  word-wrap: break-word;
  background-color: $card-bg;
  background-clip: border-box;
  border: $card-border-width solid $card-border-color;
  @include border-radius($card-border-radius);
  @include box-shadow($card-box-shadow);
}
```

In total, 5 properties are controlled by either variables or mixins. Each of these variables corresponds with a variable in the `_variables.scss` file. For example, the colour variables are defined in this file like so:

```scss
// scss-docs-start color-variables
$blue:    #0d6efd !default;
$indigo:  #6610f2 !default;
$purple:  #6f42c1 !default;
$pink:    #d63384 !default;
$red:     #dc3545 !default;
$orange:  #fd7e14 !default;
$yellow:  #ffc107 !default;
$green:   #198754 !default;
$teal:    #20c997 !default;
$cyan:    #0dcaf0 !default;
```

The `!default` flag means that a second declaration of this variable will override the first one. This means that we can write our own SASS variables with the same names in order to start customising the theme.

Take this project structure for example:

```
/package.json
/node_modules/bootstrap/scss/_variables.scss
/src/scss/_variables.scss
/src/scss/styles.scss
```

We have the original `_variables.scss` file which contains the default values for each variable. We also have a `_variables.scss` file in our `src/scss` directory containing our custom overrides. For example:

`/src/scss/_variables.scss`
```scss
$blue:    #5d95e8;
$indigo:  #916fc8;
$purple:  #5d3b9c;
$pink:    #ab4578;
$red:     #fa2f44;
$orange:  #ffa053;
$yellow:  #ffdf7e;
$green:   #4fe49e;
$teal:    #9fffe2;
$cyan:    #8eecff;
```

Here we have *overridden* the default values for these colour variables. You can read more about default values here: [Default Values](https://sass-lang.com/documentation/variables#default-values).

Inside our `src/scss/styles.scss` file we simply `@import` our custom variables before we `@import` the main Bootstrap SASS file:

```scss
@import "variables"; /* /src/scss/_variables.scss */
@import "../../node_modules/bootstrap/scss/bootstrap";

.btn-custom {
  @extend .btn-warning;
  
  &:hover {
    @extend .btn-danger;
  }
}
```

The first line is the shortcut to our custom variables. The second line is the import of the main Bootstrap SASS file from the `node_modules` directory.

Below we have a custom button style that changes colour from `btn-warning` to `btn-danger` when the user hovers over it.

```html
<button class="btn btn-custom">Warning!</button>
```

If you check the output `/dist/css/styles.css` file, you will see that this custom button class has been slotted into place within the existing Bootstrap files - instead of creating new styles at the end of the stylesheet. You should also notice that the colour theme transformations carry over to the custom button class.

To unlock the full potential of your `_variables.scss` file, take a copy of Bootstrap's version of the same file and make sure to import `Bootstrap SASS Functions` from the `node_modules` directory:

```scss
@import "../../node_modules/bootstrap/scss/functions";
```
## Lesson Task

### Brief


### Resources


### Process
