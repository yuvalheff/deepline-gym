# gym-deepline
![](render.gif)

This project is the implementation of DeepLine, a system for automatic machine learning pipeline generation. 
DeepLine is a deep reinforcement learning-based framework. It consists of a grid-world environment in which the pipeline generation process is modeled in a semi-constrained setting, and a DDQN agent.

DeepLine also introduces a novel method for handling large discrete action spaces where most of the actions are invalid in most states. The Hierarchical Step filters only the set of vaild actions by quering the agent iteratively on small subsets of the actions space. 
Extensive description of the framework is available in `deeplineThesis.pdf`.

## Installation
After cloning the repository, do the following:
```bash
cd gym-deepline
pip install -e .
```
Create a and activate a conda environment with Python 3.6 and run -
```bash
pip install -r requirements.txt
```
If you are using a MAC, you might need to run - 
```bash
brew install libomp
```

## Instructions
DeepLine's environment is implemented as an [OpenAI-Gym](https://gym.openai.com/) environmnet, and can be called by:
```python
import gym
import gym_deepline

env = gym.make('deepline-v0')
```

The environment itself is implemented in `envs/atml_env.py` and the three versions of the agent are under `agents/`.

For a more detailed example, see `example.py`.
