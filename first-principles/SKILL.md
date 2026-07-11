---
name: first-principles
description: Analyze complex or novel problems from first principles by separating objectives, evidence, hard constraints, and inherited conventions before generating and comparing solutions. Use when the user explicitly asks for first-principles reasoning, challenges assumptions, or needs architecture or process tradeoff analysis where standard patterns may obscure alternatives.
---

# First Principles Thinking

Analyze the problem from its underlying objectives and constraints rather than copying a familiar solution by default.

## Boundaries

- Treat user intent, safety, law, ethics, privacy, security, accessibility, and human impact as real constraints. Do not dismiss them as conventions for the sake of optimization.
- Distinguish facts, estimates, assumptions, preferences, and unknowns. Do not invent evidence or present uncertain claims as fundamental truths.
- Account for multiple objectives and failure modes. A single measurable target may omit important consequences.
- Prefer reversible tests before high-cost or high-impact changes.
- Preserve appropriate human review for consequential decisions.

First-principles reasoning is a method for exposing assumptions. It is not permission to ignore people, governance, or domain expertise.

## Method

### 1. Define the Objective

- State the outcome the user is trying to achieve.
- Separate the outcome from the proposed implementation.
- Identify success measures and acceptable failure thresholds where possible.
- Surface competing objectives instead of forcing them into one metric.

### 2. Inventory the Constraints

Classify each relevant statement:

- **Observed fact:** Supported by direct evidence.
- **Hard constraint:** A physical, mathematical, technical, or resource limit.
- **Governance constraint:** A legal, safety, ethical, privacy, security, policy, accessibility, or accountability requirement.
- **Preference:** A user or stakeholder choice that should be preserved or explicitly negotiated.
- **Convention:** A familiar pattern that may be changed.
- **Assumption or unknown:** A claim that needs evidence or testing.

Ask what evidence supports each item and how costly it would be to test.

### 3. Establish a Baseline

Describe the conventional or current approach fairly. Note what it does well, what it protects against, and where it fails. Do not treat novelty as evidence of quality.

### 4. Generate Alternatives

Develop options from the objective and validated constraints:

- Improve the conventional baseline.
- Remove or replace assumptions that are not required.
- Change the interface, sequence, level of automation, or system boundary.
- Consider direct system integration when it is safer and more reliable than reproducing a manual interface.
- Keep human-readable controls when review, trust, accessibility, or recovery requires them.

Generate only enough alternatives to expose meaningful tradeoffs.

### 5. Compare Tradeoffs

Evaluate each viable option against:

- expected benefit;
- evidence quality;
- cost and time;
- safety, security, privacy, and compliance risk;
- usability and accessibility;
- reversibility and recovery;
- operational complexity;
- failure modes and blast radius.

Use quantitative estimates only when their basis is available. Label estimates and sensitivity ranges clearly.

### 6. Recommend And Test

- Recommend an option and explain why it best fits the stated constraints.
- Name the strongest argument against it.
- Propose the smallest experiment that could disprove the key assumption.
- Define what evidence would change the recommendation.
- List unresolved risks and the review needed before a consequential rollout.

## Design Lanes

Two broad design lanes are often useful:

### Interface-Compatible

Preserve familiar workflows or interfaces when people need to understand, audit, approve, or recover the process, or when a legacy system exposes no safer integration.

### Objective-Oriented

Redesign the workflow around the desired outcome when systems can exchange structured data directly and the approach remains secure, observable, governable, and recoverable.

These lanes can be combined. For example, a system may use direct APIs internally while retaining a clear human approval and audit interface.

## Output Shape

For a substantial problem, organize the response as:

1. **Objective and success measures**
2. **Known facts and evidence**
3. **Constraints**
4. **Assumptions to test**
5. **Candidate approaches**
6. **Tradeoff comparison**
7. **Recommendation**
8. **Smallest useful experiment**
9. **Risks, unknowns, and review needs**

Keep the structure proportional. A narrow question may need only a few concise paragraphs.

## Cautionary Example

In the 2017 FAIR negotiation study, goal-oriented training improved negotiation performance but also caused divergence from human-like language. The researchers mixed reinforcement learning with supervised updates to preserve human-readable communication. The lesson is not that human conventions should always win; it is that an objective can omit important requirements unless they are represented as constraints and evaluated explicitly.

Remember: rebuilding from fundamentals can confirm the standard approach. The goal is a better-supported decision, not a more unusual one.
