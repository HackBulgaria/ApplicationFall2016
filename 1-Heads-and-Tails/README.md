# Heads and Tails

You are playing a coin-flipping game with your friend.

The rules are:

* You are doing `n` coin tosses and write down the results. `H` for heads and `T` for tails.
* The winner, after `n` tosses is the one who had the longest consecutive wins.

Write a program that takes a comma-separated string of `H` and `T` and outputs:

* `H wins!` if `H` wins according to the game rules.
* `T wins!` if `T` wins according to the game rules.
* `Draw!` if there is no winner.


## Examples:

* Input: `H, H, H, H, T, T, T`
* Output: `H wins!`

----

* Input: `H, H, H, H, T, T, T, T`,
* Output: `Draw!`

----

* Input: `H, T, H, T, T, H, T`,
* Output: `T wins!`
