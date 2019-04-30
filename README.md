[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

## What is it?

A collection of papers on divergence and quality diversity.

## Table of Contents

- [What is it?](#what-is-it)
- [Divergent algorithms](#divergent-algorithms)
- [Novelty Search](#novelty-search)
- [DeLeNoX](#deLeNoX)
- [Curiosity Search](#Curiosity-Search)
- [Surprise Search](#surprise-search)
- [Coupling Novelty and Surprise for Evolutionary Divergence](#coupling-novelty-and-surprise-for-evolutionary-divergence)
- [Minimal Criterion Coevolution](#minimal-criterion-coevolution)
- [SHINE](#shine)
- [Quality Diversity algorithms](#quality-diversity-algorithms)
- [Novelty Search Multiobjectivation](#novelty-search-multiobjectivation)
- [Novelty Search with Local Competition](#novelty-search-with-local-competition)
- [Map-Elites](#map-elites)
- [Quality diversity](#quality-diversity)
- [Constrained novelty search](#constrained-novelty-search)
- [Quality and Diversity Optimization: A Unifying Modular Framework](#quality-and-diversity-optimization)
- [Surrogate-Assisted Illumination (SAIL)](#surrogate-assisted-illumination-(sail))
- [Quality Diversity Through Surprise](#quality-diversity-through-surprise)
- [Go-Explore](#go-explore)
- [Constrained Map-Elites](#constrained-map-elites)
- [Map-Elites with Sliding Boundaries](#map-elites-with-sliding-boundaries)

## Divergent algorithms

### Novelty Search

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

```		
@article{lehman2011abandoning,
title={Abandoning objectives: Evolution through the search for novelty alone},
  author={Lehman, Joel and Stanley, Kenneth O},
  journal={Evolutionary computation},
  volume={19},
  number={2},
  pages={189--223},
  year={2011},
  publisher={MIT Press}	}
```
### DeLeNoX

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

```
@inproceedings{liapis2013transforming,
  title={Transforming exploratory creativity with DeLeNoX},
  author={Liapis, Antonios and Mart{\i}nez, H{\'e}ctor P and Togelius, Julian and Yannakakis, Georgios N},
  booktitle={Proceedings of the Fourth International Conference on Computational Creativity},
  pages={56--63},
  year={2013},
  organization={AAAI Press}
}
```

### Curiosity Search

<b>Abstract:</b>

<blockquote> 
Natural animals are renowned for their ability to acquire a diverse and general skill set over the course of their lifetime. However, research in artificial intelligence has yet to produce agents that acquire all or even most of the available skills in non-trivial environments. One candidate algorithm for encouraging the production of such individuals is Novelty Search, which pressures organisms to exhibit different behaviors from other individuals. However, we hypothesized that Novelty Search would produce sub-populations of specialists, in which each individual possesses a subset of skills, but no one organism acquires all or most of the skills. In this paper, we propose a new algorithm called Curiosity Search, which is designed to produce individuals that acquire as many skills as possible during their lifetime. We show that in a multiple-skill maze environment, Curiosity Search does produce individuals that explore their entire domain, while a traditional implementation of Novelty Search produces specialists. However, we reveal that when modified to encourage intra-life behavioral diversity, Novelty Search can produce organisms that explore almost as much of their environment as Curiosity Search, although Curiosity Search retains a significant performance edge. Finally, we show that Curiosity Search is a useful helper objective when combined with Novelty Search, producing individuals that acquire significantly more skills than either algorithm alone.
</blockquote>

http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0162235

```
@article{stanton2016curiosity,
  title={Curiosity search: producing generalists by encouraging individuals to continually explore and acquire skills throughout their lifetime},
  author={Stanton, Christopher and Clune, Jeff},
  journal={PloS one},
  volume={11},
  number={9},
  pages={e0162235},
  year={2016},
  publisher={Public Library of Science}
}
```

### Surprise Search

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

source code : http://www.autogamedesign.eu/software

http://www.autogamedesign.eu/surprise-search

```
@inproceedings{gravina2016surprise,
  title={Surprise search: Beyond objectives and novelty},
  author={Gravina, Daniele and Liapis, Antonios and Yannakakis, Georgios},
  booktitle={Proceedings of the 2016 on Genetic and Evolutionary Computation Conference},
  pages={677--684},
  year={2016},
  organization={ACM}
}
```

### Coupling Novelty and Surprise for Evolutionary Divergence

<b>Abstract:</b>

<blockquote>
Divergent search techniques applied to evolutionary computation,
such as novelty search and surprise search, have demonstrated
their efficacy in highly deceptive problems compared to traditional
objective-based fittness evolutionary processes. While novelty
search rewards unseen solutions, surprise search rewards unexpected
solutions. As a result these two algorithms perform a
different form of search since an expected solution can be novel
while an already seen solution can be surprising. As novelty and
surprise search have already shown much promise individually,
the hypothesis is that an evolutionary process that rewards both
novel and surprising solutions will be able to handle deception in
a better fashion and lead to more successful solutions faster. In
this paper we introduce an algorithm that realises both novelty
and surprise search and we compare it against the two algorithms
that compose it in a number of robot navigation tasks. The key
findings of this paper suggest that coupling novelty and surprise is
advantageous compared to each search approach on its own. The
introduced algorithm breaks new ground in divergent search as it
outperforms both novelty and surprise in terms of efficiency and
robustness, and it explores the behavioural space more extensively.
</blockquote>

http://gravinadaniele.com/wp-content/uploads/2016/01/surprise_novelty.pdf

source code : http://www.autogamedesign.eu/software

```
@inproceedings{gravina2017coupling,
  title={Coupling Novelty and Surprise for Evolutionary Divergence},
  author={Gravina, Daniele and Liapis, Antonios and Yannakakis, Georgios N},
  booktitle={Proceedings of the Genetic and Evolutionary Computation Conference},
  year={2017}
}
```

### Minimal Criterion Coevolution

<b>Abstract:</b>

<blockquote>
Recent studies have emphasized the merits of search processes
that lack overarching objectives, instead promoting divergence
by rewarding behavioral novelty. While this less objective search
paradigm is more open-ended and divergent, it still differs significantly
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
simultaneously coevolving and increasing in complexity. The result
is a broad range of maze topologies and successful agent trajectories
in a single run, thereby suggesting the viability of minimal criterion
coevolution as a new approach to non-objective search and a step
towards genuinely open-ended algorithms.
</blockquote>

http://eplex.cs.ucf.edu/papers/brant_gecco17.pdf

```
@inproceedings{brant2017minimal,
  title={Minimal Criterion Coevolution},
  author={Brant, Jonathan C and  Stanley, Kenneth O},
  booktitle={Proceedings of the 2017 on Genetic and Evolutionary Computation Conference},
  year={2017},
  organization={ACM}
}
```

Source code: https://github.com/jbrant/MinimalCriterionCoevolution/releases/

### SHINE

<b>Abstract:</b>

<blockquote>
Exploration of the search space through the optimisation of
phenotypic diversity is of increasing interest within the field of evolutionary
robotics. Novelty search and the more recent MAP-Elites are two
state of the art evolutionary algorithms which diversify low dimensional
phenotypic traits for divergent exploration. In this paper we introduce a
novel alternative for rapid divergent search of the feature space. Unlike
previous phenotypic search procedures, our proposed Spatial, Hierarchical,
Illuminated Neuro-Evolution (SHINE) algorithm utilises a tree structure
for the maintenance and selection of potential candidates. SHINE penalises
previous solutions in more crowded areas of the landscape. Our
experimental results show that SHINE significantly outperforms novelty
search and MAP-Elites in both performance and exploration. We conclude
that the SHINE algorithm is a viable method for rapid divergent search
of low dimensional, phenotypic landscapes
</blockquote>

https://qmro.qmul.ac.uk/xmlui/bitstream/handle/123456789/14411/Tokarchuk%20Rapid%20Phenotypic%20Landscape%202016%20Accepted.pdf.pdf?sequence=3

```
@inproceedings{smith2016rapid,
  title={Rapid phenotypic landscape exploration through hierarchical spatial partitioning},
  author={Smith, Davy and Tokarchuk, Laurissa and Wiggins, Geraint},
  booktitle={International conference on parallel problem solving from nature},
  pages={911--920},
  year={2016},
  organization={Springer}
}
```

## Quality Diversity algorithms

### Novelty Search Multiobjectivation

<b>Abstract:</b>

<blockquote> Novelty search is a recent and promising approach to evolve neurocontrollers, especially to drive robots. The main idea is to maximize the novelty of behaviors instead of the efficiency. However, abandoning the efficiency objective(s) may be too radical in many contexts. In this paper, a Pareto-based multi-objective evolutionary algorithmis employed to reconcile novelty search with objective-based optimization by following a multiobjectivization process. Several multiobjectivizations based on behavioral novelty and on behavioral diversity are compared on a maze navigation task. Results show that the bi-objective variant “Novelty + Fitness” is better at fine-tuning behaviors than basic novelty search, while keeping a comparable number of iterations to converge. </blockquote>

https://www.researchgate.net/publication/225729412_Novelty-Based_Multiobjectivization

```
@incollection{mouret2011novelty,
  title={Novelty-based multiobjectivization},
  author={Mouret, Jean-Baptiste},
  booktitle={New horizons in evolutionary robotics},
  pages={139--154},
  year={2011},
  publisher={Springer}
}
```

### Novelty Search with Local Competition

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

```
@inproceedings{lehman2011evolving,
  title={Evolving a diversity of virtual creatures through novelty search and local competition},
  author={Lehman, Joel and Stanley, Kenneth O},
  booktitle={Proceedings of the 13th annual conference on Genetic and evolutionary computation},
  pages={211--218},
  year={2011},
  organization={ACM}
}
```

### MAP-Elites

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

```
@article{mouret2015illuminating,
  title={Illuminating search spaces by mapping elites},
  author={Mouret, Jean-Baptiste and Clune, Jeff},
  journal={arXiv preprint arXiv:1504.04909},
  year={2015}
}
```

source code: https://github.com/sferes2/map_elites

### Quality Diversity

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

```
@article{pugh2016quality,
  title={Quality diversity: A new frontier for evolutionary computation},
  author={Pugh, Justin K and Soros, Lisa B and Stanley, Kenneth O},
  journal={Frontiers in Robotics and AI},
  volume={3},
  pages={40},
  year={2016},
  publisher={Frontiers}
}
```

### Constrained Novelty Search

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

```
@article{liapis2015constrained,
  title={Constrained novelty search: A study on game content generation},
  author={Liapis, Antonios and Yannakakis, Georgios N and Togelius, Julian},
  journal={Evolutionary computation},
  volume={23},
  number={1},
  pages={101--129},
  year={2015},
  publisher={MIT Press}
}
```

### Quality and Diversity Optimization: A Unifying Modular Framework

<b>Abstract:</b>

<blockquote>
The optimization of functions to find the best solution according to one or several objectives has a central role in many engineering and research fields. Recently, a new family of optimization algorithms, named Quality-Diversity optimization, has been introduced, and contrasts with classic algorithms. Instead of searching for a single solution, Quality-Diversity algorithms are searching for a large collection of both diverse and high-performing solutions. The role of this collection is to cover the range of possible solution types as much as possible, and to contain the best solution for each type. The contribution of this paper is threefold. Firstly, we present a unifying framework of Quality-Diversity optimization algorithms that covers the two main algorithms of this family (Multi-dimensional Archive of Phenotypic Elites and the Novelty Search with Local Competition), and that highlights the large variety of variants that can be investigated within this family. Secondly, we propose algorithms with a new selection mechanism for Quality-Diversity algorithms that outperforms all the algorithms tested in this paper. Lastly, we present a new collection management that overcomes the erosion issues observed when using unstructured collections. These three contributions are supported by extensive experimental comparisons of Quality-Diversity algorithms on three different experimental scenarios
</blockquote>

https://www.researchgate.net/publication/316989462_Quality_and_Diversity_Optimization_A_Unifying_Modular_Framework

```
@article{cully2017quality,
  title={Quality and Diversity Optimization: A Unifying Modular Framework},
  author={Cully, Antoine and  Demiris, Yiannis},
  journal={IEEE transactions on evolutionary computation},
  year={2017},
  publisher={IEEE}
}
```

Source code: https://github.com/sferes2/modular_QD

### Surrogate-Assisted Illumination (SAIL)

<b>Abstract:</b>

<blockquote>
  The MAP-Elites algorithm produces a set of high-performing
solutions that vary according to features defined by the user. This
technique to ’illuminate’ the problem space through the lens of
chosen features has the potential to be a powerful tool for exploring
design spaces, but is limited by the need for numerous evaluations.
The Surrogate-Assisted Illumination (SAIL) algorithm,
introduced here, integrates approximative models and intelligent
sampling of the objective function to minimize the number of
evaluations required by MAP-Elites.
The ability of SAIL to efficiently produce both accurate models
and diverse high-performing solutions is illustrated on a 2D airfoil
design problem. The search space is divided into bins, each
holding a design with a different combination of features. In each
bin SAIL produces a better performing solution than MAP-Elites,
and requires several orders of magnitude fewer evaluations. The
CMA-ES algorithm was used to produce an optimal design in
each bin: with the same number of evaluations required by CMAES
to find a near-optimal solution in a single bin, SAIL finds solutions
of similar quality in every bin.
</blockquote>

https://arxiv.org/pdf/1806.05865.pdf

```
@inproceedings{gaier2018data,
  title = {Data-Efficient Design Exploration through Surrogate-Assisted Illumination},
  author = {Gaier, Adam and Asteroth, Alexander and Mouret, Jean-Baptiste},
  journal = {Evolutionary Computation},
  volume = {26},
  number = {3},
  pages = {381-410},
  year = {2018}
}
```
### Quality Diversity Through Surprise

<b>Abstract:</b>

<blockquote>
Quality diversity is a recent family of evolutionary search algorithms which focus on finding several well-performing (quality) yet different (diversity) solutions with the aim to maintain an appropriate balance between divergence and convergence during search. While quality diversity has already delivered promising results in complex problems, the capacity of divergent search variants for quality diversity remains largely unexplored. Inspired by the notion of surprise as an effective driver of divergent search and its orthogonal nature to novelty this paper investigates the impact of the former to quality diversity performance. For that purpose we introduce three new quality diversity algorithms which employ surprise as a diversity measure, either on its own or combined with novelty, and compare their performance against novelty search with local competition, the state of the art quality diversity algorithm. The algorithms are tested in a robot navigation task across 60 highly deceptive mazes. Our findings suggest that allowing surprise and novelty to operate synergistically for divergence and in combination with local competition leads to quality diversity algorithms of significantly higher efficiency, speed and robustness.
</blockquote>

http://yannakakis.net/wp-content/uploads/2018/10/QualityDiversityThroughSurprise.pdf

source code: https://gitlab.com/2factor/QDSurprise

```
@article{gravina2018qdsurprise,
  title={Quality Diversity Through Surprise},
  author={Gravina, Daniele and Liapis, Antonios and Yannakakis, Georgios N},
  journal={IEEE Transactions on Evolutionary Computation},
  year={2018},
  publisher={IEEE}
}
```
### Go-Explore

<b>Abstract:</b>

<blockquote>
A grand challenge in reinforcement learning is intelligent exploration, especially when rewards are sparse or deceptive. Two Atari games serve as benchmarks for such hard-exploration domains: Montezuma's Revenge and Pitfall. On both games, current RL algorithms perform poorly, even those with intrinsic motivation, which is the dominant method to improve performance on hard-exploration domains. To address this shortfall, we introduce a new algorithm called Go-Explore. It exploits the following principles: (1) remember previously visited states, (2) first return to a promising state (without exploration), then explore from it, and (3) solve simulated environments through any available means (including by introducing determinism), then robustify via imitation learning. The combined effect of these principles is a dramatic performance improvement on hard-exploration problems. On Montezuma's Revenge, Go-Explore scores a mean of over 43k points, almost 4 times the previous state of the art. Go-Explore can also harness human-provided domain knowledge and, when augmented with it, scores a mean of over 650k points on Montezuma's Revenge. Its max performance of nearly 18 million surpasses the human world record, meeting even the strictest definition of "superhuman" performance. On Pitfall, Go-Explore with domain knowledge is the first algorithm to score above zero. Its mean score of almost 60k points exceeds expert human performance. Because Go-Explore produces high-performing demonstrations automatically and cheaply, it also outperforms imitation learning work where humans provide solution demonstrations. Go-Explore opens up many new research directions into improving it and weaving its insights into current RL algorithms. It may also enable progress on previously unsolvable hard-exploration problems in many domains, especially those that harness a simulator during training (e.g. robotics).
</blockquote>

https://arxiv.org/pdf/1901.10995

source code: https://github.com/uber-research/go-explore

```
@article{ecoffet2019go,
  title={Go-Explore: a New Approach for Hard-Exploration Problems},
  author={Ecoffet, Adrien and Huizinga, Joost and Lehman, Joel and Stanley, Kenneth O and Clune, Jeff},
  journal={arXiv preprint arXiv:1901.10995},
  year={2019}
}

```
### Constrained Map-Elites

<b>Abstract:</b>

<blockquote>
We describe a search-based approach to generating new levels for bullet hell games, which are action games characterized by and requiring avoidance of a very large amount of projectiles. Levels are represented using a domain-specific description language, and search in the space defined by this language is performed by a novel variant of the Map-Elites algorithm which incorporates a feasible- infeasible approach to constraint satisfaction. Simulation-based evaluation is used to gauge the fitness of levels, using an agent based on best-first search. The performance of the agent can be tuned according to the two dimensions of strategy and dexterity, making it possible to search for level configurations that require a specific combination of both. As far as we know, this paper describes the first generator for this game genre, and includes several algorithmic innovations.
</blockquote>

https://arxiv.org/abs/1806.04718

```
@inproceedings{khalifa2018talakat,
  title={Talakat: Bullet hell generation through constrained map-elites},
  author={Khalifa, Ahmed and Lee, Scott and Nealen, Andy and Togelius, Julian},
  booktitle={Proceedings of The Genetic and Evolutionary Computation Conference},
  pages={1047--1054},
  year={2018},
  organization={ACM}
}

```

### MAP-Elites with Sliding Boundaries

<b>Abstract:</b>

<blockquote>
Quality diversity (QD) algorithms such as MAP-Elites have emerged as a powerful alternative to traditional single-objective optimization methods. They were initially applied to evolutionary robotics problems such as locomotion and maze navigation, but have yet to see widespread application. We argue that these algorithms are perfectly suited to the rich domain of video games, which contains many relevant problems with a multitude of successful strategies and often also multiple dimensions along which solutions can vary. This paper introduces a novel modification of the MAP-Elites algorithm called MAP-Elites with Sliding Boundaries (MESB) and applies it to the design and rebalancing of Hearthstone, a popular collectible card game chosen for its number of multidimensional behavior features relevant to particular styles of play. To avoid overpopulating cells with conflated behaviors, MESB slides the boundaries of cells based on the distribution of evolved individuals. Experiments in this paper demonstrate the performance of MESB in Hearthstone. Results suggest MESB finds diverse ways of playing the game well along the selected behavioral dimensions. Further analysis of the evolved strategies reveals common patterns that recur across behavioral dimensions and explores how MESB can help rebalance the game.
</blockquote>

https://arxiv.org/pdf/1904.10656.pdf

```
@inproceedings{fontaine2019,
  title={Mapping Hearthstone Deck Spaces with Map-Elites with Sliding Boundaries},
  author={Matthew C. Fontaine and Scott Lee and L. B. Soros and Fernando De Mesentier Silva and Julian Togelius and Amy K. Hoover},
  booktitle={Proceedings of The Genetic and Evolutionary Computation Conference},
  year={2019},
  organization={ACM}
}
```
----

