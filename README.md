# SOS-Function
A recursive fast growing function called Step Order Shuffle 
Step Order Shuffle Function: SOS(n, N)

Overview

SOS(n, N) (Step Order Shuffle) is a recursive, probabilistic function that grows at an extreme rate. It is simple to define but creates explosive complexity and depth. For small values of n and N, the function may exceed known fast-growing functions like the Ackermann function, TREE(3), and even the Busy Beaver function.

Setup

You begin with N decks of cards.

Each deck contains N unique cards in a fixed initial order.

At each step, every deck is shuffled randomly and independently.

SOS(0, N)

Shuffle all N decks simultaneously.

Repeat this step until all N decks match — i.e., they are in the exact same card order.

Define this initial sequence of shuffles (from the start until the first match) as H0.

SOS(0, N) is the expected number of steps until this first match occurs.

SOS(1, N)

Continue shuffling all decks.

Wait until the entire sequence H0 reappears spontaneously and exactly.

After H0 is reproduced, continue shuffling.

Each time a full deck match occurs, record the permutation of cards.

Continue until all N! possible match permutations have been seen at least once.

Record the order in which these N! match permutations occurred — this is called p1.

SOS(1, N) is the expected number of steps required to reach this point, starting from the beginning.

SOS(2, N)

Continue shuffling.

Wait until the entire history H1 reappears exactly.

H1 includes: the initial H0, its reoccurrence, and the entire sequence of N! match permutations (p1).

After H1 reoccurs, continue shuffling.

Every time a full sequence like p1 is completed again, record the order.

Continue until every possible ordering of p1 has occurred (i.e. (N!)! sequences).

Record the order in which those were seen — call this pp1.

SOS(2, N) is the expected number of steps to complete this process.

SOS(n, N) — General Case

Let Hn−1 be the full shuffle history up to the end of SOS(n−1, N).

Shuffle until Hn−1 spontaneously reappears, exactly.

After it does, begin recording sequences like p...p1 from level n−1.

Continue until all possible permutations of these sequences have occurred.

SOS(n, N) is the expected number of steps to reach this point.

Cumulative History Rule (Critical)

At every level n, the history Hn includes:

Every single shuffle from the very beginning of the game, including failed attempts.

All previous history reappearances, match sequences, and permutation tracking phases.

This means each level n becomes exponentially harder — and the entire prior chaos must reappear exactly before proceeding.

Growth Behavior

Even SOS(2, 2) grows beyond astronomical size.

The growth of SOS(n, N) vastly outpaces:

Ackermann(n)

Graham's number (for fixed N)

TREE(3)

Busy Beaver BB(n)

It may become non-computable or non-total for large n, due to recursive history explosion.

Why It’s Interesting

Defined with simple rules.

Grows faster than most known functions.

Captures the recursive explosion of both history and permutation.

Could open new avenues for studying complexity, probability, and recursion.

Author

Created by Jacob Hatton. For questions, contributions, or explorations, feel free to open an issue or submit a pull request.

License

This project is licensed under the MIT License — you are free to use, modify, and distribute it with proper attribution.

