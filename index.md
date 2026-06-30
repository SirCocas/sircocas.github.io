---
layout: default
---

# Curriculum Vitae

## Experience

{% for job in site.experience %}
- **[{{ job.title }}]({{ job.url }})** — {{ job.organization }}, {{ job.location }}, {{ job.dates }}
{% endfor %}

## Education

{% for edu in site.education %}
- **[{{ edu.degree }}]({{ edu.url }})** — {{ edu.institution }}, {{ edu.location }}, {{ edu.dates }}
{% endfor %}

## Research Publications

{% for pub in site.publications %}
- **[{{ pub.title }}]({{ pub.url }})** — {{ pub.venue }}, {{ pub.year }}
{% endfor %}

## Master's Thesis

{% for thesis in site.thesis %}
- **[{{ thesis.title }}]({{ thesis.url }})** — {{ thesis.institution }}, {{ thesis.year }}
{% endfor %}

## Project Contributions

{% for project in site.projects %}
- **[{{ project.title }}]({{ project.url }})** — {{ project.role }}, {{ project.dates }}
{% endfor %}

## Miscellaneous

### Awards

{% for award in site.miscellaneous %}
{% if award.category == "award" %}
- **{{ award.title }}** — {{ award.organization }}, {{ award.year }}
{% endif %}
{% endfor %}

### Academic Activities

{% for activity in site.miscellaneous %}
{% if activity.category == "academic" %}
- **{{ activity.title }}** — {{ activity.role }}, {{ activity.year }}
{% endif %}
{% endfor %}

### Volunteering

{% for volunteer in site.miscellaneous %}
{% if volunteer.category == "volunteer" %}
- **{{ volunteer.title }}** — {{ volunteer.organization }}, {{ volunteer.year }}
{% endif %}
{% endfor %}

### Events Participation

{% for event in site.miscellaneous %}
{% if event.category == "event" %}
- **{{ event.title }}** — {{ event.event }}, {{ event.year }}
{% endif %}
{% endfor %}

### Speaker

{% for speak in site.miscellaneous %}
{% if speak.category == "speaker" %}
- **{{ speak.title }}** — {{ speak.event }}, {{ speak.year }}
{% endif %}
{% endfor %}

### Assorted Roles

{% for role in site.miscellaneous %}
{% if role.category == "role" %}
- **{{ role.title }}** — {{ role.organization }}, {{ role.year }}
{% endif %}
{% endfor %}

## Opinion Essays

{% for essay in site.opinion %}
- **[{{ essay.title }}]({{ essay.url }})** — {{ essay.date | date: "%B %Y" }}
{% endfor %}