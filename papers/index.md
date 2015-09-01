---
layout: page
title: Papers
tags: [research]
modified: 2015-09-01
comments: true
image:
  feature: header_image_code2.png
  credit: Matt Menzenski (licensed CC-BY-4.0)
  creditlink: http://www.menzenski.com
---

On this page you'll find links to papers I've written. Unless
otherwise indicated, all materials found on
this page are released under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc].

## Conference Presentations

-----

{% for paper in site.data.conferencepapers %}

#### [{{ paper.name }}]({{ paper.location }})

{{ paper.date | date: '%B %d, %Y' }}: {{ paper.description }}

### Abstract

> {{ paper.abstract }}

{% endfor %}

## Undergraduate Thesis

-----

\* *coming soon* \*

## Seminar Papers

-----

\* *coming soon* \*


[cc]: https://creativecommons.org/licenses/by-sa/4.0/
