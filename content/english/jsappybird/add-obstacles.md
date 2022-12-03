---
title: "Add the obstacles for the bird to avoid"
date: 2020-07-29T13:24:17-07:00
draft: false
weight: 4
---

Our bird is jumping now.  Next, we need to add the pipe obstacles for the birds to avoid.

### Activity 7: Add obstacles
There are two ways to do this: we can either move the bird forward or move the obstacles towards the bird.  We're going to go ahead and move the obstacles towards the bird to make things a bit simpler. 

Let's go ahead and open `add-obstacles.js` now.  There's a bunch of code in here to create the pipe obstacles for the game.  The part we are missing is near the bottom of the file around line 42.  We need to have the pipes move left so they appear on the screen for the bird to avoid.

We've moved something before - we moved the bird when we needed it to jump! Similarly, we're going to move the pipes left. Thus, we need to again use the `velocity` to setup movement. Let's set the x-velocity to -250.

``` javascript
pipe.body.velocity.x = -250;
```

Hit `Run` to see if the pipes show up now that you added code to have them move left.