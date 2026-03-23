# Tier 9: International Grandmaster (CF Rating 2600 – 2899)

> **Goal**: Mastery of advanced techniques. Alien's trick, generating functions, Link-Cut Trees, advanced geometry. Problems routinely require novel combinations of techniques or reading research papers.

At this tier you operate at the frontier of competitive programming. You master advanced geometry, persistent and specialized segment trees, randomized algorithms, and the most powerful string data structures. These topics appear in Div. 1 E and F problems and IOI/ICPC finals. By the end of Tier 9 you will be capable of solving the hardest problems in major contests.

---

## 9.1 Alien's Trick (Lambda / Lagrange Relaxation) 🔴 P1

**Topics**: Penalty-based optimization to remove a constraint (e.g., "use exactly K segments"), WQS binary search (Aliens trick), trading off a Lagrange multiplier.

**Patterns**:
- Problem: "Minimize cost using exactly K of something."
- Add a penalty λ for each unit used. Binary search on λ so that the unconstrained optimum uses exactly K units.
- The unconstrained problem (with penalty) is often much simpler (e.g., O(N) greedy instead of O(NK) DP).
- Key requirement: the answer must be convex/concave in K.

**Classical Questions**: IOI 2016 Aliens (minimum cost to cover points with K squares).

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Aliens (IOI)](https://oj.uz/problem/view/IOI16_aliens) | IOI 2016 | Alien's trick archetype |
| 2 | [Sequence (CF)](https://codeforces.com/problemset/problem/13/C) | CF 13C | WQS BS |
| 3 | [Lamps (CF)](https://codeforces.com/problemset/problem/1515/G) | CF 1515G | Alien |
| 4 | [Parallel Scheduling](https://codeforces.com/problemset/problem/802/O) | CF 802O | WQS BS |
| 5 | [Mowing the Lawn (IOI)](https://oj.uz/problem/view/IOI09_mowing) | IOI 2009 | DP + deque / WQS |
| 6 | [k-th Largest Area](https://codeforces.com/problemset/problem/1270/E) | CF 1270E | WQS related |

---

## 9.2 Generating Functions 🟠 P2

**Topics**: Ordinary generating functions (OGF), exponential generating functions (EGF), operations on formal power series (addition, multiplication, inversion, composition), solving recurrences via generating functions.

**Patterns**:
- OGF: A(x) = Σ a_n · x^n. Product of OGFs = convolution (FFT/NTT).
- Inverse: A(x)^(-1) computed via Newton's method in O(N log N).
- EGF: A(x) = Σ a_n · x^n / n!. Product corresponds to "labeled" combination.
- Partition function, Fibonacci closed form, derangement formula — all derivable via GFs.

**Classical Questions**: Computing partition numbers, composition of formal power series.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Kinematic Equation](https://codeforces.com/problemset/problem/438/E) | CF 438E | GF |
| 2 | [Inv of Formal Power Series](https://judge.yosupo.jp/problem/inv_of_formal_power_series) | Library Checker | Template |
| 3 | [Exp of Formal Power Series](https://judge.yosupo.jp/problem/exp_of_formal_power_series) | Library Checker | Template |
| 4 | [Log of Formal Power Series](https://judge.yosupo.jp/problem/log_of_formal_power_series) | Library Checker | Template |
| 5 | [Partition Function](https://judge.yosupo.jp/problem/partition_function) | Library Checker | GF application |
| 6 | [Trees (CF)](https://codeforces.com/problemset/problem/940/F) | CF 940F | EGF |
| 7 | [Subset Sum](https://judge.yosupo.jp/problem/sharp_p_subset_sum) | Library Checker | GF / NTT |

---

## 9.3 Link-Cut Trees 🟠 P2

**Topics**: Splay-tree-based dynamic forest structure. Supports cut, link, path queries, subtree queries — all in O(log N) amortized.

**Patterns**:
- **access(v)**: make v-to-root path a preferred path (single splay tree).
- **link(u, v)**: make v a child of u.
- **cut(u, v)**: remove edge (u, v).
- **path query**: access both endpoints, answer is in the splay tree.
- Used when edges are added/removed dynamically and you need path aggregates.

**Classical Questions**: Dynamic connectivity with path max, dynamic tree LCA.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Dynamic Connectivity](https://cses.fi/problemset/task/2133) | CSES 2133 | LCT / offline DSU |
| 2 | [Link-Cut Tree](https://judge.yosupo.jp/problem/dynamic_tree_vertex_add_path_sum) | Library Checker | LCT template |
| 3 | [Dynamic Tree Vertex Set Path Composite](https://judge.yosupo.jp/problem/dynamic_tree_vertex_set_path_composite) | Library Checker | LCT |
| 4 | [QTREE (Dynamic)](https://www.spoj.com/problems/QTREE/) | SPOJ | LCT |
| 5 | [OTOCI](https://www.spoj.com/problems/OTOCI/) | SPOJ | LCT |
| 6 | [Disconnected Graph](https://codeforces.com/problemset/problem/117/E) | CF 117E | LCT |

---

## 9.4 Lagrange Interpolation & Sum of Powers 🟡 P3

**Topics**: Given K+1 points, recover polynomial of degree K in O(K) or O(K log K). Computing Σi^k for i=1..N in O(K).

**Patterns**:
- **Lagrange interpolation**: P(x) = Σ y_i · Π(x - x_j) / Π(x_i - x_j) for j ≠ i.
- When x-values are 0, 1, 2, ..., K: simplify using prefix/suffix products. O(K) evaluation.
- Sum of k-th powers: S(n) = Σi^k is a polynomial of degree k+1 in n. Evaluate at k+2 points to interpolate.

**Classical Questions**: Sum of k-th powers for large N, evaluating a polynomial given by k+1 values.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Sum of k-th Powers](https://codeforces.com/problemset/problem/622/F) | CF 622F | Lagrange |
| 2 | [Polynomial Interpolation](https://judge.yosupo.jp/problem/polynomial_interpolation) | Library Checker | Template |
| 3 | [Multipoint Evaluation](https://judge.yosupo.jp/problem/multipoint_evaluate) | Library Checker | Template |
| 4 | [Xor-sequences](https://codeforces.com/problemset/problem/691/E) | CF 691E | Matrix exp + interpolation |
| 5 | [Highways](https://codeforces.com/problemset/problem/1142/E) | CF 1142E | Interpolation |
| 6 | [Bernoulli Sum](https://codeforces.com/problemset/problem/258/D) | CF 258D | Lagrange + number theory |

---

## 9.5 Advanced Computational Geometry 🟡 P3

**Topics**: Half-plane intersection, Minkowski sum, rotating calipers, Voronoi diagram intuition, line-point duality, advanced sweep line problems.

**Patterns**:
- **Rotating calipers**: Find furthest pair (diameter of convex hull) in O(N) after hull.
- **Half-plane intersection**: Intersection of half-planes = convex polygon. O(N log N) via sorting + deque.
- **Minkowski sum**: Sum of two convex polygons is a convex polygon. Computed in O(N+M).

**Classical Questions**: Width of a convex hull, maximum distance pair, visibility from a point.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Convex Hull](https://cses.fi/problemset/task/2195) | CSES 2195 | Convex hull |
| 2 | [Minimum Euclidean Distance](https://cses.fi/problemset/task/2194) | CSES 2194 | Closest pair |
| 3 | [All Manhattan Distances](https://cses.fi/problemset/task/3411) | CSES 3411 | Manhattan geometry |
| 4 | [Half-plane Intersection](https://judge.yosupo.jp/problem/convex_hull) | Library Checker | Template |
| 5 | [GCDSSQ](https://codeforces.com/problemset/problem/475/D) | CF 475D | Geometry + math |
| 6 | [Rotating Calipers](https://codeforces.com/problemset/problem/1189/D) | CF 1189D | Geometry |
| 7 | [Intersection of F(x)](https://www.spoj.com/problems/TLINE/) | SPOJ | Geometry |

---

## 9.6 Advanced Number Theory 🟡 P3

**Topics**: Pollard's Rho (factoring large numbers), Miller-Rabin primality test, Chinese Remainder Theorem (CRT), discrete logarithm (Baby-step Giant-step), primitive roots.

**Patterns**:
- **Miller-Rabin**: Probabilistic primality test in O(K log^2 N). Deterministic for N < 3.3·10^24 with specific witnesses.
- **Pollard's Rho**: Expected O(N^(1/4)) factorization.
- **CRT**: Combine congruences x ≡ a_i mod m_i (pairwise coprime) into x ≡ A mod (Πm_i).
- **BSGS**: Find x such that a^x ≡ b (mod p) in O(√p).

**Classical Questions**: Factorize a 10^18 number, solve modular equations.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Factorize](https://judge.yosupo.jp/problem/factorize) | Library Checker | Pollard's Rho |
| 2 | [Primality Test](https://judge.yosupo.jp/problem/primality_test) | Library Checker | Miller-Rabin |
| 3 | [Discrete Logarithm](https://judge.yosupo.jp/problem/discrete_logarithm_mod) | Library Checker | BSGS |
| 4 | [CRT (Chinese Remainder)](https://judge.yosupo.jp/problem/chinese_remainder) | Library Checker | CRT |
| 5 | [Primitive Root](https://judge.yosupo.jp/problem/primitive_root) | Library Checker | Template |
| 6 | [Big Primes](https://www.spoj.com/problems/BIGNUMS/) | SPOJ | Factorization |
| 7 | [Sum of Floor of Rationals](https://judge.yosupo.jp/problem/sum_of_floor_of_linear) | Library Checker | Number theory |

---

## 9.7 Sprague-Grundy Theory (Advanced) 🟢 P4

**Topics**: Grundy numbers (nimbers) for impartial games, computing Grundy values via mex, combining independent games via XOR of Grundy values, Green Hackenbush.

**Patterns**:
- **Grundy number** of a position = mex({Grundy(successor positions)}).
- mex(S) = smallest non-negative integer NOT in S.
- XOR of Grundy numbers of independent game components = Grundy number of the combined game.
- First player wins iff total Grundy ≠ 0.

**Classical Questions**: General nim-like games, turning turtles, graph games.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Grundy's Game](https://cses.fi/problemset/task/2207) | CSES 2207 | Grundy |
| 2 | [Nim Game III](https://cses.fi/problemset/task/2208) | CSES 2208 | Nim variant |
| 3 | [Another Game (CF)](https://codeforces.com/problemset/problem/850/C) | CF 850C | Game theory variant |
| 4 | [Game with string](https://codeforces.com/problemset/problem/155/B) | CF 155B | Grundy |
| 5 | [Green Hackenbush](https://codeforces.com/problemset/problem/850/C) | CF 850C | Nimber |
| 6 | [Treblecross](https://codeforces.com/problemset/problem/839/E) | CF 839E | Grundy + game |

---

### Tier 9 Summary

| Priority | Topics Covered |
|----------|---------------|
| 🔴 P1 | Alien's Trick (WQS Binary Search) |
| 🟠 P2 | Generating Functions, Link-Cut Trees |
| 🟡 P3 | Lagrange Interpolation, Advanced Geometry, Advanced Number Theory |
| 🟢 P4 | Sprague-Grundy Theory (Advanced) |

**Total problems in Tier 9: ~75**

> ✅ **Checkpoint**: You can solve Div.1 E/F problems. You read IOI/ICPC World Finals editorials comfortably. Almost any single technique is within reach.
