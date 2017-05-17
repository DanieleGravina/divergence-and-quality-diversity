## What is it?

A collection of papers on divergence and quality diversity

## Table of Contents

- [What is it?](#what-is-it)
- [Divergent Search](#divergent-search)
- [Quality Diversity?](#quality-diversity)
- [Novelty Search](#novelty-search)
- [Novelty Search Multiobjectivation](#novelty-search-multiobjectivation)
- [Novelty Search Local Competition](#novelty-search-local-competition)
- [Map-elites](#map-elites)
- [Quality diversity](#quality-diversity)
- [Constrained novelty search](#constrained-novelty-search)
- [DeLeNoX](#deLeNoX)
- [Surprise Search](#surprise-search)
- [Minimal Criterion Coevolution](#minimal-criterion-coevolution)

## Divergent Search

The widely accepted approach in search is to design a
function that will reward solutions with respect to a particular
objective that characterizes their goodness: better
solutions have higher values with respect to that objective.
In evolutionary computation the fitness function
encapsulates the principle of evolutionary pressure for fitting
(adapting) within the environment. While it is natural
to think that measuring progress in terms of fitness
is the most appropriate approach towards finding a high-fit
solution, recent findings from evolutionary divergent search
suggest that explicit objective (fitness) design can be
detrimental to evolutionary search. Instead, aspects of divergent
search beyond objectives — such as novelty — have
proven more efficient in a number of tasks such as robot
navigation and locomotion.
The effectiveness of a fitness function in EC is largely affected by 
the multimodality of the search space and the local optima that may
exist in the fitness landscape. In turn, a fitness function
attributes deceptive characteristics to the search space
such as roughness and epistasis. On that basis, an ill-posed
fitness acts against the problem’s objective as it drives the
algorithm to undesired directions in the search space.
While search towards a particular objective is a dominant
practice within EC and machine learning at large, no explicit
objectives are considered in open-ended evolution studies
within artificial life. Instead, it is typical to consider
open-ended search for e.g. survival. Most importantly
for this paper, a large body of research within computational
creativity and generative systems focuses on the
creative capacity of search rather than on the objectives,
since creativity is a human-centric and highly subjective notion
that cannot be easily formalized. Instead of objectives,
particular dimensions of creativity such as value and novelty
define dominant directions for the search towards
creative outcomes or unconventional solutions to problems.

## Quality Diversity


## Novelty search

<b>Abstract:</b>

<blockquote> In evolutionary computation, the fitness function normally measures
progress towards an objective in the search space, effectively acting as an objective
function. Through deception, such objective functions may actually prevent
the objective from being reached. While methods exist to mitigate deception,
they leave the underlying pathology untreated: Objective functions themselves
may actively misdirect search towards dead ends. This paper proposes an
approach to circumventing deception that also yields a new perspective on
open-ended evolution: Instead of either explicitly seeking an objective or
modeling natural evolution to capture open-endedness, the idea is to simply
search for behavioral novelty. Even in an objective-based problem, such novelty
search ignores the objective. Because many points in the search space collapse
to a single behavior, the search for novelty is often feasible. Furthermore,
because there are only so many simple behaviors, the search for novelty leads
to increasing complexity. By decoupling open-ended search from artificial life
worlds, the search for novelty is applicable to real world problems. Counterintuitively,
in the maze navigation and biped walking tasks in this paper,
novelty search significantly outperforms objective-based search, suggesting the
strange conclusion that some problems are best solved by methods that ignore
the objective. The main lesson is the inherent limitation of the objective-based
paradigm and the unexploited opportunity to guide search through other means. </blockquote>

http://eplex.cs.ucf.edu/papers/lehman_ecj11.pdf

source code : http://eplex.cs.ucf.edu/software/NoveltySearchC++.zip

http://eplex.cs.ucf.edu/noveltysearch/userspage/

		
@article{lehman2011abandoning,<br>
title={Abandoning objectives: Evolution through the search for novelty alone},<br>
  author={Lehman, Joel and Stanley, Kenneth O},<br>
  journal={Evolutionary computation},<br>
  volume={19},<br>
  number={2},<br>
  pages={189--223},<br>
  year={2011},<br>
  publisher={MIT Press}	}


## Novelty search multiobjectivation

<b>Abstract:</b>

<blockquote> Novelty search is a recent and promising approach to evolve neurocontrollers, especially to drive robots. The main idea is to maximize the novelty of behaviors instead of the efficiency. However, abandoning the efficiency objective(s) may be too radical in many contexts. In this paper, a Pareto-based multi-objective evolutionary algorithmis employed to reconcile novelty search with objective-based optimization by following a multiobjectivization process. Several multiobjectivizations based on behavioral novelty and on behavioral diversity are compared on a maze navigation task. Results show that the bi-objective variant “Novelty + Fitness” is better at fine-tuning behaviors than basic novelty search, while keeping a comparable number of iterations to converge. </blockquote>

https://www.researchgate.net/publication/225729412_Novelty-Based_Multiobjectivization

@incollection{mouret2011novelty,<br>
  title={Novelty-based multiobjectivization},<br>
  author={Mouret, Jean-Baptiste},<br>
  booktitle={New horizons in evolutionary robotics},<br>
  pages={139--154},<br>
  year={2011},<br>
  publisher={Springer}<br>
}

## Novelty search local competition

<b>Abstract:</b>

<blockquote> An ambitious challenge in artificial life is to craft an evolutionary
process that discovers a wide diversity of welladapted
virtual creatures within a single run. Unlike in nature,
evolving creatures in virtual worlds tend to converge
to a single morphology because selection therein greedily rewards
the morphology that is easiest to exploit. However,
novelty search, a technique that explicitly rewards diverging,
can potentially mitigate such convergence. Thus in this
paper an existing creature evolution platform is extended
with multi-objective search that balances drives for both
novelty and performance. However, there are different ways
to combine performance-driven search and novelty search.
The suggested approach is to provide evolution with both a
novelty objective that encourages diverse morphologies and
a local competition objective that rewards individuals outperforming
those most similar in morphology. The results
in an experiment evolving locomoting virtual creatures show
that novelty search with local competition discovers more
functional morphological diversity within a single run than
models with global competition, which are more predisposed
to converge. The conclusions are that novelty search with
local competition may complement recent advances in evolving
virtual creatures and may in general be a principled approach
to combining novelty search with pressure to achieve.</blockquote>

https://pdfs.semanticscholar.org/6d45/9da1ff73ec7225e92842341605e2b90d0da2.pdf

@inproceedings{lehman2011evolving,<br>
  title={Evolving a diversity of virtual creatures through novelty search and local competition},<br>
  author={Lehman, Joel and Stanley, Kenneth O},<br>
  booktitle={Proceedings of the 13th annual conference on Genetic and evolutionary computation},<br>
  pages={211--218},<br>
  year={2011},<br>
  organization={ACM}<br>
}

## Map elites

<b>Abstract:</b>

<blockquote>Nearly all science and engineering fields use search algorithms,
which automatically explore a search space to
find high-performing solutions: chemists search through the
space of molecules to discover new drugs; engineers search
for stronger, cheaper, safer designs, scientists search for
models that best explain data, etc. The goal of search algorithms
has traditionally been to return the single highestperforming
solution in a search space. Here we describe a
new, fundamentally different type of algorithm that is more
useful because it provides a holistic view of how highperforming
solutions are distributed throughout a search
space. It creates a map of high-performing solutions at each
point in a space defined by dimensions of variation that
a user gets to choose. This Multi-dimensional Archive of
Phenotypic Elites (MAP-Elites) algorithm illuminates search
spaces, allowing researchers to understand how interesting
attributes of solutions combine to affect performance,
either positively or, equally of interest, negatively. For example,
a drug company may wish to understand how performance
changes as the size of molecules and their costto-produce
vary. MAP-Elites produces a large diversity of
high-performing, yet qualitatively different solutions, which
can be more helpful than a single, high-performing solution.
Interestingly, because MAP-Elites explores more of the
search space, it also tends to find a better overall solution
than state-of-the-art search algorithms. We demonstrate the
benefits of this new algorithm in three different problem domains
ranging from producing modular neural networks to
designing simulated and real soft robots. Because MAPElites
(1) illuminates the relationship between performance
and dimensions of interest in solutions, (2) returns a set
of high-performing, yet diverse solutions, and (3) improves
the state-of-the-art for finding a single, best solution, it will
catalyze advances throughout all science and engineering
fields.</blockquote>

https://arxiv.org/pdf/1504.04909.pdf

@article{mouret2015illuminating,<br>
  title={Illuminating search spaces by mapping elites},<br>
  author={Mouret, Jean-Baptiste and Clune, Jeff},<br>
  journal={arXiv preprint arXiv:1504.04909},<br>
  year={2015}<br>
}

source code: https://github.com/sferes2/map_elites

## Quality diversity

<b>Abstract:</b>

<blockquote>While evolutionary computation and evolutionary robotics take inspiration from nature,
they have long focused mainly on problems of performance optimization. Yet, evolution
in nature can be interpreted as more nuanced than a process of simple optimization. In
particular, natural evolution is a divergent search that optimizes locally within each niche
as it simultaneously diversifies. This tendency to discover both quality and diversity at the
same time differs from many of the conventional algorithms of machine learning, and also
thereby suggests a different foundation for inferring the approach of greatest potential
for evolutionary algorithms. In fact, several recent evolutionary algorithms called quality
diversity (QD) algorithms (e.g., novelty search with local competition and MAP-Elites)
have drawn inspiration from this more nuanced view, aiming to fill a space of possibilities
with the best possible example of each type of achievable behavior. The result is a new
class of algorithms that return an archive of diverse, high-quality behaviors in a single
run. The aim in this paper is to study the application of QD algorithms in challenging
environments (in particular complex mazes) to establish their best practices for ambitious
domains in the future. In addition to providing insight into cases when QD succeeds and
fails, a new approach is investigated that hybridizes multiple views of behaviors (called
behavior characterizations) in the same run, which succeeds in overcoming some of the
challenges associated with searching for QD with respect to a behavior characterization
that is not necessarily sufficient for generating both quality and diversity at the same time.</blockquote>

http://journal.frontiersin.org/article/10.3389/frobt.2016.00040/pdf

@article{pugh2016quality,<br>
  title={Quality diversity: A new frontier for evolutionary computation},<br>
  author={Pugh, Justin K and Soros, Lisa B and Stanley, Kenneth O},<br>
  journal={Frontiers in Robotics and AI},<br>
  volume={3},<br>
  pages={40},<br>
  year={2016},<br>
  publisher={Frontiers}<br>
}

## Constrained novelty search

<b>Abstract:</b>

<blockquote>Novelty search is a recent algorithm geared towards exploring search spaces without
regard to objectives. When the presence of constraints divides a search space into feasible
space and infeasible space, interesting implications arise regarding how novelty
search explores such spaces. This paper elaborates on the problem of constrained novelty
search and proposes two novelty search algorithms which search within both the
feasible and the infeasible space. Inspired by the FI-2pop genetic algorithm, both algorithms
maintain and evolve two separate populations, one with feasible and one with
infeasible individuals, while each population can use its own selection method. The
proposed algorithms are applied to the problem of generating diverse but playable
game levels, which is representative of the larger problem of procedural game content
generation. Results show that the two-population constrained novelty search
methods can create, under certain conditions, larger and more diverse sets of feasible
game levels than current methods of novelty search, whether constrained or unconstrained.
However, the best algorithm is contingent on the particularities of the
search space and the genetic operators used. Additionally, the proposed enhancement
of offspring boosting is shown to enhance performance in all cases of two-population
novelty search.
</blockquote>

http://antoniosliapis.com/papers/constrained_novelty_search.pdf

http://antoniosliapis.com/research/novsearch.php

@article{liapis2015constrained,<br>
  title={Constrained novelty search: A study on game content generation},<br>
  author={Liapis, Antonios and Yannakakis, Georgios N and Togelius, Julian},<br>
  journal={Evolutionary computation},<br>
  volume={23},<br>
  number={1},<br>
  pages={101--129},<br>
  year={2015},<br>
  publisher={MIT Press}<br>
}

## DeLeNoX

<b>Abstract:</b>

<blockquote> 
We introduce DeLeNoX (Deep Learning Novelty Explorer),
a system that autonomously creates artifacts in
constrained spaces according to its own evolving interestingness
criterion. DeLeNoX proceeds in alternating
phases of exploration and transformation. In the exploration
phases, a version of novelty search augmented
with constraint handling searches for maximally diverse
artifacts using a given distance function. In the transformation
phases, a deep learning autoencoder learns to
compress the variation between the found artifacts into
a lower-dimensional space. The newly trained encoder
is then used as the basis for a new distance function,
transforming the criteria for the next exploration phase.
In the current paper, we apply DeLeNoX to the creation
of spaceships suitable for use in two-dimensional
arcade-style computer games, a representative problem
in procedural content generation in games. We also situate
DeLeNoX in relation to the distinction between exploratory
and transformational creativity, and in relation
to Schmidhuber’s theory of creativity through the drive
for compression progress.
</blockquote>

http://julian.togelius.com/Liapis2013Transforming.pdf

http://antoniosliapis.com/research/novsearch.php

@inproceedings{liapis2013transforming,<br>
  title={Transforming exploratory creativity with DeLeNoX},<br>
  author={Liapis, Antonios and Mart{\i}nez, H{\'e}ctor P and Togelius, Julian and Yannakakis, Georgios N},<br>
  booktitle={Proceedings of the Fourth International Conference on Computational Creativity},<br>
  pages={56--63},<br>
  year={2013},<br>
  organization={AAAI Press}<br>
}

## Surprise search

<b>Abstract:</b>

<blockquote>
Grounded in the divergent search paradigm and inspired
by the principle of surprise for unconventional discovery
in computational creativity, this paper introduces surprise
search as a new method of evolutionary divergent search.
Surprise search is tested in two robot navigation tasks and
compared against objective-based evolutionary search and
novelty search. The key findings of this paper reveal that
surprise search is advantageous compared to the other two
search processes. It outperforms objective search and it is
as efficient as novelty search in both tasks examined. Most
importantly, surprise search is, on average, faster and more
robust in solving the navigation problem compared to objective
and novelty search. Our analysis reveals that surprise
search explores the behavioral space more extensively
and yields higher population diversity compared to novelty
search.
</blockquote>

http://antoniosliapis.com/papers/surprise_search_beyond_objectives_and_novelty.pdf

http://www.autogamedesign.eu/surprise-search

@inproceedings{gravina2016surprise,<br>
  title={Surprise search: Beyond objectives and novelty},<br>
  author={Gravina, Daniele and Liapis, Antonios and Yannakakis, Georgios},<br>
  booktitle={Proceedings of the 2016 on Genetic and Evolutionary Computation Conference},<br>
  pages={677--684},<br>
  year={2016},<br>
  organization={ACM}<br>
}

## Minimal criterion coevolution

<b>Abstract:</b>

<blockquote>
Recent studies have emphasized the merits of search processes
that lack overarching objectives, instead promoting divergence
by rewarding behavioral novelty. While this less objective search
paradigm is more open-ended and divergent, it still diers signicantly
from nature’s mechanism of divergence. Rather than
measuring novelty explicitly, nature is guided by a single, fundamental
constraint: survive long enough to reproduce. Surprisingly,
this simple constraint produces both complexity and diversity in a
continual process unparalleled by any algorithm to date. Inspired
by the relative simplicity of open-endedness in nature in comparison
to recent non-objective algorithms, this paper investigates
the extent to which interactions between two coevolving populations,
both subject to their own constraint, or minimal criterion, can
produce results that are both functional and diverse even without
any behavior characterization or novelty archive. To test this new
approach, a novel maze navigation domain is introduced wherein
evolved agents must learn to navigate mazes whose structures are
simultaneously coevolving and increasing in complexity. e result
is a broad range of maze topologies and successful agent trajectories
in a single run, thereby suggesting the viability of minimal criterion
coevolution as a new approach to non-objective search and a step
towards genuinely open-ended algorithms.
</blockquote>

http://eplex.cs.ucf.edu/papers/brant_gecco17.pdf

@inproceedings{brant2017minimal,<br>
  title={Minimal Criterion Coevolution},<br>
  author={Brant, Jonathan C and  Stanley, Kenneth O},<br>
  booktitle={Proceedings of the 2017 on Genetic and Evolutionary Computation Conference},<br>
  year={2017},<br>
  organization={ACM}<br>
}

Source code: https://github.com/jbrant/MinimalCriterionCoevolution/releases/
