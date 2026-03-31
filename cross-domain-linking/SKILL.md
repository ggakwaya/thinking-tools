---
name: cross-domain-linking
description: "Systematically activate connections between concepts when one is solicited in isolation. Use this skill whenever the user is working within a corpus of interconnected ideas (a course, a field, a project, a strategic plan) and asks about one concept without referencing related ones. Also trigger when the user asks to 'make connections', 'see the big picture', 'link this to other topics', or is preparing for an evaluation that rewards cross-referencing. This skill prevents silo thinking by surfacing productive links that the user might not see."
---

# Cross-Domain Linking

## Core Principle

Knowledge organized in silos is knowledge half-used. Most complex questions — in academia, in business, in life — sit at the intersection of multiple domains. This skill ensures that when one concept is activated, related concepts are **checked for relevance**, not ignored by default.

The key discipline: a link must be **productive** (it enriches the analysis) not **decorative** (it shows off breadth without adding depth). Forcing connections is worse than missing them.

## Procedure

### Step 1 — Detect the trigger

A cross-domain link check is triggered when:
- The user asks about a specific concept within a known corpus
- The user is building an argument or analysis that could benefit from multiple perspectives
- The user is preparing for an evaluation that explicitly or implicitly rewards cross-referencing
- The response would be incomplete or misleading without acknowledging a related concept

### Step 2 — Consult the connection map

If a domain-specific configuration skill is available, load the connection map from there. This map specifies: "When concept X is activated, check whether concepts Y and Z are relevant."

If no map is available, generate candidate connections by asking:
- What *causes* or *enables* the phenomenon described by this concept?
- What *results from* or *is constrained by* this phenomenon?
- What other concept describes the *same phenomenon from a different angle*?
- What concept describes a *tension or contradiction* with this one?

### Step 3 — Evaluate relevance

For each candidate connection, apply the **productivity test**:

1. **Does it deepen the analysis?** If adding this link reveals something about the case that wasn't visible through the primary concept alone → productive.
2. **Does it answer an implicit question?** If the user's question naturally raises a follow-up that the linked concept addresses → productive.
3. **Does it merely show breadth?** If the link is technically correct but doesn't change the analysis → decorative. Skip it.

### Step 4 — Integrate, don't append

Productive links should be woven into the analysis, not listed as an afterthought.

**Wrong**: "This is an example of agency theory. It also relates to legitimacy theory."

**Right**: "The bureaucracy here results from the agency dynamic — the owner's fear of delegation drives surveillance costs beyond what the operation requires. But notice that this same surveillance also serves a legitimacy function: the paperwork signals to external stakeholders that the organization is 'well-managed,' even when the controls exist for internal reasons."

The link should feel like a *natural extension* of the reasoning, not a parenthetical reference.

### Step 5 — Signal the link to the user

When a cross-domain link materially changes the analysis, make it visible:
- In study contexts: "This is a point where the evaluator likely expects you to bridge to concept Y."
- In analytical contexts: "The interesting thing here is that this isn't just an X problem — it's also a Y problem, which changes the recommendation."
- In exploratory contexts: "This connects to something we discussed about Y — do you want to pull on that thread?"

## Calibration by Context

**Academic evaluation**: If the evaluator's profile (from evaluator-calibration skill) shows they reward cross-references, be more aggressive in surfacing links. If they penalize tangents, be more selective.

**Professional analysis**: Only surface links that change the recommendation or reveal a risk. Breadth for its own sake wastes the reader's time.

**Learning/exploration**: Surface more links, including speculative ones, and let the user decide which to pursue.

## Building a Connection Map

If working within a corpus that doesn't yet have a connection map, build one incrementally:

1. List all major concepts/frameworks in the corpus
2. For each pair, ask: "Does understanding A change how you apply B?"
3. If yes, record the link with a brief note on *how* they interact
4. Organize as a lookup table: "If the question is about A → check B and C"

Store the map in the domain-specific configuration skill for reuse.

## Anti-Patterns

**The Web of Everything**: Connecting every concept to every other concept. If everything is connected, nothing is highlighted. Limit to 1-2 productive links per analysis unless the question explicitly asks for a comprehensive mapping.

**The Name-Drop Chain**: Listing authors and theories in sequence without explaining *how* they interact. "This relates to Goffman, which connects to Suchman, which links to DiMaggio and Powell" is not a cross-domain link — it's a bibliography.

**The Forced Bridge**: Connecting two concepts because they're in the same corpus, not because they illuminate each other in this specific case. If the link doesn't change the analysis, leave it out.
