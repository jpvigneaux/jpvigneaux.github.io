---
layout: page
title: research
permalink: /research/
description: Discrete structure in continuous representations
nav: true
nav_order: 1
horizontal: false
toc:
  sidebar: left
---

Neural networks represent discrete categories (word senses, syntactic relations, intonational tunes) as vectors in continuous spaces. I study how these categories sit in a model's geometry and how that geometry shapes what the model computes, with tools from information theory and geometry.

# Current work

**Probing and steering speech models.** With [Jennifer Cole](https://sites.northwestern.edu/cole/), I ask whether speech models represent the intonational *tunes* of English, such as the final rise that turns a statement into a question. Simple classifiers (*probes*) show that a neural audio codec encodes the tunes ([Speech Prosody 2026](https://www.isca-archive.org/speechprosody_2026/vigneaux26_speechprosody.html)). In two text-to-speech systems, we located where the tune is carried and steered it with directions computed from human recordings ([arXiv](https://arxiv.org/abs/2610.27403), under review at ICLR 2027; [code](https://github.com/jpvigneaux/steering-intonation-tts)).

**Syntactic probes.** Structural probes recover some syntactic relations from a language model far better than others. Two quantities explain most of the difference: how far apart the related words are, and a similarity-aware entropy of the words that head the relation ([arXiv](https://arxiv.org/abs/2608.27813), under review; with Kennedy, Iskarous, Frank and Marcolli).

**Curvature and word meaning.** A label-free correction of distances between word embeddings, based on optimal transport, brings them closer to human judgments of how related two uses of a word are (in preparation; JMM 2027).

# Next

* Interpretability methods for generated speech, where events spread over time rather than sitting at fixed positions.
* The shape of categories in embedding spaces (curvature, local dimension, magnitude) and how a model's components act on them.
* Models as instruments: labeling intonation in large speech corpora to study what tunes mean in conversation.

# Mathematics of information

* [Topological characterization of information measures](/Research/information-topology)
* [Information dimension and measures with geometric structure](/Research/information-dimension)
* [Magnitude and diversity](/Research/magnitude)
* Entropies of group orbits ([arXiv](https://arxiv.org/abs/2512.02257), with two undergraduates)

# Students

I have mentored five undergraduates at Caltech: Stephanie Chen, Eric Paul, Ryan Leal, Bharathan Sundar and Aman Burman. Three of my papers began as their projects.
