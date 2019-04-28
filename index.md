---
layout: default
title: The Augusta Commuter
sitemap:
    priority: 0.9
    changefreq: monthly
---

{% assign collection = site.posts | sort: "date" | reverse %}

<div class="list-group">
  {% for post in collection %}
  
  <div class="list-group-item">
    {% if post.title %} <a href="/augusta-commuter{{ post.url }}"><h3>{{ post.title }}</h3></a> {% endif %}
    {% if post.date %} {{ post.date | date: "%d %B %Y" }} {% endif %}
    | <a href="http://metatheorem.org/augusta-comm uter/{{ post.url }}#disqus_thread"></a>
  </div>  
  {% endfor %}
  
</div>
