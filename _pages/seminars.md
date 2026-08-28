---
permalink: /seminars/
title: "Seminars"
author_profile: true
---

All seminars below were held at Columbia University.

{% assign all_seminars = site.seminars | concat: site.data.external_seminars | sort: "term_start" | reverse %}
{% for s in all_seminars %}
- **[{{ s.short_title | default: s.title }}]({{ s.external_url | default: s.url | relative_url }})**{% if s.external_url %} &#8599;{% endif %} &mdash; {{ s.term }}{% if s.organizers %}, with {{ s.organizers }}{% endif %}
{% endfor %}
