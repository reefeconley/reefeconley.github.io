---
layout: archive
title: "Gallery"
permalink: /portfolio/
author_profile: true
---

{% include base_path %}

Below are a miscellany of thermodynamic and fluid dynamic simulations and derivations, with a focus on applications within the Earth Sciences.

{% for post in site.portfolio %}
  {% include archive-single.html %}
{% endfor %}

