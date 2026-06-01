# Client Onboarding Automation

## What It Does
This workflow automates onboarding and communication in a loyalty program; turns a first-time guest into a repeat visitor, or a new customer signup into real loyalty.

## Workflow Preview
![Workflow Overview](./workflow-screenshot-n8n-clientOnboarding.png)

## Tools & Integrations
- **n8n** — workflow automation
- **Google Sheets** — store inventory information
- **Google Gemini** — communicates inventory numbers and alerts
- **Jotform** - sets up a form that does basic validation. turns messy human input into structured, usable data
- **Telegram** - makes errors visible and actionable; notifies team instantly of incorrect or incomplete submissions.

## How It Works
1. Trigger: Jotform form accepts loyalty program signups and performs basic validation. 
2. IF node identifies errors or incomplete submissions; Telegram immediately notifies the team and stops the process.
3. If Jotform complete, system adds the client to the CRM with a loyalty program participant status.
4. Sends a welcome message - The client instantly receives a welcome email or message
5. Launches an onboarding message sequence. After scheduled delays, the system:
- Explains how the loyalty program works.
- Sends a PDF, guide, or program rules.
- Reminds the client about bonuses and benefits.
- Updates the client status during onboarding
6. The CRM shows the client’s current stage, from new to in process to completed.
7. Notifies the team - The team is informed about:
- New loyalty program members.
- Data validation errors.
- Successful onboarding completion.

## Use Case / Problem Solved
In a restaurant, client onboarding turns a new guest into a returning one. After signup, the client needs to know:
- How the loyalty program works.
- How they earn points or bonuses.
- What rewards are available.
- When and how they can use them.
If this is unclear, the loyalty program fails. People sign up, then they forget. 

Automated client onboarding is needed to:
- Welcome the guest immediately.
- Explain the rules clearly.
- Send reminders and benefits at the right time.
- Keep the restaurant team informed.

## Files
| File | Description |
|------|-------------|
| `workflow-clientOnboarding.json` | n8n workflow export (import directly into n8n) |
| `workflow-screenshot-n8n-clientOnboarding.png` | Visual overview of the workflow |

## How to Use
1. Download `workflow-clientOnboarding.json`
2. In n8n, go to **Workflows → Import from File**
3. Add your own credentials for GoogleSheets, Jotform, Telegram, and Gemini
4. Activate and test

