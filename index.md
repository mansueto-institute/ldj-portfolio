---
layout: default
---
<section class="intro">
  <h1>{{ site.unit_tagline }}</h1>
  <p class="lede">Write one or two sentences about what your unit does and who this portfolio is for. For example: "We partner with faculty and community organizations to turn research into practical tools."</p>
  <p><a class="button" href="{{ '/projects/' | relative_url }}">Browse all projects</a></p>
</section>

<h2>Featured projects</h2>
<ul class="project-grid">
  {% assign featured = site.projects | where: "featured", true %}
  {% for p in featured %}{% include project-card.html project=p %}{% endfor %}
</ul>
