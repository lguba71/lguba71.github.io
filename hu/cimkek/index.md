---
layout: page
title: "Címkék"
description: "Szakmai jegyzetek címkék szerint rendezve."
lang: hu
permalink: /hu/cimkek/
---

{% assign hu_notes = site.pages | where: "lang", "hu" | where: "layout", "post" | where_exp: "item", "item.url contains '/hu/jegyzetek/'" | sort: "date" | reverse %}

<p style="font-size: 1.2rem; line-height: 1.5; color: #12395B;">
  Szakmai jegyzetek címkék szerint rendezve.
</p>

{% assign tags = '' | split: '' %}

{% for note in hu_notes %}
  {% for tag in note.tags %}
    {% assign tags = tags | push: tag %}
  {% endfor %}
{% endfor %}

{% assign tags = tags | uniq | sort_natural %}

{% if tags.size > 0 %}
  <div class="d-flex flex-wrap mt-3 mb-4 me-3">
    {% for tag in tags %}
      {% assign tag_slug = tag | slugify | url_encode %}
      <a class="post-tag btn btn-outline-primary" href="#{{ tag_slug }}">{{ tag }}</a>
    {% endfor %}
  </div>

  {% for tag in tags %}
    {% assign tag_slug = tag | slugify | url_encode %}
    <section id="{{ tag_slug }}" style="margin: 2rem 0;">
      <h2>{{ tag }}</h2>
      <ul>
        {% for note in hu_notes %}
          {% if note.tags contains tag %}
            <li>
              <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
            </li>
          {% endif %}
        {% endfor %}
      </ul>
    </section>
  {% endfor %}
{% else %}
  <p>Jelenleg nincs címkézett jegyzet.</p>
{% endif %}
