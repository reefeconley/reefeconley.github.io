---
layout: archive
title: "Gallery"
permalink: /portfolio/
author_profile: true
---

{% include base_path %}

### Fluid Dynamics Notes

- Fluid dynamics of the solid Earth (unfinished): [<a href="/pdfs/FDSE_notes.pdf">Link</a>]
- Atmosphere, ocean and cryosphere dynamics : [Link]

Below are a miscellany of thermodynamic and fluid dynamic simulations and derivations, with a focus on applications within the Earth Sciences.

{% for post in site.portfolio %}
  {% include archive-single.html %}
{% endfor %}

