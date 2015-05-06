---
layout: post
title:  "What is Reinforcement Learning?"
date:   2015-05-05 05:45:00
categories: jekyll update
---

**Reinforcement learning** is a type of **artificial intelligence** that tries to determine the **best action for an agent to take in a given state based on immediate and cumulative rewards.** It is used in many different fields including **game theory**, **statistics**, **control theory**, and **simulation-based optimization**. In general reinforcement learning is **unsupervised**, meaning that it is never shown the **“correct answer”** to make adjustments to its parameters. Reinforcement learning agents usually use a **Markov decision process (MDP)** to select the best action for the state they are in (or, more generally, to form a policy for choosing actions based on the state). In an MDP, given a state and an action, the state transitions are conditionally independent of all previous states and actions. In reinforcement learning, the agent doesn't have a model of the environment to begin with; it learns an approximation of the environment by interacting with it. 

![Reinforcement Learning Diagram]({{ site.url }}/assets/ReinforcementLearning.png)

There is also a tradeoff between "exploration and exploitation" in reinforcement learning. Exploration (generally implemented as random action selection) is necessary because if the agent only interacts with part of its environment it will optimize for that part and not be suited to deal with the rest. The video below shows a test agent we made based only on this concept.

<iframe width="560" height="315" src="https://www.youtube.com/embed/eg_0URXVBGM" frameborder="0" allowfullscreen> </iframe>

For Pacman, the actions are simple: **North, South, East, West, or Stop**. The rewards are also simple: **food is +10, ghosts are -500 or +200, depending, and a win is +500**. The states, however, get tricky. On a large board, Pacman is essentially operating in a continuous state space (actually it's just a very large discrete state space, but for practical purposes they're the same thing). We abstracted states to mean linear combinations of hand-picked features (like the current distance to the nearest ghost or food pellet) instead of Pacman’s coordinates on the board.

<img style="float: left" src="{{ site.url }}/assets/pacmandirections.png">

The picture on the left shows the action space, which consists of five actions: North, South, East, West, and Stop.

**Q learning** is a type of reinforcement learning algorithm. It calculates the "quantity" of a state-action combination. Each time the agent selects an action it observes a reward and enters a new state. **The Q-value is updated based on the new information. The next action is selected to maximize the Q value so that the agent gets as much reward (both immediate and cumulative) as possible.**

![Q Value Calculation]({{ site.url }}/assets/Q_LearningAlgorithm.png)

The example below is from [UC Berkeley's CS188 course](https://inst.eecs.berkeley.edu/~cs188/fa09/projects/reinforcement/reinforcement.html) It demonstrates an environment where reaching the green tile would bring a big reward and the tile below that would end the game. The Q value matrix starts with 0s. The image below demonstrates the Q values after the first episode, where the agent started at the top left hand-side corner and constantly moved left until it reached its goal. The Q values for the state-action pairs it took are updated in this image. Notice that the state-action pairs that lead to the reward have positive Q values and they increase as the state-action pair gets closer to the reward tile. This is because the Q learning algorithm takes into account the future expected reward. The image below reflects the Q values after multiple episodes, throughout which agent gets to explore every state-action pair.

![Initial Q values]({{ site.url }}/assets/QValues_initial.png)

Notice that the Q value assigned to the 'death tile' which ends the game is the lowest value and the state-action pairs that lead to this tile also have negative Q values. Learning agent takes actions based on these updated Q values in order to maximize the reward it gets.

![Final Q values]({{ site.url }}/assets/QValues_final.png)


