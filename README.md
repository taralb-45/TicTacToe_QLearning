# TicTacToe_QLearning
Q Learning algorithm implementation for Tic Tac Toe <br/>

# Description
This notebook contains code for Q Learning along with environment for playing the game.<br/>
The code is written in non oop manner for easier manipulation of constraints during training.<br/>

Custom environment for TIC TAC TOE is written from scratch.<br/>
The jupyter notebook has different cells for initialization, training and for playing with agent or 2 agents playing against each other.<br/>
Each cell has comments regarding what it does and cells are in order of execution.<br/>

# Controls
The numpad is mapped as 3x3 grid. <br/>
Player can use numpad as grid to play with agent.<br/>
For example 7 on numpad referes to top left box in the board.<br/>

# Training
Two empty Q tables are initialized for each agent.<br/>
Q variable is a list which contains all states of a tic tac toe game.<br/>
To update a Q value, index of a board is found by method Q.index(board_state).<br/>
It is used along with action (move) to enter reward in Q table for each agent after their turn using the Bellman Equation.<br/><br/>
![Bellman Equation](https://miro.medium.com/v2/resize:fit:720/format:webp/1*vTMQI14ls9lWzRXzJGi4sg.jpeg)<br/>
During training I have implemented the first move to be a random or if there are no Q values associated to current state.<br/>

The agents are trained for 60,000 games with epsilon greedy approach with value of epsilon being 0.8 for first 10,000 episodes.<br/>
This is done in order to increase exploration in initial games.<br/>
After that epsilon is set to 0.5 and decayed by 0.99 for next 40,000 episodes.<br/>
For last 10,000 epsilon is set 0.1 and not decayed.<br/>
<br/>
After the training it learnt to play fairly well against player.<br/>
But one problem persists. That is the agent playing in sequential order against each other even after randomizing first and second moves in training.<br/>


# Files
q1.xyz and q2.xyz are 2 files which are the q tables for agents. <br/>
To load it simply run the pickle.load cell, it will initialize the Q values for both agents.
