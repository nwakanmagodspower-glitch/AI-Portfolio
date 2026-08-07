# Cross-Platform Business Intelligence & Teaching Engine

## Purpose

Build one teaching-first intelligence system that discovers real business problems, verifies what systems and tools can realistically help, converts the result into a reusable **Master Insight**, and then creates platform-native educational content for Reddit, X, and LinkedIn.

The system is not a blind cross-poster. It diagnoses once, stores the shared intelligence once, then adapts the same lesson differently for each platform when the topic fits.

## Public Positioning

**Business Systems, AI & Automation Educator / Builder**

The public brand is about understanding business operations and explaining how better systems, AI, and automation can improve them. Tools are supporting evidence, not the identity.

## Core Architecture

```text
DISCOVERY / EVIDENCE
Reddit + X + LinkedIn-owned engagement + GitHub + Official Docs + Manual ideas
                               |
                               v
                     Source Intelligence
                               |
                               v
                 Cluster similar problems
                               |
                               v
                        Business Doctor
                               |
                               v
                        MASTER INSIGHT
           diagnosis + cause + lesson + evidence + diagram
                               |
                               v
                      Platform Fit Scoring
                    /          |           \
                 Reddit        X         LinkedIn
                    \          |           /
                     Platform-native drafts
                               |
                               v
                         Telegram Review
                               |
                               v
                    Controlled Publishing
                               |
                               v
                    Performance & Learning
                               |
                               v
                           Notion Memory
```

## Runtime Roles

- **GitHub** — permanent/versioned blueprint, prompts, rules, future workflow JSON, change history.
- **Notion** — live operating system and runtime memory.
- **n8n** — orchestrator.
- **OpenAI** — screening, diagnosis, research synthesis, Master Insight creation, platform adaptation, quality checks, diagram planning.
- **Telegram** — private approval and rewrite control centre.
- **Reddit** — strong founder/business-problem discovery source and permitted publishing destination.
- **X** — strong current-conversation discovery source and publishing destination.
- **LinkedIn** — professional publishing destination; owned posts/comments/engagement can become an intelligence source where authorized access allows.
- **GitHub + official product docs** — technical evidence sources used to verify capabilities, not primarily to discover ordinary founder pain.

## Runtime Notion Model

1. **System Knowledge** — rules, capabilities, platform strategy, tools, industries, source strategy.
2. **Source Intelligence** — individual discoveries/evidence items from Reddit, X, LinkedIn-owned engagement, GitHub, docs, or manual input.
3. **Master Insights** — one canonical diagnosis/lesson built from one or more source items.
4. **Platform Content** — separate Reddit/X/LinkedIn versions linked to one Master Insight.
5. **Performance & Learning** — time-based performance snapshots and lessons linked back to platform content.

## Cost Principle

Diagnose/research once when possible. Store the Master Insight. A later AI call can create all relevant platform variants in one structured response. Reuse existing Master Insights instead of paying to rediscover the same problem repeatedly.

## Publishing Principle

**Same intelligence does not mean identical copy.**

A topic may fit all three platforms or only one/two. Platform Fit scoring determines where it belongs. Each platform receives its own hook, length, structure, CTA/question style, and rule check.

## Safety / Trust Principle

Teach first. Diagnose before prescribing. Benefits before technology. No hard sell. No invented experience, statistics, case studies, savings, ROI, or guarantees. Human approval remains required before publishing during Version 1.

## Current Build Phase

The GitHub and Notion foundations are being migrated to this cross-platform architecture first. The n8n workflow will be restructured only after the data model and platform rules are stable.
