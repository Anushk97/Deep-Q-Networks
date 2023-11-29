# RL-agent-trained-on-F1-race-environment

## Introduction 

The task is to develop a reinforcement learning model of a race car going around a circular track for a total of 162 laps for a given set of tires and weather conditions. The wear of the tires is given by formulas based on the weather condition, and the model should be able to automatically decide on the most appropriate tires for a given condition, which leads to a pit stop and incurring a time penalty to change the tires. The models performance will be benchmarked according to the shortest predicted time of the race car. 

## Proposed Methodology 

### Q learning and Deep Q networks  

The neural network would take the current state as input, which could be a combination of current tyre condition ‘a’, track wetness ‘w’ and possible current lap number. The action would have 5 neurons corresponding to each of the five actions (choosing one of the 4 type of tyres or continuing without the pitstop). After each epoch, the Q values will be updated using the reward which is the negative of the time taken in that epoch or lap. At every pitstop opportunity, the algorithm will use the current Q values to decide on an action. Overtime, by exploring different actions and observing different rewards, the neural network will optimize the Q-values for the state action pairs.  

