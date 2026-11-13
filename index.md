---
layout: default
---
<header class="intro">
  <h1>{{ site.title }}</h1>
  <p class="lede">The Local Data Journalism Initiative establishes partnerships between news organizations and university data science teams using the highest caliber data science and artificial intelligence tools and methodologies. This gallery highlights our published projects and provides links to see the work yourself.</p>
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
