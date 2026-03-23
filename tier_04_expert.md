# Tier 4: Expert (CF Rating 1600 – 1899)

> **Goal**: Confidently solve Div.2 D / Div.1 A. Master intermediate DP variants, shortest-path algorithms, segment trees, and string matching.

At this tier you move from graph traversal into weighted graphs and range-query data structures. You master shortest-path algorithms, minimum spanning trees, monotonic structures for O(n) range queries, and the two most important point-update data structures: Segment Trees and Fenwick Trees. By the end of Tier 4 you will consistently solve Div. 2 D problems and occasionally reach E.

---

## 4.1 Shortest Path Algorithms 🔴 P1

**Topics**: Dijkstra's algorithm (priority queue), 0-1 BFS (deque), Bellman-Ford (negative edges, negative cycle detection), Floyd-Warshall (all-pairs), SPFA.

**Patterns**:
- **Dijkstra**: Non-negative weights only. O((V+E) log V) with priority queue. Always use `dist[u] < current` check for lazy deletion.
- **0-1 BFS**: Weights are 0 or 1. Use deque — push 0-weight to front, 1-weight to back. O(V+E).
- **Bellman-Ford**: Handles negative weights. O(VE). Run V-th iteration to detect negative cycles.
- **Floyd-Warshall**: All-pairs shortest path in O(V^3). V ≤ 500.

**Classical Questions**: Shortest path in a weighted graph, finding negative cycles, minimum cost grid path with 0/1 weights.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Shortest Routes I](https://cses.fi/problemset/task/1671) | CSES 1671 | Dijkstra template |
| 2 | ⭐ [Shortest Routes II](https://cses.fi/problemset/task/1672) | CSES 1672 | Floyd-Warshall |
| 3 | [High Score](https://cses.fi/problemset/task/1673) | CSES 1673 | Bellman-Ford / neg cycle |
| 4 | [Cycle Finding](https://cses.fi/problemset/task/1197) | CSES 1197 | Bellman-Ford |
| 5 | ⭐ [Min Cost Valid Path](https://leetcode.com/problems/minimum-cost-to-make-at-least-one-valid-path-in-a-grid/) | LC 1368 | 0-1 BFS |
| 6 | [Network Delay Time](https://leetcode.com/problems/network-delay-time/) | LC 743 | Dijkstra |
| 7 | [Cheapest Flights Within K Stops](https://leetcode.com/problems/cheapest-flights-within-k-stops/) | LC 787 | Modified BF / Dijkstra |
| 8 | [Path With Minimum Effort](https://leetcode.com/problems/path-with-minimum-effort/) | LC 1631 | Dijkstra / BS+BFS |
| 9 | [Swim in Rising Water](https://leetcode.com/problems/swim-in-rising-water/) | LC 778 | Dijkstra on grid |
| 10 | [Flight Discount](https://cses.fi/problemset/task/1195) | CSES 1195 | Layered Dijkstra |
| 11 | [Investigation](https://cses.fi/problemset/task/1202) | CSES 1202 | Dijkstra + counting |
| 12 | [Shortest Path (SPOJ)](https://www.spoj.com/problems/SHPATH/) | SPOJ SHPATH | Dijkstra |

---

## 4.2 Knapsack & Subset DP 🔴 P1

**Topics**: 0/1 Knapsack, unbounded knapsack, bounded knapsack, subset sum, counting subsets, DP over subsets (bitmask DP intro).

**Patterns**:
- **0/1 Knapsack**: `dp[i][w] = max value using first i items with capacity w`. Space optimize to 1D by iterating w in reverse.
- **Unbounded**: iterate w forward (items can be reused).
- **Bitmask DP**: State is a bitmask representing which elements are "used". Works for N ≤ 20.

**Classical Questions**: Classic knapsack, partition into two equal-sum subsets, minimum difference partition.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Book Shop](https://cses.fi/problemset/task/1158) | CSES 1158 | 0/1 Knapsack |
| 2 | ⭐ [Money Sums](https://cses.fi/problemset/task/1745) | CSES 1745 | Subset sum DP |
| 3 | [Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum/) | LC 416 | Subset sum |
| 4 | [Target Sum](https://leetcode.com/problems/target-sum/) | LC 494 | Subset sum variant |
| 5 | [Coin Change](https://leetcode.com/problems/coin-change/) | LC 322 | Unbounded knapsack |
| 6 | [Coin Change II](https://leetcode.com/problems/coin-change-ii/) | LC 518 | Counting ways |
| 7 | [Ones and Zeroes](https://leetcode.com/problems/ones-and-zeroes/) | LC 474 | 2D Knapsack |
| 8 | [Last Stone Weight II](https://leetcode.com/problems/last-stone-weight-ii/) | LC 1049 | Min diff partition |
| 9 | ⭐ [Elevator Rides](https://cses.fi/problemset/task/1653) | CSES 1653 | Bitmask DP |
| 10 | [Two Sets II](https://cses.fi/problemset/task/1093) | CSES 1093 | Subset sum count |
| 11 | [KNAPSACK - The Knapsack Problem](https://www.spoj.com/problems/KNAPSACK/) | SPOJ | Classic knapsack |
| 12 | [Profitable Schemes](https://leetcode.com/problems/profitable-schemes/) | LC 879 | 2D knapsack |

---

## 4.3 Topological Sort & DAG DP 🔴 P1

**Topics**: Topological ordering (Kahn's BFS / DFS-based), DP on DAGs (longest path, counting paths), detecting if a graph is a DAG.

**Patterns**:
- **Kahn's algorithm**: Start with nodes of in-degree 0, push to queue, process and reduce in-degrees.
- **DP on DAG**: Process nodes in topological order. `dp[v] = best over all predecessors u + edge(u,v)`.
- Longest path in a DAG is solvable in O(V+E) (unlike general graphs which are NP-hard).

**Classical Questions**: Course ordering, longest path in a DAG, counting paths from source to sink.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Course Schedule II](https://leetcode.com/problems/course-schedule-ii/) | LC 210 | Topo sort |
| 2 | ⭐ [Longest Flight Route](https://cses.fi/problemset/task/1680) | CSES 1680 | DAG DP |
| 3 | [Game Routes](https://cses.fi/problemset/task/1681) | CSES 1681 | Count paths in DAG |
| 4 | [Fox And Names](https://codeforces.com/problemset/problem/510/C) | CF 510C | Topo sort from constraints |
| 5 | [Sort Items by Groups](https://leetcode.com/problems/sort-items-by-groups-respecting-dependencies/) | LC 1203 | Multi-level topo sort |
| 6 | [Minimum Height Trees](https://leetcode.com/problems/minimum-height-trees/) | LC 310 | Topo-like peeling |
| 7 | [Toposort](https://www.spoj.com/problems/TOPOSORT/) | SPOJ | Topo sort |
| 8 | [Course Schedule IV](https://leetcode.com/problems/course-schedule-iv/) | LC 1462 | Topo + reachability |
| 9 | [Milking Order](https://usaco.org/index.php?page=viewproblem2&cpid=838) | USACO Gold | Topo sort |

---

## 4.4 MST & Advanced Graph Concepts 🟠 P2

**Topics**: Kruskal's algorithm (with DSU), Prim's algorithm, properties of MST, Eulerian paths/circuits (Hierholzer's algorithm), bridges and articulation points.

**Patterns**:
- **Kruskal's**: Sort edges by weight, add if it doesn't form a cycle (check via DSU). O(E log E).
- **Eulerian circuit** exists iff all vertices have even degree (undirected) or in-degree = out-degree (directed).
- **Bridges**: edges whose removal increases connected components. Found via Tarjan's DFS with discovery/low values.

**Classical Questions**: Minimum spanning tree, finding bridges, Euler tour.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Road Reparation](https://cses.fi/problemset/task/1675) | CSES 1675 | MST / Kruskal |
| 2 | ⭐ [Mail Delivery](https://cses.fi/problemset/task/1691) | CSES 1691 | Euler circuit |
| 3 | [De Bruijn Sequence](https://cses.fi/problemset/task/1692) | CSES 1692 | Euler path |
| 4 | [Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/) | LC 1584 | MST / Prim |
| 5 | [Critical Connections](https://leetcode.com/problems/critical-connections-in-a-network/) | LC 1192 | Bridges / Tarjan |
| 6 | [Fine Dining](https://usaco.org/index.php?page=viewproblem2&cpid=861) | USACO Gold | MST variant |
| 7 | [MST (SPOJ)](https://www.spoj.com/problems/MST/) | SPOJ MST | Kruskal |
| 8 | [Reconstruct Itinerary](https://leetcode.com/problems/reconstruct-itinerary/) | LC 332 | Euler path |
| 9 | [Teleporters Path](https://cses.fi/problemset/task/1693) | CSES 1693 | Euler path directed |
| 10 | [Redundant Connection II](https://leetcode.com/problems/redundant-connection-ii/) | LC 685 | Directed MST/DSU |

---

## 4.5 Intermediate DP: LIS, Intervals & Ranges 🟠 P2

**Topics**: Longest Increasing Subsequence (O(N log N)), interval DP, range DP, 1D DP with binary search optimization.

**Patterns**:
- **LIS in O(N log N)**: Maintain a `tails` array; for each element, binary search for the position to insert/replace.
- **Interval DP**: `dp[l][r]` = answer for the subproblem `[l, r]`. Try all split points k in `[l, r-1]`.
- "Merging adjacent elements optimally" → interval DP.

**Classical Questions**: LIS, matrix chain multiplication, optimal BST, burst balloons.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/) | LC 300 | LIS O(N log N) |
| 2 | ⭐ [Burst Balloons](https://leetcode.com/problems/burst-balloons/) | LC 312 | Interval DP |
| 3 | [Increasing Subsequence](https://cses.fi/problemset/task/1145) | CSES 1145 | LIS |
| 4 | [Russian Doll Envelopes](https://leetcode.com/problems/russian-doll-envelopes/) | LC 354 | 2D LIS |
| 5 | [Minimum Cost Tree From Leaf Values](https://leetcode.com/problems/minimum-cost-tree-from-leaf-values/) | LC 1130 | Interval DP |
| 6 | [Stone Game](https://leetcode.com/problems/stone-game/) | LC 877 | Interval DP / game |
| 7 | [Minimum Score Triangulation](https://leetcode.com/problems/minimum-score-triangulation-of-polygon/) | LC 1039 | Interval DP |
| 8 | [Longest Ideal Subsequence](https://leetcode.com/problems/longest-ideal-subsequence/) | LC 2370 | DP optimization |
| 9 | [Palindrome Partitioning II](https://leetcode.com/problems/palindrome-partitioning-ii/) | LC 132 | DP |
| 10 | [Mixtures](https://www.spoj.com/problems/MIXTURES/) | SPOJ | Interval DP |
| 11 | [Number of LIS](https://leetcode.com/problems/number-of-longest-increasing-subsequence/) | LC 673 | LIS counting |

---

## 4.6 String Algorithms: KMP, Hashing & Trie 🟠 P2

**Topics**: KMP failure function & pattern matching, string hashing (rolling hash / Rabin-Karp), Trie data structure, Z-algorithm.

**Patterns**:
- **KMP**: Precompute failure function in O(M), then match in O(N). Total O(N+M).
- **Rolling Hash**: Hash a substring in O(1) after O(N) prep. Compare substrings by hash (with collision risk).
- **Trie**: Tree of characters for prefix queries. O(L) insert/search where L = string length.
- **Z-array**: `z[i]` = length of longest substring starting at `i` that matches a prefix of the string.

**Classical Questions**: Pattern matching, finding all occurrences, autocomplete with Trie, longest common prefix.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [String Matching](https://cses.fi/problemset/task/1753) | CSES 1753 | KMP / Z / Hashing |
| 2 | ⭐ [Implement Trie](https://leetcode.com/problems/implement-trie-prefix-tree/) | LC 208 | Trie template |
| 3 | [String Functions](https://cses.fi/problemset/task/2107) | CSES 2107 | Z-algorithm |
| 4 | [Finding Periods](https://cses.fi/problemset/task/1733) | CSES 1733 | KMP failure function |
| 5 | [Finding Borders](https://cses.fi/problemset/task/1732) | CSES 1732 | KMP borders (from Tier 1) |
| 5 | [Word Search II](https://leetcode.com/problems/word-search-ii/) | LC 212 | Trie + backtracking |
| 6 | [Longest Happy Prefix](https://leetcode.com/problems/longest-happy-prefix/) | LC 1392 | KMP / Z-array |
| 7 | [Repeated DNA Sequences](https://leetcode.com/problems/repeated-dna-sequences/) | LC 187 | Rolling hash |
| 8 | [Map Sum Pairs](https://leetcode.com/problems/map-sum-pairs/) | LC 677 | Trie |
| 9 | [Replace Words](https://leetcode.com/problems/replace-words/) | LC 648 | Trie |
| 10 | [Longest Word in Dictionary](https://leetcode.com/problems/longest-word-in-dictionary/) | LC 720 | Trie |
| 11 | [NHAY - A Needle in the Haystack](https://www.spoj.com/problems/NHAY/) | SPOJ | KMP |

---

## 4.7 Combinatorics & Modular Inverse 🟡 P3

**Topics**: nCr mod p (using factorials + modular inverse), Pascal's triangle, Stars and Bars, Fermat's little theorem, Wilson's theorem.

**Patterns**:
- Precompute `fact[i]` and `inv_fact[i]` up to N using modular inverse. Then `nCr(n,r) = fact[n] * inv_fact[r] % mod * inv_fact[n-r] % mod`.
- **Modular inverse**: `a^(-1) mod p = a^(p-2) mod p` when p is prime (Fermat's little theorem).
- **Stars and Bars**: Distributing n identical items into k distinct bins = C(n+k-1, k-1).

**Classical Questions**: Counting paths on grid with obstacles, distributing items, nCr queries.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Binomial Coefficients](https://cses.fi/problemset/task/1079) | CSES 1079 | nCr mod p |
| 2 | [Creating Strings II](https://cses.fi/problemset/task/1715) | CSES 1715 | Multinomial coefficients |
| 3 | [Distributing Apples](https://cses.fi/problemset/task/1716) | CSES 1716 | Stars and Bars |
| 4 | [Christmas Party](https://cses.fi/problemset/task/1717) | CSES 1717 | Derangements |
| 5 | [Bracket Sequences I](https://cses.fi/problemset/task/2064) | CSES 2064 | Catalan numbers |
| 6 | [Unique Paths (with obstacles)](https://leetcode.com/problems/unique-paths/) | LC 62 | nCr formula |
| 7 | [Pascals Triangle](https://leetcode.com/problems/pascals-triangle/) | LC 118 | Build triangle |
| 8 | [Count Sorted Vowel Strings](https://leetcode.com/problems/count-sorted-vowel-strings/) | LC 1641 | Stars & Bars / DP |
| 9 | [Count Good Numbers](https://leetcode.com/problems/count-good-numbers/) | LC 1922 | Mod exponentiation (from Tier 1) |
| 10 | [Throwing Dice](https://cses.fi/problemset/task/1096) | CSES 1096 | Matrix exp intro |

---

## 4.8 Game Theory Basics 🟡 P3

**Topics**: Nim game, Sprague-Grundy theorem intro, winning/losing positions, game DP.

**Patterns**:
- **Nim**: XOR of all pile sizes. If XOR ≠ 0, first player wins.
- **Game DP**: `dp[state]` = WIN or LOSE. A state is WIN if there exists any move to a LOSE state.
- A state is LOSE if all moves lead to WIN states.

**Classical Questions**: Nim, stone game variants, Grundy numbers.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Nim Game I](https://cses.fi/problemset/task/1730) | CSES 1730 | Classic Nim |
| 2 | [Nim Game II](https://cses.fi/problemset/task/1098) | CSES 1098 | Nim variant |
| 3 | [Stair Game](https://cses.fi/problemset/task/1099) | CSES 1099 | Staircase Nim |
| 4 | [Stone Game](https://leetcode.com/problems/stone-game/) | LC 877 | Game DP |
| 5 | [Nim Game (LC)](https://leetcode.com/problems/nim-game/) | LC 292 | Modular |
| 6 | [Can I Win](https://leetcode.com/problems/can-i-win/) | LC 464 | Bitmask game DP |
| 7 | [Stone Game III](https://leetcode.com/problems/stone-game-iii/) | LC 1406 | Game DP |
| 8 | [Grundy's Game](https://cses.fi/problemset/task/2207) | CSES 2207 | Grundy |
| 9 | [Stick Game](https://cses.fi/problemset/task/1729) | CSES 1729 | DP game |

---

## 4.9 Interactive Problems & Output Flushing 🟢 P4

**Topics**: Interactive problem protocol, binary search via queries, flushing output (`fflush(stdout)` / `cout.flush()`), adaptive strategies.

**Patterns**:
- Read problem statement carefully for query format and limits.
- Binary search with queries: guess the answer in O(log N) queries.
- Always flush output after each query.
- Some interactive problems require randomized strategies.

**Classical Questions**: Guess the number in log(N) queries, find the minimum with comparisons.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Guess the Number](https://codeforces.com/problemset/problem/1010/A) | CF 1010A | Interactive archetype |
| 2 | [Guess Number Higher or Lower](https://leetcode.com/problems/guess-number-higher-or-lower/) | LC 374 | BS interactive |
| 3 | [Bear and Pebbles](https://codeforces.com/problemset/problem/580/A) | CF 580A | Interactive thinking |
| 4 | [Lost Numbers](https://codeforces.com/problemset/problem/1167/B) | CF 1167B | Query strategy |
| 5 | [Xor Guessing](https://codeforces.com/problemset/problem/1207/E) | CF 1207E | XOR + interactive |
| 6 | [Binary Search (interactive)](https://codeforces.com/edu/course/2/lesson/6/1/practice/contest/283911/problem/A) | CF Edu | Interactive BS |

---

### Tier 4 Summary

| Priority | Topics Covered |
|----------|---------------|
| 🔴 P1 | Shortest Paths (Dijkstra/BF/Floyd), Knapsack & Subset DP, Topo Sort & DAG DP |
| 🟠 P2 | MST & Euler Paths, LIS & Interval DP, String Algorithms (KMP/Trie) |
| 🟡 P3 | Combinatorics & Mod Inverse, Game Theory Basics |
| 🟢 P4 | Interactive Problems |

**Total problems in Tier 4: ~111**

> ✅ **Checkpoint**: You can solve CF Div.2 D / Div.1 A problems (1600–1800 rated). Dijkstra, knapsack DP, KMP, and topo sort are second nature.
