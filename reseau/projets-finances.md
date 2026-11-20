---
layout: page
title: Projets financés
---
<ul class="cartes">
  {% for p in site.projets %}
  <li class="carte">
    <div class="image-ph" aria-hidden="true"></div>
    <div class="contenu">
      <div class="meta"><span class="tag clair">{{ p.annee }}</span></div>
      <h3>{{ p.title }}</h3>
      <p>{{ p.resume }}</p>
      {% if p.porteur %}<p class="meta">Porteur : {{ p.porteur }}</p>{% endif %}
    </div>
  </li>
  {% endfor %}
</ul>
