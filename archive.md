---
layout: page
title: Archive
permalink: /archive/
---

<div class="list-group">

{% for post in site.posts %}
	{% assign currentDate = post.date | date: "%Y" %}
	{% if currentDate != myDate %}
		<h2 class="archive-page-date">{{ currentDate }}</h2>
		{% assign myDate = currentDate %}
	{% endif %}
	<a class="list-group-item list-group-item-action" href="{{ site.baseurl }}{{ post.url }}">
		<span>{{ post.date | date: "%Y-%m-%d" }}</span> &nbsp; &nbsp; {{ post.title }}
	</a>
{% endfor %}

</div>
