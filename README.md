# Death Drive

*A drive for research: how to think, present, polish, review, and never stop pursuing.*

The name is Freud's *Todestrieb*. Life and attention are finite while the pursuit is not: pursue an idea relentlessly while
it lives, and let it die when it is dead.

These Claude Code skills hold the decisions and disciplines that make research good:
- where the drive comes from: the user's curiosity and vision;
- how a question becomes worth pursuing, and how a finding becomes interesting and true;
- how to tell a finding, and how the story is re-derived from the evidence as the project moves;
- how a separate writing model (Codex GPT-6 Astra) turns the story into a finished paper, keeping only the rounds that
  improve it;
- when to let an idea go.

Procedures such as literature search, statistics, plotting and paper craft are left to other skills. The skills here tell the
agent to load them at each stage, and to give a separate writing model its own.

| Skill | Invoked by | Use it when |
|---|---|---|
| `the-drive` | agent or `/` | Starting, steering or continuing an open-ended research project |
| `finding-the-question` | agent or `/` | Starting out, returning to the origin, or when the direction is unclear |
| `judging-interest` | agent or `/` | Choosing a direction, weighing a new result, or deciding whether work is ready |
| `building-evidence` | agent | Designing experiments, testing causal claims, or resolving conflicting results |
| `narrating-work` | agent | Reporting findings, progress or problems to the user |
| `finding-the-story` | agent or `/` | Reaching a milestone, or deciding what and how to present |
| `writing-with-a-separate-model` | agent or `/` | Writing, rewriting or polishing a paper with a separate writing model (Codex GPT-6 Astra) |

## Install

From GitHub, as a Claude Code plugin:

```bash
claude plugin marketplace add Lunamos/death-drive
claude plugin install death-drive@lunamos
```

Or clone the repository and link the skills into your personal skills folder:

```bash
git clone https://github.com/Lunamos/death-drive.git
ln -s "$PWD"/death-drive/skills/* ~/.claude/skills/
```

## Companion skills

These are well-maintained collections that fit the skills here. Take only the individual skills you need, and install them
for both Claude Code and Codex.

| Stage | Skills | Source |
|---|---|---|
| Mapping the field | `paper-lookup`, `huggingface-papers` | [K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills), [huggingface/skills](https://github.com/huggingface/skills) |
| Experiments and statistics | `experimental-design`, `statistical-power`, `statistical-analysis` | K-Dense-AI/scientific-agent-skills |
| Interpretability tools | `transformer-lens`, `nnsight`, `saelens`, `pyvene` | [Orchestra-Research/AI-Research-SKILLs](https://github.com/Orchestra-Research/AI-Research-SKILLs) |
| Figures | `figure-planner`, `scientific-visualization`, `academic-plotting` | [Boom5426/Nature-Paper-Skills](https://github.com/Boom5426/Nature-Paper-Skills), K-Dense, Orchestra |
| Paper structure | `ml-paper-writing`, `research-paper-writing` | Orchestra, [Master-cai/Research-Paper-Writing-Skills](https://github.com/Master-cai/Research-Paper-Writing-Skills) |
| Posture and prose | `anti-defensive-writing`, `scientific-prose-style`, `humanizer` | Boom5426/Nature-Paper-Skills, [blader/humanizer](https://github.com/blader/humanizer) |
| Checks and review | `claim-source-verification`, `citation-verifier`, `citation-management`, `stats-reporting-audit`, `rebuttal-response` | Boom5426, K-Dense |

With the GitHub CLI (2.9 or later), for example:

```bash
gh skill install Boom5426/Nature-Paper-Skills skills/core/anti-defensive-writing/SKILL.md --agent claude-code --scope user
gh skill install Boom5426/Nature-Paper-Skills skills/core/anti-defensive-writing/SKILL.md --agent codex --scope user
```

## License

MIT
