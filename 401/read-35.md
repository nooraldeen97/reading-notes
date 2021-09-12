# Graph

A Graph is a non-linear data structure consisting of nodes and edges. The nodes are sometimes also referred to <br>as vertices and the edges are lines or arcs that connect any two nodes in the graph. <br>

its consist of the following : <br>
<br>
Vertex  also called a “node”<br>
Edge -lines or arcs that connect any two nodes in the graph<br>
Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.<br>
Degree - The degree of a vertex is the number of edges connected to that vertex.<br>
There are two types of graphs :<br>

1-Undirected Graphs : is a graph where each edge is undirected , it doesn't has a direction's .<br>

2-Directed Graphs :  is a graph where every edge is directed.<br>

3- Complete Graphs :  A complete graph is when all nodes are connected to all other nodes.<br>

4-Connected Graphs : A connected graph is graph that has all of vertices/nodes have at least one edge.<br>

5-Disconnected Graphs : A disconnected graph is a graph where some vertices may not have edges.<br>

Adjacency Matrix : is represented through a 2-dimensional array, If there are n vertices, then we are looking <br>at an n x n Boolean matrix.
Adjacency List : is a collection of linked lists or array that lists all of the other vertices that are <br>connected.<br>
Weighted Graphs A weighted graph is a graph with numbers assigned to its edges. These numbers are called <br>weights. <br>

Traversals:<br>
The traversals itself are like those of trees. <br>
1- Breadth first<br>

Here is what the algorithm breadth first traversal looks like:<br>

Enqueue the declared start node into the Queue.<br>
Create a loop that will run while the node still has nodes present.<br>
Dequeue the first node from the queue<br>
if the Dequeue‘d node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.<br>
 
2- Depth first <br>

Push the root node into the stack<br>
Start a while loop while the stack is not empty<br>
Peek at the top node in the stack<br>
If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back <br>into the stack.<br>
If the top node does not have any unvisited children, Pop that node off the stack<br>
repeat until the stack is empty.<br>
 

Graphs are extremely popular when it comes to it’s uses. Here are just a few examples of graphs in use:<br>

GPS and Mapping<br>
Driving Directions<br>
Social Networks<br>
Airline Traffic<br>
Netflix uses graphs for suggestions of products<br>