# RL-Navigation

Project to train RL agent for [Udacity Navigation Environment](https://github.com/udacity/Value-based-methods/tree/main/p1_navigation)

## About Project

The notebook included in this repository trains a Deep Q Network to predict the action values for an agent in Udacity Navigation Environment, which in turn can be used to control the agent's policy towards optimal policy. 

![Navigation Environment Gif](udacity_navigation_env.gif)

[Gif Source: Udacity DRLND Repository](https://github.com/udacity/deep-reinforcement-learning/tree/master/p1_navigation)

In this environment, at each time step, the agent is given information about the environment in the form of a 37-dimensional vector, which contains information such as the agent's velocity and the ray-based view of objects in the agent's forward direction.

Based on this representation of the state, the agent can choose one of four actions (move forward, move backward, turn left, turn right) at each timestep to navigate around a large 2D space. 

When the agent runs into a yellow banana, the agent receives a reward of +1, while running into a blue banana yields a reward of -1. The goal of the agent is to maximize the reward at the end of each episode. 

The environment is considered "solved" when the agent receives an average reward > 13 over 100 consecutive episodes. 

## Dependencies

To set up your python environment to run the code in this repository, follow the adapted [instructions from Udacity DRLND repository](https://github.com/udacity/deep-reinforcement-learning) below:

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
	
2. If running in **Windows**, ensure you have the "Build Tools for Visual Studio 2019" installed from this [site](https://visualstudio.microsoft.com/downloads/).  This [article](https://towardsdatascience.com/how-to-install-openai-gym-in-a-windows-environment-338969e24d30) may also be very helpful.  This was confirmed to work in Windows 10 Home.  

3. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of OpenAI gym.  
	- Next, install the **classic control** environment group by following the instructions [here](https://github.com/openai/gym#classic-control).
	- Then, install the **box2d** environment group by following the instructions [here](https://github.com/openai/gym#box2d).
	
4. Clone the repository (if you haven't already!), and navigate to the `python/` folder.  Then, install several dependencies.  
    ```bash
    git clone git@github.com:jkim222383/RL-Navigation.git
    cd RL-Navigation/python
    pip install .
    ```

5. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.    
    ```bash
    python -m ipykernel install --user --name drlnd --display-name "drlnd"
    ```

6. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 

## Instructions

Follow the instructions on [Navigation Jupyter Notebook](p1_navigation/Navigation.ipynb).

You can choose to train a new model from scratch while experimenting with different combinations of hyperparameters (in `config_grid`), or simply load the pretrained model weights and observe the agent's policy in the environment. 
