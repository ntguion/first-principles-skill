---
name: first-principles
description: Apply first principles thinking to complex problems by breaking them down to fundamental truths and reasoning up from there. Use when tackling novel problems, designing systems, optimizing workflows, questioning assumptions, or when traditional approaches may be limiting. Particularly valuable for architecture decisions, automation strategy, and situations where the user requests 'first principles', 'fundamental approach', or 'alien solutions'. Works across all domains - technical, process, business, and creative problems.
---

# First Principles Thinking

Apply first principles thinking to decompose problems into fundamental truths and build solutions from the ground up, rather than reasoning by analogy.

## Core Methodology

**First principles thinking** means boiling problems down to their most fundamental, indisputable truths—then reasoning up from there. It contrasts with **reasoning by analogy**, where solutions copy what others do with slight variations.

### The Three-Step Process

1. **Question All Assumptions**
   - List every assumption, belief, and "best practice" about the problem
   - Challenge each one: "What if this isn't true?" or "Why do we believe this?"
   - Identify which are actually fundamental constraints vs inherited conventions

2. **Deconstruct to Fundamental Truths**
   - Break the problem down to its most basic, indivisible elements
   - Ask: "What are we absolutely sure is true?"
   - Focus on physical constraints, mathematical truths, or core requirements
   - Seek the "physics of the problem" - the immutable realities

3. **Rebuild from the Ground Up**
   - Use only the fundamental truths as your foundation
   - Design solutions without inheriting human workflows or historical approaches
   - Consider "alien solutions" - approaches that seem strange but are mathematically superior
   - Optimize for the objective function, not for familiarity

## Key Principles

### Distinguish Between Two Design Lanes

When solving problems, recognize two valid approaches:

**Biomimicry (Human-Centric)**
- Replicate how humans do it: linear processing, visual interfaces, familiar patterns
- Use when: Humans need to audit the process, legacy systems require UI interaction, user trust requires transparency
- Example: An agent that opens a browser, searches LinkedIn, and copies to CRM

**First Principles (Objective-Centric)**
- Solve for the objective function directly, ignoring human constraints
- Use when: Pure outcome efficiency matters, systems can communicate natively, parallel processing is possible
- Example: An agent that spawns 1000 parallel threads, queries APIs directly, processes data via vector operations

Both approaches are valid - choose based on the problem's constraints and goals.

### Question the "How Humans Do It"

Human workflows often encode biological limitations that don't apply to computational systems:

- **Categorical organization** → May not be optimal (see: Amazon's "chaos storage")
- **Serial processing** → Parallel is often possible and faster
- **Visual interfaces** → Direct API access may be more efficient
- **Natural language** → Structured data exchange may be superior
- **Step-by-step SOPs** → Might be decomposable into concurrent operations

### Focus on Physics, Not Convention

Ask questions like:
- "What are the actual physical/mathematical constraints?"
- "What is the objective function we're optimizing?"
- "What would this look like if we designed it from scratch today?"
- "What information actually needs to flow, ignoring how it currently flows?"

## Illustrative Examples

**SpaceX Rockets**
- Conventional: "Rockets cost $65M because that's the market price"
- First principles: "What is a rocket made of? Aluminum, titanium, copper, carbon fiber. What do those materials cost? About 2% of the rocket price."
- Result: Built rockets at 10x lower cost

**Amazon Fulfillment** (Chaos Storage)
- Conventional: Organize warehouse by category (shirts with shirts) for human retrievability
- First principles: Optimize for travel paths and congestion, place items randomly, let algorithms remember locations
- Result: Faster fulfillment despite appearing chaotic to humans

**Agent Communication** (Facebook AI)
- Conventional: Agents should speak grammatical English
- First principles: Agents optimized for information bandwidth, developed shorthand tokens
- Result: More efficient communication, though alien-looking to humans

## Application to Current Task

When applying first principles to the user's problem:

1. **Identify the real objective** - What outcome are we actually trying to achieve?

2. **List all assumptions** - What are we assuming about how this must be done?

3. **Find the fundamentals** - What are the immutable constraints (physics, math, core requirements)?

4. **Consider alien solutions** - What would an optimal solution look like if we ignored human conventions?

5. **Choose the appropriate lane**:
   - If humans need to audit/understand: Use biomimicry but with optimizations
   - If pure efficiency matters: Design from first principles

6. **Reason up from scratch** - Build the solution based only on fundamental truths

Remember: The goal isn't to be different for the sake of being different. It's to avoid being trapped by conventions that don't serve the objective function. Sometimes the human way is optimal; sometimes there's a Move 37 waiting to be discovered.
