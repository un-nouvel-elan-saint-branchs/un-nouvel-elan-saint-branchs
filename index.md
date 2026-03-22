---
layout: default
title: Accueil
---

![Bandeau]({{ site.baseurl }}/assets/images/bandeau.jpg)

## Bienvenue

**Un nouvel élan pour Saint-Branchs** est un groupe d'élus engagés pour une commune plus transparente, participative et dynamique.

---

## 📰 Dernières actualités

{% for post in site.posts limit:3 %}
- [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
{% endfor %}

---

## 🏛️ Dernier conseil municipal

{% assign conseil = site.conseils | last %}
- [{{ conseil.title }}]({{ site.baseurl }}{{ conseil.url }})

---

## 👥 L'équipe

<div class="team-grid">
{% for membre in site.data.equipe %}
<div class="team-card">
  <img src="{{ site.baseurl }}{{ membre.photo }}" alt="{{ membre.nom }}" class="team-photo">
  <strong>{{ membre.nom }}</strong>
  <span>{{ membre.description }}</span>
</div>
{% endfor %}
</div>
