# Tier 8: Grandmaster (CF Rating 2400 – 2599)

> **Goal**: Network flow, FFT/NTT, advanced DP tricks (CHT, Alien's), Suffix Automaton. Problems regularly require combining 2–3 advanced techniques.

At this tier you enter the domain of elite competitive programmers. You master FFT/NTT for polynomial multiplication, advanced DP optimizations, min-cost flow, and combinatorial game theory. These topics appear in Div. 1 E and F problems. By the end of Tier 8 you will consistently solve Div. 1 D/E.

---

## 8.1 Max Flow & Min Cut [P1]

**Topics**: Ford-Fulkerson method, Edmonds-Karp (BFS-based, O(VE^2)), Dinic's algorithm (O(V^2·E)), Min-Cut Max-Flow theorem, modeling problems as flow networks.

**Patterns**:
- **Dinic's**: Builds level graph via BFS, finds blocking flows via DFS. Very fast in practice.
- **Min-Cut = Max-Flow**: The minimum set of edges to cut to disconnect source from sink = max flow value.
- Modeling: "choose one of two sides" → min-cut. Resource allocation → max flow.

**Classical Questions**: Maximum flow in a network, minimum cut, closure problem.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Download Speed](https://cses.fi/problemset/task/1694) | CSES 1694 | Max flow / Dinic |
| 2 | ★ [Police Chase](https://cses.fi/problemset/task/1695) | CSES 1695 | Min cut |
| 3 | [FASTFLOW](https://www.spoj.com/problems/FASTFLOW/) | SPOJ | Dinic stress test |
| 4 | [Escape (CF)](https://codeforces.com/problemset/problem/1082/G) | CF 1082G | Max flow |
| 5 | [Maximum Flow](https://judge.yosupo.jp/problem/maximum_flow) | Library Checker | Template |
| 6 | [School Dance](https://cses.fi/problemset/task/1696) | CSES 1696 | Bipartite matching |
| 7 | [Distinct Routes](https://cses.fi/problemset/task/1711) | CSES 1711 | Edge-disjoint paths |

---

## 8.2 Bipartite Matching [P1]

**Topics**: Maximum bipartite matching (Hopcroft-Karp O(E√V), Hungarian O(N^3)), König's theorem (min vertex cover = max matching in bipartite), Hall's theorem.

**Patterns**:
- **Hopcroft-Karp**: Multiple BFS phases + DFS to find augmenting paths. O(E√V).
- **König's theorem**: In bipartite graphs, max matching = min vertex cover.
- **Hall's theorem**: Perfect matching exists iff for every subset S of one side, |N(S)| ≥ |S|.

**Classical Questions**: Maximum number of job assignments, minimum vertex cover in bipartite.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [School Dance](https://cses.fi/problemset/task/1696) | CSES 1696 | Bipartite matching |
| 2 | [MATCHING - Fast Matching](https://www.spoj.com/problems/MATCHING/) | SPOJ | Hopcroft-Karp |
| 3 | [Maximum Matching](https://judge.yosupo.jp/problem/bipartitematching) | Library Checker | Template |
| 4 | [Course Schedule (Matching)](https://leetcode.com/problems/course-schedule/) | LC 207 | Matching variant |
| 5 | [Cats and Dogs](https://codeforces.com/problemset/problem/808/G) | CF 808G | Bipartite matching |
| 6 | [Distinct Routes](https://cses.fi/problemset/task/1711) | CSES 1711 | Edge-disjoint paths |
| 7 | [Distinct Routes II](https://cses.fi/problemset/task/2130) | CSES 2130 | Flow / matching |

---

## 8.3 FFT & NTT (Polynomial Multiplication) [P2]

**Topics**: Fast Fourier Transform for O(N log N) polynomial multiplication, Number Theoretic Transform (mod prime), convolution for counting problems.

**Patterns**:
- Polynomial multiplication: A(x)·B(x). Naively O(N^2), FFT makes it O(N log N).
- Convert coefficients → point values (FFT), multiply point-wise, convert back (inverse FFT).
- NTT: same as FFT but in modular arithmetic (using primitive roots mod prime like 998244353).
- "Count pairs summing to k" → coefficient of x^k in A(x)·B(x).

**Classical Questions**: Multiply two large numbers, count subset sums, polynomial convolution.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Apples and Bananas](https://cses.fi/problemset/task/2111) | CSES 2111 | FFT archetype |
| 2 | ★ [One Bit Positions](https://cses.fi/problemset/task/2112) | CSES 2112 | FFT / NTT |
| 3 | [POLYMUL - Polynomial Multiplication](https://www.spoj.com/problems/POLYMUL/) | SPOJ | FFT template |
| 4 | [Multiply Strings (FFT)](https://leetcode.com/problems/multiply-strings/) | LC 43 | Big number multiply |
| 5 | [Convolution mod](https://judge.yosupo.jp/problem/convolution_mod) | Library Checker | NTT template |
| 6 | [Moving Robots](https://cses.fi/problemset/task/1726) | CSES 1726 | Probability + FFT |
| 7 | [Kinematic Equation](https://codeforces.com/problemset/problem/438/E) | CF 438E | Generating functions |
| 8 | [Signal Processing](https://cses.fi/problemset/task/2113) | CSES 2113 | FFT |

---

## 8.4 Convex Hull Trick (CHT) [P2]

**Topics**: Optimizing DP of the form `dp[i] = min/max(m_j · x_i + b_j)` where lines `y = m_j·x + b_j` are added dynamically. Li Chao tree for arbitrary order.

**Patterns**:
- If slopes are monotonic, maintain a convex hull of lines and binary search. O(N log N) total.
- If queries' x-values are also monotonic, pointer trick gives O(N) total.
- **Li Chao tree**: handles arbitrary insertion order, queries by x-value. O(N log(range)).

**Classical Questions**: Minimizing `a_j · x_i + b_j` over DP transitions, line container.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Monster Game I](https://cses.fi/problemset/task/2084) | CSES 2084 | CHT |
| 2 | ★ [Monster Game II](https://cses.fi/problemset/task/2085) | CSES 2085 | Li Chao tree |
| 3 | [NKLEAVES - Leaves](https://www.spoj.com/problems/NKLEAVES/) | SPOJ | DP + CHT |
| 4 | [Kalila and Dimna](https://codeforces.com/problemset/problem/319/C) | CF 319C | CHT |
| 5 | [Frog 3](https://atcoder.jp/contests/dp/tasks/dp_z) | AtCoder DP-Z | CHT template |
| 6 | [Line Container](https://judge.yosupo.jp/problem/line_add_get_min) | Library Checker | CHT template |
| 7 | [Commando](https://dmoj.ca/problem/ioicommando) | IOI 2010 | CHT |

---

## 8.5 Suffix Automaton [P2]

**Topics**: Building a suffix automaton (DAWG) in O(N), counting distinct substrings, LCS of two strings, substring matching.

**Patterns**:
- Suffix automaton has at most 2N-1 states and 3N-4 transitions.
- Each state represents an equivalence class of substrings (same right extensions).
- Number of distinct substrings = Σ(len[v] - len[link[v]]) for all states v.
- LCS via suffix automaton: process second string on first string's SAM.

**Classical Questions**: Number of distinct substrings, longest common substring, lexicographic k-th substring.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [SUBLEX - Lex Substring Search](https://www.spoj.com/problems/SUBLEX/) | SPOJ | SAM archetype |
| 2 | [Distinct Substrings (SAM)](https://www.spoj.com/problems/DISUBSTR/) | SPOJ | SAM |
| 3 | [Suffix Automaton](https://judge.yosupo.jp/problem/number_of_substrings) | Library Checker | SAM template |
| 4 | [LCS2 - Longest Common Substring II](https://www.spoj.com/problems/LCS2/) | SPOJ | SAM multi-string |
| 5 | [Longest Common Substring](https://www.spoj.com/problems/LCS/) | SPOJ | SAM |
| 6 | [Good Substrings (CF)](https://codeforces.com/problemset/problem/271/D) | CF 271D | SAM / hash |
| 7 | [Repeat (CF)](https://codeforces.com/problemset/problem/1015/F) | CF 1015F | SAM |

---

## 8.6 Linear Algebra & Gaussian Elimination [P3]

**Topics**: Gaussian elimination over reals and GF(2) (XOR), solving systems of linear equations, matrix rank, determinant, linear basis (XOR basis).

**Patterns**:
- **XOR Basis / Linear Basis**: Represent numbers as vectors over GF(2). Build a basis of at most 60 elements (for 64-bit integers). The maximum XOR subset is found greedily.
- **Gaussian elimination**: O(N^3) for N equations. Over GF(2): O(N^2/32) with bitset.

**Classical Questions**: Max XOR of any subset, solving systems of XOR equations.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Ivan and Burgers](https://codeforces.com/problemset/problem/1100/F) | CF 1100F | Linear basis |
| 2 | [XOR Basis](https://judge.yosupo.jp/problem/xor_basis) | Library Checker | Template |
| 3 | [Maximum XOR Subarray](https://www.spoj.com/problems/XMAX/) | SPOJ | Linear basis |
| 4 | [Gaussian Elimination GF2](https://judge.yosupo.jp/problem/system_of_linear_equations) | Library Checker | Template |
| 5 | [XOR on Segment](https://codeforces.com/problemset/problem/1654/F) | CF 1654F | Basis + SegTree |
| 6 | [Maximum XOR of Two Numbers](https://leetcode.com/problems/maximum-xor-of-two-numbers-in-an-array/) | LC 421 | Trie / basis |
| 7 | [Check if There is a Valid Path](https://codeforces.com/problemset/problem/100/J) | CF | Gauss elim |
| 8 | [Determinant (Mod)](https://judge.yosupo.jp/problem/matrix_det) | Library Checker | Gauss |

---

## 8.7 Advanced Combinatorics [P3]

**Topics**: Burnside's lemma (counting under symmetry), Polya enumeration, Catalan numbers, Stirling numbers, advanced counting.

**Patterns**:
- **Burnside's lemma**: Number of distinct colorings = (1/|G|) · Σ|Fix(g)| over all symmetries g.
- **Catalan numbers**: C(n) = C(2n, n)/(n+1). Counts: balanced brackets, binary trees, non-crossing partitions, etc.
- **Stirling numbers** of 2nd kind S(n,k): partitioning n items into k non-empty subsets.

**Classical Questions**: Counting distinct necklaces under rotation, distributing objects into indistinguishable boxes.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Colorings (Burnside)](https://codeforces.com/problemset/problem/1474/F) | CF 1474F | Burnside |
| 2 | [Bracket Sequences I](https://cses.fi/problemset/task/2064) | CSES 2064 | Catalan |
| 3 | [Bracket Sequences II](https://cses.fi/problemset/task/2187) | CSES 2187 | Catalan variant |
| 4 | [Stirling Numbers 2nd](https://judge.yosupo.jp/problem/stirling_number_of_the_second_kind) | Library Checker | Template |
| 5 | [Counting Necklaces](https://cses.fi/problemset/task/2209) | CSES 2209 | Burnside |
| 6 | [Necklace (Burnside)](https://codeforces.com/problemset/problem/886/E) | CF 886E | Burnside |
| 7 | [Unique BSTs](https://leetcode.com/problems/unique-binary-search-trees/) | LC 96 | Catalan |

---

## 8.8 Min-Cost Max Flow (MCMF) [P4]

**Topics**: MCMF algorithms (SPFA-based, Bellman-Ford-based), modeling assignment/transportation problems as MCMF.

**Patterns**:
- Extend max flow to also minimize total cost. Each edge has both capacity and cost-per-unit-flow.
- Build flow network with costs. Use SPFA (or Bellman-Ford) for finding minimum cost augmenting paths.
- Applications: optimal assignment, transportation, weighted bipartite matching.

**Classical Questions**: Optimal job assignment with costs, minimum cost circulation.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Parcel Delivery](https://cses.fi/problemset/task/2121) | CSES 2121 | MCMF |
| 2 | [Task Assignment](https://cses.fi/problemset/task/2129) | CSES 2129 | MCMF |
| 3 | [Min Cost Flow](https://judge.yosupo.jp/problem/min_cost_b_flow) | Library Checker | MCMF template |
| 4 | [GREED (SPOJ)](https://www.spoj.com/problems/GREED/) | SPOJ | MCMF |
| 5 | [Cost Flow](https://codeforces.com/problemset/problem/164/C) | CF 164C | MCMF |
| 6 | [Minimum Cost to Buy Apples](https://leetcode.com/problems/minimum-cost-to-buy-apples/) | LC 2473 | MCMF / Dijkstra |

---

### Tier 8 Summary

| Priority | Topics Covered |
|----------|---------------|
| [P1] | Max Flow & Min Cut, Bipartite Matching |
| [P2] | FFT/NTT, Convex Hull Trick, Suffix Automaton |
| [P3] | Linear Algebra & Gauss, Advanced Combinatorics |
| [P4] | Min-Cost Max Flow |

**Total problems in Tier 8: ~90**

> [Checkpoint] **Checkpoint**: You can solve Div.1 D/E problems (2400–2600 rated). Flow networks, FFT, CHT, and suffix automatons are tools you reach for naturally.
