---
title: "MIT Battlecode"
---

I am participating in MIT Battlecode 2024

## 2024

### Objective

- Food has become a scarcity in this world filled with Duck life
- It's your job to defend your faction's valuable bread while simultaneously preparing a strategic attack against the other team
- Build traps, dig water channels, and hide bread to ward off enemy factions
- Capture all enemy team's bread to win

### Map Elements

#### The Dam

The Dam is the impassable barrier that divides both teams
- Keeps teams separate for the first 200 rounds (setup phase)
- Once removed, doesn't come back

#### Spawn Zone

9 tiles where your ducks are allowed to spawn
- Each map has exactly three for each team
- Your team's bread is placed here by default, but can be moved during setup

#### Crumbs

Boosts team supplies of crumbs
- Used to build traps and dig water
- Gained passively by each team in addition to these boosters

#### Water

An impassable tile
- Ducks can dig which creates water
- Ducks can fill which removes water

#### Walls

Impassable barriers
- Fixed as part of the map and cannot be changed

### Resources

Only resource is crumb which will be gained passively 

### Robots

#### Duck

- The base and only unit
- Only 50 ducks max for each team
- Other variants are upgrades of the base duck
- Can automatically 'specialize' in certain actions by performing them
- Respawns in the spawn zone after being removed from the game after certain # of rounds


#### Builder Duck

- Appears once the base duck becomes high enough in the 'build' skill
- Is more adept at performing build actions
- Cannot be multiple duck variants at once

#### Attack Duck

- Appears once the base duck becomes high enough in the 'attack' skill
- Is more adept at performing attack actions
- Cannot be multiple duck variants at one time

#### Healer Duck

- Appears once the base duck becomes high enough in the 'heal' skill
- Is more adept at performing heal actions
- Cannot be multiple duck variants at one time

## Traps

Traps can be built by the ducks using crumbs

#### Water Trap

When set off by another duck it'll dig water in a radius from the trap (blocks cannot be traversed by the duck)

#### Stun

Stuns all enemy ducks within a radius

#### Explosive

Harm all enemy ducks in a certain radius

## Bread

Flag that you're protecting and the flag you want to obtain from the opposing team

## Global Upgrades

- Each team gets **one** upgrade point every 750 rounds
- Applies to all ducks, and each upgrade can be activated once
	- Can't use same upgrade twice
	- Whatever upgrade you use all ducks will be affected
	- Game ends automatically after `2,000` rounds so the max you can obtain is `2`

![[Pasted image 20240114002918.png]]



