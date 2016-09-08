# Game of Bottles

In one of the neighborhoods in Sofia, there's a very popular drinking game, called Game of Bottles.

The game is unusual, because it combines math & drinking:

* In a standard `2D` plain (usually a football field), different bottles are arranged. Each bottle has position, described by `(x, y)` coordinates.
* In order to walk between bottles, **you can use only horizontal and vertical lines** - no diagonals.
* You can visit a bottle only once.

**Your task is to find the best way(s) to walk between bottles that will give you the smallest walking distance.**

## Example

Lets have the following bottles:

* `A = (1, 1)`
* `B = (1, 2)`
* `C = (3, 3)`

* The distance between `A` and `B` is 1 (you need to go one step up)
* The distance between `A` and `C` is 4 (you need to go 2 steps to the left and 2 steps up)
* The distance between `B` and `C` is 3 (you need to go 2 steps to the left and 1 step up)

The obvious solution is taking `A -> B -> C` for total distance of 4. There is another solution `C -> B -> A` with distance 4.

## Input

* One thing you need to know is that there are going to be, at most, 9 bottles on the field.
* Another thing is that all coordinates are going to have positive `x` and `y` coordinates. Imagine the origin of the plane sitting at one of the corners of the field.

You will receive the coordinates as follows:

* First, a number `n` telling you all the points
* On the next `n` lines, space separated `x` and `y` coordinates.


```
3
1 1
1 2
3 3
```

You need to output the length of a possible solutions with the smallest walking distance:

```
4
```
