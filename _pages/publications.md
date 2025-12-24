---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
classes: publications-page
---

<div class="pub-list">
  {% assign pubs = site.publications | sort: "date" | reverse %}
  {% assign current_year = "" %}

  {% for p in pubs %}
    {% assign y = p.date | date: "%Y" %}

    {% if y != current_year %}
      {% assign current_year = y %}
      <h2 class="pub-year">{{ current_year }}</h2>
    {% endif %}

    {% include pub-card.html item=p %}
  {% endfor %}
</div>

