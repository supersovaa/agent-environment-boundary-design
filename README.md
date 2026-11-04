# agent-environment-boundary-design

A lightweight skill for defining the externally meaningful contract between an agent and an interactive environment.

## Core idea

An agent needs a determined observation, a meaningful decision, legal actions, and a defined boundary for automatic environment progression. Learning and evaluation may also require an explicit semantic action unit.

## When to use

Activate when designing or revising an agent's observations, decision points, legal candidates, accepted actions, automatic progression, or learning/evaluation units in a game, simulator, or interactive learning environment.

## Responsibility

Define the agent-visible decision contract, distinguish successive selections from completed actions, address equivalent choice orders, and settle the progress/stop contract for repeatable optional actions separately from their rule legality. Keep internal implementation choices with implementation.

[execution-path-design-audit](https://github.com/supersovaa/execution-path-design-audit) owns design-completion auditing. [repo-first-game-digitization](https://github.com/supersovaa/repo-first-game-digitization) owns applicable game rules and digitization canons.

Detailed operating rules live in [SKILL.md](SKILL.md).

## Installation

Install this repository as a skill directory in an AI-agent environment supporting `SKILL.md`. Keep `SKILL.md` at the skill directory root and register it at design and requirements/grill entry points that define the agent–environment contract.
