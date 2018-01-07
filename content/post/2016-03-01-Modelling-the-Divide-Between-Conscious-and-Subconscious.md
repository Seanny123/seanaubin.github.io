+++
title = "Modelling the Divide Between Conscious and Subconscious"
date = "2016-03-01"
categories = ["Cogntive Science", "Consciousness"]
+++

*\[epistemic status: although I've become adept with the Neural Engineering Framework and the Semantic Pointer Architecture, I'm not super comfortable in the philosophical depths of Cognitive Science. This article is not a professional presenting a final answer, but an amateur formulating their current view.\]*

The divide between what is conscious and what is subconscious is a fascinating question often because it acts as a proxy for more urgent personal questions, such as:

- Who am I?
- How much can I change?
- What do I have control over?

In this article, I won’t attempt to answer these questions directly (given they’re freaking hard questions), instead I’d like to approach this question in the only way I know how: by building a model based off of empirical, experimental and philosophical evidence. By “building” I mean just putting together two models that have already been built and by “evidence” I mean using the evidence in the papers that I took the models from, without explicitly stating it here.

To understand the subconscious, we first have to understand what is consciousness. To model consciousness we need to select our tools. The modelling tool that I find the most power in (surprising no one given it comes from my lab) is the Semantic Pointer Architecture (SPA).

The SPA is based on the idea that computation in the brain is done by manipulating vectors called Semantic Pointers (SPs) by binding and compressing them using neurons. This idea is kind of sophisticated, but the easiest way to understand it is seeing Spaun, which was built using the SPA, in action.

<iframe frameborder="0" height="480" scrolling="no" src="https://www.youtube.com/embed/mP7DX6x9PX8?feature=oembed" width="640"></iframe>

In the above video, Spaun takes the high dimensional input of the many pixels on a screen, transforms it into the concept of ‘4’ and ‘3’ to perform the task by going up the visual hierarchy, and then writes it the number back out by going down the motor hierarchy.

This shows how manipulating vectors is a model of brain processes. It also shows how concepts are tied to the sensory information received from the outside world.

How can this be applied to consciousness? In [this model by Paul Thagard and Terry Stewart](http://cogsci.uwaterloo.ca/Articles/thagard.two-theories.consc&cog.2014.pdf), consciousness is modelled as competition between SPs.

{{< figure
  src="/img/Modelling-the-Divide-Between-Conscious-and-Subconscious_0.png"
  class=""
  title=""
  caption="Taken from Thagard and Stewart 2014"
  label=""
  attr=""
  attrlink=""
  alt=""
  link=""
 >}}

Basically, it’s saying you get representations in your brain from your motor system, your sensory inputs, your emotions and your verbal productions. What you become conscious of is a result of one of those representations winning/losing the fight for your attention.

That’s consciousness, so everything below that must be subconscious. Most of those inputs are pretty easily explainable, except emotion. What is emotion? There’s a model for that too using SPs in [this book chapter by Paul Thagard and Tobias Schröder](http://cogsci.uwaterloo.ca/Articles/thagard-schroeder.emotions-pointers.2013.pdf).

{{< figure
  src="/img/Modelling-the-Divide-Between-Conscious-and-Subconscious_1.png"
  class=""
  title=""
  caption="Taken from Thagard and Schröder 2013"
  label=""
  attr=""
  attrlink=""
  alt=""
  link=""
 >}}

It argues that emotion is a result of a combination of neural representations of your physiology (am I hot/cold?), your situation (can I turn up the thermostat?), and your appraisal (what do I think about all of this?).

Putting these two together, you get something that looks like this.

{{< figure
  src="/img/Modelling-the-Divide-Between-Conscious-and-Subconscious_2.png"
  class=""
  title=""
  caption="You can tell I made this figure because of it came from Google Draw"
  label=""
  attr=""
  attrlink=""
  alt=""
  link=""
 >}}

This is all very abstract and hard to follow, so let’s use a more practical example in the form of someone who has anxiety. Because often the best way to understand a system is to look at it while it’s malfunctioning and (more importantly) coming up with ways to fix it.

Anxiety has multiple causes and thus multiple solutions. Sometimes it can be a product of a situation, in which case the situation can be fixed or avoided using action. Other times the cause is less concrete, arriving in the form of a maladaptive thought pattern, in which case the appraisal part of this system needs to be remedied, possibly using [Cognitive Behaviour Therapy]({{< ref "2015-08-15-Debugging-Your-Thoughts-with-Mind-Maps.md">}}). Finally, there’s the possibility that physiologically the person consistently finds they are constantly in “flight or fight” mode without cause, which could be remedied with medication. Obviously every case of anxiety disorder is unique and which options are pursued are up to the individual.

This is one view of consciousness, which provides some useful explanatory mechanisms, but I'm certainly not claiming it’s the right one. I'm currently trying to gain more subtlety in my perspective on this matter by reading different perspectives, such as [Joscha Bach](https://www.youtube.com/watch?v=2o2xBOQeB7Q)’s MicroPsi framework. I’ll write another post (or more likely post a question/answer on [CogSci.SE](https://cogsci.stackexchange.com/tour)) once I've put my thoughts together.
