---
layout: page
title: research
permalink: /research/
description: Interests and projects
nav: true
nav_order: 1
#display_categories: [work, fun]
horizontal: false
toc:
  sidebar: left

#  **Explainability of LLMs used as classifiers** *Joint project with Markus Marks.* We use large language models as classifiers and assign relevance scores (i.e. contributions to the prediction of the correct class) to all neurons using layer-wise relevance propagation {cite Montavon2019}, which has recently been extended to transformers {cite Achtibat2024}. The tensor of all these scores is a high dimensional object, that we reduce using the techniques in {cite Kondapaneni2024}, based on nonnegative matrix factorization (NMF) {cite Lee2000}. In {cite Kondapaneni2024}, image classifiers were applied to birds and the factors obtained by NMF (visualized directly on the input image) were aligned with expert criteria to make them interpretable. In the case of language, we aim to obtain similar interpretable clusters---not only at the input level but across all layers|postulating that more abstract concepts (e.g., criteria of textual analysis) become available at deeper levels in the network, analogous to what occurs in convolutional neural networks {cite Zeiler2014}. We are currently working on code implementation.)  

---

# AI interpretability

I am currently working on AI interpretability, with a particular focus on transformer-based large language models (LLMs). I am actively working on two projects:

### Geometry of LLMs' latent representations and emergence of compositional features.

  Previous work point to a nontrivial intrinsic geometry of token embeddings: they can be seen as points of a stratified space {% cite Robinson2024 %}, and different models (even trained on different modalities) have comparable embeddings {% cite Roads2020 Luo2024a %}. I have computed that in language models such as GPT-2, k-means clustering or hierarchical clustering of the token embeddings reveal some degree of organization that combines semantics and potential syntactic roles.   As a first approximation, a *primitive feature* is a characteristic of an embedded token (possibly shared by members of cluster) that is exploited by some attention or MLP block. Instead of taking the matrices of these blocks as the main objects of interest, my focus is on the coordinate-independent geometric entities (e.g. linear subspaces) that the matrices define in residual space,  e.g. via  their kernels, images, and singular vectors. Rather than interpreting the singular vectors directly in terms of input tokens, as in {% cite Elhage2021 %} or {% cite Dar2023 %}, I interpret them as providing incremental modifications to the initial embeddings, "constructing" new context-dependent features from the primitives (thus obtaining *compositional features*); the interaction with layer norm might contribute to the emergence of discrete classes {% cite Winsor2022 %}. Since deeper layers do not only read the initial token embeddings but also the modifications introduced by previous blocks, we need new tools to quantify the relevance of modifications introduced at each layer. A combination of hierarchical clustering and matrix-based input-independent analysis of heads will give us a hierarchy of coarse grained descriptions of the action of each block on tokens and a coarse grained view of the interaction between different blocks. 
  
### Understanding internal representations of syntax in LLMs via mechanistic interpretability
  
   *Joint project with Aman Burman  (undergraduate student) and Matilde Marcolli.* Transformer-based language models are able to produce text that follows syntactic rules; such ability suddenly emerges in a brief period during training {% cite Chen2024 %}. By analogy with some toy models (see e.g. {% cite Li2023 %}), we can hypothesize that a transformer encodes syntax as part of an internal "world representation". We are using tools from mechanistic interpretability on small language models to extract encoded syntactic features, understand how they are distributed across layers, and identify which subnetworks or *circuits* utilize this information. We are investigating whether the syntactic processing in language models is hierarchical and analogous to syntactic trees in linguistics. Here we have in mind, in particular, the mathematical formalization of Chomsky's minimalist program in the language of Hopf algebras {% cite Marcolli2023 Marcolli2023a %}. We want to refine the analysis in {% cite Manning2020 %}, which shows that the activations of attention heads are correlated with syntactic binary relations, but did not explore the mechanisms by which these relations are assembled into more complex trees.  

# Mathematics of information 

More broadly, I'm interested in mathematical aspects of **information theory**, particularly in connection with category theory and  geometry (metric geometry, geometric measure theory, ...).  My work in this regard can be organized around three axes: 
* [Topological characterization of information measures](#minfo-topology) 
* [Information dimension and measures with geometric structure](#dimension)
* [Magnitude and diversity](#magnitude)

Each of these is described in more detail below. I've included links to videos and slides of relevant presentations, along other resources. 

### Topological characterization of information measures {#minfo-topology}

In "simple" terms, *information topology* regards a statistical system as a generalized topological space (a *topos*) and identifies Shannon entropy, along other important "measures of information" used in information theory, as an [invariant](https://en.wikipedia.org/wiki/Invariant_(mathematics)) associated to this space. 

[Toposes or topoi](https://en.wikipedia.org/wiki/Topos) are an abstraction of topological spaces in the language of category theory and sheaves introduced by Grothendieck and his collaborators (Artin, Verdier,...). Toposes allow richer cohomology theories than set-theoretic topological spaces, and some of these theories (e.g. étale cohomology) play a key role in modern algebraic geometry. Moreover, these *Grothendieck toposes* are particular cases of *elementary toposes*, which are "nice" categories with properties analogous to those of the category of sets that play an important role in logic. 

Baudot and Bennequin {% cite Baudot2015 %} first identified Shannon's discrete entropy as a toposic invariant of certain categories of discrete observables. My Ph.D. thesis {% cite Vigneaux2019-thesis %} and a series of articles extended their results in several directions. Namely, the general homological constructions were abstracted from the concrete setting of discrete variables via  *information structures* (categories that encode the relations of refinement between observables), allowing seamless extensions and generalizations to other settings such as continuous vector-valued observables {%cite Vigneaux2020information %}. 

When the information structure encodes discrete observables, the classical information functions—--
Shannon entropy, Tsallis $\alpha$-entropy, Kullback-Leibler divergence—--appear as 1-cocycles; the corresponding "coefficients" of the cohomology are probabilistic functionals (i.e. functions of probability laws).
There is also a combinatorial version of the theory (coefficients are  functions of histograms) where the only 0-cocycle is the exponential function and the 1-cocycles are generalized multinomial coefficients (Fontené-Ward) {% cite  Vigneaux2023characterization %}. There is an asymptotic relation between the combinatorial and probabilistic cocycles. 

For information structures that contain continuous vector-valued observables (besides discrete ones), the only new degree-one cocycles are Shannon's differential entropy entropy and the dimension (of the support of the measure) {% cite Vigneaux-GSI21-cohomology %}. This constitutes a novel algebraic characterization of differential entropy.

Information cohomology has seen some advances in the last years. Marcolli and Manin {% cite Manin2020homotopy %} related information structures with other homotopy- and category-theoretic models of neural information networks. Similar perspectives have been developed more recently by Belfiore and Bennequin {% cite belfiore2021topos %} to tackle the problem of interpretability of neural networks. They associate to each neural network a certain category equipped with a Grothendieck topology (determined by the connectivity of the neurons), and study the category of sheaves on it, which is a topos. Every topos has an internal logic, and they are linking this internal toposic logic with the classification capabilities that emerge in each layer of a trained neural network (these were previously studied in the experimental article {% cite belfiore2021logical %}). 

**Presentations:** 
* ["Cohomological Aspects of Information" [video]](https://www.youtube.com/watch?v=Nzx9MotxEas), Topos Institute, 2024: I summarize  the main results that I have obtained in this domain. 
* ["Information Cohomology of Classical Vector-valued Observables" [video]](https://www.youtube.com/watch?v=rW76AlxMbrU), GSI2021: I provide details on the characterization of the differential entropy and the dimension as the only cohomology classes in degree 1 for systems of vector-valued observables.
* ["Entropy under disintegrations" [video]](https://www.youtube.com/watch?v=uYoW-pGbEWY), GSI 2021: I explain how every disintegration of a reference measure $\lambda$ induces a chain rule for the generalized differential entropy $S(\rho) = -\int \log (\frac{d\rho}{d\lambda}) d\rho$, which gives a foundation to the extension of information cohomology to more general observables e.g. with values in locally compact topological groups. 
* ["Variations on Information Theory: Categories, Cohomology, Entropy" [video]](https://www.youtube.com/watch?v=eZqo_JcTk3I), IHES, 2016: an older presentation, aimed at probabilistists, where I introduce the notion of (de Rham) cohomology  and it's analogue in our theory.

**Other references:**
* ["On the Structure of Information Cohomology"](https://tspace.library.utoronto.ca/bitstream/1807/130552/3/Dub%EF%BF%BD_Hubert_202311_PhD_thesis.pdf), Ph.D. thesis by Hubert Dubé (U. Toronto), which introduces the Mayer-Vietoris long exact sequence, Shapiro's lemma and Hochschild-Serre spectral sequence in the framework of information cohomology, and provides some bounds on the cohomological dimension along with new cohomological computations. 
* ["Information cohomology and Entropy"](https://sites.unimi.it/barbieri/castiglioni.pdf), master thesis by Luca Castiglioni (University of Milan).

### Information dimension and measures with geometric structure {#dimension}

From an analytic perspective, the *dimension* has played an important in information theory since its inception, mainly in connection with quantization.  By partitioning $\Rr^d$ into cubes with vertexes in $\mathbb Z^d/n$, one might quantize a continuous probability measure $\rho$ into a measure $\rho_n$ with countable support, whose entropy satisfies
\begin{equation}\label{eq:expansion_law}
H(\rho_n) = D\ln n + h + o(1),
\end{equation}
where $D=d$ and $h=h(\rho)$ is the differential entropy of $\rho$ {% cite Kolmogorov1993 %}. Renyi {% cite Renyi1959 %} turned this into a definition: if $\rho$ is now a general law and the expansion \eqref{eq:expansion_law} holds for some constants $D,h\in \Rr$, one calls $D$ the information dimension of $\rho$ and $h$ its $d$-dimensional entropy. He wondered about the "topological meaning" of the entropic dimension, which might be  noninteger. 


In {% cite Vigneaux2023typicality %} I introduced an *asymptotic equipartition property* for discrete-continuous mixtures or, more generally, of convex combination of rectifiable measures on $\Rr^d$. In particular, it gives an interpretation for the information dimension $D$ of one of these measures $\rho$: 
the product $(\Rr^d)^n$ naturally splits into strata of different dimensions, and the typical realizations of $\rho^{\otimes n}$ concentrate on strata of a few dimensions close to $nD$. I also obtained volume estimates (in terms of Hausdorff measures) for the typical realizations in each typical stratum. (A measure $\rho$ is $m$-rectifiable if there exists a set $E$, equal to a  countable union of $C^1$ manifolds, such that $\rho$ has a density with respect to the restricted HAusdorff measure $\mathcal H^m|_E$, which is the natural notion of $m$-dimensional volume on $E$.)

**Presentations:**
* ["On the entropy of rectifiable and stratified measures" [slides]]({{site.baseurl}}/assets/pdf/slides/GSI23-stratified.pdf), GSI 2023, Saint Malò, France. 
* ["Typicality for stratified measures" [slides]]({{site.baseurl}}/assets/pdf/slides/ETH-2023-stratified.pdf), ETH Zurich, 2023. 

### Magnitude and diversity {#magnitude}

Magnitude {% cite Leinster2008 %} is a common categorical generalization of cardinality and of the Euler characteristic of a simplicial complex. It applies to enriched categories, of which metric spaces are a notable example, and in that case gives a new isometric invariant of metric spaces {% cite Leinster2013 %}. Applied to infinite metric spaces, this metric invariant---somehow surprisingly---encodes a lot of nontrivial geometric information, such as Minkowski dimension, volume, surface area, etc.{% cite Meckes2015 Barcelo2018 Gimperlein2021 %}. Partial differential equations, pseudodifferential operators and potential theory have played an important role in establishing these results.

In joint work with Stephanie Chen {% cite Chen2023formula %} (SURF program 2022), we gave a new formula for the magnitude of a finite category $\cat{A}$ in terms of the pseudoinverse of the  matrix 
\begin{equation}
\zeta:\Ob\cat{A}\times \Ob \cat{A}\to \Zz, \, (a,b)\mapsto |\Hom(a,b)|.
\end{equation}
This was closer to the definition for posets {% cite Rota1964 %} that had inspired Leinster. Our work also rederived algebraic properties of the magnitude from properties of the pseudoinverse.
 
 In {% cite Vigneaux2024combinatorial %} I propose a novel combinatorial interpretation for the inverse or pseudoinverse of $\zeta$, along the lines of {% cite Brualdi2008 %}. The interpretation generalizes a celebrated theorem by Philip Hall {% cite Rota1964 %}:
 \begin{equation}
 \zeta^{-1}(a,b)=\sum_{k\geq 0} (-1)^k \\# \\{ \text{nondegenerate paths between  }a\text{ and }b \\}
 \end{equation}
  when $a$ and $b$ are elements of a finite poset (in this case $\zeta$ is invertible; its inverse is known as Möbius function). 

  What does this have to do with information? Following Boltzmann ideas, entropy can be seen as an extension of cardinality: when all elements of a finite set $X$ are equiprobable, the entropy is $\ln |X|$. In turn, magnitude is a generalization of cardinality, and it is natural to introduce a probabilistic extension of it: "categorical entropy". Stephanie and I 
  {% cite Chen2023formula %} proposed that categorical entropy is defined on finite categories equipped with a probability $p$ on objects and a "kernel" $\theta:\Ob\cat{A} \times \Ob \cat{A} \to [0,\infty)$ such that $\theta(a,a')=0$ whenever $a\not\to a'$ via the formula 
 \begin{equation}\label{eq:cat_entropy}
 \mathcal H(A,p,\theta) = - \sum_{a\in \Ob \cat A} p(a) \ln \left(\sum_{b\in \Ob \cat A} \theta(a,b)p(b) \right).
 \end{equation}
This function shares many "nice" properties with Shannon entropy. In the context of metric spaces equipped with probability, \eqref{eq:cat_entropy} appears as a measure of diversity between species when $p$ is its relative abundance and $\theta$ measures their similarity {% cite Leinster2012 %}.

**Presentations:**
* ["A Combinatorial Approach to Categorical Möbius Inversion and Magnitude" [video]](https://www.youtube.com/watch?v=CGzOVeQLLnA), Applied Algebraic Topology Network, 2024.
* ["Categorical Magnitude and Entropy" [slides]]({{site.baseurl}}/assets/pdf/slides/GSI23-magnitude.pdf), GSI 2023, Saint Malo, France.


# Bibliography

{% bibliography --cited %}
