# DAHAO Core

**Decentralized Autonomous Harmonized Axiomatic Ontology**

The universal governance framework for purpose-driven communities.

---

## What is DAHAO Core?

DAHAO Core is the "operating system" for collaborative value evolution. It provides:

- **Universal vocabulary** for governance (proposals, consensus, evidence)
- **Locked principles** that all domains must inherit
- **Rules** for how communities evolve their values
- **Self-modifying governance** — the rules for changing rules

DAHAO Core is **domain-agnostic**. It doesn't define what's ethical — it defines how communities can collaboratively determine what's ethical for their domain.

---

## Architecture

```
DAHAO CORE (This Repo)
│
├── Universal terms: @purpose, @proposal, @consensus, @evidence
├── Locked principles: @democratic_evolution, @transparency
├── Governance rules: How to propose, discuss, vote, merge
│
└── DOMAINS INHERIT THIS:
    ├── Animal Welfare (dahao-org/animal-welfare)
    ├── AI Ethics (future)
    ├── Climate Justice (future)
    └── [Any purpose-driven community]
```

---

## Core Components

### Terms (`data/terms.json`)
Universal vocabulary that all domains share:
- `@purpose` — What a DAHAO exists to achieve
- `@stakeholder` — Who is affected by decisions
- `@proposal` — How changes are suggested
- `@consensus` — How agreement is measured
- `@evidence` — How claims are supported

### Principles (`data/principles.json`)
Locked values that cannot be violated:
- `@purpose_primacy` — Decisions must serve stated purpose
- `@democratic_evolution` — Community decides, not individuals
- `@transparency` — All reasoning is public
- `@precautionary_default` — When uncertain, protect

### Rules (`data/rules.json`)
Governance procedures:
- `@rule_proposal_process` — Discussion → Vote → Merge
- `@rule_consensus_threshold` — Different thresholds for different changes
- `@rule_protection_ratchet` — Harder to remove protection than add

---

## Creating a Domain

To create a new DAHAO domain:

1. Create new repository
2. Declare inheritance from core:
   ```json
   {
     "_meta": {
       "inherits": "dahao-org/core-test v1.0.0",
       "purpose": "Your domain's purpose statement"
     }
   }
   ```
3. Add domain-specific terms, principles, rules
4. Domain automatically inherits core's locked principles

See [dahao-org/animal-welfare](https://github.com/dahao-org/animal-welfare) as reference implementation.

---

## Self-Evolution

DAHAO Core evolves through its own rules:

1. **Propose** — Create GitHub Discussion with change
2. **Discuss** — Dialectic process (thesis → antithesis → synthesis)
3. **Vote** — Community consensus required
4. **Merge** — Versioned change with full history

Even governance rules can change — by following governance rules.

---

## Version

**Current Version**: v1.0.0

Versioning follows semantic versioning:
- MAJOR: Breaking changes (removed terms, weakened principles)
- MINOR: Additions (new terms, new rules)
- PATCH: Clarifications (typos, better wording)

---

## License

CC BY-SA 4.0 — Share and adapt with attribution.

---

## Links

- **Whitepaper**: [DAHAO: A Living Framework for Collaborative Ethical Evolution](./WHITEPAPER.md)
- **Animal Welfare Domain**: [github.com/dahao-org/animal-welfare](https://github.com/dahao-org/animal-welfare)
- **Discussions**: [GitHub Discussions](https://github.com/dahao-org/core-test/discussions)
