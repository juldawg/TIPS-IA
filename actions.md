---
layout: page
title: Actions
---
{% assign annees = site.actions | map: "annee" | uniq | sort | reverse %}

<div class="grille-boutons">
  {% for a in annees %}
  <a class="carte-bouton" href="#{{ a }}">{{ a }}</a>
  {% endfor %}
</div>

{% for a in annees %}
<h2 id="{{ a }}">{{ a }}</h2>
<ul class="cartes">
  {% assign items = site.actions | where: "annee", a | sort: "date" | reverse %}
  {% for it in items %}
  <li class="carte">
    {% if it.image %}<img src="{{ it.image | relative_url }}" alt="">{% else %}<div class="image-ph" aria-hidden="true"></div>{% endif %}
    <div class="contenu">
      <h3>{{ it.title }}</h3>
      <p>{{ it.resume }}</p>
      <a class="lien" href="{{ it.url | relative_url }}">En savoir plus →</a>
    </div>
  </li>
  {% endfor %}
</ul>
{% endfor %}
