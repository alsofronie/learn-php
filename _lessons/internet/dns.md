---
title: Lesson 02
description: DNS - Domain Name Service
layout: "default"
---

# DNS - Domain Name Service
### Lesson 1.

> A DNS is an address book that translates the domain name to a corresponding IP Address.

The TCP/IP protocol uses numerical addresses to identify the connected computers. These numerical addreses are formed by 4 numbers between 0 and 255, separated by a dot (`.`) character. They are called **IP Addresses**.

Example:

    216.58.213.228

Because humans have notorious difficulty dealing with numbers, a name / IP Address was invented, so the **domains** were born.

Basically, a DNS Server (which provides domain name services) is like a contact list that knows the IP address of a domain name. When a DNS Server does not know an IP address, it will ask other DNS servers about that IP address until one knows about it.

There are some Top Level Domains (TLD): `com`, `net`, `org`, `mil`, `net`, `ro`, and many many other.

When you acquire a domain, let's say `google.com`, it means you must acquire it from the `com` owner. Each owner has control on his own subdomains. For `google.com`, the `google` part is a subdomain of `com`. But, because the TLD's are not directly accessible, when we are talking about `google.com` we say it is a **domain** name. When we are taking about `www.google.com` we say the `www` is the subdomain of `google.com`. Remember, `google.com` has the control over `www.google.com`, `developers.google.com`, `mail.google.com` and so on.

When you acquire a domain, you can create unlimited subdomains, given their name is unique and a DNS translates the subdomain in their respective IP address. So, in our example, `analytics.google.com` and `mail.google.com` can have different IP addresses or not.

For an in-depth knowledge of DNS, take a look at (this good document by Digital Ocean)[https://www.digitalocean.com/community/tutorials/an-introduction-to-dns-terminology-components-and-concepts].

