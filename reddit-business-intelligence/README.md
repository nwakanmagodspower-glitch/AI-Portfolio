# Reddit Business Intelligence & Teaching Engine

## Purpose

Build a teaching-first system that studies real founder and business problems on Reddit, diagnoses the underlying process issue, researches suitable tools and solutions, and turns that intelligence into simple educational content that builds trust.

The system is not designed to mass-market services or spam communities. It is designed to help readers understand their business problems, what kind of solution may help, what outcomes are possible, and what should remain human-controlled.

## Positioning

**Business Systems, AI & Automation Educator / Builder**

The public brand is about understanding business operations and explaining how better systems, AI, and automation can improve them. n8n is one tool in the toolbox, not the brand itself.

## Version 1 Architecture

```text
Reddit research
    ↓
n8n discovery + filtering
    ↓
OpenAI screening
    ↓
Business diagnosis
    ↓
Capability matching
    ↓
Tool / industry research
    ↓
Teaching content generator
    ↓
Diagram planner
    ↓
Quality + promotion-risk check
    ↓
Telegram approval
    ↓
Human-controlled publishing
    ↓
Performance tracking + memory
```

## Core Principle

Every post should leave the reader with at least one useful business insight even if they never become a client.

## Version 1 Boundaries

Automate:
- research and discovery
- deduplication
- problem diagnosis
- capability matching
- tool research
- educational drafting
- diagram planning
- storage
- Telegram approval cards

Keep human-controlled:
- Reddit profile posts
- subreddit posts
- comments and replies
- contact details
- promotional language
- claims about personal experience or results

## Project Documents

- `capability-profile.md` — what the AI may and may not claim
- `publishing-rules.md` — safety, quality, anti-spam, and approval rules
- `research-map.md` — initial communities, business problems, keywords/themes, and classification structure

## Planned n8n Modules

1. Reddit Research
2. Business Problem Analyzer
3. Tool & Solution Research
4. Content Generator
5. Diagram Planner
6. Telegram Approval
7. Reddit Publisher
8. Performance Collector

The system should be modular rather than one oversized workflow so each section can be tested and improved independently.
