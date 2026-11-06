---
layout: page
permalink: /blog/
title: Blog
description: "Notes on research, security, and standardization."
nav: true
nav_order: 3
pagination:
  enabled: true
  collection: posts
  permalink: /page/:num/
  per_page: 10
  sort_field: date
  sort_reverse: true
  trail:
    before: 1
    after: 2
---

{% if paginator %}
  {% assign blog_posts = paginator.posts %}
{% else %}
  {% assign blog_posts = site.posts %}
{% endif %}

<ul class="post-list">
  {% for post in blog_posts %}
    <li>
      <p class="post-meta"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: '%Y-%m-%d' }}</time></p>
      <h2><a class="post-title" href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      {% if post.description %}<p>{{ post.description }}</p>{% endif %}
    </li>
  {% endfor %}
</ul>

{% if paginator.total_pages > 1 %}
  {% include pagination.liquid %}
{% endif %}
