# Maximum Bipartite Matching using Hungarian Method & Edmonds-Karp Algorithm

This project implements and compares two classic algorithms for solving the **Maximum Bipartite Matching** problem:
- **Hungarian Method**
- **Edmonds-Karp Algorithm** (with both BFS and DFS variants)

---

## Project Overview

In graph theory, a **bipartite graph** is a graph whose vertices can be divided into two disjoint sets \( V_0 \) and \( V_1 \) such that every edge connects a vertex in \( V_0 \) to one in \( V_1 \).

The **Maximum Bipartite Matching** problem aims to find the largest possible set of edges such that no two edges share a vertex — i.e., to match as many pairs as possible without overlap.

This project models real-world pairing problems (like applicants and job positions) and compares the efficiency of two algorithmic approaches.

---

## Algorithm Summary

### 1. Hungarian Method

- Core idea: **Augmenting path**.
- Efficiently finds maximum matchings by alternating between matched and unmatched edges.
- Based on the work of Kuhn, König, and Egerváry.

### 2. Edmonds-Karp Algorithm

- Transforms the matching problem into a **maximum flow** problem.
- Adds a **source** and **sink** to the bipartite graph and treats all edges with capacity = 1.
- Uses:
  - **BFS** for shortest augmenting paths.
  - **DFS** for deep path exploration.

---

## How to Run

### Compilation (Windows)

Use a C++ compiler such as g++:

```bash
g++ Source.cpp -o matcher.exe
````

### Input Format (input.txt)

```
4
4
1 1
1 3
2 1
3 3
4 1
4 2
4 3
-1 -1
```

* Line 1: Number of vertices in set V0 (e.g., men)
* Line 2: Number of vertices in set V1 (e.g., women)
* Line 3+: List of matching edges, end with `-1 -1`

### Execution

Run the program and choose a method:

```
Select the algorithm for solving Bipartite Matching:
1. Hungarian Method
2. Edmonds-Karp (BFS)
3. Edmonds-Karp (DFS)
4. Exit
```

The program will compute and print:

* Maximum matching count
* Execution time (in milliseconds)

---

## Benchmark Results (100 random test cases)

| Algorithm          | Average Time (ms) |
| ------------------ | ----------------- |
| Hungarian Method   | **0.75 ms**       |
| Edmonds-Karp (DFS) | 2.01 ms           |
| Edmonds-Karp (BFS) | 2.40 ms           |

**Conclusion:** The Hungarian Method consistently achieved the best performance across randomly generated test cases.

---

## Authors

| Name          | Student ID |
| ------------- | ---------- |
| Charlie Lai   | 1083301    |
| Yu-Yueh Chang | 1081542    |

> Supervisor: Professor Ching-Lueh Chang
> Institution: Department of Computer Science and Engineering, Yuan Ze University
