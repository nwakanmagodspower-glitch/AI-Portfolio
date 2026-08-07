# User Experience — What the System Feels Like to Use

This document describes the system from the operator's point of view, not from the node/API point of view.

## 1. The system wakes up and looks for useful business problems

You do not open Reddit, X, LinkedIn, GitHub, and product documentation one by one.

The system collects permitted intelligence from its enabled sources:

- Reddit discussions
- X conversations
- LinkedIn engagement on content/accounts we are authorized to read
- GitHub issues/repositories when technical evidence is useful
- official product documentation when capabilities need verification
- manual ideas/questions entered by you

Each raw item becomes a **Source Intelligence** record in Notion.

At this stage the system is not writing a social-media post yet. It is asking: `Is there a real business problem or useful signal here?`

## 2. Similar discoveries are grouped together

Suppose the system finds:

- Reddit: `My reps forget to follow up leads.`
- X: `Our CRM is full but nobody knows what to do next.`
- another Reddit discussion: `Leads disappear after the first call.`

These should not become three unrelated posts.

The system sees that they point to the same pattern and creates one cluster:

`Lead follow-up depends on memory instead of a reliable next-action process.`

This reduces noise and API cost.

## 3. The Business Doctor creates one Master Insight

The system then creates the reusable intelligence object called a **Master Insight**.

Example:

- Symptoms: leads disappear after enquiry.
- Diagnosis: there is no dependable next-action process.
- Root cause: follow-up depends on individual memory and disconnected tools.
- Desired outcome: every lead has an owner, status and next action.
- Master lesson: `More leads do not fix broken follow-up.`
- Relevant capability: lead follow-up / CRM workflow design.
- Potential tools: CRM + automation + reminders, only if verified.
- Diagram brief: `Lead -> Owner -> Next Action -> Reminder -> Outcome`.

The Master Insight is stored in Notion and can be reused forever unless the facts become outdated.

## 4. Research is requested only when needed

The system does not research every topic deeply by default.

If the Master Insight makes a claim such as `HubSpot + Calendly + n8n can support this journey`, the research layer verifies the capability using official documentation first and GitHub evidence where useful.

The Master Insight then receives an evidence state such as:

- Verified
- Needs Research
- Mixed
- Blocked

A weak or unverified claim does not move directly to publishing.

## 5. The system decides where the idea belongs

The same lesson is scored independently for each platform.

Example:

- Reddit Fit: 94/100
- X Fit: 82/100
- LinkedIn Fit: 91/100
- Best Primary Platform: Multi-platform

Another topic may be:

- Reddit Fit: 95
- X Fit: 48
- LinkedIn Fit: 30

That topic should remain Reddit-only.

You are never forced to publish a topic everywhere.

## 6. One Master Insight is split into native platform versions

For every platform that passes the fit threshold, the system creates a separate **Platform Content** record.

### Reddit version

Feels like participation in a real discussion:

- more context
- conversational explanation
- direct diagnosis of the founder's problem
- practical process change
- community-sensitive language
- useful question when appropriate

### X version

Feels native to X:

- strong first line
- compressed lesson
- one main idea
- short post or mini-thread only if needed
- fast, clear language

### LinkedIn version

Feels professional:

- business/operations framing
- implications for teams, managers and customers
- structured paragraphs
- stronger authority/teaching tone
- diagram/document style can be used when helpful

The underlying lesson is shared, but the wording and structure are different.

## 7. You receive one Telegram approval package

Instead of three unrelated notifications, Telegram should present the topic as one content package.

Example:

```text
MASTER INSIGHT #47
More leads do not fix broken follow-up.

Evidence: VERIFIED
Opportunity: 91/100

PLATFORM FIT
Reddit   94/100   READY
X        82/100   READY
LinkedIn 91/100   READY

[VIEW REDDIT]
[VIEW X]
[VIEW LINKEDIN]
[APPROVE ALL]
[REWRITE]
[RESEARCH MORE]
[IGNORE]
```

You can approve all or approve only selected platform versions.

For example:

- Approve Reddit
- Rewrite LinkedIn
- Skip X

The Master Insight remains the same; only the platform expression changes.

## 8. Publishing happens through platform-specific gates

Approved content is sent only through the platform connector that is permitted and configured.

Before publishing, the system checks:

- platform permissions
- community/page/account rules where applicable
- promotional risk
- duplicate/repetitive content
- required human approval

Version 1 keeps publishing human-controlled through Telegram approval.

## 9. Performance comes back into Notion

After publishing, each platform version gets its own performance record.

The system can learn things such as:

- LinkedIn audiences respond strongly to client-onboarding diagrams.
- Reddit responds better to specific problem breakdowns than broad AI posts.
- X performs better when the insight is compressed into one strong sentence.

This does not change the truth of the Master Insight. It changes future packaging and topic priority.

## 10. Published engagement can create new topics

A comment under one of your own LinkedIn posts might ask:

`What if our CRM already has reminders but the sales team ignores them?`

That comment becomes a new Source Intelligence record.

The system may then create another Master Insight:

`A reminder system cannot fix unclear ownership or weak sales-process discipline.`

This creates a compounding teaching loop.

## The Operator Experience in One Sentence

You mainly interact with **Telegram for decisions** and **Notion for visibility**; n8n, OpenAI and the platform APIs do the background work, while GitHub preserves the permanent system blueprint.
