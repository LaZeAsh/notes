---
title: "Counterfactual Regret Minimization (CFR)"
aliases:
- CFR
tags:
- "Game Theory"
---

Counterfactual Regret Minimization (CFR) is a self play algorithm that learns by playing against itself repeatedly. It first starts by playing with a random uniform action (each action has an equal chance of being chosen) and iterates on these strategies to get closer to the [[Nash Equilibrium]]

## Regret

Regret in CFR is defined as not having chosen an action as the difference between the utility of that action and the utility of the action we actually chose, with respect to the choices of other players

For example:

Rock paper scissors, if the opponent plays rock then these are our possible actions:

1. If played Paper regret is +1 as we have won
2. If played Rock regret is 0 as we have tied
3. If played Scissors regret is -1 as we have lost

In this case lets say we played scissors and lost...

We regret that we did not play rock and tied but we regret **even more** that we did not play paper even more as our gain (in points) would have been the greatest if we played paper

Ideally in a game one would want to focus on minimizing regret but if you face an opponent who is aware that you are using the approach regret matching then you could do the same computations, observe any bias that it may have towards a play and exploit that bias. By the time that the algorithm has learned to regret that bias the damage will have already been done.

`Terminal game state` - State where the game has ended (eg: checkmate in chess)

## Understanding Pseudocode Implementation for CFR 



## Unfamiliar Terms

I am learning about CFR while reading the paper http://modelai.gettysburg.edu/2013/cfr/cfr.pdf. I have made a list of terms I was unfamiliar with in the paper and their definitions.

`Game Tree` - Graphical representation of all possible states and moves in a game
- Each Node in the tree represents a specific state of the game
- Different states:
	- `Chance Nodes` - Points in the game where a random event occurs (eg: rolling a dice or drawing a card)
		- Each edge coming from a chance node represents a possible outcome of random event
		- Each edge is also labeled with the probability of that outcome
	- `Decision Nodes` - Points where a player makes a decision
		- Each edge from a decision node represents a possible action that the player can take
		- Edges lead to successor states, which are results of the player's actions

`Edges` (the lines connecting the nodes) - Represent transition between states, which occur due to actions taken by players or chance events

