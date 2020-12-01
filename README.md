# Blackjack simulations with parallel processing

## Description

In this repository, we consider a specific blackjack scenario in
which the player (me, I suppose) is dealt two 8's, and the dealer
shows a 9. To determine the optimal strategy (hit vs. stand vs. split),
we run 20,000 simulations of each strategy and analyze the outcomes.

Though this project is quite short, the code in this repository is meant
to showcase:

- Parallel processing with the `parallel` package in R
- Efficient use of functions, which build on each other to perform 
increasingly complex tasks

## Simplifying assumptions

To keep the focus on coding vs. the intricacies of blackjack, we make the
following simplifying assumptions:

- Assume one dealer and one player
- Assume it is always the start of a new shoe (set of 7 card decks) and you
  have 8, 8; the dealer shows a card valued at 9
- If you choose to "hit", you will continue to "hit" until you reach at least
  17
- The dealer will always "hit" until 17 or above is reached
- If after a "split", you have 8, 8, then you will "split" again
- In the event of a "split", if more hands are won than lost, this is a "win"
  If more hands are lost than won, it is a "loss". Otherwise, it is a push
- Aces count as 1 or 11. If one of the possible values gives you at least 17,
  then you must "stand". For example, if you "split" and get 8, Ace, this
  counts as 9 or 19. In this case you must take Ace as 11 and stand per the
  assumption above. The same holds for the dealer
  
## Potential extensions

There are several ways in which this project could be extended:

- Remove one or more of the assumptions listed above
- Allow for more potential starting hands than 8 and 8 for the player and
9 for the dealter
- Create an interactive game (e.g., through a Shiny app), providing 
probabilities of success to users along the way but allowing said users
to make their decisions

## Acknowledgements

This project was completed as part of STA 523 (Statistical Programming) at 
Duke, taught by Professor Shawn Santo. While the code for this portion of the
project is completely my own, two of of classmates, Cathy Shi and Guanqi Zeng,
provided valuable problem-solving support.
