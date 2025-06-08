---
title: "Home"
layout: gridlay
sitemap: false
permalink: /
---


## Home

{% for member in site.data.pi %}

<div class="jumbotron">
<div class="row">
<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-8 col-xs-12">
  <h3>{{ member.name }}</h3>
  <h4><i>{{ member.info }}</i></h4>
<div style="display: flex; flex-wrap: wrap; align-items: center; gap: 15px; margin-top: 10px;">
{% if member.email %}
  <a href="mailto:{{ member.email }}" target="_blank" style="display: inline-block;"><i class="fa fa-envelope-square fa-3x"></i></a>
{% endif %}
{% if member.cv %}
  <a href="{{ site.baseurl }}/{{ member.cv }}" download style="display: inline-block;"
     onclick="gtag('event', 'cv_download', { 'event_category': 'engagement', 'event_label': 'CV Button' });">
     <i class="ai ai-cv-square ai-3x"></i>
  </a>
{% endif %}
{% if member.gmail %}
  <a href="mailto:{{ member.gmail }}" target="_blank" style="display: inline-block;"><i class="fa fa-google-plus fa-3x"></i></a>
{% endif %}
{% if member.linkedin %}
  <a href="{{ member.linkedin }}" target="_blank" style="display: inline-block;"><i class="fa fa-linkedin-square fa-3x"></i></a>
{% endif %}
</div>


  <ul style="overflow: hidden">
    {% for education in member.education %}
      <li>{{ education | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>

</div>
</div>
</div>
{% endfor %}


{% if site.data.research %}
<div class="jumbotron">
  <h3>Research Areas</h3>
  <ul>
    {% for item in site.data.research %}
      <li>{{ item.area }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}


{% if site.data.skills %}
<div class="jumbotron">
  <h3>Skills</h3>
  <ul>
    {% for skill in site.data.skills %}
      <li>{{ skill.name }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}


{% if site.data.languages %}
<div class="jumbotron">
  <h3>Languages</h3>
  <ul>
    {% for lang in site.data.languages %}
      <li>{{ lang.language }} – {{ lang.level }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

<div class="jumbotron">
  <h3>Want to know more?</h3>
  <p>Learn more about my academic journey, interests, and research focus.</p>
  <a class="btn btn-primary btn-lg" href="about/" role="button">Go to About</a>
</div>
