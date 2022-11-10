---
title: Teaching
layout: default
permalink: /teaching/
published: true
---

<div class="TeachingContainer">

	<div class="gallery">


  {% for teaching in site.teaching %}

  {% if teaching.redirect %}
  <div class="teachingTile">
          <a href="{{ teaching.redirect }}" target="_blank">
          <span>
              <h2>{{ teaching.title }}</h2>
              <br/>
              <p>{{ teaching.description }}</p>
          </span>
          </a>
  </div>

  {% else %}

  <div class="teachingTile">
          <a href="{{ teaching.url | prepend: site.baseurl | prepend: site.url }}">
          <span>
              <h2>{{ teaching.title }}</h2>
              <br/>
              <p>{{ teaching.description }}</p>
          </span>
          </a>
  </div>

  {% endif %}

  {% endfor %}

	</div>

</div>
