+++
title = "My Experience with Programming Languages"
date = "2018-04-02"
categories = ["Software"]
+++

I keep seeing comic strips classifying programming languages. They're unavoidably offensive, because it's impossible to say anything about a programming language without offending the language's users. Which makes sense, because you can't help but get emotionally attached to the thing you've been using for years to weave your dreams. It's also super fun to be hyper-critical about programming languages to the point of inaccuracy. All programmers have been wronged by their language of choice or found themselves in the depths of debugging hell with a foreign language. How can you *not* resonate with criticism reflecting your pain?

Throwing out all that prior consideration and thoughtfulness, here's my experience with programming languages in no particular order.

## Assembly

What everything compiles to. Unless it's running on a virtual machine (like the one for Java or Erlang), but even then, every language bottoms out at assembly. The worst experience ever if you don't have any tooling.

## Web Assembly

Because web browsers are virtual machines now, so they need their own assembly language.

## Fortran

Super old language. Still used for writing math libraries and physics simulations that must run as fast as possible.

## C

Successor to Fortran. Runs on damn near everything. It's what wrote the code for the microprocessors in your car, airplane and your hearing aid.

## COBOL

Business successor to C. Runs most of the world's banking, insurance and accounting software on hardware. Makes you throw out everything you thought you knew about computers, which means consultants who write this language make tons of money.

## C++

Successor to C allowing for Object Oriented Programming, templates and other more questionable features. The foundation for many essential systems and the cause of [much anguish](https://twitter.com/i/events/1226639307710095360).

## LISP

Let's people define their own domain specific languages. In theory, extremely powerful. In practice, makes reading someone else's code extremely painful. I don't trust anyone's opinion on it, unless they've also written a large program in OCaml.

## OCaml

One of the original functional languages. Some people at Facebook are so excited about it, they're using it for everything.

## Rust

Saw the code people were writing in C/C++ and decided to make it easier to write parallel code without breaking things. Equivalent to sun breaking through the clouds after 40 days of rain for many C++ systems developers.

## Zig

An alternative to C, created by eliminating all the horrible parts of C (pre-processor, ridiculous build tools, awkward memory deallocation). Aims for the niche where [C is needed, but Rust is too complicated](https://www.youtube.com/watch?v=eCHM8-_poZY). Created by a person so convinced they could make a better alternative, that they [quit their job and live off donations](https://www.patreon.com/andrewrk).

## Java

Saw the code people were writing in C/C++ and tried to bring them closer to Smalltalk. Also, wanted to stop people doing evil things like redifining False to 1. Now synonymous with boring business systems and obtuse descriptions of simple concepts.

## Go

Google’s alternative to Java and C++. Compiles fast and runs fast, while maintaining [utter contempt](https://twitter.com/16kbps/status/1195081752659865615?s=20) for developer's ability to learn new skills.

## Basic

First programming language of many elder programmers because it shipped with a bunch of old computer systems and it was easy to modify games with it.

## Logo

Seymour Papert's attempt at a language for children.

## Smalltalk

Alan Kay's attempt at a language for children.

## Quorum

Academia's attempt at an evidence-based language for everyone.

## Scala

When functional programming people have to work with Java people.

## Clojure

When LISP people have to work with Java people.

## C\#

Microsoft's response to Java and C++. Jeff Atwood loves it.

## Objective-C

Apple's response to C++. No one loves it.

## Swift

Apple's apology for Objective-C.

## Kotlin

Jetbrain's apology for Google making everyone write Android apps using Java.

## VisualBasic

Microsoft's idea of a high level scripting language. Mostly found in Excel macros. Visual Basic 6 came with a delightful IDE that allowed you to make windows-looking apps in seconds. It died...

## Haskell

The language for lovers of pure functions and complicated types. Writing it feels like doing math.

## F\#

Microsoft's idea of a functional language.

## Purescript

Haskell, but for building Web pages, instead of proving theorems.

## Elm

Wait, this is Haskell for building web pages? Ugh, whatever. The language that helped me "get" functional programming, because it let me make a gosh darned web-page instead of contemplating the innate beauty of binary trees.

## Matlab

The original engineering/science language. Unparalleled at creating systems I have no experience with. Horrible for creating a bunch of systems I do have experience with. A bunch of tools are written in this, so it's still used today in various fields. Great for starting language wars between scientists.

## Julia

The language scientists should be using today. Fast, understandable and debuggable. The community used to be [filled with jerks](https://danluu.com/julialang/), but have calmed down now and are very friendly.

## Wolfram

A refined Matlab I've never used.

## Tcl

Supposed to be a higher level alternative to C. Mostly extinct, but lives on embedded in various applications. Last time I saw it was the testing scripts of a telecom company.

## Perl

Wanted an expressive way to do things quickly, but ended up ugly as hell. There's a new version, but I don't trust it.

## PHP

Designed to help C programmers make web pages. Has slowly gotten better over the years, but still hurts my eyes.

## Hack

An attempt to put typing into PHP by Facebook to make it faster. Hated by many.

## Lua

Keeps popping up where I don't expect it, like Game Dev and Deep Learning, since it's an easily embeddable language. Has a JIT so beautiful it makes readers weep.

## Erlang

Used by telecom companies and people with super hardcore distributed systems to maintain. Where the Actor model of concurrency comes from.

## Ruby

Syntactic sugar taken to its conceptual extreme. Adored by the Japanese. Has this thing called meta-programming, which I've never had a need to use, but allowed for the creation of Ruby on Rails which people still swear by for creating websites that need to access and modify a database.

## Crystal

Statically typed, compiled language for Ruby programmers. Because making Ruby fast is so difficult, you sometimes need to write a whole new language.

## Elixir

Created by a Ruby-lover who wanted to use Erlang's BEAM VM with a modern functional language. The new hottest language for building a website.

## Python

Decided from the beginning to be as understandable as possible. Consequently, has libraries for damn near everything (Deep Learning, scientific computation, statistics, making visual novels... etc). People like to argue about v2 vs. v3, but it's never been a problem for me.

## Nim

Statically typed, compiled language for Python programmers. Because [making Python fast is so difficult]({{< ref "2020-02-09-Faster-Python.md" >}}), you sometimes need to write a whole new language.

## R

A language designed for statisticians. Great for starting fights between stats nerds by [comparing it to smoking](https://www.johndcook.com/blog/2012/02/29/comparing-r-to-smoking/).

## JavaScript

The only thing running on the Web for years now, so people have been working really hard to nurture it from its awkward beginnings into a mature language. They have seen moderate success in this endeavour over the last few years. Has started running on servers too, because people hate having to know two languages.

## TypeScript

Not technically a language, but adds types to JavaScript. This enhances IDE use and reduces the number of errors so drastically it feels like a new language. Made me realise I didn't hate static typing, I just hated C++.

## Bash

Glues a bunch of shell tools together. Occasionally abused to create large-scale programs.

## PowerShell

An object oriented (returns objects instead of the Unix text-streams approach) and API-focused shell language from Microsoft. Mainly praised/derided for not being Bash.

## TLA+

Some next-level systems design language I don't understand how to use properly. Tried working through Hillel's book about it, but got lost. I would someday like to learn how it's related to Alloy.

## AutoHotkey

Language for automating tasks using keyboard shortcuts on Windows. No equivalent on Linux, because the Windows Manager ecosystem is too fragmented.

## Nock/Hoon

Neo-reactionary language that [lets you turn political enemies into unpersons](https://www.popehat.com/2013/12/06/nock-hoon-etc-for-non-vulcans-why-urbit-matters/).

## Notes

- It's pretty funny/sad how everyone keeps trying to get away from C++ and it keeps dragging them back. To its credit, the language does keep updating, but it's similar how an amorphous ooze monster absorbing another house is an update.
