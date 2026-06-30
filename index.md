---
layout: default
---

# Curriculum Vitae

## Experience

{% assign jobs = site.experience | sort: 'dates' | reverse %}
{% for job in jobs %}
- **{{ job.title }}** — {{ job.organization }}, {{ job.location }}, {{ job.dates }}
{% endfor %}

## Education

{% assign edu = site.education | sort: 'dates' | reverse %}
{% for edu in edu %}
- **{{ edu.degree }}** — {{ edu.institution }}, {{ edu.location }}, {{ edu.dates }}
{% endfor %}

## Research Publications

{% assign pubs = site.publications | sort: 'year' | reverse %}
{% for pub in pubs %}
{% if pub.pdf %}
- **[{{ pub.title }}]({{ pub.pdf }})** — {{ pub.venue }}, {{ pub.year }}
{% else %}
- **{{ pub.title }}** — {{ pub.venue }}, {{ pub.year }}
{% endif %}
{% endfor %}

## Theses

{% assign theses = site.thesis | sort: 'year' | reverse %}
{% for thesis in theses %}
- **[{{ thesis.title }}]({{ thesis.url }})** — {{ thesis.institution }}, {{ thesis.year }}
{% endfor %}

## Project Contributions

{% assign projects = site.projects | sort: 'dates' | reverse %}
{% for project in projects %}
- **{{ project.title }}** — {{ project.role }}, {{ project.dates }}
{% endfor %}

## Miscellaneous

{% assign misc = site.miscellaneous | sort: 'year' | reverse %}

### Awards

{% for item in misc %}
{% if item.category == "award" %}
- **{{ item.title }}** — {{ item.organization }}, {{ item.year }}
{% endif %}
{% endfor %}

### Academic Activities

{% for item in misc %}
{% if item.category == "academic" %}
- **{{ item.title }}** — {{ item.role }}, {{ item.year }}
{% endif %}
{% endfor %}

### Volunteering

{% for item in misc %}
{% if item.category == "volunteer" %}
- **{{ item.title }}** — {{ item.organization }}, {{ item.year }}
{% endif %}
{% endfor %}

### Events Participation

{% for item in misc %}
{% if item.category == "event" %}
{% if item.pdf %}
- **[{{ item.title }}]({{ item.pdf }})** — {{ item.event }}, {{ item.year }}
{% else %}
- **{{ item.title }}** — {{ item.event }}, {{ item.year }}
{% endif %}
{% endif %}
{% endfor %}

### Speaker

{% for item in misc %}
{% if item.category == "speaker" %}
{% if item.pdf %}
- **[{{ item.title }}]({{ item.pdf }})** — {{ item.event }}, {{ item.year }}
{% else %}
- **{{ item.title }}** — {{ item.event }}, {{ item.year }}
{% endif %}
{% endif %}
{% endfor %}

### Assorted Roles

{% for item in misc %}
{% if item.category == "role" %}
- **{{ item.title }}** — {{ item.organization }}, {{ item.year }}
{% endif %}
{% endfor %}
