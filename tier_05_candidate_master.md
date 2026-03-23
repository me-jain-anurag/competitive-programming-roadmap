# Tier 5: Candidate Master (CF Rating 1900 – 2099)

> **Goal**: Combine data structures with DP. Master segment trees, BIT, bitmask DP, digit DP, and tree algorithms. Solve Div.1 B problems.

At this tier you push into advanced algorithmic territory. You master bitmask DP, interval DP, and tree DP — the three DP paradigms that appear in nearly every hard contest problem. You learn sparse tables for O(1) RMQ, number theory tools (modular inverse, combinatorics, CRT), and the two most important string algorithms (KMP and Z-function). By the end of Tier 5 you will consistently solve Div. 1 B and occasionally reach C.

---

## 5.1 Segment Tree (Point Update, Range Query) 🔴 P1

**Topics**: Segment tree build, point update, range query (sum, min, max, GCD), iterative vs recursive implementation, coordinate compression with segment trees.

**Patterns**:
- Build in O(N), query and update in O(log N).
- Tree is stored in array of size 4N. Node `i` has children `2i` and `2i+1`.
- Range query: split range into O(log N) segments of the tree.
- Can answer any associative operation (sum, min, max, GCD, XOR, etc.).

**Classical Questions**: Dynamic range sum/min queries, range GCD queries.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Dynamic Range Sum Queries](https://cses.fi/problemset/task/1648) | CSES 1648 | SegTree template |
| 2 | ⭐ [Dynamic Range Minimum Queries](https://cses.fi/problemset/task/1649) | CSES 1649 | SegTree min |
| 3 | [Range Sum Query - Mutable](https://leetcode.com/problems/range-sum-query-mutable/) | LC 307 | SegTree / BIT |
| 4 | [Count of Smaller Numbers After Self](https://leetcode.com/problems/count-of-smaller-numbers-after-self/) | LC 315 | SegTree / BIT |
| 5 | [Hotel Queries](https://cses.fi/problemset/task/1143) | CSES 1143 | SegTree + walk |
| 6 | [List Removals](https://cses.fi/problemset/task/1749) | CSES 1749 | SegTree order statistics |
| 7 | [Salary Queries](https://cses.fi/problemset/task/1144) | CSES 1144 | SegTree + compression |
| 8 | [Range XOR Queries](https://cses.fi/problemset/task/1650) | CSES 1650 | Prefix XOR / SegTree |
| 9 | [Pizzeria Queries](https://cses.fi/problemset/task/2206) | CSES 2206 | SegTree |
| 10 | [GSS1 - Max Sum](https://www.spoj.com/problems/GSS1/) | SPOJ GSS1 | SegTree max subarray |
| 11 | [GSS3 - Max Sum with Updates](https://www.spoj.com/problems/GSS3/) | SPOJ GSS3 | SegTree + update |
| 12 | [My Calendar I](https://leetcode.com/problems/my-calendar-i/) | LC 729 | SegTree / balanced BST |

---

## 5.2 Binary Indexed Tree (Fenwick Tree) 🔴 P1

**Topics**: BIT for prefix sums with point updates, 2D BIT, order statistics with BIT, difference array + BIT for range update point query.

**Patterns**:
- BIT is simpler and faster than segment trees for prefix-sum-like operations.
- `update(i, delta)`: add delta at index i. `query(i)`: prefix sum up to index i. Both O(log N).
- Range sum `[l, r] = query(r) - query(l-1)`.
- For "count of elements ≤ x" type queries, use BIT over value domain.

**Classical Questions**: Dynamic prefix sums, counting inversions with BIT.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Dynamic Range Sum](https://cses.fi/problemset/task/1648) | CSES 1648 | BIT or SegTree |
| 2 | [Inversion Count (BIT)](https://www.spoj.com/problems/INVCNT/) | SPOJ | BIT approach |
| 3 | [Josephus Queries](https://cses.fi/problemset/task/2162) | CSES 2162 | BIT / simulation |
| 4 | [Nested Ranges Count](https://cses.fi/problemset/task/2169) | CSES 2169 | BIT + sort |
| 5 | [Nested Ranges Check](https://cses.fi/problemset/task/2168) | CSES 2168 | BIT + sort |
| 6 | [Count Good Triplets in Array](https://leetcode.com/problems/count-good-triplets-in-an-array/) | LC 2179 | BIT |
| 7 | [Reverse Pairs](https://leetcode.com/problems/reverse-pairs/) | LC 493 | BIT / merge sort |
| 8 | [UPDATEIT](https://www.spoj.com/problems/UPDATEIT/) | SPOJ | Range update + point query |

---

## 5.3 Bitmask DP 🔴 P1

**Topics**: DP where state includes a bitmask representing a subset of N ≤ 20 elements. TSP, assignment problems, Hamiltonian paths.

**Patterns**:
- State: `dp[mask]` or `dp[mask][last]` where `mask` indicates which elements are used.
- Transition: try adding each unused element. `dp[mask | (1<<j)][j] = dp[mask][i] + cost(i,j)`.
- Total states: O(2^N · N). Works for N ≤ 20 (2^20 ≈ 10^6).

**Classical Questions**: TSP, minimum cost assignment, Hamiltonian path counting.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Hamiltonian Flights](https://cses.fi/problemset/task/1690) | CSES 1690 | Bitmask DP |
| 2 | ⭐ [Elevator Rides](https://cses.fi/problemset/task/1653) | CSES 1653 | Bitmask DP |
| 3 | [Shortest Hamilton Walk](https://codeforces.com/problemset/problem/580/D) | CF 580D | Bitmask DP |
| 4 | [Shortest Superstring](https://leetcode.com/problems/find-the-shortest-superstring/) | LC 943 | TSP variant |
| 5 | [Partition to K Equal Sum Subsets](https://leetcode.com/problems/partition-to-k-equal-sum-subsets/) | LC 698 | Bitmask DP |
| 6 | [Maximum Students in Exam](https://leetcode.com/problems/maximum-students-taking-exam/) | LC 1349 | Bitmask DP |
| 7 | [Minimum XOR Sum of Two Arrays](https://leetcode.com/problems/minimum-xor-sum-of-two-arrays/) | LC 1879 | Assignment |
| 8 | [Can I Win](https://leetcode.com/problems/can-i-win/) | LC 464 | Bitmask game |
| 9 | [Traveling Salesman](https://www.spoj.com/problems/TVAC/) | SPOJ | TSP |
| 10 | [Matching](https://atcoder.jp/contests/dp/tasks/dp_o) | AtCoder DP-O | Assignment |

---

## 5.4 Tree DP 🟠 P2

**Topics**: DP on trees (rooted), computing subtree properties, diameter, max independent set, matching on trees.

**Patterns**:
- Root the tree at node 1. DFS from root, compute answers bottom-up.
- `dp[v]` depends on `dp[child]` for all children of v.
- Tree diameter: two BFS trick, or DP `dp[v] = max depth in subtree of v`, diameter = max over all v of `dp[left_child] + dp[right_child]`.

**Classical Questions**: Tree diameter, max weight independent set, tree matching.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Tree Diameter](https://cses.fi/problemset/task/1131) | CSES 1131 | DFS/BFS |
| 2 | ⭐ [Tree Matching](https://cses.fi/problemset/task/1130) | CSES 1130 | Tree DP |
| 3 | [Subordinates](https://cses.fi/problemset/task/1674) | CSES 1674 | Subtree size |
| 4 | [Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/) | LC 124 | Tree DP |
| 5 | [Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/) | LC 543 | Tree DP |
| 6 | [House Robber III](https://leetcode.com/problems/house-robber-iii/) | LC 337 | Tree DP |
| 7 | [Sum of Distances in Tree](https://leetcode.com/problems/sum-of-distances-in-tree/) | LC 834 | Re-rooting intro |
| 8 | [Tree Painting](https://usaco.org/index.php?page=viewproblem2&cpid=1193) | USACO Gold | Tree DP |
| 9 | [Barn Painting](https://usaco.org/index.php?page=viewproblem2&cpid=766) | USACO Gold | Tree DP |
| 10 | [Apple Tree](https://www.spoj.com/problems/PT07X/) | SPOJ PT07X | Max independent set |

---

## 5.5 LCA & Binary Lifting 🟠 P2

**Topics**: Lowest Common Ancestor computation, binary lifting (sparse table on tree), ancestor queries, path queries decomposition.

**Patterns**:
- **Binary Lifting**: Precompute `up[v][k]` = 2^k-th ancestor of v. LCA in O(log N) per query after O(N log N) preprocessing.
- To answer "distance between u and v on tree": `dist(u,v) = depth[u] + depth[v] - 2 * depth[LCA(u,v)]`.
- Euler Tour + Sparse Table gives O(1) LCA queries after O(N log N) preprocessing.

**Classical Questions**: LCA queries, k-th ancestor queries, path queries.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Company Queries I](https://cses.fi/problemset/task/1687) | CSES 1687 | Binary lifting |
| 2 | ⭐ [Company Queries II](https://cses.fi/problemset/task/1688) | CSES 1688 | LCA |
| 3 | [Distance Queries](https://cses.fi/problemset/task/1135) | CSES 1135 | LCA + depth |
| 4 | [Counting Paths](https://cses.fi/problemset/task/1136) | CSES 1136 | LCA + diff on tree |
| 5 | [LCA of Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/) | LC 236 | DFS |
| 6 | [Kth Ancestor of Tree Node](https://leetcode.com/problems/kth-ancestor-of-a-tree-node/) | LC 1483 | Binary lifting |
| 7 | [LCA (SPOJ)](https://www.spoj.com/problems/LCA/) | SPOJ LCA | LCA queries |
| 8 | [Milk Visits](https://usaco.org/index.php?page=viewproblem2&cpid=970) | USACO Gold | LCA |
| 9 | [Planets Queries I](https://cses.fi/problemset/task/1750) | CSES 1750 | Binary lifting (functional graph) |
| 10 | [Planets Queries II](https://cses.fi/problemset/task/1160) | CSES 1160 | Cycle + binary lifting |

---

## 5.6 Sparse Table & RMQ 🟡 P3

**Topics**: Sparse Table for O(1) range minimum/maximum queries (static), precomputation in O(N log N), idempotent operations.

**Patterns**:
- Works for idempotent operations (min, max, GCD, OR, AND) — where `f(a,a) = a`.
- `st[i][j]` = answer for range starting at index i with length 2^j.
- Query `[l,r]`: k = floor(log2(r-l+1)), answer = f(st[l][k], st[r-2^k+1][k]).
- Does NOT work for sum (not idempotent). Use BIT/SegTree for sum.

**Classical Questions**: Range Minimum Query (static), range GCD.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Static Range Min Queries](https://cses.fi/problemset/task/1647) | CSES 1647 | Sparse table |
| 2 | [RMQSQ](https://www.spoj.com/problems/RMQSQ/) | SPOJ | RMQ classic |
| 3 | [THRBL - Troublesome](https://www.spoj.com/problems/THRBL/) | SPOJ | Range max query |
| 4 | [Maximum of Minimums of Array](https://leetcode.com/problems/minimum-of-maximum-of-minimum-of-maximum/) | LC | Sparse table app |
| 5 | [Range XOR Queries](https://cses.fi/problemset/task/1650) | CSES 1650 | XOR is idempotent but note: typically BIT suffices |
| 6 | [Static RMQ](https://judge.yosupo.jp/problem/staticrmq) | Library Checker | Template verification |

---

## 5.7 Digit DP 🟡 P3

**Topics**: Counting numbers in range [L, R] satisfying some digit-based property. Tight/loose constraint, leading zeros handling.

**Patterns**:
- State: `dp[position][tight][...extra state]`.
  - `position`: current digit position being decided.
  - `tight`: whether we're still bounded by the upper limit.
  - Extra state: depends on problem (digit sum, last digit, count of some digit, etc.).
- Count for [L, R] = count for [0, R] - count for [0, L-1].

**Classical Questions**: Count numbers ≤ N without digit 4, count numbers with digit sum = S.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [LUCIFER - Lucifer Number](https://www.spoj.com/problems/LUCIFER/) | SPOJ | Digit DP intro |
| 2 | [Counting Numbers](https://cses.fi/problemset/task/2220) | CSES 2220 | Digit DP |
| 3 | [Numbers At Most N Given Digit Set](https://leetcode.com/problems/numbers-at-most-n-given-digit-set/) | LC 902 | Digit DP |
| 4 | [Count Numbers with Unique Digits](https://leetcode.com/problems/count-numbers-with-unique-digits/) | LC 357 | Digit DP / math |
| 5 | [Non-negative Integers without Consecutive Ones](https://leetcode.com/problems/non-negative-integers-without-consecutive-ones/) | LC 600 | Digit DP |
| 6 | [RAONE](https://www.spoj.com/problems/RAONE/) | SPOJ | Digit DP |
| 7 | [Digit Sum](https://www.spoj.com/problems/CPCRC1C/) | SPOJ | Digit DP |
| 8 | [Count of Integers](https://leetcode.com/problems/count-of-integers/) | LC 2719 | Digit DP |
| 9 | [Magic Number](https://codeforces.com/problemset/problem/628/D) | CF 628D | Digit DP |

---

## 5.8 Probability DP & Expected Value 🟡 P3

**Topics**: Expected value via DP, linearity of expectation, probability as DP state, Markov chains (simple).

**Patterns**:
- **Linearity of Expectation**: E[X+Y] = E[X] + E[Y], even when X and Y are NOT independent.
- Expected value DP: `E[state]` = sum over transitions of `probability * (cost + E[next_state])`.
- Coupon collector's problem: expected steps to collect all N types = N · H(N) ≈ N · ln(N).

**Classical Questions**: Expected dice rolls to reach a target, coupon collector.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Dice Probability](https://cses.fi/problemset/task/1725) | CSES 1725 | Probability DP |
| 2 | [Soup Servings](https://leetcode.com/problems/soup-servings/) | LC 808 | Probability DP |
| 3 | [Knight Probability in Chessboard](https://leetcode.com/problems/knight-probability-in-chessboard/) | LC 688 | Probability DP |
| 4 | [New 21 Game](https://leetcode.com/problems/new-21-game/) | LC 837 | Probability DP |
| 5 | [Random Pick with Weight](https://leetcode.com/problems/random-pick-with-weight/) | LC 528 | Prefix sum + BS |
| 6 | [Dice Expectations (CF)](https://codeforces.com/problemset/problem/453/A) | CF 453A | Expected value |
| 7 | [Cat and Mouse II](https://leetcode.com/problems/cat-and-mouse-ii/) | LC 1728 | Game + probability |

---

## 5.9 Monotonic Deque & Sliding Window Max/Min 🟢 P4

**Topics**: Sliding window maximum/minimum using deque, DP optimization with monotonic deque.

**Patterns**:
- Maintain a deque of indices where values are monotonically decreasing (for max) or increasing (for min).
- For each new element: pop from back while current ≤ back. Pop from front if out of window. Front = answer.
- Used to optimize DP transitions like `dp[i] = max(dp[j] + ...) for j in [i-k, i-1]`.

**Classical Questions**: Sliding window max, max sum subarray of size at most K.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/) | LC 239 | Deque template |
| 2 | [Sliding Cost](https://cses.fi/problemset/task/1077) | CSES 1077 | Two heaps + sliding |
| 3 | [Sliding Median](https://cses.fi/problemset/task/1076) | CSES 1076 | Two multisets |
| 4 | [Jump Game VI](https://leetcode.com/problems/jump-game-vi/) | LC 1696 | DP + deque |
| 5 | [Shortest Subarray with Sum ≥ K](https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/) | LC 862 | Deque + prefix sums |
| 6 | [Constrained Subsequence Sum](https://leetcode.com/problems/constrained-subsequence-sum/) | LC 1425 | DP + deque |
| 7 | [Max Value of Equation](https://leetcode.com/problems/max-value-of-equation/) | LC 1499 | Deque optimization |

---

## 5.10 Policy-Based Data Structures (PBDS) 🟢 P4

**Topics**: GNU `__gnu_pbds::tree` (ordered set / order statistics tree), finding k-th smallest element in O(log N), counting elements strictly less than X in O(log N), using PBDS as a replacement for balanced BSTs.

**Patterns**:
- `#include <ext/pb_ds/assoc_container.hpp>` and `#include <ext/pb_ds/tree_policy.hpp>`.
- `tree<int, null_type, less<int>, rb_tree_tag, tree_order_statistics_node_update>` — an ordered set with:
  - `find_by_order(k)` → iterator to k-th element (0-indexed).
  - `order_of_key(x)` → count of elements strictly less than x.
- To handle duplicates, use `tree<pair<int,int>, ...>` with unique second elements (e.g., index).
- Useful as a drop-in replacement when you need dynamic order statistics without implementing a full segment tree + coordinate compression.

**Classical Questions**: Dynamic k-th smallest, counting inversions online, rank queries.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [List Removals](https://cses.fi/problemset/task/1749) | CSES 1749 | Order statistics |
| 2 | ⭐ [Josephus Problem II](https://cses.fi/problemset/task/2163) | CSES 2163 | PBDS / SegTree |
| 3 | [Salary Queries](https://cses.fi/problemset/task/1144) | CSES 1144 | PBDS or SegTree+compress |
| 4 | [Inversion Count](https://www.spoj.com/problems/INVCNT/) | SPOJ | PBDS approach |
| 5 | [Count of Smaller Numbers After Self](https://leetcode.com/problems/count-of-smaller-numbers-after-self/) | LC 315 | PBDS / BIT / SegTree |
| 6 | [Kth Smallest Element in a Sorted Matrix](https://leetcode.com/problems/kth-smallest-element-in-a-sorted-matrix/) | LC 378 | Heap / PBDS |
| 7 | [Sliding Window Median](https://leetcode.com/problems/sliding-window-median/) | LC 480 | PBDS / two multisets |
| 8 | [Rank from Stream](https://leetcode.com/problems/rank-from-stream-lcci/) | LC | PBDS / BIT |
| 9 | [ORDERSET](https://www.spoj.com/problems/ORDERSET/) | SPOJ | PBDS archetype |
| 10 | [Nested Ranges Count](https://cses.fi/problemset/task/2169) | CSES 2169 | PBDS / BIT |

---

### Tier 5 Summary

| Priority | Topics Covered |
|----------|---------------|
| 🔴 P1 | Segment Tree, Fenwick Tree (BIT), Bitmask DP |
| 🟠 P2 | Tree DP, LCA & Binary Lifting |
| 🟡 P3 | Sparse Table, Digit DP, Probability DP |
| 🟢 P4 | Monotonic Deque, Policy-Based Data Structures (PBDS) |

**Total problems in Tier 5: ~118**

> ✅ **Checkpoint**: You can solve Div.1 B / Div.2 E problems (1900–2000 rated). Segment trees and bitmask DP are comfortable. You can implement LCA from scratch.
