# thinking-tools

Skills that teach Claude *how to think*, not *what to know*.

## The problem

Large language models default to encyclopedic mode: ask about a theory, get a description of the theory. But in most real-world contexts: exams, consulting, analysis, decision-making, describing a framework is worthless. What matters is using it to *see something you couldn't see without it*.

These skills encode transferable intellectual competencies as reusable instructions for Claude. They are domain-agnostic: the same skills work whether you're analyzing a small business, preparing for a law exam, or evaluating a grant proposal. The domain-specific content is loaded separately as a configuration file.

## Architecture

```
thinking-tools/
├── analytical-framework/
│   └── SKILL.md
├── evaluator-calibration/
│   └── SKILL.md
├── cross-domain-linking/
│   └── SKILL.md
└── README.md
```

**Three generic skills. One configuration pattern.**

The skills define *how* to think. A separate domain-specific configuration skill (not included here, you build your own) provides *what* to think with: the frameworks, the evaluator profile, the connection map.

## The skills

### analytical-framework

Applies theoretical frameworks as diagnostic instruments rather than definitions to recite.

**Without this skill**, Claude says: "Agency theory, developed by Jensen and Meckling, proposes that..."

**With this skill**, Claude says: "The bureaucracy here isn't driven by operational needs, it's the principal-agent dynamic. The owner's fear of delegation inflates surveillance costs beyond what the situation requires."

The procedure: identify which framework the question activates → formulate the diagnostic question it answers → apply to the case (mechanism → nuance → consequence) → never describe the lens, describe what you see through it.

### evaluator-calibration

Decodes an evaluator's implicit expectations from their artifacts (past exams, answer keys, grading patterns, verbal instructions) and calibrates responses to match.

Every evaluator has a *revealed* preference structure that may differ from their *stated* one. This skill closes the gap by building a profile across five dimensions: what is tested, what earns full marks, what loses points, what is valued implicitly, and what the constraints are.

Works for professors, interviewers, clients, grant reviewers, or anyone whose approval you need to earn through a structured output.

### cross-domain-linking

Prevents silo thinking by systematically checking for productive connections when a single concept is solicited.

The key discipline: a link must be **productive** (it enriches the analysis) not **decorative** (it shows off breadth). The skill consults a connection map, evaluates whether each candidate link actually changes the analysis, and integrates relevant links as natural extensions of the reasoning, not as afterthoughts.

## Usage

### With Claude Projects

Add the skill files to a Claude Project as project knowledge. Claude will consult them when relevant.

### With a domain configuration

The skills are designed to consume a fourth, domain-specific file that you create for your context. This configuration provides:

1. **The frameworks** — the diagnostic tools relevant to your domain, with their questions, authors, and expected mechanisms
2. **The evaluator profile** — what your specific evaluator rewards, penalizes, and expects
3. **The connection map** — which concepts link to which, and how

Example structure with a domain configuration:

```
your-project/
├── thinking-tools/          ← this repo (generic)
│   ├── analytical-framework/
│   ├── evaluator-calibration/
│   └── cross-domain-linking/
└── configs/                 ← your domain configs (specific)
    ├── corporate-finance-401/
    │   └── SKILL.md
    ├── client-pitch-acme/
    │   └── SKILL.md
    └── bar-exam-prep/
        └── SKILL.md
```

The generic skills stay the same. The configuration changes per context. Swap the config, keep the competencies.

## Design principles

**Skills encode procedures, not content.** A skill tells Claude *how to reason* in a type of situation. Content belongs in the domain configuration or in the conversation context.

**The productivity test governs everything.** Whether it's a cross-domain link, a theoretical reference, or an example: if it doesn't change the analysis, leave it out.

**Anti-patterns are as important as patterns.** Each skill explicitly names what *not* to do. The Encyclopedia Entry, the Label Without the Because, the Web of Everything, the Forced Bridge, these failure modes are common enough to warrant explicit prevention.

**Transferability over specificity.** These skills should work for a first-year undergraduate and a senior consultant. The depth of application changes; the procedure doesn't.

## Origin

These skills emerged from a concrete project: preparing for a university course in SME management. The course presented seven organizational theories as a diagnostic toolkit for consultants, but framed them as academic content. Reframing the theories as *tools*, and extracting the underlying intellectual competencies from the domain-specific content, produced skills that turned out to be useful far beyond that one course.

The domain-specific configuration for that original course is not included here, but its structure serves as the reference implementation for the configuration pattern.

## License
MIT
