# Cold Email Outreach Workflow for n8n

This n8n workflow automates sending cold emails using Gmail and Google Sheets.

---

## Features
- Reads a list of recipients from Google Sheets.
- Checks if emails were already sent.
- Sends personalized emails using templates.
- Updates Google Sheets with the status and timestamp.

---

## Setup

1. **Import the workflow**
   - Open n8n → Workflows → Import → Upload `COLD_EMAIL_OUTREACH.json`.

2. **Add your credentials**
   - Google Sheets OAuth2
   - Gmail OAuth2

3. **Replace placeholders**
   - `YOUR_GOOGLE_SHEET_ID` → Your Google Sheet ID.
   - `YOUR_NAME` → Your name for email sender.

4. **Prepare your Google Sheets**
   - Sheet1: Email list with columns `Email`, `Status`, `Owner / Manager`, `Business Name`.
   - Sheet2: Email templates with columns `Subject`, `Body`.

5. **Execution**
   - Click **Execute workflow** in n8n.
   - The workflow will loop over your recipients and send emails.

---

## Notes
- Ensure Gmail account has **"less secure apps" enabled or OAuth2 set up**.
- Adjust batch size in "Loop Over Items" node if sending large volumes.
- Test workflow with a small list before running full campaigns.
