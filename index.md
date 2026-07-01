---
layout: default
---

# Curriculum Vitae

## About

<div class="about">
  <div class="about-photo">
    <img src="{{ '/assets/img/headshot.jpg' | relative_url }}" alt="Headshot">
  </div>
  <div class="about-text">
    <p>
      Add a short bio here. Keep it concise — two or three lines about your research interests, background, and current focus.
    </p>
    <div class="social-links">
      <a href="https://www.linkedin.com/in/YOUR_PROFILE/" target="_blank" rel="noopener" aria-label="LinkedIn">
        <svg viewBox="0 0 24 24" width="20" height="20" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
      </a>
      <a href="https://scholar.google.com/citations?user=YOUR_ID" target="_blank" rel="noopener" aria-label="Google Scholar">
        <svg viewBox="0 0 24 24" width="20" height="20" fill="currentColor"><path d="M12 24a7 7 0 1 1 0-14 7 7 0 0 1 0 14zm0-24L0 9.5l4.838 3.94A8 8 0 0 1 12 9a8 8 0 0 1 7.162 4.44L24 9.5z"/></svg>
      </a>
      <a href="https://www.scopus.com/authid/detail.uri?authorId=YOUR_ID" target="_blank" rel="noopener" aria-label="Scopus">
        <svg viewBox="0 0 24 24" width="20" height="20" fill="currentColor"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
      </a>
    </div>
  </div>
</div>

---

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
