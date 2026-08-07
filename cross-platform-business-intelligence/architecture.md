# Architecture Blueprint

## One problem, one Master Insight, many native outputs

The system separates **intelligence creation** from **content distribution**.

### Stage 1 — Discovery

Possible sources:
- Reddit discussions and comments
- X posts/conversations
- LinkedIn comments/replies on authorized owned content
- GitHub issues/repositories when technical evidence matters
- Official product/API documentation
- Manual ideas entered by the operator

Every discovered item becomes a `Source Intelligence` record.

### Stage 2 — Screening and clustering

The system scores relevance and groups similar items. Five different people complaining about missed follow-ups should not automatically create five separate topics. They can strengthen one recurring problem cluster.

### Stage 3 — Business Doctor

The Business Doctor creates a canonical diagnosis:

Symptoms -> Diagnosis -> Root Cause -> Desired Outcome -> Better Process -> Relevant Tools -> Business Outcome -> Limits.

### Stage 4 — Master Insight

A Master Insight is the reusable intellectual asset. It stores:
- the underlying problem
- evidence/source summary
- diagnosis
- root cause
- desired outcome
- master lesson
- master explanation
- capability match
- relevant tools
- cautions
- diagram concept
- opportunity score
- platform-fit scores

The Master Insight should make sense even if no social platform existed.

### Stage 5 — Platform Fit

Each Master Insight receives scores for Reddit, X, and LinkedIn. A weak fit is skipped instead of forced.

Example:

```text
Topic: Why leads disappear after enquiry
Reddit fit:   94
X fit:        84
LinkedIn fit: 92
Decision: adapt for all three
```

Another example:

```text
Topic: Why a specific subreddit removes a certain promotion style
Reddit fit:   96
X fit:        25
LinkedIn fit: 18
Decision: Reddit only
```

### Stage 6 — Platform Adaptation

The same Master Insight can produce separate content records:
- Reddit: deeper, conversational, community-aware
- X: compressed insight or short thread
- LinkedIn: professional operating lesson, clear structure, strong business framing

The system may generate all relevant variants in one structured AI call to reduce cost.

### Stage 7 — Telegram Review

Telegram shows one Master Insight plus its proposed platform versions. The operator can approve individually rather than approving an all-or-nothing cross-post.

Suggested actions:
- Approve All
- Approve Reddit
- Approve X
- Approve LinkedIn
- Rewrite
- Research More
- Ignore

### Stage 8 — Controlled publishing

Only approved platform versions are published. Platform-specific policy/rule checks are applied before the write action.

### Stage 9 — Performance and learning

Performance is stored by platform version, not only by topic. This allows the system to learn that the same business lesson may perform differently on Reddit, X, and LinkedIn.

### Stage 10 — Compounding memory

When similar source items appear later, n8n checks whether a Master Insight already exists. If it does, the system can update/reuse it instead of paying to research and diagnose from zero.
