---
title: "Start the game"
date: 2020-02-10T13:24:17-07:00
draft: false
weight: 2
---

Let's start by fixing the start screen so that when we press the space bar the game will start.
       
<!-- ### Working Together

In the Replit window below, we started the code with the line `game.load.image('bird', 'assets/bird.png');`.

![alt text](../img/loadbird.png "image to add the bird in the file")

In your console you should see a Jsappy bird after you press **run** and then the space bar:

![alt text](../img/loadbird_output.png "bird image in the output") -->

### How do we start the game?

Navigate to the `start-screen.js` file.  You can find it on the left side in the file list. 

This file sets up the start screen for the JSappy bird game. There's some code in here, but all you need to know is that it sets the background color and text for the starting screen in the game.

Go ahead and click `Run`.  You should see a blue box on the right side with the text `Press Space to Start` in it.  However, if you press the space bar, the game doesn't start.

### Activity 1: Start when space key is down

Our task here is to start the game when the space key is pressed.  We are storing a variable called `spaceKey` that stores the space key input from your keyboard.  We just need to find a way to use it!

Let's add this code in line after the comment for `ACTIVITY 1:`:

``` javascript
spaceKey.onDown.add(startGame, this);
```

Try hitting `Run` after adding that code and you should see the start screen load again. If you hit the spacebar now, you should see our little bird appear on the screen. Our next steps will be to get our bird to move and jump.

<!-- ### Working Together

In the Replit window below, we started the code with the line `var text = game.add.text(0, 0, "Press Space to Start", textOptions);`.

![alt text](../img/startscreen.png "image to add the bird in the file")

In your console you should see `Press Space to Start` after you press **run**:

![alt text](../img/startscreen_output.png "bird image in the output") -->
