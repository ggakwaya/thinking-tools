---
name: analytical-framework
description: "Apply theoretical frameworks as diagnostic tools rather than definitions to recite. Use this skill whenever the user asks to analyze a situation, case, organization, or problem using a named theory, model, or framework, or when the user is preparing for an evaluation that tests applied understanding. Also trigger when the user says things like 'apply X to this case', 'analyze this using Y', 'what does theory Z tell us about this situation', or 'help me use this model'. This skill transforms encyclopedic knowledge of theories into diagnostic reasoning."
---

# Analytical Framework Application

## Core Principle

A theoretical framework is not an answer, it is a **lens**. The goal is never to describe the lens. The goal is to describe **what you see through it**.

## Procedure

When the user asks to apply a framework to a situation, follow this sequence strictly:

### Step 1 - Identify the activated tool

Determine which framework the question activates. If the user names it explicitly, confirm. If the question is ambiguous, identify 2-3 candidate frameworks and ask which angle the user wants, or apply the most relevant one and flag the alternatives.

### Step 2 - Formulate the diagnostic question

Every framework answers a specific question. Before applying it, state that question explicitly. This prevents drifting into generic description.

Examples of diagnostic questions:
- Legitimacy: "Is this organization perceived as socially acceptable in its environment?"
- Agency theory: "Is the bureaucracy here justified by operational needs or by the principal-agent dynamic?"
- Stakeholder mapping: "Who matters, who doesn't, and where should this organization invest its time?"

If a domain-specific configuration skill is available (e.g., a course-specific skill), load the diagnostic questions from there.

### Step 3 - Apply, don't describe

Structure the response as:

1. **The mechanism** (2-3 sentences): What the framework reveals about *this specific case*. Not what the framework says in general, what it says about *this*. Name the causal mechanism, not the definition.

2. **The nuance** (2-3 sentences): The condition, context, tension, or complication that makes this case non-trivial. This is where depth lives.

3. **The consequence** (1-2 sentences): What this means concretely, a recommendation, a risk, a prediction, a tradeoff.

### Step 4 - Name the authors when it matters

If the framework has named originators that signal mastery of the material (especially in academic contexts), include them naturally in the mechanism statement. Don't drop names decoratively, integrate them as part of the reasoning.

## Anti-Patterns to Avoid

**The Encyclopedia Entry**: Starting with "Theory X, developed by Author Y in Year Z, states that..." This is description, not application. The framework should appear *inside* the analysis, not as a preamble to it.

**The Label Without the Because**: Saying "this is an example of isomorphism" without explaining *why* it's isomorphism and *what mechanism* makes it so. The label alone earns zero diagnostic value.

**The Abstract Float**: Applying the framework without anchoring it in concrete, observable details of the case. If the analysis could apply to any organization, it's not diagnostic, it's generic.

**The Single-Lens Tunnel**: Applying only the requested framework when a second framework would visibly strengthen the analysis. Check whether a cross-domain link is productive (see cross-domain-linking skill if available). But don't force connections, a productive link enriches; a decorative one dilutes.

## Calibration

The depth and formality of the analysis should match the context:
- **Exam preparation**: Match the expected answer format of the evaluator. If an evaluator-calibration skill is available, load format expectations from there.
- **Professional analysis**: Prioritize actionable consequences over theoretical elegance.
- **Exploratory conversation**: Allow more speculative reasoning, flag uncertainty openly.

## Loading Domain-Specific Frameworks

This skill is domain-agnostic. It operates on whatever frameworks are provided in context. If a domain-specific configuration skill exists (e.g., for a course, a field, or a project), load the list of available frameworks, their diagnostic questions, key authors, and expected mechanisms from that skill.

Without a domain configuration, ask the user: "What framework would you like me to apply, and what's the situation you want to analyze?"
