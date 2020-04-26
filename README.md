# DRLND-Project3-collab-compet
This repository contains my implementation of multi-agent Tennis environment project for Deep Reinforcement Learning Nano Degree program. For this project, a multi-agent framework is set. Multi-agent Deep Deterministic Policy Gradient (DDPG) is used to solve the [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment.

## Goal of the Project
The task is episodic, and in order to solve the environment, agents must get an **average score of +0.5 for over 100 consecutive episodes**, after taking the maximum over both agents. 

## Environment
[Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment can be downloaded from the following links for different operatin systems:

    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux_NoVis.zip) to obtain the "headless" version of the environment.  You will **not** be able to watch the agent without enabling a virtual screen, but you will be able to train the agent.  (_To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the **Linux** operating system above._)

## State/Action Space and Reward
The **state/observation space** consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation.

The **action space** has dimention of two, which are continuous, corresponding to movement toward (or away from) the net, and jumping. 

The **reward**  function is defined that after each episode, the rewards that each agent has received are added up (without discounting), to get a score for each agent. This yields 2 (potentially different) scores, then the maximum of these two scores yields a single score for each episode.

## Instructions
1. Activate the conda environment `drlnd` as established in [Udacity deep reinforcement learning repository](https://github.com/udacity/deep-reinforcement-learning)
2. Open `Tennis.ipynb` and follow the instructions in it.
3. Change kernel to `drlnd` in `Tennis.ipynb`
4. Unzip the downloaded Tennis environment and give its path to `file_name="..."` in `Tennis.ipynb`.
5. Execute the code cell in `Tennis.ipynb` from beginning to the end. The trained agent will be saved in `checkpoint_actor.pth` and `checkpoint_critic.pt` if the average score > 0.5.

