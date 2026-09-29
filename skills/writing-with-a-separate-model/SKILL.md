---
name: writing-with-a-separate-model
description: Use when a paper, its figures or a talk should be written, rewritten or polished, or when reviews of a draft are needed to decide how to continue
---

# Writing with a separate model

## Overview

Thinking and presenting are different strengths:
- **The main model** owns the truth: questions, experiments, data and claims.
- **A separate writing model** owns the form: prose, figures, layout, polish and self-review.

Keep them apart, give the writing model exactly what it needs, and let the user's taste choose.

## Setting up

- **The model.** Use the strongest available writing model, at high effort, in any harness. It runs in its own working directory
  and session, inside tmux with a log. Later rounds resume the same session.
- **The materials folder.** Give it a materials folder rather than the project:
  - the current draft, as a reference;
  - the exact data behind every figure, exported from the figure scripts;
  - the generated tables;
  - the numbers the text may use, each with its source;
  - the findings log;
  - the venue's style and writing guides.
- **The brief** fixes what is not the writer's to change: the claims, the numbers and the user's decisions. It rules out data
  processing and new experiments.

## From scratch, then choose

- **A new draft.** The writing model writes the whole paper anew rather than editing the old draft. It redraws every figure from
  the exported data and checks its own rendered pages.
- **Blind reviews.** Reviewers read each version independently, and a separate agent compares them. The user sees both and
  chooses the lead version.

## Polishing

- **Each round has a short brief,** in this order: the user's decisions verbatim, then plain errors, then review advice.
- **Division of edits.** Prose and figures change only through the writing model; data and claims only through the main model.
- **One visual concern per round.** Look at the rendered pages after each round, and show the user anything that is a matter of
  taste.

## Decisions for the user

These are the user's decisions:
- whether to rewrite;
- which writing model to use;
- the lead version;
- anything that would need new experiments.
