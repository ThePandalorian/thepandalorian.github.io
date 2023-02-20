---
layout: page
title: Evolution in Finite Populations
description: Modelling stochastic evolutionary dynamics from first principles (MS thesis project)
img: assets/img/evolutionary_branching.png
importance: 1
category: Current
permalink: /projects/MS_thesis
---

<i> June 2022 - Present <br>
Supervisors: Dr. Vishwesha Guttal, Prof. Rohini Balakrishnan</i>

<div style="text-align: justify">

Many central questions of population biology relate to the number of distinct variants of an entity that can emerge and coexist in a closed population. Examples include the study of standing genetic variation (alleles), polymorphisms (genotypes/phenotypes), and sympatric speciation (species). Historically, these questions have often been studied through phenomenological models formulated for infinitely large populations. However, we increasingly realize that demographic stochasticity can have important consequences for evolution. For example, in adaptive diversification models, demographic stochasticity can delay or prevent evolutionary branching in finite populations.
<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/evolutionary_branching.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
Two different realizations of a stochastic individual-based model of resource competition in one dimension where individuals compete according to a continuous  trait analogue of the logistic equation. The model on top has a population of around 1000 individuals, and remains monomorphic. The model on the bottom has a population of around 10000 individuals, and exhibits evolutionary branching, where an initially monomorphic population evolves to become dimorphic. All other model parameters are identical across both simulations.
</div>
<br>

On the other hand, finite population models in population genetics, such as the Wright-Fisher or Moran models, often assume a fixed population size and do not allow populations to fluctuate, limiting their generality. For my Master's dissertation, I am working with <a href='https://teelabiisc.wordpress.com/'>Dr. Vishwesha Guttal</a> and <a href = 'https://sites.google.com/view/rohinibalakrishnanlab/home'>Prof. Rohini Balakrishnan</a> at the Centre for Ecological Sciences at IISc Bangalore to build more general models for evolution in finite populations using ideas from statistical physics and stochastic processes. Starting from a density-dependent ‘birth-death process’ describing an arbitrary closed population of individuals with discrete traits, I derive a set of stochastic differential equations for how trait frequencies change over time. Well-known equations of evolution such as the replicator-mutator equation (from evolutionary game theory), Fisher’s fundamental theorem (from population genetics), and the Price equation are recovered as special cases in the infinite population limit.
<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/schematic_BD_process.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
<b>A.</b> A schematic description of a one-dimensional stochastic birth-death process for a population of identical individuals. The entire population is characterized by the population size, and changes in population size are mediated by density-dependent birth and death rates. On the bottom row, time series of a realization of a stochastic version of the logsitic equation for finite populations in which the carrying capacity is <b>B.</b> 500, <b>C.</b> 1000, and <b>D.</b> 10,000. Here, carrying capacity controls the total population size and thus the amoount of stochasticity. The exact stochastic simulation, various analytical approximations, and the deterministic (infinite population) limit are all plotted. 
</div>
<br>

While the mathematics of birth-death processes works well for discrete traits, it breaks down for quantitative traits such as height, in which individuals can take on uncountably many values and the population is thus characterized by a function and not just a vector. The mathematicians then use something called measure-valued branching processes (MVBPs), but the theory of MVBPs is still very much in develeopment, and is not very accessible to people without formal training in measure theory and functional analysis. In my thesis, I've shown that one can still extend the general idea we used for discrete traits to one-dimensional quantitative traits through a ‘stochastic field theory’ that yields frameworks such as Kimura's continuum-of-alleles, adaptive dynamics, and certain models of intraspecific trait variation in community ecology as special cases. This derivation presents a heuristic alternative to the rigorous but inaccessible models for evolution of quantitative traits that are based in MVBPs. The formulation of field equations also means that we can now use the powerful heuristic tools of physics such as the path integral formalism, though I personally do not do this in my work.
<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/discrete_vs_quant_trait_comparison.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
<b>A.</b> If traits vary in a discrete fashion, the entire population can be characterized by a vector that counts the number of each allowed type. For example, if we imagine a population of birds whose plumage comes in one of two colors (here, red and blue), then the population as a whole can be characterized by a two-dimensional vector counting the number of red birds and blue birds in the population. <b>B.</b> If instead the trait varies continuously, individuals can take on uncountably many values. For example, if we imagine a population of birds in which beak length varies continuously, the number of allowed beak lengths is uncountably infinite, and therefore, the population as a whole must be described by a finite measure obtained by placing a Dirac mass for each bird in the population.
</div>
<br>

Throughout, I make no major assumptions other than density-dependence and the impossibility of infinite growth. The resultant equations reveal a new directional evolutionary force, ‘noise-induced selection’, that is particular to finite populations and has been overlooked in standard mathematical formulations of evolution. This noise-induced selection can act in opposition to classical natural selection, and, if sufficiently strong, can reverse the direction of evolution predicted by infinite-population models, as seen in some recent computational studies. My work thus derives a set of fundamental equations showcasing the common stochastic underpinnings of several formal structures in population biology and predicts a new evolutionary force unique to finite populations.

</div>
