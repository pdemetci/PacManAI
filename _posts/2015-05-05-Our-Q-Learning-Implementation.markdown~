---
layout: post
title:  "Our Q Learning Implementation"
date:   2015-05-05 05:30:00
categories: jekyll update
---

On a large board, PacMan esentially operates in a continuous state space. In such a space, implementing Q values in a matrix is not viable. To address this, we have abstracted states to linear combinations of features instead of PacMan's coordinates on the board.

![Q Function Approximation]({{ site.url }}/assets/approximateQ.png){: .center-image }

Learning happens when the agent updates the weights associated with each feature after every move and learns which features to prioritize. This makes the approximated Q value converge to the real Q value.

![Weight Update Function]({{ site.url }}/assets/weightupdates.png){: .center-image }

The features we have included are: 
- Nearest capsule distance
- Food pellet distance
- Nearest ghost distance
- Nearest scared ghost distance
- Score

Our code architecture is explained in the diagram below. The classes we have implemented are "Features", whis is the super class of all the features used in Q value approximation and SimpleQAgent, which is the learning agent. The other classes create the game environment. 

![Code Architecture]({{ site.url }}/assets/UMLDigram_Pacman_withoutAttributesMethods.png)

For further information on reinforcement learning in continuous spaces, you can download and check Hado van Hasselt's paper on [Reinforcement Learning in Continuous State and Action Spaces](http://webdocs.cs.ualberta.ca/~vanhasse/papers/RL_in_Continuous_Spaces.pdf) 

