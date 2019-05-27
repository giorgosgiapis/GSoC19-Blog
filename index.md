***Student Name: Georgios Giapitzakis Tzintanos***

***Project Title: Improvements of the graph module***

***Project URL: [https://summerofcode.withgoogle.com/projects/#5046505600188416](https://summerofcode.withgoogle.com/projects/#5046505600188416 "GSoC Page")***

## Beginning

When I first learned about Google Summer of Code program I had no idea how to contribute to open source projects. I was, however, really excited to get to know the world of open source software and, eventually, become a part of it. The reason I have chosen SageMath to contribute and apply to is that I wanted to work on something that is close to my field of studies (Mathematics) and (if possible) to one of my areas of interest such as graph theory. 

## First contribution

Before submitting their final proposals students are asked to make some contribution to SageMath. This contribution can be either reporting a bug, suggesting a feature or fixing an already open issue. I worked on implementing Floyd-Warshall algorithm to compute the all pairs shortest paths in an (un)weighted (un)directed graph. My work can be found in [this](https://trac.sagemath.org/ticket/27518) ticket which is now closed and merged into Sage.

## Project overview

This project consists of four main parts:
  * Cythonize some of the current methods which are slow
  * Implement some approximation algorithms to solve some well known NP problems
  * Create a class specifically for trees and implement related methods
  * Improve graph traversals and possibly add new ones

## Contributions related to my project

To keep track of all issues SageMath uses a system called [Trac](https://trac.edgewall.org/). All bug/bugfixes and new functionality or enhancements have to be reported through SageMath's Trac wiki. Below you can find all the tickets I issued throughout the GSoC period related to my project along with a short description of what each ticket aims at implementing:

