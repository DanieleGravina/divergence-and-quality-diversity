## What is it?

A collection of papers on divergence and quality diversity

## Table of Contents

- [What is it?](#what-is-it)
- [Novelty Search](#novelty-search)
- [Novelty Search Multiobjectivation](#novelty-search-multiobjectivation)
- [Novelty Search Local Competition](#novelty-search-local-competition)
- [Map-elites](#map-elites)
- [Quality diversity](#quality-diversity)
- [Constrained novelty search](#constrained-novelty-search)
- [DeLeNoX](#deLeNoX)
- [Surprise Search](#surprise-search)
- [Minimal Criterion Coevolution](#minimal-criterion-coevolution)


## Novelty search

Abstract

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

https://www.researchgate.net/publication/225729412_Novelty-Based_Multiobjectivization

@incollection{mouret2011novelty,
  title={Novelty-based multiobjectivization},
  author={Mouret, Jean-Baptiste},
  booktitle={New horizons in evolutionary robotics},
  pages={139--154},
  year={2011},
  publisher={Springer}
}

## Novelty search local competition

https://pdfs.semanticscholar.org/6d45/9da1ff73ec7225e92842341605e2b90d0da2.pdf

@inproceedings{lehman2011evolving,
  title={Evolving a diversity of virtual creatures through novelty search and local competition},
  author={Lehman, Joel and Stanley, Kenneth O},
  booktitle={Proceedings of the 13th annual conference on Genetic and evolutionary computation},
  pages={211--218},
  year={2011},
  organization={ACM}
}

## Map elites

https://arxiv.org/pdf/1504.04909.pdf

@article{mouret2015illuminating,
  title={Illuminating search spaces by mapping elites},
  author={Mouret, Jean-Baptiste and Clune, Jeff},
  journal={arXiv preprint arXiv:1504.04909},
  year={2015}
}

source code: https://github.com/sferes2/map_elites

## Quality diversity

http://journal.frontiersin.org/article/10.3389/frobt.2016.00040/pdf

@article{pugh2016quality,
  title={Quality diversity: A new frontier for evolutionary computation},
  author={Pugh, Justin K and Soros, Lisa B and Stanley, Kenneth O},
  journal={Frontiers in Robotics and AI},
  volume={3},
  pages={40},
  year={2016},
  publisher={Frontiers}
}

## Constrained novelty search

http://antoniosliapis.com/papers/constrained_novelty_search.pdf

http://antoniosliapis.com/research/novsearch.php

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

## DeLeNoX

http://julian.togelius.com/Liapis2013Transforming.pdf

http://antoniosliapis.com/research/novsearch.php

@inproceedings{liapis2013transforming,
  title={Transforming exploratory creativity with DeLeNoX},
  author={Liapis, Antonios and Mart{\i}nez, H{\'e}ctor P and Togelius, Julian and Yannakakis, Georgios N},
  booktitle={Proceedings of the Fourth International Conference on Computational Creativity},
  pages={56--63},
  year={2013},
  organization={AAAI Press}
}

## Surprise search

http://antoniosliapis.com/papers/surprise_search_beyond_objectives_and_novelty.pdf

http://www.autogamedesign.eu/surprise-search

@inproceedings{gravina2016surprise,
  title={Surprise search: Beyond objectives and novelty},
  author={Gravina, Daniele and Liapis, Antonios and Yannakakis, Georgios},
  booktitle={Proceedings of the 2016 on Genetic and Evolutionary Computation Conference},
  pages={677--684},
  year={2016},
  organization={ACM}
}

## Minimal criterion coevolution

http://eplex.cs.ucf.edu/papers/brant_gecco17.pdf

@inproceedings{brant2017minimal,
  title={Minimal Criterion Coevolution},
  author={Brant, Jonathan C and  Stanley, Kenneth O},
  booktitle={Proceedings of the 2017 on Genetic and Evolutionary Computation Conference},
  year={2017},
  organization={ACM}
}

Source code: https://github.com/jbrant/MinimalCriterionCoevolution/releases/
