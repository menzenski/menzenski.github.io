---
layout: post
comments: true
title: Automating the Creation of a Tohono O'odham Verb Database
categories: [oodham-aspect]
tags: [nlp, python, oodham, aspect]
fullview: true
---

#### To do corpus linguistics, first you need a corpus

In a field methods class last year, I was struck by seeming
similarities between verbal aspect in Russian and verbal aspect in
Tohono O'odham (an Uto-Aztecan language spoken in what is today
southern Arizona and northern Sonora, Mexico). Both languages utilize
a basic distinction between the perfective and imperfective aspect,


Here's a sample entry from Mathiot's dictionary, just so you can see
what I'm starting with:

> **baañiop** Vintr pls (for sgs see **baañimeḑ**)
> [Neutr: def baañio; hort and indef baañiop. Correl: baañiop-k; immed: baañiop-ka-'i]:
> to crawl on all fours (same as **baabañimeḑ**) ex: Mt o 'i baañio miisa
> veco! (You pl will) crawl under the table! -- M(<'am) g o 'i baañiop
> kolai veco! (You pl) crawl under the fence!-- 'Idam 'o cum hekid abx
> baañiop. These crawl on all fours all the time. -- M g o 'i baañiopk
> 'am o ho(<ha)'ui. (You pl) crawl there and get them!

Not very intuitive, is it? There's a lot of information packed into
this dictionary entry. The Python script I'm working on needs to be
able to pull several pieces of information from an entry like this,
and convert it into a form that lends itself more easily to
organization in a spreadsheet or database.

1. Identify and separate dictionary entries for verbs from other
   entries.
2. Determine the general semantic class of the verb (intransitive,
   here).
3. Identify the given forms of the verb (e.g., Correlative:
   baañiop-k).
4. Identify the verb's definition.
5. (Perhaps) collect any example sentences given.
