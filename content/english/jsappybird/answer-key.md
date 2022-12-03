---
title: "Answer Key"
date: 2020-02-10T13:24:17-07:00
draft: false
hidden: true
weight: 15
---

#### Activity 1: start-screen.js
``` javascript
spaceKey.onDown.add(startGame, this);
```

#### Activity 2: create-game.js
``` javascript
bird.body.gravity.y = 900;
```

#### Activity 3: create-game.js
``` javascript
bird.events.onOutOfBounds.add(endGame, this);
```

#### Activity 4: create-game.js
``` javascript
spaceKey.onDown.add(jump, this);
```

#### Activity 5: create-game.js -> jump()
``` javascript
bird.body.velocity.y = -350;
```

#### Activity 6: create-game.js -> jump()
``` javascript
jumpSound = game.add.audio('jump');
jumpSound.play();
```

#### Activity 7: add-obstacle.js (line 42)
``` javascript
pipe.body.velocity.x = -250;
```

#### Activity 8: update-game.js
``` javascript
score = score + 1;
```

#### Activity 9: update-game.js
``` javascript
game.physics.arcade.overlap(bird, pipes, hitPipe, null, this);
```

#### Activity 10: update-game.js
``` javascript
// Add hit sound
hitSound = game.add.audio('hit');
// Play hit sound
hitSound.play(); 
```
