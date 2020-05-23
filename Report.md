# project 3 : Collaboration and Competition 

In this environment , its a tennis playing 2D environment , where 2 agents control 2 rackets on 2 opposite side of the court they have to compete with each other. If an agent hits the ball over the net, it receives a reward of +0.1.  If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01.  Thus, the goal of each agent is to keep the ball in play.

the task here is an episodic task , the environment must get +0.5 over 100 consecutive episodes 

#Algorithm Used 

A deep determinsitic Policy Gradient was proposed in continious control with deep reinforcement learning DDPG is an off policy algorithm and is used in continious action apaces
it parallely learns the function and a policy . its an actor critic method that uses 2 neural networks. the algorithm uses experience replay and target networks to stabilize the training in the neural networks . 

The network consists of 3 fully connected layers with batch normalization applied . the network maps the pairs to Q-values. it uses ReLU as activation function in the first 2 layers .


# Hyperparameters Used 

	
    fc1_units=400 # Number of nodes in the first hidden layer
    fc2_units=300 # Number of nodes in the second hidden layer
    BUFFER_SIZE = int(1e6) # replay buffer size
    BATCH_SIZE = 256 # minibatch size
    GAMMA = 0.99 # discount factor
    TAU = 2e-3 # for soft update of target parameters
    LR_ACTOR = 1e-3 # learning rate of the actor
    LR_CRITIC = 1e-3 # learning rate of the critic
    WEIGHT_DECAY = 0 # L2 weight decay
    LEARN_EVERY = 1 # learning timestep interval
    LEARN_NUM = 10 # number of learning passes
    GRAD_CLIPPING = 1.0 # gradient clipping
    EPSILON = 1.0 # for epsilon in the noise process (act step)
    EPSILON_DECAY = 1e-6 # epsilon decay rate

