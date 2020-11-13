---
layout: default
---

# Meeting Minutes
{: .no_toc}

* TOC
{:toc}


{% assign yearly_minutes = site.minutes | group_by_exp: "item", "item.date | date: '%Y'" %}

## Regular WG call and F2F minutes

{% for year in yearly_minutes reversed %}

### {{ year.name }}

<ul>
{% for item in year.items reversed %}
  {% unless item.url contains "epub-a11y"  %}
      <li><a href="{{ site.baseurl }}{{ item.url }}"><em>{{ item.title }}</em></a></li>
  {% endunless %}
{% endfor %}
</ul>

{% endfor %}

## Accessibility Task Force minutes

{% for year in yearly_minutes reversed %}

### {{ year.name }}

<ul>
{% for item in year.items reversed %}
  {% if item.url contains "epub-a11y"  %}
      <li><a href="{{ site.baseurl }}{{ item.url }}"><em>{{ item.title }}</em></a></li>
  {% endif %}
{% endfor %}
</ul>

{% endfor %}

