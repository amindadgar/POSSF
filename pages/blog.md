---
layout: page
permalink: /blog/
lang: fa
title: وبلاگ و مطالب جشنواره اوپن سورس فارسی
---

<h2>اسامی مطالب اخیر</h2>

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      {% assign date_format = site.cayman-blog.date_format | default: "%b %-d, %Y" %}
      <span class="post-meta">{{ post.date | date: date_format }}</span>
      <h2>
        <a class="post-link" href="{{ post.url | relative_url }}" title="{{ post.title }}">{{ post.title | escape }}</a>
      </h2>
      <span>{{ post.excerpt | markdownify | truncatewords: 30 }}</span>
    </li>
  {% endfor %}
</ul>