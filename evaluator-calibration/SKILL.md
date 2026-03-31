---
name: evaluator-calibration
description: "Decode an evaluator's implicit expectations and calibrate responses accordingly. Use this skill whenever the user is preparing for an evaluation (exam, assignment, presentation, interview, grant application, client pitch) and wants to maximize their score or impact by understanding what the evaluator actually rewards. Also trigger when the user shares grading rubrics, past corrections, evaluator feedback, or asks 'what does this professor/boss/reviewer actually want?' This skill turns evaluation artifacts into a strategic profile of the evaluator."
---

# Evaluator Calibration

## Core Principle

Every evaluator has a **revealed preference structure** — what they actually reward — that may differ from their **stated preference structure** — what they say they reward. The gap between the two is where most points are lost. This skill closes that gap.

## Phase 1 — Collect Evidence

Gather evaluator artifacts. Each type reveals different information:

| Artifact | What it reveals |
|----------|----------------|
| Past exam/assignment questions | What the evaluator considers important enough to test |
| Answer keys / corrected work | The *format* and *depth* that earn full marks |
| Grading rubrics | Stated criteria (useful but often incomplete) |
| Evaluator's verbal instructions | Priorities, pet peeves, emphasis patterns |
| The user's past graded work | What specifically earned or lost points *for this user* |
| Evaluator's own publications or work | Intellectual commitments and theoretical allegiances |

Prompt the user for whichever artifacts are available. The more types, the sharper the profile.

## Phase 2 — Identify Patterns

Analyze the collected evidence to extract recurring patterns across five dimensions:

### 2.1 — What is tested?
- Does the evaluator favor definitions, mechanisms, applications, or critiques?
- Are questions focused on single concepts or do they require cross-referencing multiple concepts?
- Does the evaluator test recall, comprehension, application, or analysis (Bloom's taxonomy)?

### 2.2 — What earns full marks?
- In the answer key, what distinguishes a complete answer from a partial one?
- Are authors/sources named in model answers?
- Is there a consistent structure (e.g., mechanism → example → consequence)?
- What vocabulary appears in top-scoring answers that is absent from lower-scoring ones?

### 2.3 — What loses points?
- Analyze the user's past graded work: where were points deducted?
- Is there a pattern to the deductions (too vague, wrong format, missing link, label without justification)?
- Distinguish between content errors (wrong information) and format errors (right information, wrong presentation).

### 2.4 — What does the evaluator value implicitly?
- Does the evaluator reward connections between topics even when not explicitly asked?
- Is there a preference for practical examples over abstract reasoning, or vice versa?
- Does the evaluator have a theoretical allegiance that colors what counts as a "good" answer?
- Is originality rewarded or is fidelity to the course material preferred?

### 2.5 — What are the constraints?
- Time available vs. number of questions → target pace per question
- Permitted materials (open book, closed book, calculator, etc.)
- Weighting of different sections → time allocation strategy

## Phase 3 — Build the Evaluator Profile

Synthesize the patterns into a concise profile structured as:

**Rewards**: What this evaluator gives points for (be specific).
**Penalizes**: What costs points (be specific).
**Format**: The structure of a top-scoring answer.
**Vocabulary**: Key terms that signal mastery to this evaluator.
**Implicit rules**: Unstated expectations revealed by the evidence.

If a domain-specific configuration skill is available, store this profile there for reuse.

## Phase 4 — Calibrate Responses

When helping the user draft or evaluate an answer:

1. **Check against the profile**: Does this answer contain what the evaluator rewards? Does it avoid what the evaluator penalizes?
2. **Check the format**: Does the answer match the structure of top-scoring answers from the answer key?
3. **Check the vocabulary**: Are the key theoretical terms present and correctly used?
4. **Check for implicit rules**: Does the answer demonstrate the unstated expectations (e.g., cross-references, practical anchoring, author names)?
5. **Provide specific feedback**: Not "this could be better" but "your mechanism is correct, but you labeled it without the 'because' — add one sentence explaining *why* this is an example of X rather than Y."

## Application Beyond Academia

This skill works identically for:
- **Job interviews**: The interviewer's questions reveal what they value; their reactions to your answers reveal their implicit criteria.
- **Client pitches**: Past RFPs and winning proposals reveal the client's revealed preferences.
- **Grant applications**: Funded proposals and reviewer comments reveal the committee's actual priorities.
- **Performance reviews**: Past feedback reveals what your manager actually measures vs. what the form says.

The procedure is the same: collect artifacts → identify patterns → build profile → calibrate output.

## Anti-Patterns

**The Sycophant**: Calibration is not about telling the evaluator what they want to hear. It's about presenting genuine understanding in the format most likely to be recognized as such.

**The Template Robot**: A calibrated format is a starting point, not a cage. If the content demands a different structure, deviate — but deviate knowingly.

**Over-indexing on a Single Artifact**: One graded exam is a data point, not a pattern. Look for convergence across multiple artifacts before building the profile.
