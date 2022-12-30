---
layout: page
title: Projects
permalink: /projects/
description: 
nav: true
horizontal: false
---

## <b> Current Projects </b>
<br>

<b> <font size="5">  
Demographic stochasticity in adaptive diversification models for the evolution of polymorphisms
</font>  </b> 

<i> June 2022 - Present <br>
Supervisors: Dr. Vishwesha Guttal, Prof. Rohini Balakrishnan</i>

<div class="row">
    <div class="col-sm mt-3 mt-md-0" style="text-align: center">
        <img class="img-fluid rounded z-depth-1" src="/assets/img/evolutionary_branching.png" alt="" title="" />
    </div>
</div>
<div class="caption" style="text-align: center">
Two different realizations of stochastic individual-based model of resource competition in one dimension where individuals compete according to a continuous version of the logistic equation, written in Python. The model on top has a population of around 1000 individuals, and remains monomorphic. The model on the bottom has a population of around 10000 individuals, and exhibits evolutionary branching, where an initially monomorphic population evolves to become dimorphic. All other model parameters are identical across both simulations.
</div>

<div style="text-align: justify">
The creation and coexistence of multiple phenotypically distinct, ecologically relevant variants of an organism in sympatry is important in several different contexts in the natural world. Examples include alternative reproductive tactics, trophic resource polymorphisms, and mating types in isogamous species. In many cases, even though the emergent alternative morphs are discretely distributed, the underlying heritable traits are continuously varying due to the influence of a large number of genes. In the case of quantitative traits, an idea called 'adaptive diversification', where an initially monomorphic population evolves to become polymorphic due to frequency-dependent selection, is often used as an explanation for the creation and maintenance of phenotypic polymorphism. Adaptive diversification has traditionally been addressed in three broad modeling frameworks: 'Adaptive dynamics', which crucially assumes infinite population sizes and separation of timescales between ecology and evolution; PDE models, which relax the latter assumption but retain the former one; and stochastic individual-based models, which relax both assumptions. All three predict that diversification is a robust phenomenon, in the sense of occurring in a wide variety of ecological contexts. However, theory often predicts branching to be prolific even for weak frequency dependence, and furthermore, predicts much quicker and easier branching as well as an exponential increase in the number of coexisting morphs as the dimensionality of the trait space increases. Since organisms generally live in rather high-dimensional trait spaces, if we were to go by the theory, we may expect an extremely high diversity of phenotypic polymorphism to be the norm in nature. Empirical insights suggest that this is a rather terrible prediction, and furthermore, the all-too-common prediction of infinite branching that often comes with Gaussian functional forms in adaptive dynamics formalisms is useless for explaining why different organisms may have different degrees of polymorphism. What may explain this disagreement between theory and data, and how may we remedy it? One major culprit may be the assumption of infinite population size. Intuitively, larger demographic stochasticity can lead to lower diversity due to the stochastic elimination of rare mutants regardless of their fitness advantage, in stark contrast to the 'invasion implies fixation' paradigm of deterministic models such as adaptive dynamics. Larger demographic stochasticity also leaves populations with less 'access' to mutations per unit time, which may explain why studies have consistently observed a larger wait time to diversification with increasing demographic stochasticity. For my Master's dissertation, I am working with Dr. Vishwesha Guttal and Prof. Rohini Balakrishnan at the Centre for Ecological Sciences at IISc Bangalore to investigate the expected number of distinct morphs that can be harbored in a finite population using stochastic birth-death processes constructed from first principles.
<!---
Discrete phenotypic polymorphisms, where individuals of a single species are present in more than one distinct phenotype, are ubiquitous in nature. These polymorphisms occur in ecologically important scenarios such as mate choice (alternative reproductive tactics) and foraging (trophic resource polymorphisms). Evolutionary branching, the phenomenon of diversification of an initially monomorphic population due to frequency-dependent selection, is a useful framework in which to study the evolution and maintenance of discrete polymorphisms. Studying the factors affecting the diversity of polymorphisms maintained in a system could in turn could provide more general insights into the role of frequency-dependent selection in speciation and the creation and maintenance of biodiversity. Evolutionary branching has historically been examined through the lens of adaptive dynamics, a certain off-shoot of evolutionary game theory which allows for continuously varying strategies and non-linear payoff functions between strategies (Corresponding to nonlinear games such as playing-the-field games in EGT). A well-known theoretical result relating to the concept of limiting similarity dictates that in the context of resource competition, populations in which the trait space has more dimensions generally harbour more polymorphisms at equilibrium. However, this result has been formulated in the infinite species limit, whereas in real life, demographic stochasticity plays an important role. For my Master's dissertation, I am working with Dr. Vishwesha Guttal and Dr. Rohini Balakrishnan at the Indian Institute of Science (IISc), where I wish to examine the interplay between demographic stochasticity (population size) and dimensionality of the trait space in determining the expected diversity of polymorphisms in populations of competing individuals.
--->
</div>

<br>


<b> <font size="5">  
Fitness benefits of alternative reproductive tactics in tree crickets
</font>  </b> 

<i> Jan 2021 - Present <br>
Supervisors: Prof. Rohini Balakrishnan, Dr. Vishwesha Guttal</i>

<div class="row">
    <div class="col-sm mt-3 mt-md-0" style="text-align: center">
        <img class="img-fluid rounded z-depth-1" width = "700" height = "430" src="/assets/img/cricket_IbM.gif" alt="" title="" />
    </div>                                              
</div>
<div class="caption" style="text-align: center">
   IbM consisting of <i>Oecanthus henryi</i> females moving towards and mating with males which exhibit various kinds of strategies.
</div>

<div style="text-align: justify">
Males of the tree cricket <i>Oecanthus henryi</i> use one of three distinct alternative reproductive tactics (ARTs) to obtain mates:

<ul>

    <li> <i>Bafflers</i> construct an acoustic structure called a `baffle' using leaves and call from within this baffle. The baffle increases the amplitude of their calls, and females are known to prefer louder males. </li>
    <li> <i>Callers</i> simply call from perches to attract mates. The amplitude of the call of a caller is less than that of a baffler. </li>
    <li> <i>Silent males</i> do not call at all, and simply wait silently for females. </li>
</ul>
 
In collaboration with Mohammed Aamir Sadiq, a Ph.D. student in Dr. Rohini Balakrishnan's lab at IISc, I have constructed an individual-based model (IbM) with extensive inputs from field and laboratory experiments. Using this model, we are examining how baffling trait frequency and spatial structure affect the reproductive success of these three male alternative reproductive tactics over ecological timescales.
</div>

<br>
<br>
## <b> Previous Projects </b>
<br>
<b> <font size="5">  
Ecological stability of Lotka-Volterra communities
</font>  </b> 

<i> May 2021 - Dec 2021 <br>
Supervisor: Prof. Sutirth Dey </i>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="/assets/img/bacteria.png" alt="" title="" />
    </div>
</div>
<div class="caption">
    Differential survival of members of a Lotka-Volterra community following a perturbation from equilibrium. The community on the right has a much higher proportion of mutualistic interactions than the one on the left, showing that an increase in the proportion of mutualistic interactions destabilizes communities (self-written Python implementation of an IbM originally formulated by <a href = "https://science.sciencemag.org/content/350/6261/663.abstract">Coyte <i>et al.</i> 2015</a>)
</div>

<div style="text-align: justify">
Which processes govern the stability of ecological communities in nature? Can the particular types of interactions present in a community affect its stability?<br>
In the summer of 2021, I worked with Suryadeepto Nag, a fellow undergraduate at IISER Pune, in <a href = "https://sites.google.com/a/acads.iiserpune.ac.in/sdlab/pbl-iiser-p">Dr. Sutirth Dey's lab</a>, where I used mathematical and computational tools to try and understand how the distribution of interaction types (mutualism, competition, and exploitation) affect the dynamics of Lotka-Volterra communities (Bhat <i>et al.</i> in prep).

</div>
<br>
<b> <font size="5">  
Modeling evolution of novel castes in (eusocial) ants
</font>  </b>

<i> July 2020 - Oct 2020 <br>
Supervisors: - </i>
<div style="text-align: justify">
How do novel specialized castes evolve in ants if workers do not reproduce and castes are often only useful after being sufficiently specialized? During the fall semester of 2020 (Aug 2020 – Dec 2020), I worked with Suryadeepto Nag, a fellow undergraduate, to independently formulate a (very) simple mathematical model for how discrete novel phenotypes may evolve in eusocial colonies. This model used some general principles from economics and optimization theory to mathematically formalize concepts first articulated as a verbal model by Dr. Matheiu Molet’s group in 2012 <a href='https://www.journals.uchicago.edu/doi/10.1086/667368'>(Molet <i>et al.</i> 2012)</a>. With some inputs, comments, and guidance from Dr. Sutirth Dey from IISER Pune and Dr. Raghavendra Gadagkar from IISc, this work has led to a paper in <i>Heliyon</i> (Nag and Bhat, 2022).
</div>
<br>
<b> <font size="5">  
Context-dependent vocal sequences in frogs
</font>  </b>

<i> June 2019 - Aug 2020 <br>
Supervisors: Dr. Anand Krishnan, Dr. Seshadri K.S.</i>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="/assets/img/pseudophilautus.png" alt="" title="" />
    </div>
</div>
<div class="caption" style="text-align: left">
   Left: Two male <i>Pseudophilautus amboli</i> engaged in male-male combat; Right: Co-occurrence analysis for <i>P. amboli</i>. Co-occurrence analysis is a computational tool we developed to look for higher-order vocal sequence patterns in animal vocalizations.
</div>
<div style="text-align: justify">
Do frogs use different types of vocal sequences in different contexts? If so, how may sequence structure vary with social context? I spent the monsoon of 2019 recording vocalizations of <i>Nyctibatrachus humayuni</i>, a frog with a simple two-note repertoire, and the monsoon of 2020 recording the vocalizations of <i>Pseudophilautus amboli</i>, a frog with a complex six-note repertoire, to try to answer these questions. This work was conducted as two summer projects in
 <a href = "https://sites.google.com/view/eceb-lab/home">Dr. Anand Krishnan's lab</a> at IISER Pune and in collaboration with <a href = "http://seshadriks.weebly.com/">Dr. Seshadri K.S.</a>, a postdoc in <a href = "https://mariathaker.weebly.com/">Dr. Maria Thaker’s lab</a> at IISc. We uncovered evidence that anurans change vocal sequence structure based on behavioral context, and do so in diverse ways. As part of this project, I developed a novel computational technique for analyzing vocal sequence that has since found more general applications in describing and studying the syntactic structure of animal vocalizations (Jagan <i>et al.</i> 2022). This technique, which we call `co-occurrence analysis', is a more robust alternative to the common technique of obtaining transition probability matrices to describe vocal sequence structure by assuming the underlying processes are low-order Markovian (an assumption that we know is often not justified). The findings of these two years have now been published as a in <i>Animal Behaviour</i> <a href='https://doi.org/10.1016/j.anbehav.2021.12.004'>(Bhat <i>et al.</i> 2022)</a>. You can listen to me talk on the topic <a href = 'https://www.youtube.com/watch?v=QCsX88lTaos'>here</a>. The presentation got me selected as a finalist for SICB's Marlene Zuk best student presentation award in 2022.
</div>



