---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
classes: publications-page
---

<div class="pub-list">
  {% assign pubs = site.publications | sort: "date" | reverse %}
  {% for p in pubs %}
    {% include pub-card.html item=p %}
  {% endfor %}
</div>
