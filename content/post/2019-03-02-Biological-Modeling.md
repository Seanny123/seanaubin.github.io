+++
title = "Why Biologically Plausible Modelling is Ignored"
date = "2018-03-02"
categories = ["Cognitive Science"]
draft = true
+++

In a [previous post](https://seanaubin.com/post/2017-05-09-Book-Review-The-Entrepreneurial-State/), I noted:

> When I was first getting interested in Cognitive Science, I started reading “How to Build a Brain” by Chris Eliasmith. By the end of it, I felt biologically plausible modelling was hugely important for the advance of Cognitive Science. I also knew this feeling was misleading given I had no familiarity of the argument landscape. Why wasn’t everyone else doing biologically plausible modelling? Why were they still using their seemingly inferior frameworks?

Years later, I can say with some confidence that there a generally four beliefs (three invalid and one valid) people hold about biologically cognitive modelling justifying their lack of investigation into it's approach:

# I. Neuroscience isn't ready

## Example argument

There isn't enough information about the brain's biological details to inform explanations of behaviour. Neuroscience is still at the level of characterizing brain areas and occasionally brain inter-area communication. At finer levels, you mostly just get an avalanche of spikes with little context.

## Reply

Theoretical neuroscience strongly suggest the following features for neuron-level computation:

### 1. Neurons can do certain types of computations.

1. Neurons enable continuous time, gradual actions (not instant) and parallel (as opposed to sequential) evaluation. Which means no "if-statements" (or heaviside functions) where small input changes create large change in output.
2. Neurons limit how information is shared, due to the finite number of connections in the brain and the latency of synapse communication. A neuron cannot have perfect information of what every other neuron is doing.
3. Neurons require learning to be explicitly explained in a natural environment. No magical outside control of learning.

### 2. Neurons noisily represent the outside world.

The previous section's list constrain how neurons represent the outside world and perform computations on these representations. Due to `1.`, representations cannot be binary or discrete. Due to `2.` and `3.` representation modification must be achievable and learnable by groups of neurons without unrealistic inter-neuron coordination. The current favoured representation, [Vector Symbolic Architecture](http://home.wlu.edu/~levys/vsa.html), satisfies all these constraints.

### 3. There are explicit modules present in the brain.

- Rick Granger's lab has deconstructed the brain into general purpose modules, as shown in "[Elemental cognitive acts, and their architecture](https://aaai.org/ocs/index.php/FSS/FSS17/paper/view/15984)".
- Similar modules appear in Eliasmith's research. Specifically, the hippocampus appears to be used for temporal processing. Memorized transforms happen in temporal cortex, while working memory in the prefrontal. There's a fast and a slow system. Slow system is probably BG-Thal-Cortex loop.

Applying these three neuronal constraints to behavioural models creates [better explanations](https://psychology.stackexchange.com/q/6247/4397).

# II. Existing approaches will be validated by biology

## Example argument

Existing approaches (Deep Learning, Bayesian Networks, Symbolic Computation... etc.) will eventually be shown to map to biology. Consequently, there's no point trying to tie things to biological details directly.

## Reply

Some modelling approaches have been mapped to biological implementations. Feed-forward Deep Learning seems [more biologically plausible every day](https://psychology.stackexchange.com/a/19776/4397). My ex-labmate Su published a thesis on [bayesian computation in spiking networks](https://uwspace.uwaterloo.ca/handle/10012/13503). However, there are limits on what can be biologically validated. I've seen many biology-imitating systems, which take into account the lessons from Section I, still making biologically implausible assumptions which will never be validated, such as:

1. It is possble to do k-Winner-Take-All instantaneously. See [Leabra](https://psychology.stackexchange.com/a/17388/4397).
2. It is possible to change the connection weights of a neural network instantaneously. See [Conceptors](https://github.com/CogSciUOS/Conceptors).

Consequently, I consider this argument to be unfounded.

# III. Pursuing biological plausibility is a losing game

## Example argument

Going after biological plausibility is a losing game. You'll never have enough detail. Look at the Blue Brain project. A million dollars and years later, they [modelled a few neurons of a mouse's barrel cortex](https://www.cell.com/abstract/S0092-8674(15)01191-5). How are they ever going to scale up to a human cortex? They stopped at the detail of a few chemicals and molecules. Later, people will claim it was a travesty to not go down to atoms, since quantum effects are necessary to explain the brain.

## Reply

Like any puritanical pursuit, biological purism is doomed to failure. However, one can still pursue biological plausibility by choosing the right level of abstraction for the right model. As discussed in "[The use and abuse of large-scale brain models](https://www.sciencedirect.com/science/article/pii/S095943881300189X)":

> For the brain, we do not know the right level of detail beforehand, but exploring plausible levels *in the context of behavior* is likely to lead, most efficiently, to a good understanding of the structure/function relation.
>
> With these considerations in mind, it seems clear that arguing over the 'right' level of detail for brain models is misguided. We should always ask "right for what purpose?" The correct answer will often be controversial. But, building detailed models and simplifying them carefully is a good method for determining the best answers to such questions.

To allow for the "right" level to be selected and for simplification to be carried out "carefully", you require tools that let you move between levels. As I discuss in a [previous post](https://seanaubin.com/post/2017-01-09-Deep-Learning-is-almost-the-brain/), the Neural Engineering Framework and the Semantic Pointer Architecture are an example of this tool type.

# IV. Explaining variation is equivalent to explaining mechanisms

## Example argument

[oh god, what do I mean by "variation" and "mechanistic". i have to unpack these terms]

As shown in "[Toward an Integration of Deep Learning and Neuroscience](https://www.frontiersin.org/articles/10.3389/fncom.2016.00094/full)", Deep Learning can explain a large amount of variation in the human visual cortex. Furthermore, these variation-explaining structures are equivalent to a mechanistic explanation. Deep Learning is becoming less of a Black Box with [encouraging research from many parties](https://twitter.com/voyageur_techno/status/866488636463697920). Even when considering the previous replies, approaching cognitive modelling while ignoring biology still yields the most meaningful explanations.

## Concession and conclusion

There is no reasonable way to argue against this. Although guided by empirical evidence, deciding on a research path is ultimately a personal decision [guided by the scientist's personal values](https://medium.com/what-to-build/human-values-a-quick-primer-b01ef9617925).

Personally, I find meaning in integration of disparate fields and perspectives. I find reassurance by being grounded in biology. Most importantly, I see hope in building something to understand it. I think the latter value is shared with all cognitive modellers, regardless of their concern with biology. This shared value means regardless of the modeller I'm talking to, I can at least find some common ground, which brings me great comfort.

*If you liked this post, consider joining [my mailing list](http://eepurl.com/cOiPPD) to get updated about future psychology and neuroscience posts.*
