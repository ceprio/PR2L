# PR2L

This is a repository for a small reinforcement learning library I made while reading "Deep Reinforcement Learning Hands-On" by [Maxim Lapan](https://github.com/Shmuma). The motivation for this library comes from PTAN being outdated with respect to the latest features of Gym/Gymnasium. Therefore this library is similar to PTAN with extra features for rendering environments and aiding training. A few functions here may be found in PTAN, however most have been replaced since the creation of this library. I've also left a few RL agent scripts in the repository as examples.

Currently, PR2L has six modules: training (new), agent, experience, playground, rendering, and utilities. Each module file includes a brief description of its usage.

Notes:
- The agent module is PTAN but with actions and agent modules all in one.  

******

RL SCRIPTS:

### A3C on BattleZone
An Asynchronous Actor Critic agent playing the Atari Battlezone game. The AtariPreprocessing class from OpenAI is used to process the agent's observation space before inference. Hence, the agent's observation space is reduced from the typical 210 by 160 RGB pixel ATARI observation to a more traditional 84 by 84 greyscale pixel format, along with other changes. To simulate motion, the current frame was combined with n prior frames, each of which has had its values decremented by an arbitrary amount.

<img src="https://github.com/Ianpro1/RL-agents/blob/master/GIF/BattleZone.gif" width="400">

******

### RainbowDQN-Variant on Freeway
This is a variant of the Rainbow DQN architecture playing Freeway.  
PREPROCESSING: The agent uses the same preprocessing as the above model.

<img src="https://github.com/Ianpro1/RL-agents/blob/master/GIF/Freeway.gif" width="400">

### DDPG on Tosser
A Deep Deterministic Policy Gradient agent playing Tosser: a MuJoCo task/environment by OpenAI.

<img src="https://github.com/Ianpro1/PR2L/blob/master/GIF/TosserCPPGIF.gif" width="600">

#### How to Install

Simply run these commands:  
```
>git clone https://github.com/Ianpro1/PR2L
>pip install ./PR2L
```

_Versions and Dependencies (NOT INCLUDED IN PACKAGE): PyTorch CUDA 11.6, Python 3.10.8, gym 0.26.2, Pygame 2.1.2 and gymnasium 0.27.1 (gymnasium is recommended over gym)._  
<sup>- Most dependencies will work at different versions with the exception of gym/gymnasium (the library handles truncated flags [Not Yet], therefore older versions are not supported.)</sup>
