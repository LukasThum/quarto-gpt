# the board game quartro
i want to define a notation for the boardgame quatro that i'm sure you are
familliar with. the game will be played via a chat system.

## board
the board is made of 4x4 squares. the squares are numbered
like on a chess board but half the size.

## pieces
the pieces are defined by a string of four characters that define their features.
the features are:
 1. bright (b) and dark (d)
 2. tall (t) and short (s)
 3. circle (c) and rectangular (r)
 4. flat (f) and hole (h)

so the bright, tall, rectangular and hole piece would be btrh. the order of the
features in this representation always has to be preserved.
however, when i input a piece in chat it might not be in this order.

## moves
for a move to play out the player who's turn it is to choose a piece for the
opponent writes that piece to chat. the player who has to place it then has to
write the position to chat. the game plays out as described in the rules, players
take turn in choosing a piece or placing it until one player has won.

## board representation in ascii
you should always output the current state of the board when you print to chat.
this way i can always tell the state of the game, too.

### in game
this is what a running game could look like, notice the fact that every square
is 5 chars wide, even if emtpy. this is to ensure the board is readable.
the first char can be used to add information to the board (like winnning
lines by exclamation mark, mentioned later). it could also be used as a way
for you to give me hints of maybe an order of piece placement.

```diff
--+-----+-----+-----+-----+
4 | brht|     |     |     |
--+-----+-----+-----+-----+
3 |     |     | drhs|     |
--+-----+-----+-----+-----+
2 |     | brhs|     |     |
--+-----+-----+-----+-----+
1 | brhs|     |     | drhs|
--+-----+-----+-----+-----+
  |  a  |  b  |  c  |  d  |
```

### end of game
this is how you would represent a winning row (in this case all pieces are
bright) by adding exclamationmarks on the left of the pieces:

```diff
--+-----+-----+-----+-----+
4 |!brht|     |     |     |
--+-----+-----+-----+-----+
3 |!bcht|     | drhs|     |
--+-----+-----+-----+-----+
2 |!brhs|     |     |     |
--+-----+-----+-----+-----+
1 |!brhs|     |     | drhs|
--+-----+-----+-----+-----+
  |  a  |  b  |  c  |  d  |
```

ok then, we will play a game against each other, the board is emtpy, let's begin!
