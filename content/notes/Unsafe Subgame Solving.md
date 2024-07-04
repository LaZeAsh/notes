---
title: "Unsafe Subgame Solving"
draft: true
---

Unsafe subgame solving is a method used in to determine strategies for specific parts of the game, subgames, based on the assumption that players have followed a predefined strategy, the blueprint ([[Nash Equilibrium]]), before reaching the subgame.

Blueprint Strategy: Before reaching the subgame it is assumed that both players have played according to a strategy known as the blueprint ([[Nash Equilibrium]]). This defines a probability distribution over the nodes at the root of the subgame `S`

[[Probability Distribution]]: This distribution represents the likelihood that the actual game state matches any given node at the subgame's root

Reading paper: https://arxiv.org/pdf/1705.02955
