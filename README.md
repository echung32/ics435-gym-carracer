# TLDR
Homework assignment in which students must train a convolutional neural network (CNN) to drive a car using Behavioral Cloning on OpenAI Gym's implementation of CarRacer.

# OpenAI CarRacing with Behavioral Cloning

In this homework, you will train an agent to drive on a race track in a video-game style simulator. The agent has a neural network controller that you will train using example data of a car racing around the track. At each timestep, the neural network takes in the *state* of the car as an image and outputs which *action* to take. This system is known as a *Markov Decision Process (MDP)* because at each discrete timestep, the agent makes a decision using only the current state, with no memory of the previous state (this is called the Markov property). 

The simulator is the CarRacing-v2 environment from OpenAI. In this environment, a *state* is a (96, 96, 3) color image which shows the position of the car along with the current speed, stearing position, and braking status in the bottom of the image. The *actions* that are available to the agent are stear (between -1 and 1), accelerate (0 to 1), and break (0 to 1). To simplify this assignment, I have converted this into a classification problem with only seven discrete actions:

0. Do nothing
1. Left
2. Left+Break
3. Right
4. Right+Break
5. Accelerate!
6. Break

A dataset of 11,132 example (state, action) pairs is provided for training. These were sampled from simulations of a highly-skilled AI agent. In the context of Reinforcement Learning, this training strategy is known as *behavioral cloning* because we are learning by copying the actions of another agent.  

The first cell downloads the data and installs many of the dependencies needed to run the simulations and generate videos in Google Colab. You should be able to train your agent and view videos of your agent within Colab.

## Tasks:
1.   Create a class called `Agent` with methods 'train' and 'act'.
2.   Train the agent to drive. Optimize hyperparameters such as the learning rate, network architecture, etc. You can do this by hand (you don't need to do anything fancy).
3. Create a video of your agent driving.

## To turn in:
1. Your code as a jupyter notebook.
2. A description of your agent model and its performance. Include this description after your code in the jupyter notebook. I don't expect you to do extensive hyperparameter tuning, but you **must** describe the performance of your model on a validation set using the appropriate metrics so that you know when you are overfitting.
3. Upload a video of your best agent to [this google drive]([https://drive.google.com/drive/folders/1Hk4PTqfr5A3BeW2m3mgAuQmbxo_Z-8AK?usp=sharing](https://drive.google.com/drive/u/1/folders/11PlWaXvLYgVHY55vMEvKwWECsp1hO0wH)). (Feel free to also upload any funny or interesting behavior.)
