# Graph

Graphs are a type of data structure made up of vertices (or nodes) connected by edges. Here are some key terms and concepts related to graphs:

#### Vertex (Node): A data point that can have zero or more connections to other vertices.

#### Edge: A link or connection between two vertices.

#### Neighbor: Vertices connected by an edge are called neighbors.

#### Degree: The number of edges connected to a vertex.

### Directed vs. Undirected:

Undirected Graph: In this type of graph, edges have no direction; they simply connect two vertices.

Directed Graph (Digraph): In a directed graph, each edge has a direction, pointing from one vertex to another.

### Complete vs. Connected vs. Disconnected:

Complete Graph: Every vertex is connected to every other vertex.

Connected Graph: All vertices have at least one edge.

Disconnected Graph: Some vertices may not have edges.

### Acyclic vs. Cyclic:

Acyclic Graph: A directed graph without cycles (cycles are paths that loop back to the starting vertex).

Cyclic Graph: A graph that contains cycles.

### Adjacency Matrix and List:

Adjacency Matrix: A 2D array where each row and column represent vertices. The value in each cell indicates whether there's an edge between the corresponding vertices.

Adjacency List: A collection of linked lists or arrays that lists the neighbors of each vertex.

### Weighted Graphs:

Weighted Graph: Edges have numerical values assigned to them, called weights.
Graph Traversals:

Breadth-First Traversal: Starting at a specific vertex, visit all its neighbors before moving to their neighbors. Be cautious with cyclic graphs to avoid infinite loops.

Depth-First Traversal: Use a stack to explore as deeply as possible along each branch before backtracking.

### Real-World Uses:

Graphs find applications in various real-world scenarios, such as:

GPS and Mapping: Finding routes and directions.

Social Networks: Representing relationships between users.

Airline Traffic: Modeling flight connections.

Netflix Recommendations: Suggesting content based on user preferences.

Graphs are a versatile data structure used in many domains to solve complex problems efficiently.