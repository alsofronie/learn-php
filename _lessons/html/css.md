---
title: Lesson 04
description: HTML and CSS
layout: "default"
---

# HTML and CSS
### Lesson 4.

Take a look at the [source file](https://github.com/alsofronie/learn-php/blob/master/sources/simple-navbar.html) for a bery basic navbar with an interesting functionality: an active element (with the help of CSS `:hover`) that interacts with the visitor. You can [preview it here](https://alsofronie.github.io/learn-php/sources/simple-navbar.html).

Do not think this is an active or decision-logic implementation. The HTML has no `if` or `when`. Well, maybe a limited `when`, indicating a state of an element with the mouse cursor over it. The absolutely positioned element is basically shown or hidden based on the mouse hovering over an element, but the actual structure of the HTML remains the same.

To review, a `.` (dot) indicates a **class** and a `#` indicates and **id**. You can style a **tag** meaning all of those elements will look as instructed.

For example, we want to style the `body` tag (only one for HTML):

```css
body {
  margin:0;
  padding:0;
}
``` 

As expected, we instruct the browser not to render any margin or padding on our `body` element.

In the next block, we style all the `ul` that have a class of `menu` (like `<ul class="menu">`):

```css
ul.menu {
  list-style-type: none;
  margin:0;
  padding:0 10px;
  display: block;
  background-color: grey;
}
```

We can have more control on what we style and what not. For example, styling the immediate `li` descendant of `ul` will involve a CSS fragment like the next one, in which we use the `>` character to indicate the descendance:

```css
ul.menu > li {
  display: inline-block;
  height: 40px;
  line-height: 40px;
  position: relative;
}
```

We can have an arbitrary number of linked definitions, but for a readable code, a three level is a good limit you might want to use:

```css
ul.menu > li > a {
  display: block;
  padding: 0 10px;
  color: white;
  text-decoration: none;
}
```

The above fragment will style an `a` which is direct descendant of an `li`, as this one is the direct descendant of the `ul` with a *menu* class. An example of the affected html will be:

```html
<ul class="menu">
  <li><a href="#">This is styled</a></li>
</ul>
```

You should note a difference with the next fragment:

```css
ul.menu ul {
  list-style-type: none;
  display: none;
  position: absolute;
  left: 0;
  top: 100%;
  width: 300px;
  margin:0;
  padding:0;
  background-color: black;
  z-index: 100;
}
```

We did not use the `>` character, meaning we defined a style for **all** the `ul` tags inside an `ul.menu`.
