# Ex.No:2
# Ex.Name:
There are N cities numbered from 1 to N.
You are given connections, where each connections[i] = [city1, city2, cost] represents the cost to connect city1 and city2together.  (A connection is bidirectional: connecting city1 and city2 is the same as connecting city2 and city1.)
Return the minimum cost so that for every pair of cities, there exists a path of connections (possibly of length 1) that connects those two cities together. 
The cost is the sum of the connection costs used. 

## Date: 06/11/2025
## Aim:
To write a C++ program to find the minimum cost required to connect all N cities such that every city is reachable from every other city, using Minimum Spanning Tree (Kruskal’s Algorithm).

## Algorithm:
```
1. Start the program.
2. Read the number of cities N and number of connections M.
3. Store all connections as edges consisting of (city1, city2, cost).
4. Sort all edges in increasing order of their cost.
5. Use a Disjoint Set Union (DSU) structure to detect cycles.
6. For each edge in sorted order:

   * If the two cities belong to different sets, include the edge in MST and merge the sets.
   * Add the cost to total MST cost.
7. If all cities are connected, print the total MST cost.
8. Stop the program.
```





## Program:
```cpp
void addEdge (int x, int y, int w)
    {
        edgelist.push_back({w ,x , y });
    }
```


## Output:
<img width="496" height="416" alt="image" src="https://github.com/user-attachments/assets/dcf776cc-3f35-43a4-ab81-37e7b866bb4e" />



## Result:
The program successfully computes the minimum cost required to connect all cities using the edges of the Minimum Spanning Tree.

