---
layout: page
title: Evolution in Finite Populations
description: Modelling stochastic evolutionary dynamics from first principles (MS thesis project)
img: assets/img/stochastic_sims.gif
importance: 1
category: Previous
permalink: /projects/MS_thesis
---

<i> June 2022 - May 2023<br>
Supervisors: Prof. Vishwesha Guttal, Prof. Rohini Balakrishnan</i>


<h1> Part 1: Noise-induced selection and its effects in finite populations of non-constant size </h1>

<div style="text-align: justify">

Many central questions of population biology relate to the number of distinct variants of an entity that can emerge and coexist in a closed population. Examples include the study of standing genetic variation (alleles), polymorphisms (genotypes/phenotypes), and sympatric speciation (species). Historically, these questions have often been studied through phenomenological models formulated for infinitely large populations. However, we increasingly realize that demographic stochasticity can have important consequences for evolution. For example, in adaptive diversification models, demographic stochasticity can delay or prevent evolutionary branching in finite populations.
<br>
<br>
<div class="row" style="text-align: center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/evolutionary_branching.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
Two different realizations of a stochastic individual-based model of resource competition in one dimension where individuals compete according to a continuous  trait analogue of the logistic equation. The model on top has a population of around 1000 individuals, and remains monomorphic. The model on the bottom has a population of around 10000 individuals, and exhibits evolutionary branching, where an initially monomorphic population evolves to become dimorphic. All other model parameters are identical across both simulations.
</div>
<br>
While we understand natural selection very generally through frameworks such as the Price equation, finite population models in population genetics, such as the Wright-Fisher or Moran models, often assume a fixed population size, greatly limiting their generality. For my Master's dissertation, I worked with <a href='https://teelabiisc.wordpress.com/'>Prof. Vishwesha Guttal</a> and <a href = 'https://sites.google.com/view/rohinibalakrishnanlab/home'>Prof. Rohini Balakrishnan</a> at the Centre for Ecological Sciences at IISc Bangalore to build more general analytical (mathematical) theory for evolution in finite populations from first principles using ideas from statistical physics and stochastic processes. Starting from a density-dependent 'birth-death process’ describing a population of individuals with discrete traits, I derive stochastic differential equations (SDEs) for how the relative population sizes and trait frequencies change over time. These SDEs recover well-known results such as the replicator-mutator equation, the Price equation, and Fisher’s fundamental theorem in the infinite population limit, illustrating consistency with known formal descriptions of evolution and showing that these equations are 'universal', in the sense that almost any sufficiently large population will satisfy these equations, no matter how complicated the biology of the population. For finite populations, these same SDEs generically reveal a directional evolutionary force, 'noise-induced selection’, that is particular to finite, fluctuating populations and is present even when all types have the same fitness. The strength of noise-induced selection depends directly on the difference in turnover rates between types and inversely on the total population size. Noise-induced selection can reverse the direction of evolution predicted by infinite-population frameworks. This general derivation of evolutionary dynamics helps unify and organize several previous studies - typically performed for specific evolutionary and ecological contexts - under a single set of equations.
<br>
<br>
<div class="row" style="text-align: center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/schematic_BD_process.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
<b>A.</b> A schematic description of a one-dimensional stochastic birth-death process for a population of identical individuals. The entire population is characterized by the population size, and changes in population size are mediated by density-dependent birth and death rates. On the bottom row, time series of a realization of a stochastic version of the logsitic equation for finite populations in which the carrying capacity is <b>B.</b> 500, <b>C.</b> 1000, and <b>D.</b> 10,000. Here, carrying capacity controls the total population size and thus the amoount of stochasticity. The exact stochastic simulation, various analytical approximations, and the deterministic (infinite population) limit are all plotted. 
</div>
<br>
The formalism of birth-death processes and their description via master equations are well known to physicists and mathematicians. This thesis focused on the biological implications of the master equation/system-size expansion formalism for biological populations, which is relatively newer. In particular, two important biological observations, (i) that birth and death rates in biological populations must always admit per-capita descriptions, and (ii) Ecological interactions are in terms of individuals and densities but evolutionary processes are described in terms of frequencies, calling for a non-linear change of variables that requires It\^o's formula, both have major implications for the behavior of these systems. Remarkably, we find that we can (asymptotically) recover standard equations of theoretical biology such as the replicator equation and the Price equation with just these observations. Our equations also clarify and unite several previous studies that have illustrated the presence of noise-induced selection in various specific model systems postulated in diverse areas of biology such as epidemiology, heterogamety, life-history evolution, and social evolution by capturing their results in a single set of very general stochastic differential equations. Our equations also take the form of generalizations of the replicator-mutator and Price equations, which are familiar to biologists, thus more clearly illustrating the effects of noise-induced selection without resorting to tools such as slow manifold analysis that are ubiquitous in physics circles. Lastly, our equations make concrete biological predictions such as systematic deviations from true neutrality despite equal fitness that can, in principle, be directly measured empirically. This work has been accepted for publication in <i>The American Naturalist</i> (<a href='https://doi.org/10.1086/733196'>Bhat and Guttal, 2024</a>). A preprint is also available on <a href='https://www.biorxiv.org/content/10.1101/2024.02.19.580940v1'>bioRxiv</a>. You can also read a Twitter thread about the paper <a href='https://x.com/ShikharaBhat/status/1760427751092166839'>here</a>. I was invited to give a 40 minute talk about this work at a monthly seminar organized by the Drosophila Ecology and Evolution supergroup in India, and you can listen to that talk here:

{% include youtube.html id="vVVWCT62c0c" %}

<br>
<br>

<h1> Part 2: A stochastic field theory for modelling the dynamics of populations bearing quantitative traits </h1>

<div style="text-align: justify">

Phenotypic traits such as human height are often under the influence of a very large number of genes. Due to the complex genetic and epigenetic factors affecting the expression of such phenotypic traits, they take on so many values that they can be said to vary approximately 'continuously' over some interval (Trait values may take all possible values in [0,1], for example). Since infinitely many distinct trait values may arise in populations bearing such 'quantitative' traits, these populations cannot be characterized by a vector or matrix containing the number of individuals bearing each trait value. Instead, the population is best characterized via a function or distribution, and the object describing the state of the system at any given point is thus, in general, infinite-dimensional. While the mathematics of birth-death processes that I described above works well for discrete traits, it is not easily extended to the study of the sort of infinite-dimensional stochastic processes that arise when attempting to model quantitative traits.


<br>
<br>
<div class="row justify-content-sm-center"  style="text-align: center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/discrete_vs_quant_trait_comparison.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
<b>A.</b> If traits vary in a discrete fashion, the entire population can be characterized by a vector that counts the number of each allowed type. For example, if we imagine a population of birds whose plumage comes in one of two colors (here, red and blue), then the population as a whole can be characterized by a two-dimensional vector counting the number of red birds and blue birds in the population. <b>B.</b> If instead the trait varies continuously, individuals can take on uncountably many values. For example, if we imagine a population of birds in which beak length varies continuously, the number of allowed beak lengths is uncountably infinite, and therefore, the population as a whole must be described by a finite measure obtained by placing a Dirac mass for each bird in the population.
</div>
<br>

The mathematicians use something called measure-valued branching processes (MVBPs) to model such processes. However, the theory of MVBPs is still very much in development and is not very accessible to people without formal training in measure theory and functional analysis. In my thesis, I've used heuristic ideas from statistical physics to show that one can still extend the general theory we built for discrete traits above to one-dimensional quantitative traits through a ‘stochastic field theory’. This leads to the formulation of some field equations that yield standard equations of population genetics such as the continuous replicator-mutator equation, Price equation, Kimura's continuum-of-alleles model, and Lande's selection gradient dynamics in the infinite population limit and generalize them to finite populations of non-constant size. The approach consists of describing the population as a stochastic 'field' (function over space and time), assuming there exists an ecological carrying capacity, and then using ideas from statistical physics to derive stochastic equations that describe how this field changes over time when the carrying capacity is not too small. My framework largely only uses tools from calculus, calculus of variations, and some heuristics for spacetime white noise. As such, it complements the rigorous measure-theoretic framework presented in previous studies with a formalism that may be more accessible to those without a background in measure theory. The formulation of field equations also means that we can now use the powerful heuristic tools of field theories in physics such as the path integral formalism to attack questions about the evolution of quantitative traits in finite populations, though I personally do not do this in my work.

The formulation of stochastic field equations for populations bearing quantitative traits using tools from statistical physics is, to the best of our knowledge, also original mathematically and may be of independent interest to applied mathematicians and physicists. The work covering quantitative traits is currently in review in <i>Theoretical Population Biology</i>. A preprint is available on arxiv (<a href='https://arxiv.org/abs/2406.10739'>Bhat, 2024</a>). You can also read a Twitter thread about the paper <a href='https://x.com/ShikharaBhat/status/1802973714297851964'>here</a>. I have spoken about the mathematical ideas and steps involved in a lab meet, and a recording of this talk can be viewed here (this talk assumes that you understand the mathematical ideas used in the discrete trait case, <i>i.e.</i> the mathematics of 'part 1' above):

{% include youtube.html id="Pt_YeEN_b64" %}

<br>
<br>

If any of this interests you, you can feel free to read my MS thesis <a href="https://thepandalorian.github.io/assets/pdf/Shikhara_MS_thesis.pdf">by clicking this link</a> (warning: links to a 175 page PDF). Please don't hesitate to reach out to me if you have any questions or just want to chat about this work!!

</div>
