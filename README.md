# Cartpole-Policy-Gradient-PyTorch
A policy gradient network was implemented for the OpenAI Cartpole using the PyTorch framework.

The purpose of this project is to use the concept of Policy Gradient which is under the branch of Reinforcement Learning to allow the OpenAI Cartpole to keep the Cartpole balanced by applying appropriate forces to a pivot point.

**Before training the Cartpole as shown below**

![](https://github.com/harrisloi/Cartpole-Policy-Gradient-PyTorch/blob/main/Images/Untrained%20Cartpole.gif)

**After training the Cartpole as shown below**

![](https://github.com/harrisloi/Cartpole-Policy-Gradient-PyTorch/blob/main/Images/Trained%20Cartpole.gif)

## Libraries
| Libraries used in this experiment  |
| ------------- |
| 1. Gym | 
| 2. Numpy |
| 3. Matplotlib |
| 4. Torch |
| 5. Pandas |
| 6. IPython |
| 7. random |
| 8. glob |
| 9. io |
| 10. time |
| 11. base64 |

## Hyperparameters
![Hyperparameters for the policy gradient approach](https://github.com/harrisloi/Cartpole-Policy-Gradient-PyTorch/blob/main/Images/Hyperparameters.png) 

We have a total of 5000 episodes to run in the training, max_t is the iteration of sampling the action from the current policy, gamma is the discount factor set to 0.95, and print_every variable simply means printing the result every 100 steps. Lastly, the learning_rate is set to 1e-2, which is 0.01 in this case.

## Results

![](https://github.com/harrisloi/Cartpole-Policy-Gradient-PyTorch/blob/main/Images/Cartpole%20Result%20with%20Adam%20Optimiser.png) 


We used Adam Optimization Algorithm for the policy gradient approach, this optimiser allowed us to be more able to get the maximum average reward, which is 190 for the Cartpole environment, to keep the pole vertical and horizontal without falling over. 

![](https://github.com/harrisloi/Cartpole-Policy-Gradient-PyTorch/blob/main/Images/Result.png) 


The maximum number of episodes was set to 5000, but the training process was terminated at set 3945 with an average reward of 195.03

## Experiment with different Gamma rates

We also conducted some experiments to see what results we would get from using different hyperparameters during training. The hyperparameter we modified was gamma, also known as the discount rate.

The gamma discount factor simply indicates how much the reinforcement learning agent is concerned regarding long-term rewards vs short-term rewards. The lower the discount factor, the less the agent is likely to be bothered about future actions, as it is only concerned with immediate returns. Conversely, when the discount factor is high, the agent will assess each of its actions against the sum of all its future rewards.

![](https://github.com/harrisloi/Cartpole-Policy-Gradient-PyTorch/blob/main/Images/Rewards%20in%20epochs%20for%20different%20Discount%20Factors.png) 

We can see that low discount factors like 0.85, 0.9 and 0.925 will usually receive lower rewards from time to time. There is no improvement at all when the discount factor is 0.85, which means the Cartpole agent did not learn any valuable action to maximise its rewards. While high discount factors like 0.95, 0.975 and 0.995 are more likely to have greater rewards. However, the higher discount factors mean a higher variance as the reinforcement learning agent will consider many unnecessary or irrelevant information during the training, which makes it challenging to learn.
