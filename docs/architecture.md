# System Architecture

## Overview

The AI Recruitment & Hiring Automation system is an end-to-end workflow built with n8n that automates the candidate screening and interview scheduling process using AI and Google Workspace integrations.

The workflow receives candidate applications, extracts resume information, evaluates candidates using a Large Language Model (LLM), schedules interviews for qualified candidates, generates professional evaluation reports, and notifies the HR team automatically.

---

## Architecture Diagram

![System Architecture](../assets/architecture.png)

---

## High-Level Workflow

```
Candidate
    │
    ▼
Receive Application (Webhook)
    │
    ▼
Upload Resume to Google Drive
    │
    ▼
Extract Resume Text
    │
    ▼
Prepare Candidate Data
    │
    ▼
AI HR Agent (Groq LLM)
    │
    ▼
Parse AI Response
    │
    ▼
Candidate Qualified?
   ├───────────────┐
   │               │
 YES             NO
   │               │
   ▼               ▼
Create Interview   Save Candidate
Event              as Rejected
   │               │
   ▼               ▼
Send Interview     Send Rejection
Email              Email
   │
   ▼
Generate HTML Report
   │
   ▼
Generate PDF Report
   │
   ▼
Upload Report
   │
   ▼
Share Report
   │
   ▼
Notify HR
```

---

# System Components

## Candidate Submission

Candidates submit their application and resume through a webhook endpoint.

---

## Resume Processing

The uploaded resume is stored in Google Drive and its content is extracted from the PDF.

---

## Candidate Data Preparation

Candidate information and extracted resume text are combined into a structured format before being sent to the AI model.

---

## AI Candidate Evaluation

The Groq LLM analyzes the candidate's:

- Technical skills
- Soft skills
- Experience
- Education
- Strengths
- Weaknesses
- Seniority level
- Interview recommendation
- Suggested interview questions

---

## Decision Engine

The AI recommendation determines whether the candidate should proceed to the interview stage.

### Qualified Candidate

- Save to CRM
- Create Google Calendar event
- Send interview invitation
- Generate evaluation report
- Notify HR

### Rejected Candidate

- Save rejection status
- Send rejection email

---

## Reporting

A professional HTML report is generated and converted into a PDF document.

The report is uploaded to Google Drive and shared with HR.

---

## Notification

The HR team receives a notification containing the candidate evaluation report and interview status.

---

# Technologies Used

- n8n
- Groq LLM
- Google Drive
- Google Sheets
- Gmail
- Google Calendar
- PDFShift API
- JavaScript
- Webhooks

---

# Benefits

- Faster candidate screening
- Reduced manual effort
- Consistent AI evaluations
- Automated interview scheduling
- Professional PDF reports
- Centralized candidate management