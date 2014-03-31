---
layout: page
title: Posts
---

<ul>
  {% for post in site.posts %}
    <li>
      <small>{{ post.date | date_to_string }}</small>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>