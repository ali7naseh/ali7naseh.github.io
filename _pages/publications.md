---
layout: archive
title: "Selected Publications"
permalink: /publications/
author_profile: true
classes: publications-page
---
<p class="pub-note">
  For a complete list of publications, please see my
  <a href="https://scholar.google.com/citations?view_op=list_works&hl=en&hl=en&user=1K2KvWwAAAAJ" target="_blank">
    Google Scholar profile
  </a>.
</p>

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

