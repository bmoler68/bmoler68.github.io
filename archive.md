---
layout: page
title: Blog Archive
---

{% assign sorted_tags = site.tags | sort %}
{% for tag in sorted_tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% assign sorted_posts = tag[1] | sort: "date" | reverse %}
    {% for post in sorted_posts %}
      <li><a href="{{ post.url }}">{{ post.date | date: "%B %Y" }} - {{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}