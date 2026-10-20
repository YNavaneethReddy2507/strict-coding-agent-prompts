# Strict Coding-Agent Prompts

A reusable Antigravity skill and prompting framework for authoring and executing deterministic, high-discipline coding-agent prompts.

## Overview

Coding agents frequently experience drift, perform silent modifications to unrelated files, hallucinate test verifications, or engage in runaway implementation across multiple unapproved phases.

The **Strict Coding-Agent Prompts** skill solves this by enforcing 9 core structural pillars:

1. **Files Allowlist**: Precise file and directory boundaries; zero edits permitted outside the allowlist.
2. **Verify First**: Baseline environment inspection (root, Git branch, HEAD, working tree) prior to any mutations.
3. **Pre-Checks**: Falsifiable hypotheses verified before proceeding; immediate stop-and-report if any condition fails.
4. **Minimal Targeted Implementation**: Strict scope containment without speculative scaffolding or unrequested boilerplate.
5. **"Do Not Touch" Guardrails**: Explicit negative constraints protecting existing code, tests, and configuration.
6. **Acceptance Checklist**: Concrete pass/fail criteria verified empirically.
7. **Commit Requirements**: Explicit version control instructions, staging boundaries, and commit message formats.
8. **Empirical Evidence Report**: Structured table containing executed commands and verbatim terminal output.
9. **Explicit Stop Conditions**: Hard execution termination preventing autonomous progression into subsequent milestones.

## Skill Installation

To use this skill in your Antigravity workspace, clone or copy the `.agent` directory into your project root:

```bash
git clone https://github.com/YNavaneethReddy2507/strict-coding-agent-prompts.git
cp -r strict-coding-agent-prompts/.agent /path/to/your/project/
```

Antigravity will automatically discover the skill under:
```text
.agent/skills/strict-coding-agent-prompts/SKILL.md
```

## Structure

```text
.
├── README.md
└── .agent/
    └── skills/
        └── strict-coding-agent-prompts/
            └── SKILL.md
```

## License

MIT
