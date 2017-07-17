---
layout: default
title: Movies & Serial Digest
order: 2
---

<div class="home">

  <h1 class="page-heading">Movies and Serial Digest</h1>
  <ul class="post-list">
    {% for post in site.categories.movies_serial %}
      <li>
        {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
        <span class="post-meta">{{ post.date | date: date_format }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p>

</div>