# General Information
_**This chunk of information is taken straight from the assignment document, further information about each category can be found further below**_

## Deliverables
A single GDD placed as the readme for the repository for this project on GitHub. K-kruusi
invited to the repo as a contributor. Your name included in the readme, and a brief
description of your contribution submitted on blackboard.
Introduction
High up in the snowy mountains of Alterac Valley, there exists an eternal conflict between
the Dwarves of the Alliance and the Frost Wolf Orc Tribe of the Horde. Players must choose
a faction and a character representing one of the four arch-types: Tank, Healer, Mage, and
Assassin; and assist their faction leader in capturing dominion of all Alterac Valley.
## Background
Modeled after Alterac Valley from World of Warcraft, your game will have a much smaller
scope. No persistent characters, no inventory or gear. Just Orcs Vs Dwarves locked in epic
battle for now.
## Game Mechanics
1. Team - When joining players must choose a faction; Horde or Alliance
1. Unit - After picking a faction players must choose a role.
1. Graveyard - If your character dies, your ghost is transported back to the nearest
graveyard; and put into a queue of at most 30 seconds, before respawning at the
graveyard location. Graveyards are capturable, after holding the node for 5 minutes.
1. Each team starts off with 3 graveyards, an additional graveyard located in the center of
the map starts off unowned.
1. Towers - Near the fortress and each graveyard that the teams start off with is a tower;
towers have archers that will attack any opposing side forces that fight near them. They
have limited range and can be burnt down by the opposing team. The archers on the
tower can be killed but will respawn if the tower stands. Towers do not respawn.
1. Captains - Periodically captains of the faction will buff players belonging to that faction
with their own faction buff. Captains can be attacked by opposing side, after dying they
do not respawn.
1. Generals - Defeating the general of the opposing faction wins the game.The Generals
are guarded by 1 Advisor for each active tower that faction has. It’s almost impossible to
kill the general with multiple advisors up.
1. Spawn Location - Players start the match at an uncapturable graveyard just outside of
their main base. If their team controls no graveyards players will spawn at the entrance.
## Genre
40 vs 40 Cooperative competitive multiplayer game.
## Characters
1. Knight - High Passive Survivability, Low Damage, Disruption
1. Mage - High Damage, Cooldown-Based Survivability, Range
1. Assassin - High Damage, High Mobility, Disruption
1. Priest - Ability to Heal Self/Others, Range
## Abilities
Each class should at the minimum have 4 skills that fit their kit described above.
## Controls
1. Standard World of Warcraft like controls.
1. WASD movement.
1. Mouse based UI and scene target selection
1. Keys 1 through 0 for abilities
1. Menu for game settings
1. Menu for starting / joining a game
1. Escape for seeing the score + metagame information like HKs, killing blows etc.
## UI
1. Health of self
1. Resource (aka mana) of self
1. Ability buttons with mouse over descriptions
1. Current Target
1. Targets Health and resources
1. Buffs on allies and self
1. Group Members



# Gameplay

# Tools

## Game Editor
Loading models into the game space. Being able to scale,rotate, move and determine whether they have/are Collided with something. Camera movement(wasd and mouse to look around. Click to place the object). When a model is selected (Knight ,Mage, Assassin ,Priest) a list of parameters will appear in the inspector that can be changed the object can then be moved around the game space as well.

![worldmap-alterac-old](https://user-images.githubusercontent.com/44447609/51505961-af5f7480-1db7-11e9-9774-990f7c47d40f.jpg)

## UI for Game Editor
A menu that has the list of objects that can be placed in the game space. A inspector that shows that parameters for the object. Example, scale, rotate, and location. Once placed in world and selected again the inspector will show all parameters plus a delete option.

1. Character spawn menu (NPC, player char, animal).
1. Terrain (forest, soil, snow covered land, water). 
1. Asset (Tree, Rock, building, flags). 
1. Starting point, end point, out of bounds point (Spawn points will be selected and units will keep spawn by user click).

## Character Editor
Controls character stats such as requirement for Level, str, dex, int, MP (Magic/Mana/Mist Points), EXP(Experience Points), Defense Power, Evasion, and setting abilities. Also controls NPC stats ex. Guards as well.

![636141782667101293](https://user-images.githubusercontent.com/44447609/51506213-2d704b00-1db9-11e9-8b00-cf2b953a8bee.jpg)

## File Format
Json save character stats and account of player or database(MySQL).

![wc3_editor_objects](https://user-images.githubusercontent.com/44447609/51506261-6e685f80-1db9-11e9-89db-57f6342d7f0e.png)

## Particle System
contain four different particle effects which will used by certain characters in the game. The particles will be controlled with things such as their size, brightness, lifespan, speed, rotation, duration and maximum amount of particles.

## Animation System
control animations of the player character and NPCs

![cap1](https://user-images.githubusercontent.com/44447609/51506291-a5d70c00-1db9-11e9-8328-531cec2b63be.JPG)

# Graphics

# **Networking**

## **TCP Server**
test
Used for when the player logs in or logs out of the game (need safe and reliable connection to server) and when they choose what game they will play in and also what their character / class will be before the game begins.

1. Player information (username, password, email).
1. Player statistics (wins, loses).
1. Character faction and class.
1. Core UI information 
1. Character deaths / kills for scoreboard

1. *Stretch goals: Sending messages to other players in the game. Needs to be TCP as the information must be accurate.*
1. *Stretch goals: Character creator information*

## **UDP Server**

For the gameplay (less error checking but it is much faster which is required for a game running online with 40-80 people ideally at 60 frames per second). 
Information to be sent in data packets:

1. Transform information (location and rotation).
1. Player actions (attacks, heals, captures of areas like graveyards).
1. Buffs and debuffs (let the player know if they get a buff and how long it will last. Client will handle how the buff changes their actions).
1. Character health (to be displayed on other players UI and to check for validity).

1. *Stretch Goals: TDB*

## **TCP or UDP**
1. Broadcasting tower / graveyard captures and captain / general deaths
1. NOTE: Logistics of sending information via TCP and UDP at the same time. Is it possible to connect players to 2 ports at the same time?

## **Database Information**
This section will list what we will need to store in the database
MySQL is the most likely candidate - We previously used it.

1. Player account information: username, email, password, etc.
1. Player gameplay statistics: wins / loses.
1. Character class statistics: health, actions, abilities.
1. Game version: What patch is the game running on, does the game need to be updated

1. *Stretch goals: Able to pull character creator information*




# Markup Text Testing

Here you can find references on how to use the markup language

It's very easy to make some words **bold** and other words *italic* with Markdown. 

You can even [link to Google!](http://google.com)

# This is an h1
## This is an h2 tag
###### This is an h6 tag

*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_

1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
   
   
I think you should use an
`<addr>` element here instead.


```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
