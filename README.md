# AI Insurance Claim Processing System

An AI-powered insurance claim processing system with no frontend all requests simulated via Postman. The solution automates the complete insurance claim lifecycle using multiple automation platforms and free services.

## Platforms & Tools
- Postman
- Make.com
- n8n
- Airtable
- Google Drive
- Gmail
- Slack / Discord
- Groq AI
- OCR.Space Free API
- Webhooks

## Data Flow
Postman → Make.com → Airtable → Google Drive → OCR.Space API → Groq AI → n8n → Gmail / Slack (or Discord) → Airtable → Weekly Reports

## Workflows

| # | Workflow | Description | Platform | Live Demo |
|---|----------|-------------|----------|-----------|
| 1 | Claim Submission | Receives claim data from Postman, creates a unique claim record, stores documents, initializes the claim. | Make.com | [View](https://eu1.make.com/public/shared-scenario/56xTk6fi2Kf/workflow-1-claim-submission) |
| 2 | Document Processing | Extracts text using OCR, validates required information, detects missing fields, updates the database. | Make.com | [View](https://eu1.make.com/public/shared-scenario/Tz472AAE3E7/workflow-2-document-processing) |
| 3 | AI Claim Review | Uses AI to summarize the claim, classify claim type, estimate priority, flag suspicious/incomplete claims. | Make.com | [View](https://eu1.make.com/public/shared-scenario/5uA0nRS4Uy7/workflow-3-ai-claim-review) |
| 4 | Claim Status Management | Manages status changes (Under Review, Additional Documents Required, Approved, Rejected, Closed) and notifies relevant parties. | n8n | [JSON](./n8n-workflows/workflow-4-claim-status-management.json) |
| 5 | Scheduled Follow-up | Automatically checks pending claims, sends reminder emails, updates follow-up history. | n8n | [JSON](./n8n-workflows/workflow-5-scheduled-followup.json) |
| 6 | Analytics & Reporting | Generates weekly reports showing claim statistics, processing performance, and AI-generated summaries. | n8n | [JSON](./n8n-workflows/workflow-6-analytics-reporting.json) |

> n8n doesn't support public view-only links, so these 3 workflows are shared as exported workflow JSON files instead — importable directly into any n8n instance via Workflows → Import from File.

## Deliverables
- Complete automation solution
- Minimum six workflows
- Airtable database
- Architecture diagram
- Testing screenshots
- Technical documentation
- Sample reports

## Success Criteria
- End-to-end claim processing
- Integration of multiple automation tools
- Successful OCR extraction
- AI-based claim analysis
- Lifecycle tracking
- Automated follow-ups
- Weekly reporting
- Proper logging and error handling
