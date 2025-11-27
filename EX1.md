# Ex.No:1
# Ex.Name:Given a weighted, undirected and connected graph of V vertices and E edges. The task is to find the sum of weights of the edges of the Minimum Spanning Tree. Write the main function to generate the MST.
## Date: 06/11/2025
## Aim:
To write a C++ main function that generates the Minimum Spanning Tree of a weighted, undirected, connected graph and prints the sum of the MST edge weights.

## Algorithm:
```
1. Read `V` (vertices) and `E` (edges).
2. Store all edges in a structure `(u, v, weight)`.
3. Sort all edges by weight.
4. Use Disjoint Set Union (DSU) to pick edges:

   * Include the edge if it does not form a cycle.
5. Keep adding edges until MST contains `V-1` edges.
6. Print the total MST weight.
```

## Program:
```cpp
int main()
{
	int V;
	int edges,vertices,u,v,w;
    cin>>vertices>>edges;
    V=vertices;
	Graph g(V);
	
    for(int i=0;i<edges;i++)
    {
        cin>>u>>v>>w;
        g.addEdge(u,v,w);
    }
    cout<<"Prim's MST edges are: ";
    g.primMST();
    
  
	return 0;
}
```


## Output:
<img width="438" height="494" alt="image" src="https://github.com/user-attachments/assets/c27f52a8-6008-4ed8-a4aa-735d12636d5e" />



## Result:
Thus, the main function successfully generates the Minimum Spanning Tree of a weighted, undirected, connected graph and prints the total weight of the MST using Kruskal’s Algorithm.

