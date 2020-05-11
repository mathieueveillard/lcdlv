# Othello

[Othello](https://en.wikipedia.org/wiki/Reversi#Rules) is a board game for two players. This kata requires you to write a function that, given the current board and the current player, computes the list of all possible moves. Bellow is an example.

Assuming the given board (`W` stands for white disks, `B` for black ones):

```
  A B C D E F G H
1 . . . . . . . .
2 . . . . . . . .
3 . . . . . . . .
4 . . . W B . . .
5 . . . B W . . .
6 . . . . . . . .
7 . . . . . . . .
8 . . . . . . . .
```

Blacks start ; the possibles moves are:

```
(D,3), (F,5), (E,6), (C,4)
```

We're going to build the solution from the "inside" to the "outside" (the final expected behavior), as we would do while playing Lego:

1. Write a `isValidMoveForDirection(board, player, position, direction)` function that returns `true` if the given `player` can flip at least one of their opponent's disks by placing a disk of their assigned color at `position`, given the current `board` (`false` otherwise).
2. Write a `isValidMove(board, player, position)` function that returns `true` if `player` can make the move at `position` given the current `board` (`false` otherwise).
3. Write the final `getPossibleMoves(board, player)` function that returns the list of all valid moves for `player` by iterating over the current `board`.

[A possible solution](https://github.com/mathieueveillard/othello-js)
