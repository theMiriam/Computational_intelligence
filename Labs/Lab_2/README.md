The goal of the lab is to develop an evolutionary strategy able to identify the best strategy among a range of possible strategies to play Nim.

The strategy that we thought of with Massimo Porcheddu and Paolo Mucilli  was to create many strategies and a genome that had the probability of taking them.
Therefore, to evaluate the best strategy, several games are played for each move and the best move is found after that.
For a better evaluation of the move, only the first move from that point of the nim is evaluated and then the optimal one is used to complete the pseudogame linked to that move.

There are currently 7 strategies implemented and although very simple, with the right combination they produce good results