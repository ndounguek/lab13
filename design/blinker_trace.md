# Blinker hand trace

Patch: rows 3-7, columns 8-12. `#` = alive, `.` = dead.

## Generation 0: (4,10) (5,10) (6,10)

        8 9 10 11 12        Neighbor counts
    3   . .  .  .  .        0 1 1 1 0
    4   . .  #  .  .        0 2 1 2 0
    5   . .  #  .  .        0 3 2 3 0
    6   . .  #  .  .        0 2 1 2 0
    7   . .  .  .  .        0 1 1 1 0

- (4,10) and (6,10): alive with 1 neighbor -> die
- (5,10): alive with 2 -> survives
- (5,9) and (5,11): dead with 3 -> born

## Generation 1: (5,9) (5,10) (5,11)

        8 9 10 11 12        Neighbor counts
    3   . .  .  .  .        0 0 0 0 0
    4   . .  .  .  .        1 2 3 2 1
    5   . #  #  #  .        1 1 2 1 1
    6   . .  .  .  .        1 2 3 2 1
    7   . .  .  .  .        0 0 0 0 0

- (5,9) and (5,11): alive with 1 -> die
- (5,10): alive with 2 -> survives
- (4,10) and (6,10): dead with 3 -> born

## Generation 2: (4,10) (5,10) (6,10)

        8 9 10 11 12
    3   . .  .  .  .
    4   . .  #  .  .
    5   . .  #  .  .
    6   . .  #  .  .
    7   . .  .  .  .

Same as generation 0: the blinker has period 2.
