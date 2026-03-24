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
| 4 | [Binary Deque](https://codeforces.com/problemset/problem/1692/E) | CF 1692E | O(N) or O(N log N) |
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
