# Initial Reddit Communities & Research Map

## Objective

Use Reddit as a source of real founder and business problems. The system should search for operational pain, diagnose the underlying process, and decide whether the best output is an educational profile post, a helpful community reply, a private opportunity alert, more research, or no action.

The goal is not to search only for people asking for “n8n.” The goal is to find problems that better systems, automation, AI, CRM discipline, scheduling, support tooling, or process redesign could solve.

## Tier 1 Communities

### r/smallbusiness
Audience: owners and operators.

Watch for:
- missed leads
- CRM confusion
- customer support workload
- appointments and reminders
- repetitive admin
- reporting
- scattered information
- manual customer follow-up

Best contribution style: specific, practical, non-promotional teaching.

### r/Entrepreneur
Audience: entrepreneurs and founders.

Watch for:
- sales-process bottlenecks
- operational inefficiency
- software/tool overload
- customer acquisition workflows
- delegation and team handoffs
- repetitive work
- business systems questions

Best contribution style: explain the business problem and possible operating model without turning the answer into a pitch.

### r/startups
Audience: startup founders and early teams.

Watch for:
- early operating systems
- customer onboarding
- support processes
- lead handling
- founder time bottlenecks
- reporting and internal coordination
- manual processes that stop scaling

### r/SaaS
Audience: SaaS founders/operators.

Watch for:
- trials and onboarding
- customer support
- lead qualification
- churn-related processes
- customer success handoffs
- reporting
- repetitive account administration

### r/agency
Audience: agency owners and teams.

Watch for:
- client onboarding
- contracts/forms/document collection
- project handoffs
- client communication
- reporting
- lead follow-up
- repetitive setup work

## Tier 2 Specialist Intelligence

### r/n8n
Use primarily as a technical-intelligence source: integration patterns, common workflow problems, what users are attempting, and what breaks. Do not let this community define the public brand.

### r/automation
Use for automation patterns, workflow ideas, operational use cases, and recurring pain points.

### r/sales
Use for lead routing, CRM discipline, follow-up, pipeline management, sales handoffs, and repetitive sales administration.

## Expansion Rule

Do not permanently add a new subreddit to the automated research list until the workflow stores:

- subreddit name
- audience
- relevant business problems
- promotion risk
- current posting/reply rules
- date rules were last checked
- whether the community is active enough to justify monitoring

Potential future categories include customer success, operations, consulting, e-commerce operations, CRM-specific communities, support/helpdesk communities, and software-specific communities.

## Search Themes

The research engine should look beyond exact keywords and understand intent around phrases such as:

- takes too much time
- doing this manually
- keep forgetting
- missed follow-up
- losing leads
- too many tools
- copying data
- customer support overload
- onboarding is messy
- CRM is not updated
- how do you track
- how do you automate
- what tools do you use
- bottleneck
- repetitive
- spreadsheet
- handoff
- reminder
- appointment
- reporting
- data entry
- follow up
- customer questions
- team is overwhelmed
- process breaks
- information is scattered

## Problem Classification

Every useful discussion should be classified into one primary category and optional secondary categories:

- Sales / Leads
- Customer Support
- Client Onboarding
- Internal Operations
- Scheduling
- CRM
- Reporting
- Data Entry
- Team Handoffs
- Document Collection
- Notifications
- Customer Communication
- Knowledge Management
- Project Setup
- AI Opportunity
- Automation Opportunity

## Research Decision Logic

```text
Reddit discussion
      ↓
Is there a real business problem?
      ↓
No → Ignore / archive
Yes
      ↓
What is the underlying process failure?
      ↓
Does it match the capability profile?
      ↓
No → Research only / archive
Yes
      ↓
Is this a recurring problem useful to many businesses?
      ↓
Yes → Profile teaching post candidate
      ↓
Is the original poster asking for help and can we genuinely teach something useful?
      ↓
Yes → Community reply candidate
      ↓
Does it look like a strong commercial-fit problem requiring personal attention?
      ↓
Yes → Private Telegram opportunity alert
```

## Opportunity Scoring Factors

Score 0–100 using factors such as:

- clear business pain
- frequency / recurrence
- business impact
- match with capability profile
- ability to explain a practical solution
- usefulness to other founders
- freshness
- evidence that the person is actively trying to solve the problem
- risk of sounding promotional
- uncertainty about facts or tool capabilities

High score should never mean “auto-sell.” It means the problem is worth better research and teaching.

## Content Research Rule

For possibility-led content such as “what happens when Calendly, a CRM, and an automation layer work together,” the workflow should verify current product capabilities before drafting.

Prefer:
1. official documentation
2. official integration/API documentation
3. current product pages
4. GitHub repositories/documentation when relevant
5. Reddit/community discussion for real-world pain and experience, not as the sole source of technical facts

## Learning Loop

Store every captured problem so the system can later answer:

- Which industries produce the most high-fit problems?
- Which problems recur most often?
- Which tools are repeatedly relevant?
- Which teaching topics earn meaningful discussion?
- Which posts are rejected for being too promotional, too generic, or outside the capability profile?

The research database should become a growing library of real business problems rather than a disposable content feed.
