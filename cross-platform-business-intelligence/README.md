# Cross-Platform Business Intelligence & Teaching Engine

## Purpose

Build one teaching-first intelligence system that discovers real business problems, verifies what systems and tools can realistically help, converts the result into a reusable **Master Insight**, and then creates platform-native educational content for Reddit, X, and LinkedIn.

This is **not a blind cross-poster**. The system understands a business problem once, stores the shared intelligence once, then decides where the topic belongs and adapts it to each platform's audience and behavior.

## Public Positioning

**Business Systems, AI & Automation Educator / Builder**

The public brand is about understanding business operations and explaining how better systems, AI, and automation can improve them. Tools support the lesson; tools are not the identity.

## Canonical Topic Lineage

```text
DISCOVERY SOURCES
Reddit + X + LinkedIn-owned engagement + Manual ideas
                     |
                     v
              Source Intelligence
                     |
       cluster similar evidence/items
                     |
                     v
                Business Doctor
                     |
                     v
                MASTER INSIGHT
 diagnosis + root cause + lesson + evidence + outcome
                     |
                     +----> GitHub / Official Docs verification
                     |
                     v
              Platform Fit Scoring
              /        |         \
          Reddit       X       LinkedIn
            fit       fit        fit
              \        |         /
               Platform Adapter
              /        |         \
        Reddit draft  X draft  LinkedIn draft
              \        |         /
               Telegram Review
                     |
             controlled publishing
                     |
             Performance & Learning
                     |
                 Notion Memory
```

## The Core Rule

**Source is not destination.**

A problem discovered on Reddit can become a LinkedIn post, an X post, a Reddit reply, or all three. Likewise, an X conversation can become a LinkedIn lesson. What matters is the underlying business lesson and each platform's fit score.

## Five Runtime Objects

1. **System Knowledge** — rules, capabilities, platform behavior, tool knowledge, industries, search strategy and prompts.
2. **Source Intelligence** — individual posts, comments, discussions, issues, docs or manual observations. This is evidence, not yet content.
3. **Master Insights** — the canonical diagnosis/lesson. Similar sources can point to the same Master Insight.
4. **Platform Content** — separate Reddit, X and LinkedIn expressions of one Master Insight.
5. **Performance & Learning** — what happened after publishing and what should influence future topic selection/adaptation.

## Source Roles

- **Reddit** — high-value founder/operator problem discovery; community replies and permitted educational publishing.
- **X** — current public conversation discovery and fast insight distribution.
- **LinkedIn** — professional authority/distribution. Authorized engagement on our own posts/pages can later feed new Source Intelligence.
- **GitHub** — technical evidence: repositories, issues, implementation patterns and integration evidence where relevant.
- **Official documentation** — highest-priority source for verifying current product/API capabilities.
- **Manual input** — user ideas, client questions, observations and topics can enter the same pipeline.

## Master Insight Model

A Master Insight contains the reusable intelligence, for example:

- Symptom: leads disappear after enquiry.
- Diagnosis: follow-up depends on memory instead of a visible next-action process.
- Root cause: no reliable ownership/state/reminder system.
- Desired outcome: every lead has an owner and next action.
- Master lesson: **more leads do not solve broken follow-up.**
- Evidence: original discussions + verified product capabilities.
- Relevant systems/tools: only when verified and genuinely useful.
- Diagram: Lead -> Owner -> Next Action -> Reminder -> Outcome.

The system should reuse this Master Insight instead of paying OpenAI to rediscover it every time.

## Platform Fit

Each Master Insight gets three independent scores from 0-100:

- Reddit Fit
- X Fit
- LinkedIn Fit

Default guidance:
- 80-100 = strong native fit
- 60-79 = publish only if adaptation is genuinely useful
- below 60 = normally skip

No platform is mandatory. A topic can go to one, two, all three, or none.

## Native Adaptation

**Same intelligence does not mean identical copy.**

- Reddit: conversational, context-rich, helpful, community-sensitive.
- X: compressed, sharp, one main insight; thread only if needed.
- LinkedIn: professional operations framing, management/business outcomes, structured authority content.

The Platform Adapter should normally generate all qualifying variants in one structured AI call to control API cost.

## Runtime Roles

- **GitHub** — permanent/versioned blueprint, prompts, rules, future workflow JSON, change history.
- **Notion** — live operating system and runtime memory.
- **n8n** — orchestrator.
- **OpenAI** — screening, diagnosis, research synthesis, Master Insight creation, platform-fit scoring, adaptation, quality checks and diagram planning.
- **Telegram** — private approval/rewrite/research/ignore control centre.

## Cost Principle

1. Cheap screening before deep reasoning where possible.
2. Cluster duplicates/similar problems.
3. Research and diagnose once.
4. Store the Master Insight.
5. Verify tool claims only when required.
6. Generate relevant Reddit/X/LinkedIn variants in one structured adaptation call.
7. Reuse the stored Master Insight for future rewrites, new platforms or follow-up content.

## Publishing Principle

Human approval remains required in Version 1. The system does not mass-post, mass-DM, manipulate engagement, invent experience, or force every topic onto every platform.

**Teach first. Diagnose before prescribing. Benefits before technology. No hard sell.**

## Current Build Phase

GitHub and Notion are the canonical architecture now. The next engineering step is restructuring the existing n8n production workflow around the five runtime objects above while preserving the credentials and infrastructure already being connected.
