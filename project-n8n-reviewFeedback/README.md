# Reviews and Feedback Automation

## What It Does
AI-powered feedback automation system using n8n and Google Gemini to find online reviews and structure them for proper notification and feedback. 

## Workflow Preview
![Workflow Overview](./workflow-screenshot.png)

## Tools & Integrations
- **n8n** — workflow automation
- **Google Sheets and Gemini** — information storage and routing
- **HTTP Request Webhook** - Sets up API key and auth credentials to update database with web data

## How It Works
1. An HTTP Request scrapes reviews from Google Maps
2. Any new reviews for the target create a new row added to Google Sheets
3. The workflow analyzes the customer’s feedback, classifies it by category (question, problem, suggestion) and area (kitchen, delivery, service), then updates the sheet automatically. 
4. Based on classification, the system routes notifications to the appropriate department via Gmail.

## Use Case / Problem Solved
Enables a business to immediately see feedback concerning their products or services and routes that feedback to the departments accountable for improving those services or products.

## Files
| File | Description |
|------|-------------|
| `workflow-feedback.json` | n8n workflow export (import directly into n8n) |
| `workflow-screenshot-n8n-feedback.png` | Visual overview of the workflow |

## How to Use
1. Download `workflow-feedback.json`
2. In n8n, go to **Workflows → Import from File**
3. Add your own credentials for Google Gemini, HTTP Request and Google Sheets
4. Activate and test
