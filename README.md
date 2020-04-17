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
- To change the number of nodes, cahnge the range of **vertices**. ***(Eg: vertices=random.randrange(50,60); for 50-60 nodes)***

***To rum it in .py, donwload directly from Google Colaba or run the hamiltonian.py in this repository.***

----

### Solution
The solution was implemented in **Python** using the Google Colab **GPU**. 

#### Sample Output:
The following output is a simple example for 5 nodes with created with at least one hamiltonian path. 
![Alt text](hamiltoniam/photos/sample_output.png?raw=true "Samlpe Graph")

#### Libraries used:
- NetwrokX
- Matplotlib, Pyplot 

#### Algorithm:
The idea behind my solution is to use a simple Depth First Search (**DFS**) and recursion. 

#### Time Complexity:


----

#### Drawbacks

#### Errors
    What tools, language, and libraries did you use to implement your solution? Why did you pick them?
    What is the (Big O) time complexity of your solution? Are there more efficient ways to implement a solution? Why did you choose the algorithm that you did?
    How did you handle errors? What are the cases where your code does not work?
