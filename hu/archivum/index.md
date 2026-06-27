---
layout: page
title: "Magyar archívum"
description: "Régebbi magyar nyelvű szakmai jegyzetek archívuma gépésztervezésről, gyártástámogatásról, CAD-ről, készülékekről és célgép-projektekről."
lang: hu
permalink: /hu/archivum/
---

{% assign hu_notes = site.pages | where: "lang", "hu" | where: "layout", "post" | where_exp: "item", "item.url contains '/hu/jegyzetek/'" | sort: "date" | reverse %}

<section style="margin-bottom: 2rem;">

  <p style="font-size: 1.2rem; line-height: 1.5; color: #12395B;">
    Régebbi magyar szakmai jegyzetek gyártástámogatásról, gépésztervezésről,
    CAD-ről, műszaki dokumentációról és célgép-projektekről.
  </p>

</section>

<section style="margin: 2rem 0;">

  <h2>Régebbi jegyzetek</h2>

  {% if hu_notes.size > 5 %}
    <ul>
      {% for note in hu_notes offset:5 %}
        <li>
          <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
        </li>
      {% endfor %}
    </ul>
  {% else %}
    <p>
      Jelenleg nincs archív magyar jegyzet. Az első öt magyar jegyzet a
      <a href="{{ '/hu/jegyzetek/' | relative_url }}">Jegyzetek</a> oldalon jelenik meg;
      a hatodik bejegyzéstől a régebbiek ide kerülnek.
    </p>
  {% endif %}

</section>

<section style="margin: 2rem 0;">

  <p>
    <a href="{{ '/hu/jegyzetek/' | relative_url }}">← Vissza a magyar jegyzetekhez</a>
  </p>

</section>
