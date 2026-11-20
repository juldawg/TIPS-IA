---
layout: page
title: Vidéos
---
<ul class="cartes">
  {% for v in site.videos %}
  <li class="carte">
    <div class="image-ph" aria-hidden="true"></div>
    <div class="contenu">
      <h3>{{ v.title }}</h3>
      <p>{{ v.resume }}</p>
      <a class="lien" href="{{ v.url }}" target="_blank" rel="noopener">Voir la vidéo →</a>
    </div>
  </li>
  {% endfor %}
</ul>
