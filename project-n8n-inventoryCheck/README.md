# Inventory Check

## What It Does
Automated inventory monitoring system using n8n, Google Sheets, and Google Gemini. 

## Workflow Preview
![Workflow Overview](./workflow-screenshot-n8n-inventoryCheck.png)

## Tools & Integrations
- **n8n** — workflow automation
- **Google Sheets** — store inventory information
- **Google Gemini** — communicates inventory numbers and alerts

## How It Works
The workflow runs weekly, checks stock levels against predefined thresholds, and detects low-stock items automatically. 
When inventory falls below the limit, the system aggregates affected products and sends a structured alert via Gmail. 

## Use Case / Problem Solved
This automation prevents stockouts, reduces manual checks, and improves purchasing efficiency.

## Files
| File | Description |
|------|-------------|
| `workflow-inventoryCheck.json` | n8n workflow export (import directly into n8n) |
| `workflow-screenshot-n8n-inventoryCheck.png` | Visual overview of the workflow |

## How to Use
1. Download `workflow-inventoryCheck.json`
2. In n8n, go to **Workflows → Import from File**
3. Add your own credentials for Gemini and Gmail
4. Activate and test
