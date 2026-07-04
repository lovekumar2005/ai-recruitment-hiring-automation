# Customization Guide

This workflow is fully modular and can be customized to fit different recruitment processes and business requirements.

---

# AI Model

The workflow currently uses **Groq LLM**.

You can replace it with:

- OpenAI
- Anthropic Claude
- Google Gemini
- Azure OpenAI
- Ollama (Self-hosted)

No major workflow changes are required.

---

# Candidate Evaluation

Modify the AI HR Agent prompt to change:

- Evaluation criteria
- Scoring system
- Hiring recommendation rules
- Seniority levels
- Interview questions

The prompt can be found in:

```
prompts/ai-hr-agent.md
```

---

# Email Templates

Interview and rejection emails can be customized.

You can modify:

- Subject lines
- Company branding
- Meeting instructions
- Signature
- Tone of communication

Templates are located in:

```
prompts/email-templates.md
```

---

# Report Design

The generated report can be customized by editing the HTML prompt.

You can change:

- Colors
- Company logo
- Fonts
- Layout
- Tables
- Branding
- Footer

Prompt location:

```
prompts/html-report-generator.md
```

---

# Google Sheets CRM

Add or remove columns depending on your hiring process.

Examples:

- Salary Expectation
- Current Location
- Notice Period
- Recruiter Name
- Hiring Manager
- Department
- Interview Stage
- Candidate Source

---

# Google Drive

Change folder structure to match your organization.

Example:

```
Recruitment/

├── Resumes

├── Reports

├── Offer Letters

└── Archived Candidates
```

---

# Calendar

Modify interview events by adding:

- Google Meet link
- Office location
- Interview duration
- Multiple interviewers
- Notes

---

# HR Notification

Currently, HR receives an email notification.

You can easily replace or extend this with:

- Slack
- Microsoft Teams
- Discord
- WhatsApp
- Telegram

---

# Additional Integrations

This workflow can be expanded with:

- LinkedIn
- Greenhouse ATS
- Lever ATS
- BambooHR
- HubSpot CRM
- Salesforce
- Airtable
- Notion
- Microsoft Outlook

---

# Additional AI Features

Possible enhancements include:

- Resume ranking
- Duplicate candidate detection
- Skill matching
- Job description matching
- Candidate comparison
- AI interview feedback
- AI cover letter analysis
- Salary prediction

---

# Dashboard

Connect the workflow to a BI platform for analytics.

Recommended options:

- Looker Studio
- Power BI
- Tableau
- Metabase

Possible metrics include:

- Applications received
- Interview rate
- Rejection rate
- Hiring rate
- Average candidate score
- Average processing time

---

# Security

For production environments, consider implementing:

- Role-based access control
- Secure credential management
- Audit logs
- API rate limiting
- Encrypted storage
- Data retention policies

---

# Scaling

This workflow is designed to be scalable.

It can process:

- Single candidate applications
- Batch candidate imports
- Multi-position hiring campaigns
- Multiple recruiters
- Multiple departments

---

# Future Improvements

Potential future enhancements include:

- Multi-language resume support
- OCR for scanned resumes
- Voice interview scheduling
- AI interview chatbot
- Candidate portal
- Recruiter dashboard
- Mobile notifications
- Analytics dashboard
- ATS synchronization

---

# Contribution

Feel free to fork this repository and adapt the workflow to meet your organization's recruitment process. Pull requests, improvements, and suggestions are always welcome.