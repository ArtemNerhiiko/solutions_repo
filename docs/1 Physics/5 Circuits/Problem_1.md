# Problem 1

## Describing the algorithm for calculating the equivalent resistance using graph theory


This method uses concepts from graph theory and linear algebra to compute the equivalent resistance between two nodes in a resistive electrical circuit.


## 1. Model the Circuit as a Graph

- **Nodes**: Represent junctions in the circuit.

- **Edges**: Represent resistors.

- **Edge Weights**: Use **conductance** $G = \frac{1}{R}$, the reciprocal of resistance.


## 2. Construct the Graph Laplacian Matrix

Let:

- $G$: the graph with $n$ nodes.

- $w_{ij}$: conductance of edge between nodes $i$ and $j$.

- $L \in \mathbb{R}^{n \times n}$: Laplacian matrix.



## 3. Compute Equivalent Resistance Using the Pseudoinverse

To find the **effective resistance** $R_{ab}$ between nodes $a$ and $b$:

$$
R_{ab} = (\mathbf{e}_a - \mathbf{e}_b)^T \cdot L^+ \cdot (\mathbf{e}_a - \mathbf{e}_b)
$$

Where:

- $L^+$: Moore–Penrose pseudoinverse of the Laplacian matrix.

- $\mathbf{e}_a$, $\mathbf{e}_b$: indicator vectors for nodes $a$ and $b$.



## 4. Alternative Method: Solve a Linear System

Instead of computing $L^+$, you can:

1. Inject 1A current into node $a$, extract 1A from node $b$.

2. Solve the system:

$$
L \cdot \mathbf{v} = \mathbf{i}
$$

Where:

- $\mathbf{i}$: current injection vector (1 at $a$, -1 at $b$, 0 elsewhere).

- $\mathbf{v}$: resulting voltage vector.

3. The equivalent resistance is:

$$
R_{ab} = v_a - v_b
$$




