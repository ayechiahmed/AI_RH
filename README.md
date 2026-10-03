# AI HR Recruitment Assistant

An AI-powered recruitment automation workflow built with **n8n, Google Gemini, Gmail, Google Sheets, Google Drive, and Notion**.

The system automates the repetitive parts of a recruitment pipeline — from receiving applications and extracting CV information to evaluating candidates against job requirements, updating the ATS, notifying HR, and initiating interview scheduling.

---

## 🚀 Overview

Traditional recruitment workflows require HR teams to manually:

- Read incoming applications
- Identify recruitment emails
- Extract candidate information
- Download and read CVs
- Compare candidates with job requirements
- Update candidate records
- Notify recruiters
- Contact candidates
- Handle duplicate applications
- Track errors

This workflow turns those repetitive steps into an automated AI-assisted recruitment pipeline.

### Workflow

```text
Candidate Application
        ↓
      Gmail
        ↓
  AI Email Classification
        ↓
 Recruitment Application?
     ↙          ↘
   No            Yes
   ↓              ↓
 Ignore       Candidate Processing
                  ↓
          Duplicate Detection
                  ↓
          Send Acknowledgement
                  ↓
             CV Detection
             ↙         ↘
          No CV        CV Found
            ↓             ↓
       Request CV      Extract CV
                          ↓
                  Structure Candidate Data
                          ↓
                  Match Job Requirements
                          ↓
                    AI Candidate Evaluation
                          ↓
                    Build Candidate Record
                          ↓
              ┌───────────┼───────────┐
              ↓           ↓           ↓
           Strong       Medium        Low
              ↓           ↓           ↓
         Interview      HR Review   HR Review /
          Process                    Rejection
              ↓
        HR Notification
              ↓
        ATS + Notion Update
