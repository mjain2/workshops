---
title: "Add scoring & let's play!"
date: 2020-07-29T13:24:17-07:00
draft: false
weight: 5
---

We're almost there! Now, we just need to add to the score when the bird passes through the pipes. We also need to make sure that if the bird hits the pipe, the game ends. 

Let's find the file `update-game.js` on the left side and open it.  The code here updates things in the game while the game is still running.

### Activity 8: Update score
Let's start by updating the score when the bird goes through the pipe. Find the `Activity 8` comment (near line 26). On the line after, let's add some code.

``` javascript
score = score + 1;
```

### Activity 9: Game over if you hit a pipe!
Let's also add some code so that if a bird and pipe overlap the `hitPipe` function is called, which will essentially end the game. This change is a bit complicated as we need to take into account the physics of the game so that if the two objects of `bird` and `pipes` overlap, we trigger the `hitPipe` function. 

Let's add this to below the `Activity 9` comment a little further down.

``` javascript
game.physics.arcade.overlap(bird, pipes, hitPipe, null, this);
```

Hit `Run` now - the score should update and the game should end if you hit the pipe!


### Optional Activity 10: Add sound to when you hit a pipe
We can also add some audio to indicate the bird has hit a pipe! Find the `Activity 10` comment in the `hitPipe` function near the bottom of the `update-game.js` file. 

Here, let's do something similar as jump and add some audio for when the bird hits the pipe.

``` javascript
// Add hit sound
hitSound = game.add.audio('hit');

// Play hit sound
hitSound.play();
```

#### Congratulations, you've made a flappy bird game! What's the highest score you can get? 

# Bonus activities

{{% notice note %}}

- What happens if we make gravity stronger?
- What happens if we make gravity have a negative value?
- What other wacky ways can the bird jump?
- How can we make him rotate quicker?
- What happens if we remove the 'if' around the rotation?

{{% /notice %}}