# CSE 017 - Quiz 5

Due: 8/3 by end of day

Make one commit per question (at least).

## Question 1 

Consider the Depth First Search graph algorithm versus the Breadth First Search algorithm. They are very similar, except one uses a stack and the other uses a queue. How does the choice of datastructure in the affect the execution of the respective algorithms?

Breadth First Search uses a queue, while Depth First Search uses a stack. The type of datastructure used will determine what order the search takes place in because Queues are LIFO and Stacks are FIFO.

## Question 2

What is the difference between a tree and a graph?

A tree has parents and children leafs, but a graph can have an overall cycle going to any other leaf of the graph and can have multiple directions

## Question 3

In the circular queue datastructure we have `front` and `back` variables. What is their purpose? Why do we design the queue this way?

The front variable points to the first element in the circular queue, and the back variable points to the last element in the circular queue. This is where the circle gets connected. The next inserted item in the queue becomes the rear of the queue.

## Question 4

Encode the following graph as an adjacency matrix

![Graph](https://github.com/cmontella/cse017-quiz5/blob/master/graph.png?raw=true)

    1. 2. 3. 4. 5. 6. 7. 8. 9. 10. 11.
1.  0  0  0  13 0  0  2  0  0  0   0
2.  1  0  0  0  0  0  0  0  0  0   0
3.  25 2  0  0  30 0  0  0  0  0   0
4.  0  0  0  0  0  0  0  0  0  0   0 
5.  0  5  0  0  0  4  0  14 0  0   0
6.  0  0  11 0  0  0  0  0  9  0   0 
7.  0  0  0  12 0  17 0  0  0  8   0
8.  0  0  0  0  0  0  0  0  3  0   6
9.  0  0  0  0  15 0  0  0  0  0   0  
10. 0  0  0  0  0  0  0  0  8  0   0
11. 0  0  0  0  0  0  0  0  0  7   0

## Question 5

For the graph in the previous question, write out the steps of Dijkstra's Algorithm to find the shortest path between Node 1 and Node 11. For each step, write down the Unvisited set U, the Visited set V, and the current tenative distance vector D.

1.) Make an unvisited list
U = {1,2,3,4,5,6,7,8,9,10,11}
2.) Assign distance so far
D = [∞,∞,∞,∞,∞,∞,∞,∞,∞,∞,∞]
3.) For the current node, calculate distances to adjacent nodes through current node
D = [0,∞,∞,13,∞,∞,2,∞,∞,∞,∞]
4.) Mark current node as visible
V = {1}, U = {2,3,4,5,6,7,8,9,10,11}
5.) Choose unvisited node with the shortest distance so far as the next node
6.) Go to 3 and continue.

Current = 7                                     Current = 10                                Current = 4                             Current = 9
V = {1}                                         V = {1,7}                                   V = {1,7,10}                            V = {1,4,7,10}
U = {2,3,4,5,6,7,8,9,10,11}         --->        U = {2,3,4,5,6,8,9,10,11}       --->        U = {2,3,4,5,6,8,9,11}       --->       U = {2,3,5,6,8,9,11}
D = [0,∞,∞,13,∞,∞,2,∞,∞,∞,∞]                    D = [0,∞,∞,13,∞,∞,2,∞,∞,8,∞]                D = [0,∞,∞,13,∞,∞,2,∞,8,8,∞]            D = [0,∞,∞,13,15,∞,2,∞,8,8,∞]

Current = 5                                     Current = 8                                Current = 11                             
V = {1,4,7,9,10}                                V = {1,4,5,7,9,10}                         V = {1,4,5,7,8,9,10}                    
U = {2,3,5,6,8,11}                  --->        U = {2,3,6,8,11}                --->       U = {2,3,6,11}               
D = [0,5,∞,13,15,4,2,14,8,8,∞]                  D = [0,5,11,13,15,4,2,14,8,8,∞]            D = [25,7,11,13,45,4,2,14,8,8,6]

Shortest path = 53

    


