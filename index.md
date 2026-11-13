---
layout: default
---
<header class="intro">
  <h1>{{ site.title }}</h1>
  <p class="lede">Write a short introduction here: what this portfolio is, who made the work, and who it's for. Two or three sentences is plenty.</p>
  <p>You can add a second paragraph if you need one, for example to explain how projects are chosen or how to get in touch.</p>
</header>

<ol class="project-list">
{% assign projects = site.projects | sort: "order" %}
{% for p in projects %}
  <li class="project">
    <h2>{{ p.title }}</h2>
    {% if p.year or p.status or p.team %}
      <p class="project-meta">
        {%- if p.year -%}{{ p.year }}{%- endif -%}
        {%- if p.status -%}{% if p.year %}, {% endif %}{{ p.status }}{%- endif -%}
        {%- if p.team -%}<br>{{ p.team }}{%- endif -%}
      </p>
    {% endif %}

    {% if p.images %}
      <div class="project-images{% if p.images.size > 1 %} project-images--many{% endif %}">
        {% for img in p.images %}
          <figure>
            <img src="{{ img.src | relative_url }}" alt="{{ img.alt }}" loading="lazy">
            {% if img.caption %}<figcaption>{{ img.caption }}</figcaption>{% endif %}
          </figure>
        {% endfor %}
      </div>
    {% endif %}

    <div class="project-text">{{ p.content | markdownify }}</div>

    {% if p.links %}
      <ul class="link-list">
        {% for l in p.links %}<li><a href="{{ l.url }}">{{ l.label }}</a></li>{% endfor %}
      </ul>
    {% endif %}
  </li>
{% endfor %}
</ol>
