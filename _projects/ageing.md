---
layout: page
title: The Evolution of Ageing
description: Formal models of ageing via damage accumulation
img: assets/img/ageing_ponies.png
importance: 1
category: Current
permalink: /projects/ageing
---

<i> Feb 2024 - Present <br>
Supervisors: Prof. Hanna Kokko</i>

<div style="text-align: justify">

Ageing, or senescence, is the phenomenon of mortality rates of organisms increasing through the course of their lives. Despite senescence having obvious negative fitness consequences (such as death), it is nevertheless a fact of life that most organisms age. At the proximate level, senescence can be more mechanistically understood via the accumulation of failures of various physiological processes required for organismal function. In this view, an organism is a complex system consisting of many interdependent sub-systems, each with some intrinsic risk of failure due to the vagaries of life. These sub-systems could be genes, organs, tissues, or something more abstract, such as cellular pathways, metabolic functions, or foraging ability. Crucially, in any such conceptualization, the functioning of each sub-part depends on the well-being of other sub-parts. For instance, a faulty heart places additional stresses on lung functioning. Thus, in general, failure begets failure and the failure rate of a sub-system depends on how many sub-systems have already failed. Organismal mortality then depend on the fraction of currently operational sub-parts. For my PhD, I am using mathematical models to build a general framework to formulate and study models that begin with such functional interdependencies and predict patterns of demographic senescence (mortality curves). 
<br>
<br>
So far, we have built some general models to study how selective disappearance induced by stochastic mortality risk alters the predictions of failure accumulation models. Specifically, we start with a general birth-death framework where the number of failed sub-systems within an individual either increases or decreases stochastically due to failure and repair respectively. Mortality is modelled as an additional stochastic rate at which each individual transitions to an unobserved 'cemetery state' and thus disappears from the population. Using diffusion approximations, we then analytically derive expressions showing how selective disappearance systematically alters observed failure and mortality accumulation curves. A fundamental result from mathematics called the Feynman-Kac formula lets us relate measurements made on organisms how measurements made on populations with selective disappearance can be represented in terms of the failure accumulation process alone where mortality is disallowed. Along the way, we also propose some tentative criteria that failure accumulation and mortality rates should obey based on biological principles and show that these criteria generically lead to Gompertz-Makeham and logistic (Perks) mortality curves during the initial part of the failure accumulation process.
<br>
I am now trying to extend these kinds of models to allow for variable finite cohort/sample sizes and births of individual, bringing in the possibility of studying eco-evolutionary dynamics for such systems by tracking mortality patterns over multiple generations. Below, I provide an outline of the general flavour of models I am currently thinking about.
</div>
<br>
<br>

Consider a cohort consisting of $$M$$ independent, non-interacting organisms. Each organism has $$N$$ sub-systems capable of failure. Within the $$i$$th organism, $$F^{(i)}_t$$, the number of failed sub-systems at time $$t$$, follows a density-dependent birth-death process on $$\{0,1,2,\cdots,N\}$$ with transition rates $$F \to F \pm 1 \textrm{ at rate } Nr_{\pm}(F/N)$$, corresponding to stochastic failure and repair of failed sub-systems. This defines the individual-level dynamics. At the population level, one of two variants are considered. In the <i>non-conservative</i> model, an individual with $$F \in \{0,1,2,..,N\}$$ failures is chosen to die at rate $$\mu(F/N)$$. Thus, the population-level dynamics consist of individuals disappearing from the population at a rate equal to their mortality hazard. In the <i>conservative</i> model, an individual chosen for death is instantaneously replaced by a copy of another individual, chosen uniformly at random from the population of $$M$$ organisms, ensuring that the total population size remains constant. Thus, in the latter case, the population-level dynamics are described by a Moran process with selection and Death-birth updating. We can reframe this as a sub-probability measure-valued stochastic process with state variable

$$
\xi^{M,N}_t(\cdot) = \frac{1}{M}\sum\limits_{i=1}^{M}\delta_{f^{(i)}_t}(\cdot)
$$

where $$f^{(i)}_t = F^{(i)}_t/N$$ is a rescaled version of the individual-level process governing failure dynamics. The stochastic process $$\{\xi^{M,N}_t\}_{t \geq 0}$$ tracks the proportion of individuals in the population having a proportion $$f = F/N$$ failed sub-systems, and takes values in the space of sub-probability measures on $$\{0,\frac{1}{N},\frac{2}{N},\ldots,1\}$$. 

<br>
<div class="row" style="text-align: center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/MLS_ageing.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
A description of a two level stochastic process for modelling mortality curves and senescence patterns. <b>(A)</b> The model consists of <i>M</i> organisms, each of which have <i>N</i> intra-organismal sub-systems capable of failure. <b>(B)</b> An organism with <i>f = F/N</i> failures may either accumulate another failure, repair a failed sub-system, or die. Death is either without replacement or with instantaneous replacement by another individual chosen uniformly at random from the population. <b>(C)</b> We characterise the population via a ball and urn scheme by counting the number of organisms that have <i>f = F/N</i> failures for each posssible value of <i>f</i>, and then dividing this number by the initial population size <i>M</i>.
</div>
<br>



If we first take $$M \to \infty$$ (very large cohort size) and then use a diffusion approximation on $$N$$ by neglecting terms of $$\mathcal{O}(N^{-2})$$, it can be shown that the stochastic process $$\{\xi^{M,N}_t\}_{t \geq 0}$$ converges to a deterministic measure $$P(f,t)$$ described by the Fokker-Planck-Kolmogorov type PDE
 
$$
\frac{\partial P(f,t)}{\partial t} =  -\frac{\partial}{\partial f}\{r(f)P(f,t)\} + \frac{1}{2N}\frac{\partial^2}{\partial f^2}\{\tau(f)P(f,t)\} - \left(\mu(f) - \mathbb{1}_{R}\int\limits_0^1\mu(x)P(x,t)dx\right)P(f,t)
$$

where $$r(f) = r_{+}(f) - r_-(f), \tau(f) = r_{+}(f) + r_-(f)$$, and $$\mathbb{1}_{R} = 1$$ if we are considering the model with instantaneous replacement and 0 otherwise. The PDE is conservative in the former case and non-conservative in the latter. Curiously, from a stochastic process perspective, the PDE above with $$\mathbb{1}_{R} = 0$$ is precisely the Kolmogorov forward equation for a well-known stochastic process called <i>diffusion with killing</i> with instantaneous killing rate $$\mu$$. The PDE with $$\mathbb{1}_{R} = 1$$ describes the conditional probability density of this same stochastic process conditioned on non-absorption/survival. Furthermore, on biological grounds, we are able to argue that we often expect $$r(f)$$ to take the form $$r(f) = \lambda(1-f)(\phi + kf)$$ for positive constants $$\lambda, \phi, k$$. Similar equations with $$\phi = k = 1$$ appear in multi-level selection theory and the evolution of cooperation literature if we interpret mortality as a negative payoff. We are currently writing up much of these results as a manuscript.

<div style="text-align: justify">
 I am interested in trying to more thoroughly understand how to translate known results between multi-level selection and the evolution of senescence using these PDEs. I am also interested in understanding the biological consequences of the fact that the conservative version of the PDE can both be interpreted as a deterministic model of an infinitely large population (as the scaling limit of the stochastic process above, as used in MLS) and as a stochastic model of a single individual with failure, repair, and mortality risk conditioned on survival of the individual (as arising from the generator of a diffusion with killing; similar things have been used in senescence/demography literature). I am currently trying to do this via Feynman-Kac techniques but overall remain somewhat befuddled.
 </div>
 <br>

 There are also other scaling limits of $$\{\xi^{M,N}_t\}_{t \geq 0}$$ that are biologically interesting and natural. For instance, for a closely related model arising in multi-level selection theory, <a href='https://iopscience.iop.org/article/10.1088/1361-6544/aa5499'>Luo and Mattingly 2017</a> have characterised the limit $$M\to\infty, N\to \infty, N/M \to \theta < \infty$$ using martingale techniques. For senescence, the most biologically pertinent limit is $$N \to \infty, M < \infty$$ (very large number of sub-systems within each organism, limited cohort size), but in this limit, the process is a scary measure-valued branching process on the space of sub-probability measures on $$[0,1]$$ that I don't really understand yet :(

