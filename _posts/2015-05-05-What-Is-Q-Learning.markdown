---
layout: post
title:  "What is Q-learning?"
date:   2015-05-05 05:00:00
categories: jekyll update
---
Reinforcement learning is a type of artificial intelligence that tries to determine the best action for an agent to take in a given state based on immediate and cumulative rewards. It is used in many different fields including game theory, statistics, control theory, and simulation-based optimization. In general reinforcement learning is unsupervised, meaning that it is never shown the “correct answer” to make adjustments to its parameters. Reinforcement learning agents usually use a Markov decision process (MDP) to select the best action for the state they are in (or, more generally, to form a policy for choosing actions based on the state). In an MDP, given a state and an action, the state transitions are conditionally independent of all previous states and actions. 

For Pacman, the actions are simple: North, South, East, West, or Stop. The rewards are also simple: food is +10, ghosts are -500 or +200, depending, and a win is +500. The states, however, get tricky. On a large board, Pacman is essentially operating in a continuous state space. We abstracted states to mean linear combinations of features instead of Pacman’s coordinates on the board.
![PacMan Reinforcement Learning]()
The picture above shows the action space, which consists of five actions: North, South, East, West, and Stop.

There are only a few different kinds of rewards in this game.
Food: 10
Scared ghost: 200
Winning: 500
Losing: -500
Time delay: -1


