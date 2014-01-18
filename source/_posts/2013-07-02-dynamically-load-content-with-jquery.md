---
layout: post
title: "Dynamically Load Content With jQuery"
date: 2013-07-02 09:04
comments: true
categories: web development
---

This post is more for my reference than anything else.

I've been working on a fairly simple static site, based on Twitter's [Bootstrap](http://twitter.github.io/bootstrap/) framework. I don't really want to add the complexity of a templating system or anything like that, but as the site has started to grow, maintaining a bunch of static pages has gotten a little unwieldy (yesterday I caught myself copy-pasting the footer div to 6 different files...yuck!)

The solution? Dynamically load content that's repeated across a lot of pages, using jQuery.

Here's how I did it (I'll use the footer as an example):

First, I put the repeated content into a separate HTML file (`footer.html`).

Then, on each page I want to have this footer in, I put in an empty div in the place I want the footer to be loaded in:

{% codeblock lang:html %}
<div id="footer"></div> <!-- footer loaded here -->
{% endcodeblock %}

At the end of the document, I use a jQuery function to load the content of the footer into the current page:


{% codeblock lang:javascript %}
$(function() {
  $("#footer").load("footer.html");
  $.ajaxSetup({
    async: false
  });
});
{% endcodeblock %}

The call to `ajaxSetup` with the `async: false` parameter is optional. I put it in there to try and reduce the visual "flicker" that happens when the content is loaded after the rest of the page. There's still a small delay, but it's not really noticeable. It's also probably not necessary for a normal footer, since it's likely to be "below the fold" anyway.
