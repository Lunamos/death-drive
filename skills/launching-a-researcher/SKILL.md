---
name: launching-a-researcher
description: Use when starting an autonomous research agent, writing its goal, choosing which new or stalled project to give it, or checking on research agents that are already running
---

# Launching a researcher

## Overview

An autonomous researcher pursues what its goal makes easy to pursue. A goal that hands over a claim gets a paper that confirms
the claim. A goal that hands over a question and the user's curiosity leaves room for a result that surprises its author.

## Choosing the project

- **Survey with subagents.** For each candidate, find the idea, how far it got, why it stopped, the assets and what remains.
- **Revive the curiosity, not the frame.** A stalled project is revived for the question that made it worth starting. Its old
  claims and framing are hypotheses at most.
- **The user chooses.** Present the candidates with a recommendation.

## Writing the goal

Keep the goal in a file in the project, and start the agent with a one-line pointer to it.
- **The question, in the user's words.** Quote the user verbatim. Inspiration is welcome; label it as a starting point, not a
  topic, and say that the agent may change direction.
- **No claim to confirm.** Leave out candidate claims and the experiments meant to prove them: they become the paper.
- **The object of curiosity stays central.** When the user wants to understand an object, methods and instruments are means.
- **Novelty.** Name the existing work, ours and others', that the agent should not continue.
- **The stop condition.** "A result the user finds interesting, or a documented stop", never "a complete paper on X".
- **Light procedure.** Controls, datasheets and pre-registration serve a surprising claim (building-evidence, "Explore, then
  freeze"). Ask early for a note on what surprised the agent.
- **Data as a first-class job,** when a project depends on data: the agent is expected to build it, not to shrink the question.
- **Resources and rules:**
  - shared compute and how to share it;
  - the disk budget;
  - spending limits;
  - the workspace;
  - what may leave the machine;
  - which sessions and processes are its own; it touches no others.
- **Reporting.** Whether the user is present, and where reports go.
- **Its skills.** The agent starts with the-drive and loads the companion skills of each stage.

## Launching

Give the agent the highest reasoning effort, its own session and its own workspace.

## Watching

- **Read the record, not the activity.** Follow the story, the findings log and the reports at turning points (narrating-work).
- **Judge with a fresh reader** (the-drive). When the work turns ordinary, say so and propose a reframe or a stop.
- **Signs of drift:** the claim is the goal's own; interest checks name only gaps in defensibility; audits choose the
  experiments.
- **The user decides** whether to continue, reframe or stop.
