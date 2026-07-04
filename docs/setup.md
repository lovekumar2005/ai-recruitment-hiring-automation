# Setup Guide

This guide explains how to configure and run the AI Recruitment & Hiring Automation workflow in n8n.

---

# Prerequisites

Before importing the workflow, ensure you have access to the following services:

- n8n (Cloud or Self-Hosted)
- Groq API Key
- Google Account
- Google Drive API
- Google Sheets API
- Google Calendar API
- Gmail API
- PDFShift API Key

---

# Project Structure

```
AI-Recruitment-Hiring-Automation/

├── workflow/
├── docs/
├── prompts/
├── assets/
└── examples/
```

---

# Step 1 — Import the Workflow

1. Open your n8n workspace.
2. Click **Import Workflow**.
3. Select:

```
workflow/AI Recruitment & Hiring Automation.json
```

4. Save the workflow.

---

# Step 2 — Configure Credentials

The workflow uses several external services. Create the following credentials inside n8n.

## Google Drive

Used for:

- Uploading resumes
- Uploading reports
- Sharing reports

---

## Google Sheets

Used as the Candidate CRM.

Stores:

- Candidate Name
- Email
- Position
- AI Score
- Recommendation
- Interview Status

---

## Gmail

Used for:

- Interview invitations
- Rejection emails
- HR notifications

---

## Google Calendar

Used for creating interview events automatically.

---

## Groq

Create an HTTP credential using your Groq API key.

This service performs:

- Resume analysis
- Candidate scoring
- Skills extraction
- Hiring recommendation

---

## PDFShift

Used for converting HTML reports into PDF documents.

---

# Step 3 — Configure Google Resources

Create the following resources in your Google account.

### Google Drive Folder

Recommended folders:

```
Recruitment/

    ├── Resumes/

    └── Reports/
```

---

### Google Sheet

Create a sheet for candidate tracking.

Recommended columns:

- Candidate Name
- Email
- Position
- Overall Score
- Rating
- Category
- Recommendation
- Interview Status
- Resume Link
- Report Link

---

### Google Calendar

Create a dedicated interview calendar.

Example:

```
Recruitment Interviews
```

---

# Step 4 — Update Workflow Settings

Update any IDs inside the workflow if necessary.

Examples include:

- Google Drive Folder IDs
- Google Sheet ID
- Calendar ID
- Email addresses

---

# Step 5 — Test the Workflow

Trigger the webhook by submitting a candidate application.

The workflow should automatically:

- Upload the resume
- Extract resume text
- Analyze the candidate
- Store candidate information
- Schedule an interview (if qualified)
- Send email
- Generate report
- Upload report
- Notify HR

---

# Expected Workflow Output

For qualified candidates:

- Resume uploaded
- Candidate evaluated
- Google Sheet updated
- Calendar event created
- Interview email sent
- PDF report generated
- HR notified

For rejected candidates:

- Candidate stored
- Rejection email sent

---

# Troubleshooting

## AI Response Error

Verify:

- Groq API Key
- Prompt configuration
- JSON parsing

---

## Gmail Errors

Verify:

- Gmail credentials
- OAuth permissions

---

## Google Drive Errors

Verify:

- Folder permissions
- Folder IDs

---

## Google Calendar Errors

Verify:

- Calendar ID
- OAuth permissions

---

## PDF Generation Issues

Verify:

- PDFShift API key
- HTML generation

---

# Support

If you encounter configuration issues, review each integration inside the workflow and ensure all required credentials are correctly connected before execution.