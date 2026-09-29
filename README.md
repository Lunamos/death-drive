# Todestrieb

*A drive for research: how to think, present, polish, review, and never stop pursuing.*

These Claude Code skills hold the decisions and disciplines that make research good:
- where the drive comes from: the user's curiosity and vision;
- how a question becomes worth pursuing, and how a finding becomes interesting and true;
- how to tell a finding, and how the story is re-derived from the evidence as the project moves;
- how a separate writing model turns the story into a finished paper;
- when to let an idea go.

Procedures such as LaTeX, plotting and submission are left to other skills.

| Skill | Invoked by | Use it when |
|---|---|---|
| `the-drive` | agent or `/` | Starting, steering or continuing an open-ended research project |
| `finding-the-question` | agent or `/` | Starting out, returning to the origin, or when the direction is unclear |
| `judging-interest` | agent or `/` | Choosing a direction, weighing a new result, or deciding whether work is ready |
| `building-evidence` | agent | Designing experiments, testing causal claims, or resolving conflicting results |
| `narrating-work` | agent | Reporting findings, progress or problems to the user |
| `finding-the-story` | agent or `/` | Reaching a milestone, or deciding what and how to present |
| `writing-with-a-separate-model` | agent or `/` | Writing, rewriting or polishing a paper with a separate writing model |

## Install

From GitHub, as a Claude Code plugin:

```bash
claude plugin marketplace add Lunamos/todestrieb
claude plugin install todestrieb@lunamos
```

Or clone the repository and link the skills into your personal skills folder:

```bash
git clone https://github.com/Lunamos/todestrieb.git
ln -s "$PWD"/todestrieb/skills/* ~/.claude/skills/
```

## License

MIT
