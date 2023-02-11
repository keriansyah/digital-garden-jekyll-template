---
title: Archives
permalink: /archive
---
<h1>{{page.title}}</h1>
{% assign grouped_by_year = site.notes | group_by_exp: "note", "note.date | date: '%Y'" %}
{% for year in grouped_by_year %}
<div class="arch">
<span><strong>{{ year.name }}</strong></span>
{% assign grouped_by_month = year.items | group_by_exp: "note", "note.date | date: '%B'" %}
{% for month in grouped_by_month %}
<span class="childright"><strong>{{ month.name }}</strong></span>
</div>
<ul class="arch-ul">{% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
{% for note in recent_notes %}
    <li><a class="internal-link" href="{{ note.url }}">{{ note.title }}</a><span class="n-desc">{{note.description}}</span></li>
{% endfor %}
</ul>
{% endfor %}
{% endfor %}

