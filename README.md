# AutoBugTracer – AI-Powered Bug Tracker & Hotfix Recommender

> Built during #KestraHackWeek with 💙 by Geetha pranay

AutoBugTracer is an AI-enhanced DevOps assistant that:
- Traces bugs to their originating commits using logs & GitHub issues
- Suggests GPT-4-powered patches
- Auto-generates hotfix PRs
- Posts daily reports to Slack

## Use Case
Save developer time and reduce MTTR by automatically:
- Linking logs ↔ issues ↔ commits
- Recommending fixes based on prior patterns
- Reducing context switching for OSS maintainers

## How It Works

1. **Ingests GitHub commits, issues, and logs daily**
2. **GPT-4** identifies correlations between logs and bugs
3. **Auto-suggests patches** and creates PRs if fixable
4. **Sends reports** to Slack for human review

## Tech Stack
- [Kestra](https://kestra.io) – Workflow orchestration
- OpenAI GPT-4 – AI analysis & patch generation
- GitHub API – Issue + PR management
- Slack API – Notifications
- AWS S3 / ELK – Log ingestion

## Setup

1. Add these secrets:
   - `GITHUB_TOKEN`
   - `OPENAI_API_KEY`
   - `AWS_KEY`, `AWS_SECRET`
   - `SLACK_TOKEN`

2. Deploy the `flow.yaml` via Kestra UI or CLI.

3. Schedule runs or trigger on-demand.


## Maintainer Notes

- The GPT prompt is fully editable
- Can be extended to monorepos or multi-env support
- Logs can be pulled from any log backend (e.g., Datadog, S3, ELK)

---

🧹 From bug chaos to clarity — one flow at a time.
