---
title: "Make the bird jump & add gravity"
date: 2020-02-10T13:24:17-07:00
draft: false
weight: 3
---

### What should we do with the bird?

First, we need to have the bird falling by default.  To do this, our bird needs some weight, or `gravity`, to have it continuously fall down when a player doesn't press the space bar. 

Let's do this by going to the file: `create-game.js`.  This file helps us create important parts of the main game. You'll see some code already there that adds the bird to the screen and has it tilt down slightly. 

### Activity 2: Fall, bird, fall!

Look for the `Activity 2` comment and below that, we're going to add some gravity to have the bird fall by default. 

``` javascript
bird.body.gravity.y = 900;
```

This code looks for our bird we've added on the screen and adds some gravity on it's body in the `y` direction, or vertically. Hit `Run` to see if the bird falls automatically now. 

> Challenge: Try different values to have the bird fall faster or slower! 

### Activity 3: End the game if the bird is out of bounds

Uh oh - the bird has disappeared and the game hasn't ended.  What do we do? 

We need to tell the game to end the game when the bird goes off-screen, or out of bounds.  

Look for the `Activity 3` comment slightly below the `Activity 2` comment.  We need to add some code to tell our game to end when the bird goes out of bounds. 

``` javascript
bird.events.onOutOfBounds.add(endGame, this);
```

Hit `Run` to see what happens.

### Actiity 4: Let's make the bird jump
Now that the game ends if the bird goes out of bounds, let's make sure we can add some way of keeping the bird in bounds.  Let's add some code so the bird can jump. 

Look for `Activity 4` comment, slightly below the `Activity 3` comment.  

``` javascript
spaceKey.onDown.add(jump, this);
```

Hmm, if you hit `Run` it's doing something now, but it's still not jumping properly. 


### Activity 5: Fix the jump
We need to fix the jump functionality.  To fix, we basically need to add some speed upwards to the bird so it goes upwards instead of falling down. We set `gravity` before to have it fall down and now to move the bird in a direction (in our case, up) we need to set something called the `velocity` of the bird.  The `velocity` helps simulate a jump for the bird. 

Scroll down until you see the `jump()` function and within that you should see a comment for `Activity 5`.  Under that comment add:

```javascript
bird.body.velocity.y = -350;
```

What happens when you hit `Run` now?

### Optional Activity 6: Can we add sound?
Let's have each jump make a sound effect. We need to do this in two steps: first we need to add some audio for the jump to the game, then second we have to play the sound when the bird jumps.

To do this, let's scroll down to `Activity 6` still within the `jump()` function.  Under the comment, let's add the audio:

``` javascript
// Add jump sound
jumpSound = game.add.audio('jump');
```

Next, let's play the sound! Hit enter after the line you just added and on the next line add:

``` javascript
// Play the jump sound
jumpSound.play();
```

Hit `Run` to hear the sound of jumping.

<!-- 
### Working Together

In the Replit window below, we started the code with the line `spaceKey.onDown.add(jump, this);`.

![alt text](../img/jump.png "image to add jump down")

In your console you should see a Jsappy bird jumping after you press **run**:

![alt text](../img/jump_output.png "Image of jumping bird")

## Add gravity
### Working Together

In the Replit window below, we started the code with the line `bird.body.gravity.y = 900;`.

![alt text](../img/gravity.png "image to add gravity to the bird")

In your console you should see a JSappy bird jumping with gravity after you press **run**:

![alt text](../img/jump_output.png "bird jumping with gravity") -->

