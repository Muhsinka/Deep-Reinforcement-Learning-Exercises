# The Environment
This project works with the [CartPoleV1](https://gym.openai.com/envs/CartPole-v1/)

![1_oMSg2_mKguAGKy1C64UFlw](https://user-images.githubusercontent.com/43606874/57767825-f4b30380-7712-11e9-9893-a78ecfd9e9ad.gif)

A pole is attached by an un-actuated joint to a cart, which moves along a frictionless track. The system is controlled by applying a force of +1 or -1 to the cart. The pendulum starts upright, and the goal is to prevent it from falling over. A reward of +1 is provided for every timestep that the pole remains upright. The episode ends when the pole is more than 15 degrees from vertical, or the cart moves more than 2.4 units from the center.

# Dependencies

To set up your python environment to run the code in this repository, follow the instructions below.

1. Create (and activate) a new environment with Python 3.6.

	- __Linux__ or __Mac__: 
	```bash
	conda create --name drlnd python=3.6
	source activate drlnd
	```
	- __Windows__: 
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```
	
2. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of OpenAI gym.  
	- Next, install the **classic control** environment group by following the instructions [here](https://github.com/openai/gym#classic-control).
	- Then, install the **box2d** environment group by following the instructions [here](https://github.com/openai/gym#box2d).
	
3. Clone the repository (if you haven't already!), and navigate to the `python/` folder.  Then, install several dependencies.
```bash
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.  
```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

5. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 

# Installation

Follow the instructions below to explore the environment on your own machine! You will also learn how to use the Python API to control your agent.

## Step 1: Activate the Environment
If you haven't already, please follow the instructions in the DRLND GitHub repository to set up your Python environment. These instructions can be found in README.md at the root of the repository. By following these instructions, you will install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project.

(For Windows users) The ML-Agents toolkit supports Windows 10. While it might be possible to run the ML-Agents toolkit using other versions of Windows, it has not been tested on other versions. Furthermore, the ML-Agents toolkit has not been tested on a Windows VM such as Bootcamp or Parallels.

SPECIAL NOTE TO BETA TESTERS - please also download the p3_collab-compet folder from here and place it in the DRLND GitHub repository.

## Step 2: Installation

To get started, you’ll need to have Python 3.5+ installed. Simply install gym using pip:

```pip install gym```

## Building from Source
If you prefer, you can also clone the ```gym``` Git repository directly. This is particularly useful when you’re working on modifying Gym itself or adding environments. Download and install using:

```git clone https://github.com/openai/gym
cd gym
pip install -e .```

You can later run ```pip install -e .[all]``` to perform a full installation containing all environments. This requires installing several more involved dependencies, including ```cmake``` and a recent ```pip``` version.

## Enviroments
Here’s a bare minimum example of getting something running. This will run an instance of the CartPole-v0 environment for 1000 timesteps, rendering the environment at each step. You should see a window pop up rendering the classic cart-pole problem:

```import gym
env = gym.make('CartPole-v0')
env.reset()
for _ in range(1000):
    env.render()
    env.step(env.action_space.sample()) # take a random action
env.close()```
