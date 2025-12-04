---
layout: page
title: The Evolution of Ageing
description: Formal models of the developmental theory of ageing
img: assets/img/aging_networks.png
importance: 1
category: Current
permalink: /projects/aging_and_hyperfunction
---

<i> Feb 2024 - Present <br>
Supervisors: Prof. Hanna Kokko</i>

<div style="text-align: justify">

Ageing, or senescence, is the phenomenon of mortality rates of organisms increasing through the course of their lives. Despite senescence having obvious negative fitness consequences (such as death), it is nevertheless a fact of life that most organisms age. Why doesn't natural selection lead to ever-increasing lifespans?  The 'developmental theory of aging' (DTA) suggests that aging evolves due to evolution prioritizing optimization of early-life fitness at the cost of fitness later in life (For example, see <a href="https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.3002513">Lemaître et al. 2024</a>). In other words, if the optimal value of a trait varies with age, the DTA posits that evolution favors optimality early in life even if this comes with a cost later in life. Aging in this framework is thus a consequence of failure to adapt to a changing optimum leading to either hypofunction or hyperfunction in gene regulation, which in turn leads to sub-optimal, and eventually catastrophic, organismal function. I am using tools from mathematical optimization theory and the calculus of variations to formalize this idea and examine when age-dependent optimal trait expression can lead to senescence. For instance, studies of aging routinely assume that selection is weaker later in life (the famous 'selection shadow'). Is a selection shadow really necessary for aging as envivionsed by the DTA? If so, how strong must this shadow be? If not, can aging evolve simply due to limited plasticity in trait expression?

<br>
<br>
<div class="row" style="text-align: center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/aging_as_tipping.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
A schematic depiction of the evolution of ageing as a result of hypofunction/hyperfuuction arising from failure to track a changing optimum.
</div>
<br>

At the proximate level, senescence can be more mechanistically understood via the accumulation of failures of various physiological processes required for organismal function. In this view, an organism is a complex system consisting of many interdependent sub-systems, each with some intrinsic risk of failure due to the vagaries of life. These sub-systems could be genes, organs, tissues, or something more abstract, such as cellular pathways, metabolic functions, or foraging ability. Crucially, in any such conceptualization, the functioning of each sub-part depends on the well-being of other sub-parts. For instance, a faulty heart places additional stresses on lung functioning. Organismal functioning and mortality then depend on the fraction of currently operational sub-parts. For my PhD, I am using mathematical models to study whether such interdependencies are sufficient to reproduce patterns of demographic senescence without invoking a selection shadow.

<br>
<div class="row" style="text-align: center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/aging_networks.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
If ageing is conceptualized as cascading failures in complex interdependent systems, aging rate crucially depends on network structure of interdependencies --- some networks, such as cyclic graphs, show negligible senescence, whereas others, such as complete graphs or graphs with power law degree distributions, exhibit Gompertzian patterns of system failure.
</div>
<br>
</div>

I am currently trying to model such stochastic accumulation of failures as a two-level branching process (one within the individual due to failure and repair of systems, one at the population level due to births and deaths of individuals). Note that the associated Fokker-Planck equation will be non-conservative since individuals can be lost to death. On the stochastics side, the relevant stochastic process modelling such systems is diffusion with killing.
