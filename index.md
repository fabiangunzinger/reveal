---
layout: default
title: Home
---

{% for post in site.posts %}
<article>
  <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
  <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time>
  {% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncate: 200 }}</p>{% endif %}
</article>
{% unless forloop.last %}<hr>{% endunless %}
{% endfor %}
