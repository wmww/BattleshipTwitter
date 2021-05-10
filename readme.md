# BattleshipTwitter (bst)

__You are not required to fully understand these rules in order to play.__ Gameplay is not automated and the host will explain things as you go. Feel free to read this whole doc now, or just consult it when needed.

## Overview
These are the rules for a turn-based game inspired by Battleship and optimized to be played on Twitter. The game can have many players and is played over a period of hours or days. All players are on a single shared board.

## #bst hashtag
In the interest of making this as unobnoxious as possible to those not interested, all host tweets will contain `mute #bst to hide BattleshipTwitter`. All tweets relating to the game should also include `#bst` so they get caught by the mute as well.

## Board
The board can be any size. For my first game I'm going to use a board that's 20x20. I estimate this will be suitable for about a dozen players. I might let in more for additional chaos.

## Setup
Each player gets two ships. They may choose either:
- an aircraft carrier (5 long) and a submarine (1 long), or
- two cruisers (3 long each)

A player starts by DMing the host the desired initial position of both ships. For example:
```
sub: A2
carrier: C1-C5
```
would request a submarine in the top-left and an aircraft carrier below it.

Keep in mind that if you request a cruiser to be flush with the edge of the board, or an aircraft carrier along the edge within 1 square, you won't be able to rotate it to move it elsewhere. It will be stuck on that edge.

### Initial Placement Collisions
Since all players are on a shared board, there's a chance of two players requesting ships on the same square. If this happens, both players are alerted of the conflicting ship and can request new positions for both their ships. They may re-request the same positions if they desire.

__TODO: this won't work. On a 20x20 if you do the math, only ~7 players can place their ships before, on average, every new ship causes an avalanche that forces every ship to move.__

## Turns
Like original Battleship it's turn-based, but unlike the original all player's actions are executed simultaneously. A turn lasts 8 hours (unless the host slept in, in which case it could be a little longer). Players may declare their action at any time during the turn. There's no penalty for missing a turn except the lost opportunity to do something.

## Actions
Each turn each player can do exactly one of four things:
- Nothing (the default if they don't specify anything)
- Shoot
- Rotate
- Move forward or backward

### Shooting
This is done by publicly commenting the square you want to shoot at, for example:
```
#bst H14
```
On the next turn the map will show your twitter avi in the location you shot, and indicate if it was a hit or a miss.

### Rotate
You may rotate at most one of your ships 90° around it's center. There is not a distinction between the bow and stern, so rotation direction is irrelevant. Submarines do not have an orientation and so do not need to be rotated.

Moves and rotations should be sent as DMs to the host:
```
rotate carrier at E8
```

### Move
You may move a ship forward or backward up to the length of the ship. Submarines do not have an orientation, so can move one square in any of the four directions.

Moves and rotations should be sent as DMs to the host:
```
move cruiser at G7 3 up
```

If a move results in a collision, affected ships are stopped where they collide and are informed.

## Destroying Ships
When a ship gets hit, that spot is permanently damaged. Future hits to the same spot register as hits, but don't inflict additional damage (unlike the original game, this can happen because ships move). When all spots on a ship are damaged, the ship is destroyed.

When a ship is destroyed it appears on the public map, and its player is visible. It sticks around and can no longer be moved. When both of a player's ships are destroyed the player is out of the game.

## Win Condition
Last player standing with at least one non-destroyed ship wins.

## Host Duties
The host keeps track of the state of the board, and reports info both publicly and privately. Each turn the host posts a game board showing where players shot and if each shot was a hit or a miss. After initial placement and when players move, the host DMs them a board showing just their ships. At the end the host publishes a video showing the location of all ships throughout the whole battle.

## Unofficial Alliances, Strategizing Publicly, Strategizing Privately, Trash Talk, Psyops, and Metagaming
Encouraged