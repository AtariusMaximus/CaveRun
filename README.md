# CaveRun
This is the code repository for the Atari 2600 game Cave Run.

<img><img src="https://github.com/AtariusMaximus/CaveRun/blob/main/CaveRun_screenshot1.jpg">
<img><img src="https://github.com/AtariusMaximus/CaveRun/blob/main/CaveRun_screenshot2.jpg">

The object of Cave Run is to run through thirty horizontally placed screens (or "caves") and grab the treasures on each level. Some backtracking and creative jumping is required to reach some of them. Once you have collected all the treasures the final screen unlocks. If you successfully navigate the last screen you win the game. You start the game with three lives.  My notes from 2012 indicate that this release does not run correctly on real Atari hardware, but works fine in emulation on Stella.

Here's the an outline of the basics:

Obstacles:

Any of these obstacles will cause you to lose a life. When you die you "explode" like a bomb, I threw that in there from the beginning mostly because I thought it was kind of funny. I have no specific explanation as to why you explode when dying in this game. :)

The Bat. There is a bat that flies around each screen, if it touches you you will lose a life. The bat will disappear after a hit just for the screen you are on, it will reappear when you change screens.

The Pits. If you fall off the bottom of the screen you will lose a life.

Barriers. Some screens have a barrier that moves back and forth. If you hit it, it will push you to the right and could cause you to fall into a pit. Be careful to time your jumps and avoid them.

Treasures:

There are 2 treasures in each of the 31 rooms. Some move in patterns that require precise jumps, others are positioned so that you may have to fall into them to collect them, and some are static. All 62 need to be collected to win the game. You score 10,000 points for each treasure, but it's more of a way to keep track of how many you've collected. You'll end up with the same score every time if you beat the game. I used batari's 5+1 score minikernel, so the right side represents your remaining lives.

Options:

I've included an options screen at the beginning of the game that lets you choose the speed of the bat, god mode (which disables collisions with the bat and barriers), gravity and jump velocity. To choose an option, move the joystick up and down to select which option you want to change, and then push the joystick left or right to select the setting for that option. Pressing the fire button will start the game. Please note that the default options for gravity and jump velocity are what I designed the with, some platforms are placed in a very specific places that match up with the defaults. Choosing different options is fun to play around with in the game, but certain combinations of them could make the game unwinnable.

Bat Speed: High or Low. Low is the default. High simply makes the bat fly around faster.

Player Speed: High or Low. Low is the default. High makes the player run faster.

God: On or Off. Off is the default. Turning God mode on disables collision detection with the bat and barriers, and also allows you to fall into a pit and survive.

Gravity: High or Low. High Gravity is the default. Switching to Low gravity will allow you to jump farther.

Random Start: On or Off. Off is the default, you'll always start in the first room at the beginning of the map. Turning random on will cause you to start in a random location.

Velocity: High or Low. Low velocity is the default. Switching to High velocity will allow you to jump higher. High velocity jumping may make it impossible to get to certain treasures.

The Map Screen:

Press the color/BW switch (F4/F3 in Stella) to go to the Map screen. The map screen shows all 31 rooms in order from the top left down to the bottom right. It also shows your current position on the map and which rooms still have treasures in them that need to be picked up. The remaining treasures will only be shown on the current row you're in on the map screen.

 
