---
layout: splash
permalink: /
hidden: true
{% if site.show_hero_image %}
header:
  overlay_image: /assets/images/home-banner.jpg
  overlay_filter: 0.5
classes:
  - landing
  - custom-header-height
{% else %}
classes:
  - landing
{% endif %}
---

{% include feature_row %} 