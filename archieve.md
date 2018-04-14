---
layout: page
title: Archieve
permalink: /archieve/
---

{% assign old_year=0 %}
{% for post in site.posts %}
{% capture new_year%}} {{post.date | date: '%Y'}} {% endcapture %}
{% if old_year!=new_year %}
## {{post.date | date: '%Y'}}
{% assign old_year=new_year %}
{% endif %}
- {{post.date | date: '%m'}}/{{post.date | date: '%d'}} [{{post.title}}]({{post.url}}) 
{% endfor %}