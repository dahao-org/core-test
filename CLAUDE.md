# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

DAHAO Core is a decentralized governance framework - the "operating system" for collaborative value evolution. This repository contains **data files** (JSON) that define universal vocabulary, principles, and rules that domain-specific communities inherit.

## Repository Structure

This is a data/documentation repository, not a code project. There are no build commands, tests, or linting.

```
dahao/
├── data/
│   ├── terms.json      # Universal vocabulary (@purpose, @stakeholder, @proposal, etc.)
│   ├── principles.json # Locked values (@purpose_primacy, @democratic_evolution, etc.)
│   ├── rules.json      # Governance procedures
│   └── governance.json # Meta-governance rules
├── README.md           # Project overview
├── CONTRIBUTING.md     # Proposal process documentation
└── LICENSE             # CC BY-SA 4.0
```

## Key Concepts

- **Terms** (`@term_name`): Universal vocabulary shared across all domains
- **Principles**: Locked values that cannot be violated (unlocking requires 95% consensus)
- **Rules**: Governance procedures for proposals, voting, and changes
- **Domains**: Child repositories that inherit from core (e.g., dahao-org/animal-welfare)

## Locked Principles

These cannot be violated even by high-consensus proposals:
- `@purpose_primacy`
- `@democratic_evolution`
- `@transparency`
- `@precautionary_default`
- `@protection_asymmetry`
- `@inheritance_integrity`

## Inheritance Model

Domains declare inheritance via `_meta` block:
```json
{
  "_meta": {
    "inherits": "dahao-org/core-test v1.0.0",
    "purpose": "Domain purpose statement"
  }
}
```

## Versioning

Follows semantic versioning:
- MAJOR: Breaking changes (removed terms, weakened principles)
- MINOR: Additions (new terms, new rules)
- PATCH: Clarifications

## Change Process

Changes follow the dialectic proposal process (see CONTRIBUTING.md):
1. Create Discussion with `[PROPOSAL]` format
2. Wait for `[ANTITHESIS]` responses
3. Post `[SYNTHESIS]` incorporating valid concerns
4. Voting phase (thresholds vary by change type: 66%-95%)
5. Merge with version bump

## License

CC BY-SA 4.0 - Share and adapt with attribution.
