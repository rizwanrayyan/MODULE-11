# Ex.No:5

# Ex.Name:A traveller needs to visit all cities from a list, where distances between all cities are known and visited once. What is the shortest possible routes that he visits each city exactly once and returns to the origin city?. Find the TSP solution using CPP function.

## Date: 06/11/2025

## Aim:
To write a C++ program to find the shortest possible route for the Travelling Salesman Problem (TSP), where a traveller must visit every city exactly once and return to the origin city, using Brute Force (Permutation Method).

## Algorithm:
```
1. Start the program.
2. Read the number of cities **N**.
3. Read the **distance matrix** of size N × N.
4. Create a list of cities excluding the starting city (0).
5. Generate all possible permutations of these cities.
6. For each permutation:

   * Compute the total path cost starting at city 0, visiting each city in order, and returning to 0.
   * Update the minimum route cost.
7. Print the shortest route cost.
8. Stop.
```





## Program:
```cpp
int TSP(int p)  
{
    vector<int> ver; 
    for(int i = 0; i <V; i++)
    {
        
        if(i!=p)
        ver.push_back(i);
    }
    int m_p = INT_MAX; 
    do
    {
        int cur_pth = 0;
        int k = p;
        for(int i=0;i<(int)ver.size();i++)
        {
            cur_pth += adjMatrix[k][ver[i]];
            k = ver[i];
        }
        cur_pth += adjMatrix[k][p];
        m_p = min(m_p, cur_pth);
   }
   while (next_permutation(ver.begin(), ver.end()));
   return m_p;
}
```



## Output:
<img width="601" height="850" alt="image" src="https://github.com/user-attachments/assets/7cb89a17-592d-47ec-86b0-55e9c213e96a" />



## Result:
The program successfully computes the minimum cost to visit every city exactly once and return to the origin city using the Travelling Salesman Problem (TSP) algorithm.

