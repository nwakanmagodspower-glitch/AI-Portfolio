# Runtime Data Model

## 1. System Knowledge

Purpose: live rules/configuration read by n8n and OpenAI.

Contains capabilities, platform rules, source strategy, tools, industries, prompts, configuration, and verification metadata.

## 2. Source Intelligence

One record per discovered source/evidence item.

Core fields:
- Source Item
- Source Platform
- Source Type
- Source URL
- Source Context
- Source Text
- Detected At
- Engagement Score
- Relevance Score
- Problem Category
- Cluster Key
- Evidence Quality
- Status
- linked Master Insight
- Notes

Source Platform values include Reddit, X, LinkedIn Owned, GitHub, Official Docs, and Manual.

## 3. Master Insights

One record per canonical business lesson/diagnosis.

Core fields:
- Insight / Insight ID
- Status
- Problem Category
- Industry
- Symptoms
- Diagnosis
- Root Cause
- Desired Outcome
- Master Lesson
- Master Explanation
- Relevant Capability
- Tools
- Evidence Summary / Evidence Status
- Opportunity Score
- Reddit Fit / X Fit / LinkedIn Fit
- Best Primary Platform
- Diagram Type / Diagram Brief
- Promotion Risk
- Source Count
- Reuse Count
- Last Adapted

A Master Insight may be supported by multiple source items and may generate multiple platform content records.

## 4. Platform Content

One record per platform-specific version.

Core fields:
- Content Version
- Platform
- Format
- linked Master Insight
- Platform Fit
- Hook / Title
- Draft
- Teaching Question
- Diagram Type / Diagram Brief
- Rule Check
- Promotion Risk
- Approval Status
- Published URL / Published At
- Telegram Message ID
- Version

One Master Insight can therefore have three different drafts without duplicating the underlying research.

## 5. Performance & Learning

One record per performance snapshot.

Core fields:
- Snapshot
- linked Platform Content
- Platform
- Snapshot At
- Views / Impressions
- Likes / Upvotes
- Comments / Replies
- Shares / Reposts
- Clicks
- Engagement Rate
- Learning Signal
- Next Action

This keeps platform performance separate from the Master Insight itself.

## Relationship Model

```text
Source Intelligence (many)
        |
        v
Master Insights (one canonical lesson)
        |
        v
Platform Content (many native versions)
        |
        v
Performance & Learning (many snapshots)
```

System Knowledge influences every stage but is not part of the content lineage itself.
