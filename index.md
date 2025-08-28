---
title: Home
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

# {{ site.title }}

Hi, I’m Charley. I build machine learning systems with a focus on reliable, real-time deployment and measurable impact.

**Quick links:**  
- [About](/about/)  
- [Resume](/assets/docs/Charley_Sanchez_resume.pdf){:target="_blank"}

---

## Projects

<ul class="grid">
{% for p in site.data.projects %}
  <li class="card">
    {% if p.image %}
      <img src="{{ p.image | relative_url }}" alt="{{ p.title }}">
    {% endif %}
    <h3>{{ p.title }}</h3>
    <p>{{ p.description }}</p>
    {% if p.tech %}
      <p class="meta">{{ p.tech | join: ' · ' }}</p>
    {% endif %}
    <p class="links">
      {% if p.repo %}<a href="{{ p.repo }}" target="_blank">Code</a>{% endif %}
      {% if p.demo %}{% if p.repo %} · {% endif %}<a href="{{ p.demo }}" target="_blank">Demo</a>{% endif %}
      {% if p.paper %}{% if p.repo or p.demo %} · {% endif %}<a href="{{ p.paper }}" target="_blank">Paper</a>{% endif %}
    </p>
  </li>
{% endfor %}
</ul>
