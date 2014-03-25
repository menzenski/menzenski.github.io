---
layout: post
comments: true
title: Towards a Better List of Russian Stopwords
categories: [stopwords-project]
tags: [russian, nlp, python, 520]
fullview: true
---

In this post I'm going to take a look at some of the resources
available for Russian text analysis. Specifically, I'm interested in
*stop words*, those words which occur very frequently and which
contribute negligible meaning to a given text.

I've so far only been able to find two stop word lists for
Russian. The first is provided in the Natural Language Toolkit for the
Python programming language. Here's how to find this list if you've got
Python and the NLTK installed:

{% highlight python linenos %}
>>> from nltk.corpus import stopwords
>>> import codecs
>>> russian_stopwords = stopwords.words('russian')
>>> for word in russian_stopwords:
... print word.decode('utf8'),
...
"и в во не что он на я с со как а то все она так его но да ты к у же вы
за бы по только ее мне было вот от меня еще нет о из ему теперь когда
даже ну вдруг ли если уже или ни быть был него до вас нибудь опять уж
вам ведь там потом себя ничего ей может они тут где есть надо ней для
мы тебя их чем была сам чтоб без будто чего раз тоже себе под будет ж
тогда кто этот того потому этого какой совсем ним здесь этом один
почти мой тем чтобы нее сейчас были куда зачем всех никогда можно при
наконец два об другой хоть после над больше тот через эти нас про
всего них какая много разве три эту моя впрочем хорошо свою этой перед
иногда лучше чуть том нельзя такой им более всегда конечно всю между"
{% endhighlight %}

