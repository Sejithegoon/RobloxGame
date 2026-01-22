# README

**Top Devs:** Seji, Pyro, Ranv1rw

All scripts and assets for the game are stored in this repository.



## Game Idea

**Roleplaying + Chance + Grinding + Lore**

Main concept: **Catch a Bug!**



## Core Pillars

### Roleplaying
*(TBD)*

### Chance

**Bug Rarity Tiers:** Common, Rare, Epic, Legendary, Mythic

**Bug Examples**
- **Common:** Ladybugs, Ants, Mosquitoes, Flies  
- **Rare:** Bees, ...  
- **Epic:** ...  
- **Legendary:** ...  
- **Mythic:** ...  

### Grinding
*(TBD)*



## Main Features

### Main Mechanics
**Bugs**
- Bugs fly around, rest on trees, and walk around.

**Player**
- Hunt with a weapon  
- Sell bugs  
- Index/collect bugs  
- **Flex bugs**

### Sub Mechanics
**Weapons**
- Luck stat  
- Simple accessories  

### Map
**One Big Island**
- Sell Shop  
- Buy Shop  
- Leaderboard  
- NPCs  

### Lore
Bugs are going missing one by one — your job is to collect every type of bug.



## Bug System

**Bug Properties:** Size, Rarity, Type, Animations, Destination

1. **Size**  
   Each bug has a size range. Each bug type has its own size variation.  
   Size affects sell price: bigger bug = higher sell value.

2. **Rarity**  
   Each rarity tier has its own set of bugs.  
   Higher rarity increases sell price more.

3. **Type**  
   *(TBD)*

4. **Animations**  
   *(TBD)*

5. **Destination**  
   When a bug spawns, the tree passes it a destination.  
   - If a player catches the bug before it reaches the destination → bug is collected.  
   - If it reaches the destination uncaught → bug despawns there.
   
   ###### Code Used
   Script is stored in tree leaf's it
   ```lua
   local tree = script.Parent -- should be stored in tree leaf part

   local listOfTrees = {} --list of all the tress 

   while true do -- will run forever

	local randomTree = listOfTrees[math.random(1, #listOfTrees)] -- picks random tree in from the list 

	local newBug = game.ReplicatedStorage.Bug:Clone() -- clones a bug from Replacated Storage (this should be a random bug based on the rates )

	newBug.Position = tree.Position  -- gives the bug a postion, which is the same as the leaf of parent tree

	newBug.Name = "Common Bug" -- should pass the name as the bug bassed on which bug cloned 

	newBug:SetAttribute("Goal",listOfTrees[math.random(1, #listOfTrees)].Position) -- passes the "Attribute"  the goal(destination) to the bug 

	newBug.Parent = game.Workspace -- put the bug into the work space (the game)

	task.wait(15) -- timer to spawn the next bug
	
   end

   
   ```

   


## Weapons
*(TBD)*

## Player
*(TBD)*

## Score
*(TBD)*



## Planning

### Everyone (Tasks everyone should do)
**Deadline:** Continuous  
- Learn how to navigate **Roblox Studio**
- Know how to access this repo and add/remove files

### Implement Early Essential Scripts
**Seji, Ranv1rw**  
**Deadline:** Continuous  
- Create core systems:
  - Bug spawning from trees
  - Catching bugs
  - Sell/buy system
- Store all new scripts in the `scripts/` folder with a short description of:
  - what it does
  - where it belongs in Roblox Studio

### Early Game Models
**Seji, Pyro**  
**Deadline:** 05-01-2026  
- Trees, common bug types, and map
- Low-detail meshes, good enough for early testing
