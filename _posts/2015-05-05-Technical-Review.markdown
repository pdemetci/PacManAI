---
layout: post
title:  "Technical Review"
date:   2015-05-05 01:06:00
categories: jekyll update
---

#Technical Review I: Preparation and Framing

##**Background and Context**: 
* Project goal: Develop our own artificial intelligence algorithm for the pacman agent to learn how to play based on the agent’s experience in earning rewards by acting on different states
  * Continuing to use the UC Berkeley code as the foundation of our AI algorithm
* We have abstracted the game by focusing on agent collecting food and not including ghosts (... for now…)
* Plan to implement Q learning adaptation that uses a linear combination of the agent’s set of states and actions
  * Instead of using a Q matrix, as a we presented last time, because the number of states to keep track of in a game would be infeasible
  * Please see Reinforcement Learning: Q Learning Adaptation handout for high level overview
* We are currently considering using the python library called python to implement the learning algorithm
  * We will contact Gabrielle, who has previous experience using pybrain, to learn more about the library and how to use it

## Key Questions: 
Questions for Class
1. Looking at the measurements listed, which ones do you think will be the most important and when? Also, what other measurements from the pacman environment may be useful to include in our function?
2. What might some of the measurement functions look like?
3. Is it best to store the weight vector by pickling? Or is there a better method? (Dependent on Question 1 for Paul)
4. Ideas for implementing Manhattan distance with walls?

Questions for Paul
1. When and how do we update the weights vector? How do rewards factor in?
  * In other words, how does the weight’s vector map to the feature which got the agent to it’s present state?
  * Maybe update by keeping track of Q? Or time since agent ate a capsule?
2. What is the purpose of the constant b and what does it do?

## Agenda for Technical Review Session: (25 minutes)
### 5 minutes: Talk about how we have implemented feedback from the design review and our current status
* Using Q function instead of Q matrix
* Not including ghosts in our code design (... for now…)
### 15 Minutes: Q Learning Adaptation
* Going through Reinforcement Learning: Q Learning Adaptation Guide
* Explaining the different parts of the Q function
* Ideate other possible measurements to include in function to determine agent’s optimal action
* Discuss how to update the weight vector
### 5 Minutes: Show current code
* Basic Q function example
* A-star Search that theoretically works
* Identify next steps
