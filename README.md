# AI-Automation-project-1
# 🤖 AI-Powered Sales Analyzer — n8n Automation

An intelligent automation workflow built with **n8n** that automatically analyzes sales data from Google Sheets using **Gemini AI** and writes insights back to the sheet — fully automated, zero manual work!

---

## 🚀 Project Overview

This workflow monitors a Google Sheet for new sales entries, sends the data to Google Gemini AI for analysis, and writes AI-generated insights and recommendations directly back into the sheet.

---

## 📸 Workflow Preview

<img width="1264" height="490" alt="Screenshot 2026-07-03 104754" src="https://github.com/user-attachments/assets/8b9cf58c-e9de-4c6e-8f48-868481f51d7f" />


---

## ⚙️ Workflow Nodes

```
Google Sheets Trigger
        ↓
Edit Fields (Prompt Builder)
        ↓
Gemini AI (Message a Model)
        ↓
Google Sheets (Append/Update Row)
```

| Node | Tool | Purpose |
|------|------|---------|
| 1 | Google Sheets Trigger | Detects new row added |
| 2 | Edit Fields | Builds AI prompt from row data |
| 3 | Gemini AI | Analyzes data & generates insights |
| 4 | Google Sheets | Writes AI insight back to sheet |

---

## 🛠️ Tools & Technologies

- **n8n** — Workflow automation platform
- **Google Sheets** — Data input & output
- **Google Gemini AI API** — AI analysis engine (free tier)
- **HTTP Request Node** — API communication

---

## 📋 Google Sheet Structure

| Column | Description |
|--------|-------------|
| Product | Product name (e.g. Laptop) |
| Region | Sales region (e.g. North) |
| Month | Month of sale (e.g. January) |
| Revenue | Revenue amount (e.g. 50000) |
| AI Insight | ← AI fills this automatically ✅ |

---

## 🔧 Setup Instructions

### 1. Import Workflow
- Download the `workflow.json` file from this repo
- Open n8n → **Import from File** → select `workflow.json`

### 2. Connect Google Sheets
- In n8n, go to **Credentials**
- Add **Google Sheets OAuth2** credential
- Connect your Google account

### 3. Get Gemini API Key
- Go to → [aistudio.google.com](https://aistudio.google.com)
- Click **"Get API Key"**
- Copy your free API key

### 4. Activate Workflow
- Click the **Toggle** in n8n to activate
- Add a new row to Google Sheet
- Watch AI fill the Insight column automatically! 🎉

---

## ✅ Features

- 🔄 Fully automated — no manual triggers needed
- 🤖 AI-generated insights for every sales entry
- 📊 Works with any Google Sheet
- 💰 100% free (Google Gemini free tier)
- ⚡ Real-time processing on new row addition

---

## 🌱 Future Improvements

- [ ] Add email notification with insights
- [ ] Weekly automated report generation
- [ ] Dashboard with charts using Google Looker Studio
- [ ] Multi-sheet support

---



