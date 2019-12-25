[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/42386929-76f671f0-8106-11e8-9376-f17da2ae852e.png "Kernel"


# Project 2: Continuous Control

### Introduction

This project is solving [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment with [DDPG](https://towardsdatascience.com/deep-deterministic-policy-gradients-explained-2d94655a9b7b) algorithm.

![Trained Agent][image1]

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

### Distributed Training

For this project, I was provided with two separate versions of the Unity environment:
- The first version contained a single agent.
- The second version contained 20 identical agents, each with its own copy of the environment.  

I have chosen the second version as it is more useful for algorithms like [PPO](https://arxiv.org/pdf/1707.06347.pdf), [A3C](https://arxiv.org/pdf/1602.01783.pdf), [D4PG](https://openreview.net/pdf?id=SyZipzbCb), and [DDPG](https://towardsdatascience.com/deep-deterministic-policy-gradients-explained-2d94655a9b7b) that use multiple (non-interacting, parallel) copies of the same agent to distribute the task of gathering experience.  
### Dependencies
This project is designed to work within **_[DRLND](https://github.com/udacity/deep-reinforcement-learning#dependencies)_** anaconda environment.

### Getting Started
1. Follow the steps to install [DRLND](https://github.com/udacity/deep-reinforcement-learning#dependencies) repository

2. Download and place the environment in `deep-reinforcement-learning\p2_continuous-control`.  You need only select the environment that matches your operating system:

    - **_ Twenty (20) Agents_**
        - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
        - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

3. Download and place contents of this repository in `deep-reinforcement-learning\p2_continuous-control`

4. Launch Anaconda Prompt and type `jupyter notebook`

5. Change active kernel to drlnd  
![Kernel][image2]

6. Navigate to `deep-reinforcement-learning\p2_continuous-control` and select `Continuous_Control.ipynb` to get started with training your own agent!  
