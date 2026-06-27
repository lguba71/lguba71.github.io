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

</section>

<section style="margin: 2rem 0;">

  <h2>Jövőbeli témák</h2>

  <p>A következő magyar jegyzetek várhatóan ilyen témák köré épülnek:</p>

  <ul>
    <li>gyártható CAD-modellek és használható műszaki alapok,</li>
    <li>régi papírrajzok, 2D rajzok és hiányos dokumentációk feldolgozása,</li>
    <li>készülékek, jigek, befogók és gyártási segédeszközök tervezése,</li>
    <li>célgép-részegységek és meglévő berendezések gépészeti módosítása,</li>
    <li>gyártási rajzok, BOM-ok és műszaki dokumentáció rendezése,</li>
    <li>külső mérnöki kapacitás bevonása gyártási és automatizálási projektekbe.</li>
  </ul>

</section>

<section style="margin: 2rem 0;">

  <h2>Megjelenési gyakoriság</h2>

  <p>
    A cél havi egy rövid, gyakorlati magyar szakmai jegyzet közzététele.
    A fókusz nem a nagy mennyiségű blogolás, hanem az üzletileg és műszakilag
    hasznos témák bemutatása magyar gyártó cégek, célgépépítők és automatizálási
    projektek számára.
  </p>

  <p>
    A régebbi jegyzetek az <a href="{{ '/hu/archivum/' | relative_url }}">archívumban</a> találhatók.
  </p>

