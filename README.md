### SMT Gaming Presents

Robo Escape
===========

##### Version 0.3 Build Release for Assignment 1 Part 3

Contributors
------------

* Asemota33
* SAMgit81
* trentb10

[Click here to play the game!](https://trentb10.github.io/COMP397-W2021-Group14-Assignment1-Part3-BUILD/)

Build Release Overview
----------------------

This is the version 0.3 build release for Robo Escape that was made for COMP397 Web Game Programming 2021 Winter Semester at Centennial College. 

The following features made this build release:

* Main Menu
  * Options Menu
    * Adjustable volume slider for music
    * Rebindable keys for `Jump` and `Pause` actions only
  * Load Menu
    * Layout only; No functionality to load a save point is implemented
* In-Game
  * Functioning player health
    * Hazards and enemies lower HP
  * Functioning minimap
  * Semi-functioning pause menu
    * `P` key brings up pause menu
    * `Resume`, `Save`, and `Load` buttons are not clickable
  * Semi-functioning inventory
    * `I` key brings up inventory menu
    * Key does not appear in inventory menu after picking it up
  * Semi-functioning player weapon
    * Rifle only
    * Soundfx and firing visual fx implemented
    * Weapon does not deal damage
  * (Maybe more than?) Semi-functioning key
    * Key can be picked up and used to open the door at the end of the level
    * Key does not appear in player inventory
  * Game over screen implemented
    * `Restart` and `Main` buttons are functional
    * Points counter is static

The following information was taken from the Robo Escape Game Design Document. 
Most of the game features discussed here were planned from the beginning but didn't
make the build release for A1P3 and A2P3/Final release.

Game Overview
-------------

In a futuristic dystopian world/post-apocalyptic future, you were captured and taken to a base of a secret agency, called the Cyber Intelligence Bureau (CIB). The agency wants to interrogate you for a cybercrime you know you didn’t commit. Knowing death is certain, you try to escape the base and make it out alive. 

The goal of the game is to escape the secret base. Each level will have a door at the end which needs to be opened by a key carried by a security guard. Levels will have enemies which consists of security guards, agents, and security robots. Level hazards such as spikes and tripwires will appear as the player progresses through the game. The guard that has the key will be distinguishable from other enemies.

Game Type
---------

Initially, the game was intended to be a 3D side-scrolling platformer. After further considerations regarding the game design, we have decided to instead do a first-person 3D platformer.

Mechanics, Dynamics, Aesthetics
-------------------------------

### Mechanics

The goal is to escape the secret base. The player must navigate through the level and eliminate enemies while dealing with various traps around the base. 

Enemies can only be eliminated using melee attacks (no weapon equipped) or with a weapon.

Every level will have a door that the player must enter through to advance to the next level. The door must be opened by a key carried by an enemy which is distinguishable from other enemies (eg. Enemies will have blue attire but the enemy with the key will have red attire).

### Dynamics

Weapons are dropped by enemies upon eliminating them and the player can pick them up and use them.

The inventory can be accessed anytime by pressing the `I` key. Health packs can quickly be accessed by pressing the `H` key.

The `F` key is used to interact with the environment and dynamically changes based on the context the player is in. For example, if the player is standing in front of a security camera, a prompt will appear that says, `Press F to disable security camera.`

## Aesthetics & Game World

The game takes place in a futuristic dystopian world/post-apocalyptic future.

Our game world uses the ides of linear method where the player follows a direct path. Though, the given areas provide many places to explore, the events take place within restricted location.

Levels
------

The first level will be easy and will explain the basic controls, mechanics, and goals. 

The second level will introduce enemies that can harm the player. These enemies will only have basic attacks (eg. Punch).

The third level will introduce more difficult enemies, as well as environmental objects like spikes that can harm the player. Fall damage will also be introduced here.

Game Progression
----------------

The player will be able to receive new abilities as the player advances to the next level. Abilities include double jump, added health, etc.

Scoring
-------

The object of the game is to reach the end of a level and use the key carried by the security guard to unlock the door. After each level a certain number of points will be allocated to the user. Defeating enemies throughout the level is also another way to receive points. Ultimately the way to beat the game is to make it through all the levels and unlocking each door.

Controls
--------

| Key | Control |
| --- | ------- |
| W / Up Arrow | Move Forward |
| A / Down Arrow | Move Backward |
| S / Left Arrow | Strafe Left |
| D / Right Arrow | Strafe Right |
| Space Bar | Jump |
| F | Interact |
| M | Toggle Map |
| I | Inventory |
| P | Toggle Menu |
| H | Use Health Pack
|   |   |
| Mouse X/Y Axis | Look Around / Aim |
| Left Mouse Button | Attack |

Saving and Loading 
------------------

Various checkpoints will be available around the map. Checkpoints serves as save points which allows players to resume where they left off upon quitting/dying and retain collected items.

Level and UI Sketches
---------------------

(To-Do: Add images for level and ui sketches)

Screen Captures
---------------

(To-Do: Add images for all sections below)

### Menu and Options Screens

### Gameplay Screens

Characters, Vehicles, Cameras
-----------------------------

### The Characters

#### Playable Character

The main character can be named by the user player but the design is pre-made. So far, we’ve decided the character will be a robot. The player will be able to name their character at the start of the game.

#### Non-Playable Characters / Friendly NPC's

Some agents in the secret base are friendly agents---they know that the agency is corrupt and you’re innocent. These agents will give you various hints and tips at how to complete the level, such as the location of the door that completes the level, how to dodge a trap up ahead, where the guard with the key is, and more. 

#### The Camera

The view of the player will be in first person. The player will be able to look around by moving the mouse.

Enemies (AI)
------------

These characters consists of security guards and agents. Both guards and agents are either humans or robots. These attack the player on sight and drop their weapons upon elimination. Possible weapons they can carry include batons, knives, pistols, SMGs, rifles, laser pistols, and laser rifles. NPCs that carry weapons that deal high damage are found in higher levels. 

A distinguishable enemy NPC will be somewhere in the level. This NPC will carry the key that must be used on the door to complete the level. The player must find this NPC and eliminate them to take the key.

Weapons
-------

The weapons that can be used are batons, knives, pistols, SMGs, rifles, laser pistols, and laser rifles.

| Weapon | Damage | Range * |
| ------ | ------ | ------- |
| Baton | Very Low | n/a |
| Knife | Low | n/a |
| Pistol | Low | Short |
| Laser Pistol | Low | Far |
| SMG | Medium | Short |
| Rifle | High | Medium |
| Laser Rifle | Medium | Far |

 *A weapon's range determines how far a bullet can travel before damage is 
 reduced.

 Items
 -----

The user will be able to pick up health packs during gameplay. These health packs will refuel the character from damage taken by enemies or from steep drops. Other Items available are security Jammers, which temporarily disable the cameras, Extra strength packs which make damage from enemies and steep drops less effective.

| Item | Effect |
| ---- | ------ |
| Health Pack | Restore health by 300 HP |
| Strength Buff Pack | Increase strength for 60 seconds |
| Security Camera Jammer | Jam a security camera and make the area passable for 15 seconds |

Abilities
---------

As the robot progresses through the level's, abilities will be given to it. The initial abilities given are running, jumping and utilizing inventory items. Additional abilities such as air jumps and laser zaps will be given to the robot as they earn higher scoring positions.

| Added Ability | Effect | Activation |
| ------------- | ------ | ---------- |
| Air Jump/Double Jump | Jump while in the air after an initial jump. Can only be used once until the player lands. | Press jump button twice |
| Laser Zap | Deals very low damage close range but good for finishing off enemies with low health. Activates once every 10 seconds | Contact an enemy |

Sound Index
-----------

| Clip Title | Author | Description |
| ---------- | ------ | ----------- |
| Futuristic Gun SoundFX | MGWSoundDesign |   |
| Game App SFX Pack 002 - Futuristic USER - FREEBIE EDITION | Arcade Arthur |   |
| theme-finalv1.wav | trentb10 | Robo Escape theme; Looped in main menu |
| level1-finalv1.wav | trentb10 | Level 1 theme; played on loop |
| level2-finalv1.wav | trentb10 | Level 2 theme; played on loop |
| level3-finalv1.wav | trentb10 | Level 3 theme; played on loop |

Art and Multimedia Index
------------------------

| Art Title/File Name | Author | Description |
| ------------------- | ------ | ----------- |
| Inventory | Brackeys | Art assets for inventory system |
| Health Bar | Brackeys | Art assets for health bar |
