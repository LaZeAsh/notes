---
title: "Kuhn Poker"
---

Kuhn Poker is a simplified form of poker with 3-cards invented by Harold E. Kuhn.

It is a two player zero-sum-game.

Learning about Kuhn Poker while working alongside Steven Gong for PokerAI
## How it's played?

1. Each player is forced to bet 1 (as the pot)
2. Each player is dealt one of 3 cards and the third is put aside unseen
3. Player one can check or bet 1
	1. If player one checks than player two can check or bet 1
		1. If player two checks there is a showdown for the pot of 2 (higher card wins 1 from the other player)
		2. If player two bets and then player one calls there is a showdown for the pot of 4 (higher card wins 2 from the other player)
	2. If player one bets then player two can fold or call
		1. If player two folds then player one takes the pot of 3 (takes one from player 2)
		2. If player two calls there is a showdown for the pot of 4 (higher card wins 2 from the other player)

List of possible actions in Kuhn Poker:

![[Pasted image 20240705214726.png]]

## Cards

Mentioned previously Kuhn Poker only consists of 3 cards and the 3 cards are as follows:

1. Jack (J) - Lowest value card in Kuhn Poker
2. Queen (Q) - Middle value card in Kuhn Poker
3. King (K) - Highest value card in Kuhn Poker

