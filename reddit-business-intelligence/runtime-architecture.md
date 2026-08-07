# Runtime Architecture

## Architecture Decision

Version 1 uses **Notion instead of Google Sheets** as the live operational database.

- **GitHub** = permanent/versioned master blueprint and n8n workflow JSON.
- **Notion** = human manual + live runtime knowledge + content memory.
- **n8n** = orchestrator.
- **OpenAI** = screening, diagnosis, teaching draft, rewrite, diagram planning.
- **Telegram** = private approval/control centre.
- **Reddit** = research/distribution layer added after the core chain passes testing.

## Runtime Data Sources

### System Knowledge

- Notion database: `System Knowledge`
- Data source ID: `9fe295cd-2a1b-4079-8ce1-a96b614fd0cb`
- Purpose: live rules, capabilities, communities, tools, industries, prompts, and configuration.

Important runtime fields:

- `Name`
- `Type`
- `Status`
- `Priority`
- `Runtime Text`
- `Boundary / Notes`
- `Source URL`
- `Last Verified`

n8n should normally read only records where `Status = Active`, plus `Verify` tool records only when a tool-research step explicitly needs them.

### Content Intelligence

- Notion database: `Content Intelligence`
- Data source ID: `ec1117e5-22de-419e-843f-bc9bcd5a5df8`
- Purpose: live operational memory for every worthwhile founder problem/content opportunity.

Key fields:

- `Title`
- `Status`
- `Content Type`
- `Subreddit`
- `Reddit URL`
- `Industry`
- `Problem Category`
- `Symptom`
- `Diagnosis`
- `Underlying Cause`
- `Business Impact`
- `Relevant Capability`
- `Tools`
- `Opportunity Score`
- `Teaching Angle`
- `Draft Body`
- `Diagram Type`
- `Diagram Brief`
- `Promotion Risk`
- `Community Rule Check`
- `Telegram Message ID`
- `Published URL`
- `Views`
- `Upvotes`
- `Comments`
- `Detected At`
- `Published At`

## Runtime Flow

```text
Founder problem / Reddit discussion
            |
            v
           n8n
            |
            +---- read active System Knowledge from Notion
            |
            v
          OpenAI
            |
            +---- symptom
            +---- diagnosis
            +---- underlying cause
            +---- business impact
            +---- capability match
            +---- suitable tools (only if relevant)
            +---- opportunity score
            +---- content type
            +---- teaching angle
            +---- business-first draft
            +---- diagram type + brief
            +---- promotion-risk assessment
            |
            v
   Content Intelligence
            |
            v
         Telegram
            |
   Approve / Rewrite /
 Research More / Ignore
            |
            v
           n8n
            |
            v
   update Notion status
```

## Doctor Model

Every analysis should reason in this order:

1. Symptoms — what the founder is experiencing.
2. Diagnosis — the underlying process failure.
3. Cause — why it keeps happening.
4. Treatment — what process/system should change.
5. Tools — only after the process is understood.
6. Implementation journey — what would need to change inside the business, without unnecessary technical detail.
7. Outcome — what becomes easier, faster, clearer, or more reliable.
8. Limits — what still needs a human or more information.
9. Teaching question — only when it naturally improves discussion.

## Source-of-Truth Rule

GitHub is the **versioned master blueprint**.

Notion System Knowledge is the **runtime-readable configuration**.

Do not create continuous two-way synchronization. Configuration changes should flow deliberately:

```text
GitHub master
    |
manual/controlled sync
    v
Notion System Knowledge
    |
    v
n8n runtime
```

Content Intelligence flows the other direction only as operational data and does not need to be committed to GitHub.

## Security

Never store secrets in GitHub or Notion.

Secrets belong only in n8n Credentials/environment configuration:

- OpenAI API key
- Notion integration secret
- Telegram bot token
- Reddit credentials/tokens
- future third-party API keys

## Version 1 Safety and Quality Boundaries

- Human approval before every Reddit profile/community post or reply.
- No automated DMs.
- No vote/karma manipulation.
- No mass-posting similar content.
- No invented case studies, experience, statistics, ROI, savings, revenue, or tool capabilities.
- No guaranteed business outcomes.
- Community rules must be checked before community participation.
- Tool capabilities must be verified before a specific integration is presented as fact.

## First Milestone

The system is considered alive when this chain works reliably:

```text
Manual Sample Problem
        -> Notion System Knowledge
        -> OpenAI diagnosis/draft
        -> Notion Content Intelligence
        -> Telegram review message
```

Reddit ingestion and publishing are intentionally excluded until that core chain is stable.
