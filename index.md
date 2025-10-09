---
layout: default
title: Home
---

<ul class="postlist">
  {% assign posts = site.posts | sort: 'date' | reverse %}
  {% for post in posts %}
    <li class="postitem">
      <a class="postlink" href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
      <time class="postdate" datetime="{{ post.date | date_to_xmlschema }}">
        {{ post.date | date: "%-d %b, %Y" }}
      </time>
    </li>
  {% endfor %}
</ul>
