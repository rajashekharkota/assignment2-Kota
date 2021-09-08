# assignment2-Kota
# Rajashekhar kota
###### Agra-India
Agra is famous for ***Taj mahal*** which is located in delhi.Delhi is famous for ***roadside food***.
_____

## Directions
---
1. Book your flight tickets to your  destination.
   1. Pack your luggages.
   2. Book a cab from your present location to nearest airport
   3. Reach airport in time.
   4. Checkin.

List of iteams:
* Cloths.
* Money.
  * currency of your destination country.
* Electronic gadgets.

**[AboutMe](AboutMe.md)**
____
## Food and Drinks
----
This table shows food and drinks available at different places.

|Food|Location|Cost|
|---|---|---| 
|Chicken Biryani|Bawarchi biryani center|$30|
|Pizza|Domino's|$6|
|Coke|Student union canteen|$1|
|Burger|Burger King|$2|
----
## Pithy Quotes
---
> I may not be happy all the times,
But, I smile to make somepeople to be happy.
- *Rajashekhar Kota*
> The purpose of our live is to be happy.
- *Dalai lama*

## Code Fencing
----
   int n;  
   vector<vector<int>> adj; // adjacency matrix of graph  
   const int INF = 1000000000; // weight INF means  there is no edge   

   struct Edge {  
      int w = INF, to = -1;  
   };  

   void prim() {  
      int total_weight = 0;  
      vector<bool> selected(n, false);  
      vector<Edge> min_e(n);  
      min_e[0].w = 0;  

      for (int i=0; i<n; ++i) {  
         int v = -1;  
         for (int j = 0; j < n; ++j) {  
               if (!selected[j] && (v == -1 || min_e[j].w < min_e[v].w))  
                  v = j;  
         }  

         if (min_e[v].w == INF) {  
               cout << "No MST!" << endl;  
               exit(0);  
         }  

         selected[v] = true;  
         total_weight += min_e[v].w;  
         if (min_e[v].to != -1)  
               cout << v << " " << min_e[v].to << endl;  

         for (int to = 0; to < n; ++to) {  
               if (adj[v][to] < min_e[to].w)  
                  min_e[to] = {adj[v][to], v};  
         }  
      }  

      cout << total_weight << endl;  
   }  
   
> In computer science, Prim's algorithm (also known as Jarník's algorithm) is a greedy algorithm that finds a minimum spanning tree for a weighted undirected graph. This means it finds a subset of the edges that forms a tree that includes every vertex, where the total weight of all the edges in the tree is minimized. The algorithm operates by building this tree one vertex at a time, from an arbitrary starting vertex, at each step adding the cheapest possible connection from the tree to another vertex.

[Graphs Spanning- prim's algorithm.](https://en.wikipedia.org/wiki/Prim%27s_algorithm)

  var m := map(0 → 0, 1 → 1)  
  function fib(n)  
      if key n is not in map m  
          m[n] := fib(n − 1) + fib(n − 2)  
      return m[n]

[code source](https://en.wikipedia.org/wiki/Parallel_algorithms_for_minimum_spanning_trees)

