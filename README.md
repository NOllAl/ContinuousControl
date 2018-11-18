# Introduction

In this project, we use the [Deep Deterministic Policy Gradient (DDPG)](https://arxiv.org/abs/1509.02971) algorithm for a robotics problem. Specifically, a robotic arm is supposed to track a moving target. 

## Environment

The environment is the [Unity Reacher environment](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher). The robotic arm has two joints and should follow a target location. We use 20 robotic arms simultaneously to speed up training. 

### Observation Space

The observation space is 33 dimensional corresponding to position, velocity and angular velocity of the arm.

### Actions Space

The action space is four dimensional and the four dimensions correspond to the torque applied to the two joints and take value between -1 and 1.

### Reward

Whenever the agent is in the goal location, a reward between 0.01 and 0.04 is award, depending on how close it is to the center of the target sphere.

The environment is considered solved if the the agents receive and average score of 30 over 100 consectutive episodes.


# Installation

#### Step 1: Clone the repo
`git clone https://github.com/NollAl/continuous_control.git`.


#### Step 2: Install Dependencies
Create a conda environment that with the required dependencies to run the project (here for Mac)

```
conda create --name drlnd_continuous_control python=3.6
source activate drlnd_continuous_control
conda install -y python.app
conda install -y pytorch -c pytorch
pip install torchsummary unityagents
```


#### Step 3: Download Reacher environment

Install the [pre-compiled Unity environment](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip).  

Download the file into the top level directory of this repo and unzip it.


## Train your agent

To train the agent run the notebook `Report.ipynb`.