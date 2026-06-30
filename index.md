---
layout: default
---

# Curriculum Vitae

## Experience

{% for job in site.experience %}
- **[{{ job.title }}]({{ job.url }})** — {{ job.organization }}, {{ job.location }}, {{ job.dates }}
{% endfor %}

[Edit experience](_experience/) | [Add entry](_experience/template.md)

---

## Education

{% for edu in site.education %}
- **[{{ edu.degree }}]({{ edu.url }})** — {{ edu.institution }}, {{ edu.location }}, {{ edu.dates }}
{% endfor %}

[Edit education](_education/) | [Add entry](_education/template.md)

---

## Research Publications

{% for pub in site.publications %}
- **[{{ pub.title }}]({{ pub.url }})** — {{ pub.venue }}, {{ pub.year }}
{% endfor %}

[Edit publications](_publications/) | [Add entry](_publications/template.md)

---

## Master's Thesis

{% for thesis in site.thesis %}
- **[{{ thesis.title }}]({{ thesis.url }})** — {{ thesis.institution }}, {{ thesis.year }}
{% endfor %}

[Edit thesis](_thesis/) | [Add entry](_thesis/template.md)

---

## Project Contributions

{% for project in site.projects %}
- **[{{ project.title }}]({{ project.url }})** — {{ project.role }}, {{ project.dates }}
{% endfor %}

[Edit projects](_projects/) | [Add entry](_projects/template.md)

---

## Miscellaneous

### Awards

{% for award in site.miscellaneous %}
{% if award.category == "award" %}
- **{{ award.title }}** — {{ award.organization }}, {{ award.year }}
{% endif %}
{% endfor %}

[Add award entry](_miscellaneous/template.md?category=award)

### Academic Activities

{% for activity in site.miscellaneous %}
{% if activity.category == "academic" %}
- **{{ activity.title }}** — {{ activity.role }}, {{ activity.year }}
{% endif %}
{% endfor %}

[Add academic activity entry](_miscellaneous/template.md?category=academic)

### Volunteering

{% for volunteer in site.miscellaneous %}
{% if volunteer.category == "volunteer" %}
- **{{ volunteer.title }}** — {{ volunteer.organization }}, {{ volunteer.year }}
{% endif %}
{% endfor %}

[Add volunteering entry](_miscellaneous/template.md?category=volunteer)

### Events Participation

{% for event in site.miscellaneous %}
{% if event.category == "event" %}
- **{{ event.title }}** — {{ event.event }}, {{ event.year }}
{% endif %}
{% endfor %}

[Add event entry](_miscellaneous/template.md?category=event)

### Speaker

{% for speak in site.miscellaneous %}
{% if speak.category == "speaker" %}
- **{{ speak.title }}** — {{ speak.event }}, {{ speak.year }}
{% endif %}
{% endfor %}

[Add speaker entry](_miscellaneous/template.md?category=speaker)

### Assorted Roles

{% for role in site.miscellaneous %}
{% if role.category == "role" %}
- **{{ role.title }}** — {{ role.organization }}, {{ role.year }}
{% endif %}
{% endfor %}

[Add role entry](_miscellaneous/template.md?category=role)

---

## Opinion Essays

{% for essay in site.opinion %}
- **[{{ essay.title }}]({{ essay.url }})** — {{ essay.date | date: "%B %Y" }}
{% endfor %}

[Edit essays](_opinion/) | [Add essay](_opinion/template.md)

---

[Edit this page on GitHub](https://github.com/sircocas/sircocas.github.io/edit/main/index.md) | [Add miscellaneous entry](_miscellaneous/template.md)