+++
title = "Why Biologically Plausible Modelling is Ignored"
date = "2017-11-18"
categories = ["Cognitive Science"]
+++

In a [previous post](https://seanny123.github.io/post/2017-05-09-Book-Review-The-Entrepreneurial-State/), I noted:

>When I was first getting interested in Cognitive Science, I started reading “How to Build a Brain” by Chris Eliasmith. By the end of it, I felt biologically plausible modelling was hugely important for the advance of Cognitive Science. I also knew this feeling was misleading given I had no familiarity of the argument landscape. Why wasn’t everyone else doing biologically plausible modelling? Why were they still using their seemingly inferior frameworks?

Years later, I can say with some confidence that there a generally three beliefs people hold about biologically cognitive modelling which justifies their lack of investigation into it's approach:

## 1. Neuroscience isn't ready

There isn't enough information about the biological details to model them properly. Neuroscience is still at the level of characterizing brain areas and occasionally brain inter-area communication. At finer levels, you mostly just get an avalanche of spikes with little context.

My counter-argument to this is neuroscience is moderately ready and will never be ready if we don't help. What is definitely obvious from neuroscience:

1. Neurons represent inputs and the outside world
2. Neurons transform these inputs using synapses, dendrites and axons
3. Neurons learn over time how to do both these things
4. Brain areas specialize to carry out certain computations

Neuroscientific models will only gain explanatory power with greater constraints.

## 2. Existing approaches will be validated by biology

The biological details will be figured out later and will support the existing approach. So there's no point trying to tie things to biological details. Deep Learning or Bayesian Networks or Symbolic Computation will be biological plausible later, so there's no point figuring out how, since it will just validate that the existing methods are biologically plausible.

Feed-forward Deep Learning is seeming more biologically plausible every day. My labmate Su is working on bayesian networks and symbolic computation. However, the devil is in the details.

1. You can do k-WTA instantaneously.
2. Deep Learning has timing problems that means it can't learn instantaneously.
3. Seriously, no is paying attention to continuous time. 

## 3. Pursuing biological plausibility is a losing game

Going after biological plausibility is a losing game. You'll never have enough detail. Look at the Blue Brain project. Millions of dollars and years later, they modelled a few neurons of the barrel cortex of a mouse. How are they ever going to scale up to a human cortex? They stopped at the detail of a few chemicals and molecules. But later, people will claim it was a travesty to not go down to atoms or they will claim quantum effects are necessary to explain the brain.

Like any puritanical pursuit, biological purism is doomed to failure. However, one can still pursue biological plausibility by choosing the right level of abstraction for the right model. As discussed in "[The use and abuse of large-scale brain models](https://www.sciencedirect.com/science/article/pii/S095943881300189X)":

>For the brain, we do not know the right level of detail beforehand, but exploring plausible levels *in the context of behavior* is likely to lead, most efficiently, to a good understanding of the structure/function relation.
>
>With these considerations in mind, it seems clear that arguing over the ‘right’ level of detail for brain models is misguided. We should always ask “right for what purpose?” The correct answer will often be controversial. But, building detailed models and simplifying them carefully is a good method for determining the best answers to such questions.

To allow for the "right" level to be selected and for simplification to be carried out "carefully", you require tools that let you move between levels. As I discuss in a [previous post](https://seanny123.github.io/post/2017-01-09-Deep-Learning-is-almost-the-brain/), due to it's commitments to biological plausibility, the Neural Engineering Framework and the Semantic Pointer architecture offers a unique ability to move between these levels.

## 4. Explaining variation is equivalent to explaining mechanisms

As shown in "[Toward an Integration of Deep Learning and Neuroscience](https://www.frontiersin.org/articles/10.3389/fncom.2016.00094/full)", Deep Learning can explain a large amount of variation in the human visual cortex. This is encouraged by neural nets becoming less like black boxes with [encouraging research from many parties](https://twitter.com/voyageur_techno/status/866488636463697920).

What's the difference between explaining learning mechanisms and explaining the resulting mechanisms?

---

As I note in the conclusion of nearly all my posts, these beliefs are all partially right. Deciding on a research path is ultimately a personal decision. Although guided by empirical evidence, heuristics and intuition end making most of the final call.

I find meaning in integration of disparate fields and perspectives. I find reassurance by being grounded in biology. Most importantly, I see hope in building something to understand it, which I'm sure I share with all cognitive modellers, whether they are concerned with biology or not.

*If you liked this post, consider joining [my mailing list](http://eepurl.com/cOiPPD) to get updated about future posts.*
