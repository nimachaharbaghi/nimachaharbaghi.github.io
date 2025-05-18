---
title: "News"
layout: textlay
sitemap: false
permalink: /allnews.html
---

## News

<div class="jumbotron">

{% for item in site.data.news %}
  <h3>{{ item.title }}</h3>
  <p><strong>{{ item.date }}</strong></p>
  <p>{{ item.content }}</p>
  <p>
    <a href="{{ item.link }}" target="_blank" rel="noopener">
      <button type="button" style="padding: 10px 20px; font-size: 16px; cursor: pointer; background-color: #007acc; color: white; border: none; border-radius: 5px;">
          View Certificate
      </button>
    </a>
  </p>
{% endfor %}





</div>
