---
layout: default
title: {{ site.name }}
---

<div id="home">
  <h1 style="text-align:center;">Machine Learning</h1>
</div>

<ul>
{% for post in site.posts %} 
{% if post.categories contains "Machine Learning" %}
	<li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
{% endif %}
{% endfor %}