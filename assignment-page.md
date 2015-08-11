## Backbone Views

### Description

Backbone is a framework that's happy to be used piecemeal. We've spent time earlier this week learning about Backbone models and collections; today we learned about Backbone views. Views and models work amazingly together, but let's get comfortable with views themselves before we smush everything together next week.

### Normal Mode

Let's build a Backbone View-based version of the game [Concentration](https://en.wikipedia.org/wiki/Concentration_(game)). (You may know it by some other name, or just as "that flip over cards and find matching pairs game".)

The basic rules of the game are that pairs of cards are shuffled together, and dealt face down. Players can turn over a single card at a time. When two cards are turned over, if they have the same face, then they're removed from the board. If they're dissimilar, both are placed back face down where they originally were. The goal of the game is to remove all pairs from the board.

Flesh out the Card class in `card.js` that's extending Backbone.View. It should have some property that it accepts during `initialize` which tracks the card's color; it should also have some property/ies that track's the card's state of being flipped face down/flipped face up/"removed" from the board.

In the `index.js` file, there's an array being created of 16 new instances of the Card class, with two each of eight colors; those instances are getting appended into the game. You shouldn't need to edit that section of the code, but you will probably want to do some other work in that file to manage the game state (so that when two cards are flipped over they're other turned face down or "removed").

All sixteen cards should fill the entire page and all be displayed at once, regardless of window size. You can take advantage of the height and width properties with display:inline-block to make this pretty easy.

### Hard Mode

Once you're done with Normal Mode, try to turn this into an actual game. With, like, scorekeeping and everything.

Create a visible "timer" somewhere on the screen that counts down from, lets say, 1000 points. For every second that passes between the start of the game and the end of the game, remove 10 points from the score. (See if you can break it down so it removes 1 point at every tenth of a second.) For every non-matching pair that you need to flip back over, remove 25 points from the score. The user should see their score descending in real time.

When the game is over, let the user know what their score is so they can try to beat it next time.