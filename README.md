# hamiltonian 
This is a Hamiltonian path finder implementation for a non directed graph. 

----

### Deliverables: 
- [x] Represent a random graph with n vertices of at least degree one (n is at least 100).
- [x] Randomly select two vertices **(x,y)** from the graph.
- [x] Find all of the possible hamiltonian paths in the graph.

----
### How to run the solution.

To run the Colab Notebook:
- Open the Notebok using Google Colab
- Under Runtime, **Run All**
- To change the number of nodes, cahnge the range of **vertices**. _(Eg: vertices=random.randrange(50,60); for 50-60 nodes)_

_To rum it as .py, donwload directly from Google Colaba or run the hamiltonian.py in this repository._

----

## Solution
The solution was implemented in **Python** using the Google Colab **GPU**. 

#### Sample Output:
The following output is a simple example for 5 nodes with created with at least one hamiltonian path. 
![](photos/sample_output.png?raw=true "Samlpe Graph")

Using the implementation explained below we get the result shown below:
![](photos/Output.png?raw=true "Samlpe Graph")

#### Libraries used:
- NetwrokX
- Matplotlib, Pyplot

----

#### Algorithm:
The idea behind my solution is to use a simple Depth First Search (**DFS**) and recursion. 
_This is not the most optimal solution. 

We start a depth first search traversal from **x** and do the following at each vertex:
1. Store each visited node in an array called **path**. 
2. Mark the node as True (for visited) in a **visited** array; where the index of the node corresponds to the node. This will prevent any cycles from occuring. 

When we reach the node **y**, we print the whole path array if it meets the following important **condition**:
- The len(path) is equal to the number of nodes; meaning all nodes have been visited. 

----

#### Optimizing the above
The fllowing are logical assumptions we can make to optimize the algorithm above. 

- **Lemma 1**: The graph will not have a Hamiltonian Path if any node other than x,y has only one adjacent node.
  - Using this, we can end the algorithm if the above is encoutered. 

----

#### Time Complexity:

The Big O time complexity for the above algorithm is:
**O(n!)**; where n is the number of nodes. 

Although there are better solutions like the famous Help Karp Algorithm with O(n<sup>2</sup>2<sup>n</sup>)(see below), for our case of a 100 nodes, this slution will be better for the worst case. 

*However, as n increase to thousands, it will be less optimal.*

----

#### Drawbacks

- **Time Complexity:** execution time increases as number of nodes increases.
- **Recursion:** May lead to Stack Overflow.
- **Space Complexity:** The algorithm forms a new array(named path) every time the destination is reached. *May be handled by garbage collector.*

#### Handling issues and errors during implementation
- Many a times, I recieved a *Maximum Recursion Depth* Exeeded error.
  - First, I was convinced my algorithm was extremely bad in terms of time complexity. However, there was simple but of not returning the recursive call. 

----

### More Optimal Solutions 

#### For graphs with maximum degree of 3
- Time Complexity: O(1.251<sup>n</sup>)
- More Details: [Kyoto University Research]: https://link.springer.com/chapter/10.1007%2F978-3-540-73545-8_13

#### Bellman, Held, and Karp Algorithm
- Time Complexity: O(n<sup>2</sup>2<sup>n</sup>)
- Algorithm: In short, it uses Dynamic Programming to check for paths in subgraphs and saving the state for each subgrah. 
- More details: [Hamiltonian Path Algorithm]: https://en.wikipedia.org/wiki/Held%E2%80%93Karp_algorithm
