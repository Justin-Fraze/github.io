---
title: "DNS Explained Like You're 12"
layout: single
author_profile: true
categories: [Networking, Fundamentals]
tags: [DNS, IT Support]
---

DNS is like the phonebook of the internet.

When you type `google.com` in your browser, your computer doesn't understand it directly. It needs the IP address, like `142.250.64.78`.

So it goes through a process called **DNS resolution**, asking a chain of servers what the correct IP is. It happens fast — usually in milliseconds.

Here’s how the process works:

1. Check local cache
2. Ask the DNS resolver (like `8.8.8.8`)
3. Ask root servers for `.com`
4. Ask `.com` servers for `google.com`
5. Ask the authoritative server for the exact IP
6. Return the IP to your browser

You can try this using:

```bash
nslookup google.com
dig google.com

