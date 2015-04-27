---
layout: blog
categories: [blog, literature] 
date: 2015-02-03
comments: true
title: Metonymy and Narrative Structure
---

William Croft's Radical Construction Grammar requires
only one syntactic structure to account for the complexity of the
world's languages: the part-whole relationship of grammatical
constructions. That's a bold claim, but the relationship between a
whole and its parts is even more powerful an explanatory force than
Croft makes it out to be.

Jerome Bruner's article "The Narrative Construction of Reality" is a
heady one. While it's likely true that any article purporting to
discuss the underpinnings of reality and the basic elements of human
existence is bound to be complicated, it should tell you something
about Bruner's that I made sense of it by explaining it to myself in
terms of computer programming languages.

Anyone who's studied literature a little has an understanding of some
of the basic building blocks of narrative: a story is a self-contained
narrative, a character is someone in a story, a plot is the series of
events that take place in a story, and so on. Understanding narratives
to this degree is like programming in Python.

Python is a high-level programming language, which makes it broadly
applicable. It's also famously human-readable. To display "Hello
World" on the screen, for instance (the usual first program one learns
in a new language), you simply type:

<script src="https://gist.github.com/menzenski/0b8d0e2ab7f08a864fc5.js"></script>

You can run Python on just about any computer without too
much difficulty, because in Python you don't have to worry about all the
particular ways a programming language interfaces with the computer
hardware it's installed on. In a sense, this makes it less powerful
than other programming languages, but not everyone needs all that
power. For many tasks, including linguistics-relevant tasks like
natural language processing and statistical computing, Python is
usually plenty powerful. Many people never come up against the limits
of what Python is capable of.

Likewise, many people are content to go through life discussing
"high-level literature". Indeed, entire university programs are
built around this sort of study, and entire academic careers are spent
discussing literature only from a high-level perspective, i.e., in
terms of authors and their decisions, readers and their
interpretations. All of these are worthwhile subjects, sure, but
they're also all *conscious*. There's a lot more to the literature
iceberg that's lurking below the surface, and that's the subject of
Bruner's article.

Bruner approaches narrative not from a high-level Python perspective,
but from a low-level Assembly perspective. He's less interested in the
sorts of things that authors and readers consciously put into and take
away from narratives, and more interested in the structures which
underlie those elements, which may not be used consciously by authors
and readers but are nevertheless fundamentally important to
narrative.

Remember that Python script above, and how simple it was to make
"Hello World" appear on screen? If I wanted to write a program in
Assembly language to display that same message on screen, here's how it
would look (sourced from
[Wikipedia](http://en.wikipedia.org/wiki/List_of_Hello_world_program_examples)): 

<script src="https://gist.github.com/menzenski/74dab45619ca69a00df3.js"></script>

Suddenly we realize that there's a lot of processing going on
behind-the-scenes in that Python example above. Assembly language
interfaces directly with hardware in a way that Python doesn't, which
is why this program is so much longer than its Python counterpart. We
need to specify everything very precisely—Assembly language allows us
to literally interface with the 1s and 0s of the computer's actual
machine language. 

### Back to narratives

The analogy between narratology and computer science is not a
perfect one, of course. In many ways, the two fields are moving in
different directions. Computers began as ordered sequences of 0s and
1s (that's really still what they are, even if we don't look that
deeply into their innards very often now), and higher-level
programming languages at their core are simply abstractions, taking
advantage of structures which have become conventionalized. In
narratology, and more broadly in all fields of inquiry concerning the
mind, we're starting at the other end of the process: we've already
got the high-level abstractions and conventions, and we're searching
for the 0s and 1s.

In his article, Bruner lays out ten elements of narrative which may in
one sense be considered those 0s and 1s, the fundamental building
blocks of narrative structure.

* **Narrative diachronicity:** narratives involve events occurring
  over time, and thus are fundamentally and irreducibly durative. 
* **Particularity:** a narrative must be embodied by specific
  participants and events, even though these particulars are
  frequently instantiations of a more general 'type'.
* **Intentional state entailment:** the intentionality and agency of
  the participants is crucial. Those events which are not intentional
  in their causes (acts of nature, etc.) play a role in narrative
  primarily by affecting the intentional state of the participants.
* **Hermeneutic composability:** a narrative and its comprehension as
  such depend on our ability to interpret knowledge. This interpretive
  ability is distinct from the modes of processing proposed by the
  rationalist and empiricist traditions.
* **Canonicity and breach:** A recounted, particular, diachronic
  sequence of events is necessary but non-sufficient to an
  understanding of narrative. A narrative requires a certain
  "worth-telling-about-ness".
* **Referentiality:** "Truth", in narrative, is judged by its
  verisimilitude rather than by its verifiability.
* **Genericness:** Genre is both a property of a given text and a way
  of comprehending narrative, a higher-order abstraction or
  conventionalization of universal (or near-universal) human plights.
* **Normativeness:** The driving force in narrative is a "breach" of
  convention or of norms.
* **Context sensitivity and negotiability:** Our ability to interpret
  narratives is in fact a much broader part of human cognition, and is
  more important a part of everyday life than might have been
  assumed. Our ability to understand and interpret narratives in
  context is also demonstrated in daily cultural negotiations.
* **Narrative accrual:** Just as words are added together to make
  sentences, and sentences to make narratives, so too do narratives
  accrue into larger units. These are called variously "cultures",
  "histories", or "traditions".

If some of these don't sound specific to narrative, that's part of the
point. We might call Bruner's view cognitive narratology: narratives
are not a fundamentally unique human creation, separate and distinct
from other means of conveying information; rather, they make use of
the same abilities, and are subject to the same constraints, as human
cognition more generally. In a cognitive approach to linguistics,
human language takes the forms it does because it constitutes an
interaction between such human abilities as pattern recognition,
memory, judgement/interpretation, abstraction and conventionalization,
etc. Those same cognitive abliities underlie the human narrative
ability as well.

(This post now has me wondering: can a computer program be a narrative?)
