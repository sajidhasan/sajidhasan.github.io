---
layout: default
title: {{ site.name }}
---

<div id="home">
  <h1 style="text-align:center;">Perl Scripting</h1>
</div>
<ul>
{% for post in site.posts %} 
{% if post.categories contains "perl" %}
	<li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
{% endif %}
{% endfor %}