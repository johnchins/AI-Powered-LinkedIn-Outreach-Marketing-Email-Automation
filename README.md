# AI-Powered-LinkedIn-Outreach-Marketing-Email-Automation
![Workflow](https://github.com/user-attachments/assets/4a681665-01b6-4124-b9be-c598e99128bc)


## 📌 Project Overview

This project is a fully automated **AI-powered LinkedIn prospecting and personalized outreach system** built using:

- **n8n** (workflow automation)
- **Apify (Playwright Adaptive)** for dynamic scraping
- **OpenAI (GPT-4o-mini)** for AI-generated emails
- **Telegram Bot API** as a conversational interface
- **Google Sheets API** for lead logging

It enables:

1. Submission of a service offering via Telegram  
2. Input of a LinkedIn profile URL  
3. Automated scraping of public profile metadata  
4. AI-generated personalized marketing email  
5. Human approval before logging  
6. Automatic logging into Google Sheets  

This demonstrates real-world applications of:

- AI workflow orchestration  
- Prompt engineering  
- Web scraping automation  
- Conversational bots  
- Human-in-the-loop AI systems  
- Lead management pipelines  
- Structured data transformation  

---

## 🏗 Workflow Architecture

### 🔄 High-Level System Flow

```
User (Telegram)
      ↓
Telegram Trigger (n8n)
      ↓
Collect Service Offering
      ↓
Collect LinkedIn URL
      ↓
Apify Scraper (Playwright Adaptive)
      ↓
Extract Profile Metadata
      ↓
OpenAI GPT Email Generator
      ↓
Send Draft for Approval (Telegram)
      ↓
IF Confirmed
      ↓
Log to Google Sheets
      ↓
Success Notification
```

---

## 🧠 Core Components Breakdown

### 1️⃣ Telegram Bot Interface

Acts as the conversational entry point.

Collects:
- Business offering
- LinkedIn prospect URL

Sends:
- Draft email for confirmation
- Success/cancellation feedback
---

### 2️⃣ LinkedIn Scraping via Apify

Uses:

- Apify node  
- `playwright:adaptive` crawler  

Extracted Data:
- Profile Name  
- Headline  
- About section  
- Public email (if available)  

---

### 3️⃣ AI Email Generation (OpenAI)

Model:
- `gpt-4o-mini`

Prompt includes:
- Prospect profile data
- Service offering
- Personalization instructions
- 200–300 word constraint
- Professional tone
- Clear CTA
- Structured sign-off

Output:
- Human-like personalized email
- Context-aware content
- Use-case-driven messaging

---

### 4️⃣ Human-in-the-Loop Approval Gate

Before logging:

User must reply **"confirm"**

If confirmed:
→ Logs to Google Sheets

If canceled:
→ Workflow stops safely

---

### 5️⃣ Google Sheets Logging

Stored Fields:
- Profile Name
- Profile Link
- Profile Description
- Drafted Email
- Timestamp

Use Cases:
- CRM-lite tracking
- Outreach monitoring
- Lead database creation

---

## 📊 Real-World Applications

- B2B lead generation
- Recruitment prospecting
- Sales automation
- Agency outreach
- AI-powered cold email systems
- CRM pre-processing
- Marketing automation pipelines

---

## 📈 Business Value

This system enables:

- ⚡ Faster outreach creation
- 🎯 High personalization at scale
- 🧠 AI-assisted prospect targeting
- 📋 Structured outreach logging
- 🤖 Reduced manual drafting
- 🔁 Repeatable workflow system

---

## 🔐 Production-Level Considerations

- Human approval checkpoint
- Replaceable AI model layer
- Modular scraping architecture
- Structured data mapping
- Error-safe branching
- Controlled AI output variability

---
