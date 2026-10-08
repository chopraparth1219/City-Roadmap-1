# City-Roadmap-1
# MAT2002 | Graph Theory Toolkit for a City Road Network

An interactive web-based toolkit demonstrating fundamental graph theory algorithms and discrete mathematics concepts applied to a shared city road network[cite: 1, 2].

The application allows users to explore the original 8-city road network from the project report, test routing and spanning tree algorithms, analyze structural properties, or dynamically construct custom graphs directly on an interactive canvas[cite: 2, 4].

---

## Features

### 1. Interactive Graph Visualizer & Builder
* **Move / Inspect**: Drag cities to adjust network layout; click any city or edge to view connection details and local vertex degrees[cite: 3].
* **Add City**: Place new vertices anywhere on the blank canvas.
* **Add Road**: Connect any two cities and specify edge weights (distance in km)[cite: 2].
* **Delete Item**: Remove specific vertices or edges dynamically.
* **Reset**: Quickly restore the baseline 8-city, 12-road benchmark network[cite: 2].

### 2. Core Graph Algorithms Implemented
* **Dijkstra's Algorithm (Shortest Path)**: Computes shortest routing between any two selectable cities, displaying the step-by-step priority queue finalization order, total distance, and path highlights[cite: 3, 5, 6].
* **Minimum Spanning Tree (MST)**:
  * **Kruskal's Algorithm**: Greedy edge selection with cycle detection via disjoint sets[cite: 3, 6].
  * **Prim's Algorithm**: Priority queue expansion starting from a designated vertex[cite: 3, 6].
* **Matrix Representations**:
  * Unweighted Adjacency Matrix ($0/1$)[cite: 3, 5]
  * Weighted Adjacency Matrix (distances in km)[cite: 3, 5]
  * Incidence Matrix ($\vert{}V\vert{} \times \vert{}E\vert{}$)[cite: 3, 5]
* **Structural Graph Analysis**:
  * **Degrees & Handshaking Lemma**: Calculates degree sequences and verifies $\sum \text{deg}(v) = 2\vert{}E\vert{}$[cite: 3, 5].
  * **Connectedness**: BFS-based connected component count[cite: 3, 5].
  * **Euler Trail / Circuit**: Odd-degree vertex analysis based on Euler's theorem[cite: 3, 7].
  * **Hamiltonian Cycle**: Backtracking search for a closed tour visiting every vertex exactly once[cite: 3, 8].
  * **Bipartite Test**: BFS 2-coloring test checking for odd-length cycles[cite: 3, 8].

---

## Baseline Road Network

The benchmark dataset consists of 8 vertices (cities) and 12 undirected weighted edges (distances in km)[cite: 2]:

| Edge | City 1 | City 2 | Distance (km) |
| :--- | :--- | :--- | :--- |
| e1 | Delhi | Jaipur | 280 |
| e2 | Delhi | Agra | 230 |
| e3 | Delhi | Lucknow | 550 |
| e4 | Jaipur | Agra | 240 |
| e5 | Jaipur | Indore | 560 |
| e6 | Agra | Kanpur | 280 |
| e7 | Lucknow | Kanpur | 90 |
| e8 | Agra | Bhopal | 600 |
| e9 | Kanpur | Bhopal | 650 |
| e10 | Bhopal | Indore | 190 |
| e11 | Bhopal | Nagpur | 350 |
| e12 | Indore | Nagpur | 440 |

*(Source: MAT2002 Project Benchmark Data)*[cite: 1, 2]

---

## Project Structure

```text
├── index.html        # Complete standalone web application (UI, SVG visualizer, algorithms)
└── README.md         # Project documentation
