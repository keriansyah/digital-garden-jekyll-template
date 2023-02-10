---
title: Archives
layout: page
permalink: /archive
---
<h1>{{page.title}}</h1>
{% assign grouped_by_year = site.notes | group_by_exp: "note", "note.date | date: '%Y'" %}
{% for year in grouped_by_year %}
<h2>{{ year.name }}</h2>
{% assign grouped_by_month = year.items | group_by_exp: "note", "note.date | date: '%B'" %}
{% for month in grouped_by_month %}
<strong>{{ month.name }}</strong>
<ul>{% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
{% for note in recent_notes %}
    <li><a class="internal-link" href="{{ note.url }}">{{ note.title }}</a><span class="n-desc">{{note.description}}</span></li>
{% endfor %}
</ul>
{% endfor %}
{% endfor %}