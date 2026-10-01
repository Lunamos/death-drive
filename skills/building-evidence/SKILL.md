---
name: building-evidence
description: Use when designing experiments, testing a hypothesis or causal claim, checking whether a result generalizes, resolving results that conflict with each other or with prior work, and before calling a result finished
user-invocable: false
---

# Building evidence

## Overview

Hypothesize boldly, verify carefully. A claim is strong when it meets four tests:
- an intervention demonstrates it;
- controls exclude the obvious alternatives;
- independent methods agree;
- it predicts cases it has not seen.

## Designing experiments

- **Missing or unused?** Ask whether a failure comes from a missing ability or from an ability that is present but unused.
  Decide with the smallest intervention that could reveal it, with everything else held fixed.
- **Controlled settings.** Prefer settings where the variable of interest is set directly and the measurement is exact, and
  track progress with one summary measure.
- **Breadth.** Test across the systems, scales and conditions that matter, and across more than one kind of task or data. Add
  an independent replication, e.g. a system built from scratch, to see whether the account emerges on its own.
- **Practice.** Carry the result to a real setting where it can matter in practice.

- **Explore, then freeze.** Explore with cheap tests, each with its matched control, until a result surprises or kills the
  idea; then freeze the design and the predictions to confirm it.

Load the skills for experimental design, statistics and the field's tools before designing (the-drive, Other skills).

## Causal claims

- **Use needs intervention.** Observations show what is present; interventions show what is used or what causes what. Base
  every causal claim on an intervention.
- **Matched controls.** Give each intervention a matched control:
  - a random change of equal size;
  - the same change applied elsewhere;
  - no change.
- **Convergence.** Look for agreement across observations, interventions and independent replications.

## Predictions

1. Turn the explanation into a rule for new cases.
2. Before testing, commit the rule, the predicted values and the result that would kill the idea. Design the test so that
   either outcome points to the next question.
3. Report the hits and the misses.

## Before a result counts as finished

- **Measures.** Run each measure where its answer is known, and check it against blind labels made by reading raw cases, with
  a second annotator for the key ones.
- **Inputs.** Check on raw items that every item contains what the task needs, in the intended format and order; nothing
  needed is dropped or truncated.
- **Independent re-implementation.** An agent that has not seen the reported values recomputes the key numbers from raw files
  with its own code.
- **Matched control and replication.** A change of matched size on an unrelated target, and a replication on new items with a
  new seed.
- **Raw cases.** Read 10-20 raw cases behind each number a claim rests on. Numbers come only from finished runs.

## Records

- **Every run** records its settings, seeds and per-item outputs.
- **Comparisons** run all methods on the same items, and report paired intervals.
- **The findings log** is written as results land, including those that do not fit.
- **Traceability.** Every claim traces to its result files and commands.
- **Main-setting changes.** When the main setting changes, re-run everything reported under it.

## Conflicts

When results disagree (ours with ours, or ours with prior work), compare the setups line by line: systems, data, order,
protocol and measurement. Existing controls often settle the question; otherwise, design the experiment that does.
