---
name: agent-environment-boundary-design
description: Design observation, decision, legal-action, automatic-progression, and action-unit contracts between a decision-making agent and an interactive game, simulator, or learning environment.
---

# Agent–Environment Boundary Design

Use this skill when defining or revising the interaction contract between a decision-making agent and an interactive game, simulator, or learning environment.

This skill targets a single-user AI-agent design workflow.

## Establish the interaction contract

Start from settled requirements, authoritative domain rules, and the environment's existing design canon. Define the externally meaningful contract for the behavior in scope:

1. What the agent observes at each decision, including information visibility and the acting player's or agent's perspective.
2. When a decision is requested, who decides, what the choice means, and which legal candidates are presented. Establish candidate eligibility from information available at that point.
3. What the response commits, when its meaning affects environment state, what the environment advances automatically afterward, and where the next observation, decision, termination, or external stop occurs.
4. Where successive selections form one completed semantic action or learning unit, and where they represent separate decisions. Define the unit that an evaluator or learner attributes value to when the distinction affects the external contract.
5. When independent selections can be reordered, establish whether the resulting meaning is equivalent and whether order changes observation, legal candidates, recorded decisions, or learning/evaluation units.

## Resolve progression and ambiguity

Examine optional actions that can repeat without moving toward an externally meaningful next state or termination. Define the required continuation, progress, stop, or error contract separately from the domain legality of each action. Use a user-settled decision when a progress constraint would change agent-visible behavior.

When legal candidates depend on an unresolved player choice, optional effect, or future state, define the decision and candidate-generation boundary that makes the choice determinate at the time of presentation.

Record guarantees that affect replay, persistence, public APIs, or other consumers only to the extent that they change the interaction contract.

## Keep design at the contract boundary

Ask the user to settle missing requirements, domain rulings, or externally observable choices when needed. Leave data structures, container choices, internal algorithms, caching, and helper decomposition to implementation when the same contract permits alternatives.

Record settled interaction guarantees in the owning design canon. Use that project's rules canon for game legality and meaning.

## Responsibility boundary

This skill designs agent–environment interaction guarantees.

[execution-path-design-audit](https://github.com/supersovaa/execution-path-design-audit/blob/main/SKILL.md) audits whether the resulting execution path is complete; it owns identifying remaining gaps rather than making design decisions. [repo-first-game-digitization](https://github.com/supersovaa/repo-first-game-digitization/blob/main/SKILL.md) owns game-rule and digitization canons where applicable. The surrounding design and requirement workflow owns user decisions and persistence; implementation owns internal mechanisms.
