# Continous Control project

## Description

### Environment
The task in this project is to train a reinforcement learning agent to control a double jointed arm with a hand at the top. The agent is supposed to move the hand to a goal location defined by the environment and highlighted by a green sphere. The agent receives a reward of +0.1 for each time step that the agents hand is in the target position.

<p align="center">
	<img src="content/reacher_env.gif" width=50% height=50%>
</p>

There are two types of environments available. One environment does only contain a single arm, while the second environment contains 20 arms that need to be controlled and trained in parallel.


### Task
The code in this repository is applied to the single arm environment. In total there are 33 state parameters corresponding to position, rotation, velocity, and angular velocities of the arm. An action is described with four numbers between -1 and 1 corresponding to torque applicable to the two joints.

The task is considered to be solved if the agent has achieved an average score larger than 30 over 100 consecutive episodes.


## Setup

### File description
- `Continuous_Control.ipynb`: Jupyter notebook to load the environment and train the agent
- `ddpg_agent.py`    : Contains an agent class that interactions with and learns from the environment
- `ddpg_model.py`    : Contains a model class that creates a q-network for the agent
- `agt_actor_check.pth`    : File containing the successful actor network
- `agt_critic_check.pth`   : File containing the successful critic network
- `report.pdf`      : Report about the used approaches and presentation of results
- `requirements.txt`: Text file containing the installation requirements

### Dependencies
To execute the code in the Continous_Controle notebook, you need to have a Python 3 environment. In addition you need to install all required packages  listed in `requirements.pip` by executing the following command:
```
pip install requirements.txt
```

To execute the environment on your machine, you need to download the environment which matches your operating system from one of the links below. Afterwards, you need to unzip the file in your repository folder.

- Linux : [Download link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
- MAC OSX : [Download link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
- Windows (32-bit): [Download link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
- Windows (64-bit): [Download link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)


## Execution

Open the `Continuous_Control.ipynb` notebook and execute the cells in sequential order to load and explore the environment and to train the agent. The training time can be varied by modifying the `n_epsiodes` and `max_t` parameter of the `ddpg` function used to train the agent. All other parameters to optimize the training are already set inside the `ddpg_agent.py` file.
