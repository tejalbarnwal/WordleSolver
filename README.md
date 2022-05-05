# WordleSolver

## Introduction
We are Optimising Solution Algorithm for n-Blank Guessing Puzzles. For solving Wordle, we see that every guess has a possible set of outcomes which gives us clues as to what the solution could be.

We see that the [guess set](https://github.com/tejalbarnwal/WordleSolver/blob/main/datasets/valid_guesses.csv) (12989 words) is the superset of the [solution set](https://github.com/tejalbarnwal/WordleSolver/blob/main/datasets/valid_solutions.csv)(2315 words) and can be used to explore the solution set.  

## Approach
The main idea is to minimize the number of tries in which we reach the solution. This implies at each guess we shrink our solution set to a smaller pool increasing the probability of guessing the solution in the next try.

To scorre the remaining words, we came up three metrics:

* Letter Frequency: Captures the occurrence and position information of each individual alphabets in the solution set([Source Code](https://github.com/tejalbarnwal/WordleSolver/blob/main/dictionary_feature_finding.ipynb))

* Covariance: Encompasses occurrence of any two alphabets and returns number of words that contain the corresponding pair([Source Code](https://github.com/tejalbarnwal/WordleSolver/blob/main/covariance_finding.ipynb))

* Entropy: Is the expected information when you play a certain guess.

## Algorithm
The final alogrithm uses information theory(Entropy) and cuts the set by eliminating the words from the dataframe. The [Python source code](https://github.com/tejalbarnwal/WordleSolver/blob/main/wordle_interactive_solver.ipynb) for the same can be found here. It has been created for both manual and automatic mode.

## Contributors
1. Shivani Verma
2. Suryansh Singh
3. Sahil Malik
4. Tejal Barnwal