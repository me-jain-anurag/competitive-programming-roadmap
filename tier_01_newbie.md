# Tier 1: Newbie (CF Rating < 1200)

> **Goal**: Translate thoughts into code flawlessly. Learn basic complexities. Recognize the simplest patterns. Build the habit of reading constraints before thinking of an algorithm.

At this tier you are building the absolute foundations of competitive programming: reading and writing input/output efficiently, manipulating arrays and strings, applying elementary math, implementing basic sorting, and thinking recursively. By the end of Tier 1 you will be comfortable solving straightforward implementation problems, handling edge cases in simple loops, and writing clean brute-force solutions that pass within time limits on easy contests.

---

## 1.1 Basic I/O, Data Types & Control Flow 🔴 P1

**Topics**: Fast I/O (`scanf/printf` or `ios::sync_with_stdio`), integer overflow awareness (`int` vs `long long`), loops, conditionals, basic type casting.

**Patterns**:
- Always check if the answer could exceed `2^31 – 1`; if so, use `long long`.
- Read the full input specification carefully — many WAs come from misread input.
- Use `'\n'` instead of `endl` for faster output.

**Classical Questions**: Read two numbers and print their sum, find the maximum of three numbers, check if a year is a leap year.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Watermelon](https://codeforces.com/problemset/problem/4/A) | CF 4A | Parity check |
| 2 | [Way Too Long Words](https://codeforces.com/problemset/problem/71/A) | CF 71A | String basics |
| 3 | [Team](https://codeforces.com/problemset/problem/231/A) | CF 231A | Simple counting |
| 4 | [Boy or Girl](https://codeforces.com/problemset/problem/236/A) | CF 236A | Set / distinct chars |
| 5 | [Wrong Subtraction](https://codeforces.com/problemset/problem/977/A) | CF 977A | Simulation loop |
| 6 | [Stones on the Table](https://codeforces.com/problemset/problem/266/A) | CF 266A | Adjacent comparison |
| 7 | ⭐ [Weird Algorithm](https://cses.fi/problemset/task/1068) | CSES 1068 | Simulation / overflow |
| 8 | [Missing Number](https://cses.fi/problemset/task/1083) | CSES 1083 | Sum formula |
| 9 | [Two Sum](https://leetcode.com/problems/two-sum/) | LC 1 | Hash map intro |
| 10 | [Fizz Buzz](https://leetcode.com/problems/fizz-buzz/) | LC 412 | Control flow |
| 11 | [Palindrome Number](https://leetcode.com/problems/palindrome-number/) | LC 9 | Reversal logic |
| 12 | [Theatre Square](https://codeforces.com/problemset/problem/1/A) | CF 1A | Ceiling division |
| 13 | [Football](https://codeforces.com/problemset/problem/96/A) | CF 96A | Counting consecutive |
| 14 | [Factorial](https://www.spoj.com/problems/FCTRL) | SPOJ | Trailing zeroes |

---

## 1.2 Simple Math & Number Properties 🔴 P1

**Topics**: Divisibility, modular arithmetic basics, parity (odd/even), floor/ceil division, absolute value, basic formulas (sum of 1..N, area, etc.).

**Patterns**:
- `ceil(a/b)` for integers = `(a + b - 1) / b`.
- Parity of a sum depends only on the count of odd numbers.
- If constraints say N ≤ 10^6, an O(N) solution is fine; if N ≤ 10^3, O(N^2) is fine.

**Classical Questions**: Check if a number is even and > 2 (Watermelon), domino piling on a grid, compute GCD by hand.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Domino Piling](https://codeforces.com/problemset/problem/50/A) | CF 50A | floor(m*n/2) |
| 2 | [Beautiful Matrix](https://codeforces.com/problemset/problem/263/A) | CF 263A | Manhattan distance |
| 3 | [Even Odds](https://codeforces.com/problemset/problem/318/A) | CF 318A | Parity + formula |
| 4 | [Helpful Maths](https://codeforces.com/problemset/problem/339/A) | CF 339A | Parsing + sorting |
| 5 | [Number Spiral](https://cses.fi/problemset/task/1071) | CSES 1071 | Math / observation |
| 6 | ⭐ [Two Knights](https://cses.fi/problemset/task/1072) | CSES 1072 | Counting / inclusion |
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

## 1.3 Basic Strings & Character Manipulation 🔴 P1

**Topics**: String traversal, character comparison, ASCII values, substring extraction, string reversal, frequency counting with arrays.

**Patterns**:
- Use `s[i] - 'a'` to get 0-indexed position of lowercase chars.
- Frequency array of size 26 replaces hash maps for lowercase Latin letters.
- Always consider empty strings and single-character strings as edge cases.

**Classical Questions**: Check if a string is a palindrome, count vowels, reverse words.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Bit++](https://codeforces.com/problemset/problem/282/A) | CF 282A | String parsing |
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

## 1.4 Arrays, Sorting & Simple Searching 🟠 P2

**Topics**: Array traversal, finding min/max, counting occurrences, built-in sort, custom comparators (conceptual), linear search, basic set usage.

**Patterns**:
- "Find the minimum/maximum" → single pass O(N).
- "Are there duplicates?" → sort then check adjacent, or use a set.
- "Find the k-th smallest" → sort then index.

**Classical Questions**: Find the second largest element, check if array is sorted, count frequency of each element.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Distinct Numbers](https://cses.fi/problemset/task/1621) | CSES 1621 | Sort or set |
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

## 1.5 Simulation & Ad-Hoc 🟠 P2

**Topics**: Following problem statements exactly, game simulation, cycle detection in simulation, state tracking, matrix/grid traversal.

**Patterns**:
- When N is small (≤ 1000), just simulate step by step.
- If simulation runs for 10^9 steps, look for a cycle — states must eventually repeat.
- Grid problems: use `dx[], dy[]` arrays for 4 or 8 directions.

**Classical Questions**: Robot on a grid, simulate a card game, Collatz conjecture.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Buy a Shovel](https://codeforces.com/problemset/problem/732/A) | CF 732A | Modular cycle |
| 2 | [Die Roll](https://codeforces.com/problemset/problem/9/A) | CF 9A | Probability / counting |
| 3 | [Anton and Danik](https://codeforces.com/problemset/problem/734/A) | CF 734A | Counting wins |
| 4 | ⭐ [Spiral Matrix](https://leetcode.com/problems/spiral-matrix/) | LC 54 | Grid simulation |
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

## 1.6 Intro to Greedy Thinking 🟡 P3

**Topics**: Making locally optimal choices, coin change with greedy (when valid), activity selection intuition, always pick the best available option.

**Patterns**:
- "Maximize the count of something" → often sort and pick greedily.
- "Minimize operations" → think about what the cheapest single operation is.
- Greedy only works when local optimum leads to global optimum — verify with small cases.

**Classical Questions**: Maximize coins collected, minimize moves to equalize, activity selection.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Young Physicist](https://codeforces.com/problemset/problem/69/A) | CF 69A | Vector sum = 0 |
| 2 | [Nearly Lucky Number](https://codeforces.com/problemset/problem/110/A) | CF 110A | Counting digits |
| 3 | [Insomnia cure](https://codeforces.com/problemset/problem/148/A) | CF 148A | Inclusion-exclusion lite |
| 4 | [Drinks](https://codeforces.com/problemset/problem/200/A) | CF 200A | Average |
| 5 | ⭐ [Apartments](https://cses.fi/problemset/task/1084) | CSES 1084 | Greedy / two pointer |
| 6 | [Lemonade Stand](https://leetcode.com/problems/lemonade-change/) | LC 860 | Greedy change-making |
| 7 | [Assign Cookies](https://leetcode.com/problems/assign-cookies/) | LC 455 | Sort + greedy |
| 8 | [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/) | LC 121 | Running min |
| 9 | [Best Time to Buy and Sell Stock II](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-ii/) | LC 122 | Greedy local gains |
| 10 | [Daisy](https://usaco.org/index.php?page=viewproblem2&cpid=1060) | USACO Bronze | Counting |
| 11 | [Maximum Units on a Truck](https://leetcode.com/problems/maximum-units-on-a-truck/) | LC 1710 | Sort + greedy |
| 12 | [Stick Lengths](https://cses.fi/problemset/task/1074) | CSES 1074 | Median minimizes sum |

---

## 1.7 Basic Recursion 🟡 P3

**Topics**: Understanding the call stack, base cases, recursive thinking (break a problem into smaller identical sub-problems), simple recursive implementations.

**Patterns**:
- Every recursion needs a **base case** (when to stop) and a **recursive case** (how to reduce).
- "Compute f(n) using f(n-1)" is the simplest pattern.
- Recursion depth > ~10^4 can cause stack overflow — be aware.

**Classical Questions**: Factorial, Fibonacci, Tower of Hanoi, power function.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Power of Three](https://leetcode.com/problems/power-of-three/) | LC 326 | Recursive check |
| 2 | [Climbing Stairs](https://leetcode.com/problems/climbing-stairs/) | LC 70 | Fib recursion → DP |
| 3 | [Fibonacci Number](https://leetcode.com/problems/fibonacci-number/) | LC 509 | Classic recursion |
| 4 | [Pow(x, n)](https://leetcode.com/problems/powx-n/) | LC 50 | Fast power recursion |
| 5 | [Recursive Digit Sum](https://leetcode.com/problems/add-digits/) | LC 258 | Digital root |
| 6 | ⭐ [Tower of Hanoi](https://cses.fi/problemset/task/2165) | CSES 2165 | Classic recursion |
| 8 | [Apple Division](https://cses.fi/problemset/task/1623) | CSES 1623 | Brute force via recursion |

---

## 1.8 Parity, Invariants & Pigeonhole 🟢 P4

**Topics**: Using parity (odd/even) arguments to prove impossibility, identifying quantities that never change under allowed operations, Pigeonhole principle for existence proofs.

**Patterns**:
- "Is it possible to reach state X?" → Check if some invariant (like parity of a sum, or XOR) is preserved.
- Chessboard coloring: placing a domino always covers one black and one white cell.
- Pigeonhole: N+1 items in N boxes → at least one box has ≥ 2 items.

**Classical Questions**: Tiling a chessboard with removed corners, swapping adjacent elements and parity of inversions.

| # | Problem | Source | Notes |
|---|---------|--------|-------|
| 1 | ⭐ [Watermelon](https://codeforces.com/problemset/problem/4/A) | CF 4A | Parity |
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
| 🔴 P1 | I/O & Data Types, Simple Math, Basic Strings |
| 🟠 P2 | Arrays & Sorting, Simulation & Ad-Hoc |
| 🟡 P3 | Intro to Greedy, Basic Recursion |
| 🟢 P4 | Parity, Invariants & Pigeonhole |

**Total problems in Tier 1: ~99**

> ✅ **Checkpoint**: Before moving to Tier 2, you should be able to solve most CF Div.2 A problems (800-rated) within 10–15 minutes.
