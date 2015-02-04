---
layout: post-light-feature
title: Metonymy and Narrative Structure
description: "William Croft's Radical Construction Grammar requires
only one syntactic structure to account for the complexity of the
world's languages: the part-whole relationship of grammatical
constructions. That's a bold claim, but the relationship between a
whole and its parts is even more powerful an explanatory force than
Croft makes it out to be."
categories: [blog, literature, narratology] 
date: 2015-02-03
comments: true
image: 
        feature: typewriter.jpg
---


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

```Python
print "Hello World"
```

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
Assembly language to display the same message on screen, here's how it
would look (sourced from
[Wikipedia](http://en.wikipedia.org/wiki/List_of_Hello_world_program_examples)): 

```Assembly
; MacOS X: /usr/local/bin/nasm -f macho64 *.s && ld -macosx_version_min 10.7 *.o
; Solaris/FreeBSD/DragonFly: nasm -f elf64 -D UNIX *.s && ld *.o
; NetBSD: nasm -f elf64 -D UNIX -D NetBSD *.s && ld *.o
; OpenBSD: nasm -f elf64 -D UNIX -D OpenBSD *.s && ld -static *.o
; OpenIndiana: nasm -f elf64 -D UNIX *.s && ld -m elf_x86_64 *.o
; Linux: nasm -f elf64 *.s && ld *.o
 
%ifdef  NetBSD
section .note.netbsd.ident
        dd      7,4,1
        db      "NetBSD",0,0
        dd      200000000       ; amd64 supported since 2.0
%endif
 
%ifdef  OpenBSD
section .note.openbsd.ident
        align   2
        dd      8,4,1
        db      "OpenBSD",0
        dd      0
        align   2
%endif
 
section .text
 
%ifidn __OUTPUT_FORMAT__, macho64       ; MacOS X
        %define SYS_exit        0x2000001
        %define SYS_write       0x2000004
 
        global  start
        start:
%elifidn __OUTPUT_FORMAT__, elf64
        %ifdef  UNIX            ; Solaris/OI/FreeBSD/NetBSD/OpenBSD/DragonFly
                %define SYS_exit        1
                %define SYS_write       4
        %else                   ; Linux
                %define SYS_exit        60
                %define SYS_write       1
        %endif
 
        global  _start
        _start:
%else
        %error  "Unsupported platform"
%endif
 
        mov     rax,SYS_write
        mov     rdi,1           ; stdout
        mov     rsi,msg
        mov     rdx,len
        syscall
        mov     rax,SYS_exit
        xor     rdi,rdi         ; exit code 0
        syscall
 
section .data
 
msg     db      "Hello, world!",10
len     equ     $-msg
```
