# Ex.No:4

# Ex.Name: Write a CPP function to find the bipartite of a graph which is given by user.

## Date: 06/11/2025

## Aim:
To write a C++ function to check whether a user-given graph is bipartite using BFS and coloring technique.

## Algorithm:
```
1. Start the program.
2. Read the number of vertices and edges.
3. Create an adjacency list to represent the graph.
4. Initialize a color array with -1 for all vertices.
5. For every unvisited vertex:

   * Assign color 0 and start BFS.
   * For every adjacent vertex:

     * If it is uncolored, assign the opposite color.
     * If it has the same color, the graph is not bipartite.
6. If BFS completes without conflict, the graph is bipartite.
7. Stop the program.
```
## Program:
```cpp
bool isBipartite(int V, vector<int> adj[])
{
    vector<int> col(V, -1);
 
    queue<pair<int, int> > q;
   
    for (int i = 0; i < V; i++)
    {
        if (col[i] == -1)
        {
            q.push({ i, 0 });
            col[i] = 0;
            while (!q.empty()) 
            {
                pair<int, int> p = q.front();
                q.pop();
            
                int v = p.first;
                int c = p.second;
                 
                for (int j : adj[v])
                {
                   
                    if (col[j] == c)
                        return 0;
                   
                    if (col[j] == -1)
                    {
                        col[j] = (c) ? 0 : 1;
                        q.push({ j, col[j] });
                    }
                }
            }
        }
    }
    return 1;
}
```



## Output:
<img width="499" height="789" alt="image" src="https://github.com/user-attachments/assets/7a66f655-7b30-4e11-ab97-3f114b2fc7fb" />



 ## Result:
The program correctly checks whether the user-given graph is bipartite by using BFS with alternate coloring.

