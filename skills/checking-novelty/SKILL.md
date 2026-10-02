---
name: checking-novelty
description: Use when choosing a research question, when a result first looks new or surprising, when the story is re-derived at a milestone, before writing a paper, and before calling a work finished, to find the closest prior results and state exactly what this work adds
---

# Checking novelty

## Overview

A result is new only relative to the closest prior *result*, not to the papers that happen to be cited. Citing the closest
work without saying what it already shows is how a paper loses its novelty in review. The novelty check finds those results,
reads them, and writes down what this work adds beyond each one.

## When

- **Choosing a question** (finding-the-question): for each candidate direction, before investing in it.
- **A result first looks surprising:** a quick check, before building on it.
- **At each milestone** (finding-the-story): the current claim is checked, and the novelty map is updated.
- **Before writing, and in the strict review before finishing** (the-drive): a full check.

Scale the check to the moment: a quick search when a result is fresh, and a full check when the claim is about to be written
down or committed to.

## How

1. **Split the claim.** Write the one-sentence claim, then its parts separately: the phenomenon, the method, the systems and
   the conclusion.
2. **Search each part.**
   - Search the phenomenon in the words other fields would use, the method, the systems and data, and the conclusion as others
     would phrase it.
   - Cover the last twelve months: preprints, workshop papers, lab blog posts.
   - Cover the user's own prior work.
   - Follow forward citations of the closest works.
   - Use the available literature-search skills.
3. **Read the closest results themselves.** For the three to five closest, read what was shown, on which systems and how
   large it was, not only the abstract.
4. **Write the novelty map** in the project (e.g. `NOVELTY.md`). For each closest result, record:
   - what it shows;
   - what this work adds: a new question, broader systems, a causal rather than correlational test, a quantitative law, or a
     contradiction resolved;
   - whether the overlap changes the claim.
5. **Verify every reference.** Check that it exists and says what is attributed to it. References proposed by a subagent or
   a search summary are hypotheses until read.

## Reading the outcome

- **New:** proceed. The paper's related work states the differences result by result, from the novelty map.
- **Partly done:** narrow the claim to what is new, or reframe it so that the prior result becomes a special case or the
  starting point. The positioning is written in the paper, never left for reviewers to find.
- **Done:** a replication is not the work, unless this version overturns the earlier result. Let the idea go (the-drive,
  "Letting go").
- **Scooped during the work:** check quickly what remains new, narrow or reframe, and tell the user.

## Effort

- **Breadth:** a subagent with search tools per angle of the search (phenomenon, method, conclusion), never several doing the
  same search.
- **Depth:** the main model reads the closest results itself, because what they show decides the claim.
