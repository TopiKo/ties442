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
            
            - Is it possible to reveive pass from the teammate holding the ball
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
    - Enviroment consist: field, teammates, opponents, ball and two goals.
    - State is described by the locations, velocities and accelerations of all the players + ball. 

* What actuators the agent would need? Which actions it would need to perform?
    - Legs. 
    - Abilities: running, running with ball, ability to pass opponents (tricks/bluffs), passing ball to teammate, kicking ball to goal, taking ball from opponent. 

* What sensors the agent would need? What kinds of things it should be able to
  perceive?
    - Vision.
    - The approximate positions and state of motion of teammates and opponents. Accurate position and velocity of ball.

This is the so-called PEAS scheme for analyzing agents (performance,
environment, actuators, sensors). It is a tool for defining the basic building
blocks of agents. Search the web for more information about it.

* Example: <http://www4.ncsu.edu/~stamant/411/lectures/02-agents/peas.pdf>

Learn about simple reflex agents on the web. What kinds of reflexes
(or *if-then*-rules) the soccer agent would need to succeed?

    - if I have ball then I run towards attack end with it.
    - if opponent is coming towards then I change direction.
    - if goal is unguarded then I kick ball into it.
    - ...

What could be added to the agent, in addition to simple reflexes, to make it
perform better?
    - 

## Task 2

Refresh your memory on finite state machines. Describe with a brief example,
what are the start state, final state, transition, input and output of a
machine. What is the difference between Moore and Mealy machines?
    
    - start state = the state in which the machine is supposed to receive input.
    - final state = accept state = The machine ends in this state after processing the input if the given input has been of type that the machine understands. Ex. machine which determines if given input has even number of zeros: if even input has even number of zeros final state machine will end in the final state = accept state, if there is odd number of zeros the final state machine does not end in the accept state. 
    - transition =  is a set of actions to be executed when a condition is fulfilled or when an event is received. Ex. When timer says 'time!' traffic lights change from green to red.
    - input = whatever thing the machine eats.
    - output = signal given by the machine.

    Moore machine: output depends only on the state of the machine.
    Mealey machine: output depends on the input and the state of the machine. 

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

    - perceptions: is this cell dirty, is the cell I'm trying to enter closed.
    - actions: move, clean

What is the performance measure of the agent?

    - how much is has removed dirt in time unit.
    - how much it has removed dirt per energy unit?

What kinds of reflexes (or *if-then*-rules) the agent should have in order to
keep the world clean with optimal cost? What affects the cost?

    - if this cell is dirty then clean it
    - if this cell is dirty then try to probe the nearby cells for dirt as well
    - if the cell ahead is closed turn
    
How would you describe the agent as a state machine?

    - See state_diag.pdf

How does the speed at which the world becomes dirty affect, how often the agent
should clean the world instead of resting?

    - See robot_cleaner_math.pdf
    
Will the agent succeed also at cleaning the other world depicted in the
image below?
    
    - It should be but this of course takes some amount of time depending how the n-moves is defined and does it for example change in time. n- could for exapmle develop like 1, 2,..., N, 1, 2,..., N, ..., 1, 2,..., N. The machine making spirals (assuming no walls) that change their origin. 


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
