---
layout: frontpage
title: Papers
---

# Papers

On this page you'll find links to papers I've written. Unless
otherwise indicated, all materials found on
this page are released under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc]. 

## Conference Presentations

{% for paper in site.data.conferencepapers %}

-----

#### [{{ paper.name }}]({{ paper.location }})

{{ paper.date | date: '%B %d, %Y' }}: {{ paper.description }}

### Abstract

> {{ paper.abstract }}

{% endfor %}

## Undergraduate Thesis

\* *coming soon* \*

## Seminar Papers

\* *coming soon* \*


[cc]: https://creativecommons.org/licenses/by-sa/4.0/
