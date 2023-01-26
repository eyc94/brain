# :heavy_check_mark: Graph

![Image of a graph](../../../images/data-structures/non-linear/graph/graph.png)

## :round_pushpin: Summary
- Non-linear data structure.
- Consists of vertices (or nodes) and edges.
- Edges connect pairs of nodes.
  - Edges are ordered pairs of vertices `(u, v)`.
  - Ordered because `(u, v)` and `(v, u)` are different in directed graphs (di-graph).
  - Edges may have weight, value, or cost.
- A `directed, acyclic graph (DAG)`, is a directed graph with no cycles.
- Hierarchical.
- Arranged in a tree-like strcture.
- Top-most node is called the `root` node.

## :round_pushpin: Characteristics
- Max distance from a vertex to all other vertices is the `Eccentricity` of that vertex.
- Vertex with minimum eccentricity is considered the central point of the graph.
- The minimum value of `Eccentricity` is considered the radius of a connected graph.

## :round_pushpin: Representations
### Adjacency Matrix
![Image of an adjacency matrix](../../../images/data-structures/non-linear/graph/adjacency-matrix.png)
- 2D array of size `V x V`, where `V` is the number of vertices in the graph.
- If the 2D array is `arr[][]`, `arr[i][j]` means that there is an edge from vertex `i` to vertex `j`.
- Undirected graph matrix is always symmetric.
- Can be used for weighted graphs: `arr[i][j] = w`, meaning edge from `i` to `j` with weight `w`.
- Advantages:
  - Easy to follow.
  - Removing edges is `O(1)`.
  - Queries for finding an edge is `O(1)`.
- Disadvantages:
  - Consumes more space `O(V^2)`.
  - Adding a vertex is `O(V^2)` time.
  - Computing neighbors of a vertex is `O(V)` time.

### Adjacency List
![Image of an adjacency list](../../../images/data-structures/non-linear/graph/adjacency-list.png)
- Array of lists.
- Size of array is number of vertices.
- Let the array be `arr[]`.
- Entry `arr[i]` represents the list of vertices adjacent to the `i`th vertex.
  - Can be used to represent a weighted graph.
  - Weights of edges can be represented as a list of pairs.
- Advantages:
  - Saves space: `O(|V| + |E|)`.
  - Adding vertex is easier.
  - Computing all neighbors of a vertex is optimal.
- Disadvantages:
  - Determining if an edge exists is not efficient: `O(V)` time.
  - In real-life, graphs are sparse `|E| << |V|^2`.
    - Commonly used for storing graphs.
    - Matrix will enforce `|V|^2` bound on time complexity.

## :round_pushpin: Traversals
Similar to tree BFS and DFS approaches but graphs may contain cycles.
- To keep track of this, use an array to keep track of visited nodes.
### Depth-First Search (DFS)
- Uses stack.
- Start at the root.
- Explore as far as possible before backtracking.
- Time: `O(V + E)` where `V` is the number of vertices and `E` is the number of edges.
- Space: `O(V)` because of the visited array.
- Note: Watch for disconnected graphs (edge case).
- Applications:
  - Cycle detection.
  - Path finding.
  - Topological Sorting.
  - Checking if graph is bipartite.
  - Finding strongly connected components of a graph.
  - Solving puzzles with one solution (e.g. a maze).

### Breadth-First Search (BFS)
- Uses queue.
- Start at the root.
- Explore neighbors before going as far down.
- Time: `O(V + E)` where `V` is the number of vertices and `E` is the number of edges.
- Space: `O(V)` because of the visited array.
- Note: Watch for disconnected graphs (edge case).
- Applications:
  - Shortest path and minimum spanning tree for unweighted graph.
  - Peer-to-peer networks.
  - Crawlers in search engines.
  - Social Networking Websites.
  - GPS Navigation Systems.
  - Broadcasting in network.
  - Garbage collection.
  - Cycle detection in undirected graph.
  - Ford-Fulkerson algorithm.
  - Test if a graph is bipartite.
  - Path finding.
  - Finding all nodes withing on connected component.
