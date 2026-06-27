---
layout: page
title: "Magyar szakmai jegyzetek"
description: "Magyar nyelvű gyártástámogató szakmai jegyzetek gépésztervezésről, CAD-ről, gyártási dokumentációról, készülékekről és célgép-támogatásról."
lang: hu
permalink: /hu/jegyzetek/
---

{% assign hu_notes = site.pages | where: "lang", "hu" | where: "layout", "post" | where_exp: "item", "item.url contains '/hu/jegyzetek/'" | sort: "date" | reverse %}

<section style="margin-bottom: 2rem;">

  <p style="font-size: 1.2rem; line-height: 1.5; color: #12395B;">
    Magyar nyelvű gyártástámogató szakmai jegyzetek gépésztervezésről,
    CAD-modellezésről, gyártási dokumentációról, készülékekről és célgép-projektekről.
  </p>

  <p>
    Ezek a cikkek elsősorban magyar gyártócégeknek, célgépépítőknek,
    automatizálási vállalkozásoknak és műszaki vezetőknek szólnak.
    A cél nem általános blogolás, hanem gyakorlati műszaki problémák,
    döntési helyzetek és szolgáltatási területek érthető bemutatása.
  </p>

</section>

<section style="margin: 2rem 0;">

  <h2>Legutóbbi jegyzetek</h2>

  {% if hu_notes.size > 0 %}
    <ul>
      {% for note in hu_notes limit:5 %}
        <li>
          <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
        </li>
      {% endfor %}
    </ul>
  {% else %}
    <p>Jelenleg nincs megjelent magyar jegyzet.</p>
  {% endif %}

  {% if hu_notes.size > 5 %}
    <p>
      <a href="{{ '/hu/archivum/' | relative_url }}">Régebbi magyar jegyzetek az archívumban</a>
    </p>
  {% endif %}

</section>

<section style="margin: 2rem 0;">

  <p>
    <a href="{{ '/hu/' | relative_url }}">← Vissza a magyar kezdőlapra</a>
  </p>

</section>
