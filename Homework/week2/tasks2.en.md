---
title: TIES442 - Tasks - Week 2
lang: en
...

# Weekly tasks 2

Final version, published 17 March 2015 9:40

Deadlines for handing in the tasks, and their effects on the awarded points:

* max 3 points: 24 March 2015 10:15 am
* max 2 points: 31 March 2015 10:15 am
* max 1 point: 30 June 2015 12:00 pm

----

The tasks will appear latest 17 March 10 am. Otherwise, the deadlines will be
moved forward as well.

----

## Task 1

Design a simple *reflex agent*, that plays simplified soccer in a 2D world. It
is part of a team, and there is also an opposing team, but focus on just this
one agent.

* How could the agent's performance be measured?
1. Agents team has ball:
    1.1. teammate has ball:
        -Is it possible to reveive pass from the teammate holding the ball
            - But is it still on its own 'area' i.e., defender has to stay lower...
    1.2. Agent has the ball:
        - Velocity to the attack end. 
        - Distance from opponents.
        - How many options to pass the ball to teammates, prefer the attack direction. 
2. Agents team does not have the ball:
        - Own area.
        - Keeping close to one opponent player that is on agents area.
        - If ball comes close - try to get closer to it... 
* What is the environment like? What kinds of elements describe its state?

* What actuators the agent would need? Which actions it would need to perform?
* What sensors the agent would need? What kinds of things it should be able to
  perceive?

This is the so-called PEAS scheme for analyzing agents (performance,
environment, actuators, sensors). It is a tool for defining the basic building
blocks of agents. Search the web for more information about it.

* Example: <http://www4.ncsu.edu/~stamant/411/lectures/02-agents/peas.pdf>

Learn about simple reflex agents on the web. What kinds of reflexes
(or *if-then*-rules) the soccer agent would need to succeed?

What could be added to the agent, in addition to simple reflexes, to make it
perform better?

## Task 2

Refresh your memory on finite state machines. Describe with a brief example,
what are the start state, final state, transition, input and output of a
machine. What is the difference between Moore and Mealy machines?

* For example:
* <http://en.wikipedia.org/wiki/Finite-state_machine>
* <https://www.youtube.com/watch?v=hJIST1cEf6A>

## Task 3

(This task is more complex, don't worry if you can't finish it)

Let us imagine the so-called *vacuum cleaner world*, that is described in
Russell and Norvig's book. There are several different versions of this, but we
shall follow the rules present here. We know the following.

* The world consists of rectangular cells, that are either open or closed.
* The agent is initially in some open cell and can move up, down, left or right,
  if the target cell is open; if it is closed, the result is an error.
  Moving consumes one unit of energy and time despite the result.
* The world is a 10x10 grid, where the outer boundaries consist of closed cells.
  Other cells can be either open or closed. Let us assume though, that all open
  cells are connected.
* Open cells may be dirty, and they will become dirty over time at certain
  speed, i.e. one new dirty cell appears in T time units.
* The agent can perceive, if the cell where it is located, is dirty.
* The agent can clean a dirty cell, which consumes 2 units of energy and 1 unit
  of time.
* The agent can also choose to stay idle whore one time unit, which does not
  consume energy, but does consume one unit of time.

The goal of the agent is to minimize, at the same time,

* the *average* number of dirty cells per time unit, and
* the *average* amount of energy consumed per time unit.

Design a reflex agent, whose task is to keep clean the world depicted in the
image below. The agent is represented by the circle, black squares are closed.

![World 1](/images/world_1.png)

What perceptions and actions the agent has?

What is the performance measure of the agent?

What kinds of reflexes (or *if-then*-rules) the agent should have in order to
keep the world clean with optimal cost? What affects the cost?

How would you describe the agent as a state machine?

How does the speed at which the world becomes dirty affect, how often the agent
should clean the world instead of resting?

Will the agent succeed also at cleaning the other world depicted in the
image below?

![World 2](/images/world_2.png)

Try to think, if it is possible to come up with a world that your agent is not
able to clean, which means there will be corners in the world where the agent
will never move due to its transition logic.

## Extra: Task 4

Teach to yourself what *subsumption architecture* means. In what way the
workings of the vacuum cleaner agent would change, if it were designed according
to this architecture? How should the task description change to get benefit
from using this architecture?

* <http://en.wikipedia.org/wiki/Subsumption_architecture>
* <http://ai.eecs.umich.edu/cogarch3/Brooks/Brooks.html>
* <https://www.youtube.com/watch?v=bBIKXM1k12k>

----
