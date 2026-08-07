# n8n Workflows

This folder contains importable workflow JSON for the Reddit Business Intelligence & Teaching Engine.

## Version 1 Philosophy

Do not start by automating Reddit publishing.

First prove this core chain:

```text
Manual sample problem
    -> read Notion System Knowledge
    -> OpenAI diagnosis + teaching draft
    -> create Notion Content Intelligence record
    -> Telegram review message
```

Once that works reliably, add Reddit ingestion. Publishing remains human-controlled until the research and community-rule checks are stable.

## Workflow 01 — Core Brain Test

File: `01-core-brain-test.json`

Purpose:

1. Start manually.
2. Inject a sample founder problem.
3. Read runtime knowledge from the Notion `System Knowledge` database.
4. Build a compact context for OpenAI.
5. Ask OpenAI for structured business-first analysis and a teaching draft.
6. Parse the response.
7. Create a record in Notion `Content Intelligence`.
8. Send a Telegram review card.

## Runtime Notion IDs

- System Knowledge data source: `9fe295cd-2a1b-4079-8ce1-a96b614fd0cb`
- Content Intelligence data source: `ec1117e5-22de-419e-843f-bc9bcd5a5df8`

The workflow also includes the Notion database page IDs in its notes where useful.

## Credentials Required in n8n

After import, choose/create these credentials in the relevant nodes:

### Notion

Create a Notion integration and give it access to the project foundation page and both child databases.

Select the Notion credential in:

- `Read System Knowledge`
- `Create Content Record`

### OpenAI

Select your OpenAI credential in `OpenAI Business Diagnosis`.

The workflow is designed so the model can be changed without changing the business logic. Start with a cost-conscious model for testing.

### Telegram

Create a Telegram bot with BotFather, add its token as a Telegram credential in n8n, then set your private chat ID in `Send Telegram Review`.

## Import

In n8n:

1. Create/Open a workflow.
2. Use **Import from File** and upload `01-core-brain-test.json`, or use **Import from URL** with the raw GitHub URL.
3. Open every credential-warning node and select the correct credential.
4. Set your Telegram chat ID.
5. Inspect the Notion property mapping in `Create Content Record` because n8n may refresh the database schema after your credential is selected.
6. Run the workflow manually.

## Expected Test

Sample problem:

> Our team gets leads from several places, but staff keep forgetting who needs another follow-up and some interested prospects disappear.

Expected outcome:

- OpenAI identifies the real problem as a follow-up/next-action process issue rather than merely “not enough leads.”
- A new item is created in Content Intelligence.
- Telegram receives an educational opportunity card with diagnosis, impact, teaching angle, draft, and diagram idea.

## Important Compatibility Note

n8n node schemas can change between versions. The JSON is a **Version 1 importable skeleton** with live Notion database IDs but no secrets. After import, n8n may ask you to re-select resources or refresh fields, especially in the Notion Create node. Do that in the editor rather than adding secrets to GitHub.

## Secrets Policy

Never commit:

- Notion integration secret
- OpenAI API key
- Telegram bot token
- Reddit credentials

Credentials stay only inside your self-hosted n8n Credentials/environment.
