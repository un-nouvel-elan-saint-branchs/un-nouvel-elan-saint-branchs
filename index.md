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
- [{{ post.title }}]({{ post.url }})
{% endfor %}

---

## 🏛️ Dernier conseil municipal

{% assign conseil = site.conseils | last %}
- [{{ conseil.title }}]({{ conseil.url }})

---

## 👥 L'équipe

{% for membre in site.data.equipe %}
### {{ membre.nom }}
![photo]({{ site.baseurl }}/{{ membre.photo }})
{{ membre.description }}
{% endfor %}
