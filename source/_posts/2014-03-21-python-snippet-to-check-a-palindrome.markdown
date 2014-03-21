---
layout: post
title: "Python Snippet To Check A Palindrome"
date: 2014-03-21 10:49:02 -0500
comments: true
categories: development
---

Found a little Python snippet to determine if a string is a palindrome.

{% codeblock lang:python %}
is_palindrome = lambda s: s == s[::-1]
{% endcodeblock %}

Nifty.
