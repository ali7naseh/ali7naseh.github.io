---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a fourth-year Ph.D. student at the Manning College of Information & Computer Sciences at UMass Amherst, advised by [Amir Houmansadr](https://people.cs.umass.edu/~amir/). My research focuses on **trustworthy generative AI**, with an emphasis on **privacy and security risks in large language models and multimodal systems**. I obtained my bachelor's degree from Sharif University of Technology.

### 🤝 Open to Collaboration

Curious about how to break generative models? Me too. I'm happy to chat, brainstorm, or collaborate on new ideas around **LLM and multimodal model vulnerabilities**. Just shoot me an email: anaseh (at) umass.edu.



## News

{% assign k = 5 %}
{% assign news_sorted = site.data.news | sort: "date" | reverse %}

<ul class="news-list">
  {% for item in news_sorted limit:k %}
    <li class="news-item">
      <span class="news-date">{{ item.date | date: "%B %-d, %Y" }}</span>
      <span class="news-text">{{ item.text }}</span>
    </li>
  {% endfor %}
</ul>

{% if news_sorted.size > k %}
  <details class="news-more">
    <summary>Show older news</summary>

    <ul class="news-list news-list--older">
      {% for item in news_sorted offset:k %}
        <li class="news-item">
          <span class="news-date">{{ item.date | date: "%B %-d, %Y" }}</span>
          <span class="news-text">{{ item.text }}</span>
        </li>
      {% endfor %}
    </ul>
  </details>
{% endif %}
