---
layout: blog
categories: [blog, literature] 
date: 2015-05-11
comments: true
title: Sentiment in "War and Peace", Part I
---

I've been having a lot of fun playing around with Matthew Jockers'
[*Syuzhet* package for R][syuzhetpackage] recently. There's been a lot
of discussion about Syuzhet on blogs and on Twitter since Jockers
released it in February, and I thought I'd add some of my own thoughts
here.

I've been using Syuzhet to explore sentiment in some translations of
classic Russian novels (the topic of Syuzhet in translated works is
one I plan to explore in a later post), and some interesting things
have emerged. "The Russian Novel" has a reputation, at least among my
generation, as being depressing but there's nevertheless many more
words with positive sentiment than negative.

Both of the following diagrams show the sentiment totals in Leo
Tolstoy's "War and Peace", with sentiment assigned using the NRC
sentiment lexicon. (I'm using the Maude translation
[available on Project Gutenberg][gb] to create these.)

In this first diagram, sentiment is summed for each **sentence** (there
are more than 27,000 sentences in the Maude translation!):

![Sentence-level sentiment totals in "War and Peace](/images/2015-05-11/WarAndPeace_nrc_sentence_600.png "Sentence-level sentiment totals in 'War and Peace'")

In the second diagram, sentiment is summed by **chapter**:

![Chapter-level sentiment totals in "War and Peace](/images/2015-05-11/WarAndPeace_nrc_chapter_600.png "Chapter-level sentiment totals in 'War and Peace'")

The visual differences between these two diagrams are striking, aren't
they? Find the "zero" value on the vertical axis and follow that point
across the diagram. Lots of sentences have a total sentiment in the
negative values, although it's hard to tell from this graph just how
many, but almost no chapters have a negative total sentiment.

When I crunched the numbers, the picture gets much more
interesting. There are 6,213 sentences with a negative total sentiment
(sum < 0), and 6,236 sentences with a positive total sentiment (sum >
0), with the rest having a neutral total sentiment (sum = 0). The
number of positive-sentiment sentences and the number of negative
sentiment-sentences is *almost exactly the same*.

[syuzhetpackage]: http://www.matthewjockers.net/2015/02/02/syuzhet/
[gb]: http://www.gutenberg.org/ebooks/2600
