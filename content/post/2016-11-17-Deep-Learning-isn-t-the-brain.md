+++
title = "Deep Learning isn’t the brain"
subtitle = "(but sometimes the results look like one)"
date = "2016-11-17"
categories = ["Artificial Intelligence", "Neuroscience", "Deep Learning", "Cognitive Science", "Machine Learning"]
+++

*\[epistemic status: I work in a lab dedicated to biologically plausible neural circuits, so I’m informed on the problem, but probably still biased. There’s probably going be a follow-up post to this once I get a bunch of rebuttals from people smarter than me.\]*

***Update:*** *As expected, I got a bunch of rebuttals and have* [*adjusted my position accordingly*](https://medium.com/@seanaubin/deep-learning-is-almost-the-brain-3aaecd924f3d)

I keep seeing [academic](http://biorxiv.org/content/biorxiv/early/2016/08/23/071076.full.pdf) and [non-academic articles](http://timdettmers.com/2015/07/27/brain-vs-deep-learning-singularity/) comparing Deep Learning (DL) and the brain. This offends my sensibilities a bit, because although there are [many](http://compneuro.uwaterloo.ca/publications/sharma2016b.html) [results](http://www.pnas.org/content/111/23/8619.abstract) from DL that resembles certain areas of the brain, DL is not a good overall description of the brain. DL explicitly passes the buck on biological plausibility (like almost every other cognitive modelling approach) and implies that it’s “neurons” can be implemented biologically, it’s just that no one has bothered yet. I think the problem goes much deeper and that DL is missing a lot of the key features of the brain, which makes it a poor analogical target.

---

#### The brain is low power

DL is power hungry. Alpha GO consumed the power of [1202 CPUs and 176 GPUs](https://www.tastehit.com/blog/google-deepmind-alphago-how-it-works/), not to train, but *just to run*. The [TenserFlow Processing Unit](https://cloudplatform.googleblog.com/2016/05/Google-supercharges-machine-learning-tasks-with-custom-chip.html) is an attempt to satiate this hunger, but it’s still not even close to the [brain’s power consumption of 20W](http://cogsci.stackexchange.com/q/12750/4397). IBM’s TrueNorth chip is another example of trying to bring low-power computation, but [it’s capabilities are quite limited when compared to other Neuromorphic hardware](https://medium.com/@seanaubin/a-way-around-the-coming-performance-walls-neuromorphic-hardware-with-spiking-neurons-facd4291b201#.86xjo9oyf). Specifically, True North only implements feed-forward networks and has no on-chip learning.

#### The brain can’t do back-prop

Back-propagation is the foundation of all DL. Although there is evidence that errors being propagated through multiple layers is happening in the brain, no one has come up with a method for back-propagation (back-prop)that doesn’t rely on information propagating backwards through unidirectional synapses. I personally think it’s only a matter of time before a biologically plausible method is discovered, but until then it is unwise to ignore the implementation details and the restrictions it might place on what can be learned.

#### The brain uses spikes to communicate

Although it is possible to [convert DL networks into spiking neurons for use on neuromorphic hardware](https://arxiv.org/abs/1510.08829), these spikes are not leveraged for specific computational advantages. As far as I know (and I still have some reading to do), spiking computation has yet to be used anywhere for the learning in DL.

#### Neurotransmitters aren’t just spike transporters and neurons aren’t just spike-machines

DL completely ignores the role of neurotransmitters. However, neurotransmitters have been shown to be computationally significant in adapting the receptive features networks on the fly, something which DL has really hard time doing.

#### The brain is noisy

Given the choice between neuron redundancy and neuron performance, evolution chose to make the brain redundant. [Neurons are noisy](http://icwww.epfl.ch/~gerstner/SPNM/node33.html), which isn’t surprising when you consider the warm, biologically variable environment they’re in. Although certain DL networks can cope with loss of their nodes, DL isn’t known for it’s robustness to noisy input or noisy training data.

---

In conclusion, there are a lot of features of the brain that DL is omitting, thus using DL as an analogy for neural circuitry isn’t ideal. The alternative to comparing with DL is using a modelling paradigm that takes these challenges into account. At the time of writing, the only approach I know of is the Neural Engineering Framework (NEF) from the laboratory I belong to, but I’m sure as research marches forward other frameworks will emerge.

“But Sean,” you cry with a gleam of mischief in your eye, “don’t most NEF models from the lab you belong to suffer from the same problems as DL? The models usually stop at LIF neurons, which aren’t realistic neurons at all! Why don’t you use more complex neuron models, i.e. things like [dendritic computation](http://pub.ist.ac.at/Pubs/courses/AY1314/MolandCellNeuro_S14/files/Stuart%20et%20al_Dendrites_Chapter16.pdf), multi-compartmental neurons, [glial cells](http://www.cell.com/trends/immunology/abstract/S1471-4906%2815%2900200-8) and neurogenesis?”

That’s a work in progress. There are 2 people ([Aaron Voelker](http://compneuro.uwaterloo.ca/people/aaron-russell-voelker.html) and [Peter Duggins](http://compneuro.uwaterloo.ca/people/peter-duggins.html)) of the 16-strong [Computation Neuroscience Research Group](http://compneuro.uwaterloo.ca/index.html) (CNRG) that I belong to who are working on the problem of more complex neuron models. [Eric Hunsberger](http://compneuro.uwaterloo.ca/people/eric-hunsberger.html) is working on biologically plausible back-prop and the moment he has a break-through you can be sure I’ll be shoving it in everyone’s face.

As for neurogenesis, There’s no good computational model of what neurogenesis does and the CNRG lacks the resources to do that sort of basic research. Dendritic and glial cell computation has no one working on it, because we’re only 16 people. If that bothers you, maybe you want to join us?

