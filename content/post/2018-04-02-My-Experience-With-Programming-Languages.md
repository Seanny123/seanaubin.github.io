+++
title = "My Experience with Programming Languages"
date = "2018-04-02"
categories = ["Software"]
draft = true
+++

I keep seeing comic strips classifying programming languages. They're intentionally offensive, because it's impossible to say anything about a programming language without offending the language's users. Which makes sense, because you can't help but get emotionally attached to the thing you've been using for years to weave your dreams. So, throwing out all that prior consideration, here's my experience with programming languages.

## Assembly

What everything compiles to. Unless it's running on a virtual machine (like the one for Java or Erlang), but even then, every language bottoms out at assembly. The worst experience ever if you don't have any tooling.

## Web Assembly

Because web browsers are virtual machines now, so they need their own assembly language.

## Fortran

Super old language. Still used for writing math libraries and physics simulations that must run as fast as possible.

## C

Successor to Fortran. Runs on damn near everything. It's what's probably running in your car, airplane and your hearing aid.

## COBOL

Business successor to C. Runs most of the world's banking, insurance and accounting software on hardware that makes you throw out everything you thought you knew about computers, which means consultants who write this language make tons of money.

## RPG

The pre-cursor to COBOL. If seen in the wild, be afraid. Be VERY afraid.

## C++

Successor to C allowing for Object Oriented Programming and templates. The foundation for many foundational systems.

## Rust

Saw the code people were writing in C/C++ and decided to make it easier to write parallel code without breaking things. Equivalent to sun breaking through the clouds after 40 days of rain for many C++ systems developpers.

## Java

Saw the code people were writing in C/C++ and bring them closer to Smalltalk. Also, wanted to stop people doing evil things like redifining False to 1. Now synonymous with boring business systems.

## Go

Google’s response to Java and C++. Compiles fast and runs fast, while still being pretty easy for a programmer to write.

## Basic

First programming language of many elder programmers because it shipped with a bunch of old computer systems and it was easy to modify games with it.

## Logo

Seymour Papert's attempt at a language for children.

## Smalltalk

Alan Kay's attempt at a language for children.

## Quorum

Academia's attempt at an evidence-based language for everyone.

## Scala

When people who do functional programming have to work with Java people.

## C\#

Microsoft's response to Java and C++. Jeff Atwood loves it.

## Objective-C

Apple's response to C++. No one loves it.

## Swift

Apple's apology for Objective-C.

## Kotlin

The alternative to Java, when you still need your code to run on Android.

## VisualBasic

Microsoft's idea of a high level scripting language. Mostly found in Excel macros.

## LISP

Apparently amazing, but I don't have a high enough IQ to use it. Let's people define their own domain specific languages. In theory, extremely powerful. In practice, makes reading someone else's code extremely painful. The modern manifestation of this is Clojure.

## Haskell

Supppsed to be even more amazing than LISP, but with an equivalently high learning curve. Writing it feels like doing math.

## F\#

Microsoft's idea of a functional language.

## Idris

Apparently even more amazing than Haskell for weird typing reasons I don't understand.

## Elm

Haskell, but for building Web pages.

## Purescript

Wait, this is Haskell for building web pages? Ugh. Whatever.

## Ocaml

One of the original functional languages. Some people at Facebook are so excited about it, they're using it for everything.

## Matlab

The original engineering/science language. Unparalleled at creating systems I have no experience with. A bunch of tools are written in this, so it's still used today in various fields. Great for starting language wars between scientists.

## Julia

The language scientists should be using today. Fast, understandable and debuggable. The community used to be [filled with jerks](https://danluu.com/julialang/), but [have calmed down now](https://twitter.com/voyageur_techno/status/938490814522572801)?

## Wolfram

A refined Matlab I've never used.

## Tcl

Supposed to be a higher level alternative to C. Mostly extinct. Last time I saw it was the testing scripts of a telecom company.

## Perl

Wanted an expressive way to do things quickly, but ended up ugly as hell. There's a new version, but I don't trust it.

## Lua

Keeps popping up where I don't expect it, like Game dev and Deep Learning. Has a JIT so beautiful it makes readers weep.

## PHP

Designed to help C programmers make web pages. Has slowly gotten better over the years, but still hurts my eyes.

## Hack

An attempt to put typing into PHP by Facebook to make it faster. Hated by many.

## Ruby

Syntactic sugar taken to its conceptual extreme. Adored by the Japanese. Has this thing called meta-programming, which I've never had a need to use, but allowed for the creation of Ruby on Rails which people still swear by for creating websites that need to access and modify a database.

## Python

Decided from the beginning to be as understandable as possible. Consequently, has ## libraries for damn near everything (Deep Learning, scientific computation, statistics, making visual novels... etc). People like to argue about v2 vs. v3, but it's never been a problem for me.

## R

A language designed for statisticians. People move between R and Python all the time. ## Great for starting fights between stats nerds by [comparing it to smoking](https://www.johndcook.com/blog/2012/02/29/comparing-r-to-smoking/)

## JavaScript

it's the only running on the Web for years now, so people have been working really hard to nurture it from its awkward beginnings into a mature language. They have seen moderate success in this endeavour over the last few years. Has started running on servers too, because people hate having to know two languages.

## TypeScript

not technically a language, but adds types to JavaScript which makes it possible to use with an IDE and reduces the number of errors so drastically that I feel it should be mentioned. Made me realise I didn't hate static typing, I just hated C++.

## Erlang/Elixir

Used by telecom companies and people with super hardcore distributed systems to maintain. Where the Actor model of concurrency comes from.

## Bash

Lets you glue a bunch of powerful shell tools together. Occasionally abused to create large-scale programs.

## PowerShell

An object oriented shell language from Microsoft. Mainly praised/derided for not being Bash.

## TLA+

Some next-level systems design language I don't understand how to use properly. Currently waiting for [Hillel Wayne](https://hillelwayne.com/) to finish writing his book about it.

## Nock/Hoon

Neo-reactionary language that [lets you turn political enemies into unpersons](https://www.popehat.com/2013/12/06/nock-hoon-etc-for-non-vulcans-why-urbit-matters/)

## Notes

- [Nobody actually knows what a functional language is](https://twitter.com/Hillelogram/status/962452705280233472?ref_src=twcamp%5Eshare%7Ctwsrc%5Em5%7Ctwgr%5Eemail%7Ctwcon%5E7046%7Ctwterm%5E1)
- The trade-off between compiled and interpreted languages is [constantly fluctuating](http://jamie-wong.com/bending-the-pl-curve/) 
- It's pretty funny/sad how everyone keeps trying to get away from C++ and it keeps dragging them back. To its credit, the language does keep updating, but it's similar how an amorphous ooze monster absorbing another house is an update.
- No one is sure what programming language to teach first, but it probably isn't C/C++ or Java given [this research](https://quorumlanguage.com/evidence.html).
- Everyone is trying to make their language easier to visualize. Turns out, it's super hard. A lot of people think it requires designing totally new languages/interfaces. For an overview of these attempts, see [this slideshow](https://docs.google.com/presentation/d/1MD-CgzODFWzdpnYXr8bEgysfDmb8PDV6iCAjH5JIvaI/edit?usp=sharing).
- The biggest leaps in languages come from taking ideas from extensive research. This is really hard to do correctly. Look at [this blog post](https://graydon2.dreamwidth.org/253769.html) summarizing cool things around the corner for more info.
