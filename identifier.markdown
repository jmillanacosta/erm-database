---
layout: page
title: Identifiers
permalink: /identifiers/
---

<div class="tag-cloud">
{% assign sortedtags = site.tags | sort %}
{% for tag in sortedtags %}
  <ul class="post-list">
  {% assign tag_name = tag[0] %}
  {% if tag_name contains "erm:" %}
    <li>
      <a href="{{ tag_name | slice: 4,20 | prepend: '/substance/' | relative_url }}">{{ tag | first }}</a>
    </li>
  {% endif %}
  </ul>
{% endfor %}
</div>
