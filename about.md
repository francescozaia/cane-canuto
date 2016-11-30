---
layout: page
permalink: /about/index.html
title: Cane canuto
tags: [cane, canuto]
imagefeature: fourseasons.jpg
chart: true
---
<figure>
  <img src="{{ site.url }}/images/me.jpg" alt="Hossain Mohammad Faysal">
  <figcaption>Yooooo</figcaption>
</figure>

{% assign total_words = 0 %}
{% assign total_readtime = 0 %}
{% assign featuredcount = 0 %}
{% assign statuscount = 0 %}

{% for post in site.posts %}
    {% assign post_words = post.content | strip_html | number_of_words %}
    {% assign readtime = post_words | append: '.0' | divided_by:200 %}
    {% assign total_words = total_words | plus: post_words %}
    {% assign total_readtime = total_readtime | plus: readtime %}
    {% if post.featured %}
    {% assign featuredcount = featuredcount | plus: 1 %}
    {% endif %}
{% endfor %}


***This is the space to create.***