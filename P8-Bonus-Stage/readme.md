# Welcome to bonus stage

Welcome to bonus stage! Your task, should you accept, is to work through the list of challenges and take your game to the next level.

There are no solutions provided and I would encourage you to discuss potential solutions with your fellow students, it's good to collaborate and often results in new exciting directions.

It would be a good idea to create a **new branch** in your repo for these challenges.

# Mechanical Improvements

There are a couple issues that might cause problems if the game is played for more than points. Sushi Pieces are added and increment their z-position. This means that after a number of pieces are added pieces will eventually appear above other elements, like the cat, button, score, and life bar. 

This line in `addTowerPiece(side:)` points to the problem: 

```Swift
newPiece.zPosition = lastZPosition + 1
```

Here each new piece is assigned the last z-position + 1. 

Here are a couple solutions you could use to solve this: 
- Create an empty node, and use it as the parent element for sushi pieces. Pieces would inside that node at their z-position, outside the node they will stack at the z-position assigned to the node. 
- Reset the z-position of all pieces when adding a new piece. You could do that in `addRandomPieces(total:)`. This would keep all of the pieces at a z-position of 1 to 10 (or the number of pieces you have), other nodes that need to stack on top would need a z-position greater than the number of pieces. 

After following the tutorial, I notice I need to tap the play button twice to continue the game. Could be an error on my part, or it could have something to do with the `gameState`. 

Hiding the play button while playing the game, and show the button after the game is over would be a big improvement. 

# Improve Gameplay

The game was pretty hard to play using the values in the tutorial. Editing the amount the health bar decreases and the amount of health added with each pieces removed, can go a long way to improving the fun and playability. 

# Improve the main menu

The main menu is a little boring, just a play button.  Although this is certainly functional it would be nice to dress this up and at the very least display the game title.

> [challenge]
> Improve the main menu intro, one idea might be the mat could roll down the screen and display a **Sushi Neko** title using an *SKLabel*.
> **Hint**: Take a look at *mat.png*

#Game over

When the game ends there is no real fan fare, why not use some of the skills employed in the last chapter?

> [challenge]
> Improve the game over stage.

#Sushi variety

How about adding a little variety to the sushi?

> [challenge]
> Can you create different types of sushi, perhaps some of these have different point values or even change the game in some way.

#Game Center

This challenge is a bit more advanced.  However, as a developer you need to challenge yourself to progress.  You should be familiar with using Google to help solve problems, it will come in handy I'm sure :]

Here is a good starting place.  [Game Center](https://developer.apple.com/game-center/)

> [challenge]
> Implement a Game Center high score mechanic and for a further challenge add achievements.

#Summary

Congratulations on completing the bonus stage!
