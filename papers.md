---
layout: frontpage
title: Papers
---

## Conference Presentations

{% for paper in site.data.conferencepapers %}

#### {{ paper.name }}

-----

[{{ paper.name }}]({{ paper.location }})

{{ paper.date | date: '%B %d, %Y' }}: {{ paper.description }}

### Abstract

> {{ paper.abstract }}

{% endfor %}


