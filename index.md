***Student Name: Georgios Giapitzakis Tzintanos***

***Project Title: Improvements of the graph module***

***Project URL: [https://summerofcode.withgoogle.com/projects/#5046505600188416](https://summerofcode.withgoogle.com/projects/#5046505600188416 "GSoC Page")***

## Beginning

When I first learned about Google Summer of Code program I had no idea how to contribute to any open source project. I was, however, really excited to get to know the world of open source software and, eventually, become a part of it. The reason I have chosen SageMath to contribute and apply to is that I wanted to work on something that is close to my field of studies (Mathematics) and (if possible) to one of my areas of interest such as graph theory. 

## First contribution

Before submitting their final proposals students are asked to make some contribution to SageMath. This contribution can be either reporting a bug, suggesting a feature or fixing an already open issue. I worked on implementing Floyd-Warshall algorithm to compute the all pairs shortest paths in an (un)weighted (un)directed graph. My work can be found in [this](https://trac.sagemath.org/ticket/27518) ticket which is now closed and merged into Sage.

## Project overview

This project consists of two parts:

  * Cythonize some of the current methods which are slow
  
  * Improve graph traversals and possibly add new ones

## A little bit about Cython

[Cython](https://cython.org/) is a superset of Python that additionally supports calling C/C++ functions. Using Cython we can obtain very efficient code and that is why cythonizing (rewriting existing Python code into Cython) is really important.

## Contributions related to my project

To keep track of all issues SageMath uses a system called [Trac](https://trac.edgewall.org/). All bug/bugfixes and new functionality or enhancements have to be reported through SageMath's Trac wiki. Below you can find all the tickets I issued throughout the GSoC period related to my project along with a short description of what each ticket aims at implementing:
  * [#27875](https://trac.sagemath.org/ticket/27875): (**Merged**) In this patch all methods related to the computation of line graphs were cythonized
  
  * [#27882](https://trac.sagemath.org/ticket/27882): (**Merged**) Just like in the above patch, all methods related to graph coloring were cythonized
  
  * [#27928](https://trac.sagemath.org/ticket/27928): (**Merged**) In this ticket graph traversal Lexicographic DFS (LexDFS) <span id="a1">[[1]](#f1)</span> was implemented. Also, the existing traversal Lexicographic BFS (LexBFS) <span id="a1">[[1]](#f1)</span> was re-implemented in Cython in order to achieve better time complexity. Lexicographic BFS is a very important algorithm since we can check if a graph is [chordal](https://en.wikipedia.org/wiki/Chordal_graph) just by examining the ordering produced by LexBFS. With a good implementation of the traversal this can be achieved in linear time.
  
  * [#28195](https://trac.sagemath.org/ticket/28195): (**Merged**) In this patch Lexicographic UP (LexUP) and Lexicographic DOWN (LexDOWN) <span id="a2">[[2]](#f2)</span> graph traversals were implemented
  
  * [#28271](https://trac.sagemath.org/ticket/28271): (**Merged**) The last ticket implements Lexicographic M (LexM) <span id="a3">[[3]](#f3)</span><span id="a4">[[4]](#f4)</span> graph traversal. This traversal is particularly useful since it can be used to obtain a triangulation of a graph.

## Further work

Participating in Google Summer of Code was definitely a great experience. I learned how open source projects work, how to write efficient and easy to read and maintain code and I was given the chance to understand and implement some very sophisticated algorithms through several research papers. That's why I intend to continue contributing to SageMath and possibly other open source projects. As for my project, I am planning on implementing some parts of it that were left out due to limited time. These include the creation of a Tree class and the implementation of some approximation algorithms to solve algorithmically hard problems.

## Conclusion

I would like to thank my mentors for their vital contribution to making this a wonderful experience. Not only did they guide me throughout the GSoC period, they also offered great help with any technical difficulty that occurred and provided great advice on writing better code and good documentation. Finally, I would like to thank Google for giving the opportunity to students all around the world to get to know and engage with open source software development through GSoC.

## References

1. <span id="f1"></span> [Derek G. Corneil and Richard M. Krueger. A Unified View of Graph Searching](http://www.cs.toronto.edu/~krueger/papers/unified.ps) [↩](#a1)

2. <span id="f2"></span> [Arthur Milchior. (Quasi-)linear time algorithm to compute LexDFS, LexUP
and LexDown orderings](https://arxiv.org/pdf/1701.00305.pdf) [↩](#a2)

3. <span id="f3"></span> [Yon Dourisbourea and Cyril Gavoilleb. Tree-decompositions with bags of small diameter](http://dept-info.labri.fr/~gavoille/article/DG07) [↩](#a3)

4. <span id="f4"></span> Donald J. Rose, R. Endre Tarjan and George S. Lueker. Algorithmic aspects of vertex elimination on graphs [↩](#a4)
