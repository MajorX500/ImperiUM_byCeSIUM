# World Edit

**A Minecraft Map Editor... that runs in-game!**

* With selections, schematics, copy and paste, brushes, and scripting!
* Use it in creative, survival in single player or on your server.
* Use it on your Minecraft server to fix grieving and mistakes.

## Commands

Note
Arguments enclosed in [ ] are optional, those enclosed in < > are required.

Tip
You can access a command listing in-game via the //help command.


## /worldedit (or /we)
Description 	WorldEdit commands
Usage 	`/worldedit <help|version|trace|reload|cui|tz|report>`

## /undo (or //undo)
Description 	Undoes the last action (from history)
Usage 	`/undo [times] [player]`
	- [times] 	Number of undoes to perform
	- [player] 	Undo this player’s operations

## /redo (or //redo)
Description 	Redoes the last action (from history)
Usage 	`/redo [times] [player]`
	- [times] 	Number of redoes to perform
  	- [player] 	Redo this player’s operations

## /clearhistory (or //clearhistory)
Description 	Clear your history
Usage 	`/clearhistory`

## //limit
Description 	Modify block change limit
Usage 	`//limit [limit]`
  [limit] 	The limit to set

## //timeout
Description 	Modify evaluation timeout time.
Usage 	`//timeout [limit]`
  [limit] 	The timeout time to set

## //perf
Description 	

Toggle side effects for performance

Note that this command is GOING to change in the future. Do not depend on the exact format of this command yet.
Usage 	`//perf [-h] [sideEffect] [newState]`
  [sideEffect] 	The side effect
  [newState] 	The new side effect state
  [-h] 	Show the info box

## //reorder
Description 	Sets the reorder mode of WorldEdit
Usage 	`//reorder [reorderMode]`
  [reorderMode] 	The reorder mode

## //drawsel
Description 	Toggle drawing the current selection
Usage 	`//drawsel [drawSelection]`
  [drawSelection] 	The new draw selection state

## //world
Description 	Sets the world override
Usage 	`//world [world]`
  [world] 	The world override

## //watchdog
Description 	

Changes watchdog hook state.

This is dependent on platform implementation. Not all platforms support watchdog hooks, or contain a watchdog.
Usage 	`//watchdog [hookMode]`
  [hookMode] 	The mode to set the watchdog hook to

## /gmask (or //gmask)
Description 	Set the global mask
Usage 	`/gmask [mask]`
  [mask] 	The mask to set

## /toggleplace (or //toggleplace)
Description 	Switch between your position and pos1 for placement
Usage 	`/toggleplace`

## /searchitem (or //searchitem, //l, //search)
Description 	Search for an item
Usage 	`/searchitem [-bi] [-p <page>] <query...>`
  [-b] 	Only search for blocks
  [-i] 	Only search for items
  [-p <page>] 	Page of results to return
  <query...> 	Search query
Navigation Commands

## /unstuck (or /!)
Description 	Escape from being stuck inside a bl`ock`
Usage 	`/unstuck`

## /ascend (or /asc)
Description 	Go up a floor
Usage 	`/ascend [levels]`
  [levels] 	# of levels to ascend

## /descend (or /desc)
Description 	Go down a floor
Usage 	`/descend [levels]`
  [levels] 	# of levels to descend

## /ceil
Description 	Go to the ceiling
Usage 	`/ceil [-fg] [clearance]`
  [clearance] 	# of blocks to leave above you
  [-f] 	Force using flight to keep you still
  [-g] 	Force using glass to keep you still

## /thru
Description 	Pass through walls
Usage 	`/thru`

## /jumpto (or /j)
Description 	Teleport to a location
Usage 	`/jumpto`

## /up
Description 	Go upwards some distance
Usage 	`/up [-fg] <distance>`
  <distance> 	Distance to go upwards
  [-f] 	Force using flight to keep you still
  [-g] 	Force using glass to keep you still
Selection Commands

## //pos1
Description 	Set position 1
Usage 	`//pos1 [coordinates]`
  [coordinates] 	Coordinates to set position 1 to

## //pos2
Description 	Set position 2
Usage 	`//pos2 [coordinates]`
  [coordinates] 	Coordinates to set position 2 to

## //hpos1
Description 	Set position 1 to targeted block
Usage 	`//hpos1`

## //hpos2
Description 	Set position 2 to targeted block
Usage 	`//hpos2`

## //chunk
Description 	

Set the selection to your current chunk.

This command selects 256-block-tall areas, which can be specified by the y-coordinate. E.g. -c x,1,z will select from y=256 to y=511.
Usage 	`//chunk [-cs] [coordinates]`
  [coordinates] 	The chunk to select
  [-s] 	Expand your selection to encompass all chunks that are part of it
  [-c] 	Use chunk coordinates instead of block coordinates

## //wand
Description 	Get the wand object
Usage 	`//wand [-n]`
  [-n] 	Get a navigation wand

## /toggleeditwand
Description 	Remind the user that the wand is now a tool and can be unbound with /tool none.
Usage 	`/toggleeditwand`

## //contract
Description 	Contract the selection area
Usage 	`//contract <amount> [reverseAmount] [direction]`
  <amount> 	Amount to contract the selection by
  [reverseAmount] 	Amount to contract the selection by in the other direction
  [direction] 	Direction to contract

## //shift
Description 	Shift the selection area
Usage 	`//shift <amount> [direction]`
  <amount> 	Amount to shift the selection by
  [direction] 	Direction to contract

## //outset
Description 	Outset the selection area
Usage 	`//outset [-hv] <amount>`
  <amount> 	Amount to expand the selection by in all directions
  [-h] 	Only expand horizontally
  [-v] 	Only expand vertically

## //inset
Description 	Inset the selection area
Usage 	`//inset [-hv] <amount>`
  <amount> 	Amount to contract the selection by in all directions
  [-h] 	Only contract horizontally
  [-v] 	Only contract vertically

## //size
Description 	Get information about the selection
Usage 	`//size [-c]`
  [-c] 	Get clipboard info instead

## //count
Description 	Counts the number of blocks matching a mask
Usage 	`//count <mask>`
  <mask> 	The mask of blocks to match

## //distr
Description 	Get the distribution of blocks in the selection
Usage 	`//distr [-cd] [-p <page>]`
  [-c] 	Get the distribution of the clipboard instead
  [-d] 	Separate blocks by state
  [-p <page>] 	Gets page from a previous distribution.

## //sel (or /;, //desel, //deselect)
Description 	Choose a region selector
Usage 	`//sel [-d] [selector]`
  [selector] 	Selector to switch to
  [-d] 	Set default selector

## //expand
Description 	Expand the selection area
Usage 	`//expand <vert|<amount> [reverseAmount] [direction]>`
  <amount> 	Amount to expand the selection by, can be vert to expand to the whole vertical column
  [reverseAmount] 	Amount to expand the selection by in the other direction
  [direction] 	Direction to expand

## //expand vert
Description 	Vertically expand the selection to world limits.
Usage 	`//expand vert [height]`
  [height] 	The height to expand both upwards and downwards
Region Commands

## //set
Description 	Sets all the blocks in the region
Usage 	`//set <pattern>`
  <pattern> 	The pattern of blocks to set

## //line
Description 	

Draws line segments between cuboid selection corners or convex polyhedral selection vertices

Can only be used with a cuboid selection or a convex polyhedral selection
Usage 	`//line [-h] <pattern> [thickness]`
  <pattern> 	The pattern of blocks to place
  [thickness] 	The thickness of the line
  [-h] 	Generate only a shell

## //curve
Description 	

Draws a spline through selected points

Can only be used with a convex polyhedral selection
Usage 	`//curve [-h] <pattern> [thickness]`
  <pattern> 	The pattern of blocks to place
  [thickness] 	The thickness of the curve
  [-h] 	Generate only a shell

## //replace (or //re, //rep)
Description 	Replace all blocks in the selection with another
Usage 	`//replace [from] <to>`
  [from] 	The mask representing blocks to replace
  <to> 	The pattern of blocks to replace with

## //overlay
Description 	Set a block on top of blocks in the region
Usage 	`//overlay <pattern>`
  <pattern> 	The pattern of blocks to overlay

## //center (or //middle)
Description 	Set the center block(s)
Usage 	`//center <pattern>`
  <pattern> 	The pattern of blocks to set

## //naturalize
Description 	3 layers of dirt on top then rock below
Usage 	`//naturalize`

## //walls
Description 	Build the four sides of the selection
Usage 	`//walls <pattern>`
  <pattern> 	The pattern of blocks to set

## //faces (or //outline)
Description 	Build the walls, ceiling, and floor of a selection
Usage 	`//faces <pattern>`
  <pattern> 	The pattern of blocks to set

## //smooth
Description 	

Smooth the elevation in the selection

Example: ‘//smooth 1 grass_block,dirt,stone’ would only smooth natural surface terrain.
Usage 	`//smooth [iterations] [mask]`
  [iterations] 	# of iterations to perform
  [mask] 	The mask of blocks to use as the height map

## //move
Description 	Move the contents of the selection
Usage 	`//move [-abes] [multiplier] [offset] [replace] [-m <mask>]`
  [multiplier] 	number of times to apply the offset
  [offset] 	The offset to move
  [replace] 	The pattern of blocks to leave
  [-s] 	Shift the selection to the target location
  [-a] 	Ignore air blocks
  [-e] 	Also copy entities
  [-b] 	Also copy biomes
  [-m <mask>] 	Set the include mask, non-matching blocks become air

## //stack
Description 	Repeat the contents of the selection
Usage 	`//stack [-abers] [count] [offset] [-m <mask>]`
  [count] 	# of copies to stack
  [offset] 	How far to move the contents each stack
  [-s] 	Shift the selection to the last stacked copy
  [-a] 	Ignore air blocks
  [-e] 	Also copy entities
  [-b] 	Also copy biomes
  [-r] 	Use block units
  [-m <mask>] 	Set the include mask, non-matching blocks become air

## //regen
Description 	Regenerates the contents of the selection
Usage 	`//regen [-b] [seed]`
  [seed] 	The seed to regenerate with, otherwise uses world seed
  [-b] 	Regenerate biomes as well

## //deform
Description 	

Deforms a selected region with an expression

The expression is executed for each block and is expected to modify the variables x, y and z to point to a new block to fetch. See also https://tinyurl.com/weexpr
Usage 	`//deform [-cor] <expression...>`
  <expression...> 	The expression to use
  [-r] 	Use the game’s coordinate origin
  [-o] 	Use the placement’s coordinate origin
  [-c] 	Use the selection’s center as origin

## //hollow
Description 	

Hollows out the object contained in this selection

Thickness is measured in manhattan distance.
Usage 	`//hollow [thickness] [pattern]`
  [thickness] 	Thickness of the shell to leave
  [pattern] 	The pattern of blocks to replace the hollowed area with

## //forest
Description 	Make a forest within the region
Usage 	`//forest [type] [density]`
  [type] 	The type of tree to place
  [density] 	The density of the forest

## //flora
Description 	Make flora within the region
Usage 	`//flora [density]`
  [density] 	The density of the forest
Generation Commands

## //hcyl
Description 	Generates a hollow cylinder.
Usage 	`//hcyl <pattern> <radii> [height]`
  <pattern> 	The pattern of blocks to generate
  <radii> 	The radii of the cylinder. 1st is N/S, 2nd is E/W
  [height] 	The height of the cylinder

## //cyl
Description 	Generates a cylinder.
Usage 	`//cyl [-h] <pattern> <radii> [height]`
  <pattern> 	The pattern of blocks to generate
  <radii> 	The radii of the cylinder. 1st is N/S, 2nd is E/W
  [height] 	The height of the cylinder
  [-h] 	Make a hollow cylinder

## //hsphere
Description 	Generates a hollow sphere.
Usage 	`//hsphere [-r] <pattern> <radii>`
  <pattern> 	The pattern of blocks to generate
  <radii> 	The radii of the sphere. Order is N/S, U/D, E/W
  [-r] 	Raise the bottom of the sphere to the placement position

## //sphere
Description 	Generates a filled sphere.
Usage 	`//sphere [-hr] <pattern> <radii>`
  <pattern> 	The pattern of blocks to generate
  <radii> 	The radii of the sphere. Order is N/S, U/D, E/W
  [-r] 	Raise the bottom of the sphere to the placement position
  [-h] 	Make a hollow sphere

## /forestgen
Description 	Generate a forest
Usage 	`/forestgen [size] [type] [density]`
  [size] 	The size of the forest, in blocks
  [type] 	The type of forest
  [density] 	The density of the forest, between 0 and 100

## /pumpkins
Description 	Generate pumpkin patches
Usage 	`/pumpkins [size]`
  [size] 	The size of the patch

## //hpyramid
Description 	Generate a hollow pyramid
Usage 	`//hpyramid <pattern> <size>`
  <pattern> 	The pattern of blocks to set
  <size> 	The size of the pyramid

## //pyramid
Description 	Generate a filled pyramid
Usage 	`//pyramid [-h] <pattern> <size>`
  <pattern> 	The pattern of blocks to set
  <size> 	The size of the pyramid
  [-h] 	Make a hollow pyramid

## //generate (or //gen, //g)
Description 	

Generates a shape according to a formula.

See also https://tinyurl.com/weexpr.
Usage 	`//generate [-chor] <pattern> <expression...>`
  <pattern> 	The pattern of blocks to set
  <expression...> 	Expression to test block placement locations and set block type
  [-h] 	Generate a hollow shape
  [-r] 	Use the game’s coordinate origin
  [-o] 	Use the placement’s coordinate origin
  [-c] 	Use the selection’s center as origin

## //generatebiome (or //genbiome, //gb)
Description 	

Sets biome according to a formula.

See also https://tinyurl.com/weexpr.
Usage 	`//generatebiome [-chor] <target> <expression...>`
  <target> 	The biome type to set
  <expression...> 	Expression to test block placement locations and set biome type
  [-h] 	Generate a hollow shape
  [-r] 	Use the game’s coordinate origin
  [-o] 	Use the placement’s coordinate origin
  [-c] 	Use the selection’s center as origin
Schematic and Clipboard Commands

## /schematic (or /schem, //schematic, //schem)
Description 	Schematic commands for saving/loading areas
Usage 	`/schematic <list|formats|load|delete|save>`

## /schematic list (or /schematic all, /schematic ls)
Description 	

List saved schematics

Note: Format is not fully verified until loading.
Usage 	`/schematic list [-dn] [-p <page>]`
  [-p <page>] 	Page to view.
  [-d] 	Sort by date, oldest first
  [-n] 	Sort by date, newest first

## /schematic formats (or /schematic listformats, /schematic f)
Description 	List available formats
Usage 	`/schematic formats`

## /schematic load
Description 	Load a schematic into your clipboard
Usage 	`/schematic load <filename> [formatName]`
  <filename> 	File name.
  [formatName] 	Format name.

## /schematic delete (or /schematic d)
Description 	Delete a saved schematic
Usage 	`/schematic delete <filename>`
  <filename> 	File name.

## /schematic save
Description 	Save a schematic into your clipboard
Usage 	`/schematic save [-f] <filename> [formatName]`
  <filename> 	File name.
  [formatName] 	Format name.
  [-f] 	Overwrite an existing file.

## //copy
Description 	Copy the selection to the clipboard
Usage 	`//copy [-be] [-m <mask>]`
  [-e] 	Also copy entities
  [-b] 	Also copy biomes
  [-m <mask>] 	Set the include mask, non-matching blocks become air

## //cut
Description 	Cut the selection to the clipboard
Usage 	`//cut [-be] [leavePattern] [-m <mask>]`
  [leavePattern] 	Pattern to leave in place of the selection
  [-e] 	Also cut entities
  [-b] 	Also copy biomes, source biomes are unaffected
  [-m <mask>] 	Set the exclude mask, non-matching blocks become air

## //paste
Description 	Paste the clipboard’s contents
Usage 	`//paste [-abenos] [-m <sourceMask>]`
  [-a] 	Skip air blocks
  [-o] 	Paste at the original position
  [-s] 	Select the region after pasting
  [-n] 	No paste, select only. (Implies -s)
  [-e] 	Paste entities if available
  [-b] 	Paste biomes if available
  [-m <sourceMask>] 	Only paste blocks matching this mask

## //rotate
Description 	

Rotate the contents of the clipboard

Non-destructively rotate the contents of the clipboard. Angles are provided in degrees and a positive angle will result in a clockwise rotation. Multiple rotations can be stacked. Interpolation is not performed so angles should be a multiple of 90 degrees.
Usage 	`//rotate <rotateY> [rotateX] [rotateZ]`
  <rotateY> 	Amount to rotate on the y-axis
  [rotateX] 	Amount to rotate on the x-axis
  [rotateZ] 	Amount to rotate on the z-axis

## //flip
Description 	Flip the contents of the clipboard across the origin
Usage 	`//flip [direction]`
  [direction] 	The direction to flip, defaults to look direction.

## /clearclipboard
Description 	Clear your clipboard
Usage 	`/clearclipboard`
Tool Commands

## /tool
Description 	Binds a tool to the item in your hand
Usage 	`/tool <stacker|selwand|tree|repl|farwand|none|deltree|lrbuild|floodfill|cycler|navwand|info>`

## /tool stacker
Description 	Block stacker tool
Usage 	`/tool stacker [range] [mask]`
  [range] 	The max range of the stack
  [mask] 	The mask to stack until

## /tool selwand
Description 	Selection wand tool
Usage 	`/tool selwand`

## /tool tree
Description 	Tree generator tool
Usage 	`/tool tree [type]`
  [type] 	Type of tree to generate

## /tool repl
Description 	Block replacer tool
Usage 	`/tool repl <pattern>`
  <pattern> 	The pattern of blocks to place

## /tool farwand
Description 	Wand at a distance tool
Usage 	`/tool farwand`

## /tool none (or /tool unbind)
Description 	Unbind a bound tool from your current item
Usage 	`/tool none`

## /tool deltree
Description 	Floating tree remover tool
Usage 	`/tool deltree`

## /tool lrbuild
Description 	Long-range building tool
Usage 	`/tool lrbuild <primary> <secondary>`
  <primary> 	Pattern to set on left-click
  <secondary> 	Pattern to set on right-click

## /tool floodfill (or /tool flood)
Description 	Flood fill tool
Usage 	`/tool floodfill <pattern> <range>`
  <pattern> 	The pattern to flood fill
  <range> 	The range to perform the fill

## /tool cycler
Description 	Block data cycler tool
Usage 	`/tool cycler`

## /tool navwand
Description 	Navigation wand tool
Usage 	`/tool navwand`

## /tool info
Description 	Block information tool
Usage 	`/tool info`

## // (or /,)
Description 	Toggle the super pickaxe function
Usage 	`// [superPickaxe]`
  [superPickaxe] 	The new super pickaxe state

## /mask
Description 	Set the brush mask
Usage 	`mask [mask]`
  [mask] 	The mask to set

## /material (or //material)
Description 	Set the brush material
Usage 	`/material <pattern>`
  <pattern> 	The pattern of blocks to use

## /range
Description 	Set the brush range
Usage 	`/range <range>`
  <range> 	The range of the brush

## /size
Description 	Set the brush size
Usage 	`/size <size>`
  <size> 	The size of the brush

## /tracemask
Description 	Set the mask used to stop tool traces
Usage 	`/tracemask [mask]`
  [mask] 	The trace mask to set
Super Pickaxe Commands

## /superpickaxe (or /pickaxe, /sp)
Description 	Super-pickaxe commands
Usage 	`/superpickaxe <single|area|recursive>`

## /superpickaxe single
Description 	Enable the single block super pickaxe mode
Usage 	`/superpickaxe single`

## /superpickaxe area
Description 	Enable the area super pickaxe pickaxe mode
Usage 	`/superpickaxe area <range>`
  <range> 	The range of the area pickaxe

## /superpickaxe recursive (or /superpickaxe recur)
Description 	Enable the recursive super pickaxe pickaxe mode
Usage 	`/superpickaxe recursive <range>`
  <range> 	The range of the recursive pickaxe
Brush Commands

## /brush (or /br, //brush, //br)
Description 	Brushing commands
Usage 	`/brush <forest|butcher|paint|none|clipboard|gravity|heightmap|extinguish|sphere|raise|smooth|cylinder|set|apply|deform|lower|snow|biome>`

## /brush forest
Description 	Forest brush, creates a forest in the area
Usage 	`/brush forest <shape> [radius] [density] <type>`
  <shape> 	The shape of the region
  [radius] 	The size of the brush
  [density] 	The density of the brush
  <type> 	The type of tree to use

## /brush butcher (or /brush kill)
Description 	Butcher brush, kills mobs within a radius
Usage 	`/brush butcher [-abfgnprtw] [radius]`
  [radius] 	Radius to kill mobs in
  [-p] 	Also kill pets
  [-n] 	Also kill NPCs
  [-g] 	Also kill golems
  [-a] 	Also kill animals
  [-b] 	Also kill ambient mobs
  [-t] 	Also kill mobs with name tags
  [-f] 	Also kill all friendly mobs (Applies the flags -abgnpt)
  [-r] 	Also destroy armor stands
  [-w] 	Also kill water mobs

## /brush paint
Description 	Paint brush, apply a function to a surface
Usage 	`/brush paint <shape> [radius] [density] <forest|item|set>`
  <shape> 	The shape of the region
  [radius] 	The size of the brush
  [density] 	The density of the brush

## /brush none (or /brush unbind)
Description 	Unbind a bound brush from your current item
Usage 	`/brush none`

## /brush clipboard (or /brush copy)
Description 	Choose the clipboard brush
Usage 	`/brush clipboard [-abeo] [-m <sourceMask>]`
  [-a] 	Don’t paste air from the clipboard
  [-o] 	Paste starting at the target location, instead of centering on it
  [-e] 	Paste entities if available
  [-b] 	Paste biomes if available
  [-m <sourceMask>] 	Skip blocks matching this mask in the clipboard

## /brush gravity (or /brush grav)
Description 	Gravity brush, simulates the effect of gravity
Usage 	`/brush gravity [radius] [-h <height>]`
  [radius] 	The radius to apply gravity in
  [-h <height>] 	Affect blocks between the given height, upwards and downwards, rather than the target location Y + radius

## /brush heightmap
Description 	Heightmap brush, raises or lowers terrain using an image heightmap
Usage 	`/brush heightmap [-efr] <imageName> [radius] [intensity]`
  <imageName> 	The name of the image
  [radius] 	The size of the brush
  [intensity] 	The intensity of the brush
  [-e] 	Erase blocks instead of filling them
  [-f] 	Don’t change blocks above the selected height
  [-r] 	Randomizes the brush’s height slightly.

## /brush extinguish (or /brush ex)
Description 	Shortcut fire extinguisher brush
Usage 	`/brush extinguish [radius]`
  [radius] 	The radius to extinguish

## /brush sphere (or /brush s)
Description 	Choose the sphere brush
Usage 	`/brush sphere [-h] <pattern> [radius]`
  <pattern> 	The pattern of blocks to set
  [radius] 	The radius of the sphere
  [-h] 	Create hollow spheres instead

## /brush raise
Description 	Raise brush, raise all blocks by one
Usage 	`/brush raise <shape> [radius]`
  <shape> 	The shape of the region
  [radius] 	The size of the brush

## /brush smooth
Description 	

Choose the terrain softener brush

Example: ‘/brush smooth 2 4 grass_block,dirt,stone’
Usage 	`/brush smooth [radius] [iterations] [mask]`
  [radius] 	The radius to sample for softening
  [iterations] 	The number of iterations to perform
  [mask] 	The mask of blocks to use for the heightmap

## /brush cylinder (or /brush cyl, /brush c)
Description 	Choose the cylinder brush
Usage 	`/brush cylinder [-h] <pattern> [radius] [height]`
  <pattern> 	The pattern of blocks to set
  [radius] 	The radius of the cylinder
  [height] 	The height of the cylinder
  [-h] 	Create hollow cylinders instead

## /brush set
Description 	Set brush, sets all blocks in the area
Usage 	`/brush set <shape> [radius] <pattern>`
  <shape> 	The shape of the region
  [radius] 	The size of the brush
  <pattern> 	The pattern of blocks to set

## /brush apply
Description 	Apply brush, apply a function to every block
Usage 	`/brush apply <shape> [radius] <forest|item|set>`
  <shape> 	The shape of the region
  [radius] 	The size of the brush

## /brush deform
Description 	Deform brush, applies an expression to an area
Usage 	`/brush deform [-or] <shape> [radius] [expression]`
  <shape> 	The shape of the region
  [radius] 	The size of the brush
  [expression] 	Expression to apply
  [-r] 	Use the game’s coordinate origin
  [-o] 	Use the placement position as the origin

## /brush lower
Description 	Lower brush, lower all blocks by one
Usage 	`/brush lower <shape> [radius]`
  <shape> 	The shape of the region
  [radius] 	The size of the brush

## /brush snow
Description 	Snow brush, sets snow in the area
Usage 	`/brush snow [-s] <shape> [radius]`
  <shape> 	The shape of the region
  [radius] 	The size of the brush
  [-s] 	Whether to stack snow

## /brush biome
Description 	Biome brush, sets biomes in the area
Usage 	`/brush biome <shape> [radius] <biomeType>`
  <shape> 	The shape of the region
  [radius] 	The size of the brush
  <biomeType> 	The biome type
Biome Commands

## /biomelist (or /biomels)
Description 	Gets all biomes available.
Usage 	`/biomelist [-p <page>]`
  [-p <page>] 	Page number.

## /biomeinfo
Description 	

Get the biome of the targeted block.

By default, uses all blocks in your selection.
Usage 	`/biomeinfo [-pt]`
  [-t] 	Use the block you are looking at.
  [-p] 	Use the block you are currently in.

## //setbiome
Description 	

Sets the biome of your current block or region.

By default, uses all the blocks in your selection
Usage 	`//setbiome [-p] <target>`
  <target> 	Biome type.
  [-p] 	Use your current position
Chunk Commands

## /chunkinfo
Description 	Get information about the chunk you’re inside
Usage 	`/chunkinfo`

## /listchunks
Description 	List chunks that your selection includes
Usage 	`/listchunks [-p <page>]`
  [-p <page>] 	Page number.

## /delchunks
Description 	Delete chunks that your selection includes
Usage 	`/delchunks [-o <beforeTime>]`
  [-o <beforeTime>] 	Only delete chunks older than the specified time.
Snapshot Commands

## /restore (or //restore)
Description 	Restore the selection from a snapshot
Usage 	`/restore [snapshot]`
  [snapshot] 	The snapshot to restore

## /snapshot (or /snap)
Description 	Snapshot commands for restoring backups
Usage 	`/snapshot <before|use|sel|after|list>`

## /snapshot before
Description 	Choose the nearest snapshot before a date
Usage 	`/snapshot before <date>`
  <date> 	The soonest date that may be used

## /snapshot use
Description 	Choose a snapshot to use
Usage 	`/snapshot use <name>`
  <name> 	Snapshot to use

## /snapshot sel
Description 	Choose the snapshot based on the list id
Usage 	`/snapshot sel <index>`
  <index> 	The list ID to select

## /snapshot after
Description 	Choose the nearest snapshot after a date
Usage 	`/snapshot after <date>`
  <date> 	The soonest date that may be used

## /snapshot list
Description 	List snapshots
Usage 	`/snapshot list [-p <page>]`
  [-p <page>] 	Page of results to return
Scripting Commands

## /cs
Description 	Execute a CraftScript
Usage 	`/cs <filename> [args...]`
  <filename> 	Filename of the CraftScript to load
  [args...] 	Arguments to the CraftScript

## /.s
Description 	Execute last CraftScript
Usage 	`/.s [args...]`
  [args...] 	Arguments to the CraftScript
Utility Commands

## //fill
Description 	Fill a hole
Usage 	`//fill <pattern> <radius> [depth]`
  <pattern> 	The blocks to fill with
  <radius> 	The radius to fill in
  [depth] 	The depth to fill

## //fillr
Description 	Fill a hole recursively
Usage 	`//fillr <pattern> <radius> [depth]`
  <pattern> 	The blocks to fill with
  <radius> 	The radius to fill in
  [depth] 	The depth to fill

## //drain
Description 	Drain a pool
Usage 	`//drain [-w] <radius>`
  <radius> 	The radius to drain
  [-w] 	Also un-waterlog blocks

## /fixlava (or //fixlava)
Description 	Fix lava to be stationary
Usage 	`/fixlava <radius>`
  <radius> 	The radius to fix in

## /fixwater (or //fixwater)
Description 	Fix water to be stationary
Usage 	`/fixwater <radius>`
  <radius> 	The radius to fix in

## /removeabove (or //removeabove)
Description 	Remove blocks above your head.
Usage 	`/removeabove [size] [height]`
  [size] 	The apothem of the square to remove from
  [height] 	The maximum height above you to remove from

## /removebelow (or //removebelow)
Description 	Remove blocks below you.
Usage 	`/removebelow [size] [height]`
  [size] 	The apothem of the square to remove from
  [height] 	The maximum height below you to remove from

## /removenear (or //removenear)
Description 	Remove blocks near you.
Usage 	`/removenear <mask> [radius]`
  <mask> 	The mask of blocks to remove
  [radius] 	The radius of the square to remove from

## /replacenear (or //replacenear)
Description 	Replace nearby blocks
Usage 	`/replacenear <radius> [from] <to>`
  <radius> 	The radius of the square to remove in
  [from] 	The mask matching blocks to remove
  <to> 	The pattern of blocks to replace with

## /snow (or //snow)
Description 	Simulates snow
Usage 	`/snow [-s] [size] [height]`
  [size] 	The radius of the cylinder to snow in
  [height] 	The height of the cylinder to snow in
  [-s] 	Stack snow layers

## /thaw (or //thaw)
Description 	Thaws the area
Usage 	`/thaw [size] [height]`
  [size] 	The radius of the cylinder to thaw in
  [height] 	The height of the cylinder to thaw in

## /green (or //green)
Description 	Converts dirt to grass blocks in the area
Usage 	`/green [-f] [size] [height]`
  [size] 	The radius of the cylinder to convert in
  [height] 	The height of the cylinder to convert in
  [-f] 	Also convert coarse dirt

## /extinguish (or //ex, //ext, //extinguish, /ex, /ext)
Description 	Extinguish nearby fire
Usage 	`/extinguish [radius]`
  [radius] 	The radius of the square to remove in

## /butcher
Description 	Kill all or nearby mobs
Usage 	`/butcher [-abfgnprtw] [radius]`
  [radius] 	Radius to kill mobs in
  [-p] 	Also kill pets
  [-n] 	Also kill NPCs
  [-g] 	Also kill golems
  [-a] 	Also kill animals
  [-b] 	Also kill ambient mobs
  [-t] 	Also kill mobs with name tags
  [-f] 	Also kill all friendly mobs (Applies the flags -abgnpt)
  [-r] 	Also destroy armor stands
  [-w] 	Also kill water mobs

## /remove (or /rem, /rement)
Description 	Remove all entities of a type
Usage 	`/remove <remover> <radius>`
  <remover> 	The type of entity to remove
  <radius> 	The radius of the cuboid to remove from

## //calculate (or //calc, //eval, //evaluate, //solve)
Description 	Evaluate a mathematical expression
Usage 	`//calculate <input...>`
  <input...> 	Expression to evaluate

## //help
Description 	Displays help for WorldEdit commands
Usage 	`//help [-s] [-p <page>] [command...]`
  [-s] 	List sub-commands of the given command, if applicable
  [-p <page>] 	The page to retrieve
  [command...] 	The command to retrieve help for
