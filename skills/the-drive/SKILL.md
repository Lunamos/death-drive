---
name: the-drive
description: Use when starting, steering or continuing an open-ended research project with the user, when choosing the next step, when a result seems good enough to stop, or when an idea keeps failing its tests or stays uninteresting
---

# The drive

## Overview

The drive comes from the user's curiosity and vision (finding-the-question). The model supplies relentless, careful work toward
it: bold hypotheses, careful verification, and each result pushed toward its strongest true form. The model also lets go of
what has died. Life, attention and tokens are finite, while the pursuit is not.

Aim for milestone-level work. It teaches readers something they did not know, it closes its loop, and later work builds on it
and is guided by it.

## The loop

Origin -> think -> test -> narrate -> judge -> pursue -> ...

- **Origin:** the user's question and vision (finding-the-question).
- **Think:** form bold hypotheses, and find the cheapest experiment that decides them (building-evidence).
- **Narrate:** explain each finding plainly (narrating-work); load it before the first report.
- **Judge:** weigh the finding honestly against the origin and that ambition (judging-interest). Call ordinary results ordinary, and name the move
  that could make them extraordinary.
- **Pursue:** run the experiment that most strengthens the main claim, or do the consolidation it needs. Re-derive the story at
  each milestone (finding-the-story).

## Disciplines

- **Persist.** Keep going until the goal is met. Exploration is free; the goal is fixed. Letting a dead idea go is part of the
  pursuit, not the end of it.
- **Cheap tests first.** Run the cheapest decisive tests first, and costly ones when they are what answers the question.
- **Completeness.** Every reported result is consistent with the others under one main setting. A gap that could change the
  story gets an experiment; others go to the appendix.
- **Narrow, don't bury.** A result that does not fit narrows the claim, and it stays in the findings log.
- **One question, one complete work.** Merge what answers the same question, and archive the rest with traceable records.
- **Verify before reporting:** run it, render it, read it.
- **Independent critics.** After each block of results, a fresh subagent with no stake gets the claims, the scripts and the
  result files, and tries to break them: confounds, sample composition, measurement, incomplete runs, prior work. Every critic
  ends with the one or two experiments that would most strengthen or break the claim; run the one that could most change the
  story.
- **A fresh reader for interest.** When a result first looks surprising, and again before writing, a subagent that knows the
  field but not the project gets the question and predicts the answer. Then it sees the one-sentence claim and the main figure,
  and says what it did not expect and whether it would cite the work. "Nothing" or "I expected that" means the work is
  ordinary: reframe it or recommend stopping.
- **Approval before release.** Anything that leaves the machine goes out only after the user approves what goes where.

## Letting go

Persist while an idea has a live core, and let go when the core is gone.

- **A live core is still there when** a result is genuinely surprising, and:
  - an explanation survives intervention;
  - the signal grows as the tests get fairer.

  Then keep trying new angles. Surviving tests shows that a core is true, not that it is worth pursuing; truth alone does not
  keep it alive.
- **The core is gone when either holds:**
  - the idea itself fails fair verification;
  - after honest reframes, its best reachable version is still uninteresting.

  Then neither a modest paper nor a report is the outcome.
- **Ending well:**
  1. Write down what was tried, what was refuted and what it teaches.
  2. Archive it with traceable records.
  3. Tell the user plainly, recommending a stop.
  4. Return to the origin with a fresh idea.

A clean ending with its lessons frees the effort for the next beginning. This is a judgment on the idea, made after fair
attempts. It is not a shortcut around hard work.

## Other skills

Death Drive holds the judgments; the procedures come from other skills. Using them is part of the discipline.

- **Load the skills of each stage before working in it.** Look through the available skills, load the ones the stage needs,
  and name them in the plan:

  | Stage | Skills to look for |
  |---|---|
  | Mapping the field | literature and paper search, deep research |
  | Designing experiments | experimental design, statistical power |
  | Running and analyzing | the field's tools (e.g. interpretability libraries), statistical analysis |
  | Figures | figure planning, scientific visualization |
  | Writing and review | paper writing, anti-defensive writing, prose style and AI tells, claim and citation checks, rebuttal |

- **Give other agents their skills.** A subagent or a separate model gets the skills its task needs: name them in its brief,
  and make sure its host has them installed (for Codex, `~/.codex/skills`).
- **When a needed skill is missing,** add a well-maintained one: widely used, recently updated, concrete rather than generic,
  with a clear license. Take only the skills needed, never a whole catalog. Install it for every agent that will use it, and
  tell the user what was added.
- **Precedence.** When another skill conflicts with these judgments or with the user's decisions, these win.

## Roles

- **The user** supplies the drive (curiosity, vision and taste) and makes the decisions.
- **When the user is away,** make the decisions that would stall the work, record the alternatives, report each one
  (narrating-work) and continue. Release and spending still wait for the user.
- **The main model** maps, explores, designs, runs and verifies. It owns the truth.
- **A writing model** (Codex GPT-6 Astra, high or xhigh) presents and polishes, in its own environment. Only its rounds that
  improve the work are kept (writing-with-a-separate-model).
- **Subagents and other agents** do parallel work on separate tasks. Each project keeps its own workspace.
- **A launching agent** proposes projects and writes the goal for the one the user chooses (launching-a-researcher).

Work autonomously, and bring the user findings and decisions, not activity.
