+++
title = "Eternal Conceptual Disagreements in Programming Languages"
date = "2020-02-09"
categories = ["Programming", "Software"]
draft=true
+++

Differentiating concrete concepts from vague categories is an essential step to mastering a domain of knowledge. This took me years in Computer Science, because practitioners are more likely to argue in a circular manner, rather than participate in an adversarial collaboration. Thus, for all the noobs out there, here is a list of unanswerable questions, to either steer clear of or to dive into. But at the very least, you should know that if someone claims to have an ultimate answer to any of these questions, they're a gosh-darned liar.

# What makes a language functional vs. object-oriented?

## Functional languages

There's a few attributes that make a language amenable to functional programming:

- Support for recursion (bonus points for Tail-Call Optimisation)
- Anonymous functions
- Closures
- Currying, which is also called partial application
- Lazy evaluation

However, there is no definition of a "functional language". Even Haskell, the most popular example of a functional language, [behaves in a somewhat non-functional manner at IO boundaries](https://futureofcoding.org/essays/dctp.html#haskell-and-the-io-monad). As discussed in the previously linked article, making a language "functional" is an ongoing area of research.

## Object-Oriented languages

When people think about Object Oriented Programming (OOP), they typically think of Java. If they're a bit more sophisticated they bring up SmallTalk as the original OOP language. However, [SmallTalk did not invent the term Object](https://www.hillelwayne.com/post/alan-kay/). Furthermore, what many consider one of the most essential parts of SmallTalk (message-passing) [isn't really possible in Java](https://softwareengineering.stackexchange.com/a/140607/98711). Thus, does that mean that [Erlang is *more* Object Oriented than Java](https://www.infoq.com/interviews/johnson-armstrong-oop/)? Or maybe, as said by Hillel Wayne: "Terms evolve as problems do."

## OOP vs Functional

To summarize the two sections above in a pithy manner, here's Hillel Wayne again:

{{< figure
  src="/img/hillel-fp-oop-tweet.png"
  class=""
  title=""
  caption=""
  label=""
  attr=""
  attrlink=""
  alt=""
  link="https://twitter.com/Hillelogram/status/962452705280233472"
 >}}

 # What is the fastest language?

Well, C, but that's only because we've [spent decades tuning processors for it](https://queue.acm.org/detail.cfm?id=3212479). But really which culture of programming are we talking about? Is it throughput or reactivity?

{{< figure
  src="/img/hillel-fp-oop-tweet.png"
  class=""
  title=""
  caption=""
  label=""
  attr=""
  attrlink=""
  alt=""
  link="https://twitter.com/worrydream/status/1071191862462038016"
 >}}

Because if we're talking about throughput, have you tried writing multi-machine multi-GPU code in C? Julia is much better at this. Alternatively, if you're focused on reactivity, you have to start reckoning with the overhead added by various processor architectures and operating systems.

{{< figure
  src="/img/hillel-fp-oop-tweet.png"
  class=""
  title=""
  caption=""
  label=""
  attr=""
  attrlink=""
  alt=""
  link="https://twitter.com/andy_kelley/status/1218408056108830721"
 >}}

And you may start wondering if [we were better off before all this complexity was added](https://threadreaderapp.com/thread/927593460642615296.html).

Anyways, yeah, properly written C is hard to beat, but not for the reasons typically mentioned. Are you sure you can't use [Zig](https://ziglang.org/) instead?


# What makes a language embeddable?

embedding a programming language is a different problem than programming an embedded system. [Nobody can agree on what makes a language "embeddable"](https://softwareengineering.stackexchange.com/q/403911/98711).

# What are the trade-offs between compiled and interpreted languages?

The trade-off between compiled and interpreted languages is [constantly fluctuating](http://jamie-wong.com/bending-the-pl-curve/)

# What is the best language for teaching?

No one is sure what programming language to teach first, but it probably isn't C/C++ or Java given [this research](https://quorumlanguage.com/evidence.html).

# What is the best language for visualisation?

Creating a language for visualization is called Projectional Editing. Allowing the manipulation of that projection is called Bidirectional Manipulation. Both of these problems are incredibly challenging.

A lot of people think it requires designing totally new languages/interfaces. Steven Krouse has made an [excellent overview of previous attempts](https://futureofcoding.org/catalog/).

# What is the future of programming?

The biggest leaps in languages come from taking ideas from extensive research. This is really hard to do correctly. Look at [this blog post from one of the creators of Rust](https://graydon2.dreamwidth.org/253769.html) summarizing cool things around the corner for more info. His whole blog is fabulous.
