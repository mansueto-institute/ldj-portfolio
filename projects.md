---
layout: default
title: Projects
permalink: /projects/
---
<h1 class="page-heading">Projects</h1>
<p class="lede">A short sentence introducing the full list of projects.</p>

<ul class="project-grid">
  {% assign projects = site.projects | sort: "year" | reverse %}
  {% for p in projects %}{% include project-card.html project=p %}{% endfor %}
</ul>
