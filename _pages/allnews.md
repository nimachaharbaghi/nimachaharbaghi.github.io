---
title: "News"
layout: textlay
sitemap: false
permalink: /allnews.html
---

## News

<div class="jumbotron">

{% for article in site.data.news %}
  <article class="news-item">
    <h3>{{ item.title }}</h3>
    <p><strong>{{ item.date | date: "%B %d, %Y" }}</strong></p>
    <p>{{ item.content }}</p>
    {% if item.link %}
      <p><a href="{{ item.link }}" target="_blank">View Certificate</a></p>
    {% endif %}
  </article>
{% endfor %}

</div>
