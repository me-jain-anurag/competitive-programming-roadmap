# Tier 10: Legendary Grandmaster (CF Rating 3000+)

> **Goal**: The absolute apex. Problems at this level require novel algorithmic ideas, research-level math, extreme constant-factor optimization, and synthesizing 3+ advanced techniques in a single solution.

This is the pinnacle of competitive programming. At this tier you engage with research-level algorithms, advanced combinatorics, cutting-edge DP techniques, and olympiad-level problem solving strategies. These topics appear in the hardest problems of Codeforces Div. 1, IOI, and ICPC World Finals. Mastery here requires not just knowing algorithms but inventing new approaches.

---

## 10.1 Advanced Flow & Matroid Theory 🔴 P1

**Topics**: General matching (Edmonds' blossom algorithm), matroid intersection, Gomory-Hu trees (all-pairs min-cut), min-cut applications, project selection.

**Patterns**:
- **General matching** (non-bipartite): Edmonds' blossom algorithm. O(V^3). Rarely implemented from scratch — use library.
- **Gomory-Hu tree**: A weighted tree on V vertices such that the min-cut between any pair (u,v) equals the min edge on the path u→v in this tree. Built with V-1 max-flow calls.
- **Matroid intersection**: Finding common independent set in two matroids. Used for problems that combine two types of "independence" constraints.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [General Matching](https://judge.yosupo.jp/problem/general_matching) | Library Checker | Blossom |
| 2 | [Gomory-Hu Tree](https://judge.yosupo.jp/problem/gomory_hu_tree) | Library Checker | Template |
| 3 | [Project Selection](https://codeforces.com/problemset/problem/311/E) | CF 311E | Min-cut |
| 4 | [Minimum Weight Closure](https://codeforces.com/problemset/problem/1082/G) | CF 1082G | Flow + closure |
| 5 | [Matroid Intersection](https://judge.yosupo.jp/problem/matroid_intersection) | Library Checker | Template |
| 6 | [Stable Marriage (Gale-Shapley)](https://www.spoj.com/problems/STABLEMP/) | SPOJ | Stable matching |

---

## 10.2 Top Trees & Euler Tour Trees 🟠 P2

**Topics**: Top Trees for aggregation over dynamic forests (more powerful than LCT for subtree queries), Euler Tour Trees (ETT) via balanced BSTs for dynamic forest connectivity and subtree aggregates.

**Patterns**:
- **ETT**: Represent a tree as its Euler tour sequence in a balanced BST (splay/treap). Inserting/deleting edges = sequence manipulations.
- **Top Trees**: Cluster-based tree decomposition supporting arbitrary path/subtree queries with lazy propagation on the cluster structure.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | [Dynamic Tree Subtree Sum](https://judge.yosupo.jp/problem/dynamic_tree_subtree_add_subtree_sum) | Library Checker | ETT/Top Tree |
| 2 | [Dynamic Tree Edge Set Path Composite](https://judge.yosupo.jp/problem/dynamic_tree_edge_set_path_composite) | Library Checker | ETT |
| 3 | [DYNACON1](https://www.spoj.com/problems/DYNACON1/) | SPOJ | Dynamic connectivity |
| 4 | [Dynamic Connectivity](https://cses.fi/problemset/task/2133) | CSES 2133 | Offline DSU / LCT |
| 5 | [Offline Dynamic Connectivity](https://judge.yosupo.jp/problem/dynamic_graph_vertex_add_component_sum) | Library Checker | ETT |

---

## 10.3 Palindromic Tree (Eertree) 🟠 P2

**Topics**: A tree of palindromic substrings. Each node represents a distinct palindromic substring. Built online in O(N).

**Patterns**:
- Two roots: one for odd-length palindromes, one for even-length.
- Each node has a suffix link (longest proper palindromic suffix).
- Total distinct palindromic substrings ≤ N+2.
- Useful for counting palindromic substrings, finding the longest palindromic substring ending at each position.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Eertree / Palindromic Tree](https://judge.yosupo.jp/problem/eertree) | Library Checker | Template |
| 2 | [Palindromic Characteristics](https://codeforces.com/problemset/problem/906/E) | CF 906E | Eertree |
| 3 | [Palindrome Pairs](https://leetcode.com/problems/palindrome-pairs/) | LC 336 | Eertree / hashing |
| 4 | [Palindromes (CF)](https://codeforces.com/problemset/problem/835/D) | CF 835D | Eertree |
| 5 | [A Lot of Palindromes](https://codeforces.com/problemset/problem/245/H) | CF 245H | Eertree / manacher |

---

## 10.4 Randomized Algorithms & Hashing Tricks 🟡 P3

**Topics**: Randomized hashing for collision avoidance, treaps, random sampling, probabilistic arguments in solutions, birthday paradox applications, anti-hash tests.

**Patterns**:
- **Treap**: Randomized BST. Expected O(log N) operations. Easy to implement split/merge.
- Use random bases for polynomial hashing to avoid anti-hash tests.
- Random sampling: if > 50% of elements satisfy a property, random sampling finds one in O(1) expected tries.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | [Treap](https://judge.yosupo.jp/problem/dynamic_sequence_range_affine_range_sum) | Library Checker | Implicit treap |
| 2 | [Insertion Sort](https://codeforces.com/problemset/problem/1045/G) | CF 1045G | Treap |
| 3 | [Array with Random Operations](https://codeforces.com/problemset/problem/1523/E) | CF 1523E | Randomized |
| 4 | [Test Generation](https://codeforces.com/problemset/problem/1523/D) | CF 1523D | Probability |
| 5 | [Implicit Key Treap](https://codeforces.com/edu/course/2/lesson/2) | CF EDU | Treap tutorial |

---

## 10.5 Subset Sum Convolution & Advanced Transforms 🟡 P3

**Topics**: Subset sum convolution (combining SOS with inclusion-exclusion), Mobius inversion on subsets, OR/AND convolution, advanced NTT applications.

**Patterns**:
- **Subset sum convolution**: h(S) = Σ_{T⊆S} f(T) · g(S\T). Computed in O(2^N · N^2) via "ranked" zeta/Mobius transform.
- OR convolution: h(S) = Σ_{A|B=S} f(A) · g(B). Computed via superset zeta transform + pointwise product + Mobius inversion.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Subset Sum Convolution](https://judge.yosupo.jp/problem/subset_convolution) | Library Checker | Template |
| 2 | [Bitwise AND Convolution](https://judge.yosupo.jp/problem/bitwise_and_convolution) | Library Checker | Template |
| 3 | [Bitwise OR Convolution](https://judge.yosupo.jp/problem/bitwise_or_convolution) | Library Checker | Template |
| 4 | [Square Root of FPS](https://judge.yosupo.jp/problem/sqrt_of_formal_power_series) | Library Checker | FPS |
| 5 | [Composition of FPS](https://judge.yosupo.jp/problem/composition_of_formal_power_series) | Library Checker | FPS |
| 6 | [XOR Convolution](https://judge.yosupo.jp/problem/bitwise_xor_convolution) | Library Checker | Walsh-Hadamard |

---

## 10.6 Miscellaneous Advanced & Research-Level 🟢 P4

**Topics**: Fractional cascading, wavelet tree, persistent arrays, succinct data structures, multi-dimensional range trees, kinetic data structures, offline-to-online reductions.

**Patterns**:
- **Wavelet tree**: Answers rank/select/quantile queries on sequences in O(log σ) where σ = alphabet size. Supports range k-th smallest, range frequency, etc.
- **Fractional cascading**: Speed up binary searches across multiple sorted lists from O(K log N) to O(K + log N).

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | [Range Kth Smallest](https://judge.yosupo.jp/problem/range_kth_smallest) | Library Checker | Wavelet tree |
| 2 | [Rectangle Sum](https://judge.yosupo.jp/problem/rectangle_sum) | Library Checker | 2D range tree |
| 3 | [Persistent Array](https://judge.yosupo.jp/problem/persistent_unionfind) | Library Checker | Persistent |
| 4 | [Range Frequency](https://judge.yosupo.jp/problem/static_range_frequency) | Library Checker | Wavelet tree |
| 5 | [Offline LCA](https://judge.yosupo.jp/problem/lca) | Library Checker | Tarjan offline |
| 6 | [Dynamic Minimum Spanning Forest](https://judge.yosupo.jp/problem/dynamic_graph_vertex_add_component_sum) | Library Checker | Advanced |

---

### Tier 10 Summary

| Priority | Topics Covered |
|----------|---------------|
| 🔴 P1 | Advanced Flow, Matroid Theory, General Matching |
| 🟠 P2 | Top Trees, Euler Tour Trees, Palindromic Tree |
| 🟡 P3 | Randomized Algorithms, Subset Sum Convolution |
| 🟢 P4 | Wavelet Trees, Fractional Cascading, Research-Level |

**Total problems in Tier 10: ~55**

> ✅ **Checkpoint**: You are among the best competitive programmers in the world. You can solve nearly any problem given enough time and can invent new techniques when needed.
