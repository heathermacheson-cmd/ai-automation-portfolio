# Real Estate Call Automation

## What It Does


## Workflow Preview
![Workflow Overview](./workflow-screenshot-n8n-automateRealEstateCalls.png)

## Tools & Integrations
- **n8n** — workflow automation
- **Google Sheets** — store inventory information
- **Google Gemini** — communicates inventory numbers and alerts
- **HubSpot** - acts as a CRM
- **Jotform** - sets up a form that does basic validation. turns messy human input into structured, usable data
- **Telegram** - makes errors visible and actionable; notifies team instantly of incorrect or incomplete submissions.

## How It Works

### Trigger: Workflow 1 – Live Call Logic 
1. Webhook receives data from ElevenLabs during the call.
2. IF node checks:
- If user wants to sell → go to Seller path
- Otherwise → Buyer path

#### Seller Path
- Create property in Airtable
- Send team notification via Gmail
- Respond to Webhook (AI confirms to caller)

#### Buyer Path
- AI Agent (Gemini) analyzes request
- Uses Airtable tool to search properties
- Returns availability result
- Respond to Webhook (AI speaks answer)

### Workflow 2 – Post-Call Logging
1. Webhook 2 triggers when call ends 
2. Saves call data (cost, etc.) to Airtable

## Use Case / Problem Solved



## Files
| File | Description |
|------|-------------|
| `workflow-automateRealEstateCalls.json` | n8n workflow export (import directly into n8n) |
| `workflow-screenshot-n8n-automateRealEstateCalls.png` | Visual overview of the workflow |

## How to Use
1. Download `workflow-automateRealEstateCalls.json`
2. In n8n, go to **Workflows → Import from File**
3. Add your own credentials for GoogleSheets, Jotform, Telegram, and Gemini
4. Activate and test


