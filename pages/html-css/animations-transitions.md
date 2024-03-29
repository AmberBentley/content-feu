---
title: Animations and Transitions
keywords: sample
tags: HTML and CSS
sidebar: html-css
permalink: html-css/animations-transitions.html
folder: html-css
---

## Introduction

Animations and transitions:

- enhance the user interface and can make it more engaging.
- can make the site easier to understand and explain what's happening, such as showing a section based on a user click or moving between pages.
- can also focus the user's attention and help with context switching.

Be careful when adding animations and transitions. Too many of them can make it hard to focus on what is important to the user. Remember that the styling added should improve the user's experience of the website.

## Animations

To create an animation, choose a name for your animation and set it on the element you'd like to animate.

In this example we're going to make a ball that bounces, and so the `animation-name` we’ve chosen is ‘bounce’. We also need to set how long the animation is to run using the `animation-duration` property.

Once you’ve set the animation-name and duration, you need to set what the animation does. To set what the animation does in CSS we need to use `@keyframes{}` and set what happens at various moments in the animation.

At 0% of the animation we want the ball to be at 300px from the top of the page. At 50% of the way through the animation, we want the ball to be at the top of the page, and by 100% of the animation we want to be at 300px from the top again.

You can choose what percentages you use and what styling is applied, but it's important to see how we use `@keyframes` to decide what our animation does.

### Animation Properties

Animation Property What it Does animation-name Name to be used in the @keyframes rule animation-duration How long the animation should run animation-iteration-count How many times the animation should run animation-fill-mode What styles should apply before/after animation has run animation-delay The delay before the animation starts animation-timing-function Manages acceleration in the animation animation-direction Direction the animation should run in. It can be reversed

## Transitions

Transitions allow you to smooth out changes in the user interface. Unlike an animation, they need a trigger to start them. A common trigger in CSS would be a user hovering over an element.

To use a transition on an element, you need to set to what property you'd like the transition to apply. You can select all or choose specific properties if you want the transition to only apply to them. Choosing individual properties also allow you to run the transitions on different delays.

In the code above, the ball will change colour on hover, but instead of it being a jarring change from red to blue, there is a 2s transition which will ease the change.

You can't use a transition on any styling. There needs to be a way of finding middle points for the transition. For example, transitions won't work on the display property because there's no middle point. If you did want to reveal/hide an element, then you would need to use the opacity property because there you can transition between 0.5 and 1 for example.

<hr>

## Activities

**WATCH**

The below tutorial video on animations and transitions (13m 28s).

<iframe src="https://player.vimeo.com/video/630771102?h=9ff631e16b&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="1914" height="1034" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen title="Animations and Transitions"></iframe>

<hr>

## Lesson Task

### Brief

There are practice questions in the master branch of [this repo](https://github.com/Noroff-Education/lesson-task-htmlcss-module4-lesson2).

Attempt the answers before checking them against the answers in the [answers branch](https://github.com/Noroff-Education/lesson-task-htmlcss-module4-lesson2/tree/answers) of the repo.
