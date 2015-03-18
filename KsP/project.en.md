---
title: TIES442 - Assignment project instructions
lang: en
...

# Assignment project instructions

[Finnish version](project.fi.md)

Viimeksi päivitetty 11.3.2015

Passing the course requires completing an *obligatory* assignment project. It
can be completed alone or in groups of 2-3 students. The assignment is
designing the architecture and algorithms for an agent performing some
well-defined task. Completing its task typically requires that the agent can

* search in some space of options,
* reason based on the available information and make decisions,
* plan, or chain multiple decisions for reaching a goal,
* possibly perform some simple learning, or modify its behavior based on its
  experiences.

An integral part of the assignment is formulating the task, the objectives, the
available knowledge, and searching and decision-making steps in sufficient
detail for turning into a computer program that implements the agent and is able
to carry out its tasks. The time allocated for the project may not be sufficient
for designing all aspects of the agent completely, but the goal is, that
motivated students will have the skills for completing the plan on their own.

## Schedule

There will be weekly phases for finishing the project during the course. At the
end of the lecture every Tuesday will be presented the assignments for the next
week. The results will be handed in before the next Tuesday's lecture, which
will earn every team member 2 points if the content is reasonable. Late
submissions that are handed in before 30 June 2015 will earn 1 point per team
member.

In the following there are links to the instructions for each phase and a rough
overview of each week's assignments. Please note, that the linked documents
**may be updated** until the Tuesday lecture of the corresponding week.

* Phase 1, selecting and describing the topic, background work.
* Phase 2, analyzing the task based on simple behavioral rules.
  The goal is to notice, how difficult it is to solve anything but the simplest
  problems in this way. All topics should be sufficiently complex to prevent
  solving more than just small sub-parts in this fashion.
* Phase 3, analyzing the search tasks related to the topic and
  describing them.
* Phase 4, selecting a search algorithm and describing it in
  detail from the point of view of the project topic. Presenting a practical
  example of how the algorithm works.
* Phase 5, analyzing the knowledge that the agent must possess
  and how it is described.
* Phase 6, analyzing the reasoning tasks that the agent must be
  able to perform based on its knowledge. Writing a few examples.
* Phase 7, analyzing the planning tasks that the agent must be
  able to perform. Choosing a planning algorithm and describing it in detail
  from the point of view of the project topic. Presenting a practical example of
  how the algorithm works.
* Phase 8, analyzing whether the agent needs the ability to
  learn. Isolating the sub-tasks that require learning. If the learning tasks
  are simple, designing an algorithm for performing the tasks.
* Phase 9, finalizing the plan and making a summary.

The purpose of the weekly phases and deadlines is to guide a fast iterative
process for advancing the project. The results that are handed in weekly do not
have to be final or complete, but they can be improved during the whole duration
of the course. Estimated time to spend on each weekly assignment is **4 hours**,
so students should take this into account when allocating their time.

After the lecture course has neded, the team writes a final report of the
project and sends it to the teacher before 30 June 2015. The tool used for
writing the report may be chosen freely, as long as the teacher is able to read
the end result; recommended formats are web-pages and pdf documents. The
assignment project is *mandatory*, so the grades will be awarded only after
handing in the final report. Estimated time spent writing the final report is
4-8 hours per team member.

## Instructions for handing in the weekly results

Handing in the assignment results works the same way as the handing in of the
weekly tasks. Only one team member needs to send the results, but it would be
good to mention the names and email addresses of all team members every week.
The possible methods of sending the results are

* email message, with possible pictures as attachments,
* document written with a word processor, generated into a pdf and sent via
  email (preferably linking to Dropbox or similar),
* web-page, and the link to it sent via email,
* and the recommended way is cloning the yousource repository of the course
  page and sending its address to the teacher (only needs to be done once for
  each team, and only one repository per team is needed).

**More detailed instructions will be given later.**

## Examples of suitable topics

Any sufficiently complicated proble is fine, as long as it is possible to
formulate it as a searching, planning or decision making problem. We will try to
find for each project a suitable focus area either from searching, planning or
decision making, but in every project there should be some small aspect from all
three. If the task is otherwise very simple but its solution can apply some
simple learning methods, it is possible to choose also learning as the focus
area.

Remember that the projects are iterative. It is important to get started quickly
with some interesting problem. If it is too big or too small, we can adjust it
during the course.

In the following, there are some examples of suitable topics.

* Computer version of some board game involving chance, such as throwing dice,
  and/or making choices. Monopoly is an example of these. An important part of
  these projects will be modeling different choices of strategy and how they are
  affected by the choices of other players.
* Many games that require allocation of resources, such as various strategy
  games. Requires modeling decision making and goals (long-term strategy).
* Easier games that are combined with simple methods for learning the playing
  style of the opponents and predicting their moves.
* Robot simulations: instead of building a real robot, we simulate one in a
  virtual world, preferably two-dimensional; either a 'discrete' world where
  robot moves tile by tile, or 'continuous' world where it moves according to
  vectors. Requires pathfinding and planning actions for more than one step. The
  robot will carry out some task on its own, such as clean or move objects
  around, or competes against other robots. Some computer games where a
  character is controlled and moved around fall into this category.
* Virtual assistants, that carry out simple tasks or searches or make simple
  choices. Usually requires designing a knowledge base. A limiting factor is,
  that analyzing natural language is too difficult problem. The agent must
  accept only queries presented in a formal language, or interpret free-form
  queries based on keywords.

## Examples of bad topics

* Simple games that can be solved easily by checking all options; tic-tac-toe
  and many brain puzzles are examples of these. Some of these are used as
  examples and exercises during the course.
* A boundary case might be simple games, where the depth of search is limited
  artificially and the agent is forced to make a choice based on limited
  knowledge. Requires designing a criterion for evaluating the value of each
  position. The best way might be learning by experience, so this kind of topic
  might be good for projects focusing on learning.
* Games, that are based on reacting to events, or agents that are based on
  scripted behaviors. Examples of these are the ghosts of Pac-Man an the
  opponents of most combat games. The same game might be suitable, if it is
  possible to add goal-drive behavior and implementing different strategies via
  search and decision making.
* Complicated games with too many choices. Go is an example of a game, where
  success probably requires complicated pattern recognition and learning.
* Tasks requiring natural language analysis. This is a too difficult problem,
  although there has been some progress recently.
* Tasks requiring perception, such as analyzing camera images. This is also a
  difficult problem. However, it is possible to simulate perceptions by giving
  them to the agent in a symbolic form.
