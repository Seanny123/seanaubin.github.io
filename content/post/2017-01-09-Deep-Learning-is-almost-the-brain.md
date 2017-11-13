+++
title = "Deep Learning is almost the brain"
subtitle = "(and it’s results still look like one sometimes)"
date = "2017-01-09"
categories = ["Artificial Intelligence", "Neuroscience", "Deep Learning", "Cognitive Science", "Machine Learning"]
+++

*\[epistemic status: an update on a* [*previous position*](https://hackernoon.com/deep-learning-isnt-the-brain-e1d800ebb5a9#.qkv2fs6ah) *as a result of discussion with people smarter than me\]*

People emailed me and I read their stuff! As I predicted, I was sometimes horribly wrong and often too simplistic.

{{< figure
  src="/img/Deep-Learning-is-almost-the-brain_0.png"
  class=""
  title=""
  caption="It currently has 800 views, which is 10 times more than my usual readership."
  label=""
  attr=""
  attrlink=""
  alt=""
  link=""
 >}}
{{< section "end" >}}

Below is an update/clarification on my positions.

---

## Some form of back-prop could be biologically plausible

There is [a ton of work](http://cogsci.stackexchange.com/q/16269/4397) on biologically plausible back-prop and it was really unfair of me to dismiss them all in one paragraph. That being said, I’m still sceptical of the various implementations, due to the fact they seem to exist in isolation of each other and I can’t find any of their code anywhere (except for “[Deep learning with segregated dendrites](https://arxiv.org/abs/1610.00161)”) so I can evaluate them.

## Against theoretical isolation: a manifesto

My new, much better informed position on DL is that I wish it didn’t exist in such isolation. [As I’ve written before](https://medium.com/@seanaubin/understanding-the-brain-where-metaphors-limit-you-13d5d5fbdc57#.9fw8ikmog), I think a promising line of research is integrating it with other approaches to cognitive modelling. If there was some way it was possible to move up and down the ladder of abstraction with DL, I would consider it a much better analogy for neural computation. Additionally, this would resolve the other weaker arguments (about DL not leveraging biological details, the limitations of current neuromorphic hardware and the lack of spike use in learning) from my previous post. Finally, this would also allow for the leveraging of the powerful developmental explanations allowed by DL by other cognitive modelling paradigms.

{{< figure
  src="/img/Deep-Learning-is-almost-the-brain_0.png"
  class=""
  title=""
  caption="The Cognitive Modelling [Ladder of Abstraction](http://worrydream.com/LadderOfAbstraction/). ([image source](https://docs.google.com/drawings/d/1mknlMUpnFzRXpb3L_dt-x8hxYK42b1pxlNfYstDH8uc/edit?usp=sharing))"
  label=""
  attr=""
  attrlink=""
  alt=""
  link=""
 >}}
{{< section "end" >}}

I realise this is a purely philosophical position about what a good future for cognitive modelling looks like. I’m sure there are detractors who consider it unnecessary to connect to different approaches via biology. However I feel like a lack of synthesis can lead to overly complicated, unscalable models. For example, [Eric Crawford’s model of knowledge representation](http://compneuro.uwaterloo.ca/publications/crawford2015.html), which demonstrated how using symbols and neurons allows for much more scalable model than a purely neural approach. Alternatively, consider [Spaun](http://science.sciencemag.org/content/338/6111/1202). It is only able to perform many tasks and generate many predictions as a result of mixing different approaches which would only be possible with a much greater increase in complexity. However these are feelings, not facts.

{{< figure
  src="/img/Deep-Learning-is-almost-the-brain_1.png"
  class=""
  title=""
  caption="([source](https://twitter.com/umruehren/status/816665138161799168))"
  label=""
  attr=""
  attrlink=""
  alt=""
  link=""
 >}}
{{< section "end" >}}

The only way I can see my philosophy can be proved wrong is if cognitive modelling advances without consulting biology. In which case I will abandon my pretences and join everyone in the realm of pure mathematics. Until then I’ll keep trying to build my ladder.

---

This philosophical approach isn’t easy and I’m sure others have attempted this. I’m just not clear on why the other attempts failed. Is it a [lack of reproducible computational experiments due to various problems](https://medium.com/@seanaubin/the-surprising-things-i-learned-from-grad-school-8a0efd458ae0#.94hfg15yq)? Or was it just too difficult until now? I look forward to working to find out.

*If you liked this article and want to read more of my brain science posts, consider* [*subscribing to my mailing list*](https://uwaterloo.us15.list-manage.com/subscribe?u=d5612fe997cc72aac70c4ffe9&id=76226838bc)*.*

