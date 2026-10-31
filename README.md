# n8n Automation Portfolio

A collection of workflow automation projects built with **n8n**, integrating AI, Google Sheets, Gmail, web research, and data processing.

> **Security note:** The workflow exports in this repository are sanitized portfolio copies. n8n credential bindings and credential metadata, webhook IDs, workflow-instance metadata, pinned execution data, and Google Sheets document identifiers have been removed or replaced with setup placeholders. Reconnect credentials and configure your own resources after importing. Never commit API keys, OAuth tokens, passwords, or private customer data.

## Projects

| Project | What it does | Main integrations |
|---|---|---|
| [Lead Response](./lead-response/) | Captures and scores incoming leads, drafts a personalized response with AI, sends the email, and updates lead records. | n8n Forms, Google Sheets, OpenAI, Gmail, Slack |
| [Nimzlot Proto](./nimzlot-proto/) | Finds prospects from spreadsheet criteria, enriches company/contact details, scrapes websites, and generates personalized icebreakers. | Google Sheets, Apify, Hunter.io, HTTP Request, HTML extraction, OpenAI |
| [Invoice Follow-up](./invoice-follow-up/) | Reviews invoice age and email history, decides whether a reminder is appropriate, and sends staged follow-ups. | Google Sheets, Gmail, OpenAI |

## Repository structure

```text
n8n-automation-portfolio/
├── README.md
├── .gitignore
├── lead-response/
│   ├── README.md
│   └── lead-response.json
├── nimzlot-proto/
│   ├── README.md
│   └── nimzlot-proto.json
└── invoice-follow-up/
    ├── README.md
    └── invoice-follow-up.json
```

## Importing a workflow

1. Open your n8n instance.
2. Create a new workflow or use the workflow import option.
3. Import the corresponding JSON file.
4. Reconnect each required service using credentials stored securely in n8n.
5. Replace Google Sheets placeholders with your own spreadsheet IDs and verify sheet/tab names and column mappings.
6. Review triggers, schedules, email recipients, and external API settings before activating.
7. Run controlled tests with dummy data before using real customer records.

## Security and responsible use

- Store credentials in n8n's credential manager; do not hard-code secrets in workflow nodes.
- Use environment variables or n8n credentials for private configuration.
- Keep customer names, email addresses, invoice details, and execution data out of public repositories.
- Review AI prompts and outbound messages before enabling automatic sending.
- Apply rate limits and comply with applicable privacy, email, and website terms.
- The sanitized exports are templates: credential reconnection and resource configuration are required before they can run.

## Status

These files document the exported workflow configuration. They are not a guarantee that third-party services, credentials, external APIs, or live execution are currently available.
