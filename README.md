# First Principles Thinking Skill

A Claude Code skill that enables first principles thinking for complex problem-solving. Break down problems to fundamental truths and rebuild solutions from the ground up, rather than reasoning by analogy.

## Overview

This skill teaches Claude to apply first principles thinking—a methodology popularized by physicists and innovators like Elon Musk. Instead of copying what others do with slight variations (reasoning by analogy), first principles thinking means:

1. **Question all assumptions** - Challenge every belief, "best practice," and inherited convention
2. **Deconstruct to fundamental truths** - Find the immutable constraints (physics, math, core requirements)
3. **Rebuild from scratch** - Design solutions based only on fundamental truths, not traditions

## When to Use

The skill automatically triggers for:

- **Complex/novel problems** where traditional approaches may be limiting
- **System design & architecture** decisions
- **Process optimization** and automation strategy
- **Workflow efficiency** challenges
- Situations requiring **"alien solutions"** - approaches that seem strange but are mathematically superior

You can also explicitly invoke it: `/first-principles [your problem]`

## Key Concepts

### Two Design Lanes

The skill helps you distinguish between two valid approaches:

**Biomimicry (Human-Centric)**
- Replicate how humans do it: linear processing, visual interfaces, familiar patterns
- Use when humans need to audit the process or legacy systems require UI interaction

**First Principles (Objective-Centric)**
- Solve for the objective function directly, ignoring human constraints
- Use when pure outcome efficiency matters and systems can communicate natively

### Real-World Examples

The skill references proven examples of first principles thinking:

- **SpaceX Rockets**: Questioned why rockets cost $65M, analyzed material costs (2% of price), built at 10x lower cost
- **Amazon Fulfillment**: Abandoned categorical organization for "chaos storage" - random placement optimized for travel paths
- **AI Communication**: Facebook's agents developed shorthand tokens instead of grammatical English for bandwidth efficiency

## Installation

### Option 1: Install .skill file

Download `first-principles.skill` and install via Claude Code:

```bash
claude skills install first-principles.skill
```

### Option 2: Install from source

Clone this repository and package the skill:

```bash
git clone https://github.com/ntguion/first-principles-skill.git
cd first-principles-skill/first-principles
# Package and install through Claude Code
```

## Usage

Once installed, the skill will automatically activate when you're working on complex problems. You can also explicitly invoke it:

```
/first-principles Design a caching system for API responses
```

The skill will guide you through:
1. Identifying the real objective
2. Listing all assumptions about how it "must" be done
3. Finding fundamental constraints (physics, math, requirements)
4. Considering "alien solutions" that ignore human conventions
5. Choosing between biomimicry and first principles approaches
6. Reasoning up from fundamental truths

## Example Session

**User**: "I need to build a notification system. The standard approach is Firebase Cloud Messaging with a bell icon and badge count."

**Claude (with skill)**:
- Questions assumptions: Must notifications be push? Must we show all history? Is badge count optimal?
- Identifies fundamentals: Core objective is "inform users of important state changes" with limited attention
- Proposes first principles solution: Tiered delivery (SMS for critical, push for timely, in-app for ambient), event stream architecture, adaptive interruption based on user behavior
- Distinguishes: Use biomimicry for UI (bell icon), first principles for architecture (event stream)

## Philosophy

As described in Chase Hughes' "[Beyond the Replica: The Case for First-Principles Agents](https://chasewughes.com)":

> "If we limit agents to only doing what humans do—exactly how humans do it—we trap them in a local optimum. To unlock the true promise of the 'Agent OS' era, we need to be willing to ask: When should we automate the worker, and when should we solve the problem?"

This skill embodies that philosophy—helping you identify when to think like a human and when to think like an alien intelligence optimizing purely for the objective function.

## Contributing

Issues and pull requests welcome! If you discover improvements to the skill's methodology or find it triggers in situations where it shouldn't (or vice versa), please open an issue.

## License

MIT License - see LICENSE file for details

## Acknowledgments

- Inspired by [Chase Hughes' "Beyond the Replica"](https://chasewughes.com) article on first principles agents
- Methodology based on Elon Musk's approach to problem-solving
- Examples drawn from SpaceX, Amazon, Facebook AI Research, and other real-world applications
