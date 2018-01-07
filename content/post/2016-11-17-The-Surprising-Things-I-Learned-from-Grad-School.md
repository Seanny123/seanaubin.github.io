+++
title = "The Surprising Things I Learned from Grad School"
date = "2016-11-17"
categories = ["Academia", "Software"]
+++

I’ve been in grad school for a year now, so I figured now was as good of a time to reflect as ever.

I learned a lot of things I expected to learn, like how to write a paper, what’s the difference between a conference paper and a journal paper and how do you get grants to support your research.

I also was totally blindsided by a lot of other things, which mostly fall into the categories “Computery Things” (because my lab develops a ton of software) and “Social Things”. If you only care about one of those categories, you can skip the other.

---

## Writing good code is non-trivial

I used to think I was a pretty good coder. I left comments and I tried not duplicate code everywhere. Then I start having code-reviews whenever I submitted code to our big software project Nengo, where my lab-mates reviewed everything I had written and made suggestion. These code-reviews have taught me so much in terms of habits, setups and intuition that I couldn’t have gotten anywhere else. This kind of scares me, because it means I have no idea how non-computery labs are supposed to get better. Post snippets of their code on [codereview.stackexchange.com](http://codereview.stackexchange.com/)? Walk down the hall to the computer science department and force them to sit down with you?

## Dev Ops is foundational

For any successful commercial software project to be able to evolve, [the amount of time required for a new developer to get from interest to running code should be minimal](http://www.joelonsoftware.com/articles/fog0000000043.html). Not only that, but you should be able to log bugs, automatically run minimal tests and be able to quickly get the most updated code. All of these things fall under the umbrella of “Dev Ops”.

Dev Ops being important doesn’t stop being true when you’re a scientist writing scientific code, which is tragic because:

1.  

    **Dev Ops is freaking *hard*.** You have to learn a bunch of different tools that haven’t been made non-hacker friendly yet. Travis-CI, whatever testing framework and builder your language uses (if it’s Matlab, good luck), and git (*shudder)* suddenly go from become things you’ve heard of to things you need to understand *right now*.
2.  

    **Dev Ops isn’t taught *anywhere*.** Not in Software Carpentry, Coursera and definitely not at your institution, so you need to wrangle together a bunch of tutorials from the Internet and sacrifice a mouse to the computer gods.


Given these obstacles, it’s not surprising to learn that Dev Ops in scientific code is practically unheard of, even in widely distributed and used libraries. Before my Master’s degree I would have shrugged it off has not being a major problem in science, but now [I scream in horror](https://bullshit.ist/why-im-an-open-source-nerd-an-apology-7d7a3e0e13e9#.f8rjqga4h).

## Centralized documentation is life support

Having your documentation to your project somewhere online, where anyone can propose edits, is the only way your project’s docs will remain up to date and thus the only way your software will be able to proliferate and survive. Luckily, unlike everything else in this article, there’s tons of solutions to this! I just don’t know which one to recommend to absolute beginners… Leave a comment and I’ll update this section?

## Scientific tooling is horrible

Part of keeping up with research is reading a lot of papers. I thought for sure there would be tools for this everywhere. A unified program (I use a bunch of separate ones) that lets you tag papers, then search through the tags and annotations. A website where you can subscribe to feeds on research you’re interested in (lots of those exist) and collaboratively comment (nope) on publications. [Interactive drawing/coding tools](https://www.youtube.com/watch?v=YuGVC8VqXz0&list=WL&index=45) for making complex animated figures. A thriving StackExchange where researchers bounce ideas off each other and drive synthesis of new concepts. Nope. Instead you get ResearchGate, Twitter, Mendeley, Google Draw and spam.

{{< figure
  src="/img/The-Surprising-Things-I-Learned-from-Grad-School_0.png"
  class=""
  title=""
  caption="Follow me on Twitter for more hilarious insights into why things are horrible."
  label=""
  attr=""
  attrlink=""
  alt=""
  link=""
 >}}

---

## Your team is essential

Lab-mates are important. I knew they were important, but I didn’t know just *how* important. Without my lab-mate Aaron, I would have never published my first paper. Without my lab-mate Terry, I would have never been able to determine the appropriate scope for my initial research for that paper. Without my lab-mate Trevor, I would have never learned how to write good scientific software.

## Communicating concepts is excavation

I used to think of myself as a pretty good communicator. I even put it on my resume. However, this year all evidence that I had of that was utterly and irrevocably refuted. This year was the year I learned Non-Violent Communication, which taught me how to talk about emotions and has literally changed my life, but that’s a whole other blog post. This was also the year where I routinely needed to quickly grasp concepts and relate them to my current knowledge so I could remember the faint outline of their importance for later. This technical communication style did not come easily for me.

Here’s are a few tricks I use when teaching or learning from other people.

**Useful questions**

- What’s the last thing you understood?
- Can you say what I just said back to me, but using different words?
- What is the closest thing that you think you know to this concept?
- What do you mean by… ? What did you think I meant by… ?


**When meeting with someone**

- Be specific about what you need from them: “I want your help deciding… ?”
- Make sure you both leave with the same conclusion: “What I’m going to remember from this is… ? Is this what you wanted me to remember?”


The post-doc in my lab, Terry Stewart, has this down to an art form. To the point that I frequently like to watch him teach concepts to people just to see how he manoeuvres through their understanding like a hawk through a canyon.

Admittedly, I still need to work on my similes and metaphors.

## Mathematical notation is a foreign language

I currently have no idea how to communicate with mathematical concepts textually. I literally have to translate them from/to code. I learned this during my undergrad, where math made sense to me for the first time in my life after I learned how to program. However, I only realised serious it was this semester. I look at a sum and I think “Okay, a for-loop”. I see a chain of equations and I think “Where’s the source code?”

Consequently, unless I’ve programmed something, like back-prop or the Neural Engineering Framework. I cannot say I truly understand it. This is a bit problematic at the moment, given my immense confusion with the following things which I need to rectify in the next 7 months and I’m not sure they’re easy to code.

Wish me luck.
