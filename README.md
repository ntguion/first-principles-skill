# First Principles Thinking Skill

An Agent Skill for analyzing complex problems by separating objectives, evidence, constraints, and inherited conventions before comparing possible solutions.

The skill is designed for Claude Code and follows the portable [Agent Skills](https://agentskills.io/) directory format.

## What It Does

The skill guides an analysis through a repeatable sequence:

1. Define the actual objective and success criteria.
2. Separate known facts from estimates and assumptions.
3. Classify hard constraints, governance constraints, and inherited conventions.
4. Generate a conventional baseline and at least one alternative derived from the stated constraints.
5. Compare tradeoffs, failure modes, reversibility, and evidence quality.
6. Recommend the smallest useful test or next step.

It is most useful for novel problems, architecture decisions, workflow redesign, and situations where a familiar pattern may be hiding a better option.

## What It Does Not Do

First-principles reasoning does not make safety, law, ethics, privacy, accessibility, user intent, or human impact optional. Those are real design constraints. It also cannot replace missing domain evidence or decide value judgments on the user's behalf.

## Installation

Claude Code discovers skills from directories containing a `SKILL.md` file.

### Personal Skill

Install the skill for use across projects:

```bash
git clone https://github.com/ntguion/first-principles-skill.git
mkdir -p ~/.claude/skills/first-principles
cp first-principles-skill/first-principles/SKILL.md \
  ~/.claude/skills/first-principles/SKILL.md
```

### Project Skill

Copy the skill into a repository when it should be shared with that project:

```bash
mkdir -p .claude/skills/first-principles
cp /path/to/first-principles-skill/first-principles/SKILL.md \
  .claude/skills/first-principles/SKILL.md
```

Claude Code detects skills in these locations. If a new top-level skills directory is not detected in an existing session, restart that session.

## Usage

Invoke the skill directly:

```text
/first-principles Design a caching strategy for API responses with strict freshness requirements.
```

Claude Code may also load it when a request matches the activation description in the skill frontmatter.

The response should identify:

- the objective and success measures;
- known constraints and evidence;
- assumptions worth testing;
- candidate approaches and tradeoffs;
- a recommendation;
- the smallest useful experiment;
- remaining risks and unknowns.

## Example

For a notification system, the analysis might question whether every event needs immediate push delivery while preserving non-negotiable requirements such as consent, accessibility, delivery reliability, and user control. It could then compare a conventional push-first design with a tiered design that uses different channels for critical, timely, and ambient events.

The point is not to choose the unusual design automatically. The point is to expose assumptions and compare options against explicit objectives and constraints.

## Validation

Run a basic frontmatter and path check from the repository root:

```bash
ruby -ryaml -e 'text = File.read("first-principles/SKILL.md"); data = YAML.safe_load(text.split(/^---\s*$\n/, 3)[1]); abort unless data["name"] == "first-principles" && data["description"].is_a?(String)'
```

The repository intentionally keeps `first-principles/SKILL.md` as the single distributable source instead of maintaining a duplicate packaged archive.

## Limitations

- Results depend on the accuracy and completeness of the stated facts and constraints.
- A novel alternative is not necessarily better than a proven pattern.
- Quantitative claims still need data, benchmarks, or experiments.
- High-impact decisions need domain review and proportionate human oversight.
- Some conventions encode lessons that are easy to lose when rebuilding from scratch.

## Sources And Inspiration

- Chase Hughes, [Beyond the Replica: The Case for First-Principles Agents](https://www.chasewhughes.com/writing/beyond-the-replica-the-case-for-first-principles-agents)
- Lewis et al., [Deal or No Deal? End-to-End Learning for Negotiation Dialogues](https://arxiv.org/abs/1706.05125), used here as a caution that optimizing a measurable goal can degrade an unmodeled requirement such as human-readable communication

## Contributing

Issues and pull requests are welcome, especially for clearer activation criteria, stronger evaluation methods, and examples with well-supported tradeoffs.

## License

MIT License. See [LICENSE](LICENSE).
