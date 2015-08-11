##Memory Game

The classic game of matching cards powered by Backbone.js. Play at <a href="http://younglearnersguide.com/memory.html">younglearnersguide.com/memory.html</a>

###Description

Flip The Cards and Remember What They Are To Match Them - THE GAME is my take on the classic game of Memory (or Concentration depending on where you grew up). The game play is the same as you may remember: reveal two cards at a time. Clear the board by matching all the pairs. Unmatched cards are flipped back over, leaving it on you to remember where each color is.

###Gameplay

The game has been spiced up in a few ways. Your score counts down from 1000. A mismatched pair subtracts 25 points, while a match gets you a bonus of 50. Final scores are tallied in the Winnerboard.


###Build Notes

The game was designed to be responsive to different screen sizes so the cards will change size. That said, I like keeping the cards vertically-oriented rectangles, hence the central container column.

I toyed with intervals to hide two revealed cards, but that left me with the problem of users clicking faster than the interval timer. For simplicity and error-prevention I opted to build an internal counter that hides any revealed cards only after a third card is clicked.
