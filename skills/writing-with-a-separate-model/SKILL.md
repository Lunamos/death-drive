---
name: writing-with-a-separate-model
description: Use when a paper, its figures or a talk should be written, rewritten or polished, or when reviews of a draft are needed to decide how to continue
---

# Writing with a separate model

## Overview

Thinking and presenting are different strengths:
- **The main model** owns the truth: questions, experiments, data and claims.
- **A separate writing model** owns the form: prose, figures, layout, polish and self-review.

The main model drafts, the writing model rewrites once, and from then on the work is edited, not redone. Figures that work
stay as they are.

## Setting up

- **The model.** The writing model is Codex running GPT-6 Astra at high or xhigh reasoning effort
  (`codex exec -m gpt-6-astra -c 'model_reasoning_effort="high"'`, or `"xhigh"`).
  - It runs in its own working directory and session, sandboxed to that directory, inside tmux with a log.
  - The tmux session closes when the work ends; the writer's session ID, kept in its directory, is enough to resume it.
  - Edits resume the same session (`codex exec resume <id>`).
- **Its skills.** The writing model needs writing skills of its own. Before the rewrite, check its skills folder
  (`~/.codex/skills` for Codex) for paper writing, figure planning, anti-defensive writing, prose style and AI tells, and
  claim and citation checks; install what is missing (the-drive, Other skills). The brief names the skills to load, in
  order: structure and claims first, then posture (anti-defensive writing), then sentences (prose style, AI tells).
- **The materials folder.** Give it a materials folder rather than the project:
  - the main model's first draft;
  - the plotting script for every figure, with the exact data behind it, exported from the analysis;
  - the generated tables;
  - the numbers the text may use, each with its source;
  - the findings log;
  - the novelty map (checking-novelty), so that the related work states differences result by result;
  - the venue's style and writing guides.
- **The brief** fixes what is not the writer's to change: the claims, the numbers and the user's decisions. It rules out data
  processing and new experiments.
- **The writer's notes.** The brief asks the writer to keep `NOTES.md`: numbers or claims it wanted but could not find, and
  disagreements between the materials. Read it as an audit of the materials.

## The pipeline

1. **First draft by the main model:** the story, the structure, the numbers, and a plotting script for every figure.
2. **One rewrite by the writing model.**
   - It rewrites the text, and redraws the figures through the plotting scripts, which stay in the paper folder.
   - The main figure may be a separate commission: a panel-by-panel brief (each panel's claim, its data file, the real lead
     example) to a separate session.
3. **One light check.** A blind reviewer compares the rewrite with the first draft (see below). If the rewrite is better, it
   becomes the lead version; if not, redo it once in a fresh session.
4. **Edit on top.**
   - Later changes are edits to the lead version, made by resuming the writer's session with a short brief: the user's
     decisions verbatim, then plain errors, then review advice.
   - Each edit round names what it fixes. A round that would only reshuffle wording is skipped.
   - There are no further rewrites.
5. **Figures inherit.**
   - Accepted figures are frozen. A figure changes only when a brief names it, and then by editing its plotting script.
   - Anything added to a figure replaces something else, or goes to a table or the appendix.
6. **Redo only for a new story.** A full rewrite happens only when the story changes substantially. Even then the plotting
   scripts are inherited.
7. **A strict review before finishing.** Before the paper is called finished, a blind reviewer at area-chair level reads only
   the PDF, searches the literature and scores it by a top venue's standard (the-drive, Finish what holds).

## Edits

- **Division of edits.** Prose and figures change only through the writing model; data and claims only through the main model.
- **Numbers in the prose.** At most one key number per sentence in the abstract and introduction; intervals and details go to
  figures, tables and the appendix. A paper whose sentences each carry several statistics reads as a results log, and the
  idea gets lost. The brief says so.
- **Look at the rendered pages** after each edit, and show the user anything that is a matter of taste.

## Watching for a degraded writer

Astra's quality varies from run to run. Check where it can do damage: the rewrite, a redrawn figure, a large edit.
- **Light and anchored.** One blind reviewer (random labels, document metadata stripped) answers: "which version is better,
  and what got worse?".
  - Compare with the lead version, not only with the previous step: small changes that each look fine can add up.
  - A version that does not improve the work counts as worse; keep the lead version.
- **Figures on their own.** Judge each changed figure side by side with its accepted version, at print size, by the user's
  standard:
  - readable at a glance;
  - one message per panel;
  - few marker types;
  - legible fonts;
  - no prose inside the figure.

  More information is not better if it costs readability. A figure that regresses keeps its accepted version.
- **Claim before accuracy.** The reviewer first states the paper's claim in one sentence and says whether it is interesting;
  accuracy comes second. A more accurate version that loses the claim from the abstract is worse. Audit the numbers in full
  once, on the final candidate.
- **Signs of degraded work:**
  - the claim blurred, or gone from the abstract;
  - claims beyond the brief, new overclaims or new hedges;
  - numbers that are not in the numbers file, or a result attached to a setting where it was not measured;
  - several names for one thing, or terms drifting away from the figures;
  - sentences carrying several numbers each;
  - content silently dropped, and repeated or garbled sentences;
  - figures growing denser (more panels, markers, annotations or text boxes), or layout that regresses;
  - internal names or revision history leaking into the text;
  - explicit instructions in the brief left undone.
- **Redoing.** A fresh session with a narrow brief and a short list of exact changes changes less and breaks less.

## Decisions for the user

These are the user's decisions:
- whether to rewrite;
- which writing model to use;
- the lead version, when there is a choice;
- anything that would need new experiments.

When the user is away, decide by the blind check, and report the choice with the alternatives.
