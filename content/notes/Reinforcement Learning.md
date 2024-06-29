---
title: "Reinforcement Learning"
draft: true
---

Learned about this concept at the Chess Hackathon in San Francisco!

The goal of reinforcement learning is to learn a good strategy for the agent from trials and simple feedback. With optimal strategy the [[AI Agents|agent]] can adapt to the environment to maximize future rewards


## Key Concepts

- `Environment` - Refers to the external system which a Reinforcement Learning agent interacts with (aka the world of the agent). 
	- State (S): The state of the environment at any given time, provides all the relevant information about the current situation
	- Action (A): The set of possible moves or decisions that the Reinforcement Learning agent can make. Actions affect the state of the environment
	- Reward (R): Feedback from the environment to the agent after it takes an action. Indicates how good or bad the action was in a specific state
	- Transition Function (T): This defines how the environment changes from one state to another based on the agent's action
	- Markov Property: Property that states that the future state can depend only on the current state and action not on the sequence of states (future states?) and actions that preceded them
	- Episodic vs. Continuous: Environments can be episodic (with distinct episodes or trials) or continuous (with ongoing interactions)
	- Observable vs Partially Observable: An environment is observable if the agent can directly observe the current state. If some information is hidden or uncertain it's partially observable
	- Deterministic vs Stochastic: Deterministic environments always produce the same next state and reward given a state and action. Stochastic environments introduce randomness into state transitions or rewards
	- Static vs Dynamic: Static environments do not change over time, while dynamic environments may have changing dynamics or rules


