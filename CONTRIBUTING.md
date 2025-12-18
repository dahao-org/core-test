# Contributing to DAHAO Core

DAHAO Core evolves through its own governance process. This document explains how to participate.

---

## Ways to Contribute

### 1. Participate in Discussions

- Browse [GitHub Discussions](https://github.com/dahao-org/core-test/discussions)
- Comment on active proposals
- Raise concerns (antithesis)
- Help synthesize solutions

### 2. Propose Changes

Any contributor can propose changes to terms, principles, or rules.

### 3. Vote

Once proposals reach voting phase, cast your vote.

### 4. Create a Domain

Start a new DAHAO domain for your purpose area.

---

## The Proposal Process

### Step 1: Create Discussion

Create a new GitHub Discussion with this format:

**Title:**
```
[PROPOSAL] {action} @{term_name} (v{current} → v{proposed})
```

**Body:**
```markdown
## [THESIS]

### Summary
Brief description of the proposed change.

### Current State
What exists now (with version reference).

### Proposed Change
What you want to change.

### Evidence
- [Author (Year)] Title. Source. URL
- [Author (Year)] Title. Source. URL

### Alignment Check
- [ ] Serves core purpose
- [ ] No conflict with locked principles
- [ ] Evidence meets minimum requirements

### Justification
Why this change improves DAHAO.
```

### Step 2: Dialectic Discussion

Wait for community response:

- **[ANTITHESIS]** — Others raise concerns, questions, counter-arguments
- You must address substantive objections
- **[SYNTHESIS]** — Post refined proposal incorporating valid concerns

**Minimum discussion period:** 7 days for rules, 14 days for principles

### Step 3: Voting

After synthesis, request voting phase:

- Add `ready-for-vote` label
- Create poll or request PR reviews
- **Minimum voting period:** 3-7 days depending on type

### Step 4: Decision

- **If consensus met + quorum met:** Proposal accepted, merged with version bump
- **If consensus not met:** Proposal rejected with documented reasoning
- **If quorum not met:** Extended voting period or proposal expires

---

## Consensus Thresholds

| Change Type | Threshold |
|-------------|-----------|
| Add/modify term | 66% |
| Remove term | 85% |
| Add/modify rule | 75% |
| Remove rule | 90% |
| Add principle | 85% |
| Modify principle | 90% |
| Remove principle | 95% |
| Governance change | 90% |

**Protection Ratchet:** Removing protections requires threshold × 1.5

---

## Evidence Requirements

Proposals modifying factual claims require evidence:

| Tier | Type | Weight |
|------|------|--------|
| S | Peer-reviewed meta-analysis | 1.0 |
| A | Peer-reviewed primary research | 0.8 |
| B | Institutional reports | 0.6 |
| C | Expert opinion | 0.4 |
| D | Anecdotal | 0.1 |

**Minimum:** 1 source, Tier C or higher

---

## Locked Principles

These cannot be violated, even by proposals with high consensus:

- `@purpose_primacy`
- `@democratic_evolution`
- `@transparency`
- `@precautionary_default`
- `@protection_asymmetry`
- `@inheritance_integrity`

Unlocking requires 95% consensus through separate proposal.

---

## Creating a Domain

To create a new DAHAO domain:

1. Create new repository
2. Add `data/` folder with:
   - `terms.json`
   - `principles.json`
   - `rules.json`
   - `governance.json`

3. Declare inheritance in each file:
   ```json
   {
     "_meta": {
       "inherits": "dahao-org/core-test v1.0.0",
       "purpose": "Your domain purpose"
     }
   }
   ```

4. Add domain-specific content
5. Register in core's domain registry (optional but recommended)

See [dahao-org/animal-welfare](https://github.com/dahao-org/animal-welfare) as example.

---

## Code of Conduct

Per `@good_faith` principle:

- Assume charitable interpretation
- Disagree with arguments, not people
- Focus on purpose, not politics
- Provide evidence for claims
- Accept being wrong gracefully

---

## Questions?

- Open a Discussion with `[QUESTION]` tag
- Tag maintainers for urgent issues

---

*This document is itself governed by DAHAO rules. Propose changes through the standard process.*
