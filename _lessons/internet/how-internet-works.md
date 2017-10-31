---
title: Lesson 01
description: How Internet Works
layout: "default"
---

# How Internet works
### Lesson 1.

Skipping the (internet history)[https://en.wikipedia.org/wiki/History_of_the_Internet], we will focus
on exactly how the technology behind the Internet websites work.

> Sometimes the descriptions and definitions are somewhat limited and inaccurate, just to simplify things from the reader's perspective.

A server is a program that exists only to serve some services to other programs / users. Usually, a machine (a computer) that has only (or mainly) such programs is called also a Server.

A protocol is a set of rules that governs a discussion. Think of it as a spoken language. If two participants know the same language, they can understand each other. It's the same with the computers, but we can build in protocol some failsafe mechanisms and security.

The protocol that governs the Internet is called (TCP/IP)[https://en.wikipedia.org/wiki/Internet_protocol_suite]. Using a mechanism called encapsulation, we can use higher level protocols (protocols that rely on TCP/IP and decorate it with some new functionalities) to communicate in a somewhat *friendlier* way. The one that concerns us is (HTTP)[https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol].

An HTTP server is a program that *listens* to queries and responses to each query. A query is defined (among other things) by the scheme and an **URL**. The URL contains the server name and a *path*:

    http://php.net/manual/en/tutorial.php

Where:

 - `http` is the scheme, indicating the protocol used
 - `php.net` is the domain name (server name)
 - `/manual/en` is the path
 - `tutorial.php` is the file name

So, we want the `tutorial.php` file from the `/manual/en` path on `php.net` server.

By default, that is all a HTTP Server does. It returns the resource you requested by the URL.

There is one notable convention that should be mentioned here. When you request a path (and not a file), there are two behaviours the HTTP Server can implement. For example,

    http://php.net/manual/en/

is a request that does not want a file, but a directory. Based on the configuration of the HTTP Server, there can be two outcomes (two different responses) for this request: one is to return a representation for the list of the files in that directory on the disk; the other is to return a special file, named `index.html` in the root of that drectory. This convention is very important because, when you do not specify *any* path, the server response is the file located in it's root path, named `index.html` (or, as we will learn PHP, `index.php`).

So, the following three requests:

    http://www.php.net
    http://www.php.net/
    http://www.php.net/index.php

They all return the same result, namely the `index.php` file in the root directory.
