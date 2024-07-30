# Everything we know about Chrome Dino Game: From Game Mechanics to the Hacks

![Chrome Dino](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*IaADpP3fD8-oJDPHQ2vrkA.jpeg)

A small dino-shaped creature appears on our screen whenever our device is disconnected from the internet. The creature is a pixelated Tyrannosaurus Rex that runs forward to avoid objects like cacti and pterodactyls, a specific type of pterosaur from the group Pterosauria.

The game works when we click space after the screen appears and the T. Rex starts running and it goes on until the creature hits one of the objects that runs towards it. We are limited to cacti as foreign objects till we cross the score of 500 after which we can also get pterodactyls flying towards us. The difficulty level gradually increases and after we cross 700, the standard mode changes to dark mode and changes back to standard after 1400. This happens every multiple of 700.

We can pause the gameplay with Alt or F11 which also helps us switch to full-screen. Afterward, we can click the screen and resume the game.

## History of Dino Game

The Chrome Dino game is a browser game developed by Google and integrated into the Google Chrome web browser. The dinosaur represents a joke that not having an internet connection is just like living in the prehistoric Jurassic age with no technology. The members of the Chrome UX team launched the game in September 2014 with designers Sebastien Gabriel, Alan Bettes, and Edward Jung. Originally, the game wasn’t supported on older devices which is why the team updated the code and re-released it in December 2014. Apart from these, pterodactyls were also only added with a browser update in 2015. The source code of the game is available on Chromium.

## Accessing the game

The game can be accessed in three ways:

1. Turn off the internet on your computer and then input a URL in the address bar.

![No internet](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*cFaj-ig8Ir-VpbZ57BEMhA.png)

2. Type `chrome://dino` on the browser.

![Chrome Dino](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*C--vqoVkgklRxzyprGRIrA.png)

3.  Type `chrome://network-error/-106` on the browser

![network error](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*8XQzMqGm50QEeMAen7Ppeg.png)

## The Scoring System

The primary factor in determining our score in the Chrome dino game is how far the dinosaur runs. This means that the longer the dinosaur survives, the higher our score will be. As the game progresses, the dinosaur’s speed increases, resulting in a faster accumulation of points.

## Hacks to master the game

After starting the game, the difficulty level is gradually increased. This means that the speed and frequency of the obstacles increase. But we needn’t worry!!

Let’s discuss some hacks that we can use to master the game.

1. Step one is to open the game in any of the ways mentioned above.

2. Next, we need to open Chrome DevTools. We can open it by clicking right anywhere on the screen and selecting inspect from the menu that appears. Then, we need to select the tab “Console”.

![Inspect](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*YDYNUOAHz6Q7JceA4c5S8g.png)

Alternatively, we can press `Ctrl+Shift+I` and jump straight to the console tab without the hassle.

![Console](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*6jJp8sGqgrbAqjXsOqMiWg.png)

3. Now that we are in this space, we have three options:

- To increase speed
- To increase the jump strength
- To be invincible

While we suggest you apply all, it’s important to know the working of all the commands. If we decide to opt for all three, we must first go for the option to be invincible because it might be a little harder to control when only the speed and jump strength are increased.

The first line of code to enter in the console tab for invincibility is:

`let x = Runner.prototype.gameOver`

![step one](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*JIvkExJ-B5snm2qi-UqJ1g.png)

The second line must be:

`Runner.prototype.gameOver = function (){}`

After pressing enter in the second line, we will see `f(){}` in the next.

![step 2](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*Dgk6nHdVi9jNDa9vWfK-yg.png)

For speed,

`Runner.instance_.setSpeed(speed)`

![Speed](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*tEEQe7niBMsai13CpnSrnA.png)

For jump,

`Runner.instance_.tRex.setJumpVelocity(jumping_height)`

![jump](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*QAbcRdyiG_sJVNZECWzGxw.png)

## Stopping the Game After the Hack

When we apply the invincibility hack, the game keeps on going and we are going to need to stop the game at some point. Here, we restore the original `gameOver` function.

`Runner.prototype.gameOver = x`

![stop](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*zFG-lbgNxUQnRNUblgXN_g.png)

## What does this code do?

When the game is over coming into contact with a cactus or bird, `Runner.prototype.gameOver()` is called and the action is triggered. In this case, we will hear a sound and the game stops and the game over message appears.

But we will replace the gameOver function with an empty function with our code. This means that instead of hearing the sound, called the `gameOver` function, and the appearance of the message, nothing happens upon collision, allowing us to can keep running.
