---
layout: blog
categories: [blog, literature] 
date: 2015-05-11
comments: true
title: Sentiment in "War and Peace"
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
sentiment lexicon. (I'm using the Maude translation, which is
[available on Project Gutenberg][gb], to create these.)

In this first diagram, sentiment is summed for each **sentence** (there
are well over 20,000 sentences in the Maude translation!):

![Sentence-level sentiment totals in "War and Peace](/images/2015-05-11/WarAndPeace_nrc_sentence_600.png "Sentence-level sentiment totals in 'War and Peace'")

In this second diagram, sentiment is summed by **chapter** (there are
365 chapters!):

![Chapter-level sentiment totals in "War and Peace](/images/2015-05-11/WarAndPeace_nrc_chapter_600.png "Chapter-level sentiment totals in 'War and Peace'")

The visual differences between these two diagrams are striking, aren't
they? Find the "zero" value on the vertical axis and follow that point
across the diagram. Lots of sentences have a total sentiment in the
negative values, although it's hard to tell from this graph just how
many, but almost no chapters have a negative total sentiment. When
using the NRC lexicon to assign sentiment values, there are actually
9,204 sentences with positive sentiment (sum of word sentiments > 0)
and 4,802 sentences with negative sentiment (sum < 0). The rest of the
sentences have neutral sentiment (sum = 0).<sup>[1](#fn1)</sup>

What do these diagrams tell us about *War and Peace*? It's hard to
say. The Syuzhet package includes a `get_percentages()` function which
divides a text into one hundred chunks of equal size and plots mean
sentiment for each. For *War and Peace*, the resulting diagram looks
like this:

![Sentiment in "War and Peace" by percentage-based mean values](/images/2015-05-11/WarAndPeace_nrc_percentage_600.png "Sentiment in 'War and Peace' by percentage-based mean values")

I'll grant that comparing sentiment totals across all sentences in a
text (as shown in the first diagram above) isn't very revealing,
especially for a text containing as many sentences as *War and
Peace*. I'll also grant that dividing a text into one-percent chunks
represents a means of comparing texts of different lengths to one
another. But I don't like that we're ignoring chapter divisions when
we're exploring sentiment. Divisions of a text into chapters certainly
seem to fall under *syuzhet* rather than *fabula*. We shouldn't throw
them out when doing this sort of textual exploration.


### Notes

<a name="fn1">[1]</a>: Using the Bing lexicon (rather than the NRC
lexicon) to assign sentiment results in 6,213 sentences with a
negative total sentiment (sum < 0), and 6,236 sentences with a
positive total sentiment (sum > 0), with the rest having a neutral
total sentiment (sum = 0). The number of positive-sentiment sentences
and the number of negative sentiment-sentences is *almost exactly the
same*.

[syuzhetpackage]: http://www.matthewjockers.net/2015/02/02/syuzhet/
[gb]: http://www.gutenberg.org/ebooks/2600
