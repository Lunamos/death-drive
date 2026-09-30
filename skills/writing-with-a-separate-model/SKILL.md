---
name: writing-with-a-separate-model
description: Use when a paper, its figures or a talk should be written, rewritten or polished, or when reviews of a draft are needed to decide how to continue
---

# Writing with a separate model

## Overview

Thinking and presenting are different strengths:
- **The main model** owns the truth: questions, experiments, data and claims.
- **A separate writing model** owns the form: prose, figures, layout, polish and self-review.

Keep them apart, give the writing model exactly what it needs, keep only the rounds that improve the work, and let the
user's taste choose.

## Setting up

- **The model.** The writing model is Codex running GPT-6 Astra at high or xhigh reasoning effort
  (`codex exec -m gpt-6-astra -c 'model_reasoning_effort="high"'`, or `"xhigh"`). It runs in its own working directory and
  session, sandboxed to that directory, inside tmux with a log. Later rounds resume the same session
  (`codex exec resume <id>`); a round that degrades is redone in a fresh session.
- **Its skills.** The writing model needs writing skills of its own. Before the first round, check its skills folder
  (`~/.codex/skills` for Codex) for paper writing, figure planning, anti-defensive writing, prose style and AI tells, and
  claim and citation checks; install what is missing (the-drive, Other skills). The brief names the skills to load, in
  order: structure and claims first, then posture (anti-defensive writing), then sentences (prose style, AI tells).
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

## Watching for degraded rounds

Astra's quality varies from run to run: some rounds are sharp, others are clearly worse. A rewrite is only a candidate.
- **Keep only improvements.** After each round, compare the new version with the one it would replace, blind (random
  labels, document metadata stripped). If it is better, keep it. If it does not improve the work, count it as worse: keep
  the previous version and redo the round, in a fresh session or later.
- **Keep the check light.** For a rewrite or polishing round, one blind reviewer asked "which version is better, and what
  got worse?" is enough. Several reviewers are for choosing between independent drafts.
- **Signs of a degraded round:**
  - claims beyond the brief, new overclaims or new hedges;
  - numbers that are not in the numbers file, or a result attached to a setting where it was not measured;
  - several names for one thing, or terms drifting away from the figures;
  - content silently dropped, and repeated or garbled sentences;
  - figures or layout that regress;
  - internal names or revision history leaking into the text;
  - explicit instructions in the brief left undone.
- **Redoing a round.** A fresh session with a narrow brief, a short list of exact changes, changes less and breaks less.

## Decisions for the user

These are the user's decisions:
- whether to rewrite;
- which writing model to use;
- the lead version;
- anything that would need new experiments.
