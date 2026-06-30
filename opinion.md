---
layout: default
title: Opinion Essays
---

# Opinion Essays

{% for essay in site.opinion %}
- **[{{ essay.title }}]({{ essay.url }})** — {{ essay.date | date: "%B %Y" }}
{% endfor %}
