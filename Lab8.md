Lab8
======

Scientific Computation 10/30/15

Beating the [word ladder game](https://en.wikipedia.org/wiki/Word_ladder) and its variations.

The original implementation was taken from https://github.com/networkx/networkx/blob/master/examples/graph/words.py

The results of running the original implementation was:

Loaded words_dat.txt containing 5757 five-letter English words.

Two words are connected if they differ in one letter.

Graph has 5757 nodes with 14135 edges

853 connected components

Shortest path between chaos and order is
13
chaos

chats

coats

colts

colas

codas

codes

coder

cider

eider

elder

older

order

Shortest path between nodes and graph is
10

nodes

modes

moles

molds

golds

goads

grads

grade

grape

graph

Shortest path between moron and smart is
17

moron

boron

baron

caron

capon

capos

capes

canes

banes

bands

bends

beads

bears

sears

stars

start

smart

Shortest path between pound and marks is
None

I then edited the code (words1.py) to work on a list of 4-letter words:
These are the following results on two tests:

Loaded words4.dat containing 2174 four-letter English words.

Two words are connected if they differ in one letter.

Graph has 2174 nodes with 8040 edges

129 connected components

Shortest path between cold and warm is

5

cold

cord

word

worm

warm

Shortest path between love and hate is

4

love

hove

have

hate



There is a variation of the word ladder game where we consider two words(nodes) are 
adjacent if the number of letters that differ (not necessarily in the same position) by 1.
To beat this variation, I altered the edit_distance_one function to return a yield of every different combination of "cc" within the given word. These yields are now considered legal connections (through edges) with the original word.
These are the following results on the same test as the original:

Loaded words_dat.txt containing 5757 five-letter English words.

Two words are connected if they differ in one letter (not necessarily in the same position).

Graph has 5757 nodes with 20927 edges

306 connected components

Shortest path between chaos and order is
6

chaos

chose

whose

horse

horde

order

Shortest path between nodes and graph is
7

nodes

codes

copes

capes

gapes

grape

graph

Shortest path between moron and smart is
5

moron

morns

mores

mares

smart

Shortest path between pound and marks is
7

pound

bound

bunds

bands

banks

barks

marks
