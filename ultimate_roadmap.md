# 🏆 The Ultimate Competitive Programming Roadmap

> A comprehensive, progressive guide from **Newbie** to **Legendary Grandmaster**.
> Complete with patterns, classical questions, priority rankings, and **~730 practice problems**
> cross-referenced from **Codeforces, CSES, LeetCode, SPOJ, USACO, AtCoder, and IOI/ICPC**.

---

## How to Use This Roadmap

| Symbol | Meaning |
|--------|---------|
| 🔴 **P1** | **Highest Priority** — Master this before moving on. |
| 🟠 **P2** | **High Priority** — Core topic, do after P1. |
| 🟡 **P3** | **Medium Priority** — Important but can be revisited. |
| 🟢 **P4** | **Lower Priority** — Niche or supplementary. |
| ⭐ | Especially classic / frequently tested problem. |

**Rule**: Problems in each section only require knowledge of topics from the current tier and all previous tiers.

---

## Tier Index (Matching Codeforces Titles Exactly)

| Tier | Title | CF Rating Range | File | Problems |
|------|-------|-----------------|------|----------|
| 1 | [**Newbie**](tier_01_newbie.md) | < 1200 | `tier_01_newbie.md` | ~99 |
| 2 | [**Pupil**](tier_02_pupil.md) | 1200 – 1399 | `tier_02_pupil.md` | ~89 |
| 3 | [**Specialist**](tier_03_specialist.md) | 1400 – 1599 | `tier_03_specialist.md` | ~99 |
| 4 | [**Expert**](tier_04_expert.md) | 1600 – 1899 | `tier_04_expert.md` | ~91 |
| 5 | [**Candidate Master**](tier_05_candidate_master.md) | 1900 – 2099 | `tier_05_candidate_master.md` | ~89 |
| 6 | [**Master**](tier_06_master.md) | 2100 – 2299 | `tier_06_master.md` | ~67 |
| 7 | [**International Master**](tier_07_international_master.md) | 2300 – 2399 | `tier_07_international_master.md` | ~61 |
| 8 | [**Grandmaster**](tier_08_grandmaster.md) | 2400 – 2599 | `tier_08_grandmaster.md` | ~57 |
| 9 | [**International Grandmaster**](tier_09_international_grandmaster.md) | 2600 – 2899 | `tier_09_international_grandmaster.md` | ~45 |
| 10 | [**Legendary Grandmaster**](tier_10_legendary_grandmaster.md) | 3000+ | `tier_10_legendary_grandmaster.md` | ~33 |
| | | | **Total** | **~730** |

---

## Topic Coverage by Tier

| Tier | Key Topics |
|------|------------|
| **1 — Newbie** | I/O, Math, Strings, Arrays, Sorting, Simulation, Recursion, Parity |
| **2 — Pupil** | Prefix Sums, Two Pointers, Stacks, Hash Maps, Binary Search, Number Theory, Brute Force |
| **3 — Specialist** | BS on Answer, Custom Sorting, BFS/DFS, Intro DP, Greedy, 2D DP, DSU, Meet-in-the-Middle |
| **4 — Expert** | Dijkstra/BF/Floyd, Knapsack, Topo Sort, MST, LIS/Interval DP, KMP/Trie, Combinatorics, Game Theory |
| **5 — Candidate Master** | Segment Tree, BIT, Bitmask DP, Tree DP, LCA, Sparse Table, Digit DP, Probability, PBDS |
| **6 — Master** | Lazy SegTree, Euler Tour, Re-rooting DP, SOS DP, SCCs/2-SAT, Inclusion-Exclusion, Matrix Exp, Centroid Decomp |
| **7 — Intl. Master** | Mo's Algorithm, HLD, Persistent SegTree, D&C DP, Suffix Array, Aho-Corasick, Geometry, Sweep Line |
| **8 — Grandmaster** | Max Flow, Bipartite Matching, FFT/NTT, CHT, Suffix Automaton, Linear Algebra, Burnside, MCMF |
| **9 — Intl. GM** | Alien's Trick, Generating Functions, Link-Cut Trees, Lagrange Interpolation, Advanced Geometry/NT, Sprague-Grundy |
| **10 — LGM** | General Matching, Matroid, Top Trees, Palindromic Tree, Treaps, Subset Sum Convolution, Wavelet Trees |

---

*Start from Tier 1 (Newbie) and work your way up. Do not skip tiers. Master P1 topics before P2, P2 before P3.*

# Tier 1: Newbie (CF Rating < 1200)

> **Goal**: Translate thoughts into code flawlessly. Learn basic complexities. Recognize the simplest patterns. Build the habit of reading constraints before thinking of an algorithm.

At this tier you are building the absolute foundations of competitive programming: reading and writing input/output efficiently, manipulating arrays and strings, applying elementary math, implementing basic sorting, and thinking recursively. By the end of Tier 1 you will be comfortable solving straightforward implementation problems, handling edge cases in simple loops, and writing clean brute-force solutions that pass within time limits on easy contests.

---

## 1.1 Basic I/O, Data Types & Control Flow [P1]

**Topics**: Fast I/O (`scanf/printf` or `ios::sync_with_stdio`), integer overflow awareness (`int` vs `long long`), loops, conditionals, basic type casting.

**Patterns**:
- Always check if the answer could exceed `2^31 – 1`; if so, use `long long`.
- Read the full input specification carefully — many WAs come from misread input.
- Use `'\n'` instead of `endl` for faster output.

**Classical Questions**: Read two numbers and print their sum, find the maximum of three numbers, check if a year is a leap year.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Watermelon](https://codeforces.com/problemset/problem/4/A) | CF 4A | Parity check |
| 2 | [Way Too Long Words](https://codeforces.com/problemset/problem/71/A) | CF 71A | String basics |
| 3 | [Team](https://codeforces.com/problemset/problem/231/A) | CF 231A | Simple counting |
| 4 | [Boy or Girl](https://codeforces.com/problemset/problem/236/A) | CF 236A | Set / distinct chars |
| 5 | [Wrong Subtraction](https://codeforces.com/problemset/problem/977/A) | CF 977A | Simulation loop |
| 6 | [Stones on the Table](https://codeforces.com/problemset/problem/266/A) | CF 266A | Adjacent comparison |
| 7 | ★ [Weird Algorithm](https://cses.fi/problemset/task/1068) | CSES 1068 | Simulation / overflow |
| 8 | [Missing Number](https://cses.fi/problemset/task/1083) | CSES 1083 | Sum formula |
| 9 | [Two Sum](https://leetcode.com/problems/two-sum/) | LC 1 | Hash map intro |
| 10 | [Fizz Buzz](https://leetcode.com/problems/fizz-buzz/) | LC 412 | Control flow |
| 11 | [Palindrome Number](https://leetcode.com/problems/palindrome-number/) | LC 9 | Reversal logic |
| 12 | [Theatre Square](https://codeforces.com/problemset/problem/1/A) | CF 1A | Ceiling division |
| 13 | [Football](https://codeforces.com/problemset/problem/96/A) | CF 96A | Counting consecutive |
| 14 | [Factorial](https://www.spoj.com/problems/FCTRL) | SPOJ | Trailing zeroes |

---

## 1.2 Simple Math & Number Properties [P1]

**Topics**: Divisibility, modular arithmetic basics, parity (odd/even), floor/ceil division, absolute value, basic formulas (sum of 1..N, area, etc.).

**Patterns**:
- `ceil(a/b)` for integers = `(a + b - 1) / b`.
- Parity of a sum depends only on the count of odd numbers.
- If constraints say N ≤ 10^6, an O(N) solution is fine; if N ≤ 10^3, O(N^2) is fine.

**Classical Questions**: Check if a number is even and > 2 (Watermelon), domino piling on a grid, compute GCD by hand.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Domino Piling](https://codeforces.com/problemset/problem/50/A) | CF 50A | floor(m*n/2) |
| 2 | [Beautiful Matrix](https://codeforces.com/problemset/problem/263/A) | CF 263A | Manhattan distance |
| 3 | [Even Odds](https://codeforces.com/problemset/problem/318/A) | CF 318A | Parity + formula |
| 4 | [Helpful Maths](https://codeforces.com/problemset/problem/339/A) | CF 339A | Parsing + sorting |
| 5 | [Number Spiral](https://cses.fi/problemset/task/1071) | CSES 1071 | Math / observation |
| 6 | ★ [Two Knights](https://cses.fi/problemset/task/1072) | CSES 1072 | Counting / inclusion |
| 7 | [Repetitions](https://cses.fi/problemset/task/1069) | CSES 1069 | Max consecutive |
| 8 | [Power of Two](https://leetcode.com/problems/power-of-two/) | LC 231 | Bit trick |
| 9 | [Excel Sheet Column Number](https://leetcode.com/problems/excel-sheet-column-number/) | LC 171 | Base conversion |
| 10 | [Subtract Product and Sum](https://leetcode.com/problems/subtract-the-product-and-sum-of-digits-of-an-integer/) | LC 1281 | Digit extraction |
| 11 | [Small Factors](https://usaco.org/index.php?page=viewproblem2&cpid=509) | USACO Bronze | Factor counting |
| 12 | [Test](https://www.spoj.com/problems/TEST/) | SPOJ TEST | Hello world of SPOJ |
| 13 | [Arpa's Hard Exam](https://codeforces.com/problemset/problem/742/A) | CF 742A | Pattern recognition |
| 14 | [The Useless Toy](https://codeforces.com/problemset/problem/834/A) | CF 834A | Rotation logic |
| 15 | [Prime Generator](https://www.spoj.com/problems/PRIME1) | SPOJ | Easy |

---

## 1.3 Basic Strings & Character Manipulation [P1]

**Topics**: String traversal, character comparison, ASCII values, substring extraction, string reversal, frequency counting with arrays.

**Patterns**:
- Use `s[i] - 'a'` to get 0-indexed position of lowercase chars.
- Frequency array of size 26 replaces hash maps for lowercase Latin letters.
- Always consider empty strings and single-character strings as edge cases.

**Classical Questions**: Check if a string is a palindrome, count vowels, reverse words.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Bit++](https://codeforces.com/problemset/problem/282/A) | CF 282A | String parsing |
| 2 | [Word](https://codeforces.com/problemset/problem/59/A) | CF 59A | Case counting |
| 3 | [String Task](https://codeforces.com/problemset/problem/118/A) | CF 118A | Char filtering |
| 4 | [Petya and Strings](https://codeforces.com/problemset/problem/112/A) | CF 112A | Lexicographic compare |
| 5 | [Increasing Array](https://cses.fi/problemset/task/1094) | CSES 1094 | Greedy / diff |
| 6 | [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/) | LC 125 | Two pointer + filter |
| 7 | [Reverse String](https://leetcode.com/problems/reverse-string/) | LC 344 | In-place reversal |
| 8 | [First Unique Character](https://leetcode.com/problems/first-unique-character-in-a-string/) | LC 387 | Frequency array |
| 9 | [Roman to Integer](https://leetcode.com/problems/roman-to-integer/) | LC 13 | Mapping logic |
| 10 | [Valid Anagram](https://leetcode.com/problems/valid-anagram/) | LC 242 | Frequency compare |
| 11 | [Palindromic String](https://www.spoj.com/problems/PALIN/) | SPOJ PALIN | Next palindrome |
| 12 | [cAPS lOCK](https://codeforces.com/problemset/problem/131/A) | CF 131A | Case transformation |
| 13 | [Implement strStr()](https://leetcode.com/problems/find-the-index-of-the-first-occurrence-in-a-string) | LC 28 | String matching |

---

## 1.4 Arrays, Sorting & Simple Searching [P2]

**Topics**: Array traversal, finding min/max, counting occurrences, built-in sort, custom comparators (conceptual), linear search, basic set usage.

**Patterns**:
- "Find the minimum/maximum" → single pass O(N).
- "Are there duplicates?" → sort then check adjacent, or use a set.
- "Find the k-th smallest" → sort then index.

**Classical Questions**: Find the second largest element, check if array is sorted, count frequency of each element.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Distinct Numbers](https://cses.fi/problemset/task/1621) | CSES 1621 | Sort or set |
| 2 | [Seats](https://codeforces.com/problemset/problem/6/A) | CF 6A | Triangle inequality |
| 3 | [Bear and Big Brother](https://codeforces.com/problemset/problem/791/A) | CF 791A | Simple simulation |
| 4 | [Elephant](https://codeforces.com/problemset/problem/617/A) | CF 617A | Ceil division |
| 5 | [Next Round](https://codeforces.com/problemset/problem/158/A) | CF 158A | Counting with threshold |
| 6 | [Permutations](https://cses.fi/problemset/task/1070) | CSES 1070 | Constructive |
| 7 | [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/) | LC 217 | Set / sort |
| 8 | [Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/) | LC 88 | Two pointer merge |
| 9 | [Majority Element](https://leetcode.com/problems/majority-element/) | LC 169 | Boyer-Moore or sort |
| 10 | [Missing Number](https://leetcode.com/problems/missing-number/) | LC 268 | XOR trick or sum |
| 11 | [Single Number](https://leetcode.com/problems/single-number/) | LC 136 | XOR |
| 12 | [Fence Painting](https://usaco.org/index.php?page=viewproblem2&cpid=567) | USACO Bronze | Interval overlap |
| 13 | [Ferris Wheel](https://cses.fi/problemset/task/1090) | CSES | Easy |
| 14 | [Second Order Statistics](https://codeforces.com/problemset/problem/22/A) | CF 22A | Second maximum |
| 15 | [Tram](https://codeforces.com/problemset/problem/116/A) | CF 116A | Running max |

---

## 1.5 Simulation & Ad-Hoc [P2]

**Topics**: Following problem statements exactly, game simulation, cycle detection in simulation, state tracking, matrix/grid traversal.

**Patterns**:
- When N is small (≤ 1000), just simulate step by step.
- If simulation runs for 10^9 steps, look for a cycle — states must eventually repeat.
- Grid problems: use `dx[], dy[]` arrays for 4 or 8 directions.

**Classical Questions**: Robot on a grid, simulate a card game, Collatz conjecture.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Buy a Shovel](https://codeforces.com/problemset/problem/732/A) | CF 732A | Modular cycle |
| 2 | [Die Roll](https://codeforces.com/problemset/problem/9/A) | CF 9A | Probability / counting |
| 3 | [Anton and Danik](https://codeforces.com/problemset/problem/734/A) | CF 734A | Counting wins |
| 4 | ★ [Spiral Matrix](https://leetcode.com/problems/spiral-matrix/) | LC 54 | Grid simulation |
| 5 | [Game of Life](https://leetcode.com/problems/game-of-life/) | LC 289 | Grid simulation |
| 6 | [Simulate Robot](https://leetcode.com/problems/robot-return-to-origin/) | LC 657 | Direction tracking |
| 7 | [Shell Game](https://usaco.org/index.php?page=viewproblem2&cpid=891) | USACO Bronze | Simulation |
| 8 | [Speeding](https://usaco.org/index.php?page=viewproblem2&cpid=568) | USACO Bronze | Segment simulation |
| 9 | [The Lost Cow](https://usaco.org/index.php?page=viewproblem2&cpid=735) | USACO Bronze | Simulation |
| 10 | [Set Matrix Zeroes](https://leetcode.com/problems/set-matrix-zeroes/) | LC 73 | In-place state |
| 11 | [Rotate Image](https://leetcode.com/problems/rotate-image/) | LC 48 | Matrix rotation |
| 12 | [Word Capitalization](https://codeforces.com/problemset/problem/281/A) | CF 281A | Simple string |
| 13 | [Drinks](https://codeforces.com/problemset/problem/200/B) | CF 200B | Average calculation |
| 14 | [Minimal Square](https://codeforces.com/problemset/problem/1360/A) | CF 1360A | Geometry / max |
| 15 | [King Escape](https://codeforces.com/problemset/problem/1033/A) | CF 1033A | Grid distance check |

---

## 1.6 Intro to Greedy Thinking [P3]

**Topics**: Making locally optimal choices, coin change with greedy (when valid), activity selection intuition, always pick the best available option.

**Patterns**:
- "Maximize the count of something" → often sort and pick greedily.
- "Minimize operations" → think about what the cheapest single operation is.
- Greedy only works when local optimum leads to global optimum — verify with small cases.

**Classical Questions**: Maximize coins collected, minimize moves to equalize, activity selection.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Young Physicist](https://codeforces.com/problemset/problem/69/A) | CF 69A | Vector sum = 0 |
| 2 | [Nearly Lucky Number](https://codeforces.com/problemset/problem/110/A) | CF 110A | Counting digits |
| 3 | [Insomnia cure](https://codeforces.com/problemset/problem/148/A) | CF 148A | Inclusion-exclusion lite |
| 4 | [Drinks](https://codeforces.com/problemset/problem/200/A) | CF 200A | Average |
| 5 | ★ [Apartments](https://cses.fi/problemset/task/1084) | CSES 1084 | Greedy / two pointer |
| 6 | [Lemonade Stand](https://leetcode.com/problems/lemonade-change/) | LC 860 | Greedy change-making |
| 7 | [Assign Cookies](https://leetcode.com/problems/assign-cookies/) | LC 455 | Sort + greedy |
| 8 | [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/) | LC 121 | Running min |
| 9 | [Best Time to Buy and Sell Stock II](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-ii/) | LC 122 | Greedy local gains |
| 10 | [Daisy](https://usaco.org/index.php?page=viewproblem2&cpid=1060) | USACO Bronze | Counting |
| 11 | [Maximum Units on a Truck](https://leetcode.com/problems/maximum-units-on-a-truck/) | LC 1710 | Sort + greedy |
| 12 | [Stick Lengths](https://cses.fi/problemset/task/1074) | CSES 1074 | Median minimizes sum |

---

## 1.7 Basic Recursion [P3]

**Topics**: Understanding the call stack, base cases, recursive thinking (break a problem into smaller identical sub-problems), simple recursive implementations.

**Patterns**:
- Every recursion needs a **base case** (when to stop) and a **recursive case** (how to reduce).
- "Compute f(n) using f(n-1)" is the simplest pattern.
- Recursion depth > ~10^4 can cause stack overflow — be aware.

**Classical Questions**: Factorial, Fibonacci, Tower of Hanoi, power function.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Power of Three](https://leetcode.com/problems/power-of-three/) | LC 326 | Recursive check |
| 2 | [Climbing Stairs](https://leetcode.com/problems/climbing-stairs/) | LC 70 | Fib recursion → DP |
| 3 | [Fibonacci Number](https://leetcode.com/problems/fibonacci-number/) | LC 509 | Classic recursion |
| 4 | [Pow(x, n)](https://leetcode.com/problems/powx-n/) | LC 50 | Fast power recursion |
| 5 | [Recursive Digit Sum](https://leetcode.com/problems/add-digits/) | LC 258 | Digital root |
| 6 | ★ [Tower of Hanoi](https://cses.fi/problemset/task/2165) | CSES 2165 | Classic recursion |
| 8 | [Apple Division](https://cses.fi/problemset/task/1623) | CSES 1623 | Brute force via recursion |

---

## 1.8 Parity, Invariants & Pigeonhole [P4]

**Topics**: Using parity (odd/even) arguments to prove impossibility, identifying quantities that never change under allowed operations, Pigeonhole principle for existence proofs.

**Patterns**:
- "Is it possible to reach state X?" → Check if some invariant (like parity of a sum, or XOR) is preserved.
- Chessboard coloring: placing a domino always covers one black and one white cell.
- Pigeonhole: N+1 items in N boxes → at least one box has ≥ 2 items.

**Classical Questions**: Tiling a chessboard with removed corners, swapping adjacent elements and parity of inversions.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Watermelon](https://codeforces.com/problemset/problem/4/A) | CF 4A | Parity |
| 2 | [Is it a Cube?](https://codeforces.com/problemset/problem/1619/A) | CF 1619A | Perfect cube check |
| 3 | [Valid Sudoku](https://leetcode.com/problems/valid-sudoku/) | LC 36 | State tracking / invariant |
| 4 | [Sum of Round Numbers](https://codeforces.com/problemset/problem/1352/A) | CF 1352A | Decomposition |
| 5 | [Parity Sort](https://codeforces.com/problemset/problem/1585/A) | CF 1585A | Parity invariant |
| 6 | [Permutations](https://cses.fi/problemset/task/1070) | CSES 1070 | Constructive |
| 7 | [Happy Number](https://leetcode.com/problems/happy-number/) | LC 202 | Cycle detection |
| 8 | [Distribute Candies](https://leetcode.com/problems/distribute-candies/) | LC 575 | Pigeonhole |

---

### Tier 1 Summary

| Priority | Topics Covered |
|----------|---------------|
| [P1] | I/O & Data Types, Simple Math, Basic Strings |
| [P2] | Arrays & Sorting, Simulation & Ad-Hoc |
| [P3] | Intro to Greedy, Basic Recursion |
| [P4] | Parity, Invariants & Pigeonhole |

**Total problems in Tier 1: ~99**

> [Checkpoint] **Checkpoint**: Before moving to Tier 2, you should be able to solve most CF Div.2 A problems (800-rated) within 10–15 minutes.

# Tier 2: Pupil (CF Rating 1200 – 1399)

> **Goal**: Solve most Div.2 A/B problems confidently. Build strong foundations in prefix sums, two pointers, basic binary search, and elementary number theory.

At this tier you move beyond raw implementation into algorithmic thinking. You learn to precompute range information with prefix sums, shrink search spaces with two pointers and sliding windows, make locally optimal choices with greedy strategies, binary search on sorted data, and traverse graphs with BFS and DFS. By the end of Tier 2 you will reliably solve Div. 2 A and B problems and occasionally crack C.

---

## 2.1 Prefix Sums & Difference Arrays [P1]

**Topics**: 1D prefix sums for O(1) range sum queries, 2D prefix sums for submatrix sums, difference arrays for O(1) range updates (bulk add).

**Patterns**:
- `prefix[i] = prefix[i-1] + a[i]`. Range sum `[l, r] = prefix[r] - prefix[l-1]`.
- Difference array: to add `val` to `[l, r]`, do `diff[l] += val; diff[r+1] -= val;` then take prefix sum of `diff`.
- 2D prefix sum: `P[i][j] = P[i-1][j] + P[i][j-1] - P[i-1][j-1] + a[i][j]`.

**Classical Questions**: Sum of a subarray/submatrix in O(1), applying K range updates efficiently.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Static Range Sum Queries](https://cses.fi/problemset/task/1646) | CSES 1646 | 1D prefix sum template |
| 2 | ★ [Forest Queries](https://cses.fi/problemset/task/1652) | CSES 1652 | 2D prefix sums |
| 3 | [Kuriyama Mirai's Stones](https://codeforces.com/problemset/problem/433/B) | CF 433B | Prefix sum + sorting |
| 4 | [Karen and Coffee](https://codeforces.com/problemset/problem/816/B) | CF 816B | Difference array |
| 5 | ★ [Corporate Flight Bookings](https://leetcode.com/problems/corporate-flight-bookings/) | LC 1109 | Difference array |
| 6 | [Range Sum Query 2D](https://leetcode.com/problems/range-sum-query-2d-immutable/) | LC 304 | 2D prefix sums |
| 7 | [Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/) | LC 560 | Prefix sum + hash map |
| 8 | [Little Girl and Maximum Sum](https://codeforces.com/problemset/problem/276/C) | CF 276C | Difference array |
| 9 | [Breed Counting](https://usaco.org/index.php?page=viewproblem2&cpid=572) | USACO Silver | Prefix sums |
| 10 | [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/) | LC 53 | Kadane / prefix min |
| 11 | [Contiguous Array](https://leetcode.com/problems/contiguous-array/) | LC 525 | Prefix sum + hash |
| 12 | [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/) | LC 238 | Prefix/suffix products |

---

## 2.2 Two Pointers & Sliding Window [P1]

**Topics**: Two pointers (same direction, opposite direction), fixed-size sliding window, variable-size sliding window (shrink when condition violated).

**Patterns**:
- Opposite pointers: start from both ends, move inward (e.g., `l=0, r=n-1`).
- Same direction: both start from left, right pointer expands, left shrinks (e.g., "longest substring with at most K distinct chars").
- Fixed window: maintain a window of size K, slide it across.

**Classical Questions**: Pair sum in sorted array, maximum sum subarray of size K, longest substring without repeating characters.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Books](https://codeforces.com/problemset/problem/279/B) | CF 279B | Sliding window |
| 2 | ★ [Container With Most Water](https://leetcode.com/problems/container-with-most-water/) | LC 11 | Opposite pointers |
| 3 | [Longest Substring Without Repeating](https://leetcode.com/problems/longest-substring-without-repeating-characters/) | LC 3 | Variable sliding window |
| 4 | [3Sum](https://leetcode.com/problems/3sum/) | LC 15 | Sort + two pointers |
| 5 | [Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/) | LC 128 | Hash set + expansion |
| 6 | [Sum of Two Values](https://cses.fi/problemset/task/1640) | CSES 1640 | Two pointers or hash |
| 7 | [Subarray Sum I](https://cses.fi/problemset/task/1660) | CSES 1660 | Sliding window |
| 8 | [Subarray Sum II](https://cses.fi/problemset/task/1661) | CSES 1661 | Prefix + binary search |
| 9 | [Minimum Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/) | LC 209 | Variable window |
| 10 | [Remove Duplicates from Sorted](https://leetcode.com/problems/remove-duplicates-from-sorted-array/) | LC 26 | Two pointers in-place |
| 11 | [Diamond Collector](https://usaco.org/index.php?page=viewproblem2&cpid=643) | USACO Silver | Sliding window |
| 12 | [Max Consecutive Ones III](https://leetcode.com/problems/max-consecutive-ones-iii/) | LC 1004 | Variable window |
| 13 | [Fruit Into Baskets](https://leetcode.com/problems/fruit-into-baskets/) | LC 904 | At most 2 distinct |

---

## 2.3 Stacks & Queues [P1]

**Topics**: Stack (LIFO), Queue (FIFO), monotonic stack (next greater/smaller element), matching brackets, expression evaluation.

**Patterns**:
- **Monotonic Stack**: To find "next greater element" for each position, iterate and maintain a stack of decreasing elements.
- **Bracket matching**: Push opening brackets, pop on matching closing bracket; if mismatch or stack non-empty at end → invalid.
- **Expression evaluation**: Two stacks (values + operators) or convert to postfix.

**Classical Questions**: Valid parentheses, next greater element, stock span, evaluate postfix.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/) | LC 20 | Stack template |
| 2 | ★ [Next Greater Element I](https://leetcode.com/problems/next-greater-element-i/) | LC 496 | Monotonic stack |
| 3 | [Daily Temperatures](https://leetcode.com/problems/daily-temperatures/) | LC 739 | Monotonic stack |
| 4 | [Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/) | LC 84 | Monotonic stack |
| 5 | [Min Stack](https://leetcode.com/problems/min-stack/) | LC 155 | Stack with min tracking |
| 6 | [Stock Span Problem](https://leetcode.com/problems/online-stock-span/) | LC 901 | Monotonic stack |
| 7 | [Nearest Smaller Values](https://cses.fi/problemset/task/1645) | CSES 1645 | Monotonic stack |
| 8 | ★ [Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/) | LC 42 | Monotonic stack / two-pass |
| 9 | [Odd Stack](https://www.spoj.com/problems/STPAR/) | SPOJ STPAR | Stack simulation |
| 10 | [Evaluate Reverse Polish Notation](https://leetcode.com/problems/evaluate-reverse-polish-notation/) | LC 150 | Stack evaluation |
| 11 | [Implement Queue using Stacks](https://leetcode.com/problems/implement-queue-using-stacks/) | LC 232 | Classical DS |
| 12 | [Asteroid Collision](https://leetcode.com/problems/asteroid-collision/) | LC 735 | Stack simulation |

---

## 2.4 Hash Maps & Frequency Counting [P2]

**Topics**: Hash maps for O(1) lookup, frequency counting, coordinate compression, detecting duplicates, grouping anagrams.

**Patterns**:
- "Does x exist?" → hash set.
- "How many times does x appear?" → hash map or frequency array.
- Coordinate compression: map large value range → contiguous indices using sorting + unique + map.

**Classical Questions**: Two Sum (hash map approach), group anagrams, first non-repeating character.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Two Sum](https://leetcode.com/problems/two-sum/) | LC 1 | Hash map classic |
| 2 | [Group Anagrams](https://leetcode.com/problems/group-anagrams/) | LC 49 | Hash map + sorting |
| 3 | [Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/) | LC 347 | Freq map + sort/bucket |
| 4 | [Intersection of Two Arrays II](https://leetcode.com/problems/intersection-of-two-arrays-ii/) | LC 350 | Freq map |
| 5 | [Sort Characters By Frequency](https://leetcode.com/problems/sort-characters-by-frequency/) | LC 451 | Freq map + sort |
| 6 | [Registration System](https://codeforces.com/problemset/problem/4/C) | CF 4C | Hash map |
| 7 | [Towers](https://cses.fi/problemset/task/1073) | CSES 1073 | Multiset / map |
| 8 | [Concert Tickets](https://cses.fi/problemset/task/1091) | CSES 1091 | Multiset operations |
| 9 | [Lucky Numbers](https://codeforces.com/problemset/problem/630/C) | CF 630C | Counting |
| 10 | [Jewels and Stones](https://leetcode.com/problems/jewels-and-stones/) | LC 771 | Hash set |
| 11 | ★ [Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/) | LC 128 | Hash set O(n) |

---

## 2.5 Basic Binary Search [P2]

**Topics**: Binary search on sorted arrays, `lower_bound`/`upper_bound`, finding first/last occurrence, counting elements in a range.

**Patterns**:
- **Template**: `lo = 0, hi = n-1; while(lo <= hi) { mid = (lo+hi)/2; ... }`
- `lower_bound(x)` → first position ≥ x.
- `upper_bound(x)` → first position > x.
- Count of `x` in sorted array = `upper_bound(x) - lower_bound(x)`.

**Classical Questions**: Find target in sorted array, find first/last position, search insert position.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Binary Search](https://leetcode.com/problems/binary-search/) | LC 704 | Template |
| 2 | ★ [First and Last Position](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/) | LC 34 | lower/upper bound |
| 3 | [Search Insert Position](https://leetcode.com/problems/search-insert-position/) | LC 35 | Lower bound |
| 4 | [Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/) | LC 74 | Flatten + BS |
| 5 | [Sqrt(x)](https://leetcode.com/problems/sqrtx/) | LC 69 | BS on answer intro |
| 6 | [T-primes](https://codeforces.com/problemset/problem/230/B) | CF 230B | Sieve + BS |
| 7 | [Distinct Numbers](https://cses.fi/problemset/task/1621) | CSES 1621 | Sort + distinct |
| 8 | [Aggressive Cows (Binary Search)](https://www.spoj.com/problems/AGGRCOW/) | SPOJ | BS on answer classic |
| 9 | [Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/) | LC 875 | BS on answer |
| 10 | [Social Distancing](https://usaco.org/index.php?page=viewproblem2&cpid=1038) | USACO Silver | BS on answer |

---

## 2.6 Basic Number Theory [P3]

**Topics**: Sieve of Eratosthenes, GCD (Euclidean algorithm), LCM, fast exponentiation (binary exponentiation), modular arithmetic, prime factorization.

**Patterns**:
- `gcd(a, b)` via Euclidean: `gcd(a, b) = gcd(b, a%b)`, base `gcd(a, 0) = a`.
- `lcm(a, b) = a / gcd(a, b) * b` (divide first to avoid overflow).
- Binary exponentiation: compute `a^n mod m` in O(log n).
- Sieve of Eratosthenes: find all primes up to N in O(N log log N).

**Classical Questions**: Check if prime, find all primes up to N, compute a^b mod m.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Exponentiation](https://cses.fi/problemset/task/1095) | CSES 1095 | Binary exponentiation |
| 2 | ★ [Counting Divisors](https://cses.fi/problemset/task/1713) | CSES 1713 | Sieve variant |
| 3 | [Count Primes](https://leetcode.com/problems/count-primes/) | LC 204 | Sieve |
| 4 | [Common Divisors](https://cses.fi/problemset/task/1081) | CSES 1081 | GCD / factor counting |
| 5 | [GCD of Array](https://leetcode.com/problems/find-greatest-common-divisor-of-array/) | LC 1979 | GCD basics |
| 6 | [Exponentiation II](https://cses.fi/problemset/task/1712) | CSES 1712 | Fermat's little theorem |
| 7 | [Modular Equations](https://codeforces.com/problemset/problem/495/B) | CF 495B | Modular arithmetic |
| 8 | [Sherlock and his GF](https://codeforces.com/problemset/problem/776/B) | CF 776B | Sieve + counting |
| 9 | [Almost Prime](https://codeforces.com/problemset/problem/26/A) | CF 26A | Sieve + factor count |
| 10 | [Noldbach Problem](https://codeforces.com/problemset/problem/17/A) | CF 17A | Sieve + checking |
| 11 | [Ugly Number](https://leetcode.com/problems/ugly-number/) | LC 263 | Prime factor check |
| 12 | [Perfect Number](https://leetcode.com/problems/perfect-number/) | LC 507 | Divisor sum |

---

## 2.7 Brute Force & Complete Search [P3]

**Topics**: Exhaustive enumeration, generating all possibilities (nested loops, bitmasks for small N), brute force with pruning.

**Patterns**:
- If N ≤ 20, you can enumerate all 2^N subsets using bitmasks.
- If N ≤ 8, you can enumerate all N! permutations.
- Always check constraints first: if N ≤ 10^3, O(N^2) brute force works.

**Classical Questions**: Enumerate all pairs, all subsets, all permutations for small N.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Subsets](https://leetcode.com/problems/subsets/) | LC 78 | Bitmask / backtracking |
| 2 | [Permutations](https://leetcode.com/problems/permutations/) | LC 46 | Backtracking |
| 3 | [Letter Combinations of Phone](https://leetcode.com/problems/letter-combinations-of-a-phone-number/) | LC 17 | Enumerate combos |
| 4 | ★ [Creating Strings](https://cses.fi/problemset/task/1622) | CSES 1622 | Generate permutations |
| 5 | ★ [Apple Division](https://cses.fi/problemset/task/1623) | CSES 1623 | 2^N subsets |
| 6 | [Chessboard and Queens](https://cses.fi/problemset/task/1624) | CSES 1624 | N-Queens variant |
| 7 | [Combination Sum](https://leetcode.com/problems/combination-sum/) | LC 39 | Backtracking |
| 8 | [Generate Parentheses](https://leetcode.com/problems/generate-parentheses/) | LC 22 | Backtracking |
| 9 | [Word Search](https://leetcode.com/problems/word-search/) | LC 79 | Grid backtracking |
| 10 | [N-Queens](https://leetcode.com/problems/n-queens/) | LC 51 | Classic backtracking |
| 11 | [Sudoku Solver](https://leetcode.com/problems/sudoku-solver/) | LC 37 | Backtracking + prune |
| 12 | [Grid Paths](https://cses.fi/problemset/task/1625) | CSES 1625 | Pruned brute force |
| 13 | ★ [Two Buttons](https://codeforces.com/problemset/problem/520/B) | CF 520B | BFS / reverse search |

---

## 2.8 Intro to Complexity & Strategy [P4]

**Topics**: Big-O notation intuition, reading constraints to pick algorithms, estimating runtime (10^8 operations ≈ 1 second), amortized analysis intro.

**Patterns**:
- N ≤ 10 → O(N!) or O(2^N) brute force.
- N ≤ 20 → O(2^N) or O(N^2 · 2^N) meet-in-the-middle.
- N ≤ 500 → O(N^3).
- N ≤ 5000 → O(N^2).
- N ≤ 10^5 → O(N log N) or O(N√N).
- N ≤ 10^6 → O(N) or O(N log N).
- N ≤ 10^9 → O(log N) or O(√N).

**Classical Questions**: "Given this constraint, what algorithm should I use?"

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | [Minimize Maximum Pair Sum](https://leetcode.com/problems/minimize-maximum-pair-sum-in-array/) | LC 1877 | O(N log N) sort |
| 2 | [Interesting Drink](https://codeforces.com/problemset/problem/706/B) | CF 706B | Sort + BS = O(N log N) |
| 3 | [Vanya and Lanterns](https://codeforces.com/problemset/problem/492/B) | CF 492B | Sort + max gap |
| 4 | [Sum of Three](https://codeforces.com/problemset/problem/1692/E) | CF 1692E | O(N) or O(N log N) |
| 5 | [Traffic Lights](https://cses.fi/problemset/task/1163) | CSES 1163 | Set operations |
| 6 | [Playlist](https://cses.fi/problemset/task/1141) | CSES 1141 | Sliding window |

---

### Tier 2 Summary

| Priority | Topics Covered |
|----------|---------------|
| [P1] | Prefix Sums & Difference Arrays, Two Pointers & Sliding Window, Stacks & Queues |
| [P2] | Hash Maps & Frequency Counting, Basic Binary Search |
| [P3] | Basic Number Theory, Brute Force & Complete Search |
| [P4] | Complexity Analysis & Strategy |

**Total problems in Tier 2: ~101**

> [Checkpoint] **Checkpoint**: You should be able to solve CF Div.2 B problems (1100–1200 rated) within 20 minutes. You know prefix sums, two pointers, and basic binary search cold.

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
| 5 | [Room Allocation](https://cses.fi/problemset/task/1164) | CSES 1164 | Event sorting + multiset |
| 6 | [Restaurant Customers](https://cses.fi/problemset/task/1619) | CSES 1619 | Event sorting |
| 7 | [Movie Festival](https://cses.fi/problemset/task/1629) | CSES 1629 | Activity selection |
| 8 | [Tasks and Deadlines](https://cses.fi/problemset/task/1630) | CSES 1630 | Sort by duration |
| 9 | [Queue at the School](https://codeforces.com/problemset/problem/266/B) | CF 266B | Bubble sort simulation |
| 10 | [Largest Number](https://leetcode.com/problems/largest-number/) | LC 179 | Custom comparator |
| 11 | [H-Index](https://leetcode.com/problems/h-index/) | LC 274 | Sort + count |

---

## 3.3 Graph Theory Fundamentals: BFS & DFS [P1]

**Topics**: Graph representation (adjacency list), BFS (shortest path in unweighted graphs), DFS (cycle detection, connected components), grid graphs, bipartite checking.

**Patterns**:
- **BFS** = level-order traversal, gives shortest distance in unweighted graphs.
- **DFS** = go deep, backtrack. Good for exploring all reachable nodes, finding connected components.
- Grid as graph: each cell (r,c) is a node, edges to 4/8 neighbors.
- **Bipartite check**: 2-color via BFS/DFS. If coloring fails → odd cycle → not bipartite.

**Classical Questions**: Shortest path in a maze, flood fill, number of islands, cycle detection.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Labyrinth](https://cses.fi/problemset/task/1193) | CSES 1193 | BFS shortest path |
| 2 | ★ [Building Roads](https://cses.fi/problemset/task/1666) | CSES 1666 | Connected components |
| 3 | [Number of Islands](https://leetcode.com/problems/number-of-islands/) | LC 200 | BFS/DFS flood fill |
| 4 | [Flood Fill](https://leetcode.com/problems/flood-fill/) | LC 733 | DFS |
| 5 | [Building Teams](https://cses.fi/problemset/task/1668) | CSES 1668 | Bipartite check |
| 6 | [Counting Rooms](https://cses.fi/problemset/task/1192) | CSES 1192 | Grid DFS/BFS |
| 7 | [Round Trip](https://cses.fi/problemset/task/1669) | CSES 1669 | Cycle detection |
| 8 | [Rotting Oranges](https://leetcode.com/problems/rotting-oranges/) | LC 994 | Multi-source BFS |
| 9 | [01 Matrix](https://leetcode.com/problems/01-matrix/) | LC 542 | Multi-source BFS |
| 10 | [Clone Graph](https://leetcode.com/problems/clone-graph/) | LC 133 | BFS/DFS |
| 11 | [Is Graph Bipartite?](https://leetcode.com/problems/is-graph-bipartite/) | LC 785 | 2-coloring |
| 12 | [Icy Perimeter](https://usaco.org/index.php?page=viewproblem2&cpid=895) | USACO Silver | BFS/DFS on grid |
| 13 | [Closing the Farm](https://usaco.org/index.php?page=viewproblem2&cpid=646) | USACO Silver | Reverse connectivity |
| 14 | [Course Schedule](https://leetcode.com/problems/course-schedule/) | LC 207 | Cycle detection (DAG) |

---

## 3.4 Intro to Dynamic Programming [P1]

**Topics**: 1D DP (Fibonacci-style recurrences, coin change), memoization vs tabulation, state definition, identifying overlapping subproblems.

**Patterns**:
- **State definition**: What information do I need to uniquely describe a subproblem? Usually the index and some capacity/budget.
- **Transition**: How do I build the answer for state `(i)` from smaller states?
- **Base case**: What's the answer for the smallest subproblem?
- Start by writing the recursive solution, then add memoization → then convert to bottom-up if needed.

**Classical Questions**: Fibonacci, climbing stairs, coin change (min coins, number of ways), house robber.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Dice Combinations](https://cses.fi/problemset/task/1633) | CSES 1633 | 1D DP template |
| 2 | ★ [Minimizing Coins](https://cses.fi/problemset/task/1634) | CSES 1634 | Coin change (min) |
| 3 | ★ [Coin Combinations I](https://cses.fi/problemset/task/1635) | CSES 1635 | Unbounded knapsack |
| 4 | [Coin Combinations II](https://cses.fi/problemset/task/1636) | CSES 1636 | Ordered vs unordered |
| 5 | [House Robber](https://leetcode.com/problems/house-robber/) | LC 198 | 1D DP classic |
| 6 | [House Robber II](https://leetcode.com/problems/house-robber-ii/) | LC 213 | Circular variant |
| 7 | [Climbing Stairs](https://leetcode.com/problems/climbing-stairs/) | LC 70 | Fibonacci DP |
| 8 | [Min Cost Climbing Stairs](https://leetcode.com/problems/min-cost-climbing-stairs/) | LC 746 | 1D DP |
| 9 | [Decode Ways](https://leetcode.com/problems/decode-ways/) | LC 91 | 1D DP |
| 10 | [Removing Digits](https://cses.fi/problemset/task/1637) | CSES 1637 | DP / greedy |
| 11 | [Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/) | LC 300 | LIS classic |
| 12 | [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/) | LC 53 | Kadane's DP |
| 13 | [Fence Painting](https://usaco.org/index.php?page=viewproblem2&cpid=1173) | USACO Silver | DP |
| 14 | [Alphacode](https://www.spoj.com/problems/ACODE/) | SPOJ ACODE | Decode DP |

---

## 3.5 Greedy Algorithms (Intermediate) [P2]

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

## 3.6 2D DP & Grid DP [P2]

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
| 3 | ★ [Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/) | LC 1143 | LCS |
| 4 | [Unique Paths](https://leetcode.com/problems/unique-paths/) | LC 62 | Grid counting |
| 5 | [Unique Paths II](https://leetcode.com/problems/unique-paths-ii/) | LC 63 | With obstacles |
| 6 | [Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/) | LC 64 | Grid min cost |
| 7 | [Edit Distance](https://leetcode.com/problems/edit-distance/) | LC 72 | Classic |
| 8 | [Interleaving String](https://leetcode.com/problems/interleaving-string/) | LC 97 | 2D DP |
| 9 | [Distinct Subsequences](https://leetcode.com/problems/distinct-subsequences/) | LC 115 | 2D DP |
| 10 | [Max Square](https://leetcode.com/problems/maximal-square/) | LC 221 | Grid DP |
| 11 | [Palindrome Substrings](https://leetcode.com/problems/palindromic-substrings/) | LC 647 | 2D DP / expand |
| 12 | [Money Sums](https://cses.fi/problemset/task/1745) | CSES 1745 | Subset sum DP |

---

## 3.7 Union-Find (DSU) [P3]

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

## 3.8 Constructive Algorithms & Observations [P3]

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

# Tier 4: Expert (CF Rating 1600 – 1899)

> **Goal**: Confidently solve Div.2 D / Div.1 A. Master intermediate DP variants, shortest-path algorithms, segment trees, and string matching.

At this tier you move from graph traversal into weighted graphs and range-query data structures. You master shortest-path algorithms, minimum spanning trees, monotonic structures for O(n) range queries, and the two most important point-update data structures: Segment Trees and Fenwick Trees. By the end of Tier 4 you will consistently solve Div. 2 D problems and occasionally reach E.

---

## 4.1 Shortest Path Algorithms [P1]

**Topics**: Dijkstra's algorithm (priority queue), 0-1 BFS (deque), Bellman-Ford (negative edges, negative cycle detection), Floyd-Warshall (all-pairs), SPFA.

**Patterns**:
- **Dijkstra**: Non-negative weights only. O((V+E) log V) with priority queue. Always use `dist[u] < current` check for lazy deletion.
- **0-1 BFS**: Weights are 0 or 1. Use deque — push 0-weight to front, 1-weight to back. O(V+E).
- **Bellman-Ford**: Handles negative weights. O(VE). Run V-th iteration to detect negative cycles.
- **Floyd-Warshall**: All-pairs shortest path in O(V^3). V ≤ 500.

**Classical Questions**: Shortest path in a weighted graph, finding negative cycles, minimum cost grid path with 0/1 weights.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Shortest Routes I](https://cses.fi/problemset/task/1671) | CSES 1671 | Dijkstra template |
| 2 | ★ [Shortest Routes II](https://cses.fi/problemset/task/1672) | CSES 1672 | Floyd-Warshall |
| 3 | [High Score](https://cses.fi/problemset/task/1673) | CSES 1673 | Bellman-Ford / neg cycle |
| 4 | [Cycle Finding](https://cses.fi/problemset/task/1197) | CSES 1197 | Bellman-Ford |
| 5 | ★ [Min Cost Valid Path](https://leetcode.com/problems/minimum-cost-to-make-at-least-one-valid-path-in-a-grid/) | LC 1368 | 0-1 BFS |
| 6 | [Network Delay Time](https://leetcode.com/problems/network-delay-time/) | LC 743 | Dijkstra |
| 7 | [Cheapest Flights Within K Stops](https://leetcode.com/problems/cheapest-flights-within-k-stops/) | LC 787 | Modified BF / Dijkstra |
| 8 | [Path With Minimum Effort](https://leetcode.com/problems/path-with-minimum-effort/) | LC 1631 | Dijkstra / BS+BFS |
| 9 | [Swim in Rising Water](https://leetcode.com/problems/swim-in-rising-water/) | LC 778 | Dijkstra on grid |
| 10 | [Flight Discount](https://cses.fi/problemset/task/1195) | CSES 1195 | Layered Dijkstra |
| 11 | [Investigation](https://cses.fi/problemset/task/1202) | CSES 1202 | Dijkstra + counting |
| 12 | [Shortest Path (SPOJ)](https://www.spoj.com/problems/SHPATH/) | SPOJ SHPATH | Dijkstra |

---

## 4.2 Knapsack & Subset DP [P1]

**Topics**: 0/1 Knapsack, unbounded knapsack, bounded knapsack, subset sum, counting subsets, DP over subsets (bitmask DP intro).

**Patterns**:
- **0/1 Knapsack**: `dp[i][w] = max value using first i items with capacity w`. Space optimize to 1D by iterating w in reverse.
- **Unbounded**: iterate w forward (items can be reused).
- **Bitmask DP**: State is a bitmask representing which elements are "used". Works for N ≤ 20.

**Classical Questions**: Classic knapsack, partition into two equal-sum subsets, minimum difference partition.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Book Shop](https://cses.fi/problemset/task/1158) | CSES 1158 | 0/1 Knapsack |
| 2 | ★ [Money Sums](https://cses.fi/problemset/task/1745) | CSES 1745 | Subset sum DP |
| 3 | [Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum/) | LC 416 | Subset sum |
| 4 | [Target Sum](https://leetcode.com/problems/target-sum/) | LC 494 | Subset sum variant |
| 5 | [Coin Change](https://leetcode.com/problems/coin-change/) | LC 322 | Unbounded knapsack |
| 6 | [Coin Change II](https://leetcode.com/problems/coin-change-ii/) | LC 518 | Counting ways |
| 7 | [Ones and Zeroes](https://leetcode.com/problems/ones-and-zeroes/) | LC 474 | 2D Knapsack |
| 8 | [Last Stone Weight II](https://leetcode.com/problems/last-stone-weight-ii/) | LC 1049 | Min diff partition |
| 9 | ★ [Elevator Rides](https://cses.fi/problemset/task/1653) | CSES 1653 | Bitmask DP |
| 10 | [Two Sets II](https://cses.fi/problemset/task/1093) | CSES 1093 | Subset sum count |
| 11 | [KNAPSACK - The Knapsack Problem](https://www.spoj.com/problems/KNAPSACK/) | SPOJ | Classic knapsack |
| 12 | [Profitable Schemes](https://leetcode.com/problems/profitable-schemes/) | LC 879 | 2D knapsack |

---

## 4.3 Topological Sort & DAG DP [P1]

**Topics**: Topological ordering (Kahn's BFS / DFS-based), DP on DAGs (longest path, counting paths), detecting if a graph is a DAG.

**Patterns**:
- **Kahn's algorithm**: Start with nodes of in-degree 0, push to queue, process and reduce in-degrees.
- **DP on DAG**: Process nodes in topological order. `dp[v] = best over all predecessors u + edge(u,v)`.
- Longest path in a DAG is solvable in O(V+E) (unlike general graphs which are NP-hard).

**Classical Questions**: Course ordering, longest path in a DAG, counting paths from source to sink.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Course Schedule II](https://leetcode.com/problems/course-schedule-ii/) | LC 210 | Topo sort |
| 2 | ★ [Longest Flight Route](https://cses.fi/problemset/task/1680) | CSES 1680 | DAG DP |
| 3 | [Game Routes](https://cses.fi/problemset/task/1681) | CSES 1681 | Count paths in DAG |
| 4 | [Fox And Names](https://codeforces.com/problemset/problem/510/C) | CF 510C | Topo sort from constraints |
| 5 | [Sort Items by Groups](https://leetcode.com/problems/sort-items-by-groups-respecting-dependencies/) | LC 1203 | Multi-level topo sort |
| 6 | [Minimum Height Trees](https://leetcode.com/problems/minimum-height-trees/) | LC 310 | Topo-like peeling |
| 7 | [Toposort](https://www.spoj.com/problems/TOPOSORT/) | SPOJ | Topo sort |
| 8 | [Course Schedule IV](https://leetcode.com/problems/course-schedule-iv/) | LC 1462 | Topo + reachability |
| 9 | [Milking Order](https://usaco.org/index.php?page=viewproblem2&cpid=838) | USACO Gold | Topo sort |

---

## 4.4 MST & Advanced Graph Concepts [P2]

**Topics**: Kruskal's algorithm (with DSU), Prim's algorithm, properties of MST, Eulerian paths/circuits (Hierholzer's algorithm), bridges and articulation points.

**Patterns**:
- **Kruskal's**: Sort edges by weight, add if it doesn't form a cycle (check via DSU). O(E log E).
- **Eulerian circuit** exists iff all vertices have even degree (undirected) or in-degree = out-degree (directed).
- **Bridges**: edges whose removal increases connected components. Found via Tarjan's DFS with discovery/low values.

**Classical Questions**: Minimum spanning tree, finding bridges, Euler tour.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Road Reparation](https://cses.fi/problemset/task/1675) | CSES 1675 | MST / Kruskal |
| 2 | ★ [Mail Delivery](https://cses.fi/problemset/task/1691) | CSES 1691 | Euler circuit |
| 3 | [De Bruijn Sequence](https://cses.fi/problemset/task/1692) | CSES 1692 | Euler path |
| 4 | [Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/) | LC 1584 | MST / Prim |
| 5 | [Critical Connections](https://leetcode.com/problems/critical-connections-in-a-network/) | LC 1192 | Bridges / Tarjan |
| 6 | [Fine Dining](https://usaco.org/index.php?page=viewproblem2&cpid=861) | USACO Gold | MST variant |
| 7 | [MST (SPOJ)](https://www.spoj.com/problems/MST/) | SPOJ MST | Kruskal |
| 8 | [Reconstruct Itinerary](https://leetcode.com/problems/reconstruct-itinerary/) | LC 332 | Euler path |
| 9 | [Teleporters Path](https://cses.fi/problemset/task/1693) | CSES 1693 | Euler path directed |
| 10 | [Redundant Connection II](https://leetcode.com/problems/redundant-connection-ii/) | LC 685 | Directed MST/DSU |

---

## 4.5 Intermediate DP: LIS, Intervals & Ranges [P2]

**Topics**: Longest Increasing Subsequence (O(N log N)), interval DP, range DP, 1D DP with binary search optimization.

**Patterns**:
- **LIS in O(N log N)**: Maintain a `tails` array; for each element, binary search for the position to insert/replace.
- **Interval DP**: `dp[l][r]` = answer for the subproblem `[l, r]`. Try all split points k in `[l, r-1]`.
- "Merging adjacent elements optimally" → interval DP.

**Classical Questions**: LIS, matrix chain multiplication, optimal BST, burst balloons.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/) | LC 300 | LIS O(N log N) |
| 2 | ★ [Burst Balloons](https://leetcode.com/problems/burst-balloons/) | LC 312 | Interval DP |
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

## 4.6 String Algorithms: KMP, Hashing & Trie [P2]

**Topics**: KMP failure function & pattern matching, string hashing (rolling hash / Rabin-Karp), Trie data structure, Z-algorithm.

**Patterns**:
- **KMP**: Precompute failure function in O(M), then match in O(N). Total O(N+M).
- **Rolling Hash**: Hash a substring in O(1) after O(N) prep. Compare substrings by hash (with collision risk).
- **Trie**: Tree of characters for prefix queries. O(L) insert/search where L = string length.
- **Z-array**: `z[i]` = length of longest substring starting at `i` that matches a prefix of the string.

**Classical Questions**: Pattern matching, finding all occurrences, autocomplete with Trie, longest common prefix.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [String Matching](https://cses.fi/problemset/task/1753) | CSES 1753 | KMP / Z / Hashing |
| 2 | ★ [Implement Trie](https://leetcode.com/problems/implement-trie-prefix-tree/) | LC 208 | Trie template |
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

## 4.7 Combinatorics & Modular Inverse [P3]

**Topics**: nCr mod p (using factorials + modular inverse), Pascal's triangle, Stars and Bars, Fermat's little theorem, Wilson's theorem.

**Patterns**:
- Precompute `fact[i]` and `inv_fact[i]` up to N using modular inverse. Then `nCr(n,r) = fact[n] * inv_fact[r] % mod * inv_fact[n-r] % mod`.
- **Modular inverse**: `a^(-1) mod p = a^(p-2) mod p` when p is prime (Fermat's little theorem).
- **Stars and Bars**: Distributing n identical items into k distinct bins = C(n+k-1, k-1).

**Classical Questions**: Counting paths on grid with obstacles, distributing items, nCr queries.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Binomial Coefficients](https://cses.fi/problemset/task/1079) | CSES 1079 | nCr mod p |
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

## 4.8 Game Theory Basics [P3]

**Topics**: Nim game, Sprague-Grundy theorem intro, winning/losing positions, game DP.

**Patterns**:
- **Nim**: XOR of all pile sizes. If XOR ≠ 0, first player wins.
- **Game DP**: `dp[state]` = WIN or LOSE. A state is WIN if there exists any move to a LOSE state.
- A state is LOSE if all moves lead to WIN states.

**Classical Questions**: Nim, stone game variants, Grundy numbers.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Nim Game I](https://cses.fi/problemset/task/1730) | CSES 1730 | Classic Nim |
| 2 | [Nim Game II](https://cses.fi/problemset/task/1098) | CSES 1098 | Nim variant |
| 3 | [Stair Game](https://cses.fi/problemset/task/1099) | CSES 1099 | Staircase Nim |
| 4 | [Stone Game](https://leetcode.com/problems/stone-game/) | LC 877 | Game DP |
| 5 | [Nim Game (LC)](https://leetcode.com/problems/nim-game/) | LC 292 | Modular |
| 6 | [Can I Win](https://leetcode.com/problems/can-i-win/) | LC 464 | Bitmask game DP |
| 7 | [Stone Game III](https://leetcode.com/problems/stone-game-iii/) | LC 1406 | Game DP |
| 8 | [Grundy's Game](https://cses.fi/problemset/task/2207) | CSES 2207 | Grundy |
| 9 | [Stick Game](https://cses.fi/problemset/task/1729) | CSES 1729 | DP game |

---

## 4.9 Interactive Problems & Output Flushing [P4]

**Topics**: Interactive problem protocol, binary search via queries, flushing output (`fflush(stdout)` / `cout.flush()`), adaptive strategies.

**Patterns**:
- Read problem statement carefully for query format and limits.
- Binary search with queries: guess the answer in O(log N) queries.
- Always flush output after each query.
- Some interactive problems require randomized strategies.

**Classical Questions**: Guess the number in log(N) queries, find the minimum with comparisons.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Guess the Number](https://codeforces.com/problemset/problem/1010/A) | CF 1010A | Interactive archetype |
| 2 | [Guess Number Higher or Lower](https://leetcode.com/problems/guess-number-higher-or-lower/) | LC 374 | BS interactive |
| 3 | [Bear and Pebbles](https://codeforces.com/problemset/problem/580/A) | CF 580A | Interactive thinking |
| 4 | [Lost Numbers](https://codeforces.com/problemset/problem/1167/B) | CF 1167B | Query strategy |
| 5 | [Xor Guessing](https://codeforces.com/problemset/problem/1207/E) | CF 1207E | XOR + interactive |
| 6 | [Binary Search (interactive)](https://codeforces.com/edu/course/2/lesson/6/1/practice/contest/283911/problem/A) | CF Edu | Interactive BS |

---

### Tier 4 Summary

| Priority | Topics Covered |
|----------|---------------|
| [P1] | Shortest Paths (Dijkstra/BF/Floyd), Knapsack & Subset DP, Topo Sort & DAG DP |
| [P2] | MST & Euler Paths, LIS & Interval DP, String Algorithms (KMP/Trie) |
| [P3] | Combinatorics & Mod Inverse, Game Theory Basics |
| [P4] | Interactive Problems |

**Total problems in Tier 4: ~111**

> [Checkpoint] **Checkpoint**: You can solve CF Div.2 D / Div.1 A problems (1600–1800 rated). Dijkstra, knapsack DP, KMP, and topo sort are second nature.

# Tier 5: Candidate Master (CF Rating 1900 – 2099)

> **Goal**: Combine data structures with DP. Master segment trees, BIT, bitmask DP, digit DP, and tree algorithms. Solve Div.1 B problems.

At this tier you push into advanced algorithmic territory. You master bitmask DP, interval DP, and tree DP — the three DP paradigms that appear in nearly every hard contest problem. You learn sparse tables for O(1) RMQ, number theory tools (modular inverse, combinatorics, CRT), and the two most important string algorithms (KMP and Z-function). By the end of Tier 5 you will consistently solve Div. 1 B and occasionally reach C.

---

## 5.1 Segment Tree (Point Update, Range Query) [P1]

**Topics**: Segment tree build, point update, range query (sum, min, max, GCD), iterative vs recursive implementation, coordinate compression with segment trees.

**Patterns**:
- Build in O(N), query and update in O(log N).
- Tree is stored in array of size 4N. Node `i` has children `2i` and `2i+1`.
- Range query: split range into O(log N) segments of the tree.
- Can answer any associative operation (sum, min, max, GCD, XOR, etc.).

**Classical Questions**: Dynamic range sum/min queries, range GCD queries.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Dynamic Range Sum Queries](https://cses.fi/problemset/task/1648) | CSES 1648 | SegTree template |
| 2 | ★ [Dynamic Range Minimum Queries](https://cses.fi/problemset/task/1649) | CSES 1649 | SegTree min |
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

## 5.2 Binary Indexed Tree (Fenwick Tree) [P1]

**Topics**: BIT for prefix sums with point updates, 2D BIT, order statistics with BIT, difference array + BIT for range update point query.

**Patterns**:
- BIT is simpler and faster than segment trees for prefix-sum-like operations.
- `update(i, delta)`: add delta at index i. `query(i)`: prefix sum up to index i. Both O(log N).
- Range sum `[l, r] = query(r) - query(l-1)`.
- For "count of elements ≤ x" type queries, use BIT over value domain.

**Classical Questions**: Dynamic prefix sums, counting inversions with BIT.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Dynamic Range Sum](https://cses.fi/problemset/task/1648) | CSES 1648 | BIT or SegTree |
| 2 | [Inversion Count (BIT)](https://www.spoj.com/problems/INVCNT/) | SPOJ | BIT approach |
| 3 | [Josephus Queries](https://cses.fi/problemset/task/2162) | CSES 2162 | BIT / simulation |
| 4 | [Nested Ranges Count](https://cses.fi/problemset/task/2169) | CSES 2169 | BIT + sort |
| 5 | [Nested Ranges Check](https://cses.fi/problemset/task/2168) | CSES 2168 | BIT + sort |
| 6 | [Count Good Triplets in Array](https://leetcode.com/problems/count-good-triplets-in-an-array/) | LC 2179 | BIT |
| 7 | [Reverse Pairs](https://leetcode.com/problems/reverse-pairs/) | LC 493 | BIT / merge sort |
| 8 | [UPDATEIT](https://www.spoj.com/problems/UPDATEIT/) | SPOJ | Range update + point query |

---

## 5.3 Bitmask DP [P1]

**Topics**: DP where state includes a bitmask representing a subset of N ≤ 20 elements. TSP, assignment problems, Hamiltonian paths.

**Patterns**:
- State: `dp[mask]` or `dp[mask][last]` where `mask` indicates which elements are used.
- Transition: try adding each unused element. `dp[mask | (1<<j)][j] = dp[mask][i] + cost(i,j)`.
- Total states: O(2^N · N). Works for N ≤ 20 (2^20 ≈ 10^6).

**Classical Questions**: TSP, minimum cost assignment, Hamiltonian path counting.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Hamiltonian Flights](https://cses.fi/problemset/task/1690) | CSES 1690 | Bitmask DP |
| 2 | ★ [Elevator Rides](https://cses.fi/problemset/task/1653) | CSES 1653 | Bitmask DP |
| 3 | [Shortest Hamilton Walk](https://codeforces.com/problemset/problem/580/D) | CF 580D | Bitmask DP |
| 4 | [Shortest Superstring](https://leetcode.com/problems/find-the-shortest-superstring/) | LC 943 | TSP variant |
| 5 | [Partition to K Equal Sum Subsets](https://leetcode.com/problems/partition-to-k-equal-sum-subsets/) | LC 698 | Bitmask DP |
| 6 | [Maximum Students in Exam](https://leetcode.com/problems/maximum-students-taking-exam/) | LC 1349 | Bitmask DP |
| 7 | [Minimum XOR Sum of Two Arrays](https://leetcode.com/problems/minimum-xor-sum-of-two-arrays/) | LC 1879 | Assignment |
| 8 | [Can I Win](https://leetcode.com/problems/can-i-win/) | LC 464 | Bitmask game |
| 9 | [Traveling Salesman](https://www.spoj.com/problems/TVAC/) | SPOJ | TSP |
| 10 | [Matching](https://atcoder.jp/contests/dp/tasks/dp_o) | AtCoder DP-O | Assignment |

---

## 5.4 Tree DP [P2]

**Topics**: DP on trees (rooted), computing subtree properties, diameter, max independent set, matching on trees.

**Patterns**:
- Root the tree at node 1. DFS from root, compute answers bottom-up.
- `dp[v]` depends on `dp[child]` for all children of v.
- Tree diameter: two BFS trick, or DP `dp[v] = max depth in subtree of v`, diameter = max over all v of `dp[left_child] + dp[right_child]`.

**Classical Questions**: Tree diameter, max weight independent set, tree matching.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Tree Diameter](https://cses.fi/problemset/task/1131) | CSES 1131 | DFS/BFS |
| 2 | ★ [Tree Matching](https://cses.fi/problemset/task/1130) | CSES 1130 | Tree DP |
| 3 | [Subordinates](https://cses.fi/problemset/task/1674) | CSES 1674 | Subtree size |
| 4 | [Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/) | LC 124 | Tree DP |
| 5 | [Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/) | LC 543 | Tree DP |
| 6 | [House Robber III](https://leetcode.com/problems/house-robber-iii/) | LC 337 | Tree DP |
| 7 | [Sum of Distances in Tree](https://leetcode.com/problems/sum-of-distances-in-tree/) | LC 834 | Re-rooting intro |
| 8 | [Tree Painting](https://usaco.org/index.php?page=viewproblem2&cpid=1193) | USACO Gold | Tree DP |
| 9 | [Barn Painting](https://usaco.org/index.php?page=viewproblem2&cpid=766) | USACO Gold | Tree DP |
| 10 | [Apple Tree](https://www.spoj.com/problems/PT07X/) | SPOJ PT07X | Max independent set |

---

## 5.5 LCA & Binary Lifting [P2]

**Topics**: Lowest Common Ancestor computation, binary lifting (sparse table on tree), ancestor queries, path queries decomposition.

**Patterns**:
- **Binary Lifting**: Precompute `up[v][k]` = 2^k-th ancestor of v. LCA in O(log N) per query after O(N log N) preprocessing.
- To answer "distance between u and v on tree": `dist(u,v) = depth[u] + depth[v] - 2 * depth[LCA(u,v)]`.
- Euler Tour + Sparse Table gives O(1) LCA queries after O(N log N) preprocessing.

**Classical Questions**: LCA queries, k-th ancestor queries, path queries.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Company Queries I](https://cses.fi/problemset/task/1687) | CSES 1687 | Binary lifting |
| 2 | ★ [Company Queries II](https://cses.fi/problemset/task/1688) | CSES 1688 | LCA |
| 3 | [Distance Queries](https://cses.fi/problemset/task/1135) | CSES 1135 | LCA + depth |
| 4 | [Counting Paths](https://cses.fi/problemset/task/1136) | CSES 1136 | LCA + diff on tree |
| 5 | [LCA of Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/) | LC 236 | DFS |
| 6 | [Kth Ancestor of Tree Node](https://leetcode.com/problems/kth-ancestor-of-a-tree-node/) | LC 1483 | Binary lifting |
| 7 | [LCA (SPOJ)](https://www.spoj.com/problems/LCA/) | SPOJ LCA | LCA queries |
| 8 | [Milk Visits](https://usaco.org/index.php?page=viewproblem2&cpid=970) | USACO Gold | LCA |
| 9 | [Planets Queries I](https://cses.fi/problemset/task/1750) | CSES 1750 | Binary lifting (functional graph) |
| 10 | [Planets Queries II](https://cses.fi/problemset/task/1160) | CSES 1160 | Cycle + binary lifting |

---

## 5.6 Sparse Table & RMQ [P3]

**Topics**: Sparse Table for O(1) range minimum/maximum queries (static), precomputation in O(N log N), idempotent operations.

**Patterns**:
- Works for idempotent operations (min, max, GCD, OR, AND) — where `f(a,a) = a`.
- `st[i][j]` = answer for range starting at index i with length 2^j.
- Query `[l,r]`: k = floor(log2(r-l+1)), answer = f(st[l][k], st[r-2^k+1][k]).
- Does NOT work for sum (not idempotent). Use BIT/SegTree for sum.

**Classical Questions**: Range Minimum Query (static), range GCD.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Static Range Min Queries](https://cses.fi/problemset/task/1647) | CSES 1647 | Sparse table |
| 2 | [RMQSQ](https://www.spoj.com/problems/RMQSQ/) | SPOJ | RMQ classic |
| 3 | [THRBL - Troublesome](https://www.spoj.com/problems/THRBL/) | SPOJ | Range max query |
| 4 | [Maximum of Minimums of Array](https://leetcode.com/problems/minimum-of-maximum-of-minimum-of-maximum/) | LC | Sparse table app |
| 5 | [Range XOR Queries](https://cses.fi/problemset/task/1650) | CSES 1650 | XOR is idempotent but note: typically BIT suffices |
| 6 | [Static RMQ](https://judge.yosupo.jp/problem/staticrmq) | Library Checker | Template verification |

---

## 5.7 Digit DP [P3]

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
| 1 | ★ [LUCIFER - Lucifer Number](https://www.spoj.com/problems/LUCIFER/) | SPOJ | Digit DP intro |
| 2 | [Counting Numbers](https://cses.fi/problemset/task/2220) | CSES 2220 | Digit DP |
| 3 | [Numbers At Most N Given Digit Set](https://leetcode.com/problems/numbers-at-most-n-given-digit-set/) | LC 902 | Digit DP |
| 4 | [Count Numbers with Unique Digits](https://leetcode.com/problems/count-numbers-with-unique-digits/) | LC 357 | Digit DP / math |
| 5 | [Non-negative Integers without Consecutive Ones](https://leetcode.com/problems/non-negative-integers-without-consecutive-ones/) | LC 600 | Digit DP |
| 6 | [RAONE](https://www.spoj.com/problems/RAONE/) | SPOJ | Digit DP |
| 7 | [Digit Sum](https://www.spoj.com/problems/CPCRC1C/) | SPOJ | Digit DP |
| 8 | [Count of Integers](https://leetcode.com/problems/count-of-integers/) | LC 2719 | Digit DP |
| 9 | [Magic Number](https://codeforces.com/problemset/problem/628/D) | CF 628D | Digit DP |

---

## 5.8 Probability DP & Expected Value [P3]

**Topics**: Expected value via DP, linearity of expectation, probability as DP state, Markov chains (simple).

**Patterns**:
- **Linearity of Expectation**: E[X+Y] = E[X] + E[Y], even when X and Y are NOT independent.
- Expected value DP: `E[state]` = sum over transitions of `probability * (cost + E[next_state])`.
- Coupon collector's problem: expected steps to collect all N types = N · H(N) ≈ N · ln(N).

**Classical Questions**: Expected dice rolls to reach a target, coupon collector.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Dice Probability](https://cses.fi/problemset/task/1725) | CSES 1725 | Probability DP |
| 2 | [Soup Servings](https://leetcode.com/problems/soup-servings/) | LC 808 | Probability DP |
| 3 | [Knight Probability in Chessboard](https://leetcode.com/problems/knight-probability-in-chessboard/) | LC 688 | Probability DP |
| 4 | [New 21 Game](https://leetcode.com/problems/new-21-game/) | LC 837 | Probability DP |
| 5 | [Random Pick with Weight](https://leetcode.com/problems/random-pick-with-weight/) | LC 528 | Prefix sum + BS |
| 6 | [Dice Expectations (CF)](https://codeforces.com/problemset/problem/453/A) | CF 453A | Expected value |
| 7 | [Cat and Mouse II](https://leetcode.com/problems/cat-and-mouse-ii/) | LC 1728 | Game + probability |

---

## 5.9 Monotonic Deque & Sliding Window Max/Min [P4]

**Topics**: Sliding window maximum/minimum using deque, DP optimization with monotonic deque.

**Patterns**:
- Maintain a deque of indices where values are monotonically decreasing (for max) or increasing (for min).
- For each new element: pop from back while current ≤ back. Pop from front if out of window. Front = answer.
- Used to optimize DP transitions like `dp[i] = max(dp[j] + ...) for j in [i-k, i-1]`.

**Classical Questions**: Sliding window max, max sum subarray of size at most K.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/) | LC 239 | Deque template |
| 2 | [Sliding Cost](https://cses.fi/problemset/task/1077) | CSES 1077 | Two heaps + sliding |
| 3 | [Sliding Median](https://cses.fi/problemset/task/1076) | CSES 1076 | Two multisets |
| 4 | [Jump Game VI](https://leetcode.com/problems/jump-game-vi/) | LC 1696 | DP + deque |
| 5 | [Shortest Subarray with Sum ≥ K](https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/) | LC 862 | Deque + prefix sums |
| 6 | [Constrained Subsequence Sum](https://leetcode.com/problems/constrained-subsequence-sum/) | LC 1425 | DP + deque |
| 7 | [Max Value of Equation](https://leetcode.com/problems/max-value-of-equation/) | LC 1499 | Deque optimization |

---

## 5.10 Policy-Based Data Structures (PBDS) [P4]

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
| 1 | ★ [List Removals](https://cses.fi/problemset/task/1749) | CSES 1749 | Order statistics |
| 2 | ★ [Josephus Problem II](https://cses.fi/problemset/task/2163) | CSES 2163 | PBDS / SegTree |
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
| [P1] | Segment Tree, Fenwick Tree (BIT), Bitmask DP |
| [P2] | Tree DP, LCA & Binary Lifting |
| [P3] | Sparse Table, Digit DP, Probability DP |
| [P4] | Monotonic Deque, Policy-Based Data Structures (PBDS) |

**Total problems in Tier 5: ~118**

> [Checkpoint] **Checkpoint**: You can solve Div.1 B / Div.2 E problems (1900–2000 rated). Segment trees and bitmask DP are comfortable. You can implement LCA from scratch.

# Tier 6: Master (CF Rating 2100 – 2299)

> **Goal**: Combine data structures. Segment trees with lazy propagation, advanced tree techniques, SOS DP, re-rooting DP, SCCs, 2-SAT. Solve Div.1 C problems.

At this tier you tackle the hardest graph algorithms and advanced string structures. You master strongly connected components, bridges and articulation points, Euler paths, LCA with binary lifting, suffix arrays, and network flow. These topics appear in Div. 1 C and D problems. By the end of Tier 6 you will consistently solve Div. 1 C and occasionally reach D.

---

## 6.1 Segment Tree with Lazy Propagation [P1]

**Topics**: Range update + range query, lazy propagation for additive updates, multiplicative updates, assignment updates, combining different lazy operations.

**Patterns**:
- **Lazy propagation**: Instead of updating every node in a range, store a "pending" update in internal nodes and push it down when needed.
- "Range add + Range sum", "Range set + Range min" — all need lazy.
- The `push_down` function propagates lazy values to children before accessing them.

**Classical Questions**: Range addition + range sum query, range assign + range min query.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Range Update Queries](https://cses.fi/problemset/task/1651) | CSES 1651 | Lazy SegTree template |
| 2 | ★ [Range Updates and Sums](https://cses.fi/problemset/task/1735) | CSES 1735 | Lazy add + set |
| 3 | [Polynomial Queries](https://cses.fi/problemset/task/1736) | CSES 1736 | Arithmetic progression lazy |
| 4 | [HORRIBLE - Horrible Queries](https://www.spoj.com/problems/HORRIBLE/) | SPOJ | Lazy SegTree |
| 5 | [LITE - Light Switching](https://www.spoj.com/problems/LITE/) | SPOJ | XOR lazy |
| 6 | [Range Module](https://leetcode.com/problems/range-module/) | LC 715 | Interval SegTree |
| 7 | [My Calendar III](https://leetcode.com/problems/my-calendar-iii/) | LC 732 | Lazy SegTree |
| 8 | [Falling Squares](https://leetcode.com/problems/falling-squares/) | LC 699 | Coordinate compress + lazy |
| 9 | [Count of Range Sum](https://leetcode.com/problems/count-of-range-sum/) | LC 327 | SegTree / merge sort |
| 10 | [Max Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/) | LC 1235 | DP + SegTree |

---

## 6.2 Euler Tour & Subtree/Path Queries on Trees [P1]

**Topics**: Euler Tour (flattening a tree into an array), subtree queries via range queries on the flattened array, path queries with LCA decomposition.

**Patterns**:
- **Euler Tour**: DFS traversal recording `tin[v]` (entry time) and `tout[v]` (exit time). Subtree of v = range `[tin[v], tout[v]]` in the array.
- Subtree sum/update → BIT/SegTree on the Euler tour array.
- Path queries → Euler Tour + LCA or HLD.

**Classical Questions**: Subtree sum update/query, path update/query.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Subtree Queries](https://cses.fi/problemset/task/1137) | CSES 1137 | Euler Tour + BIT |
| 2 | ★ [Path Queries](https://cses.fi/problemset/task/1138) | CSES 1138 | Euler Tour / HLD |
| 3 | [Path Queries II](https://cses.fi/problemset/task/2134) | CSES 2134 | HLD + SegTree |
| 4 | [Distinct Colors](https://cses.fi/problemset/task/1139) | CSES 1139 | Small-to-large merge |
| 5 | [Count Nodes in Sub-Tree](https://leetcode.com/problems/number-of-nodes-in-the-sub-tree-with-the-same-label/) | LC 1519 | DFS / Euler tour |
| 6 | [QTREE](https://www.spoj.com/problems/QTREE/) | SPOJ QTREE | HLD |
| 7 | [COT2](https://www.spoj.com/problems/COT2/) | SPOJ | Euler Tour + Mo |
| 8 | [Promotion Counting](https://usaco.org/index.php?page=viewproblem2&cpid=696) | USACO Gold | Euler tour merge |

---

## 6.3 Re-rooting DP [P2]

**Topics**: Computing an answer for every node as root efficiently. Bottom-up DFS followed by top-down DFS to "re-root" the tree.

**Patterns**:
1. First DFS (bottom-up): compute `dp_down[v]` = answer for subtree rooted at v.
2. Second DFS (top-down): compute `dp_up[v]` = answer from the rest of the tree (complement of v's subtree).
3. Combine: `answer[v] = combine(dp_down[v], dp_up[v])`.

**Classical Questions**: Sum of distances to all nodes from each node, farthest node from each node.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Tree Distances I](https://cses.fi/problemset/task/1132) | CSES 1132 | Re-rooting farthest |
| 2 | ★ [Tree Distances II](https://cses.fi/problemset/task/1133) | CSES 1133 | Re-rooting sum |
| 3 | [Sum of Distances in Tree](https://leetcode.com/problems/sum-of-distances-in-tree/) | LC 834 | Re-rooting |
| 4 | [Count Subtrees with Max Distance](https://leetcode.com/problems/count-subtrees-with-max-distance-between-cities/) | LC 1617 | Bitmask + tree |
| 5 | [Minimum Edge Weight Equilibrium](https://leetcode.com/problems/minimum-edge-weight-equilibrium-queries-in-a-tree/) | LC 2846 | LCA + re-root |
| 6 | [Maximum Sum BST in Binary Tree](https://leetcode.com/problems/maximum-sum-bst-in-binary-tree/) | LC 1373 | Tree DP |
| 7 | [Directory Traversal](https://usaco.org/index.php?page=viewproblem2&cpid=814) | USACO Gold | Re-rooting |

---

## 6.4 SOS DP (Sum over Subsets) [P2]

**Topics**: Efficiently computing sum/count over all subsets (or supersets) of each bitmask. O(N · 2^N) using the "zeta/Mobius transform" approach.

**Patterns**:
- For each bit position, iterate over all masks and propagate from submasks.
- `for bit in 0..N: for mask in 0..(1<<N): if mask & (1<<bit): dp[mask] += dp[mask ^ (1<<bit)]`
- After this, `dp[mask]` = sum of `original[submask]` for all submasks of mask.

**Classical Questions**: Count of submasks with property X for each mask, AND/OR convolution.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Vowels (SOS DP)](https://codeforces.com/problemset/problem/165/E) | CF 165E | SOS DP archetype |
| 2 | [Compatible Numbers](https://codeforces.com/problemset/problem/449/D) | CF 449D | SOS DP |
| 3 | [Counting Bits](https://codeforces.com/problemset/problem/1208/F) | CF 1208F | SOS DP |
| 4 | [XOR Inverse](https://codeforces.com/problemset/problem/1416/C) | CF 1416C | Bit contribution |
| 5 | [AND Plus OR](https://codeforces.com/problemset/problem/1721/E) | CF 1721E | SOS |
| 6 | [Sum Over Subsets](https://judge.yosupo.jp/problem/subset_sum_convolution) | Library Checker | Template |
| 7 | [Maximize XOR](https://leetcode.com/problems/maximum-xor-of-two-numbers-in-an-array/) | LC 421 | Trie / SOS |

---

## 6.5 SCCs, 2-SAT & Advanced Graph [P2]

**Topics**: Strongly Connected Components (Kosaraju / Tarjan), 2-SAT via implication graphs, condensation graph, topological sort on condensation.

**Patterns**:
- **Kosaraju's**: Two DFS passes — first to get finish order, second on reversed graph in reverse finish order.
- **2-SAT**: Model boolean constraints as implications (x → y means "if x then y"). Build implication graph, find SCCs. If x and ¬x are in the same SCC → unsatisfiable.
- Condensation: contract each SCC into a single node → resulting graph is a DAG.

**Classical Questions**: Finding SCCs, satisfying boolean formulas with at most 2 literals per clause.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Giant Pizza](https://cses.fi/problemset/task/1684) | CSES 1684 | 2-SAT |
| 2 | ★ [Planets and Kingdoms](https://cses.fi/problemset/task/1683) | CSES 1683 | SCCs |
| 3 | [Coin Collector](https://cses.fi/problemset/task/1686) | CSES 1686 | Condensation + DAG DP |
| 4 | [Flight Routes Check](https://cses.fi/problemset/task/1682) | CSES 1682 | SCC check |
| 5 | [Kosaraju (SPOJ)](https://www.spoj.com/problems/KOSARAJU/) | SPOJ | SCC template |
| 6 | [Stongly Connected Component](https://judge.yosupo.jp/problem/scc) | Library Checker | SCC template |
| 7 | [Satisfiability of Equality](https://leetcode.com/problems/satisfiability-of-equality-equations/) | LC 990 | 2-SAT lite |
| 8 | [Critical Connections](https://leetcode.com/problems/critical-connections-in-a-network/) | LC 1192 | Bridges/Tarjan |

---

## 6.6 Inclusion-Exclusion Principle [P3]

**Topics**: Counting via inclusion-exclusion, derangements, Euler's totient function, sieve-based inclusion-exclusion.

**Patterns**:
- |A₁ ∪ A₂ ∪ ... ∪ Aₙ| = Σ|Aᵢ| - Σ|Aᵢ ∩ Aⱼ| + Σ|Aᵢ ∩ Aⱼ ∩ Aₖ| - ...
- For counting multiples of at least one prime in a set → iterate over subsets of prime set.
- Derangement formula: D(n) = n! · Σ(-1)^k / k! for k=0..n.

**Classical Questions**: Count numbers ≤ N divisible by at least one of given primes, derangements.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Prime Multiples](https://cses.fi/problemset/task/2185) | CSES 2185 | Inclusion-Exclusion |
| 2 | [Christmas Party](https://cses.fi/problemset/task/1717) | CSES 1717 | Derangements |
| 3 | [Coprime Pairs](https://codeforces.com/problemset/problem/547/C) | CF 547C | Incl-Excl + Mobius |
| 4 | [Counting Coprime Pairs](https://cses.fi/problemset/task/2417) | CSES 2417 | Totient / IE |
| 5 | [Ugly Number III](https://leetcode.com/problems/ugly-number-iii/) | LC 1201 | Incl-Excl + BS |
| 6 | [Count Integers](https://codeforces.com/problemset/problem/630/K) | CF 630K | IE |
| 7 | [Kth Smallest Number in Multiplication Table](https://leetcode.com/problems/kth-smallest-number-in-multiplication-table/) | LC 668 | BS + counting |

---

## 6.7 Matrix Exponentiation [P3]

**Topics**: Representing linear recurrences as matrix multiplication, computing n-th term in O(K^3 · log N) where K = matrix size.

**Patterns**:
- Fibonacci: [F(n+1), F(n)] = [[1,1],[1,0]]^n · [F(1), F(0)].
- Any linear recurrence of order K → K×K matrix.
- Also used for counting paths of length N in a graph (adjacency matrix ^ N).

**Classical Questions**: N-th Fibonacci in O(log N), counting paths of exact length K in a graph.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Graph Paths I](https://cses.fi/problemset/task/1723) | CSES 1723 | Matrix exp |
| 2 | [Fibonacci Numbers](https://cses.fi/problemset/task/1722) | CSES 1722 | Matrix exp |
| 3 | [Graph Paths II](https://cses.fi/problemset/task/1724) | CSES 1724 | Matrix exp min-plus |
| 4 | [Throwing Dice](https://cses.fi/problemset/task/1096) | CSES 1096 | Matrix exp |
| 5 | [MPOW - Power of a Matrix](https://www.spoj.com/problems/MPOW/) | SPOJ | Matrix exp |
| 6 | [Nth Tribonacci Number](https://leetcode.com/problems/n-th-tribonacci-number/) | LC 1137 | Matrix exp variant |
| 7 | [Knight Dialer](https://leetcode.com/problems/knight-dialer/) | LC 935 | Matrix exp / DP |

---

## 6.8 Centroid Decomposition [P3]

**Topics**: Finding centroids of trees recursively, counting paths with specific properties, point queries on trees.

**Patterns**:
- **Centroid**: Node whose removal splits the tree into components of size ≤ N/2.
- Build a centroid decomposition tree of depth O(log N).
- For each centroid, count paths passing through it, then recurse on subtrees.
- Used for: counting paths of length K, distance queries, update/query on tree paths.

**Classical Questions**: Count pairs of vertices at distance exactly K, distance queries on trees.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Xenia and Tree](https://codeforces.com/problemset/problem/342/E) | CF 342E | Centroid decomp |
| 2 | [Finding Centroids](https://cses.fi/problemset/task/2079) | CSES 2079 | Centroid basics |
| 3 | [QTREE5](https://www.spoj.com/problems/QTREE5/) | SPOJ | Centroid decomp |
| 4 | [Race](https://oj.uz/problem/view/IOI11_race) | IOI 2011 | Centroid |
| 5 | [New Year Tree (CF)](https://codeforces.com/problemset/problem/620/E) | CF 620E | Euler tour + bitmask |
| 6 | [Centroid Decomposition](https://judge.yosupo.jp/problem/centroid_decomposition) | Library Checker | Template |

---

## 6.9 Advanced Greedy & Observation [P4]

**Topics**: Exchange arguments (formal proofs), greedy with priority queues, multi-step greedy strategies, observation-heavy problems.

**Patterns**:
- **Exchange argument**: Assume optimal solution differs from greedy. Show swapping to match greedy doesn't worsen the answer.
- Priority queue for "always process the best available" strategies.
- Many CF problems at this level require a key observation that simplifies the problem dramatically.

**Classical Questions**: Job scheduling with deadlines, Huffman coding, rearranging strings.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Reorganize String](https://leetcode.com/problems/reorganize-string/) | LC 767 | Greedy + PQ |
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
| [P1] | Lazy Segment Tree, Euler Tour + Subtree/Path Queries |
| [P2] | Re-rooting DP, SOS DP, SCCs & 2-SAT |
| [P3] | Inclusion-Exclusion, Matrix Exponentiation, Centroid Decomposition |
| [P4] | Advanced Greedy & Observation |

**Total problems in Tier 6: ~105**

> [Checkpoint] **Checkpoint**: You can solve Div.1 C problems (2100–2300 rated). Lazy segment trees, Euler tours, and 2-SAT are in your toolkit. You can combine multiple structures to solve one problem.

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

# Tier 9: International Grandmaster (CF Rating 2600 – 2899)

> **Goal**: Mastery of advanced techniques. Alien's trick, generating functions, Link-Cut Trees, advanced geometry. Problems routinely require novel combinations of techniques or reading research papers.

At this tier you operate at the frontier of competitive programming. You master advanced geometry, persistent and specialized segment trees, randomized algorithms, and the most powerful string data structures. These topics appear in Div. 1 E and F problems and IOI/ICPC finals. By the end of Tier 9 you will be capable of solving the hardest problems in major contests.

---

## 9.1 Alien's Trick (Lambda / Lagrange Relaxation) [P1]

**Topics**: Penalty-based optimization to remove a constraint (e.g., "use exactly K segments"), WQS binary search (Aliens trick), trading off a Lagrange multiplier.

**Patterns**:
- Problem: "Minimize cost using exactly K of something."
- Add a penalty λ for each unit used. Binary search on λ so that the unconstrained optimum uses exactly K units.
- The unconstrained problem (with penalty) is often much simpler (e.g., O(N) greedy instead of O(NK) DP).
- Key requirement: the answer must be convex/concave in K.

**Classical Questions**: IOI 2016 Aliens (minimum cost to cover points with K squares).

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Aliens (IOI)](https://oj.uz/problem/view/IOI16_aliens) | IOI 2016 | Alien's trick archetype |
| 2 | [Sequence (CF)](https://codeforces.com/problemset/problem/13/C) | CF 13C | WQS BS |
| 3 | [Lamps (CF)](https://codeforces.com/problemset/problem/1515/G) | CF 1515G | Alien |
| 4 | [Parallel Scheduling](https://codeforces.com/problemset/problem/802/O) | CF 802O | WQS BS |
| 5 | [Mowing the Lawn (IOI)](https://oj.uz/problem/view/IOI09_mowing) | IOI 2009 | DP + deque / WQS |
| 6 | [k-th Largest Area](https://codeforces.com/problemset/problem/1270/E) | CF 1270E | WQS related |

---

## 9.2 Generating Functions [P2]

**Topics**: Ordinary generating functions (OGF), exponential generating functions (EGF), operations on formal power series (addition, multiplication, inversion, composition), solving recurrences via generating functions.

**Patterns**:
- OGF: A(x) = Σ a_n · x^n. Product of OGFs = convolution (FFT/NTT).
- Inverse: A(x)^(-1) computed via Newton's method in O(N log N).
- EGF: A(x) = Σ a_n · x^n / n!. Product corresponds to "labeled" combination.
- Partition function, Fibonacci closed form, derangement formula — all derivable via GFs.

**Classical Questions**: Computing partition numbers, composition of formal power series.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Kinematic Equation](https://codeforces.com/problemset/problem/438/E) | CF 438E | GF |
| 2 | [Inv of Formal Power Series](https://judge.yosupo.jp/problem/inv_of_formal_power_series) | Library Checker | Template |
| 3 | [Exp of Formal Power Series](https://judge.yosupo.jp/problem/exp_of_formal_power_series) | Library Checker | Template |
| 4 | [Log of Formal Power Series](https://judge.yosupo.jp/problem/log_of_formal_power_series) | Library Checker | Template |
| 5 | [Partition Function](https://judge.yosupo.jp/problem/partition_function) | Library Checker | GF application |
| 6 | [Trees (CF)](https://codeforces.com/problemset/problem/940/F) | CF 940F | EGF |
| 7 | [Subset Sum](https://judge.yosupo.jp/problem/sharp_p_subset_sum) | Library Checker | GF / NTT |

---

## 9.3 Link-Cut Trees [P2]

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
| 1 | ★ [Dynamic Connectivity](https://cses.fi/problemset/task/2133) | CSES 2133 | LCT / offline DSU |
| 2 | [Link-Cut Tree](https://judge.yosupo.jp/problem/dynamic_tree_vertex_add_path_sum) | Library Checker | LCT template |
| 3 | [Dynamic Tree Vertex Set Path Composite](https://judge.yosupo.jp/problem/dynamic_tree_vertex_set_path_composite) | Library Checker | LCT |
| 4 | [QTREE (Dynamic)](https://www.spoj.com/problems/QTREE/) | SPOJ | LCT |
| 5 | [OTOCI](https://www.spoj.com/problems/OTOCI/) | SPOJ | LCT |
| 6 | [Disconnected Graph](https://codeforces.com/problemset/problem/117/E) | CF 117E | LCT |

---

## 9.4 Lagrange Interpolation & Sum of Powers [P3]

**Topics**: Given K+1 points, recover polynomial of degree K in O(K) or O(K log K). Computing Σi^k for i=1..N in O(K).

**Patterns**:
- **Lagrange interpolation**: P(x) = Σ y_i · Π(x - x_j) / Π(x_i - x_j) for j ≠ i.
- When x-values are 0, 1, 2, ..., K: simplify using prefix/suffix products. O(K) evaluation.
- Sum of k-th powers: S(n) = Σi^k is a polynomial of degree k+1 in n. Evaluate at k+2 points to interpolate.

**Classical Questions**: Sum of k-th powers for large N, evaluating a polynomial given by k+1 values.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Sum of k-th Powers](https://codeforces.com/problemset/problem/622/F) | CF 622F | Lagrange |
| 2 | [Polynomial Interpolation](https://judge.yosupo.jp/problem/polynomial_interpolation) | Library Checker | Template |
| 3 | [Multipoint Evaluation](https://judge.yosupo.jp/problem/multipoint_evaluate) | Library Checker | Template |
| 4 | [Xor-sequences](https://codeforces.com/problemset/problem/691/E) | CF 691E | Matrix exp + interpolation |
| 5 | [Highways](https://codeforces.com/problemset/problem/1142/E) | CF 1142E | Interpolation |
| 6 | [Bernoulli Sum](https://codeforces.com/problemset/problem/258/D) | CF 258D | Lagrange + number theory |

---

## 9.5 Advanced Computational Geometry [P3]

**Topics**: Half-plane intersection, Minkowski sum, rotating calipers, Voronoi diagram intuition, line-point duality, advanced sweep line problems.

**Patterns**:
- **Rotating calipers**: Find furthest pair (diameter of convex hull) in O(N) after hull.
- **Half-plane intersection**: Intersection of half-planes = convex polygon. O(N log N) via sorting + deque.
- **Minkowski sum**: Sum of two convex polygons is a convex polygon. Computed in O(N+M).

**Classical Questions**: Width of a convex hull, maximum distance pair, visibility from a point.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Convex Hull](https://cses.fi/problemset/task/2195) | CSES 2195 | Convex hull |
| 2 | [Minimum Euclidean Distance](https://cses.fi/problemset/task/2194) | CSES 2194 | Closest pair |
| 3 | [All Manhattan Distances](https://cses.fi/problemset/task/3411) | CSES 3411 | Manhattan geometry |
| 4 | [Half-plane Intersection](https://judge.yosupo.jp/problem/convex_hull) | Library Checker | Template |
| 5 | [GCDSSQ](https://codeforces.com/problemset/problem/475/D) | CF 475D | Geometry + math |
| 6 | [Rotating Calipers](https://codeforces.com/problemset/problem/1189/D) | CF 1189D | Geometry |
| 7 | [Intersection of F(x)](https://www.spoj.com/problems/TLINE/) | SPOJ | Geometry |

---

## 9.6 Advanced Number Theory [P3]

**Topics**: Pollard's Rho (factoring large numbers), Miller-Rabin primality test, Chinese Remainder Theorem (CRT), discrete logarithm (Baby-step Giant-step), primitive roots.

**Patterns**:
- **Miller-Rabin**: Probabilistic primality test in O(K log^2 N). Deterministic for N < 3.3·10^24 with specific witnesses.
- **Pollard's Rho**: Expected O(N^(1/4)) factorization.
- **CRT**: Combine congruences x ≡ a_i mod m_i (pairwise coprime) into x ≡ A mod (Πm_i).
- **BSGS**: Find x such that a^x ≡ b (mod p) in O(√p).

**Classical Questions**: Factorize a 10^18 number, solve modular equations.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Factorize](https://judge.yosupo.jp/problem/factorize) | Library Checker | Pollard's Rho |
| 2 | [Primality Test](https://judge.yosupo.jp/problem/primality_test) | Library Checker | Miller-Rabin |
| 3 | [Discrete Logarithm](https://judge.yosupo.jp/problem/discrete_logarithm_mod) | Library Checker | BSGS |
| 4 | [CRT (Chinese Remainder)](https://judge.yosupo.jp/problem/chinese_remainder) | Library Checker | CRT |
| 5 | [Primitive Root](https://judge.yosupo.jp/problem/primitive_root) | Library Checker | Template |
| 6 | [Big Primes](https://www.spoj.com/problems/BIGNUMS/) | SPOJ | Factorization |
| 7 | [Sum of Floor of Rationals](https://judge.yosupo.jp/problem/sum_of_floor_of_linear) | Library Checker | Number theory |

---

## 9.7 Sprague-Grundy Theory (Advanced) [P4]

**Topics**: Grundy numbers (nimbers) for impartial games, computing Grundy values via mex, combining independent games via XOR of Grundy values, Green Hackenbush.

**Patterns**:
- **Grundy number** of a position = mex({Grundy(successor positions)}).
- mex(S) = smallest non-negative integer NOT in S.
- XOR of Grundy numbers of independent game components = Grundy number of the combined game.
- First player wins iff total Grundy ≠ 0.

**Classical Questions**: General nim-like games, turning turtles, graph games.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Grundy's Game](https://cses.fi/problemset/task/2207) | CSES 2207 | Grundy |
| 2 | [Nim Game III](https://cses.fi/problemset/task/2208) | CSES 2208 | Nim variant |
| 3 | [Another Game (CF)](https://codeforces.com/problemset/problem/850/C) | CF 850C | Game theory variant |
| 4 | [Game with string](https://codeforces.com/problemset/problem/155/B) | CF 155B | Grundy |
| 5 | [Green Hackenbush](https://codeforces.com/problemset/problem/850/C) | CF 850C | Nimber |
| 6 | [Treblecross](https://codeforces.com/problemset/problem/839/E) | CF 839E | Grundy + game |

---

### Tier 9 Summary

| Priority | Topics Covered |
|----------|---------------|
| [P1] | Alien's Trick (WQS Binary Search) |
| [P2] | Generating Functions, Link-Cut Trees |
| [P3] | Lagrange Interpolation, Advanced Geometry, Advanced Number Theory |
| [P4] | Sprague-Grundy Theory (Advanced) |

**Total problems in Tier 9: ~75**

> [Checkpoint] **Checkpoint**: You can solve Div.1 E/F problems. You read IOI/ICPC World Finals editorials comfortably. Almost any single technique is within reach.

# Tier 10: Legendary Grandmaster (CF Rating 3000+)

> **Goal**: The absolute apex. Problems at this level require novel algorithmic ideas, research-level math, extreme constant-factor optimization, and synthesizing 3+ advanced techniques in a single solution.

This is the pinnacle of competitive programming. At this tier you engage with research-level algorithms, advanced combinatorics, cutting-edge DP techniques, and olympiad-level problem solving strategies. These topics appear in the hardest problems of Codeforces Div. 1, IOI, and ICPC World Finals. Mastery here requires not just knowing algorithms but inventing new approaches.

---

## 10.1 Advanced Flow & Matroid Theory [P1]

**Topics**: General matching (Edmonds' blossom algorithm), matroid intersection, Gomory-Hu trees (all-pairs min-cut), min-cut applications, project selection.

**Patterns**:
- **General matching** (non-bipartite): Edmonds' blossom algorithm. O(V^3). Rarely implemented from scratch — use library.
- **Gomory-Hu tree**: A weighted tree on V vertices such that the min-cut between any pair (u,v) equals the min edge on the path u→v in this tree. Built with V-1 max-flow calls.
- **Matroid intersection**: Finding common independent set in two matroids. Used for problems that combine two types of "independence" constraints.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [General Matching](https://judge.yosupo.jp/problem/general_matching) | Library Checker | Blossom |
| 2 | [Gomory-Hu Tree](https://judge.yosupo.jp/problem/gomory_hu_tree) | Library Checker | Template |
| 3 | [Project Selection](https://codeforces.com/problemset/problem/311/E) | CF 311E | Min-cut |
| 4 | [Minimum Weight Closure](https://codeforces.com/problemset/problem/1082/G) | CF 1082G | Flow + closure |
| 5 | [Matroid Intersection](https://judge.yosupo.jp/problem/matroid_intersection) | Library Checker | Template |
| 6 | [Stable Marriage (Gale-Shapley)](https://www.spoj.com/problems/STABLEMP/) | SPOJ | Stable matching |

---

## 10.2 Top Trees & Euler Tour Trees [P2]

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

## 10.3 Palindromic Tree (Eertree) [P2]

**Topics**: A tree of palindromic substrings. Each node represents a distinct palindromic substring. Built online in O(N).

**Patterns**:
- Two roots: one for odd-length palindromes, one for even-length.
- Each node has a suffix link (longest proper palindromic suffix).
- Total distinct palindromic substrings ≤ N+2.
- Useful for counting palindromic substrings, finding the longest palindromic substring ending at each position.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Eertree / Palindromic Tree](https://judge.yosupo.jp/problem/eertree) | Library Checker | Template |
| 2 | [Palindromic Characteristics](https://codeforces.com/problemset/problem/906/E) | CF 906E | Eertree |
| 3 | [Palindrome Pairs](https://leetcode.com/problems/palindrome-pairs/) | LC 336 | Eertree / hashing |
| 4 | [Palindromes (CF)](https://codeforces.com/problemset/problem/835/D) | CF 835D | Eertree |
| 5 | [A Lot of Palindromes](https://codeforces.com/problemset/problem/245/H) | CF 245H | Eertree / manacher |

---

## 10.4 Randomized Algorithms & Hashing Tricks [P3]

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

## 10.5 Subset Sum Convolution & Advanced Transforms [P3]

**Topics**: Subset sum convolution (combining SOS with inclusion-exclusion), Mobius inversion on subsets, OR/AND convolution, advanced NTT applications.

**Patterns**:
- **Subset sum convolution**: h(S) = Σ_{T⊆S} f(T) · g(S\T). Computed in O(2^N · N^2) via "ranked" zeta/Mobius transform.
- OR convolution: h(S) = Σ_{A|B=S} f(A) · g(B). Computed via superset zeta transform + pointwise product + Mobius inversion.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ★ [Subset Sum Convolution](https://judge.yosupo.jp/problem/subset_convolution) | Library Checker | Template |
| 2 | [Bitwise AND Convolution](https://judge.yosupo.jp/problem/bitwise_and_convolution) | Library Checker | Template |
| 3 | [Bitwise OR Convolution](https://judge.yosupo.jp/problem/bitwise_or_convolution) | Library Checker | Template |
| 4 | [Square Root of FPS](https://judge.yosupo.jp/problem/sqrt_of_formal_power_series) | Library Checker | FPS |
| 5 | [Composition of FPS](https://judge.yosupo.jp/problem/composition_of_formal_power_series) | Library Checker | FPS |
| 6 | [XOR Convolution](https://judge.yosupo.jp/problem/bitwise_xor_convolution) | Library Checker | Walsh-Hadamard |

---

## 10.6 Miscellaneous Advanced & Research-Level [P4]

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
| [P1] | Advanced Flow, Matroid Theory, General Matching |
| [P2] | Top Trees, Euler Tour Trees, Palindromic Tree |
| [P3] | Randomized Algorithms, Subset Sum Convolution |
| [P4] | Wavelet Trees, Fractional Cascading, Research-Level |

**Total problems in Tier 10: ~55**

> [Checkpoint] **Checkpoint**: You are among the best competitive programmers in the world. You can solve nearly any problem given enough time and can invent new techniques when needed.

