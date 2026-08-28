---
permalink: /seminars/
title: "Seminars"
author_profile: true
---

I co-organize learning seminars in homotopy theory at Columbia. The Fall 2025 and Spring 2026 seminars are jointly maintained with Carlos Alvarado, so their schedules and abstracts live on [his site](https://alvarado-alvarez.github.io/) — the links below go there.

{% assign all_seminars = site.seminars | concat: site.data.external_seminars | sort: "term_start" | reverse %}
{% assign current_seminars = all_seminars | where_exp: "s", "s.current == true" %}

{% if current_seminars.size > 0 %}
## Current

{% for s in current_seminars %}
- **[{{ s.short_title | default: s.title }}]({{ s.external_url | default: s.url | relative_url }})**{% if s.external_url %} &#8599;{% endif %} &mdash; {{ s.term }}{% if s.sole %} (sole organizer){% elsif s.organizers %}, with {{ s.organizers }}{% endif %}
{% endfor %}

{% endif %}
## Past

{% for s in all_seminars %}
{% unless s.current == true %}
- **[{{ s.short_title | default: s.title }}]({{ s.external_url | default: s.url | relative_url }})**{% if s.external_url %} &#8599;{% endif %} &mdash; {{ s.term }}{% if s.sole %} (sole organizer){% elsif s.organizers %}, with {{ s.organizers }}{% endif %}
{% endunless %}
{% endfor %}
