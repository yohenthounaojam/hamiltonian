# hamiltonian 
This is a Hamiltonian path finder implementation. 

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

### Solution
The solution was implemented in **Python** using the Google Colab **GPU**. 

#### Sample Output:
The following output is a simple example for 5 nodes with created with at least one hamiltonian path. 
![](photos/sample_output.png?raw=true "Samlpe Graph")

Using the implementation explained below we get the result shown below:
![](photos/Output.png?raw=true "Samlpe Graph")


#### Libraries used:
- NetwrokX
- Matplotlib, Pyplot 

#### Algorithm:
The idea behind my solution is to use a simple Depth First Search (**DFS**) and recursion. 
_This is not the most optimal solution. 

We start a depth first search traversal from **x** and do the following at each vertex:
1. Store each visited node in an array called **path**. 
2. Mark the node as True (for visited) in a **visited** array; where the index of the node corresponds to the node. This will prevent any cycles from occuring. 

When we reach the node **y**, we print the whole path array if it meets the following important **condition**:
- The len(path) is equal to the number of nodes; meaning all nodes have been visited. 

#### Optimizing the above
The fllowing are logical assumptions we can make to optimize the algorithm above. 

We know for sure that the graph will not have a Hamiltonian Path if any node other than x,y 


#### Time Complexity:


----

#### Drawbacks

#### Errors
    What tools, language, and libraries did you use to implement your solution? Why did you pick them?
    What is the (Big O) time complexity of your solution? Are there more efficient ways to implement a solution? Why did you choose the algorithm that you did?
    How did you handle errors? What are the cases where your code does not work?
