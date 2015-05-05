---
layout: post
title:  "Design Review"
date:   2015-05-05 03:04:00
categories: jekyll update
---
# Design Review I: Preparation and Framing

## What we want to get out the design review:
- Clarify how we are going to encode the states because there are many complicated variables associated with pacman. Ex. Ghosts, capsules, bonus capsule. 
- Identify next steps

## Background and Context:
Project structure uses existing code from a computer science class at UC Berkeley. We are developing our own artificial intelligence algorithm to learn how to play pacman. The code we write will control the agent in the game to ultimately win as it learns from it’s experience. 
Please look the introduction and Q-learning questions on: http://ai.berkeley.edu/reinforcement.html 
Q-learning tutorial: ttp://mnemstudio.org/path-finding-q-learning-tutorial.htm
This tutorial was used to develop our first basic q-learning example

## Key Questions: 
- Best way to encode states? Especially with regard to ghosts
- Distance from closest ghost?
- Separate encoding for every ghost, since they behave differently?
- What happens when they are scared? Do we need a whole other R matrix?
- To what extent, if any, should we modify the Berkeley game structure code to improve our project?

## Agenda for Technical Review Session: (25 minutes)
- 5 min introducing the project + existing game architecture
- 10 min on encoding problem
- explain our current approach: show paper and draw it out on white board. 
- ask other teams if they see any issues with this or have better ways to do it
- 10 min on code architecture
- discuss our current state of affairs
- collaboratively ideate on what would be most effective
- should we mess with the Berkeley code?
- Identify next steps

## Feedback:
Pybrain Neural Fitted Q learning. Has features to add such as pellets around you, ghosts around you etc. board size doesn’t really matter I guess?
