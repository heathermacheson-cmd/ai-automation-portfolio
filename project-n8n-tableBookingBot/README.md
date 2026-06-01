# Restaurant Table Booking Bot

## What It Does
AI-powered restaurant booking automation using n8n and Google Gemini. Customers can book a table by sending their name, date, time, and number of guests in chat. The AI agent extracts the data, checks availability in Google Sheets, prevents double bookings, and confirms reservations automatically.

The system ensures bookings are only added if the time slot is available and never overwrites existing reservations.

## Workflow Preview
![Workflow Overview](./workflow-screenshot.png)

## Tools & Integrations
- Chat trigger
- AI Agent
- Google Gemini model
- Memory buffer
- Google Sheets integration

## How It Works
1. Trigger: chat trigger causes Gemini AI Agent to ask and answer questions during booking
2. AI Agent requests name, date, time, and number of guests in chat.
3. AI Agent extracts the data, checks availability in Google Sheets
4. AI Agent and Memory Buffer prevent double bookings and confirm reservations automatically.
5. Reservation data is stored in Google Sheets

## Use Case / Problem Solved
Automates restaurant booking through chats and reduces opportunity for human error.

## Files
| File | Description |
|------|-------------|
| `workflow-tableBookingBot.json` | n8n workflow export (import directly into n8n) |
| `workflow-screenshot-n8n-tableBookingBot.png` | Visual overview of the workflow |

## How to Use
1. Download `workflow-tableBookingBot.json`
2. In n8n, go to **Workflows → Import from File**
3. Add your own credentials for GoogleSheets and Gemini
4. Activate and test
