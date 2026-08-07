# Reddit Business Intelligence & Teaching Engine

## Purpose

Build a teaching-first system that studies real founder and business problems on Reddit, diagnoses the underlying process issue, researches suitable tools and solutions, and turns that intelligence into simple educational content that builds trust.

The system is not designed to mass-market services or spam communities. It is designed to help readers understand their business problems, what kind of solution may help, what outcomes are possible, and what should remain human-controlled.

## Positioning

**Business Systems, AI & Automation Educator / Builder**

The public brand is about understanding business operations and explaining how better systems, AI, and automation can improve them. n8n is one tool in the toolbox, not the brand itself.

## Live Version 1 Architecture

```text
GitHub
Permanent/versioned blueprint + workflow JSON
        |
        | occasional configuration sync
        v
Notion
System Knowledge + Content Intelligence
        ^                         |
        |                         v
Reddit -> n8n -> OpenAI -> Notion -> Telegram
                   |                  |
                   +---- teaching ----+
                                      |
                              human approval
                                      |
                              controlled publish
```

### Roles

- **GitHub** — master versioned blueprint, rules, prompts, workflow JSON, and backups.
- **Notion** — human-readable project manual and live runtime database.
- **n8n** — orchestrator that reads knowledge, calls AI, stores results, and sends approval requests.
- **OpenAI** — screening, business diagnosis, structured reasoning, teaching drafts, rewrite requests, and diagram planning.
- **Telegram** — private approval centre: Approve, Rewrite, Research More, Ignore.
- **Reddit** — research/distribution layer added after the core chain is proven.

Google Sheets is intentionally excluded from Version 1 to keep the self-hosted setup simpler.

## Runtime Notion Databases

### System Knowledge

Live configuration that n8n/OpenAI can read.

- Database: `System Knowledge`
- Data source ID: `9fe295cd-2a1b-4079-8ce1-a96b614fd0cb`
- Contains: capabilities, rules, communities, tools, industries, prompts, and configuration.

### Content Intelligence

Live operational memory for problems, diagnoses, drafts, approvals, publication state, and later performance.

- Database: `Content Intelligence`
- Data source ID: `ec1117e5-22de-419e-843f-bc9bcd5a5df8`
- Contains: symptom, diagnosis, cause, impact, capability match, tools, score, teaching angle, draft, diagram brief, promotion risk, rule check, approval status, publishing status, and performance.

## Core Principle

Every post should leave the reader with at least one useful business insight even if they never become a client.

**Teach first. Diagnose before prescribing. Benefits before technology. No hard sell.**

## Doctor Teaching Model

Every useful post or reply should reason through:

1. Symptoms
2. Diagnosis
3. Cause
4. Treatment / better process
5. Relevant tools
6. Implementation journey
7. Business outcome
8. Limits / what should remain human
9. Teaching question when it naturally improves discussion

## Version 1 Build Order

1. Manual/sample founder problem.
2. Read active System Knowledge from Notion.
3. Build a compact runtime context.
4. Send the problem + context to OpenAI.
5. Require structured business-first analysis.
6. Store the result in Content Intelligence.
7. Send a Telegram review card.
8. Human chooses Approve / Rewrite / Research More / Ignore.
9. Update the Notion record.
10. Add Reddit ingestion only after the core brain/memory/control chain is stable.
11. Add publishing only after Reddit access and community-rule checks are confirmed.

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

Never:
- mass-post similar content
- automatically DM strangers
- automate voting/karma
- use multiple accounts to amplify content
- invent experience, clients, case studies, statistics, savings, revenue, or tool capabilities
- guarantee sales, ROI, growth, profit, or cost savings

## Project Files

- `capability-profile.md` — what the AI may and may not claim
- `publishing-rules.md` — quality, anti-spam, and approval rules
- `research-map.md` — initial communities, problems, themes, and classifications
- `runtime-architecture.md` — GitHub/Notion/n8n/OpenAI/Telegram responsibilities and data flow
- `workflows/README.md` — n8n import and credential setup
- `workflows/01-core-brain-test.json` — first importable workflow skeleton

## Security

Never commit secrets.

The following stay only inside n8n Credentials or environment configuration:
- OpenAI API key
- Notion integration secret
- Telegram bot token
- Reddit credentials/tokens
- any future API secrets

## Planned Modules

1. Core Brain Test
2. Telegram Approval Handler
3. Reddit Research
4. Business Problem Analyzer
5. Tool & Solution Research
6. Content Generator
7. Diagram Planner
8. Reddit Publisher
9. Performance Collector

The system is intentionally modular rather than one oversized workflow so each part can be tested and improved independently.
