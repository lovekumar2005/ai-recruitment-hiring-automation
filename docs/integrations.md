# Integrations

This workflow integrates multiple cloud services to automate the complete recruitment process.

---

# Groq LLM

## Purpose

Performs AI-powered candidate evaluation.

## Responsibilities

- Resume analysis
- Candidate scoring
- Skills extraction
- Experience evaluation
- Hiring recommendation
- Interview questions

---

# Google Drive

## Purpose

Stores all recruitment documents.

## Files Stored

- Uploaded resumes
- Generated PDF reports

---

# Google Sheets

## Purpose

Acts as the Candidate CRM.

## Data Stored

- Candidate Name
- Email
- Position
- AI Score
- Recommendation
- Interview Status
- Resume Link
- Report Link

---

# Gmail

## Purpose

Automates candidate communication.

### Emails Sent

- Interview invitation
- Rejection email
- HR notification

---

# Google Calendar

## Purpose

Automatically schedules interviews.

The event includes:

- Candidate name
- Interview date
- Time
- Meeting details

---

# PDFShift API

## Purpose

Converts HTML reports into professionally formatted PDF documents.

---

# Webhook

## Purpose

Receives candidate applications.

The webhook accepts:

- Candidate details
- Resume upload

---

# JavaScript

## Purpose

Transforms workflow data between automation steps.

Used for:

- Formatting AI output
- Preparing HTML
- Processing JSON

---

# n8n

## Purpose

Acts as the workflow orchestration platform.

Responsibilities include:

- Automation
- Data routing
- API communication
- Decision making
- Scheduling
- Error handling

---

# Integration Summary

| Service | Purpose |
|----------|---------|
| n8n | Workflow Automation |
| Groq | AI Candidate Evaluation |
| Google Drive | File Storage |
| Google Sheets | Candidate CRM |
| Gmail | Email Automation |
| Google Calendar | Interview Scheduling |
| PDFShift | PDF Generation |
| JavaScript | Data Transformation |
| Webhook | Candidate Submission |

---

# Benefits

- Fully automated recruitment pipeline
- Centralized candidate data
- Reduced manual work
- Faster hiring decisions
- Professional candidate reports
- Seamless Google Workspace integration