---
title: TIES442 - Assignment project - Phase 1
lang: fi
...

# TIES442 - Assignment project - Phase 1

Group: KsP

* Topi Korhonen, topi.korhonen@jyu.fi

## Assignments for this phase:

* Choose a topic for the project and describe it informally. What is the problem
  that you are trying to solve? How could the solution be found? Are there any
  specific design principle, that you would like to follow?

Topic is to play Rock Scissors Paper against human or algorhithm. The game is well known and it gives possibility for applying learning in order to foresee the choise of opponent. The simpler case is to try to learn patterns from the choices the opponents makes. The more advanced way would be to try to learn how to affect the choices of the opponent by own choices. 

In the simple case the solution could be found by analyzing the past decisions and trying to find/learn patterns from it. In the more advanced case the agent could try to find ways to affect the decisions of the opponen by its own choices, the analysis would still be from the past choices now together with the agents own (past) choices.

I do not know anything about desing principles... 

* Describe the system that attempts to solve the problem on a high level as an
  agent.
    - What is the working environment of the agent? Use the Russell & Norvig's
      [PEAS categories](topics1.en.md)
	
        PEAS:
        - is designed with certain Performance requirements
            - Goal is to find and learn at least simple patterns used by the opponent. 	
        - for a particular Environment or environment class 
            - Enviroment is just input from the opponent ian is one of the three RsP, also the choice of the angent affects the future choices of the opponent.
        - using certain Actuators for acting on its environment
            - Actuators are just displaying the choice of the agent.
        - and Sensors for perceiving its environment 
            - Sensors are also simple as this is just a simple game..
	
    - What kinds of observations the agent can make of its environment, what is
      the available information? Is the information precise or is there
      uncertainty involved?
        - Agent can only make observations of the history of the game. The available information is the choices made by tha opponent and the choices made by the agent. The information is precise, the opponent definetly made the choice that is seen in the history. However the history does definetly quarantee that something would happen similarly in future - this I count as uncerntainty. 
    - What kinds of actions can the agent take, and what kinds of changes it can
      effect in its environment?
        - Agent can only make one choice at a time. These choices may or may not affect the coming choices of the opponent.
    - Describe in your analysis the task environment and complexity also using
      the [dimensions](topics1.en.md) described in the material, as appropriate.
        * Is it possible to present the solution in a *modular* way?
            - What is modular...
        * What is the representation of the world?
            - World is only inputs from the user.
        * Planning horizon, or how far ahead the agent plans its actions?
            - At most couple rounds ahead.
        * Is there uncertainty, for both percepts and effects of actions?
            - Percepts are certain. The effects of the actions are higly uncertain.         
        * What are the agent's preferences?
            - Vegetarian, beatiful ladies and strong Indian pale Ales together with nice live acoustic music.
        * What is the number of agents?
            - < 5
        * Does the agent need to learn?
            - At least the agent needs to be able to regocnise patterns.
        * Are their computational limitations, such as time that can be sent on searching for solutions?	
            - The computation does not pose a problem. The amount of data is so small.
     - What kinds of strategies the agent could employ in order to come up with reasonable actions based on the available information?
        - The may be quite limited, the point is to try to quess the coming choice of the opponent based on the history of choices made by the opponent. Maybe the agent could try to find stradegy to affect the coming choices of the opponent and the use that.
            

* Choose a name for your project/agent. It can be the same as the group's name.
	- KsP
----

Remember, that the work on the project takes place iteratively during the whole
duration of the course. In each phase, the most important thing is to quickly
come up with some reasonable, preliminary content. It is possible to keep
improving each week's results during the following weeks and before handing in
the final project report.
