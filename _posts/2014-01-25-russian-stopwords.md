---
layout: post
comments: true
title: Russian Stopwords
categories: [stopwords-project]
tags: [russian, nlp, python, 520]
fullview: true
---

#### What are stop words and why should you care?

One issue that's come up for me in trying to analyze Russian text is the lack of a good list of stop words. Stop words are (according to [Wikipedia](http://en.wikipedia.org/wiki/Stop_words)) "which are filtered out prior to, or after, processing of natural language data (text)". Stop words are defined differently in different contexts, but typically include high-frequency 'function words'. In English, words like *a*, *the*, *of*, *in*, *that*, etc. are included in a stop words list.

There are several reasons why it's useful to remove stop words from a text prior to analyzing it. Perhaps you want to look at the words which occur most frequently. Stopwords typically are the most frequent in any text, and so removing them 


#### The difference that removal of stop words can make

The following picture shows the fifty most frequent words (with their frequencies) from the 2013 State of the Union address (the text of which is available [here](http://www.whitehouse.gov/the-press-office/2013/02/12/remarks-president-state-union-address)). In this first picture, no stopwords have been removed from the text prior to the creation of the tag cloud:

![Most common words in the 2013 State of the Union address]({% asset_path stopwords_not_removed.png %})

This next image shows the fifty most frequent words from the same 2013 State of the Union address, except that 174 stop words were removed prior to the creation of the tag cloud (the list of stop words used is available [here](http://www.ranks.nl/resources/stopwords.html)):

![Most common words in the 2013 State of the Union address, with stop words removed]({% asset_path stopwords_removed.png %})
