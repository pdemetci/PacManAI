---
layout: post
title:  "Design Process"
date:   2015-05-05 05:45:00
categories: jekyll update
---

1. We began our project by developing our project goals and abstracting the system
2. We decided on a type of AI algorithm to apply. Based on our research and our instructors, Paul Ruvolo, suggestion, we decided to learn about reinforcement learning.
3. We determined to use Q-learning because it seemed to be the most common type of reinforcement learning. We started off with the simplified version on the “Painless Q-Learning Tutorial” site.
4. We tried to apply what we had learned from that tutorial to Pacman, but realized that with any normal layout we would have an absurd number of states to keep track of. To address this problem, we tried to think of ways to make fewer states.
5. We took our ideas to our first design review, where Paul encouraged us to look at the states as linear combinations of features. That way, we could replace the gigantic Q matrix with a Q function, and the weights associated with the features would guide the action selection policy.
6. We built a simple agent class to test out the concept of exploration rate, but it wasn’t very effective.
7. We read “Reinforcement Learning in Continuous State and Action Spaces,” and spent a long time trying to understand the mathematical concepts. 
8. We implemented the math to the best of our abilities in a new agent class, SimpleQPacman.
9. In our implementation, we decided to add a Feature class to allow easy testing of which features were helpful and which ones were not.
10. Many of our features used a distance, which was initially calculated as a Manhattan distance. Because it did not take walls into account, our Pacman often got stuck. To fix this, we decided to implement a distance finder using an A-star search algorithm.
11. We experimented with different features, including the nearest capsule, the nearest ghost, the nearest food pellet, the total food pellets remaing, the nearest scared ghost, the score, and the capsules remaining. We found the distance based features to be the most effective based on our observations in watching pacman play the game with our algorithm. 
12. The A-star distance finding algorithm was computationally inefficient when determining the nearest food, because of running A-star for every pellet on the board. In order to improve efficiency , we implemented a depth-first search algorithm to first find a food pellet and then perform A-star once per feature extraction.
13. We tweaked our learning rate, exploration rate, and discount factors.
