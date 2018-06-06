# 8-Queens
Solution to 8 queens problem

This is another project that I wanted to implement just for fun. The problem is putting 8 queens on the chess board so
that none of them attack each other. To make it more visual I looked up and used PyQt and PyGame libraries.
Here is the solution - all 92 of them:

![ScreenShot](/screenShots/8queens.gif)


The main idea for solving the 8 queen problem is using some constraints rather than implementing exhaustive search. The first 
queen is placed in the first column, the second one is placed in second column in a manner such that it is not attacked by the
first queen, the third one is placed in 3rd row so that the first two do not attack it and so on until the solution is obtained.
Of course more often than not, we come to the dead end and can't place the next queen even though the board is not filled.
So we backtrack to the previous position and try other possible squares in the last row.

Just to ephasize the efficiency of this approach one can compare it to to the naive solution, where the first queen is placed on
any of the 64 squares, the second one is placed on any of the remaining 63 and so on. That will give us 
Chose(64,8) = 64!/((64-8)!*8!) = 4,426,165,368 positions to consider. The reduced space is only 2056!
