---
layout: page
title: Outils et Tutos
---
<ul class="cartes">
  {% for o in site.outils %}
  <li class="carte">
    <div class="image-ph" aria-hidden="true"></div>
    <div class="contenu">
      <h3>{{ o.title }}</h3>
      <p>{{ o.resume }}</p>
      {% if o.url %}<a class="lien" href="{{ o.url }}" target="_blank" rel="noopener">Accéder →</a>{% endif %}
    </div>
  </li>
  {% endfor %}
</ul>
