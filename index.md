---
layout: default
---

# Curriculum Vitae

## Experience

{% assign jobs = site.experience | sort: 'year' | reverse %}
{% for job in jobs %}
- **{{ job.title }}** — {{ job.organization }}, {{ job.location }}, {{ job.dates }}
{% if job.description %}
**Main focus:** {{job.description}}

{% endif %}
{% endfor %}

## Education

{% assign edu = site.education | sort: 'year' | reverse %}
{% for edu in edu %}
{% if edu.degree %}
- **{{ edu.degree }}** — {{ edu.institution }}, {{ edu.location }}, {{ edu.dates }}
{% if edu.thesis %}
**Thesis title:** {{edu.thesis}}

{% endif %}
{% endif %}
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



## Project Contributions

{% assign projects = site.projects | sort: 'year' | reverse %}
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
