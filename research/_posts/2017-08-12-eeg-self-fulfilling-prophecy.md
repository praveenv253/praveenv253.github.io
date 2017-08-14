---
layout: single
title: Systematically questioning the self-fulfilling prophecy of EEG's low resolution
date: 2017-08-12 12:01 -0400
day: Saturday
tags:
  - EEG
  - Nyquist rate
  - Experimental validation
---

[Electroencephalography](https://en.wikipedia.org/wiki/Electroencephalography)
(EEG) has long been believed to be a low-resolution brain imaging modality.
There is a pervasive view in the community of EEG users that increasing the
number of EEG electrodes will not improve imaging resolution. We have worked
towards systematically understanding the reasons this view exists, and towards
changing perceptions about EEG.

The heart of our argument is explained in our [recent
paper](/publications#Grover2017Information) titled "An Information-theoretic
View of EEG Sensing". We examined previous estimates of the number of sensors
needed to recover the EEG signal. These estimates relied on computing the
"spatial Nyquist rate" of scalp EEG, and it turned out that they underestimated
the number of sensors required to reliably recover the _continuous scalp
potential_. We also showed, through simulations and intuitive arguments, that
the number of EEG sensors required to recover the _signal within the brain_
could be even higher than the number prescribed by the spatial Nyquist rate.

Naturally, the follow-up question is: "What are the fundamental theoretical
limits of the imaging resolution achievable by EEG, and how does this
resolution improve with increasing numbers of sensors?" While this paper gives
a first-pass at understanding these limits, we followed up with [a
paper](/publications#Venkatesh2017Lower) that gave the first analytical results
showing that EEG's imaging resolution could improve with an increase in the
number of EEG sensors.

We also gave information-theoretic techniques to help save power in a future
implementation of an ultra-high-density EEG system. This last point, which
focuses on the practical aspects of instrumenting such a high-density EEG
system was first discussed in [Allerton
2015](/publications#Grover2015Information), where we introduced a "hierarchical
referencing mechanism" to save power and circuit area.

Towards showing experimentally and practically that high density EEG, and
specifically, super-Nyquist sampling is more informative than conventional EEG,
we recently conducted some experiments in collaboration with Amanda Robinson,
Marlene Behrmann and Mike Tarr at CMU's Psychology department, which [show
that](/publications#Robinson2017Very) high-density EEG has better
classification accuracy than low-density EEG in classifying between visual
stimuli of different spatial frequencies.

{% comment %}
Lastly, to show that EEG has practical benefit in the clinical setting, we
presented a poster at the 2016 annual meeting of the American Epilepsy Society
[6] and a talk at the 2017 World Congress on Brain Injury [7], where we show
through simulations how high density EEG has the capacity to detect "Cortical
spreading depolarizations", and propose automated algorithms to do the same.
Patients suffering from traumatic brain injury often also suffer from CSDs,
spreading waves of activity which can kill neurons and stall recovery from TBI.
If detected early, preventive measures can be taken to prevent the occurrence
of such waves, or reduce their adverse impact.
{% endcomment %}
