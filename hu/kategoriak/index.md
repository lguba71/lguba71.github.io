---
layout: page
title: "Kategóriák"
description: "Szakmai jegyzetek témakörök szerint rendezve."
lang: hu
permalink: /hu/kategoriak/
---

{% assign hu_notes = site.pages | where: "lang", "hu" | where: "layout", "post" | where_exp: "item", "item.url contains '/hu/jegyzetek/'" | sort: "date" | reverse %}

<p style="font-size: 1.2rem; line-height: 1.5; color: #12395B;">
Szakmai jegyzetek témakörök szerint rendezve.
</p>

{% assign categories = '' | split: '' %}

{% for note in hu_notes %}
{% for category in note.categories %}
{% assign display_category = category | replace: 'Magyar szakmai jegyzetek', 'Szakmai jegyzetek' %}
{% assign categories = categories | push: display_category %}
{% endfor %}
{% endfor %}

{% assign categories = categories | uniq | sort_natural %}

{% if categories.size > 0 %}
<div class="d-flex flex-wrap mt-3 mb-4 me-3">
{% for category in categories %}
{% assign category_slug = category | slugify | url_encode %}
<a class="post-tag btn btn-outline-primary" href="#{{ category_slug }}">{{ category }}</a>
{% endfor %}
</div>

{% for category in categories %}
{% assign category_slug = category | slugify | url_encode %}
<section id="{{ category_slug }}" style="margin: 2rem 0;">
<h2>{{ category }}</h2>
<ul>
{% for note in hu_notes %}
{% for note_category in note.categories %}
{% assign display_note_category = note_category | replace: 'Magyar szakmai jegyzetek', 'Szakmai jegyzetek' %}
{% if display_note_category == category %}
<li><a href="{{ note.url | relative_url }}">{{ note.title }}</a></li>
{% break %}
{% endif %}
{% endfor %}
{% endfor %}
</ul>
</section>
{% endfor %}
{% else %}
<p>Jelenleg nincs kategorizált jegyzet.</p>
{% endif %}
