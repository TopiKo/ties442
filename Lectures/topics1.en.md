---
title: TIES442 - Summary of week 1 topics
lang: en
...

# Summary of week 1 topics

Note: the english language summaries will usually be shorter due to time
constraints. Additional information can be found from various websites.

## Agents

[Categories of agents](http://www.msci.memphis.edu/~franklin/AgentProg.html).

## Intelligence from the point of view of rationality

[Marcus Hutter](http://hutter1.net/) has proposed, that intelligence could be
defined in a neutral way by using rationality as basis. An agent would be
intelligent, if it can succeed, or act rationally, in many different
environments. This requires adaptation and learning.

## Agent's task environment and PEAS

Task environment is, according to Russell and Norvig, a description for the
*problem* for which the agent is a *solution*. It includes the following
categories, that together form the acronym PEAS:

* agent's *performance measure*,
* *environment*, or the various things belonging to the world's state,
* *actuators*, that agent uses to perform actions, and
* *sensors*, that the agent uses to perceive the environment.

PEAS is a tool for rough conceptualization of agents. By listing things
belonging to the above categories informally, it is possible to get a hold of
the problem and start defining the solution in more detail.

## Task environment dimensions

The task environment can be characterized in more detail by thinking where the
environment is located on the following dimensions:

* Is the environment fully or partially observable?
* Is the environment deterministic or stochastic, meaning, are there
  uncertainties?
* Is the task of the agent episodic or sequential, meaning, are individual
  occasions of the task separate or do they depend on previous occasions?
* Is the environment static or dynamic?
* Is the environment discrete or continous, and for what part? (time, state,
  percepts, actions)
* Is there only one agent or multiple agents? Do they collaborate or compete
  with each other?

## Task complexity dimensions

Poole ja Mackworth describe in the
[section 1.5](http://artint.info/html/ArtInt_12.html) of their online book
another kind of approach to analyzing agents, namely *dimensions of complexity*.
They are partially overlappin with those defined by Russell and Norvig, but
they can be used to complement and improve the analysis for some aspects.

* Is it possible to present the solution in a *modular* way?
* What is the representation of the world?
* Planning horizon, or how far ahead the agent plans its actions?
* Is there uncertainty, for both percepts and effects of actions?
* What are the agent's preferences?
* What is the number of agents?
* Does the agent need to learn?
* Are their computational limitations, such as time that can be sent on
  searching for solutions?
