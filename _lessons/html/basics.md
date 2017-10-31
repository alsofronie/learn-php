---
title: Lesson 03
description: HTML Basics
layout: "default"
---

# HTML
### Lesson 3.

The Hypertext Markup Language is used to convey text and media contents to the visitors of a website.

Altough you can modify it on-the-fly using Javascript, as a language, HTML is a static language (there is no control logic built in HTML).

Let's review how the internet works for a simple HTML file.

The user opens the browser and types in the address bar:

    www.php.net

When `enter` is pressed, this happens:

 - the browser automatically adds `http://` (the default protocol).
 - the browser automatically queries a DNS server about the IP address of the `www.php.net`. If this query yields nothing, a DNS query about `php.net` is launched. The response contains an IP Address for tne DNS Server that governs the `php.net` domain name, which is used to ask for the IP Address for the `www` subdomain of the `php.net`.
 - a HTTP query (indicated by `http://` schema in the request) is lanched to the IP Address determined on step above.
 - The browser waits for the response
 - The browser receives the HTML file.
 - The browser **renders** the HTML file to the screen.

You must remember that the rules on which the HTML file is rendered on your screen depends on the browser. Different browsers can render (in general with small differences) the same HTML file on the same computer and screen.

The invaluable resource for HTML tags is (W3 Schools website)[https://www.w3schools.com/html/html_intro.asp].

If you need to know a feature is supported in which browser, feel free to consult (the caniuse.com website)[https://caniuse.com/].

