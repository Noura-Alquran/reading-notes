# Read: Implementation Graphs Summary :
* **A Graph** is a *non-linear* data structure consisting of nodes and edges. The nodes are sometimes also referred to as vertices and the edges are lines or arcs that connect any two nodes in the graph.
###### Common terminology:
1. **Vertex** - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
2.  **Edge** - An edge is a connection between two nodes.
3.  **Neighbor** - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
4.  **Degree** - The degree of a vertex is the number of edges connected to that vertex.

###### Directed vs Undirected
* **An Undirected Graph** is a graph where each edge is undirected or **bi-directional**. This means that the undirected graph does not move in any direction.
* **A Directed Graph** also called a **Digraph** is a graph where every edge is directed. Each node is directed at another node with a specific requirement of what node should be referenced next.

###### Complete vs Connected vs Disconnected
* **A complete graph** is when all nodes are connected to all other nodes.
* **A connected graph** is graph that has all of vertices/nodes have at least one edge.
* **A disconnected graph** is a graph where some vertices may not have edges.

###### Acyclic vs Cyclic
* **An acyclic graph** is a directed graph without cycles.
* **A Cyclic graph** is a graph that has cycles.

### Graph Representation
* We represent graphs through:
1. ***Adjacency Matrix***   
* An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix. Each Row and column represents each vertex of the data structure. The elements of both the column and the row must add up to 1 if there is an edge that connects the two, or zero if there isn’t a connection. 
* A **sparse graph** is when there are very few connections. **a dense graph** is when there are many connections
* Within an adjacency matrix, an undirected graph will always be **symmetric**. This is not the case for a directed graph. 
2. ***Adjacency List***
* An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.

###### Weighted Graphs
* A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights. 

### Traversals
1. ***Breadth First***
* Breadth first traversal is when you visit all the nodes that are closest to the root as possible. From there you traverse outwards, level by level, until you have visited all the vertices/nodes.
* Here is what the algorithm breadth first traversal looks like:
  - Enqueue the declared start node into the Queue.
  - Create a loop that will run while the node still has nodes present.
  - Dequeue the first node from the queue
  - if the Dequeue‘d node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.

2. ***Depth First***
* The algorithm for a depth first traversal is as follows:
  - Push the root node into the stack
  - Start a while loop while the stack is not empty
  - Peek at the top node in the stack
  - If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.
  - If the top node does not have any unvisited children, Pop that node off the stack
  - repeat until the stack is empty.

* ![image](https://miro.medium.com/max/3648/1*VM84VPcCQe0gSy44l9S5yA.jpeg)

###### Real World Uses of Graphs
* Here are just a few examples of graphs in use:
1. GPS and Mapping
2. Driving Directions
3. Social Networks
4. Airline Traffic
5. Netflix uses graphs for suggestions of products



