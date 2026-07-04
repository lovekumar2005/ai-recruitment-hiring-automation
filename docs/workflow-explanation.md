# Workflow Explanation

This document explains every node used in the workflow.

---

# 1. Receive Candidate Application

**Purpose**

Receives candidate information and resume through a Webhook.

**Output**

- Candidate details
- Resume file

---

# 2. Upload File

**Purpose**

Uploads the candidate's resume to Google Drive for secure storage.

**Output**

- Google Drive File ID
- Resume URL

---

# 3. Extract Resume From PDF

**Purpose**

Extracts text from the uploaded PDF resume.

**Output**

- Resume text

---

# 4. Prepare Candidate Data

**Purpose**

Combines candidate information with extracted resume text into a structured format.

**Output**

Formatted data ready for AI analysis.

---

# 5. Merge

**Purpose**

Combines multiple data streams before sending them to the AI Agent.

---

# 6. AI HR Agent

**Purpose**

Analyzes the candidate using Groq LLM.

The AI performs:

- Resume analysis
- Skills extraction
- Experience evaluation
- Education analysis
- Candidate scoring
- Hiring recommendation
- Interview question generation

---

# 7. Parse AI Response

**Purpose**

Parses the JSON response returned by the AI model into structured fields.

---

# 8. Decision (IF Node)

**Purpose**

Determines whether the candidate is recommended for an interview.

### TRUE

Proceed with interview workflow.

### FALSE

Send rejection email.

---

# 9. Save Candidate in CRM

**Purpose**

Stores candidate information in Google Sheets.

Information stored includes:

- Name
- Email
- Position
- AI Score
- Status

---

# 10. Create Interview Event

**Purpose**

Creates a Google Calendar event for the interview.

---

# 11. Send Interview Email

**Purpose**

Automatically emails the candidate with interview details.

---

# 12. Generate HTML Report

**Purpose**

Creates a professional HTML report summarizing the AI evaluation.

---

# 13. JavaScript Node

**Purpose**

Processes and formats the generated HTML before PDF conversion.

---

# 14. Generate PDF

**Purpose**

Converts the HTML report into a PDF using PDFShift API.

---

# 15. Upload Report

**Purpose**

Uploads the generated PDF to Google Drive.

---

# 16. Share Report

**Purpose**

Creates a shareable Google Drive link.

---

# 17. Notify HR

**Purpose**

Sends the report link and candidate summary to HR.

---

# Rejection Path

If the candidate is not recommended:

- Save candidate status
- Send rejection email
- End workflow

---

# Final Outcome

For qualified candidates:

- Candidate stored
- Interview scheduled
- Email sent
- PDF generated
- HR notified

For rejected candidates:

- Candidate stored
- Rejection email sent