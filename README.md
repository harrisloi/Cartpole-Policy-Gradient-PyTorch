# Cartpole-Policy-Gradient-PyTorch
A policy gradient network was implemented for the OpenAI Cartpole using the PyTorch framework.

The purpose of this project is to use the concept of Policy Gradient which is under the branch of Reinforcement Learning to allow the OpenAI Cartpole to keep the Cartpole balanced by applying appropriate forces to a pivot point.

**Before training the Cartpole as shown below**

![](https://github.com/harrisloi/Cartpole-Policy-Gradient-PyTorch/blob/main/Images/Untrained%20Cartpole.gif)

**After training the Cartpole as shown below**

![](https://github.com/harrisloi/Cartpole-Policy-Gradient-PyTorch/blob/main/Images/Trained%20Cartpole.gif)

Libraries used in this experiment
1. Gym
2. Numpy
3. Matplotlib
4. Torch
5. Pandas
6. IPython
7. random
8. glob
9. io
10. time
11. base64

![Hyperparameters for the policy gradient approach](https://github.com/harrisloi/Cartpole-Policy-Gradient-PyTorch/blob/main/Images/Hyperparameters.png) We have a total of 5000 episodes to run in the training, max_t is the iteration of sampling the action from the current policy, gamma is the discount factor set to 0.95, and print_every variable simply means printing the result every 100 steps. Lastly, the learning_rate is set to 1e-2, which is 0.01 in this case.


