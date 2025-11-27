# Ex.No:3
# Ex.Name: Write a CPP code to print shortest distances in the program to find Dijkstra's shortest path from A to all other vertices.
## Date: 06/11/2025
## Aim:
To write a C++ program to compute and print the shortest distance from source vertex A to all other vertices using Dijkstra’s Shortest Path Algorithm.

## Algorithm:
```
1. Start the program.
2. Read the number of vertices and edges.
3. Store the graph using an adjacency list where each entry contains (neighbor, weight).
4. Initialize a distance array with infinity for all vertices except the source A, which is set to 0.
5. Use a min-priority queue (min-heap) to process the vertex with the smallest known distance.
6. For each extracted vertex, relax all its adjacent edges:

   * If a shorter path is found, update the distance and push it to the priority queue.
7. Continue until all vertices are processed.
8. Print the shortest distances from A to all other vertices.
9. Stop the program.
```





## Program:
```cpp
cout<<"Vertex Distance from Source\n";
	for (int i = 0; i < V; ++i)
		cout<<char(i + 65)<<" "<<dist[i]<<"\n";
		}

```


## Output:
<img width="515" height="766" alt="image" src="https://github.com/user-attachments/assets/1782aaef-1b2e-44df-9d94-ddfd9ff24021" />



## Result:
The program successfully prints the shortest distances from vertex A to all other vertices in the graph using Dijkstra’s algorithm.

