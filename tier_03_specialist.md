# Tier 3: Specialist (CF Rating 1400 – 1599)

> **Goal**: Transition from "knowing how to code" to "knowing what to code." Binary search on answer, intro graphs, and intro DP are the pillars.

At this tier you internalize the core algorithmic toolkit that separates casual coders from competitive programmers. You master dynamic programming in its foundational forms, learn divide-and-conquer, exploit bit manipulation for compact state representation, use hashing for fast equality checks, and manage disjoint sets for connectivity queries. By the end of Tier 3 you will consistently solve Div. 2 C problems and occasionally reach D.

---

## 3.1 Binary Search on Answer & Parametric Search [P1]

**Topics**: Binary searching on the answer value instead of an index, "minimize the maximum" / "maximize the minimum" patterns, continuous binary search, ternary search on unimodal functions.

**Patterns**:
- **"Find the minimum X such that something is possible"** → Binary search on X, check feasibility.
- The `check(mid)` function is the core — if `check` is monotonic (once true, always true), BS works.
- Ternary search: used for unimodal functions (one peak/valley). Divide into thirds, remove the side that's worse.

**Classical Questions**: Allocating books to students (minimize max pages), minimum time for machines to produce items.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Factory Machines](https://cses.fi/problemset/task/1620) | CSES 1620 | BS on answer template |
| 2 | ★ [Array Division](https://cses.fi/problemset/task/1085) | CSES 1085 | BS on answer |
| 3 | ★ [Split Array Largest Sum](https://leetcode.com/problems/split-array-largest-sum/) | LC 410 | BS on answer |
| 4 | [Magic Powder](https://codeforces.com/problemset/problem/670/D1) | CF 670D1 | BS on answer |
| 5 | [Aggressive Cows](https://www.spoj.com/problems/AGGRCOW/) | SPOJ | BS on answer classic |
| 6 | [Capacity to Ship Packages](https://leetcode.com/problems/capacity-to-ship-packages-within-d-days/) | LC 1011 | BS on answer |
| 7 | [Minimum Number of Days to Make m Bouquets](https://leetcode.com/problems/minimum-number-of-days-to-make-m-bouquets/) | LC 1482 | BS on answer |
| 8 | [Magnetic Force Between Balls](https://leetcode.com/problems/magnetic-force-between-two-balls/) | LC 1552 | Maximize minimum |
| 9 | [Convention](https://usaco.org/index.php?page=viewproblem2&cpid=858) | USACO Silver | BS on answer |
| 10 | [Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/) | LC 4 | BS advanced |
| 11 | [Find Peak Element](https://leetcode.com/problems/find-peak-element/) | LC 162 | Ternary / BS |
| 12 | [EKO - Eko](https://www.spoj.com/problems/EKO/) | SPOJ EKO | BS on answer |
| 13 | [Digit Queries](https://cses.fi/problemset/task/1628) | CSES 1628 | BS on intervals |

---

## 3.2 Sorting Algorithms & Custom Comparators [P1]

**Topics**: Merge sort, counting inversions, custom comparators, sorting by multiple keys, event sorting, coordinate compression via sorting.

**Patterns**:
- **Inversions** = number of pairs (i,j) with i < j but a[i] > a[j]. Count via modified merge sort in O(N log N).
- Sort events by end time for scheduling, by start time for sweep.
- Custom comparators: `sort(a, a+n, [](int x, int y){ return x > y; })` for descending.

**Classical Questions**: Count inversions, sort intervals by end time, sort strings by length then lexicographically.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Inversion Count](https://www.spoj.com/problems/INVCNT/) | SPOJ INVCNT | Merge sort |
| 2 | [Sort an Array](https://leetcode.com/problems/sort-an-array/) | LC 912 | Implement merge sort |
| 3 | [Merge Intervals](https://leetcode.com/problems/merge-intervals/) | LC 56 | Sort by start |
| 4 | [Non-overlapping Intervals](https://leetcode.com/problems/non-overlapping-intervals/) | LC 435 | Sort by end (greedy) |
| 5 | [Restaurant Customers](https://cses.fi/problemset/task/1619) | CSES 1619 | Event sorting |
| 6 | [Room Allocation](https://cses.fi/problemset/task/1164) | CSES 1164 | Event sorting + multiset |
| 7 | [Movie Festival](https://cses.fi/problemset/task/1629) | CSES 1629 | Activity selection |
| 8 | [Tasks and Deadlines](https://cses.fi/problemset/task/1630) | CSES 1630 | Sort by duration |
| 9 | [Queue at the School](https://codeforces.com/problemset/problem/266/B) | CF 266B | Bubble sort simulation |
| 10 | [Largest Number](https://leetcode.com/problems/largest-number/) | LC 179 | Custom comparator |
| 11 | [H-Index](https://leetcode.com/problems/h-index/) | LC 274 | Sort + count |

---

## 3.3 Intro to Trees & Graphs: DFS & Flood Fill [P1]

**Topics**: Graph representation, adjacency list, basic DFS traversal, connected components, flood fill on grids.

**Patterns**:
- **DFS**: go deep, backtrack. Perfect for painting areas on a matrix (flood fill) or exploring all reachable nodes in a graph.
- Grid as graph: each cell (r,c) is a node, edges go to 4/8 neighbors.
- Connected Components: running DFS from unvisited nodes tells you how many separate pieces the graph has.

**Classical Questions**: Flood fill on a grid, counting connected components.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | [Flood Fill](https://leetcode.com/problems/flood-fill/) | LC 733 | Simplest DFS / grid intro |
| 2 | ★ [Number of Islands](https://leetcode.com/problems/number-of-islands/) | LC 200 | Classic flood fill |
| 3 | [Max Area of Island](https://leetcode.com/problems/max-area-of-island/) | LC 695 | Flood fill count |
| 4 | [Counting Rooms](https://cses.fi/problemset/task/1192) | CSES 1192 | Grid connected components |
| 5 | ★ [Building Roads](https://cses.fi/problemset/task/1666) | CSES 1666 | Graph connected components |
| 6 | [Icy Perimeter](https://usaco.org/index.php?page=viewproblem2&cpid=895) | USACO Silver | Grid DFS area/perimeter |
| 7 | [Clone Graph](https://leetcode.com/problems/clone-graph/) | LC 133 | Hash map + DFS |

---

## 3.4 Intermediate Graph Traversal: BFS & Applications [P1]

**Topics**: Queue-based BFS, shortest paths in unweighted graphs, multi-source BFS, cycle detection, bipartite checking.

**Patterns**:
- **BFS**: level-order traversal using a queue. Guarantees the shortest path in unweighted graphs.
- **Bipartite check**: 2-color via BFS. If coloring fails → odd cycle → not bipartite.
- **Path Reconstruction**: track a `parent` array while running BFS to trace backward from destination to start.

**Classical Questions**: Shortest path in a maze, multi-source spreading infection, 2-coloring.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Labyrinth](https://cses.fi/problemset/task/1193) | CSES 1193 | Unweighted shortest path |
| 2 | [Message Route](https://cses.fi/problemset/task/1667) | CSES 1667 | BFS path reconstruction |
| 3 | [Rotting Oranges](https://leetcode.com/problems/rotting-oranges/) | LC 994 | Multi-source BFS |
| 4 | [01 Matrix](https://leetcode.com/problems/01-matrix/) | LC 542 | Multi-source BFS distances |
| 5 | ★ [Is Graph Bipartite?](https://leetcode.com/problems/is-graph-bipartite/) | LC 785 | 2-coloring |
| 6 | [Building Teams](https://cses.fi/problemset/task/1668) | CSES 1668 | Graph bipartite check |
| 7 | [Course Schedule](https://leetcode.com/problems/course-schedule/) | LC 207 | Cycle detection (DAG) |
| 8 | [Round Trip](https://cses.fi/problemset/task/1669) | CSES 1669 | Undirected cycle detection |
| 9 | [Closing the Farm](https://usaco.org/index.php?page=viewproblem2&cpid=646) | USACO Silver | Connectivity tracking |

---

## 3.5 Intro to Dynamic Programming [P1]

**Topics**: 1D DP (Fibonacci-style recurrences, coin change), memoization vs tabulation, state definition, identifying overlapping subproblems.

**Patterns**:
- **State definition**: What information do I need to uniquely describe a subproblem? Usually the index and some capacity/budget.
- **Transition**: How do I build the answer for state `(i)` from smaller states?
- **Base case**: What's the answer for the smallest subproblem?
- Start by writing the recursive solution, then add memoization → then convert to bottom-up if needed.

**Classical Questions**: Fibonacci, climbing stairs, coin change (min coins, number of ways), house robber.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | [Climbing Stairs](https://leetcode.com/problems/climbing-stairs/) | LC 70 | Fibonacci DP |
| 2 | [Min Cost Climbing Stairs](https://leetcode.com/problems/min-cost-climbing-stairs/) | LC 746 | 1D DP with cost |
| 3 | ★ [Frog 1](https://atcoder.jp/contests/dp/tasks/dp_a) | AtCoder DP A | Safest 1D intro |
| 4 | ★ [Frog 2](https://atcoder.jp/contests/dp/tasks/dp_b) | AtCoder DP B | 1D with inner loop |
| 5 | [House Robber](https://leetcode.com/problems/house-robber/) | LC 198 | 1D DP classic |
| 6 | [House Robber II](https://leetcode.com/problems/house-robber-ii/) | LC 213 | Circular variant |
| 7 | [Removing Digits](https://cses.fi/problemset/task/1637) | CSES 1637 | DP / greedy bridge |
| 8 | ★ [Dice Combinations](https://cses.fi/problemset/task/1633) | CSES 1633 | 1D DP template |
| 9 | ★ [Minimizing Coins](https://cses.fi/problemset/task/1634) | CSES 1634 | Coin change (min) |
| 10 | ★ [Coin Combinations I](https://cses.fi/problemset/task/1635) | CSES 1635 | Coin change (ways) |
| 11 | ★ [Coin Combinations II](https://cses.fi/problemset/task/1636) | CSES 1636 | Ordered Unbounded |
| 12 | [Decode Ways](https://leetcode.com/problems/decode-ways/) | LC 91 | 1D DP |
| 13 | [Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/) | LC 300 | LIS classic |
| 14 | [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/) | LC 53 | Kadane's DP |
| 15 | [Fence Painting](https://usaco.org/index.php?page=viewproblem2&cpid=1173) | USACO Silver | DP |
| 16 | [Alphacode](https://www.spoj.com/problems/ACODE/) | SPOJ ACODE | Decode DP |

---

## 3.6 Greedy Algorithms (Intermediate) [P2]

**Topics**: Activity selection, fractional knapsack, Huffman coding intuition, exchange argument, scheduling problems, greedy ordering proofs.

**Patterns**:
- **Exchange argument**: Prove greedy is optimal by showing that swapping any two elements in the greedy order doesn't improve the answer.
- **Sort by deadline** for scheduling, **sort by ratio** for fractional problems.
- "Minimize the number of intervals to cover all points" → greedy by earliest end.

**Classical Questions**: Activity selection (max non-overlapping intervals), job scheduling with deadlines and profits.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Movie Festival](https://cses.fi/problemset/task/1629) | CSES 1629 | Activity selection |
| 2 | ★ [Frog Jumps](https://codeforces.com/problemset/problem/1324/C) | CF 1324C | Constructive greedy |
| 3 | [Jump Game](https://leetcode.com/problems/jump-game/) | LC 55 | Greedy reachability |
| 4 | [Jump Game II](https://leetcode.com/problems/jump-game-ii/) | LC 45 | Greedy BFS |
| 5 | [Gas Station](https://leetcode.com/problems/gas-station/) | LC 134 | Greedy circular |
| 6 | [Boats to Save People](https://leetcode.com/problems/boats-to-save-people/) | LC 881 | Sort + two pointers |
| 7 | [Candy](https://leetcode.com/problems/candy/) | LC 135 | Two-pass greedy |
| 8 | ★ [Stick Divisions](https://cses.fi/problemset/task/1161) | CSES 1161 | Reverse Huffman |
| 9 | [Minimize Maximum of Array](https://leetcode.com/problems/minimize-maximum-of-array/) | LC 2439 | Prefix avg greedy |
| 10 | [Berry Picking](https://usaco.org/index.php?page=viewproblem2&cpid=990) | USACO Silver | Greedy + BS |

---

## 3.7 2D DP & Grid DP [P2]

**Topics**: Grid path counting, grid minimum cost path, edit distance, common subsequence/substring, 2D state tables.

**Patterns**:
- Grid DP: `dp[i][j]` = answer for cell `(i,j)`, transition from `(i-1,j)` and `(i,j-1)`.
- LCS: `dp[i][j]` = LCS of first i chars of A and first j chars of B.
- Edit distance: `dp[i][j]` = min operations to convert A[1..i] to B[1..j].

**Classical Questions**: Number of paths from (0,0) to (n,m), minimum path sum, longest common subsequence, edit distance.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Grid Paths](https://cses.fi/problemset/task/1638) | CSES 1638 | Grid DP with obstacles |
| 2 | ★ [Edit Distance](https://cses.fi/problemset/task/1639) | CSES 1639 | Classic 2D DP |
| 3 | ★ [Array Description](https://cses.fi/problemset/task/1746) | CSES 1746 | 2D DP dp[i][v] |
| 4 | ★ [Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/) | LC 1143 | LCS |
| 5 | [Unique Paths](https://leetcode.com/problems/unique-paths/) | LC 62 | Grid counting |
| 6 | [Unique Paths II](https://leetcode.com/problems/unique-paths-ii/) | LC 63 | With obstacles |
| 7 | [Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/) | LC 64 | Grid min cost |
| 8 | [Edit Distance](https://leetcode.com/problems/edit-distance/) | LC 72 | Classic |
| 9 | [Interleaving String](https://leetcode.com/problems/interleaving-string/) | LC 97 | 2D DP |
| 10 | [Distinct Subsequences](https://leetcode.com/problems/distinct-subsequences/) | LC 115 | 2D DP |
| 11 | [Max Square](https://leetcode.com/problems/maximal-square/) | LC 221 | Grid DP |
| 12 | [Palindrome Substrings](https://leetcode.com/problems/palindromic-substrings/) | LC 647 | 2D DP / expand |
| 13 | [Money Sums](https://cses.fi/problemset/task/1745) | CSES 1745 | Subset sum DP |

---

## 3.8 Union-Find (DSU) [P3]

**Topics**: Disjoint Set Union with path compression and union by rank, connected components dynamically, cycle detection in undirected graphs.

**Patterns**:
- `find(x)`: returns root of x's component (with path compression).
- `unite(x, y)`: merge two components (union by rank/size).
- Online connectivity: process edges and track components.
- Cycle detection: if `find(u) == find(v)` before adding edge (u,v), there's a cycle.

**Classical Questions**: Dynamic connectivity, Kruskal's MST (uses DSU), count components.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Road Construction](https://cses.fi/problemset/task/1676) | CSES 1676 | DSU template |
| 2 | [Redundant Connection](https://leetcode.com/problems/redundant-connection/) | LC 684 | Cycle via DSU |
| 3 | [Number of Provinces](https://leetcode.com/problems/number-of-provinces/) | LC 547 | Connected components |
| 4 | [Accounts Merge](https://leetcode.com/problems/accounts-merge/) | LC 721 | DSU application |
| 5 | [Satisfiability of Equality](https://leetcode.com/problems/satisfiability-of-equality-equations/) | LC 990 | DSU |
| 6 | [Wormhole Sort](https://usaco.org/index.php?page=viewproblem2&cpid=992) | USACO Silver | DSU + BS |
| 7 | [Moocast](https://usaco.org/index.php?page=viewproblem2&cpid=668) | USACO Silver | DSU |
| 8 | [Friends](https://www.spoj.com/problems/FRIENDS/) | SPOJ | DSU |
| 9 | [News Distribution](https://codeforces.com/problemset/problem/1167/C) | CF 1167C | DSU group sizes |
| 10 | [Destroying Array](https://codeforces.com/problemset/problem/722/C) | CF 722C | Offline DSU |

---

## 3.9 Constructive Algorithms & Observations [P3]

**Topics**: Building valid solutions from constraints, finding patterns via small cases, parity/modularity arguments to determine if solutions exist, constructing permutations/arrays with given properties.

**Patterns**:
- "Construct any valid answer" → think about the simplest structure that satisfies constraints.
- Test small cases (n=1,2,3) to find the pattern.
- "Is it possible?" → look for invariants (parity, sums mod k, etc.).

**Classical Questions**: Construct array with given GCD, construct matrix with given row/column sums.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [XXXXX](https://codeforces.com/problemset/problem/1364/A) | CF 1364A | Subarray divisibility |
| 2 | [Frog Jumps](https://codeforces.com/problemset/problem/1324/C) | CF 1324C | Constructive |
| 3 | [Make It Beautiful](https://codeforces.com/problemset/problem/1714/C) | CF 1714C | Constructive |
| 4 | [Balanced Brackets](https://codeforces.com/problemset/problem/1556/C) | CF 1556C | Constructive |
| 5 | [Short Substrings](https://codeforces.com/problemset/problem/1241/A) | CF 1241A | String construction |
| 6 | [Maximize the Confusion](https://leetcode.com/problems/maximize-the-confusion-of-an-exam/) | LC 2024 | Sliding window |
| 7 | [Find Valid Matrix Given Row and Col Sums](https://leetcode.com/problems/find-valid-matrix-given-row-and-column-sums/) | LC 1605 | Greedy construction |
| 8 | [Check If Array Pairs Divisible by K](https://leetcode.com/problems/check-if-array-pairs-are-divisible-by-k/) | LC 1497 | Modular pairing |
| 9 | [Gray Code](https://cses.fi/problemset/task/2205) | CSES 2205 | Construction |
| 10 | [Towers](https://cses.fi/problemset/task/1073) | CSES 1073 | Greedy construction |

---

## 3.9 Meet-in-the-Middle [P4]

**Topics**: Splitting the input into two halves, enumerating all possibilities for each half, combining results. Turns O(2^N) into O(2^(N/2) · log).

**Patterns**:
- Split array of N ≤ 40 elements into two halves of ~20.
- Enumerate all 2^20 subsets for each half.
- Sort one half's results and binary search for complements from the other half.

**Classical Questions**: Subset sum closest to target (N ≤ 40), 4-sum.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Meet in the Middle](https://cses.fi/problemset/task/1628) | CSES 1628 | Template |
| 2 | [4Sum](https://leetcode.com/problems/4sum/) | LC 18 | Two-pointer variant |
| 3 | [Closest Subsequence Sum](https://leetcode.com/problems/closest-subsequence-sum/) | LC 1755 | MITM exact |
| 4 | [Partition Equal Subset](https://leetcode.com/problems/partition-equal-subset-sum/) | LC 416 | DP or MITM |
| 5 | [ABCDEF](https://www.spoj.com/problems/ABCDEF/) | SPOJ | MITM 6-variable |
| 6 | [Hamro and Array](https://codeforces.com/problemset/problem/911/D) | CF 911D | MITM variant |

---

### Tier 3 Summary

| Priority | Topics Covered |
|----------|---------------|
| [P1] | BS on Answer, Sorting & Comparators, BFS/DFS Graphs, Intro DP |
| [P2] | Intermediate Greedy, 2D DP & Grid DP |
| [P3] | Union-Find (DSU), Constructive Algorithms |
| [P4] | Meet-in-the-Middle |

**Total problems in Tier 3: ~107**

> [Checkpoint] **Checkpoint**: You can solve CF Div.2 C problems (1300–1500 rated). You can implement BFS/DFS from scratch, do binary search on answer, and solve basic DP problems.
