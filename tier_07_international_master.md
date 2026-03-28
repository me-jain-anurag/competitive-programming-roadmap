# Tier 7: International Master (CF Rating 2300 – 2399)

> **Goal**: Offline query techniques, advanced strings, advanced DP optimizations, and computational geometry foundations. Solve Div.1 C/D problems.

At this tier you master the most powerful tree decomposition techniques, advanced multi-pattern string matching, computational geometry, and DP speed-up tricks. These topics appear in Div. 1 D and E problems. By the end of Tier 7 you will consistently solve Div. 1 D and occasionally reach E.

---

## 7.1 Mo's Algorithm & Offline Queries [P1]

**Topics**: Mo's algorithm for offline range queries, block decomposition (√N), Mo's with updates, Mo's on trees.

**Patterns**:
- Sort queries by `(l / block, r)` where `block = √N`. Alternating sort order for R in odd blocks speeds things up.
- Maintain a "current answer" for range `[curL, curR]`. Extend/shrink by 1 element at a time.
- Total moves: O((N + Q)√N).
- Works for problems where you can add/remove elements from the current range efficiently.

**Classical Questions**: Count distinct in range, count of occurrences of each value, sum of squares of frequencies.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Distinct Values Queries](https://cses.fi/problemset/task/1734) | CSES 1734 | Mo's / offline BIT |
| 2 | ★ [D-query (Distinct Query)](https://www.spoj.com/problems/DQUERY/) | SPOJ DQUERY | Mo's archetype |
| 3 | ★ [Powerful Array](https://codeforces.com/problemset/problem/86/D) | CF 86D | Mo's |
| 4 | [XOR and Favorite Number](https://codeforces.com/problemset/problem/617/E) | CF 617E | Mo's + XOR |
| 5 | [Ynoi Easy Version](https://codeforces.com/problemset/problem/1311/F) | CF | Mo's advanced |
| 6 | [Jeff and Removing Periods](https://codeforces.com/problemset/problem/351/D) | CF 351D | Mo's + observation |
| 7 | [Little Elephant and Array](https://codeforces.com/problemset/problem/220/E) | CF 220E | Mo's |
| 8 | [FREQ2 - Frequency](https://www.spoj.com/problems/FREQ2/) | SPOJ | Mo's |
| 9 | [COT2 - Count on Tree](https://www.spoj.com/problems/COT2/) | SPOJ | Mo's on tree |
| 10 | [Path Queries](https://cses.fi/problemset/task/1138) | CSES 1138 | HLD / Euler Tour point updates |
| 11 | [Distinct Colors](https://cses.fi/problemset/task/1139) | CSES 1139 | Small-to-Large / Mo's on Trees |

---

## 7.2 Heavy-Light Decomposition (HLD) [P1]

**Topics**: Decomposing a tree into heavy chains, answering path queries with SegTree on chains, path updates.

**Patterns**:
- Decompose tree so that any root-to-leaf path crosses at most O(log N) chains.
- Each chain is a contiguous segment in an array → apply SegTree/BIT on that array.
- Path query (u,v): walk up chains to LCA, query each chain segment.
- Supports path sum, path max, path update, etc.

**Classical Questions**: Path max/sum queries, path updates on trees.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Path Queries II](https://cses.fi/problemset/task/2134) | CSES 2134 | HLD + SegTree |
| 2 | [QTREE - Query on a Tree](https://www.spoj.com/problems/QTREE/) | SPOJ QTREE | HLD archetype |
| 3 | [QTREE3](https://www.spoj.com/problems/QTREE3/) | SPOJ | HLD |
| 4 | [GOT - Gao on a Tree](https://www.spoj.com/problems/GOT/) | SPOJ | HLD / Euler Tour |
| 5 | [GRASSPLA](https://www.spoj.com/problems/GRASSPLA/) | SPOJ | HLD |
| 6 | [Vertex Set Path Composite](https://judge.yosupo.jp/problem/vertex_set_path_composite) | Library Checker | HLD template |
| 7 | [Max Flow on Tree](https://codeforces.com/problemset/problem/343/D) | CF 343D | HLD / Euler Tour |
| 8 | [New Roads Queries](https://cses.fi/problemset/task/2101) | CSES 2101 | Offline + DSU / HLD |

---

## 7.3 Persistent Data Structures [P2]

**Topics**: Persistent segment tree (version history), persistent trie, functional updates (create new version without modifying old).

**Patterns**:
- "Query the array as it was after operation i" → persistent seg tree.
- Each update creates O(log N) new nodes (path copying). Total memory: O(N log N + Q log N).
- k-th smallest in range [l, r]: persistent seg tree built from prefix frequency arrays.

**Classical Questions**: k-th smallest in arbitrary range, querying historical versions of an array.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Army Creation](https://codeforces.com/problemset/problem/813/E) | CF 813E | Persistent SegTree |
| 2 | [MKTHNUM - K-th Number](https://www.spoj.com/problems/MKTHNUM/) | SPOJ | Persistent SegTree |
| 3 | [COT - Count on a Tree](https://www.spoj.com/problems/COT/) | SPOJ | Persistent SegTree on tree |
| 4 | [Kth Smallest Element in Range](https://judge.yosupo.jp/problem/range_kth_smallest) | Library Checker | Persistent SegTree |
| 5 | [Persistent Segment Tree](https://judge.yosupo.jp/problem/persistent_unionfind) | Library Checker | Persistent DSU |
| 6 | [Lasting Sorting](https://codeforces.com/problemset/problem/1665/E) | CF 1665E | Persistent |
| 7 | [XOR on Segment](https://codeforces.com/problemset/problem/1654/F) | CF 1654F | Persistent trie |
| 8 | ★ [Counting Tilings](https://cses.fi/problemset/task/2181) | CSES 2181 | Broken Profile DP template |
| 9 | ★ [Giant Pizza](https://cses.fi/problemset/task/1684) | CSES 1684 | 2-SAT Formula constraint solver |

---

## 7.4 Divide & Conquer DP Optimization [P2]

**Topics**: Optimizing DP transitions from O(N^2) to O(N log N) when the optimal split point is monotonic (SMAWK / D&C optimization), Knuth's optimization.

**Patterns**:
- If `dp[i][j] = min over k in [0..j-1] of (dp[i-1][k] + cost(k+1, j))` and the optimal `k` for `dp[i][j]` ≤ optimal `k` for `dp[i][j+1]`, use D&C on the transition.
- Compute `dp[i][mid]` by checking only `k` in `[opt_lo, opt_hi]`, then recurse on left and right halves.
- **Knuth's optimization**: specific case where `cost` satisfies quadrangle inequality → O(N^2) from O(N^3).

**Classical Questions**: Breaking a string into pieces with minimum cost, partitioning array into K segments.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Kalila and Dimna](https://codeforces.com/problemset/problem/319/C) | CF 319C | DP optimization |
| 2 | [BRKSTRNG - Breaking String](https://www.spoj.com/problems/BRKSTRNG/) | SPOJ | Knuth optimization |
| 3 | [LARGEST - Largest Rectangle](https://www.spoj.com/problems/LARGEST/) | SPOJ | D&C |
| 4 | [Ciel and Gondola](https://codeforces.com/problemset/problem/321/E) | CF 321E | D&C DP |
| 5 | [Guards (IOI)](https://oj.uz/problem/view/APIO14_sequence) | APIO 2014 | D&C DP |
| 6 | [Optimal Binary Search Tree](https://judge.yosupo.jp/problem/optimal_binary_search_tree) | Library Checker | Knuth |

---

## 7.5 Suffix Array & LCP Array [P2]

**Topics**: Building suffix array in O(N log N) or O(N log^2 N), computing LCP array from suffix array (Kasai's algorithm), applications.

**Patterns**:
- Suffix array: sorted order of all suffixes. Enables binary search on suffixes.
- LCP array: `lcp[i]` = length of longest common prefix between suffix `sa[i]` and `sa[i-1]`.
- Number of distinct substrings = N(N+1)/2 - sum(lcp[i]).
- Pattern matching: binary search on suffix array in O(M log N).

**Classical Questions**: Number of distinct substrings, longest repeated substring, pattern matching.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [String Functions](https://cses.fi/problemset/task/2107) | CSES 2107 | Z/KMP |
| 2 | [Distinct Substrings](https://www.spoj.com/problems/DISUBSTR/) | SPOJ | Suffix array + LCP |
| 3 | [New Distinct Substrings](https://www.spoj.com/problems/SUBST1/) | SPOJ | Suffix array |
| 4 | [Suffix Array](https://judge.yosupo.jp/problem/suffixarray) | Library Checker | Template |
| 5 | [Number of Substrings](https://judge.yosupo.jp/problem/number_of_substrings) | Library Checker | SA + LCP |
| 6 | [Longest Duplicate Substring](https://leetcode.com/problems/longest-duplicate-substring/) | LC 1044 | SA / BS + hash |
| 7 | [Last Substring in Lex Order](https://leetcode.com/problems/last-substring-in-lexicographical-order/) | LC 1163 | Suffix array |
| 8 | [Repeats](https://www.spoj.com/problems/REPEATS/) | SPOJ | SA + LCP |

---

## 7.6 Aho-Corasick [P3]

**Topics**: Multi-pattern string matching, building an automaton from a dictionary of patterns, failure/suffix links.

**Patterns**:
- Build a trie of all patterns, then add failure links (BFS from root, similar to KMP failure function but on trie).
- Process the text through the automaton. At each node, follow suffix links to find all matching patterns.
- O(Σ|patterns| + |text| + matches).

**Classical Questions**: Find all occurrences of multiple patterns in a text, counting pattern matches.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [AHOCUR - Aho-Corasick](https://www.spoj.com/problems/AHOCUR/) | SPOJ | AC template |
| 2 | [Word Combinations](https://cses.fi/problemset/task/1731) | CSES 1731 | AC / DP |
| 3 | [Stream of Characters](https://leetcode.com/problems/stream-of-characters/) | LC 1032 | AC / reversed trie |
| 4 | [Multi-pattern Search](https://judge.yosupo.jp/problem/multipatternmatching) | Library Checker | AC template |
| 5 | [Ahocorasick](https://codeforces.com/problemset/problem/710/F) | CF 710F | AC + DP |
| 6 | [Forbidden Patterns](https://codeforces.com/problemset/problem/1400/F) | CF 1400F | AC application |
| 7 | [Finding Patterns](https://cses.fi/problemset/task/2102) | CSES 2102 | AC / hashing |

---

## 7.7 Computational Geometry Basics [P3]

**Topics**: Points, vectors, cross product, convex hull (Graham scan / Andrew's monotone chain), polygon area (Shoelace formula), point-in-polygon, line intersection.

**Patterns**:
- **Cross product** of vectors (A→B) × (A→C): positive = left turn, negative = right turn, zero = collinear.
- **Convex hull**: sort by x (break ties by y), build upper and lower hulls using cross product.
- **Shoelace formula**: Area = |Σ(x_i · y_{i+1} - x_{i+1} · y_i)| / 2.

**Classical Questions**: Convex hull, polygon area, checking if points are collinear.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Convex Hull](https://cses.fi/problemset/task/2195) | CSES 2195 | Graham/Andrew |
| 2 | ★ [Polygon Area](https://cses.fi/problemset/task/2191) | CSES 2191 | Shoelace formula |
| 3 | [Point Location Test](https://cses.fi/problemset/task/2189) | CSES 2189 | Cross product |
| 4 | [Line Segment Intersection](https://cses.fi/problemset/task/2190) | CSES 2190 | Geometry |
| 5 | [Polygon Lattice Points](https://cses.fi/problemset/task/2193) | CSES 2193 | Pick's theorem |
| 6 | [Point in Polygon](https://cses.fi/problemset/task/2192) | CSES 2192 | Ray casting |
| 7 | [Maximum Manhattan Distances](https://cses.fi/problemset/task/3410) | CSES 3410 | Geometry |
| 8 | [Erect the Fence](https://leetcode.com/problems/erect-the-fence/) | LC 587 | Convex hull |
| 9 | [Max Points on a Line](https://leetcode.com/problems/max-points-on-a-line/) | LC 149 | Slope counting |

---

## 7.8 Sweep Line [P3]

**Topics**: Line sweep for geometric problems, event-based processing, maintaining active set via balanced BST or segment tree.

**Patterns**:
- Sort events by x-coordinate (or time). Process events left to right.
- Maintain "active" elements in a data structure (set, multiset, SegTree).
- Common events: segment start/end, point query at a position.

**Classical Questions**: Skyline problem, counting rectangle overlaps, closest pair of points.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [The Skyline Problem](https://leetcode.com/problems/the-skyline-problem/) | LC 218 | Sweep line + multiset |
| 2 | [Area of Rectangles](https://cses.fi/problemset/task/1741) | CSES 1741 | Sweep + SegTree |
| 3 | [Room Allocation](https://cses.fi/problemset/task/1164) | CSES 1164 | Sweep / events |
| 4 | [Minimum Euclidean Distance](https://cses.fi/problemset/task/2194) | CSES 2194 | Sweep / D&C |
| 5 | [Car Fleet](https://leetcode.com/problems/car-fleet/) | LC 853 | Sort + sweep |
| 6 | [Intersection Points](https://cses.fi/problemset/task/1740) | CSES 1740 | Sweep |
| 7 | [Number of Flowers in Full Bloom](https://leetcode.com/problems/number-of-flowers-in-full-bloom/) | LC 2251 | Sweep / BS |

---

### Tier 7 Summary

| Priority | Topics Covered |
|----------|---------------|
| [P1] | Mo's Algorithm, Heavy-Light Decomposition |
| [P2] | Persistent Data Structures, D&C DP Optimization, Suffix Array |
| [P3] | Aho-Corasick, Computational Geometry, Sweep Line |

**Total problems in Tier 7: ~95**

> [Checkpoint] **Checkpoint**: You can solve Div.1 D problems (2300+ rated). Mo's, HLD, persistent seg trees, and suffix arrays are in your toolkit. You can combine sweep line with segment trees.
