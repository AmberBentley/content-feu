---
title: Local Storage
keywords: sample
tags: JavaScript 2
sidebar: javascript-2
permalink: javascript-2/localstorage.html
folder: javascript-2
---

# Local Storage:

Local Storage/`localStorage` allows us to store data in the browser that will persist across browser sessions. This means it will continue to exist after we've opened and closed the browser.

Local Storage allows us to store data for users visiting our websites and apps, however if they clear all of the browser cache then it will likely also clear these variables.

Local storage is great for storing data such as user preferences (dark mode or light mode enabled), but it can't be relied upon for long time storage. For long-term storage you would likely be utilizing a database to store the data.

**Note:** Local Storage is part of the window interface, meaning that it only exists on browsers.

## The basics:

Data in Local Storage is stored as JSON, which are key/value pairs similar to a JavaScript object.

## Viewing and clearing

We need to know how to view and clear our Local Storage. The concept is the same across all browsers, however the Local Storage data is in different tabs on different browsers.

### Chrome:

- Open the Chrome DevTools:

  - F1
  - F12
  - Windows: Ctrl + Shift I, MacOS: Cmd + Opt + I
  - Right-click the document and click Inspect.

- Click on the Application tab.

- Click on `Local Storage` in the left menu list column. You will now see an entry for the page you are on. Clicking on this entry will then show you any values stored in Local Storage for that page.

**Note:** If you haven't stored any values then this no values will show.

### Firefox:

- Open the Firefox Developer Tools with one of the following:

  - F12
  - Windows: Ctrl + Shift I, MacOS: Cmd + Opt + I
  - Right-click the document and click Inspect.

- Click on the `Storage` tab.

- Click on `Local Storage` in the left menu list column. You will now see an entry for the page you are on. Clicking on this entry will then show you any values stored in Local Storage for that page.

**Note:** If you haven't stored any values then this no values will show.

[VIMEO LINK: Where to find `localStorage`]

## Storing data:

To store data in `localStorage`, we use [?]

## Retrieving data:

To retrieve data from `localStorage`, we use

# sessionStorage:

`sessionStorage` is exactly the same as `localStorage` except it's data is cleared immediately when the page is closed.
