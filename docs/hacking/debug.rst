==========================
Debug Command Descriptions
==========================

Item Creation
=============

Create an object ``c``
  Provides a menu to let you create any object, and drops it on the floor.

Create an artifact ``C``
  Provides a menu to let you create any artifact, and drops it on the floor.

Create a good object ``g``
  Creates a good object and places it nearby. If you provide a command-
  count, creates that many good items.

Create a very good object ``v``
  Creates a very good ("excellent") object and places it nearby. If you
  provide a command-count, creates that many very good items.

Play with an object ``o``
  Lets you modify an object by randomly rerolling it as a normal, good, or
  excellent object, or lets you modify it directly, tweaking the pval and
  combat values.

Test kind ``V``
  Requires a command-count. For the tval given by command-count, creates
  one object of each sval and drops it nearby.

Detection / Information
=======================

Detect all ``d``
  Detects all traps, doors, stairs, treasure, and monsters nearby.

Magic Mapping ``m``
  Maps the nearby dungeon.

Learn about objects ``l``
  Requires a command-count. Makes you "aware" of all items with level less
  than or equal to the command-count.

Monster recall ``r``
  Gives you full monster recall on all monsters or on a chosen monster.

Wipe recall ``W``
  Resets monster recall on all monsters or on a chosen monster.

Unhide monsters ``u``
  Reveals all monsters whose distance to the character is at most 255. If
  given a command-count, uses that distance instead of 255.

Wizard-light the level ``w``
  Lights the entire level, as the Potion of Enlightenment.

Create spoilers ``"``
  Lets you create a spoiler file for objects or monsters.

Teleportation
=============

Teleport level ``j``
  Allows you to teleport to any dungeon level instantly.

Phase Door ``p``
  Teleports you up to 10 spaces away.

Teleport ``t``
  Teleports you up to 100 spaces away.

Teleport to target ``b``
  Teleports you to the targeted grid (or close to it, if it is occupied).

Character Improvement
=====================

Cure all maladies ``a``
  Removes all curses, restores all stats, xp, hp, and sp, cures all bad
  effects, and satisfies your hunger.

Advance the character ``A``
  Advances your character to level 50, maxes all stats, and gives you a
  million gold.

Edit character ``e``
  Lets you specify your base stats, xp, and gold.

Increase experience ``x``
  Doubles your current experience and adds 1. If given a command-count,
  increases your experience by that much instead.

Rerate hitpoints ``h``
  Rerates your hitpoints.

Monsters
========

Summon monster ``n``
  Prompts you for the name of a monster, then summons that monster nearby.
  You must give the name exactly as in 'monster.txt'. You may optionally
  give a command-count, in which case this command summons the monster with
  that number nearby instead of prompting you for a name.

Summon random monster ``s``
  Summons a random monster next to you. If given a command-count, summons
  that many monsters instead.

Zap monsters ``z``
  Deletes all monsters in sight. If given a command-count, deletes all
  monsters whose distance to the character is at most the command-count
  instead.

Dungeon
========

Create a trap ``T``
  Creates a random trap on your square.

Quit without saving ``X``
  Quits the game without saving (prompts first).

Query the dungeon ``q``
  Light up all the grids with a given square flag
  (see src/list-square-flags.h).

Query terrain ``F``
  Light up all the grids with a given terrain type
  (see lib/gamedata/terrain.txt).

Collect stats ``f`` or ``S``
  Collects stats on monsters and objects present on level generation.
  Requests number of runs, and whether diving or clearing levels, and
  outputs the results into the file 'stats.log' in the user directory.

Nick hack ``_``
  Maps out the reachable grids (by the sound and scent algorithm) in
  successive distances from the player grid.
