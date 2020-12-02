# Carpet

Carpet Mod is a mod for vanilla Minecraft that allows you to take full control of what matters from a technical perspective of the game.

[FULL MOD DESCRIPTION](https://youtu.be/Lt-ooRGpLz4)


---

## Cam-mode

The command to switch between spectator and survival mode is dependent on a SCARPET app called [cam.sc](https://github.com/gnembon/scarpet/blob/master/programs/survival/cam.sc), and once loaded, you can just type `/cam` to toggle between gamemodes. If "cam" is too long for you, just change the name of the file to whatever you want.

Command in app is fully customizable: by default, it functions as a "fair camera mode", meaning it can't be used to escape death, by means of the following features, all of which can be disabled:
* It has a timer (default 3 seconds) so players cannot switch instantly. Set `global_survival_timeout = 0;` in line 8 to disbale this.
* Player needs to be on the ground to switch to spectator. Delete or comment (add `//` in front) line 13 to disable.
* Player can't be drowning. Delete or comment line 14.
* Player can't be on fire. Delete or comment line 15.
* Player is placed back in its original position (also preserving motion and angles) after switching back to survival.

---

## Commands

This is the commands page explaining the commands in carpet mod. Here all commands are listed and their functions are described.

---

#### General Carpet Settings Command (requires default OP privileges)

Manages Carpet rules and settings.

##### Usage: `/carpet`

Displays the current version of carpet mod, the current non-vanilla rules and lists the categories in chat

##### Usage: `/carpet list defaults`

Lists the default configuration for this world stored in carpet.conf

##### Usage: `/carpet list`

Lists all available carpet rules

##### Usage: `/carpet list [category]`

Lists all available carpet rules in the specified category

##### Usage: `/carpet removeDefault [rule]`

Removes the custom default configuration for the specified carpet rule on that world and restores it back to the vanilla default

##### Usage: `/carpet setDefault [rule]`

Sets the default value for the specified carpet rule to the given value

##### Usage: `/carpet [rule] [value]`

Sets the specified carpet rule to the specified value. This will be restored to the default configuration for this world stored in carpet.conf if not done with `setDefault`

---

### Distance command

Useful to calculate distances between two points. Comes with an accompanying carpet: the brown one.

##### Usage: `/distance from [start] to [end?]`

Returns the Spherical, Cylindrical and Manhattan distance between the specified coordinates. If `to` is not specified, uses current executor position

##### Usage: `/distance from [start?]`

Remembers starting coordinate for the player. If used without coordinates, current executor position is used.

##### Usage: `/distance to [end?]`

Prints distances to the target position assuming starting position remembered from `from` commmand. If used without coordinates, current executor position is used.

---

### Draw

Builds simple but painful to build shapes with blocks.                                                                                                                                                                                                                                     

**NOTE: Since the last update of this page, many new shapes have been added. Check auto-complete in-game.** (TODO: update)

##### `Usage: /draw sphere [center] [radius] [block]`

Makes a sphere with the specified radius around the specified center coordinate out of the specified block

##### Usage: `/draw sphere [center] [radius] [block] replace [block/tag]`

Makes a sphere with the specified radius around the specified center coordinate out of the specified block, but only the specified block/blocks that have the specified tag get replaced

---

### Info

Gives useful information about a block. It comes with an accompanying carpet: gray

##### Usage: `/info block [coordinate]`

Gets the info for the block in the specified coordinate

##### Usage: `/info block [coordinate] grep`

Gets the specific info for the block in the specified coordinate defined in grep

---

### Log

Toggles various Carpet loggers: Information shown in various UI positions

##### Usage: `/log`

Lists the logging options in chat

##### Usage: `/log clear`

Unsubscribes the player from all logs

##### Usage `/log counter [color]`

Subscribes the player to the log of the specified counter color and shows it in their player list menu (TAB by default)

##### Usage: `/log counter clear`

Unsubscribes the player from the counter log

##### Usage: `/log fallingBlocks [brief/full]`

Logs falling blocks history of positions per tick during their lifetime (at the end).

##### Usage: `/log fallingBlocks clear`

Unsubscibes the player from the `fallingBlocks` log.

##### Usage: `/log mobcaps [dimension/dynamic]`

Subscribes the player to the mobcap log of the specified dimension or the dimension they are in if dynamic is selected. This shows the mobcaps in their player list menu (TAB by default)

##### Usage: `/log mobcaps clear`

Unsubscribes the player from the mobcaps log

##### Usage: `/log packets`

Subscribes the player to the packet log and shows incoming and outgoing packets in their player list menu (TAB by default)

##### Usage: `/log packets clear`

Unsubscibes the player from the packets log

##### Usage: `/log pathfinding [2/5/10]`

This wiki is incomplete. You can help by expanding it.

##### Usage: `/log pathfinding clear`

Unsubscibes the player from the pathfinding log

##### Usage: `/log projectiles [brief/full]`

Logs projectiles history of positions per tick during their lifetime (at the end).

##### Usage: `/log projectiles clear`

Unsubscibes the player from the projectiles log

##### Usage: `/log tnt [brief/full]`

When tnt goes boom, tells you where, when, how, why, who and what

##### Usage: `/log tnt clear`

Unsubscibes the player from the tnt log

#### Usage: `/log tps`

Subscriber the player to the TPS log and shows TPS (Ticks Per Second) and MSPT (MilliSeconds Per Tick) in the player list menu (TAB by default)

---

### Perimeter Info

Gives various information about a perimeter around a coordinate. Comes with two accompanying carpets: black and pink.

##### Usage: `/perimeterinfo coordinate`

Returns the potential spawning spaces in 128-block radius around the specified coordinate

##### Usage: `/perimeterinfo coordinate [mob]`

Returns the potential spawning spaces in 128-block radius around the specified coordinate and also the potential spawning spaces for the specified mob

---

### Tick

Gives you various ways to change the way time passes in the game

##### Usage: `/tick health [ticks]`

By default monitors the game for 5 sec/ 100 ticks. Returns the average amount of time per tick spent on various tasks by the game. These include:
* Network
* Autosave
* Off-Tick Tasks
* Mob Spawning
* Chunk Loading
* Chunk Unloading
* Block Updates
* Entity Ticks
* Block Entity Ticks
* Villages & Raids
* Environment
The total time per tick should stay below 50ms to keep the world from lagging.

##### Usage: `/tick entities [ticks]`

Works like the health command but returns the 10 entities for count and CPU time.

##### Usage: `/tick freeze`

This will stop the processing of entities, world clocks, block updates, and redstone while still letting the player move freely. Typing `/tick freeze` again will resume processing of everything.

##### Usage: `/tick step [ticks]`

While frozen you can use this command to advance the world by the given number of ticks. Note: these are game ticks, there are 2 game ticks for every redstone tick. So `/tick step 20` would advance the game 1 second because there are 20 game ticks per second even though there are only 10 redstone ticks per second.

##### Usage: `/tick rate [tps]`

Changes the rate at which things happen in the game. The default value is 20.0. Higher values make the game run faster, while lower values make it run slower. You may want to enable `smoothClientAnimations` to slow the client side animations as well.

##### Usage: `/tick warp [ticks] [cmd]`

Lets the game run as fast as it can for a set amount of time. 72000 ticks is 1 hour of game time. You can cancel the current warp by typeing `/tick warp 0`

##### Usage: `/tick superHot `

Makes minecraft work like the game of the same name. Time only advances when you move.

---

### Player

Create fake players that act almost exactly like real players. 

##### Usage: `/player <name> spawn`

Spawn a player with the given name at your current location in your current game mode

##### Usage: `/player <name> attack <continuous | interval ? | once>`

The player performs the left click equivalent action

##### Usage: `/player <name> use <continuous | interval ? | once>`

The player performs the right click equivalent action

##### Usage: `/player <name> mount`

The player rides a near by thing which is rideable

##### Usage: `/player <name> dismount`

The player gets off whatever it is currently riding

##### Usage: `/player <name> drop`

The player drops the item they are currently holding

##### Usage: `/player <name> dropStack`



##### Usage: `/player <name> jump`

##### Usage: `/player <name> kill`

##### Usage: `/player <name> look <up | down | north | south | east | west | at <x y z>>`

The player looks in the given direction

##### Usage: `/player <name> move <backward | forward | left | right>`

The player moves in the given direction

##### Usage: `/player <your name> shadow`

This will replace you with a fake player on the server. It will continue to perform any scheduled actions that you have set. This only works on servers ( not single player)

##### Usage: `/player <name> sneak`

##### Usage: `/player <name> unsneak`

##### Usage: `/player <name> sprint`

##### Usage: `/player <name> unsprint`

##### Usage: `/player <name> stop`

The player stops moving and cancels all actions the player is doing

##### Usage: `/player <name> swapHands`

The player swaps the items in their main and off hands

##### Usage: `/player <name> turn`

---

### Ping

##### Usage: `/ping`

Returns the latency of the player to the server
