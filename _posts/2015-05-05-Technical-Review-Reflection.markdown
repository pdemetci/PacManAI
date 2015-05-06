---
layout: post
title:  "Tehcnical Review Reflection"
date:   2015-05-05 00:07:00
categories: jekyll update
---

 Technical Review Process Reflection

### How did the Review go?

After the design review last week, we decided to implement Q-learning with function approximation instead of having a Q matrix to improve computational efficiency. At the technical review, we showed our implementation with two features that help us with computing the Q-value for state-action pairs: a feature for getting the PacMan to capsules and another function for moving to general areas with a high food density. The set exploration rate determined the probability of whether pacman would move randomly or execute an action based on the current weights of each feature. We updated the weights for the features in thefunction based on pacman’s reward. Key questions we had from our implementation were how to update the  weights for each function, in addition to which features to implement and how to prioritize them. In our Preparation and Framing document, we broke these questions up into questions for everyone, which were at an appropriate level for our peers, and questions specifically for Paul, who has expertise in reinforcement learning. 
We provided our audience context with a Reinforcement Learning: Q-Learning Adaptation Guide to abstract the mathematical concepts involved with our project for their understanding. By reviewing our current specific implementation of Q-learning in our program, our audience provided useful insights from the technical review that answered our questions and helped us determine our next steps.

### Did we get answers to our key questions?
### Questions for all
**Question 1:**Looking at the measurements listed, which ones do you think will be the most important and when? Also, what other measurements from the pacman environment may be useful to include in our function?
* Our list of possible environmental measures to include in the function was validated by our peers because they did not have any additions. However, they thought that we should prioritize the measurements as: pacman’s distance from the nearest capsule, the amount of time since pacman ate food and the food/unexplored areas closest to pacman. Focusing on the food location may be advantageous because pacman will learn where the capsules with experience and we will not need to code pacman’s long term behavior of going to a specific location. We hope to optimally tweak the weights of each feature. 

**Question 2:**What might some of the measurement functions look like?
* We discussed our current  function implementation of calculating the distance between pacman and a capsule and trying to implement it. If we continue to include the capsule location as a feature of the  function, we hope to adjust this to accommodate for walls by using astar search to calculate the distance and plot a path. As far as keeping track of food locations, part of the learning algorithm will “remember” explored and unexplored squares. In determining pacman’s focus, counting the amount of time since pacman last ate food may be helpful in prioritizing the weights of each variable in the  function, especially because we want to optimize pacman’s score and pacman’s score decreases with every second it does not eat food.

**Question 3:**Is it best to store the weight vector by pickling? Or is there a better method? (Dependent on Question 1 for Paul)
* The answer to this question really depends on whether pacman is learning over one game (our MVP - offline learning), which case the weight vector does not need to be stored, or multiple games (online learning), where the weight vector would be stored by pickling. 

**Question 4:**Ideas for implementing Manhattan distance with walls?
* Use Astar; alternatively, have it go in one direction eating food until it hits a wall, and only then make another decision. The latter would help prevent the difficulties our latest implementation was hitting, where it would go back and forth in the general vicinity of the nearest capsule.

###Questions for Paul

**Question 1:**When and how do we  update the weights vector? How do rewards factor in? In other words, how does the weight’s vector map to the feature which got the agent to it’s present state? Maybe update by keeping track of Q? Or time since agent ate a capsule?
* How to update the weight vector is apparently a hot area of research, but we will find papers describing an implementation or just use a library to update them for us, as well as communicate our findings to Paul.
 
**Question 2:**What is the purpose  of the constant b and what does it do?
* The b constant is the y intercept for a fit function. The y axis of that fit function would be the for a specific feature, and the x axis would be the value of the weight w for that feature. 


###Did we stick closely to our planned agenda, or did we consider new things during the discussion that made you change your plans?

We stuck fairly close to our planned agenda. We showed code as we discussed our current  
function implementation (before the last five minutes), because we wanted to provide our peers and educators with a visualization of our current difficulties. To further explain why pacman seemed confused in constantly changing direction, we showed our audience how we were updating the weight vector and finding rewards, which gave them a better understanding of where they could make suggestions to help us. 

###What could you do next time to have an even more effective technical review?
We could have done more research in implementing the weight vector and understanding more of the mathematics behind our Q-learning implementation. 


## Feedback and Decisions:
###How do you plan to incorporate feedback going forward?


Paul has sent us an article titled “Reinforcement Learning in Continuous State and Action Spaces” which talks about various algorithms and methods for finding optimal decision policies and updating parameters in reinforcement learning in continuous domains. We will find more articles based on the questions that come up during this process. After reading the articles and discussing how we could implement our project based on that, we are planning to have another meeting with Paul within a week.
One suggestion we got was to implement Q-learning in a simple layout, where we know the optimal path and comparing the Q-values and policies generated by our code to the ones we calculate ourselves. This could help us enhance our understanding about how functions compute Q-values and which function leads to what result. This should give us clearer view on how to move forward with function approximation techniques when we move on to more complex layouts.

The discussion with the audience in the class was useful to understand the key strategies for winning PacMan. For our implementation without the ghosts, we will stick with the audience’s suggestions on prioritizing the capsules, and then the time. They further suggested that we could use A* search for reaching the capsules and food. In our implementation with functions and weight updates, we will take these suggestions into account. In our final steps, we will work on testing and modifying our parameters to optimize the algorithm. 


### What new questions did we generate?
* How do we do the step-by-step calculations for a really simple board? (We tried this after the review and got stuck.)
* Should we use a library to update the weights or should we write our own implementation based on papers we read?
* Do we need to use a library/find a paper describing how to assign rewards as well? 
* What is the best architecture for us? We could do something like PyBrain, where there are Agents, Learners, Tasks, and Environments, but aren’t sure if this is too much overhead for our less-general application.
* Are we going to use a discrete action space or a continuous one?
* What is the best way to test and modify parameters?

