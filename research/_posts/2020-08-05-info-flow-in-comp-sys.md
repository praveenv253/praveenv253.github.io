---
layout: single
title: Defining and Inferring Flows of Information in Neural Circuits
date: 2020-08-05 19:06 -0400
day: Wednesday
mathjax: true
tags:
  - Information flow
  - Message
  - Computational system
  - Granger Causality
  - Synergy
  - Partial information decomposition
---

While studying existing methods for inferring information flow in neuroscience, we recognized that Granger Causality [does not always](/publications#Venkatesh2015Direction) capture information flow _about a specific message or stimulus_. We were able to construct a counterexample wherein Granger Causality inferred the incorrect flow of a message, _even when all nodes were observed and when there was no measurement noise_. This counterexample also applied to generalizations of Granger Causality, such as Transfer Entropy and Directed Information. We believe that an important reason for the failure of Granger Causality-based tools in this context was the lack of a _formal definition for information flow_ pertaining to a specific _message_ (which could be the stimulus or response in a neuroscientific experiment). The development of such a definition, in turn, was impeded by the absence of a concrete theoretical framework that linked information flow about a message to empirical measurements. [We addressed this fundamental gap](/publications#Venkatesh2018Information) in our understanding by proposing a new computational model of the brain, and by providing a new definition for information flow about a message within this model.

A central contribution of our work lies in recognizing that tracking the flow of information about a specific message _requires_ that we also account for _synergistic_ flows of information. To understand why, note that a message $M$ may be represented, in combination with some independent "noise" variable $Z$, as $M{+}Z$ and $Z$, across two different brain areas. Represented in this form, if the noise $Z$ is large, it can be very hard to ascertain the presence of information flow about $M$ in the combination $[M{+}Z, Z]$, unless we account for possible synergy between these two brain areas. Accounting for synergy, using conditional mutual information for instance, is thus crucial for tracking information flow in arbitrary computational systems. Relatedly, I have also begun exploring how synergy, along with other partial information measures such as uniqueness and redundancy, arise and interact in neural encoding using entorhinal grid cells as a case study (<a href="/publications#Venkatesh2020Understanding">Venkatesh and Grover, <em>Cosyne</em>, 2020</a>).

![Cannot track information flow without accounting for synergy](/assets/img/xor-counterexample.png){: width="400px" .align-center}

Our new measure of information flow does not have the same pitfalls as Granger Causality, while satisfying our intuition in several canonical examples of computational systems. The full impact of this work continues to be realized, as [we explore new measures in greater depth](/publications#Venkatesh2020Define), demonstrate and validate these methods on artificial neural networks, and examine the causal implications of making interventions based on information flow inferences.

[<i class="fa fa-file-text-o fa-lg" aria-hidden="true"></i>&ensp;Main paper in Transactions on Info Theory](/publications#Venkatesh2018Information){: .btn .btn--light}
[<i class="fa fa-file-text-o fa-lg" aria-hidden="true"></i>&ensp;2015 Granger Causality Counterexample paper](/publications#Venkatesh2015Direction_Allerton){: .btn .btn--light}
[<i class="fa fa-file-text-o fa-lg" aria-hidden="true"></i>&ensp;2020 ISIT paper on alternative definitions](/publications#Venkatesh2020Define){: .btn .btn--light}
