---
layout: page
title: Research
permalink: /research/

---


## Topic models and community detection in complex networks

[Topic models](https://en.wikipedia.org/wiki/Topic_model) are a popular way to extract
information from text data, but its most popular flavours (based on [Dirichlet priors](https://en.wikipedia.org/wiki/Dirichlet_distribution), such
as [LDA](https://en.wikipedia.org/wiki/Latent_Dirichlet_allocation))
make unreasonable assumptions about the data which severely limit its
applicability. Here we explore an alternative way of doing topic
modelling, based
on [stochastic block models (SBM)](https://en.wikipedia.org/wiki/Stochastic_block_model), thus
exploiting a mathematical connection with
finding [community structure](https://en.wikipedia.org/wiki/Community_structure) in networks.

To briefly illustrate some of the limitations of Dirichlet-based topic
modelling, consider the simple multi-modal mixture of three topics shown
below on the left. Since the Dirichlet distribution is unimodal, it
severely distorts the topics inferred by LDA, as shown in the middle
&mdash; even thought it is just a prior distribution over a
heterogeneous topic mixture. The SBM formulation, on the other hand, can
easily accommodate this kind of heterogeneity, since it is based on more
general priors (see [here](https://dx.doi.org/10.1103/PhysRevX.4.011047), [here](https://dx.doi.org/10.1103/PhysRevE.95.012317), and [here](https://dx.doi.org/10.1103/PhysRevX.5.011033)).

 <img src="{{ site.baseurl }}/images/triangles.png" style="display: block; margin: 0 auto; width: 400px"> 

In addition to this, the SBM method is based a nonparametric “symmetric”
formulation that allows for the simultaneous hierarchical clustering of
documents as well as words. Due to its nonparametric Bayesian nature,
the number of topics in each category, as well as the shape and depth of
the hierarchy, are automatically determined from
the [posterior distribution](https://en.wikipedia.org/wiki/Posterior_probability) according to the statistical evidence available,
avoiding both [overfitting](https://en.wikipedia.org/wiki/Overfitting) and
underfitting.

To illustrate the application of the method using real data, we show
below an example using [wikipedia](https://www.wikipedia.org/) articles:

<IMG SRC="{{ site.baseurl }}/images/bipartite.png" style="display: block; margin: 0 auto; width: 400px">
*Example: 63 Wikipedia articles related to Physics*

**References**:

* A network approach to topic models, Science Advances [[link to the paper](http://advances.sciencemag.org/content/4/7/eaaq1360)]
* TopSBM [[code](https://topsbm.github.io/)]

---

## Science of Science

#### Evolution of scientific fields

In this project, we used an information-theoretic measure of linguistic similarity (the [Jensen-Shannon divergence](https://en.wikipedia.org/wiki/Jensen%E2%80%93Shannon_divergence))
to investigate the organization and evolution of scientific
fields. An analysis of almost 20 M papers from the past
three decades reveals that the linguistic similarity is related
but different from experts and citation-based classifications,
leading to an improved view on the organization of science.
A temporal analysis of the similarity of fields shows that
some fields (e.g. computer science) are becoming increasingly
central, but that on average the similarity between pairs of
disciplines has not changed in the last decades. This suggests
that tendencies of convergence (e.g. multi-disciplinarity)
and divergence (e.g. specialization) of disciplines are in
balance.

<IMG SRC="{{ site.baseurl }}/images/evolution-of-scientific-fields.png" style="display: block; margin: 0 auto; width: 100%">
*Example: Comparison of dissimilarity between scientific disciplines based on expert classification (left), citations (middle), and language (right). Darker color means fields are more similar.*

**References**:

* Using text analysis to quantify the similarity and evolution of scientific disciplines, Royal Society Open Science [[link to paper](http://rsos.royalsocietypublishing.org/content/5/1/171545)]


**Related projects**:

* Investigating the reasons for inequality in attention to different research questions. Here we focused on genes of relatively well-defined units of knowledge in biomedical research.  
   *Large-scale investigation of the reasons why potentially important genes are ignored*, PLOS Biology [[link to paper](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.2006643)]

* Investigating where citations occur within the text of a paper.  
   *Large-scale analysis of micro-level citation patterns reveals nuanced selection criteria*, Nature Human Behaviour [[link to paper](https://www.nature.com/articles/s41562-019-0585-7)]


---
## Statistical Laws in Complex Systems

The availability of large datasets requires an improved view on statistical laws in [complex systems](https://en.wikipedia.org/wiki/Complex_system), such
as [Zipf’s law](https://en.wikipedia.org/wiki/Zipf's_law) of word frequencies, the [Gutenberg-Richter law](https://en.wikipedia.org/wiki/Gutenberg%E2%80%93Richter_law) of earthquake magnitudes, or [scale-free
degree distribution in networks](https://en.wikipedia.org/wiki/Scale-free_network). 
Here, we discuss how the statistical analysis of these laws are affected by correlations present in the observations, the typical scenario for data from complex systems. 
We show how [standard maximum-likelihood recipes](http://tuvalu.santafe.edu/~aaronc/powerlaws/) lead to false rejections of statistical laws in the presence of correlations. We then propose a conservative method (based on shuffling and undersampling the data) to test statistical laws and find that accounting for correlations leads to smaller rejection rates and larger confidence intervals on estimated parameters.

<IMG SRC="{{ site.baseurl }}/images/statistical-laws-ab.png" style="display: block; margin: 0 auto; width: 600px">

<IMG SRC="{{ site.baseurl }}/images/statistical-laws-cd.png" style="display: block; margin: 0 auto; width: 600px">

*Example of four statistical laws in complex systems together with existence of strong correlations (inset)*


**References**:

* Testing Statistical Laws in Complex Systems, Physical Review Letters [[link to paper](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.122.168301)]
* Review paper on statistical laws in language [[link to paper](https://link.springer.com/chapter/10.1007/978-3-319-24403-7_2)]

---

## Spreading of linguistic innovations

It is well accepted that [adoption of innovations](https://en.wikipedia.org/wiki/Diffusion_of_innovations) are described by [S-curves](https://en.wikipedia.org/wiki/Sigmoid_function) (slow
start, accelerating period and slow end). 
In this project we analyzed how much
information on the dynamics of innovation spreading can be obtained from a
quantitative description of S-curves. We focused on the adoption of linguistic
innovations for which detailed databases of written texts from the last
200 years allow for an unprecedented statistical precision using ([Google-ngram](https://books.google.com/ngrams) containing millions of books from the past 5 centuries). Combining data
analysis with simulations of simple models (e.g. the Bass dynamics on complex networks), we identify signatures of endogenous and exogenous factors
in the S-curves of adoption. We proposed a measure to quantify the strength
of these factors and three different methods to estimate it from S-curves. We
obtained cases in which the exogenous factors are dominant (in the adoption
of [German orthographic reforms](https://en.wikipedia.org/wiki/German_orthography_reform_of_1996) and of one irregular verb) and cases in
which endogenous factors are dominant (in the adoption of conventions for
[romanization of Russian names](https://en.wikipedia.org/wiki/Romanization_of_Russian) and in the [regularization of most studied
verbs](https://en.wikipedia.org/wiki/Regularization_(linguistics))). These results show that the shape of S-curve is not universal and
contains information on the adoption mechanism.

<IMG SRC="{{ site.baseurl }}/images/linguistic-innovations.png" style="display: block; margin: 0 auto; width: 100%">
*Example of 3 different cases for adoption of linguistic innovations. Orthographic reform in German replacing sharp-s by ss (left), romanization of Russian names (middle), and regularization of past form of English verbs such as spilled vs spilt (right).*

**References**:

* Extracting information from S-curves of language change, Journal of the Royal Society Interface [[link to paper](http://rsif.royalsocietypublishing.org/cgi/doi/10.1098/rsif.2014.1044)]

<!-- ---

## Personality and Individual Differences

jajajaja.
 -->
<!-- ---

## Scaling of urban indicators

jajajaja. -->