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

## Question 5

For the graph in the previous question, write out the steps of Dijkstra's Algorithm to find the shortest path between Node 1 and Node 11. For each step, write down the Unvisited set U, the Visited set V, and the current tenative distance vector D.
