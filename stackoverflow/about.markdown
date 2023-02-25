---
layout: page
title: About
permalink: /about/
---

## List all Tags of page
<ul>
    {% for tag in site.tags %}
        {% assign t = tag | first %}
        {% assign posts = tag | last %}

        <li>{{ t }}</li>
    {% endfor %}
</ul>

## One word Tag `featured´
<ol class="list-featured">
    {% for post in site.tags.featured %}
        <li class="mb-4">{{ post.title }}</li>
    {% endfor %}
</ol>

## Two word Tag `top featured´
<ol class="list-featured">
    {% for post in site.tags["top featured"] %}
        <li class="mb-4">{{ post.title }}</li>
    {% endfor %}
</ol>

## Two word Tag `top featured´ with **assign**
<ol class="list-featured">
    {% assign myTagName = "top featured" %}
    {% for post in site.tags[myTagName] %}
        <li class="mb-4">{{ post.title }}</li>
    {% endfor %}
</ol>
