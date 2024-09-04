# TicTacToe_QLearning
Q Learning algorithm implementation for Tic Tac Toe

# Description
The jupyter notebook has different cells for initialization, training and for playing with agent or 2 agents playing against each other.

Two empty Q tables are initialized for each agent.

#Training
Q variable contains all states which are possible and index of a board is found by method Q.index(board_state).
It is used along with action (move) to enter reward in Q table for each agent after their turn.
During training I have implemented the first move to be a random or if there are no Q values associated to current state.
