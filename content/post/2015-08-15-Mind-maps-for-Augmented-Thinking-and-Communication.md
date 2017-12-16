+++
title = "Mind-maps for Augmented Thinking and Communication"
date = "2015-08-15"
categories = ["Programming", "Mindmaps", "Communication"]
+++

In my [last post](https://seanny123.github.io/post/2015-08-15-Debugging-Your-Thoughts-with-Mind-Maps/), I introduced the concept of a mind-map and how they can be applied to Cognitive Behaviour Therapy. However, this is far from the only possible application.

This post shows how mind-maps can be used for:

1. A shared medium for enhancing inter-personal communication
2. Life-goal tracking
3. Taking notes during presentations and programming

I’ll finish off this overview with software suggestions and a bit of philosophising as to why mind-maps are so effective.

## Mind-maps for communication

I really like the Internet for various reasons, but discussion on them look like this.

{{< figure
  src="/img/Mind-maps-for-Augmented-Thinking-and-Communication_0.png"
  class=""
  title=""
  caption=""
  label=""
  attr=""
  attrlink=""
  alt=""
  link=""
 >}}
{{< section "end" >}}

I also like what a lot of people write on the Internet, but sometimes certain places on the Internet seem to cause [toxoplasmas of rage](http://slatestarcodex.com/2014/12/17/the-toxoplasma-of-rage/).

I have a hypothesis that a lot of communication breaks down because of a few simple sources of confusion that aren't well-supported in the current discussion format of the internet:

-   

    History (this is where I’m coming from)
-   

    Context (this is what I think we’re both talking about)
-   

    Time (I want to write a comment reply, not a blog post)
-   

    Audience (I’m replying to you? I’m replying to this whole thread?)
-   

    Reasoning (how did you get from point A to point B)


Like any engineering with illusions of grandeur, I started thinking of various fantastical solutions to this problem. Like creating a language where the certainty of a fact is conjugated into a verb.

More realistically, I thought about people sharing mind maps on the Internet as a medium of communication.

It would enable to attach arguments to an appropriate context in a manner of varying length. People could understand the history of where others are coming from, proof of arguments would be a lot easier to see, it would be much easier to distinguish a troll from someone who doesn't have time to describe all of the nuance in their argument.

It would also solve the problem of conflicting communities. When someone sees the word feminism or Muslim, there is a whole wide spectrum to what they could be imagining. This is a problem, because when people identify with the collective or try to critique it, they can can be identifying/critiquing crazily different things. With mind maps, you could have all the benefits of identifying with a collective (support, self-critique), with the added bonus that if you are offended confused by that collective, you can punch down to the roots to gain understanding.

For example, you’re debating with someone on the Internet about an article about women in tech. The person you’re discussing with identifies as a feminist! But wait, it turns out that she doesn’t want to silence all men, she just wants everyone to be nicer and more accepting of each other. You can probably imagine how bad things would have went if you had made the incorrect assumption.

Finally, you could also mark certainty of your nodes, so a person can be aware if you want more information on something.

I'm even so arrogant as to think that this technique could also help with [StackOverflow](https://stackoverflow.com/tour) questions! When a noob doesn’t know what the hell they’re doing, we can suggest nodes from our progamming-specific mindmaps for them! And then the noob can understand where I got this knowledge from and how to ask questions about their own nodes!

Interestingly, I’m not the first one to imagine this. The cognitive scientist Paul Thagard has been writing about this for years in the form of [cognitive-affective maps](http://cogsci.uwaterloo.ca/empathica.html), but he mostly analysed [one-to-one mappings](http://cogsci.uwaterloo.ca/Articles/thagard.2012.values.cogscisci.ch17.pdf) and [discussions](http://cogsci.uwaterloo.ca/Articles/findlay-thagard.emo-change.group-dec.2014.pdf) rather than addressing the complex audiences of the Internet.

Obviously, my idea of grandiose application to the discourse of the Internet is wrong and according to some people, this is [because the architecture of the Internet cannot support such dynamic linking and customisation.](http://hapgood.us/2015/07/21/beyond-conversation/)

So I guess I’ll have to keep dreaming about the day when the Internet finally becomes what we imagine it to be.

## Life goal tracking

For my personal use, I like to review every week in the form of a mind-map where I am and where I'm going.

{{< figure
  src="/img/Mind-maps-for-Augmented-Thinking-and-Communication_1.png"
  class=""
  title=""
  caption="Stacked-looking nodes have sub-nodes that I’ve hidden. Red nodes means I keep messing up the goal."
  label=""
  attr=""
  attrlink=""
  alt=""
  link=""
 >}}
{{< section "end" >}}

If I see one of goals hasn't had progress in a while, I can start thinking about why. Maybe that goal isn't as important to me as I thought? Is some barrier stopping me from getting started?

Like my previous post about [Unit Testing Stories](https://seanaubin.wordpress.com/2015/07/01/unit-testing-stories/#more-4), this doesn't tell you *how* to go about reaching your goals, it just gives you a base to build on or a better visual on how it’s all working out. There’s a ton of writing out there already about productivity and reaching your goals, especially from my friend Malcolm Ocean. If you want tools on how to be motivated and plan well, go see [his blog](http://malcolmocean.com/) or follow him on Facebook.

## Taking notes in one-shot lectures

I'm currently a member of the [Centre for Theoretical Neuroscience](https://uwaterloo.ca/centre-for-theoretical-neuroscience/) which has a lot of speakers come in. All the speakers present well and have interesting ideas, but for some reason, every time I attended a lecture, I would start off excited and motivated, but eventually end up lost and bored.

I realised that the main problem was the fact that I wasn't actively participating in trying to understand the material. Additionally, when I was active and I had questions, even if I wrote them down, I forgot what they were in relation to or how much I had understood to that point.

My solution was to make mind-maps as notes. They look like this.

{{< figure
  src="/img/Mind-maps-for-Augmented-Thinking-and-Communication_2.png"
  class=""
  title=""
  caption=""
  label=""
  attr=""
  attrlink=""
  alt=""
  link=""
 >}}
{{< section "end" >}}

I highlight things that confused me in red and keep two branches off of the root node for “Asides” and “Questions”. “Asides” are ideas that sprouted from this talk but probably aren’t related. “Questions” are general and require follow-up with various people.

This mostly scales only to one-shot lectures and not an actual lecture series, because of the “quick-overview” nature of one-shot lectures.

## Programming

Once upon a time in undergraduate engineering, one of my aspiring developer friends was trying to get a job with Khan Academy. He was trying to make an interactive way for kids to practice matrix operations. He called me over to help him, describing how the Khan Academy JavaScript library was impossible to understand. I asked why he had to use that library and why not just use basic JavaScript. He did exactly that and finished his work in 30 minutes.

This is a perfect example of tunnel vision, which I consider the hardest part of debugging. You can get stuck in a Google-spiral researching something to death when you should be hacking or you can be banging your head on a wall hacking when you should be searching for more elegant solutions. To balance these is non-trivial, especially since time flows so strangely in both of those troubling states.

An added bonus is the ability to review what you've considered to re-evaluate your rationality once a solution has been found or suggested by another person. What assumptions did you make that incorrectly invalidated an option? What heuristic will you use next time? It also give you something to show your boss when they think you've just made the stupidest decision ever.

{{< figure
  src="/img/Mind-maps-for-Augmented-Thinking-and-Communication_3.png"
  class=""
  title=""
  caption="Look boss! I just made some incorrect assumptions. I'm not actually incapable of rational thought!"
  label=""
  attr=""
  attrlink=""
  alt=""
  link=""
 >}}
{{< section "end" >}}

## Software

My favourite software for mindmapping is [MindMup](https://www.mindmup.com). I’ve tried about a dozen different softwares including FreeMind, FreePlane, bubbl.us and Coggle. Mindmup has just the right features for me (rarely requiring me to use my mouse, works offline, can use cloud storage or local storage), allows me to share mind maps and collaboratively work on them. It’s also free and open-source! It’s so free that the developers won’t even take donations despite the fact that I would give them $100 at this point.

## Why can mind-maps be so effective?

Although I have little evidence for this, I think that mindmaps are a way to hack around limited cognitive resources, as well as cognitive biases.

By cognitive resources, I mean your ability to keep a set of options in your head (working memory), as well as a recollection of the other options previously considered and the events leading up to your current decision (serial/episodic memory). Mind-maps are an extension of your mind letting you manipulate your thoughts in feelings in more manageable chunks.

In terms of biases, in the book *Thinking Fast and Slow* the idea of “All You See Is All There Is” is discussed. It’s the idea that after a certain point you stop looking for evidence that might disprove your current conclusion. I think mindmaps force you to slow down and question the assumptions you make at each node. This then engages you to do more research, but always remaining in the scope of the original problem so you don’t get side-tracked.

*If you liked this article and want to read more of my posts about augmenting thinking, consider* [*subscribing to my mailing list*](https://uwaterloo.us15.list-manage.com/subscribe?u=d5612fe997cc72aac70c4ffe9&id=76226838bc)*.*
