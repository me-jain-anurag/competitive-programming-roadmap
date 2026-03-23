# Tier 6: Master (CF Rating 2100 – 2299)

> **Goal**: Combine data structures. Segment trees with lazy propagation, advanced tree techniques, SOS DP, re-rooting DP, SCCs, 2-SAT. Solve Div.1 C problems.

At this tier you tackle the hardest graph algorithms and advanced string structures. You master strongly connected components, bridges and articulation points, Euler paths, LCA with binary lifting, suffix arrays, and network flow. These topics appear in Div. 1 C and D problems. By the end of Tier 6 you will consistently solve Div. 1 C and occasionally reach D.

---

## 6.1 Segment Tree with Lazy Propagation 🔴 P1

**Topics**: Range update + range query, lazy propagation for additive updates, multiplicative updates, assignment updates, combining different lazy operations.

**Patterns**:
- **Lazy propagation**: Instead of updating every node in a range, store a "pending" update in internal nodes and push it down when needed.
- "Range add + Range sum", "Range set + Range min" — all need lazy.
- The `push_down` function propagates lazy values to children before accessing them.

**Classical Questions**: Range addition + range sum query, range assign + range min query.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Range Update Queries](https://cses.fi/problemset/task/1651) | CSES 1651 | Lazy SegTree template |
| 2 | ⭐ [Range Updates and Sums](https://cses.fi/problemset/task/1735) | CSES 1735 | Lazy add + set |
| 3 | [Polynomial Queries](https://cses.fi/problemset/task/1736) | CSES 1736 | Arithmetic progression lazy |
| 4 | [HORRIBLE - Horrible Queries](https://www.spoj.com/problems/HORRIBLE/) | SPOJ | Lazy SegTree |
| 5 | [LITE - Light Switching](https://www.spoj.com/problems/LITE/) | SPOJ | XOR lazy |
| 6 | [Range Module](https://leetcode.com/problems/range-module/) | LC 715 | Interval SegTree |
| 7 | [My Calendar III](https://leetcode.com/problems/my-calendar-iii/) | LC 732 | Lazy SegTree |
| 8 | [Falling Squares](https://leetcode.com/problems/falling-squares/) | LC 699 | Coordinate compress + lazy |
| 9 | [Count of Range Sum](https://leetcode.com/problems/count-of-range-sum/) | LC 327 | SegTree / merge sort |
| 10 | [Max Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/) | LC 1235 | DP + SegTree |

---

## 6.2 Euler Tour & Subtree/Path Queries on Trees 🔴 P1

**Topics**: Euler Tour (flattening a tree into an array), subtree queries via range queries on the flattened array, path queries with LCA decomposition.

**Patterns**:
- **Euler Tour**: DFS traversal recording `tin[v]` (entry time) and `tout[v]` (exit time). Subtree of v = range `[tin[v], tout[v]]` in the array.
- Subtree sum/update → BIT/SegTree on the Euler tour array.
- Path queries → Euler Tour + LCA or HLD.

**Classical Questions**: Subtree sum update/query, path update/query.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Subtree Queries](https://cses.fi/problemset/task/1137) | CSES 1137 | Euler Tour + BIT |
| 2 | ⭐ [Path Queries](https://cses.fi/problemset/task/1138) | CSES 1138 | Euler Tour / HLD |
| 3 | [Path Queries II](https://cses.fi/problemset/task/2134) | CSES 2134 | HLD + SegTree |
| 4 | [Distinct Colors](https://cses.fi/problemset/task/1139) | CSES 1139 | Small-to-large merge |
| 5 | [Count Nodes in Sub-Tree](https://leetcode.com/problems/number-of-nodes-in-the-sub-tree-with-the-same-label/) | LC 1519 | DFS / Euler tour |
| 6 | [QTREE](https://www.spoj.com/problems/QTREE/) | SPOJ QTREE | HLD |
| 7 | [COT2](https://www.spoj.com/problems/COT2/) | SPOJ | Euler Tour + Mo |
| 8 | [Promotion Counting](https://usaco.org/index.php?page=viewproblem2&cpid=696) | USACO Gold | Euler tour merge |

---

## 6.3 Re-rooting DP 🟠 P2

**Topics**: Computing an answer for every node as root efficiently. Bottom-up DFS followed by top-down DFS to "re-root" the tree.

**Patterns**:
1. First DFS (bottom-up): compute `dp_down[v]` = answer for subtree rooted at v.
2. Second DFS (top-down): compute `dp_up[v]` = answer from the rest of the tree (complement of v's subtree).
3. Combine: `answer[v] = combine(dp_down[v], dp_up[v])`.

**Classical Questions**: Sum of distances to all nodes from each node, farthest node from each node.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Tree Distances I](https://cses.fi/problemset/task/1132) | CSES 1132 | Re-rooting farthest |
| 2 | ⭐ [Tree Distances II](https://cses.fi/problemset/task/1133) | CSES 1133 | Re-rooting sum |
| 3 | [Sum of Distances in Tree](https://leetcode.com/problems/sum-of-distances-in-tree/) | LC 834 | Re-rooting |
| 4 | [Count Subtrees with Max Distance](https://leetcode.com/problems/count-subtrees-with-max-distance-between-cities/) | LC 1617 | Bitmask + tree |
| 5 | [Minimum Edge Weight Equilibrium](https://leetcode.com/problems/minimum-edge-weight-equilibrium-queries-in-a-tree/) | LC 2846 | LCA + re-root |
| 6 | [Maximum Sum BST in Binary Tree](https://leetcode.com/problems/maximum-sum-bst-in-binary-tree/) | LC 1373 | Tree DP |
| 7 | [Directory Traversal](https://usaco.org/index.php?page=viewproblem2&cpid=814) | USACO Gold | Re-rooting |

---

## 6.4 SOS DP (Sum over Subsets) 🟠 P2

**Topics**: Efficiently computing sum/count over all subsets (or supersets) of each bitmask. O(N · 2^N) using the "zeta/Mobius transform" approach.

**Patterns**:
- For each bit position, iterate over all masks and propagate from submasks.
- `for bit in 0..N: for mask in 0..(1<<N): if mask & (1<<bit): dp[mask] += dp[mask ^ (1<<bit)]`
- After this, `dp[mask]` = sum of `original[submask]` for all submasks of mask.

**Classical Questions**: Count of submasks with property X for each mask, AND/OR convolution.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Vowels (SOS DP)](https://codeforces.com/problemset/problem/165/E) | CF 165E | SOS DP archetype |
| 2 | [Compatible Numbers](https://codeforces.com/problemset/problem/449/D) | CF 449D | SOS DP |
| 3 | [Counting Bits](https://codeforces.com/problemset/problem/1208/F) | CF 1208F | SOS DP |
| 4 | [XOR Inverse](https://codeforces.com/problemset/problem/1416/C) | CF 1416C | Bit contribution |
| 5 | [AND Plus OR](https://codeforces.com/problemset/problem/1721/E) | CF 1721E | SOS |
| 6 | [Sum Over Subsets](https://judge.yosupo.jp/problem/subset_sum_convolution) | Library Checker | Template |
| 7 | [Maximize XOR](https://leetcode.com/problems/maximum-xor-of-two-numbers-in-an-array/) | LC 421 | Trie / SOS |

---

## 6.5 SCCs, 2-SAT & Advanced Graph 🟠 P2

**Topics**: Strongly Connected Components (Kosaraju / Tarjan), 2-SAT via implication graphs, condensation graph, topological sort on condensation.

**Patterns**:
- **Kosaraju's**: Two DFS passes — first to get finish order, second on reversed graph in reverse finish order.
- **2-SAT**: Model boolean constraints as implications (x → y means "if x then y"). Build implication graph, find SCCs. If x and ¬x are in the same SCC → unsatisfiable.
- Condensation: contract each SCC into a single node → resulting graph is a DAG.

**Classical Questions**: Finding SCCs, satisfying boolean formulas with at most 2 literals per clause.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Giant Pizza](https://cses.fi/problemset/task/1684) | CSES 1684 | 2-SAT |
| 2 | ⭐ [Planets and Kingdoms](https://cses.fi/problemset/task/1683) | CSES 1683 | SCCs |
| 3 | [Coin Collector](https://cses.fi/problemset/task/1686) | CSES 1686 | Condensation + DAG DP |
| 4 | [Flight Routes Check](https://cses.fi/problemset/task/1682) | CSES 1682 | SCC check |
| 5 | [Kosaraju (SPOJ)](https://www.spoj.com/problems/KOSARAJU/) | SPOJ | SCC template |
| 6 | [Stongly Connected Component](https://judge.yosupo.jp/problem/scc) | Library Checker | SCC template |
| 7 | [Satisfiability of Equality](https://leetcode.com/problems/satisfiability-of-equality-equations/) | LC 990 | 2-SAT lite |
| 8 | [Critical Connections](https://leetcode.com/problems/critical-connections-in-a-network/) | LC 1192 | Bridges/Tarjan |

---

## 6.6 Inclusion-Exclusion Principle 🟡 P3

**Topics**: Counting via inclusion-exclusion, derangements, Euler's totient function, sieve-based inclusion-exclusion.

**Patterns**:
- |A₁ ∪ A₂ ∪ ... ∪ Aₙ| = Σ|Aᵢ| - Σ|Aᵢ ∩ Aⱼ| + Σ|Aᵢ ∩ Aⱼ ∩ Aₖ| - ...
- For counting multiples of at least one prime in a set → iterate over subsets of prime set.
- Derangement formula: D(n) = n! · Σ(-1)^k / k! for k=0..n.

**Classical Questions**: Count numbers ≤ N divisible by at least one of given primes, derangements.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Prime Multiples](https://cses.fi/problemset/task/2185) | CSES 2185 | Inclusion-Exclusion |
| 2 | [Christmas Party](https://cses.fi/problemset/task/1717) | CSES 1717 | Derangements |
| 3 | [Coprime Pairs](https://codeforces.com/problemset/problem/547/C) | CF 547C | Incl-Excl + Mobius |
| 4 | [Counting Coprime Pairs](https://cses.fi/problemset/task/2417) | CSES 2417 | Totient / IE |
| 5 | [Ugly Number III](https://leetcode.com/problems/ugly-number-iii/) | LC 1201 | Incl-Excl + BS |
| 6 | [Count Integers](https://codeforces.com/problemset/problem/630/K) | CF 630K | IE |
| 7 | [Kth Smallest Number in Multiplication Table](https://leetcode.com/problems/kth-smallest-number-in-multiplication-table/) | LC 668 | BS + counting |

---

## 6.7 Matrix Exponentiation 🟡 P3

**Topics**: Representing linear recurrences as matrix multiplication, computing n-th term in O(K^3 · log N) where K = matrix size.

**Patterns**:
- Fibonacci: [F(n+1), F(n)] = [[1,1],[1,0]]^n · [F(1), F(0)].
- Any linear recurrence of order K → K×K matrix.
- Also used for counting paths of length N in a graph (adjacency matrix ^ N).

**Classical Questions**: N-th Fibonacci in O(log N), counting paths of exact length K in a graph.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Graph Paths I](https://cses.fi/problemset/task/1723) | CSES 1723 | Matrix exp |
| 2 | [Fibonacci Numbers](https://cses.fi/problemset/task/1722) | CSES 1722 | Matrix exp |
| 3 | [Graph Paths II](https://cses.fi/problemset/task/1724) | CSES 1724 | Matrix exp min-plus |
| 4 | [Throwing Dice](https://cses.fi/problemset/task/1096) | CSES 1096 | Matrix exp |
| 5 | [MPOW - Power of a Matrix](https://www.spoj.com/problems/MPOW/) | SPOJ | Matrix exp |
| 6 | [Nth Tribonacci Number](https://leetcode.com/problems/n-th-tribonacci-number/) | LC 1137 | Matrix exp variant |
| 7 | [Knight Dialer](https://leetcode.com/problems/knight-dialer/) | LC 935 | Matrix exp / DP |

---

## 6.8 Centroid Decomposition 🟡 P3

**Topics**: Finding centroids of trees recursively, counting paths with specific properties, point queries on trees.

**Patterns**:
- **Centroid**: Node whose removal splits the tree into components of size ≤ N/2.
- Build a centroid decomposition tree of depth O(log N).
- For each centroid, count paths passing through it, then recurse on subtrees.
- Used for: counting paths of length K, distance queries, update/query on tree paths.

**Classical Questions**: Count pairs of vertices at distance exactly K, distance queries on trees.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Xenia and Tree](https://codeforces.com/problemset/problem/342/E) | CF 342E | Centroid decomp |
| 2 | [Finding Centroids](https://cses.fi/problemset/task/2079) | CSES 2079 | Centroid basics |
| 3 | [QTREE5](https://www.spoj.com/problems/QTREE5/) | SPOJ | Centroid decomp |
| 4 | [Race](https://oj.uz/problem/view/IOI11_race) | IOI 2011 | Centroid |
| 5 | [New Year Tree (CF)](https://codeforces.com/problemset/problem/620/E) | CF 620E | Euler tour + bitmask |
| 6 | [Centroid Decomposition](https://judge.yosupo.jp/problem/centroid_decomposition) | Library Checker | Template |

---

## 6.9 Advanced Greedy & Observation 🟢 P4

**Topics**: Exchange arguments (formal proofs), greedy with priority queues, multi-step greedy strategies, observation-heavy problems.

**Patterns**:
- **Exchange argument**: Assume optimal solution differs from greedy. Show swapping to match greedy doesn't worsen the answer.
- Priority queue for "always process the best available" strategies.
- Many CF problems at this level require a key observation that simplifies the problem dramatically.

**Classical Questions**: Job scheduling with deadlines, Huffman coding, rearranging strings.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Reorganize String](https://leetcode.com/problems/reorganize-string/) | LC 767 | Greedy + PQ |
| 2 | [Task Scheduler](https://leetcode.com/problems/task-scheduler/) | LC 621 | Greedy counting |
| 3 | [IPO](https://leetcode.com/problems/ipo/) | LC 502 | Greedy + PQ |
| 4 | [Minimum Number of Refueling Stops](https://leetcode.com/problems/minimum-number-of-refueling-stops/) | LC 871 | Greedy PQ |
| 5 | [Course Schedule III](https://leetcode.com/problems/course-schedule-iii/) | LC 630 | Greedy sort + PQ |
| 6 | [Kalila and Dimna](https://codeforces.com/problemset/problem/319/C) | CF 319C | Observation + DP |
| 7 | [Queue](https://codeforces.com/problemset/problem/767/C) | CF 767C | Greedy reconstruction |

---

### Tier 6 Summary

| Priority | Topics Covered |
|----------|---------------|
| 🔴 P1 | Lazy Segment Tree, Euler Tour + Subtree/Path Queries |
| 🟠 P2 | Re-rooting DP, SOS DP, SCCs & 2-SAT |
| 🟡 P3 | Inclusion-Exclusion, Matrix Exponentiation, Centroid Decomposition |
| 🟢 P4 | Advanced Greedy & Observation |

**Total problems in Tier 6: ~105**

> ✅ **Checkpoint**: You can solve Div.1 C problems (2100–2300 rated). Lazy segment trees, Euler tours, and 2-SAT are in your toolkit. You can combine multiple structures to solve one problem.
